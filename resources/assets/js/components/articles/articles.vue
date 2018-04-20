<template>
	<div>
		<h2>Articulos de Larticles</h2>
		
	</div>	
</template>

<script>
	export default {
		data() {
			return {
				articles: [],
				article: {
					id:'',
					title:'',
					body:''
				},
				article_id:'',
				pagination: {},
				edit: false
			};
		},
		create() {
			this.fetchArticles();
		},
		methods: {
			fetchArticles() {
				fetch('api/articles')
				.then(res => res.json())
				.then(res => {
					console.log(res.data)
					//this.articles = res.data;
				});	
			}
		}
	};
</script>