<script>
	// @ts-ignore
	import SocialLogos from '$lib/SocialLogos.svelte';
</script>

<header>
	<nav id="nav-container">
		<a href="/">
			<img src="tamagoFont.png" alt="Tamago Title Font" />
		</a>
		<a class="nav-link" href="/cart"> Cart </a>
		<a class="nav-link" href="/account"> My Account </a>
	</nav>
</header>

<div id="main" style="flex: 1;">
	<slot />
</div>

<footer>
	<div id="footer-container">
		<div id="footer-container-inner">
			<div id="footer-email-container">
				<p></p>
				<input>
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
	header {
		background-color: orange;
		text-align: center;
		opacity: 100%;
		box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
		height: 3em;
		width: 100%;
	}

	ul {
		list-style: none;
		padding: 0;
		display: flex;
		gap: 5px;
	}

	footer {
		margin-top: 50px;
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

	#footer-email-container {

	}

	#socials-container {
		display: flex;
		flex-direction: row-reverse;
	}

	#copyright-container {
		padding-bottom: 10px;
		text-align: center;
	}

	#nav-container {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		height: 100%;
		padding: 0 6px 0 6px;
	}

	.nav-link {
		align-self: center;
	}

	img {
		height: 100%;
		object-fit: contain;
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
