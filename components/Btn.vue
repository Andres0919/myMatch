<template>
  <vs-button :primary="primary" :danger="danger" :border="border">
    <slot></slot>
  </vs-button>
</template>

<script>
export default {
  name: 'Btn',
  props: {
    border: Boolean,
    danger: Boolean,
    primary: Boolean
  }
}
</script>
