<script>
	// @ts-ignore
	import SocialLogos from '$lib/SocialLogos.svelte';
	import { fly } from "svelte/transition";

	let menuOpened = false;
</script>

<header>
	<div id="top-bar">
		<p id="top-bar-text">
			First Purchase 15% Off & Spend $50 Dollars And Get Shipping For Free!
		</p>
	</div>
	<nav id="nav-container">
		<a href="/" class="nav-link" style="font-size: 65px;">
			TAMAGO
		</a>
		<div id="right-nav-container">
			<a class="nav-link" href="/cart"> Cart </a>
			<a class="nav-link" href="/account"> My Account </a>
			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<div class="nav-link" style="color: {menuOpened ? "orange" : ""}" on:click={() => menuOpened = !menuOpened}> MENU</div>
		</div>
		</nav>
</header>

<div id="main-page">
	<div id="main-page-inner">
		<slot />
	</div>
	{#if menuOpened}
		<div id="slide-menu" transition:fly={{x: 250}}>
			<div class="menu-item">
				Shop
			</div>
			<div class="menu-item">
				Search
			</div>
			<div class="menu-item">
				Shipping
			</div>
			<div class="menu-item">
				Faqs
			</div>
		</div>
	{/if}
</div>

<footer>
	<div id="footer-container">
		<div id="footer-container-inner">
			<div id="footer-email-container">
				<p></p>
				<!-- <input> -->
			</div>
			<div id="socials-container">
				<ul>
					<SocialLogos />
				</ul>
			</div>
		</div>
		<div id="copyright-container">
			TAMAGO Limited
		</div>
	</div>
</footer>

<style>
	a, a:visited {
		color: black;
		text-decoration: none;
	}

	#main-page {
		padding: 30px 15px 30px 30px;
		display: flex;
		flex: 1;
		flex-direction: row;
		overflow-x: clip;
	}

	#main-page-inner {
		width: 100%;
	}

	header {
		background-color: white;
		text-align: center;
		opacity: 100%;
		width: 100%;
		box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
	}

	#top-bar {
		height: 1.2em;
		background-color: orange;
		overflow: hidden;
	}

	#top-bar-text {
		margin: 0;
		height: 100%;
		line-height: 100%;
		position: relative;
		font-family: "Comic Sans MS", "Comic Sans", cursive;
		overflow: hidden;
		animation: scroll-text 30s infinite ;
	}

	@keyframes scroll-text {
		0% {
			transform: translateX(100%);
		}
		100% {
			transform: translateX(-100%);
		}
	}

	#slide-menu {
		display: flex;
		flex-direction: column;
		height: 100%;
		border-radius: 8px;
		box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
		width: 250px;
	}

	.menu-item {
		font-family: "Sunny Spells";
		text-align: center;
		font-size: 25px;
		cursor: pointer;
	}

	ul {
		list-style: none;
		padding: 0;
		display: flex;
		gap: 5px;
	}

	footer {
		/* margin-top: 50px; */
		width: 100%;
	}

	#footer-container {
		border-top: 1px solid black;
		width: 100%;
	}

	#footer-container-inner {
		display: flex;
		justify-content: space-between;
		padding: 20px;
	}

	/* #footer-email-container {

	} */

	#socials-container {
		display: flex;
		flex-direction: row-reverse;
	}

	#copyright-container {
		padding-bottom: 10px;
		text-align: center;
		font-family: "Sunny Spells";
		font-size: 20px;
	}

	#nav-container {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		padding: 0 15px 0 15px;
	}

	#right-nav-container {
		display: flex;
		gap: 25px;
	}

	.nav-link {
		align-self: center;
		font-family: "Sunny Spells";
		font-size: 30px;
		cursor: pointer;
	}

	.nav-link:hover {
		color: orange;
	}

	:global(body) {
		display: flex;
		flex: 1;
		flex-direction: column;
		margin: 0;
		width: 100vw;
		height: 100vh;
	}
</style>
