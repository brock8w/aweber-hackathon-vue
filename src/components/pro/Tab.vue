<template>
  <ul :is="tag" :class="className">
    <slot></slot>
  </ul>
</template>

<script>
import classNames from 'classnames';

export default {
  props: {
    tag: {
      type: String,
      default: "ul"
    },
    color: {
      type: String
    }
  },
  data() {
    return {
      className: classNames(
        'nav nav-tabs nav-justified',
        this.color ? this.color : ''
      )
    };
  },

};
</script>

<style scoped>
</style>
