<template>
    <div class="container">
        <div class="main">
            <h1>Навчання, яке працює!</h1>
            <h1>Відкрийте для себе найпопулярніші курси</h1>
            <div class="timeline">
    <div class="labels">
      <div class="label">Ціни раннього бронювання</div>
      <div class="label">Подорожчання на 10%</div>
      <div class="label">Подорожчання на 15%</div>
      <div class="label">Квитки вже закінчаться</div>
    </div>
    <div class="line">
        <div class="markers">
      <div class="marker" style="left: 0%;"></div>
      <div class="marker" style="left: 20%;"></div>
      <div class="marker" style="left: 50%;"></div>
      <div class="marker" style="left: 80%;"></div>
      <div class="marker" style="left: 100%;"></div>
    </div>
      <div class="crosshair" :style="{ left: crosshairPosition }">
        <img src="../public/images/time1.png">
        <div class="dot">
            <img src="../public/images/time2.png">
        </div>
      </div>
    </div>
    <div class="dates">
      <div class="date">21 серпня</div>
      <div class="date">1 вересня</div>
      <div class="date">15 вересня</div>
      <div class="date">3 жовтня</div>
    </div>
  </div>
        </div>
    </div>
</template>
<script setup>
const crosshairPosition = ref('0%');

const startDate = new Date(2023, 7, 21); 
const finalDate = new Date(2023, 9, 3);  

const currentDate = new Date();
if (currentDate < startDate) {
  crosshairPosition.value = '0%';
} else if (currentDate > finalDate) {
  crosshairPosition.value = '100%';
} else {
  const totalDays = (finalDate - startDate) / (1000 * 60 * 60 * 24);
  const passedDays = (currentDate - startDate) / (1000 * 60 * 60 * 24);
  const progress = (passedDays / totalDays) * 100;
  crosshairPosition.value = `${progress}%`;
}


const updateCrosshairPosition = () => {
  const currentDate = new Date();
  if (currentDate < startDate) {
    crosshairPosition.value = '0%';
  } else if (currentDate > finalDate) {
    crosshairPosition.value = '100%';
  } else {
    const totalDays = (finalDate - startDate) / (1000 * 60 * 60 * 24);
    const passedDays = (currentDate - startDate) / (1000 * 60 * 60 * 24);
    const progress = (passedDays / totalDays) * 100;
    crosshairPosition.value = `${progress}%`;
  }
};

const interval = setInterval(updateCrosshairPosition, 24 * 60 * 60 * 1000); 

onMounted(() => {
  updateCrosshairPosition();
});

onBeforeUnmount(() => {
  clearInterval(interval);
});

</script>
<style scoped lang="scss">
.container{
    padding-top: 104px;
    background-color: white;
    padding-bottom: 80px;
}
.main{
    padding-top: 80px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
    max-width: 1094;
    padding: 20px;
}
h1{
    color: #232323;
    font-size: 24px;
    font-family: e-Ukrainian;
    font-weight: 700;
    line-height: 36px;
    text-align: center;
    word-wrap: break-word;
    @media screen and (min-width: 768px){
      line-height: 63px;
font-size: 42px;
 
    }
}
.timeline {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 58px;
  width: 100%;
  @media screen and (max-width: 768px){
    padding-top: 28px;
  } 
}

.labels {
  display: flex;
  justify-content: space-between;
  width: 100%;
  max-width: 800px;
  padding-bottom: 38px;
  @media screen and (max-width: 768px){
    flex-direction: column;
  }
}

.label {
  text-align: center;
  flex: 1;
  font-size: 12px;
  margin-bottom: 10px;
  color: #232323;
font-size: 18px;
font-family: Raleway;
font-weight: 400;
line-height: 23.40px;
word-wrap: break-word;
}

.line {
  position: relative;
  width: 100%;
  max-width: 800px;
display: flex;
  height: 6px; /* Высота линии */
  background-color: rgba(0, 0, 0, 0.05);
  @media screen and (max-width: 768px){
    transform: rotate(90deg);
    width: 300px;
  } /* Цвет линии */
}

.progress-bar {
    position: re;
  width: calc(50% - 1px); /* 50% ширины линии - 1px (чтобы не перекрывать маркер) */
  height: 100%;
  background: linear-gradient(to right, black 50%, rgba(0, 0, 0, 0.05) 50%); /* Градиентный фон */
  border: 2px solid black; /* Толщина и цвет границы */
  z-index: -1;
  left: 0; 
}

.mark {
    position: absolute;
  width: 2px;
  height: 20px;
  background-color: black;
  transform: translateX(-1px);
  z-index: 1;
}


.markers {
  position: absolute;
  top: 0; /* Размещаем над линией */
  left: 0;
  width: 100%;
  height: 100%;
}

.marker {
  position: absolute;
  top: 50%; /* Размещаем по центру вертикально */
  transform: translateY(-50%);
  width: 2px; /* Ширина отметки */
  height: 20px; /* Высота отметки */
  background-color: #000; /* Цвет отметки */
  width: 3px;
  
}

.crosshair {
  position: absolute;
  top: -5px;
  width: 20px;
  height: 20px;
  transform: translateX(-50%);
  transition: left 0.5s ease-in-out;
}

.crosshair img {
  width: 100%;
  height: 100%;
  
}

.dot {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 8px; /* Размер точки */
  height: 8px;
  background-color: yellow; /* Цвет точки */
  border-radius: 50%;
}

.dates {
  display: flex;
  justify-content: space-between;
  width: 100%;
  max-width: 800px;
  margin-top: 35px;
  color: gray;
  font-size: 12px;
  @media screen and (max-width: 768px){
    flex-direction: column;
  }
}
.date{
    color: #232323;
font-size: 18px;
font-family: Raleway;
font-weight: 700;
line-height: 23.40px;
word-wrap: break-word
}

</style>