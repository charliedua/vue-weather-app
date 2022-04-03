<script>
export default {
  name: "HomeHelper",
  props: {
    msg: {
      type: String,
    },
  },
};
</script>

<template>
  <p>
    {{ msg }}
  </p>
</template>
