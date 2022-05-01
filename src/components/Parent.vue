<template>
  <div>Parent</div>
  <Children/>
</template>

<script>
import {
  onBeforeMount,
  onBeforeUnmount,
  onBeforeUpdate,
  onMounted,
  onUnmounted,
  onUpdated
} from "vue";
import Children from "@/components/Children";

export default {
  name: "ParentComponent",
  components: {
    Children
  },
  setup() {
    console.log(`Parent => setup()`);

    onBeforeMount(() => {
      console.log(`Parent => onBeforeMount()`);
    });

    onMounted(() => {
      console.log(`Parent => onMounted()`);
    });

    onBeforeUpdate(() => {
      console.log(`Parent => onBeforeUpdate()`);
    });

    onUpdated(() => {
      console.log(`Parent => onUpdated()`);
    });

    onBeforeUnmount(() => {
      console.log(`Parent => onBeforeUnmount()`);
    });

    onUnmounted(() => {
      console.log(`Parent => onUnmounted()`);
    });
  },
}
</script>