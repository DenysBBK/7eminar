<template>
  <div class="wrapper">
   <Main/>
   <Timeline/>
   <Table/>
   <Form/>
  </div>
</template>
<style>
* {
  padding: 0px;
  margin: 0px;
  border: 0px;
}
*,
*:before,
*:after {
  box-sizing: border-box;
}
:focus,
:active {
   outline: none;
}
a:focus,
a:active {
   outline: none;
}
html,
body {
  height: 100%;
}
body {
  line-height: 1;
  font-family: 'Nunito';
}
input,
button,
textarea {
  font-size: inherit;
  
}
button {
  cursor: pointer;
  color: inherit;
  font-family: 'Nunito';
  background-color: transparent;
}
a {
  color: inherit;
  text-decoration: none;
}
ul li {
  list-style: none;
}
img {
  vertical-align: top;
}
h1,
h2,
h3,
h4,
h5,
h6 {
  font-weight: inherit;
  font-size: inherit;
}
.wrapper {
  min-height: 100%;
  background-color: #FAFAFA;
  flex-direction: column;
  overflow: hidden;
 
}
</style>
