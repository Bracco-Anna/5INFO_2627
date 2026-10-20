<main>
	<header>
	<h1>Web App</h1>
	</header>

	<section>
	<nav>
		<ul>
			<li><a href="/chi_sono">Chi sono</a></li>
			<li><a href="/input">Input</a></li>
			<li><a href="/counter">Counter</a></li>
			<li><a href="#">About</a></li>

		</ul>
	</nav>
	<article>
	<slot />
	</article>
</section>
<footer>
	<h4>copyright &copy; Anna Bracco</h4>

</footer>
</main>



<style>
:global(body){
	margin: 0;
}
main{
	display: flex;
	flex-direction: column;
	height: 100vh;
	box-sizing: border-box;
	color: white;
}
header{
	background-color: #eeace3;
	text-align: center;
}
section {
	display: flex;
	flex-direction: row;
	flex: 10;
}
nav {
	background-color: #f190f1;
}
nav ul{
	list-style: none;
}
nav ul li{
	padding: 10px;
}
nav ul li a {
	color: white;
	text-decoration: none;
	font-size: 30px;
	font-weight: bolder;
}
article {
	color: #e084e0;
	text-align: center;
	font-size: 20px;
	flex: 1;
}

footer {
	background-color: #eeace3;
	text-align: center;
	font-size: 20px;
	flex: 1;
}
</style>