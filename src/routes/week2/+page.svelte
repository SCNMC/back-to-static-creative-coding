<script>
	import Animatedhamburger from "$lib/components/Animatedhamburger.svelte";
	import { fly } from "svelte/transition";
    import { onMount } from 'svelte';

	export let open = false;
	export let onClick = () => {
		open = !open;
	};


</script>

<header>
    <h1>CRAZY ACID MENU</h1>
	<Animatedhamburger {open} {onClick} />
	{#if open}
		<nav  class="mouse-cursor-gradient-tracking" transition:fly={{ x: 1000, duration: 500 }}>
			<a transition:fly={{y:1000, duration:1100}} href=".#">CREATIVE</a>
			<a transition:fly={{y:800, duration:1100}} href=".#">CODING</a>
			<a transition:fly={{y: 600, duration:1100}}  href="#">IS REALLY</a>
			<a transition:fly={{y:400, duration:1100}}  href=".#"
				>FUN TO DO</a
			>
		</nav>
	{/if}
</header>

<style>
	h1 {
        color: white;
		font-size: 1.5em;
	}
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin: 0.4em 2.5em;
		position: relative;
		transition: linear 0.4s;
		z-index: 2;
	}

	nav {
		position: fixed;
		display: flex;
		gap: 2em;
		align-items: center;
		justify-content: center;
		flex-direction: column;
        background-color: #985bb9;
background-image: radial-gradient(at 28% 2%, hsla(199, 85%, 61%, 1) 0, hsla(199, 85%, 61%, 0) 50%),
radial-gradient(at 41% 92%, hsla(252, 94%, 67%, 1) 0, hsla(252, 94%, 67%, 0) 50%),
radial-gradient(at 25% 85%, hsla(260, 91%, 63%, 1) 0, hsla(260, 91%, 63%, 0) 50%),
radial-gradient(at 78% 99%, hsla(163, 95%, 59%, 1) 0, hsla(163, 95%, 59%, 0) 50%),
radial-gradient(at 42% 31%, hsla(296, 91%, 63%, 1) 0, hsla(296, 91%, 63%, 0) 50%),
radial-gradient(at 73% 66%, hsla(249, 87%, 63%, 1) 0, hsla(249, 87%, 63%, 0) 50%),
radial-gradient(at 27% 94%, hsla(246, 87%, 69%, 1) 0, hsla(246, 87%, 69%, 0) 50%),
radial-gradient(at 49% 94%, hsla(355, 89%, 60%, 1) 0, hsla(355, 89%, 60%, 0) 50%);
/* background: linear-gradient(320.54deg, #00069F 0%, #120010 72.37%), linear-gradient(58.72deg, #69D200 0%, #970091 100%), linear-gradient(121.28deg, #8CFF18 0%, #6C0075 100%), linear-gradient(121.28deg, #8000FF 0%, #000000 100%), linear-gradient(180deg, #00FF19 0%, #24FF00 0.01%, #2400FF 100%), linear-gradient(52.23deg, #0500FF 0%, #FF0000 100%), linear-gradient(121.28deg, #32003A 0%, #FF4040 100%), radial-gradient(50% 72.12% at 50% 50%, #EB00FF 0%, #110055 100%);
background-blend-mode: screen, color-dodge, color-burn, screen, overlay, difference, color-dodge, normal; */
/* background: radial-gradient(50% 123.47% at 50% 50%, #00FF94 0%, #FF00C7 100%), linear-gradient(121.28deg, #213100 0%, #FF0000 100%), linear-gradient(360deg, #0029FF 0%, #8FFF00 100%), linear-gradient(114.9deg, #00C6A2 0%, #6A45A8 100%), radial-gradient(100% 148.07% at 0% 0%, #FFFFFF 0%, #1DCD00 100%);
background-blend-mode: screen, color-dodge, overlay, difference, normal; */
		width: 100%;
		height: 100%;
		top: 0;
		left: 0;
	}

	nav > a {
		font-size: 1.5em;
		transition: all 0.2s ease-in-out;
        color: black;
  text-shadow:
      0 0 7px #fff,
      0 0 10px #fff,
      0 0 21px #fff,
      0 0 42px #0fa,
      0 0 82px #0fa,
      0 0 92px #0fa,
      0 0 102px #0fa,
      0 0 151px #0fa;
      animation: shadows 1.2s ease-in infinite, move 1.2s ease-in infinite;
  text-align: center;
  margin: 0;
  letter-spacing: 0.4rem;
	}
    
    

	@media (min-width: 60em) {
		header {
			margin: 0.4em 4em;
		}
		nav {
			position: fixed;
			display: flex;
            gap: 5em;
			align-items: center;
			justify-content: center;
			flex-direction: column;
			background-color: #000;
			width: 100%;
			height: 100%;
			top: 0;
			left: 0;
		}

		nav > a {
			font-size: 4em;
			text-decoration: none;
		}

		nav :hover {
			transition: linear 0.2s;
			transform: scale(1.1);
		}
	}
</style>

