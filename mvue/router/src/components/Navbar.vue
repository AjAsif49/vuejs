<template>
	<div>
		<nav>
		<ul>
            <router-link to="/Home">Home</router-link>
            <router-link to="/About">About</router-link>
            <router-link to="/Contact">Contact</router-link>



		</ul>
		</nav>
	</div>

</template>



<script>
	export default{
		name: "Navbar",
		data(){
			return{

			}
		}
	}

</script>



<style scoped>
	nav{
		text-align: center;
	}

	nav ul{
		padding: 0;
	}
	nav li{
		display: inline-block;
		list-style-type:none;
		margin: 0;
		padding: 8px; 
	}

</style>