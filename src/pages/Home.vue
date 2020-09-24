<template>
  <div class="container">
    <div class="row">
      <span class="shade text-white text-center text-h4 q-pa-md">Safe Motherhood Foundation.org</span>
      <br> <br>
      <span class="text-weight-light q-mt-md q-px-xl text-center"> Our sisters, wives, daughters and new born still die 
        preventable deaths due to poverty, ignorance and inadequate reproductive healthcare delivery 
        throughout the country especially in rural areas - Maternal mortality is a monster that we can jointly defeat. 
        <br>- Joe Adejo</span>
        
        <div class="col-md-6 col-sm-6 col-xs-12">
          <div class="q-pa-md">
            <img src="images/mail.jpeg" alt="brandimage" width="100%"/>
          </div>

          <div class="q-pa-md">
            <q-video
              :ratio="16/9"
              src="https://www.youtube.com/embed/2C1d9q762Kw"
            />
          </div>
        </div>

        <div class="col-xs-12 col-sm-6 col-md-6">
          <div class="shader q-pa-md">
            <span class="text-h5">About the Foundation</span> <br>
            Safe Motherhood Foundation was established by Dr Joe Adejo. This vision was borne out of pain and anguish over the devastating effect of maternal mortality and new born morbidity.          
            The Safe Motherhood Foundation is a family Focused NGO set up to bring maternal mortality and child morbidity to zero tolerance level, 
            also to restore unity and maintain peace in families fostering a healthy society and a harmonious community.  
            Our research has proven that maternal mortality, child morbidity and family discord are due to ignorance and not knowing God. 
            The steps begin with handling of the teenage girls, before marriage, preconception, prenatal, through gestation, delivery and post-partum.
            Our goal is to build a culture of cleanliness, healthy living producing a healthy woman, healthy pregnancy, and a healthy child.
            <router-link to="/about">Read more...</router-link>
          </div>

<!-- B O O K S -->
          <div class="q-pa-md" style="max-width: 500px">
              <q-list bordered padding>
                <div class="shade text-white text-weight-bold text-h6">BOOKS TO HELP YOU</div>
                <q-item>
                  <q-item-section top avatar>
                    <q-img @click="book=true" src="images/mail.jpeg" style="width: 50px" />
                    
                  </q-item-section>

                  <q-item-section>
                    <q-item-label @click="book=true">Swift Childbirth Concise</q-item-label>
                    <q-item-label caption lines="2">Dr. Joe Adejo</q-item-label>
                    <q-rating
                      v-model="model"
                      max="5"
                      size="1.5em"
                      color="yellow"
                      icon="star_border"
                      icon-selected="star"
                      icon-half="star_half"
                      no-dimming
                    />                    
                  </q-item-section>

                  <q-item-section side top class="text-green">
                    <q-item-label caption>NGN 1,000</q-item-label>
                    <q-item-label caption>USD 3.00</q-item-label>                  
                  </q-item-section>
                </q-item>

                <q-separator spaced inset="item" />

                <q-item>
                  <q-item-section top avatar>
                    <q-img src="images/mail.jpeg" style="width: 50px" />
                    
                  </q-item-section>

                  <q-item-section>
                    <q-item-label>Introduction to Swift Childbirth Graphics (English)</q-item-label>
                    <q-item-label caption lines="2">Dr. Joe Adejo</q-item-label>
                    <q-rating
                      v-model="model"
                      max="5"
                      size="1.5em"
                      color="yellow"
                      icon="star_border"
                      icon-selected="star"
                      icon-half="star_half"
                      no-dimming
                    />
                  </q-item-section>

                  <q-item-section side top class="text-green">
                    <q-item-label caption>NGN 1,000</q-item-label>
                    <q-item-label caption>USD 3.00</q-item-label>                   
                  </q-item-section>
                </q-item>

                <q-separator spaced inset="item" />

                <q-item>
                  <q-item-section top avatar>
                    <q-img src="images/mail.jpeg" style="width: 50px" />
                    
                  </q-item-section>

                  <q-item-section>
                    <q-item-label>Gabatarwa Ga Haihuwa Lafiya Tare Da Hotuna</q-item-label>
                    <q-item-label caption lines="2">Dr. Joe Adejo</q-item-label>
                    <q-rating
                      v-model="model"
                      max="5"
                      size="1.5em"
                      color="yellow"
                      icon="star_border"
                      icon-selected="star"
                      icon-half="star_half"
                      no-dimming
                    />
                  </q-item-section>

                  <q-item-section side top class="text-green">
                    <q-item-label caption>NGN 1,000</q-item-label>
                    <q-item-label caption>USD 3.00</q-item-label>                  
                  </q-item-section>
                </q-item>  

                <q-separator spaced inset="item" />

                <q-item>
                  <q-item-section top avatar>
                    <q-img src="images/mail.jpeg" style="width: 50px" />
                    
                  </q-item-section>

                  <q-item-section>
                    <q-item-label>Ante-Natal Care</q-item-label>
                    <q-item-label caption lines="2">Dr. Joe Adejo</q-item-label>
                    <q-rating
                      v-model="model"
                      max="5"
                      size="1.5em"
                      color="yellow"
                      icon="star_border"
                      icon-selected="star"
                      icon-half="star_half"
                      no-dimming
                    />
                  </q-item-section>

                  <q-item-section side top class="text-green">
                    <q-item-label caption>NGN 1,000</q-item-label>
                    <q-item-label caption>USD 3.00</q-item-label>                   
                  </q-item-section>
                </q-item>  
              </q-list>
            </div>
        </div>
      </div>   

      <div class="carousel">
        <q-carousel
          v-model="slid"
          swipeable
          animated
          autoplay
          infinite
          control-color="secondary"
          :navigation="navigation"
          :navigation-position="navPos"
          height="250px"
          class="bg-grey-8 text-white"
          >

          <q-carousel-slide :name="carousel.name" class="q-pa-none" v-for="carousel in topCarousel" :key="carousel.id">
              <div>
                  <q-img :src="carousel.imageUrl" height="250px"/>
              </div>
          </q-carousel-slide>
        </q-carousel>
      </div>

<!-- Introduction -->
      <div class="row introduction">
        <div class="col-md-5 col-sm-5 col-xs-12 bg-grey-4">
          <div class="q-pa-lg">
            <span class="text-h5">The Problem</span> <br>
              Our sisters, wives, daughters and new born still die preventable deaths due to poverty, ignorance and inadequate reproductive healthcare delivery throughout the country especially in rural areas. <br>
              The major health problems of women are high maternal mortality rates associated with pregnancy, labour and childbirth.<br>
              Causes of maternal death among others are; ignorance, poverty, woman conceiving when unhealthy, malaria, excessive bleeding, infection, toxaemia of pregnancy, unsafe abortion, prolonged labour, fear, teenage pregnancy, having several sexual partners.<br>
              Maternal mortality is a monster that we can jointly defeat. <br>
              The scope of our assignment spreads across protecting the teenage girl from having VVF, ensuring safe delivery and protected babies of mothers with HIV, preventing complications due to actions and inactions that can lead to having babies with major health crisis.
          </div>
        </div>

        <div class="col-md-7 col-sm-7 col-xs-12  bg-green-7">
          <div class="q-pa-md">
            <!-- Two Cards -->
            <div class="row items-start justify-center  q-pa-md q-gutter-sm">
              <q-card class="q-pa-md text-white bg-primary" style="max-width: 350px">
                <span class="text-h3 text-weight-thin">Our Vision <br> </span>
                  <p>To see that a woman carries her pregnancy to full term, delivers 
                    her baby and both mother and baby remain healthy through postpartum 
                    while child lives beyond 5years. <br>
                    Our vision is to bring maternal mortality to zero tolerance level.
                  </p>
              </q-card>

              <q-card class="q-pa-md text-black" style="max-width: 350px"> 
                <span class="text-h3 text-weight-thin">Our Mission <br> </span>
                  <p>Our mission is to eliminate maternal mortality and new born morbidity 
                    by equipping the woman with adequate information to promote healthy lifestyle, 
                    healthy pregnancy and a healthy family. Also to work hand in hand with the 
                    health care givers to reinforce the effectiveness of effort. We carry out 
                    sensitization against HIV, STDs and needless voluntary and involuntary abortion.
                  </p>                
              </q-card>
            </div>
          </div>
        </div>        
      </div>
      <!-- B O O K -->
    <q-dialog v-model="book">
      <ModalBook/>
    </q-dialog>       
    </div>  
</template>

<script>
import ModalBook from 'components/Dialogs/ModalBook1'
export default {
  components: {
    ModalBook
  },

  data () {
    return { 
      book: false,
      model: 4,   
    // for Carousel
      slid: 'moonlove',
      navigation: true,
      navPos: 'bottom',
      slide: 1,

      topCarousel: [
        {
          id: '1',
          name: 'moonlove',
          imageUrl: '/images/preg1.jpg',
          title: '18th December, 2020',
        },
        {
          id: '2',
          name: 'lovecircle',
          imageUrl: '/images/preg2.jpg',
          title: '#MusDee2020',
        },
        {
          id: '3',
          name: 'lovelove',
          imageUrl: '/images/preg3.jpg',
          title: '#Soulmates',
        },
        {
          id: '4',
          name: 'loveRing',
          imageUrl: '/images/preg4.jpg',
          title: '#Forever',
        },                         
      ],      
    }
  }

}
</script>

<style scoped>

.custom-caption{
    bottom: 50px;
    text-align: center;
    padding: 12px;
    background-color: rgba(0, 0, 0, .3);
}

.radius{
  border-radius: 15px 0px 15px 0px;
  max-width: 350px;
}

.shade{  
    text-align: center;
    padding: 10px;
    background-color: rgb(245, 229, 6);
    border-radius: 15px 15px 15px 15px;
    margin-bottom: 5px;
    margin-right: 5px;
    transition: 0.4s;   
    margin: 15px; 
}

.shader{  
    text-align: left;
    padding: 20px;
    background-color: rgba(141, 245, 6, 0.815);
    border-radius: 0px 15px 0px 15px;
    margin-bottom: 5px;
    margin-right: 5px;
    transition: 0.4s;   
    margin: 15px; 
}


a{
    text-decoration: none;
    color: brown;
    font-weight: bold;
}
</style>
