<svelte:head>
	<title>TAMAGO - My Account</title>
</svelte:head>

<div id="account-container">
	<div id="create-account-container">
		<form class="account-form">
			<p>CREATE ACCOUNT</p>
            <div id="name-div">
                <input class="register-input" placeholder="First Name">
                <input class="register-input" placeholder="Last Name">
            </div>
            <input class="login-input" placeholder="Email Address" />
			<input class="login-input" placeholder="Password" />
            <input class="login-input" placeholder="Confirm Password" />
			<button>Create</button>
		</form>
	</div>
	<div id="account-seperator-container">
		<div id="account-seperator" />
	</div>
	<div id="login-account-container-inner">
		<form class="account-form">
			<p>SIGN IN</p>
			<input class="login-input" placeholder="Email Address" />
			<input class="login-input" placeholder="Password" />
			<button>Sign In</button>
		</form>
	</div>
</div>

<style>

    #name-div {
        display: flex;
        justify-content: space-between;
    }

	button {
		height: 40px;
		background-color: black;
		border: none;
		border-radius: 15px;
		color: white;
		cursor: pointer;
	}

	.account-form {
		display: flex;
		flex-direction: column;
		gap: 20px;
	}

	p {
		font-family: 'Morning Breeze';
		font-size: 40px;
		margin: 0;
	}

	#account-container {
		display: flex;
		justify-content: space-evenly;
		height: 100%;
	}

	#account-seperator-container {
		display: flex;
		align-items: center;
		height: 100%;
	}

	#account-seperator {
		height: 80%;
		border: thin solid black;
	}

    .register-input {
        height: 35px;
		border: 1px solid gray;
		padding: 5px 20px 5px 20px;
    }

	.login-input {
		width: 350px;
		height: 35px;
		border: 1px solid gray;
		padding: 5px 20px 5px 20px;
		/* border-radius: 8px; */
	}
</style>
