<template>
  <div>
    <HeaderNav/>
    <div class="columns is-gapless">
      <Nav-menu/>
      <ContentBase>
        <nuxt />
      </ContentBase>
    </div>
  </div>
</template>

<script>

import {
  HeaderNav,
  NavMenu,
  ContentBase,

} from '../components'
export default {
  components: {
    HeaderNav,
    NavMenu,
    ContentBase,
  },
}
</script>
