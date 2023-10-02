<template>
    <div class="main_container">
        <div class="container">
            <p class="small_title">
                Вища Бухгалтерська Online-Академія
            </p>
            <h1 class="title">
                Підвищення кваліфікації
та профперепідготовка для бухгалтерів
            </h1>
            <base-button
            class="title_btn"
            text="Обрати навчання >>"></base-button>
                    <Swiper
                    :modules="[Navigation,Autoplay]"
                    :navigation="{
                        prevEl:'.prev_btn',
                        nextEl:'.next_btn',
                        enabled:true,
                       
                    }"
                    :loop="true"
                    :speed="1000"
                    :centered-slides="true"
                    :slides-per-view="1.6"
                    :spaceBetween="-26"
                    
                    :breakpoints="{
                        '768': {
                            loop:false,
                            slidesPerView:3,
                            autoplay:true,
                            centeredSlides:true,
                            speed:2000,                          
                        }
                    }"             
               >
                <SwiperSlide v-for="item in photo" :key="item">
                    <img :src="item">
                </SwiperSlide>
               </Swiper>
                <div class="nav_btns">
                    <button class="prev_btn" type="button">
                        <img src="/images/prev.png">
                    </button>
                    <button class="next_btn" type="button">
                        <img src="/images/next.png">
                    </button>
                </div>
                <div class="full_photo">
                    <img src="../public/images/phone1.png">
                    <img src="../public/images/phone2.png">
                    <img src="../public/images/phone3.png">
                </div>

            <h2 class="main_last">
                Разом дешевше! Купуйте передплату на Вищу Бухгалтерську Online-Академію <span class="last_blue">8 професій за ціною 2</span>
            </h2>
        </div>
    </div>
</template>
<script setup>

import { Swiper, SwiperSlide} from 'swiper/vue';
import { Navigation, Autoplay} from 'swiper/modules';

import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';
import 'swiper/css/autoplay';





const photo = [
    'images/phone1.png',
    'images/phone2.png',
    'images/phone3.png',
   
];

</script>
<style scoped lang="scss">
@import url("https://fonts.googleapis.com/css?family=Raleway:100,200,300,regular,500,600,700,800,900,100italic,200italic,300italic,italic,500italic,600italic,700italic,800italic,900italic" );

.swiper{
    max-width:600px;
    height: 100%;
    margin: 0 auto;
    padding-top: 72px;
    @media screen and (min-width: 992px){
        display: none;
    }

};
.swiper_wrapper{
  
   width: 100%;
   overflow: hidden;
   margin: 0 auto;
   @media screen and (min-width: 992px){
        display: none;
    }

}
.swiper_slide{
  max-width: 220px;
  padding: 20px;
  @media screen and (min-width: 992px){
        display: none;
    }
}

.full_photo{
    padding-top: 72px;
    display: flex;
    gap: 26px;
    max-width: 992px;
    @media screen and (max-width: 992px){
        display: none;
    }
}
.full_photo img:hover{
    transform: translateY(-48px);
    
}
.full_photo img {
    transition: transform 0.3s ease;
}

.swiper-button-prev{
    color: red;
}
.swiper-button-next{
    color: green;
}

.main{
    &_container{
        background-color: white;
    margin-top: 64px;
    display: flex;
    flex-direction: column;
    align-items: center;    
    }
}
.container{
    max-width: 1078px;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}
.small_title{
    font-size: 17px;
    font-weight: 500;
    color: #232323;
    line-height: 25px;
    font-family: Raleway;
    width: 100%;
}
.title{
    font-size: 24px;
    color: #232323;
    font-weight: 700;
    font-family: e-Ukrainian;
    line-height: 36px;
    word-wrap: break-word;
    padding-top: 22px;
    max-width: 342px;
    text-align: center;
    @media screen and (min-width: 768px){
        color: #232323;
    font-size: 42px;
   
    font-weight: 700;
    line-height: 63px;
    word-wrap: break-word;
    max-width: 942px; 
    text-align: center;
    }
}
.title_btn{
    margin-top: 22px;
}
.phone_container{
    display: flex;
    flex-direction: row;
    padding-top: 40px;
    gap: 24px;
}
.main_last{
    color: #232323;
    padding-top: 40px;
    font-size: 16px;
    font-weight: 700;
    line-height: 24px;
    word-wrap: break-word;
    max-width: 342px;
    padding-bottom: 40px;
    text-align: center;
    font-family: e-Ukrainian;
    @media screen and (min-width: 768px){
        font-size: 23px;
        font-weight: 700;
        line-height: 34.50px;
        max-width: 889px;

    }
}
.last_blue{
    font-size: 16px;
    font-family: e-Ukrainian;
    font-weight: 700;
    line-height: 24px;
    word-wrap: break-word;
    color: #0066CC;
    @media screen and (min-width: 768px){
        font-size: 23px;
        font-weight: 700;
        line-height: 34.50px;
    }
}
.central{
    padding-bottom: 44px;
}
.non-central{
    padding-top: 47px;
}

.nav_btns{
    display: flex;
    align-items: center;
    gap: 6px;
    justify-content: center;
    @media screen and (min-width: 992px){
        display: none;
    }
}

.swiper-slide-active{
    margin-top: -48px;
}

</style>