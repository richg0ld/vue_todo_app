<template>
  <div id="app">
    <todo-list></todo-list>
  </div>
</template>

<script>
import TodoList from './TodoList'

export default {
  name: 'app',
  components: {
    TodoList
  }
}
</script>

<style>
/* reset */
body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,form,fieldset,legend,textarea,p,th,td,input,select,textarea,button{margin:0;padding:0}
html,body{width:100%;height:100%}
body{font-family:'Nanumgothic','돋움',dotum,tahoma,sans-serif;font-size:12px;line-height:1.5;color:#000}
fieldset,img{border:0 none;vertical-align:top}
dl,ul,ol,menu,li{list-style:none}
button{overflow:visible;border:0 none;background-color:transparent;cursor:pointer;font-family:'Nanumgothic','나눔고딕','돋움',dotum,tahoma,sans-serif}
button::-moz-focus-inner{padding:0;border:0}
address,caption,em{font-style:normal}
a{color:#000;text-decoration:none}
a:focus,a:active,a:hover{color:#000;text-decoration:underline}
table{border-collapse:collapse;table-layout:fixed;border-spacing:0}
hr{display:none}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
