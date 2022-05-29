<template>
  <div class="text-h4" v-text="header"></div>
</template>

<script>
export default {
  props: {
    header: {
      type: String,
      required: true,
    },
  },
}
</script>
