<template>
  <div class="container">
    <h2>{{ post.title }}</h2>
    <pre>{{ post.body }}</pre>
    <!-- <nuxt-link class="btn btn-outline-secondary" to="/posts"
      >Back to posts</nuxt-link
    > -->
    <a
      class="btn btn-outline-secondary"
      href="#"
      onclick="history.back();return false;"
      >Back to posts</a
    >
  </div>
</template>

<script>
	import axios from 'axios'

	export default {
		data() {
			return {
				post: ''
			}
		},
		async asyncData({params}) {
			let {data} =  await axios.get(`https://jsonplaceholder.typicode.com/posts/${params.id}`)
			return {post: data}
		},
		head() {
			return {
				title: this.post.title
			}
		}
	}
</script>