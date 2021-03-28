<script>
	import Todos from './Todos.svelte';
</script>

<main>
	<header>
		<h1>Maija's many To-do lists</h1>
		<h3>Write what you need to do today in the catagory of your choosing to stay organized</h3>
	</header>
	<div class="colour">
		<div class="lists">
			<p class="type">Work</p>
			<p class="type">Family</p>
			<p class="type">Chores</p>
		</div>
		<div class="box">
			<Todos />
		</div>
		<div class="box">
			<Todos />
		</div>
		<div class="box">
			<Todos />
		</div>	
	</div>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
	.container {
		display: inline-block;
	}
	h1 {
		color: #008cff;
		text-transform: uppercase;
		font-size: 2em;
		font-weight: 200;
		margin: 2%;
	}
	header {
		margin-bottom: 5%;
	}
	p {
		text-align: left;
	}
	.how {
		width: 30%;
		text-align: center;
	}
	.box {
		display: inline-block;
		margin: 2%;
	}
	.type {
		display: inline-block;
		padding: 20px;
		padding-right: 13%;
		padding-left: 13%;
		text-align: center;
		font-weight: 700;
	
	}
	.list {
		text-align: center;
		margin: 0;
		padding: 0;
	}
	.colour {
		background-color: aquamarine;
		border-radius: 5px;
		padding-bottom: 50%;
	}
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
	@media (max-width: 868px) {
		.box {
			margin: 0.5%;
		}
	}
	@media (max-width: 796px) {
		.box {
			margin: 0.1%;
	
		}
	}
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>