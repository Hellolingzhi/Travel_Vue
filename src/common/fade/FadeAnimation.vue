<template>
  <transition>
    <slot></slot>
  </transition>
</template>

<script>
export default {
  name: 'FadeAnimation'
}
</script>

<style lang="stylus" scoped>
.v-leave-to
.v-enter
  opacity: 0
.v-enter-active
.v-leave-active
  transition: all .8s
</style>
