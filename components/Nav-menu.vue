<template>
  <section class="section-menu column is-2">
      <aside class="column menu">
        <ul class="menu-list">
          <li
            v-for="(item, key) of items"
            :key="key"
          >
            <nuxt-link
              :to="item.to"
              exact-active-class="is-active"
            >
              <b-icon :icon="item.icon"  />
              <span class="menu-title"> {{ item.title }}</span>
            </nuxt-link>
          </li>
        </ul>
      </aside>
    </section>
</template>

<script>
export default {
  name: 'nav-menu',
  data() {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' }
        }
      ]
    }
  }
}
</script>

<style lang="sass" scoped>
.section-menu
  padding-top: 3rem;

@media (max-width:768px)
  .section-menu
    overflow: hidden;
    max-height: 0px;
    transition: max-height 0.3s ease-out;
@media (max-width: 960px)
  .menu
    text-align: left;

@media (min-width: 768px) and (max-width: 960px)
  .menu
    text-align: center;
    .menu-title
      display: none;

.show-menu
  height: auto;
  overflow: hidden;
  max-height: 600px;
  transition: max-height 1s cubic-bezier(0, 0, 0.99, 1.46);
</style>

