<template>
  <div id="cta" :style="`background:hsl(${hsla.h},${hsla.s}%,${hsla.l}%)`">
    <div>
      <slot name="cta" />
    </div>
    <div>
      <slot name="call" />
    </div>
  </div>
</template>
<script>
export default {
  name: 'Cta',
  computed: {
    hsla() {
      const { h, s, l, a } = this.$store.state.theme.light.hsla
      return { h, s, l, a }
    },
    accent() {
      const { h, s, l, a } = this.$store.state.theme.light.accent
      return { h, s, l, a }
    },
    textColor() {
      const { h, s, l, a } = this.$store.state.theme.light.textColor
      return { h, s, l, a }
    },
  },
}
</script>
<style lang="scss" scoped>
#cta {
  text-align: center;
  width: 100%;
  padding: 1rem 0 1rem 0;
}
</style>
