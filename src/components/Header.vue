<template>
	<div>
		<header>
			<div class="container">
				<img src="../assets/Logo.png" alt="Logo" height="40px">
				<input type="text" placeholder="Search here">
				<div class="cart">
					<img src="../assets/shopping-bag.png" alt="Shopping bag" height="20px">
					<p>({{cart}}) </p>
					<p>
						<span> {{amount}} kr</span>
					</p>
				</div>
				<button>Check out</button>
			</div>
			<nav>
				<a href="#">All our products</a>
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
img{
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
@media only screen and (max-width: 990px) {
	
}
</style>