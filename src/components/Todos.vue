<template>
	<div>
		<div v-bind:key="todo.id" v-for="todo in todos">
			<h3>
				{{todo.title}}
			</h3>
		</div>
	</div>
</template>
<script>
	export default { 
		name:'Todos',
		props:['todos']

    }
</script>
<style scoped>
@charset "UTF-8";

*{
    outline:0 !important;
    color:#5a7391;

}
.c-while{
    color:#fff !important;
}
body {
    font-family: 'Rubik', sans-serif;
    position: relative;
}

a {
    color: #5a7392;
}

a:hover,
a:focus {
    color: #28415f;
}

h1 {
    font-size: 60px;
    font-weight: 300;
    letter-spacing: -1px;
    margin-bottom: 1.5rem;
}

h2 {
    font-size: 45px;
    font-weight: 300;
    color: #633991;
    letter-spacing: -1px;
    margin-bottom: 1rem;
}

h3 {
    color:;
    font-size: 33px;
    font-weight: 500;
}

h4 {
    font-size: 20px;
    font-weight: 400;
}

h5 {
    font-size: 28px;
    font-weight: 300;
    color: #633991;
    margin-bottom: 0.7rem;
}

p {
    color: #b8c0cb;
}

	
</style>