<template>
  <button :class="['c-button', cls, size]"
    :type="type"
    v-bind="attrs"><slot></slot></button>
</template>

<script>
import mBase from './mixins/base'

export default {
  mixins: [mBase],
  props: {
    type: {
      type: String,
      default: 'button'
    },
    size: {
      type: String,
      default: '',
      validator (value) {
        return !value || /^x?(large|small)$/.test(value)
      }
    },
    attrs: {
      type: Object,
      default () {
        return {}
      }
    }
  }
}
</script>

<style src="styles/components/button"></style>
