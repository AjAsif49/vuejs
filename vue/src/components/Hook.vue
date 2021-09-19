<template>
	<div class="Hook">
        <h1> {{ title }} </h1>
        <button @click="ChangeTitle"> Click me </button>
    </div>

</template>



<script>
	export default{
		name: "Hook",
		data(){
			return{
                title: "Hook main part"
			}
		},
        methods:{
            ChangeTitle(){
                this.title = 'Easy Learning'
            }
        },
        beforeCreate(){
            alert('before creating hook')
        }, 
        created(){
            alert('after creating hook')

        },
        beforeUpdate(){
            alert('Before Updating hook')

        }
	}

</script>



<style>
	

</style>