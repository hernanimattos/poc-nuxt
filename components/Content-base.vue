<template>
  <section class="section section-content ">
    <slot/>
  </section>
</template>

<script>
export default {
  name: 'content-base'
}
</script>

<style lang="sass" scoped>
.section-content
  padding-top: 0.8rem;
</style>

