]<template>
  <div>FirstChildren</div>
  {{message}}
  <button @click="handleUpdate">update btn</button>
</template>

<script>
import {
  onBeforeMount,
  onBeforeUnmount,
  onBeforeUpdate,
  onMounted,
  onUnmounted,
  onUpdated,
  ref
} from "vue";

export default {
  name: "ChildrenComponent",
  setup() {
    const message = ref('before update children message');
    const handleUpdate = () => {
      message.value = 'after update children message'
    }

    console.log(`Children => setup()`);

    onBeforeMount(() => {
      console.log(`Children => onBeforeMount()`);
    });

    onMounted(() => {
      console.log(`Children => onMounted()`);
    });

    onBeforeUpdate(() => {
      console.log(`Children => onBeforeUpdate()`);
    });

    onUpdated(() => {
      console.log(`Children => onUpdated()`);
    });

    onBeforeUnmount(() => {
      console.log(`Children => onBeforeUnmount()`);
    });

    onUnmounted(() => {
      console.log(`Children => onUnmounted()`);
    });

    return {
      message,
      handleUpdate,
    }
  },

}
</script>