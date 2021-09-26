<template>
	<div>
		<nav>
		<ul>
            <router-link to="/Home">Home</router-link>
            <router-link to="/About">About</router-link>
            <router-link to="/Contact">Contact</router-link>



		</ul>
		</nav>
		<div>
			<ul>
				<li v-for="(id,index) in UserIds" :key="index" >
				    <router-link :to="{name:'Profile', params:{user_id: id}}">
						Profile {{ id }} </router-link>

				</li>
			</ul>
		</div>
	</div>

</template>



<script>
	export default{
		name: "Navbar",
		data(){
			return{
				UserIds: ['1', '2','3','4','5',]
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