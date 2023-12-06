<template>
	<header>
		<div class="conteiner">
			<nav>
				<router-link to="/">Home</router-link>|
				<router-link to="/about">About</router-link>|
				<router-link to="/about">inprogress</router-link>|
				<router-link to="/about">inprogress</router-link>|
				<router-link to="/about">inprogress</router-link>
			</nav>
		</div>
	</header>
</template>

<script setup>

</script>

<style lang="scss">
	.conteiner
	{
		margin: 0 auto;
		width: 1300px;
	}
	nav
	{
		height: 45px;
		width: 100%;
		display: flex;
		justify-content:space-around;
		a
		{
			text-decoration: none;
			color: black;
		}
		a:hover
		{
			color: blue;
		}
	}
</style>