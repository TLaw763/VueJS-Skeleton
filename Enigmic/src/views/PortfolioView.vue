<template>
  <div class="portfolio">
    <div class="container">
      <div class="text-center top-heading">
        <h1><strong>Our Work</strong></h1>
        <h5>Click on any of the cards below to check out the work we have done.</h5>
      </div>
      <div class="row">
        <div class="col-md-3">
          <div class="portfolio-card text-center">
            <!--Link to the portfolio pice-->
            <a href="">
              <img src="src/assets/img/Blork.png" alt="">
              <h4>Blork</h4>
              <div class="row">
                <img src="src/assets/img/Wordpress-icon.png" alt="" class="coding-tool">
              </div>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .portfolio {
    min-height: 100vh;
    display: flex;
    align-items: center;
    margin-top: -108px
  }
}

.portfolio-card {
  background: #333;
  border-radius: 25px;
  padding: 1rem;
}

.portfolio-card img {
  width: 90%;
  padding: 1.5rem;
  background-color: #ababab;
  border-radius: 25px;
}

.portfolio-card a h4 {
  color: #fff;
  font-weight: 700;
  margin: 2rem;
}

.portfolio-card a {
  text-decoration: none;
}

.coding-tool {
  max-width: 32%;
  background-color: #333 !important;
  padding: 0.1rem;
}

.top-heading {
  margin: 3rem 0;
}
</style>
