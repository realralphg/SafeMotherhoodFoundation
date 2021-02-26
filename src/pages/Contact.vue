<template>
  <div class="bg-white">
    <header class="custom__header-variant3 column justify-center items-center">
      <h3 class="text-white text-h2 text-weight-bolder custom__heading-white">
        <span class="text-yellow-12">Contact Us</span>
      </h3>
      <span
        class="text-white text-subtitle1 text-weight-light q-mt-md q-px-xl text-center"
      >
        Our sisters, wives, daughters and new born still die preventable deaths
        due to poverty, ignorance and inadequate reproductive healthcare
        delivery throughout the country especially in rural areas - Maternal
        mortality is a monster that we can jointly defeat. <br />-
        <span class="text-h6 text-weight-light"> Joe Adejo</span></span
      >
    </header>
    <section class="section__about-us">
      <div class="custom__container">
        <div class="row">
          <div class="col">
            <h3
              class="text-center text-h5 text-weight-light custom__heading-black"
            >
              We will love to hear from
              <span class="text-weight-bolder">You!</span>
            </h3>
            <div class="row justify-center q-mb-md">
              <div class="col-6">
                <q-input type="text" square outlined label="Your Name*" />
              </div>
            </div>
            <div class="row justify-center  q-mb-md">
              <div class="col-6">
                <q-input type="email" square outlined label="Your Email*" />
              </div>
            </div>
            <div class="row justify-center">
              <div class="col-6">
                <q-input
                  type="textarea"
                  square
                  outlined
                  label="Your Message*"
                />
              </div>
            </div>
            <div class="row justify-center q-my-md">
              <div class="col-2">
                <q-btn outline color="black" class="text-black text-capitalize"
                  >Send Message</q-btn
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data: () => ({
    slide: "style",
    lorem: "Lorem ipsum dolor,"
  })
};
</script>

<style lang="scss" scoped>
.custom__header-variant3 {
  background: linear-gradient(rgba(0, 0, 0, 0.9), rgba(0, 0, 0, 0.7)),
    url("/images/contact1.jpg");
  -webkit-background: linear-gradient(
      rgba(0, 148, 50, 0.9),
      rgba(0, 148, 146, 0.7)
    ),
    url("/images/preg5.jpg");
  background-size: cover;
  background-attachment: fixed;
  height: calc(100vh - 52px);
}

.custom__heading-white::after {
  display: block;
  height: 2px;
  width: 10%;
  background-color: #ffffff;
  content: " ";
  margin: 0 auto;
  margin-top: 20px;
  /* margin-bottom: 30px; */
}

.custom__heading-black::after {
  display: block;
  height: 2px;
  width: 10%;
  background-color: #000;
  content: " ";
  margin: 0 auto;
  margin-top: 20px;
  /* margin-bottom: 30px; */
}

.my-card {
  width: 100%;
  max-width: 650px;
}

a {
  text-decoration: none;
  color: #520131;
}
</style>
