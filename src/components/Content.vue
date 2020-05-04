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
				<img :src='image1' alt="Product image" height="300px" width="300px" class="large-image"><br>
				<img src="../assets/paper1.jpg" alt="Product image" height="90px" class="image1" @click="changeImage1">
				<img src="../assets/paper2.jpg" alt="Product image" height="90px" class="image2" @click="changeImage2">
				<img src="../assets/paper3.jpg" alt="Product image" height="90px" class="image3"  @click="changeImage3">
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
					Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Nam fermentum et magnis dis parturient montes, nascetur ridiculus mus. Nam fermentum, nulla luctus pharetra vulputate, felis tellus mollis orci, sed rhoncus sapien nunc eget odio. nulla luctus pharetra vulputate.<br>
					<span v-if="!isHidden">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra justo commodo. Proin sodales pulvinar tempor. Cum sociis natoque penatibus.<br><br>
						Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra justo commodo. Proin sodales pulvinar tempor. Cum sociis natoque penatibus et magnis dis parturient montes, nascetu
					</span>
					<button class="btn-more" @click="isHidden = !isHidden">Read more</button>
				</p>
			</div>
		</div>
		<div class="container-boxes">
				<div class="box1">
					<h3 class="title">Paper is awesome!</h3>
					<p>
						Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra justo commodo. Proin sodales pulvinar tempor. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Nam fermentum, nulla luctus pharetra vulputate, felis tellus mollis orci, sed rhoncus sapien nunc eget odio.
					</p>
				</div>
				<div class="box2">
					<h3 class="title">Paper is awesome!</h3>
					<p>
						Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet.
					</p>
				</div>
				<div class="box3">
					<h3 class="title">Paper is awesome!</h3>
					<p>
						Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet la.
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
		image1: 'https://lh3.googleusercontent.com/BIO6M_BdlnAPgTrm_om1aZpZaEzGwuanb9s0gdRAQ1C6090xWUVq9Rk34J_XSASZ3owJRx1-FJH0gsBNgTgnFDa33Jvjp4DCaPvrJ5kAfjNavBD0p1n7v6cvg58s3r3Y1QMCWnWAUw=w2400',
		image2: 'https://lh3.googleusercontent.com/JhwfYAwIVlacD-_mehDwGrAFByFxC_ytHP0dcPD0vALvqpsrvnz5nJ8S6YE402w4pxhLriKehy49dXnfZBmvIEye9RzVHJ1GJTkuXgLLsp8WgUw4x8GlCGcX0aWwMHYWAIbY-ffGHA=w2400',
		image3: "https://lh3.googleusercontent.com/83eair2sysjXX33UnvfskCkc5Nt6shXoOv77ckW0YOZuEmlvMTIZanKjD08QGseeneVepTI8epYoRY2ZMrxacznQA3BxqEh2sukQNevmR-6eGquQx8s3lC5DNUZywIUyeqy75YiZDQ=w2400"
		
	}),
	methods: {
		addCartButton(){
			this.cart += 1;
			this.amount += 599;
			this.$emit('click', this.cart, this.amount)
		},
		changeImage1(){
			this.image1 = 'https://lh3.googleusercontent.com/BIO6M_BdlnAPgTrm_om1aZpZaEzGwuanb9s0gdRAQ1C6090xWUVq9Rk34J_XSASZ3owJRx1-FJH0gsBNgTgnFDa33Jvjp4DCaPvrJ5kAfjNavBD0p1n7v6cvg58s3r3Y1QMCWnWAUw=w2400';
		},
		changeImage2(){
			this.image1 = this.image2;
		},
		changeImage3(){
			this.image1 = this.image3;
		}
	}
}
</script>


<style scoped>
@import url('https://fonts.googleapis.com/css?family=Alice&display=swap');
.container{
	display: grid;
	grid-template-columns: 1fr 2fr 3fr;
	margin: 0 0 2em;

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
.image1{
	margin: 0 0.8em 0 0;
}
.image2{
	margin: 0 0.9em 0 0;
}
img:hover{
	cursor: pointer;
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
	grid-column: 1/1;
}
.options-container{
	display: flex;
	align-items: center;
	grid-column: 2/2;
}
.options{
	margin: 0 1em 0;
	width: 80%;
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
.container-boxes{
	display: grid;
	grid-template-columns: repeat(3, 1fr);
	margin: 1em 2em 3em 313px;
	gap: 1em;
	
}
.box1{
	background-color: white;
	padding: 2em;
	grid-column: 1/1;
}
.box2{
	background-color: white;
	padding: 2em;
	grid-column: 2/2;
}
.box3{
	background-color: white;
	padding: 2em;
	grid-column: 3/3;
}
.title{
	margin: 0 0 1em;
}
@media only screen and (max-width: 1055px) {
.price{
	grid-column: 1/4;
	justify-content: center;
	margin: 0 0 0.7em;
}
.options-container{
	grid-column: 1/4;
	margin: 0 0 0.8em;
}
.options{
	margin: 0 1em 0;
	width: 100%;
}
.btn-buy{
	grid-column: 1/4;
}
}
@media only screen and (max-width: 990px) {
.container{
	display: grid;
	grid-template-columns: 1fr 2fr;
	margin: 0 0 2em;
}
.sidebar{
	display: none;
}
.container-boxes{
	display: grid;
	grid-template-columns: repeat(3, 1fr);
	margin: 1em 2em 3em 2em;
	gap: 1em;	
}
}
@media only screen and (max-width: 700px) {
.info{
	grid-column: 1/4;
	margin: 0 2em 0 2em;
}
.images{
	grid-column: 1/4;
	margin: 0 2em 0 2em;
}
.box1{
	grid-column: 1/4;
}
.box2{
	grid-column: 1/4;
}
.box3{
	grid-column: 1/4;
}
}


</style>