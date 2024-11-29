<script setup>

</script>

<template>
  <section class="portfolio">
    <div class="container">
      <div class="portfolio-title">
        <h2 class="title-1">Portfolio</h2>
      </div>
      <div class="project" data-aos="flip-up">
        <img src="@/assets/img/portfolio/01.jpg" alt="Online fashion store" class="project-img">
        <h3 class="project-title"><a href="#!">Online fashion store - Homepage</a></h3>
      </div>

      <div class="project" data-aos="flip-up">
        <img src="@/assets/img/portfolio/02.jpg" alt="Reebok Store" class="project-img">
        <h3 class="project-title"><a href="#!">Reebok Store - Concept</a></h3>
      </div>
      <div class="project" data-aos="flip-up">
        <img src="@/assets/img/portfolio/03.jpg" alt="Braun Landing Page" class="project-img">
        <h3 class="project-title"><a href="#!">Braun Landing Page - Concept</a></h3>
      </div>
    </div>
  </section>
</template>

<style scoped>

.portfolio {
  padding: 90px 0;
  background-color: #F1F1F1;
}

.portfolio-title {
  margin-bottom: 70px;
  text-align: center;
}

.project {
  text-align: center;
}

.project + .project  {
  margin-top: 90px;
}

.project-img {
  margin-bottom: 40px;
}

.project-title {
  font-size: 18px;
}

.project-title a {
  color: #000;
  text-decoration: underline;
}
@media (max-width: 700px) {
  .portfolio {
    padding: 60px 0;
  }

  .portfolio-title {
    margin-bottom: 50px;
  }

  .project-img {
    margin-bottom: 30px;
  }

  .project + .project {
    margin-top: 55px;
  }


}

</style>