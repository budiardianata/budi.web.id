<template>
  <ul class='justify-center'>
    <li v-for='(nav, index) in navLinks'
        :key='index'>
      <nuxt-link :to='nav.url' :title='nav.link'
                 class='flex items-center rounded-xl px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700'
                 @click='isOpen = false'>
        {{ nav.link }}
      </nuxt-link>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'Navigation',
  props: {},
  data() {
    return {
      navLinks: [
        {
          url: '/blog',
          link: 'Blog'
        },
        {
          url: '/profile',
          link: 'Profile'
        },
        {
          url: '/contact',
          link: 'Contact'
        }
      ]
    }
  }
}
</script>
