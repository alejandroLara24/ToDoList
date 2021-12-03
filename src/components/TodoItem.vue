<template>
  <li>
    <input type="checkbox" v-model="item.done" />
    <span v-if="!item.done">{{ item.descrip }}</span>
    <del v-else>{{ item.descrip }}</del>
  </li>
</template>

<script>
export default {
  props: ["item"],
};
</script>