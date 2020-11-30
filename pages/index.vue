<template>
  <div>
    <h2>Hello world</h2>
    <no-ssr>
      <v-select
        v-model="selected"
        placeholder="Select Category"
        :options="['foo', 'bar']"
      ></v-select>
    </no-ssr>
  </div>
</template>

<script>
	export default {
		data() {
			return {
				selected: ''
			}
		}
	}
</script>