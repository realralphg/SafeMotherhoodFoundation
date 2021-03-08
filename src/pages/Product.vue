<template>
  <div class="bg-white">
    <header class="custom__header-variant2 column justify-center items-center">
      <h3 class="text-white text-h2 text-weight-bolder custom__heading-white">
        <span class="text-white">Products</span>
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
              Our
              <span class="text-weight-bolder">Books</span>
            </h3>
            <div class="row">
              <div class="col-md-3 col-sm-6 col-xs-12 q-py-md">
                <q-img height="300px" src="/images/book1.jpg" contain />
              </div>
              <div class="col-md-3 col-sm-6 col-xs-12 q-py-md">
                <q-img height="300px" src="/images/book2.jpg" contain />
              </div>
              <div class="col-md-3 col-sm-6 col-xs-12 q-py-md">
                <q-img height="300px" src="/images/book3.jpg" contain />
              </div>
              <div class="col-md-3 col-sm-6 col-xs-12 q-py-md">
                <q-img height="300px" src="/images/book4.jpg" contain />
              </div>
            </div>
          </div>
        </div>
        <h3 class="text-center text-h5 text-weight-light custom__heading-black">
          Our <span class="text-weight-bolder">Audio Books</span>
        </h3>
        <div class="row items-center q-px-sm">
          <div class="col-md-6 col-sm-12 col-xs-12 q-pr-sm">
            <iframe
              width="100%"
              height="315"
              src="https://www.youtube.com/embed/Z0ZP8v3o3mc"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
          <div class="col-md-6 col-sm-12 col-xs-12 q-pl-sm">
            <iframe
              width="100%"
              height="315"
              src="https://www.youtube.com/embed/x9njHNFHUOg"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
        </div>
        <h3 class="text-center text-h5 text-weight-light custom__heading-black">
          <span class="text-weight-bolder">Gallery</span>
        </h3>
        <div class="row items-center">
          <div class="col-md-12 col-sm-12 col-xs-12">
            <q-carousel
              animated
              v-model="slide"
              navigation
              infinite
              :autoplay="true"
              arrows
              :fullscreen.sync="fullscreen"
              transition-prev="slide-right"
              transition-next="slide-left"
              @mouseenter="autoplay = false"
              @mouseleave="autoplay = true"
            >
              <q-carousel-slide :name="1" img-src="/images/book5.jpg" />
              <q-carousel-slide :name="2" img-src="/images/book6.jpg" />
              <q-carousel-slide :name="3" img-src="/images/book7.jpg" />
              <q-carousel-slide :name="4" img-src="/images/book8.jpg" />
              <template v-slot:control>
                <q-carousel-control position="bottom-right" :offset="[18, 18]">
                  <q-btn
                    push
                    round
                    dense
                    color="white"
                    text-color="primary"
                    :icon="fullscreen ? 'fullscreen_exit' : 'fullscreen'"
                    @click="fullscreen = !fullscreen"
                  />
                </q-carousel-control>
              </template>
            </q-carousel>
          </div>
        </div>
        <div class="row q-py-sm justify-center">
          <div class="col-md-3 col-sm-6 col-xs-12">
            <q-btn
              outline
              color="black"
              class="text-black text-capitalize q-my-sm"
              >Contact Us For Full Books</q-btn
            >
            <span class="q-mx-sm text-weight-bold text-h6">OR</span>
            <q-btn
              color="black"
              class="text-white text-capitalize"
              label="Donate Here"
            />
          </div>
          <!-- <div class="col">
          </div>
          <div class="col">
          </div> -->
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data: () => ({
    book: false,
    model: 4,
    // for Carousel
    slid: "moonlove",
    navigation: true,
    navPos: "bottom",
    slide: 1,
    fullscreen: false,
  }),
};
</script>

<style lang="scss" scoped>
.custom__header-variant2 {
  background: linear-gradient(rgba(0, 0, 0, 0.9), rgba(0, 0, 0, 0.7)),
    url("/images/product.jpg");
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
