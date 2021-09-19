<template>
	<div>
        <h1> Posts </h1><hr>
        <input type="text" v-model="searchterm" placeholder="Search">
    <div v-for="post in filtersearch" :key="post.id"> 
        <h2>{{ post.title }}</h2>
        <p> {{ post.body | snippet }} </p>
    </div>
    </div>
</template>



<script>
import axios from 'axios'
	export default{
		name: "Hook",
		data(){
			return{
                posts:[],
                searchterm: ''
			}
		},
        computed:{
        filtersearch(){
            return this.posts.filter(post =>{
                return post.title.match(this.searchterm)
            })
        }
    },

        methods:{
            
        },
        created(){
            axios.get('https://jsonplaceholder.typicode.com/posts')
            .then(response =>{
                this.posts = response.data
            })
            .catch(error=>{
                console.log(error)
            })
        }
        
	}

</script>



<style scoped>
h1{
        color: tomato;
        text-align: center;
    }
</style>>
	

