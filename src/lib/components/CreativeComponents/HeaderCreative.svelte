<section>
	<ul>
		<a href="/week1"><li>Week 1</li></a>
		<li> Week 2</li>
		<li>Week 3</li>
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
font-size: 1.5em;
    }
	@media (min-width: 70rem) {
		section {
			margin-top: -18em;
		}
	}
</style>
