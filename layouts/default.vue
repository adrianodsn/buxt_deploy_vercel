<template>
  <div>
    <Nav />
    <div class="jumbotron"></div>
    <div class="container py-5">
      <nuxt />
    </div>
  </div>
</template>

<script>
	import Nav from '@/components/Nav'
	export default {
		components: {
			Nav
		}
	}
</script>
