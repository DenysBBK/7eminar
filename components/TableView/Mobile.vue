<template>
    <div class="container">
        <h1>Передплата на Вищу бухгалтерську Онлайн-Академію</h1>
        <h3>Оберіть свій тарифний пакет:</h3>
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
        <div class="table">
            <div class="hit">
                <div class="uphead">
                        <img src="../../public/images/hit-white.png">
                        <p>ХІТ ПРОДАЖУ</p>
                        <img src="../../public/images/hit-white.png">
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
            <ul class="table_content">
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                    <p class="table_text">Поглиблені професійні курси підвищення кваліфікації <span class="table_blue">(8 курсів/рік)</span></p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                    <p class="table_text">
                        <img src="../../public/images/new.png" class="table_new">Поглиблені професійні курси підвищення кваліфікації (8 курсів/рік)</p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                    <p class="table_text">
                        <img src="../../public/images/new.png">Поглиблені професійні курси підвищення кваліфікації <span class="table_blue">(8 курсів/рік)</span></p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                    <p class="table_text">Майстер-класи зі змін у законодавстві <span class="table_blue">(4+ р./міс.)</span></p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                    <p class="table_text">Безлімітні відповіді на запитання під час онлайн-навчання</p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                    <p class="table_text">Тестові та практичні завдання зі зворотним зв'язком </p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                    <p class="table_text">Роздатковий матеріал (корисні файли, брошури, презентації)</p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                    <p class="table_text">Клуб однодумців у Viber та підтримка куратора </p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                    <p class="table_text">Сертифікати після проходження
курсів </p>
                </li>
            </ul>
            <div class="price">
                <div class="price_options">
                    <p class="old">1079 грн/міс.</p>
                    <p class="new">679 грн/міс.</p>
                </div>
                <img src="../../public/images/sale.png">
            </div>
            <base-button text="Завантажити рахунок" class="price_btn"></base-button>
            <div class="prem">
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
            <ul class="table_content">
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                        <p class="table_text">Поглиблені професійні курси підвищення кваліфікації <span class="table_blue">(8 курсів/рік)</span></p>  
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                    <p class="table_text">
                        <img src="../../public/images/new.png" class="table_new">Практичні курси автоматизації (робота в BAS, Medoc, Excel, ЕК)</p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                    <p class="table_text">
                        <img src="../../public/images/new.png" class="table_new">Закриті клубні лекції з експертами <span class="table_blue">(1 р./ міс.)</span></p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                        <p class="table_text">Майстер-класи зі змін у законодавстві  <span class="table_blue"> (4+ р./міс.)</span></p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                        <p class="table_text">Безлімітні відповіді на запитання під час онлайн-навчання</p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                        <p class="table_text">Тестові та практичні завдання зі зворотним зв'язком </p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                        <p class="table_text">Роздатковий матеріал (корисні файли, брошури, презентації)</p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                        <p class="table_text">Клуб однодумців у Viber та підтримка куратора </p> 
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                        <p class="table_text">Сертифікати після проходження курсів </p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                        <p class="table_text">Доступ до <span class="table_blue_bold">Бухгалтерської Відеоплатформи №1:</span></p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                        <p class="table_text">Відеокурси і вебінари <span class="table_blue">(1100+ вже та 20+ щомісяця)</span></p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                        <p class="table_text">Безлімітні швидкі консультації від експертів (сервіс ОК)</p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                        <p class="table_text">Бланки та зразки документів <span class="table_blue">(2000+ вже та 30+ щомісяця)</span></p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                        <p class="table_text">Консультант з пошуку та підготовки документів<span class="table_blue"> (безлімітно, щодня)</span></p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                        <p class="table_text">Калькулятори</p>
                </li>
                <li class="table_line">
                    <span class="table_icon">
                        <img src="../../public/images/done.png">
                    </span>
                        <p class="table_text">Довідники</p>
                </li>
            </ul>
            <div class="price">
                <div class="price_options">
                    <p class="old">1079 грн/міс.</p>
                    <p class="new">679 грн/міс.</p>
                </div>
                <img src="../../public/images/sale.png">
            </div>
            <base-button text="Завантажити рахунок" class="price_btn"></base-button>
        </div>
        <p class="last">
            Оплачуйте пакети <span class="last_bold">частинами без комісії!</span>
            Натискайте на кнопку <span>Оплатити карткою</span> та оформлюйте розстрочку
            через PrivatBank або Monobank  
        </p>
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
.container{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding-top: 72px;
}
h1{
    color: #232323;
    font-size: 24px;
    font-family: e-Ukraine Head;
    font-weight: 700;
    line-height: 36px;
    word-wrap: break-word;
    text-align: center;
    padding-left: 5px;
    padding-right: 5px;
}
h3{
    color: #232323;
    font-size: 18px;
    font-family: Raleway;
    font-weight: 700;
    line-height: 28px;
    word-wrap: break-word ;
    padding-top: 16px;
}
.time{
    display:flex;
    flex-direction:row;
    gap:6px;
    padding-top: 16px;
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
.table{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding-top: 24px;
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
    font-size: 14px;
    font-family: Raleway;
    font-weight: 700;
    line-height: 15.40px;
    word-wrap: break-word
 
}
.hit,
.prem{
    display: flex;
    align-items: center;
    flex-direction: column; 
    width: 314px;
}
.prem{
    padding-top: 72px;
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
        max-width: 243px;
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
.table{
    &_content{
        max-width: 312px;
        padding-top: 24px;
    }
    &_line{
        display: flex;
        gap: 6px;
        align-items: flex-start;
        padding-top: 6px;
    }
    &_text{
        color: #232323;
        font-size: 16px;
        font-family: Raleway;
        font-weight: 500;
        line-height: 22.40px;
        max-width: 280px;
    }
    &_blue{
        color: #0066CC;
        font-size: 16px;
        font-family: Raleway;
        font-weight: 500;
        line-height: 22.40px;
        word-wrap: break-word 
    }
    &_blue_bold{
        color: #0066CC;
        font-size: 16px;
        font-family: Raleway;
        font-weight: 700;
        line-height: 22.40px;
        word-wrap: break-word
    }
    &_new{
        padding-right: 5px;
    }
}
.price{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 26px;
    padding-top: 24px;
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
word-wrap: break-word;
padding-top: 5px;
}
.price_btn{
    margin-top: 12px;
}
.last{
    color: #232323;
    font-size: 16px;
    font-family: Raleway;
    font-weight: 500;
    line-height: 24px;
    word-wrap: break-word;
    text-align: center;
    max-width: 342px;
    padding-top: 48px;
    padding-bottom: 72px;
    &_bold{
        color: #232323;
        font-size: 16px;
        font-family: Raleway;
        font-weight: 700;
        line-height: 24px;
        word-wrap: break-word 
    }
}
</style>
