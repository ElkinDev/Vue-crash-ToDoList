<template>
	<div class="todo-item" v-bind:class="{'is-complete':todo.completed}">
		<input type="checkbox" @change="markComplete" name=""/>
		<p>{{todo.title}}
		</p>
		<button class="del" @click="$emit('del-todo',todo.id)">
			
		</button>
	 <!-- insted of use the property @[todo.tittle] -->
	</div>
</template>
<script >
	export default { 
		name:'TodoItem',
		props:['todo'],
		methods:{
			markComplete(){
				this.todo.completed= !this.todo.completed
			}

		}

    }
</script>
<style scoped>
	.todo-item{
		background:#f4f4f4;
		padding:10px;
		border-bottom:1px #ccc dotted;
    }

    .is-complete{ 
		text-decoration:line-through;
    }

    .del{
    	background: #ff0000;
    	color:#fff;
    	border:none;
    	padding:20px 20px;
    	border-radius:50%;
    	border:none;
    	padding:5px 9px;
    	cursor:pointer;
    	align-items:center;vertical-align: middle;
    	float: right;
    }
    

</style>