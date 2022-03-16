<template>
  <div class="contact">
    <div class="container">
      <div class="row">
        <div class="col-md-4">
          <h2>Let's get In Touch</h2>
        </div>
        <form class="col-md-8">
          <input 
            type="text" 
            v-model="name"
            name="name"
            placeholder="Your Name"
          >
          <input 
            type="email" 
            v-model="email"
            name="email"
            placeholder="Your Email Address"
            >
            <input 
            type="text" 
            v-model="subject"
            name="subject"
            placeholder="Your Project"
          >
          <textarea 
            name="message"
            v-model="message"
            cols="30" rows="7"
            placeholder="What would you like to say?">
          </textarea>
          
          <input type="submit" value="Send" class="submit-button">
        </form>
      </div>
    </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .contact {
    min-height: 100vh;
    display: flex;
    align-items: center;
    margin-top: -108px
  }

  form {
    margin-top: 100px;
  }
  input, textarea {
    width: 100%;
    margin: 0.75rem 0;
    padding: 1rem 1rem;
    line-height: 1.5rem;
    border-radius: 25px;
    background-color: rgba(116,65,255,0.1);
    border: 0 solid #000;
  }
  input.submit-button {
    font-weight: 700;
    display: block;
    margin: 0 auto;
    width: 33.333% !important;
    color: #fff;
    background-color: #2FCCDE;
  }
  input.submit-button:hover {
    background-color: #aa45f8;
  }
}

h2 {
  font-weight: 700;
}
</style>

<script>
import emailjs from 'emailjs-com';
export default {
  name: "App",
  data() {
    return {
      name: "",
      email: "",
      subject: "",
      message: "",
    };


  },
  computed: {
    formValid() {
      const { name, email, message } = this;
      return (
        name.length > 0 &&
        /(.+)@(.+){2,}.(.+){2,}/.test(email) &&
        message.length > 0
      );
    },
  },
  methods: {
    sendEmail(e) {
      try {
        emailjs.sendForm('service_b9h1d0c', 'template_sqyc5z6', e.target,
        'YOUR_USER_ID', {
          name: this.name,
          email: this.email,
          subject: this.subject,
          message: this.message
        })

      } catch(error) {
          console.log({error})
      }
      // Reset form field
      this.name = ''
      this.email = ''
      this.message = ''
    },
  },
};
</script>