<template>
  <button
    class='text-yellow-500 transition-colors duration-300 ease-linear focus:outline-none'
    aria-label="Toggle Dark Mode"
    @click="toggle">
    <span v-if='isDark'>
      <icon-dark class='w-5 h-5'></icon-dark>
    </span>
    <span v-else>
      <icon-light class='w-5 h-5' ></icon-light>
    </span>
  </button>
</template>

<script>
import IconDark from '@/assets/icons/dark.svg?inline'
import IconLight from '@/assets/icons/light.svg?inline'
export default {
  name: 'ColorToggle',
  components: {
    IconDark, IconLight
  },
  computed: {
    isDark() {
      if (this.$colorMode.preference  === 'system') {
        return this.$colorMode.value === 'dark'
      }else {
        return this.$colorMode.preference === 'dark'
      }
    }
  },
  methods: {
    toggle() {
      if (this.isDark){
        this.$colorMode.preference = 'light'
      }else {
        this.$colorMode.preference = 'dark'
      }
    }
  }
}
</script>


