<template>
  <div>
    <h2>Making API request - the Vue way</h2>
    <hr />
    <div class="row">
      <Card
        v-for="post in posts"
        :key="post.id"
        :post="post"
        class="col-sm-6 col-md-4 col-lg-3 mb-4"
      />
    </div>
    <div class="text-right">
      <button class="btn btn-outline-secondary" v-scroll-to="'body'">
        Back to Top
      </button>
    </div>
  </div>
</template>

<script>
	import axios from 'axios'
	import Card from '@/components/Card'
	import {mapGetters} from 'vuex'

	export default {
		components: {
			Card
		},
		data() {
			return {
				allPosts: '' 
			}
		},
		computed: {
			...mapGetters(['posts'])
			// allPosts() {
			// 	return this.$store.getters.posts
			// }
		},

		// async fetch({store}) {
		// 	let {data} =  await axios.get('https://jsonplaceholder.typicode.com/posts')
		// 	// return {allPosts: data}
		// 	store.dispatch('setPosts', data)
		// },   
		head: {
			title: 'List of Posts'
		}
	}
</script>
