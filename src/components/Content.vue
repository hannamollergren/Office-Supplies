<template>
	<div>
		<div class="container">
			<div class="sidebar">
				<a href="#">Paper clips</a>
				<a href="#">Post-it notes</a>
				<a href="#">Staples</a>
				<a href="#">Hole punches</a>
				<a href="#">Binders</a>
				<a href="#">Staplers</a>
				<a href="#">Laminators</a>
				<a href="#">Writing utensils</a>
				<a href="#">Paper</a>
				<a href="#">Computers</a>
				<a href="#">Printers</a>
				<a href="#">Fax machines</a>
				<a href="#">Photocopiers</a>
				<a href="#">Cash registers</a>
				<a href="#">Office furniture</a>
				<a href="#">Chairs</a>
				<a href="#">Cubicles</a> 
				<a href="#">Filing cabinet</a> 
				<a href="#">Armoire desks</a> 
			</div>
			<div class="images">
				<img src="../assets/paper1.jpg" alt="Product image" height="300px" width="300px" class="large-image"><br>
				<img src="../assets/paper1.jpg" alt="Product image" height="50px">
				<img src="../assets/paper2.jpg" alt="Product image" height="50px">
				<img src="../assets/paper3.jpg" alt="Product image" height="50px">
			</div>
			<div class="info">
				<h2>Paper</h2>
				<div class="info-container">
					<h3 class="price">599 kr</h3>
					<div class="options-container">
						<select id="cars" name="cars" class="options">
							<option value="white" selected>White</option>
							<option value="red">Red</option>
							<option value="blue" >Blue</option>
							<option value="pink">Pink</option>
						</select>
					</div>
				<button class="btn-buy" @click="addCartButton">Buy</button>
			</div>
				<p class="info-text">
					Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra justo commodo. Proin sodales pulvinar tempor. <br><br>
					Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Nam fermentum.
					<span v-if="!isHidden">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra justo commodo. Proin sodales pulvinar tempor. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Nam fermentum, nulla luctus pharetra vulputate, felis tellus mollis orci, sed rhoncus sapien nunc eget odio.
					</span>
					<button class="btn-more" @click="isHidden = !isHidden">Read more</button>
				</p>
			</div>
		</div>
	</div>
	
</template>

<script>
export default {
	data: () =>({
		cart: 0,
		amount: 0,
		isHidden: Boolean(true),
	}),
	methods: {
		addCartButton(){
			this.cart += 1;
			this.amount += 599;
			this.$emit('click', this.cart, this.amount)
		}
	}
}
</script>


<style scoped>
@import url('https://fonts.googleapis.com/css?family=Alice&display=swap');
.container{
	display: grid;
	grid-template-columns: 1fr 2fr 3fr;
	margin: 0 0 3em;

}
p{
	font-family: 'Alice', serif;
}
.sidebar{
	width: 250px;
	height: 440px;
	border: 2px solid #ED2B91;
	border-radius: 3px;
	padding: 1em;
	margin: 0 0 3em 2em;
	display: inline-block;
}
a{
	display: block;
	text-align: start;
	padding: 0.1em;
}
a:hover{
	background-color: rgb(214, 213, 213);
	transition: 0.2;
}
.images{
	padding: 2em;
	margin: 0 0 0 2em;
	background-color: white;
}
.large-image{
	margin: 0 0 1em 0;
}
.info{
	background-color: white;
	padding: 2em;
	margin: 0 2em 0 0;
}
.info-container{
	border: 1px solid #333333;
	padding: 1em;
	margin: 1em 0 0 0;
	display: grid;
	grid-template-columns: 1fr 2fr 1fr;
}
.price{
	display: flex;
	align-items: center;
	justify-content: start;
}
.options-container{
	display: flex;
	align-items: center;
}
.options{
	
	margin: 0 1em 0;
	width: 60%;
}
.btn-buy{
	grid-column: 3/3;
}
.info-text{
	margin: 1em 0 0;
}
.btn-more{
	display: flex;
	justify-content: center;
	border: 2px solid #ED2B91; 
	background-color: transparent;
	color: #333333;
	margin: 2em 0 0;
}


</style>