<template>
  <div id="app">
    <Header/>
	<Content/>
	<Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Content from './components/Content.vue'
import Footer from './components/Footer.vue'


export default {
  name: 'App',
  components: {
    Header, Content, Footer
  },
  data: () => ({
	
  })
}
</script>

<style>
*{
	box-sizing: border-box;
	padding: 0;
	margin: 0;
}
#app {
	height: 100vh;
	background-color: #F3F3F2;
	font-family: sans-serif, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #333333;
}
button{
	background: #0FA7BA;
	padding: 12px 28px;
	color: white;
	border: none;
	font-size: 0.9em;
}
button:hover{
	background: #1591A0;
	transition: 0.5s;
	cursor: pointer;
}
</style>
