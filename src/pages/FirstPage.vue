<template>
  <div>
    <div>Page</div>
    <Parent/>
  </div>
</template>

<script>
import Parent from "@/components/Parent";
import {onBeforeMount, onBeforeUnmount, onBeforeUpdate, onMounted, onUnmounted, onUpdated} from "vue";
export default {
  name: "FirstPage",
  components: {
    Parent,
  },
  setup() {
    console.log(`Page => setup()`);

    onBeforeMount(() => {
      console.log(`Page => onBeforeMount()`);
    });

    onMounted(() => {
      console.log(`Page => onMounted()`);
    });

    onBeforeUpdate(() => {
      console.log(`Page => onBeforeUpdate()`);
    });

    onUpdated(() => {
      console.log(`Page => onUpdated()`);
    });

    onBeforeUnmount(() => {
      console.log(`Page => onBeforeUnmount()`);
    });

    onUnmounted(() => {
      console.log(`Page => onUnmounted()`);
    });
  }
}
</script>

<style scoped>

</style>