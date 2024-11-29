<script setup>

</script>

<template>
  <footer class="contacts">
    <div class="container">
      <div class="contacts-title">
        <h2 class="title-1">Contacts</h2>
      </div>
      <div class="contacts-content" data-aos="fade-down">
        <p>Want to know more or just chat?<br> You are welcome!</p>
      </div>
      <div class="contacts-button" data-aos="fade-down">
        <a href="#!" class="btn">Send message</a>
      </div>
      <div class="contacts-social" data-aos="zoom-in">
        <a href="#!"><img src="@/assets/img/socials/LinkedIn.svg" alt="LinkedIn"></a>
        <a href="#!"><img src="@/assets/img/socials/Instargam.svg" alt="Instargam"></a>
        <a href="#!"><img src="@/assets/img/socials/Behance.svg" alt="Behance"></a>
        <a href="#!"><img src="@/assets/img/socials/Dribble.svg" alt="Dribble"></a>
      </div>
      <div class="contacts-footer" data-aos="fade-up">
        <p>Like me on<br> LinkedIn, Instagram, Behance, Dribble</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.contacts {
  padding: 90px 0;
  text-align: center;
}

.contacts-title {
  margin-bottom: 40px;
}

.contacts-content {
  margin: 0 auto 40px;
  max-width: 480px;
  font-size: 18px;
}

.contacts-content p + p {
  margin-top: 1em;
}

.contacts-button {
  margin-bottom: 80px;
}

.contacts-social {
  display: flex;
  justify-content: center;
  align-items: center;
  column-gap: 60px;
  margin-bottom: 40px;
}

.contacts-footer {
  color: #828282;
}
@media (max-width: 700px) {
  .contacts {
    padding: 60px 0;
  }

  .contacts-title {
    margin-bottom: 20px;
  }

  .contacts-content {
    margin-bottom: 20px;
  }

  .contacts-button {
    margin-bottom: 70px;
  }

  .contacts-social {
    column-gap: 50px;
    margin-bottom: 20px;
  }
}

</style>