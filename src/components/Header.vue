<template>
	<div>
		<header>
			<div class="container">
				<img src="../assets/hamburger.png" alt="" id="hamburger" height="20px">
				<img src="../assets/Logo.png" alt="Logo" height="40px" class="logo">
				<input type="text" placeholder="Search here">
				<div class="cart">
					<img src="../assets/shopping-bag.png" alt="Shopping bag" height="20px" class="bag-icon">
					<p>({{cart}}) </p>
					<p>
						<span class="amount"> {{amount}} kr</span>
					</p>
				</div>
				<button>Check out</button>
			</div>
			<nav>
				<a href="#" class="first-link">All our products</a>
				<a href="#"> Inspiration for the office</a>
				<a href="#">About OS</a>
			</nav>
		</header>
	</div>
</template>

<script>
export default {
	props:{
		cart: Number(0),
		amount: Number(0)
	}
}
</script>

<style scoped>
header{
	padding: 2em;
}
.container{
	display: grid;
	grid-template-columns: repeat(5, 1fr);
	margin: 0 0 1.2em;
}
.logo{
	grid-column: 1/1;
	margin: 0 0.5em 0 0;
}
input{
	margin: 0 0 0 3em;
	padding: 0.8em;
	border: none;
	width: 100%;
	grid-column: 2/4;
}
span{
	font-weight: bold;
}
.cart{
	display: flex;
	justify-content: center;
	align-self: center;
	grid-column: 5/5;
	margin: 0 1em 0 0;
}
.bag-icon{
	margin: 0 0.3em 0 0;
}
.amount{
	margin: 0 0 0 0.3em;
}
button{
	width: 100%;
	margin: 0 2em 0 0;
	grid-column: 6/6;
}
nav{
	display: block;
	text-align: start;
}
a{
	margin: 0 0.5em 0;
}
.first-link{
	margin: 0 0 0;
}
#hamburger{
	display: none;
}
@media only screen and (max-width: 990px) {
.container{
	grid-template-columns: repeat(3, 1fr);
}
nav{
	display: none;
}
input{
	display: none;
}
button{
	display: none
}
.cart{
	grid-column: 3/3;
	margin: 0;
	justify-content: flex-end;
}
.amount{
	display: none;
}
.logo{
	grid-column: 2/2;
	height: 30px;
	margin: auto;
}
#hamburger{
	display: flex;
	justify-content: center;
	align-self: center;
	grid-column: 1/1;
	display: block;
}
#hamburger:hover{
	cursor: pointer;
}
}
@media only screen and (max-width: 500px) {
.logo{
	grid-column: 2/2;
	height: 25px;
}
}
</style>