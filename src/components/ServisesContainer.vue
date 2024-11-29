<script setup>

</script>

<template>
  <section class="services">
    <div class="container">
      <div class="services-row">
        <div class="service-card" data-aos="fade-down">
          <img class="service-card-img" src="@/assets/img/services/01.svg" alt="UI/UX Design">
          <h3 class="service-card-title">UI/UX Design</h3>
          <p>Our design is translated into comprehensive digital environments built on latest development standards.</p>
        </div>
        <div class="service-card" data-aos="fade-down">
          <img class="service-card-img" src="@/assets/img/services/02.svg" alt="UI/UX Design">
          <h3 class="service-card-title">Development</h3>
          <p>Our design is translated into comprehensive digital environments built on latest development standards.</p>
        </div>
        <div class="service-card" data-aos="fade-down">
          <img class="service-card-img" src="@/assets/img/services/03.svg" alt="UI/UX Design">
          <h3 class="service-card-title">software testing</h3>
          <p>Our design is translated into comprehensive digital environments built on latest development standards.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.services {
  padding: 90px 0;
}

.services-row {
  display: flex;
  column-gap: 30px;
  row-gap: 60px;
  flex-wrap: wrap;
}

.service-card {
  flex: 1 1 0;
  min-width: 315px;
}

.service-card-img {
  margin-bottom: 30px;
}

.service-card-title {
  margin-bottom: 10px;
  font-weight: 600;
  font-size: 24px;
  text-transform: uppercase;
}

.service-card p {
  line-height: 2;
}
@media (max-width: 700px) {
  .services {
    padding: 60px 0;
  }
}

</style>