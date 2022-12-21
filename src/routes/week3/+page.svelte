<script>
    import { onMount } from "svelte";
	import { gsap } from "gsap/dist/gsap";
    onMount(() => {
	

		
	});
</script>

<body>
	<header>
		<h1>Creative </h1>
		<p>Coding</p>
		<nav>
			<ul>
				<li>About</li>
				<li>Info</li>
				<li>Menu</li>
			</ul>
		</nav>
	</header>

	<section>
		<h2>creative
        </h2>
		<img src="/assets/img1.jpg" alt="image" />
	</section>
   <section class="extra-info">
    <p>much creative</p>
    <p>very creative</p>
   </section>
</body>

<style>
	@font-face {
		font-family: "Monument Extended";
		src: url("/assets/Fonts/MonumentExtended-Regular.otf");
	}
    @font-face {
		font-family: "Voyage";
		src: url("/assets/Fonts/Voyage.ttf");
	}
    @font-face {
    font-family: 'NewYork';
    src:url('/assets/Fonts/NewYork.otf');
}

	header {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;
		gap: 1em;
		padding: 2em 2em;
        font-family: "Monument Extended";
	}
	ul {
		display: flex;
		flex-direction: row;
		gap: 1em;
	}
    body{
        background: #bebeb8;
        height: 100vh;
    }
	* {
		color: #000;
	}
	p {
		font-size: 1em;
        font-family: "Monument Extended";
	}
    h2 {
		position: absolute;
		background: none;
        font-size: 8em;
        font-family: "NewYork";
        font-weight: 200;
        color: 	#2584ec;
	}
	h1 {
		font-size: 1em;
	}
	section {
		display: flex;
		align-items: center;
		justify-content: center;
        flex-direction: column;
	}

	img {
		padding: 1em 2em;
		width: 70%;
		height: 60vh;
		object-fit: cover;
	}
    .extra-info{
            display: flex;
            flex-direction: row;
         justify-content: space-between;
         align-items: stretch;
         padding: 2em 5em;
        }

	@media (min-width: 70rem) {
		header {
			display: flex;
			flex-direction: row;
			align-items: center;
			justify-content: first baseline;
			padding: 3em 5em;
		}
		ul {
			display: flex;
			flex-direction: row;
			/* font-size: 1.2em; */
		}
		p {
			font-size: 1.5em;
		}
		h1 {
			font-size: 1.5em;
		}
        h2 {
		position: absolute;
		background: none;
        font-size: 17em;
        font-family: "NewYork";
        font-weight: 200;
        color: 	#2584ec;
	}
		section {
			display: flex;
			align-items: center;
			justify-content: center;
		}
		img {
			padding: 3em 4em;
			width: 30%;
			height: 65vh;
			object-fit: cover;
		}
        .extra-info{
            display: flex;
            flex-direction: row;
         justify-content: space-between;
         align-items: stretch;
         padding: 2em 5em;
        }
	}
</style>
