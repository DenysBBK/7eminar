<template>
    <div class="desktop">
        <TableViewDesktop
        :hours="fullHours"
        :minutes="fullMinutes"
        :seconds="fullSeconds"/>
    </div>
    <div class="mobile">
        <TableViewMobile
        :hours="fullHours"
        :minutes="fullMinutes"
        :seconds="fullSeconds"
        />
    </div>
</template>
<script setup>
const hours = ref('');
const minutes = ref('');
const seconds = ref('');
const today = ref(new Date());
const nesDate = computed(() => {
    return new Date(2023,9,3,0,0,0)
})
const fullSeconds = computed(() => seconds.value <10 ? `0${seconds.value}` : seconds.value);
const fullMinutes = computed(() => minutes.value <10 ? `0${minutes.value}` : minutes.value);
const fullHours = computed(() => hours.value <10 ? `0${hours.value}` : hours.value);

const timer = setInterval(() => {
    const difference = ref(nesDate.value - today.value);
    if(today.value < nesDate.value){
    hours.value = Math.floor((difference.value / (1000 * 60 * 60)));
    minutes.value = Math.floor((difference.value / (1000 * 60)) % 60);
    seconds.value = Math.floor((difference.value / 1000) % 60); 
    today.value = new Date() 
    }
    if(today.value >= nesDate.value){
    hours.value = '00';
    minutes.value = '00';
    seconds.value = '00'
    clearInterval(timer)
    }

}, 1000);  


</script>
<style scoped lang="scss">
@import url("https://fonts.googleapis.com/css?family=Raleway:100,200,300,regular,500,600,700,800,900,100italic,200italic,300italic,italic,500italic,600italic,700italic,800italic,900italic" );

.container{
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
.mobile{
    @media screen and (min-width: 900px){
        display: none;
    }
}
.desktop{
    @media screen and (max-width: 900px){
        display: none;
    }
}

</style>