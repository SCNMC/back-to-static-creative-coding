<section>
	<ul>
		<a href="/week1"><li>Week 1</li></a>
		<a href="/week2"><li> Week 2</li></a>
		<a href="/week3"><li>Week 3</li></a>
	</ul>
</section>

<style>
	section {
		background: #16222a; /* fallback for old browsers */
		background: -webkit-linear-gradient(
			to right,
			#3a6073,
			#16222a
		); /* Chrome 10-25, Safari 5.1-6 */
		background: linear-gradient(
			to right,
			#3a6073,
			#16222a
		); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
		height: 78vh;
    display: flex;
  justify-content: center;
		align-items: center;
	}

    ul{
        display: flex;
        gap: 3em;
        color: white;
    }

    li{
font-size: 1em;
    }
	@media (min-width: 70rem) {
		section {
			margin-top: -10em;
		}
		li{
			font-size: 4em;
		}
	}
</style>
