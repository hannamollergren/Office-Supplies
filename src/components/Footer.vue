<template>
	<div>
		<footer>
			<img src="../assets/Logo.png" alt="Logo" height="40px" class="logo">
			<p class="paragraph">
				Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra justo commodo. Proin sodales pulvinar tempor. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Nam fermentum, nulla luctus pharetra vulputate, felis tellus mollis orci, sed rhoncus sapien nunc eget odio.
			</p>
			<div class="best-sellers">
				<span>Bestsellers</span>
				<ul>
					<li><a href="#">A4</a></li>
					<li><a href="#">A5</a></li>
					<li><a href="#">Pens</a></li>
					<li><a href="#">Staplers</a></li>
				</ul>
			</div>
			<div class="best-sellers1">
				<ul>
					<li><a href="#">A4</a></li>
					<li><a href="#">A5</a></li>
					<li><a href="#">Pens</a></li>
					<li><a href="#">Staplers</a></li>
				</ul>
			</div>
			<div class="social-media">
				<span>We're social!</span>
				<p class="social-item">
					<img src="../assets/fb.png" height="20px" alt="Icon FB" class="icon"><a href="#">Facebook</a>
				</p>
				<p class="social-item">
					<img src="../assets/twitter.png" height="20px" alt="Icon Twitter" class="icon"><a href="#">Twitter</a>
	
				</p>
				<p class="social-item">
					<img src="../assets/linkedin.png" height="20px" alt="Icon LinkedIn" class="icon"><a href="#">LinkedIn</a>
					
				</p>
			</div>
		</footer>
	</div>
</template>

<script>
export default {
	data: () =>({

	})
}
</script>

<style scoped>
p, li{
	color: #CBBBA0;
}
footer{
	background-color: #0FA7BA;
	padding: 2em;
	display: grid;
	grid-template-columns: 2fr 1fr 1fr 1fr;
}
.logo{
	margin: 1em 0 1em 0;
}
.paragraph{
	margin: 0 0 1em 0;
	grid-column: 1/2;
	text-align: start;
}
.best-sellers{
	text-align: start;
	margin: 0 0 0 5em;
	grid-column: 2/2;
}
.best-sellers1{
	text-align: start;
	margin: 1.2em 0 0 2em;
	grid-column: 3/3;
}
span{
	font-weight: bold;
	color: #CBBBA0;
}
li{
	padding: 0.2em;
}
a{
	color: #CBBBA0;
}
.social-media{
	text-align: start;
	grid-column: 4/4;
}
.social-item{
	padding: 0.2em;
	display: block;
}
.icon{
	margin: 0 0.3em 0 0;
}

@media only screen and (max-width: 990px) {
.logo{
	margin: 0 0 1em 0;
	grid-column: 1/5;
}
.paragraph{
	margin: 0 0 1.2em 0;
	grid-column: 1/5;
	text-align: start;
}
.best-sellers{
	text-align: start;
	margin: 0 0 0 1em;
	grid-column: 1/5;
}
.best-sellers1{
	text-align: start;
	margin: 1em 0 1em 1em;
	grid-column: 1/5;
}
.social-media{
	text-align: start;
	grid-column: 1/5;
}

}
</style>