<template>
  <div :class="['c-pane', dir, cls]"><slot></slot></div>
</template>

<script>
import mBase from './mixins/base'

export default {
  mixins: [mBase],
  props: {
    dir: {
      type: String,
      default: ''
    }
  }
}
</script>

<style src="styles/components/pane"></style>
