<script>
	import { onMount } from "svelte";
	import { gsap } from "gsap/dist/gsap";
  import { scale } from "svelte/transition";
	onMount(() => {
		var textWrapper = document.querySelector("h2");
		textWrapper.innerHTML = textWrapper.textContent.replace(
			/\S/g,
			"<span class='letter'>$&</span>"
		);

		gsap.timeline().add({
			targets: ".title .letter  h2",
			translateY: [100, 0],
			translateZ: 0,
			opacity: [0, 1],
			easing: "easeOutExpo",
			duration: 2000,
			delay: (el, i) => 4800 + 40 * i,
		});

		gsap.to(".background", 2.4, {
			y: "-100%",
			ease: "Expo.easeInOut",
			delay: 1,
		});

		gsap.to("img", 4, {
			scale: "1",
			ease: "Expo.easeInOut",
			delay: 0,
		});

		gsap.to("img", 2.4, {
			width: "500",
			height: "700",
			ease: "Expo.easeInOut",
			delay: 3.4,
		});

		gsap.from("img", 0.4, {
			opacity: 0,
			ease: "Expo.easeInOut",
			delay: 3.4,
		});

		gsap.from(
			"header , .extra-info",
			2,
			{
				opacity: 0,
				y: 30,
				ease: "Expo.easeInOut",
				delay: 4.2,
			},
			0.1
		);
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
		<div class="background" />
		<img src="/assets/img1.jpg" alt="image" />
        <h2>creative </h2>
	</section>
	<section class="extra-info">
		<p>much creative</p>
		<p>very creative</p>
	</section>
</body>

<style>

	.title .letter {
		display: inline-block;
		line-height: 1em;
	}
	@font-face {
		font-family: "Monument Extended";
		src: url("/assets/Fonts/MonumentExtended-Regular.otf");
	}
	@font-face {
		font-family: "Voyage";
		src: url("/assets/Fonts/Voyage.ttf");
	}
	@font-face {
		font-family: "NewYork";
		src: url("/assets/Fonts/NewYork.otf");
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
    h1{
        font-family: "Monument Extended";
    }
	ul {
		display: flex;
		flex-direction: row;
		gap: 1em;
	}
	body {
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
		color: #2584ec;
	}
	h1 {
		font-size: 1em;
	}
	.background {
		background: #bebeb8;
		opacity: 1;
		position: absolute;
		top: 0;
		bottom: 0;
		right: 0;
		left: 0;
		z-index: 2;
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
	.extra-info {
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
			color: #2584ec;
		}
		section {
			display: flex;
			align-items: center;
			justify-content: center;
		}
		img {
			width: 70%;
			height: 60vh;
		}
		.extra-info {
			display: flex;
			flex-direction: row;
			justify-content: space-between;
			align-items: stretch;
			padding: 2em 5em;
            margin-top: -3em;
		}
	}
</style>
