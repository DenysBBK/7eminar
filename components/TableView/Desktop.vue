<template>
    <div class="main">
        <h1>Передплата на Вищу бухгалтерську Онлайн-Академію</h1>
        <h3>Оберіть свій тарифний пакет:</h3>
        <div class="table">
            <div class="container">
                <div class="table_head-time">
                    <div class="time">
                        <p class="light">{{ props.hours }}</p>
                        <p class="norm">:</p>
                        <p class="light">{{ props.minutes }}</p>
                        <p class="norm">:</p>
                        <p class="norm">{{ props.seconds }}</p>
                    </div>
                    <div class="time_name">
                        <p class="name_light">год</p>
                        <p class="name_light">хв</p>
                        <p class="name_norm">сек</p>
                    </div>
                    <p class="time_p">(для діючих передплатників додаткова знижка 10%)</p>
                </div>
                <div class="table_head-super">
                    <div class="uphead">
                        <img src="../../public/images/hit.png">
                        <p>ХІТ ПРОДАЖУ</p>
                        <img src="../../public/images/hit.png">
                    </div>
                        <div class="super_title">
                            <p>Суперпрофесіонал</p>
                            <img src="../../public/images/sale.png">
                        </div>
                        <p class="super_subtitle">8 професіних курсів за ціною 2</p>
                        <p class="super_old">1079 грн/міс.</p>
                        <p class="super_new">679 грн/міс.</p>
                        <base-button text="Оплатити карткою" class="super_btn"></base-button>
                        <p class="super_paid">Оплатити частинами</p>
                </div>
                <div class="table_head-prem">
                    <div class="super_title">
                            <p>Преміум</p>
                            <img src="../../public/images/sale.png">
                        </div>
                        <p class="super_subtitle">8 професіних курсів за ціною 2 + Бухгалтерська Відеоплатформа №1</p>
                        <p class="super_old">1079 грн/міс.</p>
                        <p class="super_new">679 грн/міс.</p>
                        <base-button text="Оплатити карткою" class="super_btn"></base-button>
                        <p class="super_paid">Оплатити частинами</p>
                </div>

                <div class="table_item_text line">
                    <p>Поглиблені професійні курси підвищення кваліфікації<span class="blue"> (8 курсів/рік)</span></p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/done2.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>

                <div class="table_item_text line">
                    <p><img src="../../public/images/new.png">
                                Практичні курси автоматизації (робота в BAS, Medoc, Excel, ЕК)</p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/done2.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>



                <div class="table_item_text line">
                    <p><img src="../../public/images/new.png">
                                Закриті клубні лекції з експертами<span class="blue"> (1 р./ міс.)</span></p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/done2.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>


                <div class="table_item_text line">
                    <p>Майстер-класи зі змін у законодавстві<span class="blue"> (4+ р./міс.)</span></p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/done2.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>


                <div class="table_item_text line">
                    <p>Безлімітні відповіді на запитання під час онлайн-навчання</p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/done2.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>


                <div class="table_item_text line">
                    <p>Тестові та практичні завдання зі зворотним зв'язком </p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/done2.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>


                <div class="table_item_text line">
                    <p>Роздатковий матеріал (корисні файли, брошури, презентації)</p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/done2.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>


                <div class="table_item_text line">
                    <p>Клуб однодумців у Viber та підтримка куратора </p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/done2.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>


                <div class="table_item_text line">
                    <p>Сертифікати після проходження курсів</p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/done2.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>


                <div class="table_item_text line">
                    <p>Доступ до<span class="bold"> Бухгалтерської Відеоплатформи №1:</span></p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/not-done.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>


                <div class="table_item_text line">
                    <p>Відеокурси і вебінари<span class="blue"> (1100+ вже та 20+ щомісяця)</span></p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/not-done.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>


                <div class="table_item_text line">
                    <p>Безлімітні швидкі консультації від експертів (сервіс ОК)</p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/not-done.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>


                <div class="table_item_text line">
                    <p>Бланки та зразки документів<span class="blue"> (2000+ вже та 30+ щомісяця)</span></p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/not-done.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>


                <div class="table_item_text line">
                    <p>Консультант з пошуку та підготовки документів <span class="blue"> (безлімітно, щодня)</span></p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/not-done.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>


                <div class="table_item_text line">
                    <p>Калькулятори</p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/not-done.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>


                <div class="table_item_text line">
                    <p>Довідники</p>
                </div>
                <div class="table_item line">
                    <p class="tyty"><img src="../../public/images/not-done.png"></p>
                </div>
                <div class="table_item last line">
                    <p><img src="../../public/images/done2.png"></p>
                </div>
                <div></div>
                    <div class="package">
                        <div class="price">
                            <div class="price_options">
                                <p class="old">1079 грн/міс.</p>
                                <p class="new">679 грн/міс.</p>
                            </div>
                        <img src="../../public/images/sale.png">
                    </div>
                    <base-button text="Завантажити рахунок" class="price_btn"></base-button>
                    </div>
                    <div class="package">
                        <div class="price">
                            <div class="price_options">
                                <p class="old">1079 грн/міс.</p>
                                <p class="new">679 грн/міс.</p>
                            </div>
                        <img src="../../public/images/sale.png">
                    </div>
                    <base-button text="Завантажити рахунок" class="price_btn"></base-button>
                    </div>
                
            </div>
        </div>
        <p class="table_subtitle">Оплачуйте пакети <span class="lats_bold"> частинами без комісії!</span>
            Натискайте на кнопку <span class="lats_bold"> Оплатити карткою</span> та оформлюйте розстрочку
            через PrivatBank або Monobank</p>
    </div>
</template>
<script setup>
const props = defineProps({
    hours:{
        required:true
    },
    minutes:{
        required:true
    },
    seconds:{
        required:true
    }
})
</script>
<style scoped lang="scss">
@import url("https://fonts.googleapis.com/css?family=Raleway:100,200,300,regular,500,600,700,800,900,100italic,200italic,300italic,italic,500italic,600italic,700italic,800italic,900italic" );
.main{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding-top: 104px;
}
h1{
    color: #232323;
    font-size: 42px;
    font-family: e-Ukrainian;
    font-weight: 700;
    line-height: 63px;
    word-wrap: break-word;
    max-width: 922px; 
    text-align: center;
}
h3{
    color: #232323;
    font-size: 21px;
    font-family: Raleway;
    font-weight: 700;
    line-height: 28px;
    word-wrap: break-word;
    padding-top: 16px;
}
.line{
    border-bottom: 1px rgba(35, 35, 35, 0.10) solid;
}
.table{
    padding-top: 85px;
    max-width: 1140px;   
}
.container {  display: grid;
  grid-template-columns: 320px 255px 255px;
  grid-template-rows: 1.5fr 58px 58px 58px 58px 58px 58px 58px 58px 58px 58px 58px 58px 58px 58px 58px;
  gap: 0px 31px;
  grid-auto-flow: row;
  grid-template-areas:
    ". . ."
    ". . ."
    ". . ."
    ". . ."
    ". . ."
    ". . ."
    ". . ."
    ". . ."
    ". . ."
    ". . ."
    ". . ."
    ". . ."
    ". . ."
    ". . ."
    ". . ."
    ". . ."
    ". . ."; 
}

.table_head{
    display: flex;
    
    align-items: center;
    // justify-content: flex-end;
    width: 100%;
    padding-left: 30px;
    padding-right: 30px; 
    gap: 20.5%;
    justify-content: space-between;

   
}

.table_head-time{
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
    max-width: 225px;
    
};

.time{
    display:flex;
    flex-direction:row;
    gap:6px;  
}
.light{
    color: #0066CC;
    font-size: 29px;
    font-family: Raleway;
    font-weight: 400;
    line-height: 43.50px;
    opacity:0.4
}
.norm{
    color: #0066CC;
    font-size: 29px;
    font-family: Raleway;
    font-weight: 400;
    line-height: 43.50px;
    
}
.name_light{
    color: #0066CC;
    font-size: 15px;
    font-family: Raleway;
    font-weight: 400;
    line-height: 22.50px;
    opacity:0.4

}
.name_norm{
    color: #0066CC;
    font-size: 15px;
    font-family: Raleway;
    font-weight: 400;
    line-height: 22.50px;
}
.time_name{
    display: flex;
    flex-direction: row;
    gap: 35px;
}
.time_p{
    color: #515154;
    font-size: 15px;
    font-family: Raleway;
    font-weight: 400;
    line-height: 22.50px;
    word-wrap: break-word;
    text-align: center;
    padding-top: 14px;
}
.packages{
    display: flex;
    gap: 31px;
}
.table_head-super{
    display: flex;
    align-items: center;
    flex-direction: column;
    max-width: 255px;
}
.table_head-prem{
    display: flex;
    align-items: center;
    flex-direction: column;
    max-width: 255px;
    padding-top: 11px;
    background-color:rgba(96.29, 175.31, 254.34, 0.05);
    border-top-right-radius: 15px;
    border-top-left-radius: 15px;
}
.last{
    background-color:rgba(96.29, 175.31, 254.34, 0.05);  
}
.uphead{
    display: flex;
    background-color: #FFE601;
    align-items: center;
    padding: 5px 59px 5px 59px;
    border-top-right-radius: 15px;
    border-top-left-radius: 15px;
    gap: 13px;
    white-space: nowrap;

}
.uphead p{
    color: #232323;
    font-size: 13px;
    font-family: Raleway;
    font-weight: 700;
    line-height: 14.30px; 
}
.super{
    &_title{
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 16px;
        padding-top: 11px;
    }
    &_subtitle{
        color: #232323;
        font-size: 13px;
        font-family: Raleway;
        font-weight: 500;
        text-transform: lowercase;
        line-height: 19.50px;
        word-wrap: break-word;
        text-align: center;
        padding-top: 4px;
        max-height: 40px;
    }
    &_old{
        color: #979797;
        font-size: 13px;
        font-family: Raleway;
        font-weight: 400;
        text-decoration: line-through;
        word-wrap: break-word;
        padding-top: 12px;
    }
    &_new{
        color: #232323;
        font-size: 17px;
        font-family: Raleway;
        font-weight: 700;
        word-wrap: break-word;
        padding-top: 5px;
    }
    &_btn{
       margin-top: 12px;
    }
    &_paid{
        color: #979797;
        font-size: 13px;
        font-family: Raleway;
        font-weight: 400;
        text-decoration: underline;
        padding-top: 12px;
    }
}

.super_title p{
    color: #232323;
    font-size: 13px;
    font-family: Raleway;
    font-weight: 800;
    line-height: 19.50px;
    word-wrap: break-word 
}
.table_content{
    padding-top: 25px;
}
.table_item{
    display: flex;
    flex-direction: row;
    gap: 282px;
    justify-content: center;
    align-items: center;
    padding-bottom: 6px;
}
.table_item p,
.table_item_text p{
    max-width: 320px;
    color: #232323;
font-size: 15px;
font-family: Raleway;
font-weight: 500;
line-height: 21px;
word-wrap: break-word
}
.table_item_text{
    display: flex;
    flex-direction: row;
    gap: 282px;
    align-items: center;
    padding-bottom: 6px;
}

ul{
    padding: 16px 32px 16px 32px;
    display: flex;
    flex-direction: column;
}
li{
   padding-top: 16px;
    border-bottom: 1px rgba(35, 35, 35, 0.10) solid;
    display: flex;
    // justify-content: space-around;
    align-items: center;
    gap: 282px;
}
.blue{
    color: #0066CC;
font-size: 15px;
font-family: Raleway;
font-weight: 500;
line-height: 21px;
word-wrap: break-word
}
.bold{
    color: #0066CC;
font-size: 15px;
font-family: Raleway;
font-weight: 700;
line-height: 21px;
word-wrap: break-word
}
.tyty{
    align-self: center;
    margin-left: 30px;
}
.div{
    flex: 0 1 320px;
}
.package{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 12px;
    padding-top: 40px;
}
.price{
    display: flex;
    flex-direction: row;
    gap: 26px;
}
.old{
    color: #979797;
font-size: 13px;
font-family: Raleway;
font-weight: 400;
text-decoration: line-through;
word-wrap: break-word
}
.new{
    color: #232323;
font-size: 17px;
font-family: Raleway;
font-weight: 700;
word-wrap: break-word
}
.table_subtitle{
    padding-top: 40px;
    max-width: 739px;
    text-align: center;
    color: #232323;
font-size: 17px;
font-family: Raleway;
font-weight: 500;
line-height: 25.50px;
word-wrap: break-word;
padding-bottom: 104px
};

.lats_bold{
    color: #232323;
font-size: 17px;
font-family: Raleway;
font-weight: 700;
line-height: 25.50px;
word-wrap: break-word ;
}
</style>