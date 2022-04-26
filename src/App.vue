<template>
  <div>
    <span>{{count}}</span>
    <Child :count="count" @change="change"></Child>
  </div>
</template>

<script>


import Child from "@/components/Child";
export default {
  name: 'App',
  components: {
    Child
  },
  data() {
    return {
      count: 0,
    }
  },
  methods: {
    change(value) {
      this.count = value
    }
  }
}
</script>

<style>
</style>
