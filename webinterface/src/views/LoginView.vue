<template>
  <link rel="stylesheet" href="https://unicons.iconscout.com/release/v4.0.0/css/line.css">
  <div class="login">
		<div class="login-forms">
			<span class="title">Login</span>

			<form action="#">
				<div class="input-field">
					<input type="text" placeholder="Enter you Email" required>
					<i class="uil uil-envelope nonpwvisibility"></i>
				</div>
				<div class="input-field">
					<input type="text" placeholder="Enter you Password" required>
					<i class="uil uil-key-skeleton-alt nonpwvisibility"></i>
					<i class="uil uil-eye-slash pwvisibility"></i>
					<i class="uil uil-eye pwvisibility"></i>
				</div>

				<div class="checkbox-text">
					<div class="checkbox-content">
						<input type="checkbox" name="" id="logCheck">
						<label for="logCheck">Remember me</label>
					</div>

					<a href="#">Forgot Password?</a>
				</div>

				<div class="button">
					<input type="button" value="Login Now" required>
				</div>
			</form>

			<div class="login-signup">
				<span>Problems with your account?</span>
				<a href="#">Contact Us</a>
			</div>
		</div>
  </div>
</template>

<style lang="scss" scoped>
@import '../scss/vars';
@import '../scss/fonts';
@import '../scss/general';

.login {
	font-family: $poppins;
	display: flex;
	justify-content: center;
	align-items: center;
	position: relative;
	width: 100%;
	max-width: 430px;
	border: 1px solid #c5c5c5;
	box-shadow: 0 5px 10px rgba(122, 122, 122, 0.1);
	border-radius: 10px;
	padding: 30px;
}

.login-forms {
	width: 100%;

.title {
		font-size: 27px;
		font-weight: 600;
	}

form {
	.input-field {
		width: 100%;
		position: relative;
		height: 50px;
		margin: 10px 0;

		input {
			width: 100%;
			height: 100%;
			border: none;
			outline: none;
			padding: 0 35px;
			border-bottom: 2px solid #c5c5c5;
			border-top: 2px solid transparent;
			font-size: 16px;
		}

		input:is(:focus, :valid){
			border-bottom-color: #5f5f5f;
		}

		input:is(:focus, :valid) ~ i {
			color: #5f5f5f;
		}

		i {
			position: absolute;
			font-size: 20px;
			color: #c5c5c5;
			top: 50%;
			transform: translateY(-50%);
		}

		.nonpwvisibility {
			left: 0;
		}

		.pwvisibility {
			right: 0;
		}
	}

	.checkbox-text {
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin-top: 10px;
		
		.checkbox-content {
			input {
				accent-color: #177bee;
			}

			label {
				margin-left: 10px;
			}
		}

		a {
			text-decoration: none;
			color: #177bee;
		
			&:hover{
				text-decoration: underline;
			}
		}
	}

	}
	.button {
		width: 100%;
		height: 50px;
		margin: 10px 0;

		input {
			width: 100%;
			height: 100%;
			border: none;
			font-size: 18px;
			border-radius: 10px;

			&:hover {
				border: 2px solid;
				border-color: #177bee;
				cursor: pointer;
			}
		}
	}
}

.login-signup {
	display: flex;
	justify-content: space-between;
	align-items: center;

	a {
		text-decoration: none;
		color: #177bee;
	
		&:hover{
			text-decoration: underline;
		}
	}
}
</style>