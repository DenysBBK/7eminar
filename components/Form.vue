<template>
    <div class="container">
        <div class="form">
            <div class="form_main">
                <form class="form_inputs" @submit.prevent="submitForm">
                    <h2 class="inputs_title">Залиште заявку, і ми підберемо для вас умови зі знижкою</h2>
                    <h3 v-if="success">Ви були успішно зареєстровані!</h3>
                    <h3 v-if="errorTrigger" class="error">{{ errorMessage }}</h3>
                    <div class="input_content">
                        <div class="input">
                            <span class="input_label">Ваше ім'я</span>
                            <input type="text" placeholder="Ваше ім'я" :class="{
                                'input_place': name.isValid === true,
                                'input_validation':name.isValid === false

                            }" v-model="name.data">
                            <span class="validation" v-if="name.isValid === false">Введіть ім'я</span>
                        </div>
                        <div class="input">
                            <span class="input_label">Номер телефону</span>
                            <input type="text" placeholder="Введіть Ваш номер телефону" :class="{
                                'input_place': number.isValid === true,
                                'input_validation':number.isValid === false
                            }" v-model="number.data">
                            <span class="validation" v-if="number.isValid === false">Введіть номер телефону</span>
                        </div>
                        <div class="input">
                            <span class="input_label">Ваш e-mail</span>
                            <input type="text" placeholder="Введіть Ваш e-mail" :class="{
                                'input_place': email.isValid === true,
                                'input_validation':email.isValid === false
                            }" v-model="email.data">
                            <span class="validation" v-if="email.isValid === false">Введіть пошту</span>
                        </div>
                    </div>
                    <base-button text="Зареєструватись" class="input_btn" type="submit"></base-button>
                </form>
            </div>
            <div class="form_text">
                <div class="form_content">
                    <h2 class="content_title">З передплатою Академії ви отримаєте:</h2>
                    <div class="content_block">
                        <div class="content_pair">
                            <div class="content_item">
                                <h2 class="content_main">8+</h2>
                                <p class="content_text">Професійних курсів</p>
                            </div>
                            <div class="content_item">
                                <h2 class="content_main">12</h2>
                                <p class="content_text">закритих клубних лекцій</p>
                            </div>
                        </div>
                        <div class="content_pair">
                            <div class="content_item">
                                <h2 class="content_main">48</h2>
                                <p class="content_text">нових вебінарів та тренінгів</p>
                            </div>
                            <div class="content_item">
                                <img src="../public/images/infinity.png">
                                <p class="content_text">Безлімітні відповіді
                                на запитання протягом
                                навчання</p>
                            </div>
                        </div>     
                    </div>
                    <div class="content_pair">
                        <div class="content_item">
                            <h2 class="content_last">Тестові та практичні</h2>
                            <p class="content_text">завдання зі зворотним зв'язком</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>


const name = ref({
    data:'',
    isValid:true
});
const number = ref({
    data:'',
    isValid:true
});
const email = ref({
    data:'',
    isValid:true
});

const success = ref(false);
const errorMessage = ref('');
const errorTrigger = ref(false)

async function submitForm(){
    if(name.value.data === '' && number.value.data === '' && email.value.data === '' ){
        name.value.isValid = false;
        number.value.isValid = false;
        email.value.isValid = false
        return
    };
    
    const data = await fetch('https://7eminar.ua/api/clients/campaign/test',{
        method:'POST',
        body:JSON.stringify({
            email: email.value.data,
            name: name.value.data,
            phone: number.value.data
        })
    });
    name.value.data = '';
    email.value.data = '';
    number.value.data = ''
    if(!data.ok && data.status == 429){
        errorTrigger.value = true;
        errorMessage.value = 'Забагато спроб, спробуйте пізніше'
        
    }
    if(data.ok){
        success.value = true
    }
    
    
}



</script>
<style scoped lang="scss">
.container{
    padding-top: 32px;
    margin-bottom: 56px;
    background-color: white;
    @media screen and (min-width: 768px){
        padding-top: 32px;
        margin-bottom: 176px;
        padding-bottom: 32px;
    }
}
.form{
    max-width: 1140px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin: 0 auto;
    gap: 64px;
    align-items: center;
    @media screen and (min-width: 768px){
        flex-direction: row;
        align-items: normal;
    }
    &_main{
        display: flex;
        flex-direction: column;
        max-width: 100%;
        align-items: center;
        max-width: 536px;
    }
    &_inputs{
        padding-left: 24px;
        padding-right: 24px;
    }
    &_text{
        display: flex;
        flex-direction: column;
        max-width: 513px;
    }
    &_content{
        padding-left: 32px;
        padding-right: 32px;
    }
}
.inputs_title,
.content_title{
    color: #232323;
    font-size: 23px;
    font-family: e-Ukrainian;
    font-weight: 700;
    line-height: 33.60px;
    word-wrap: break-word;
    @media screen and (min-width: 768px){
       line-height: 34.50px; 
    }
}
h3{
  
    font-size: 16px;
    font-family: e-Ukrainian;
    font-weight: 700;
    line-height: 33.60px;
    word-wrap: break-word;
    padding-top: 10px;
    color: rgb(52, 179, 52);
    @media screen and (min-width: 768px){
       line-height: 34.50px; 
    }  
}
.error{
    font-size: 16px;
    font-family: e-Ukrainian;
    font-weight: 700;
    line-height: 33.60px;
    word-wrap: break-word;
    padding-top: 10px;
    color: rgb(218, 41, 21);
    @media screen and (min-width: 768px){
       line-height: 34.50px; 
    }  
}

.input{
    display: flex;
    flex-direction: column;
    gap: 7px;


    &_content{
        padding-top: 24px;
        display: flex;
        flex-direction: column;
        gap: 16px;
    }
    &_label{
        color: #232323;
        font-size: 16px;
        font-family: Raleway;
        font-weight: 400;
        line-height: 30px;
        word-wrap: break-word   
    }
    &_place{
        border: 1px #232323 solid;
        border-radius: 32px;
        padding: 15px 24px 15px 24px;
    }
    &_btn{
        margin-top: 24px;
    }
}
.content{
    &_block{
        max-width: 423px;
        display: flex;
        flex-direction: column;

    }
    &_pair{
        display: flex;
        flex-direction: row;
        gap: 40px;
    }
    &_last{
        color: #0066CC;
        font-size: 39px;
        font-family: Raleway;
        font-weight: 700;
        line-height: 36px;
        word-wrap: break-word;
        padding-top: 16px;
        @media screen and (min-width: 768px){
        line-height: 58.50px;
    }
    }
    &_main{
        color: #0066CC;
        font-size: 63px;
        font-family: e-Ukrainian;
        font-weight: 600;
        line-height: 94.50px;
        word-wrap: break-word
    }
    &_text{
        color: #232323;
        font-size: 17px;
        font-family: Raleway;
        font-weight: 400;
        line-height: 25.50px;
        word-wrap: break-word

    }
}
.validation{
    color: #EB5757;
    font-size: 16px;
    font-family: Raleway;
    font-weight: 400;
    line-height: 30px;
    word-wrap: break-wor 
}
.input_validation{
    border: 1px #EB5757 solid;
    border-radius: 32px;
    padding: 15px 24px 15px 24px;
}
</style>