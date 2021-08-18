<template>
  <div class='block'>
    <header class='mx-auto container px-6 py-2'>
      <div class='flex items-center justify-between'>
        <nuxt-link to='/'>
          <div class='flex items-center'>
            <svg id='logo' height='44' viewBox='0 0 300 300' width='43' xmlns='http://www.w3.org/2000/svg'>
              <g>
                <path
                  fill='#4c51bf'
                  d='m234.735 35.532c-8.822 0-16 7.178-16 16s7.178 16 16 16 16-7.178 16-16-7.178-16-16-16zm0 24c-4.412 0-8-3.588-8-8s3.588-8 8-8 8 3.588 8 8-3.588 8-8 8zm-62.529-14c0-2.502 2.028-4.53 4.53-4.53s4.53 2.028 4.53 4.53c0 2.501-2.028 4.529-4.53 4.529s-4.53-2.027-4.53-4.529zm89.059 60c0 2.501-2.028 4.529-4.53 4.529s-4.53-2.028-4.53-4.529c0-2.502 2.028-4.53 4.53-4.53s4.53 2.029 4.53 4.53zm-40.522-5.459-88-51.064c-1.242-.723-2.773-.723-4.016 0l-88 51.064c-1.232.715-1.992 2.033-1.992 3.459v104c0 1.404.736 2.705 1.938 3.428l88 52.936c.635.381 1.35.572 2.062.572s1.428-.191 2.062-.572l88-52.936c1.201-.723 1.938-2.023 1.938-3.428v-104c0-1.426-.76-2.744-1.992-3.459zm-90.008-42.98 80.085 46.47-52.95 31.289-23.135-13.607v-21.713c0-2.209-1.791-4-4-4s-4 1.791-4 4v21.713l-26.027 15.309c-1.223.719-1.973 2.029-1.973 3.447v29.795l-52 30.727v-94.688zm0 198.707-80.189-48.237 51.467-30.412 24.723 14.539v19.842c0 2.209 1.791 4 4 4s4-1.791 4-4v-19.842l26.027-15.307c1.223-.719 1.973-2.029 1.973-3.447v-31.667l52-30.728v94.729z'
                />
              </g>
            </svg>
          </div>
        </nuxt-link>
        <div class='flex items-center space-x-4'>
          <nav role='navigation' class='hidden md:flex' aria-label="Main-Menu">
            <Navigation class='flex'/>
          </nav>
          <div class='flex items-center'>
            <ColorToggle/>
          </div>
          <button aria-label="open menu" class='pl-4 py-4 md:hidden flex focus:outline-none' @click='toggle'>
            <span v-if='isOpen'>
              <IconClose class='w-6 h-6' />
            </span>
            <span v-else>
              <IconMenu class='w-6 h-6' />
            </span>
          </button>
        </div>
      </div>
    </header>
    <aside v-show='isOpen'
           class='absolute w-full h-full transform z-40'
           aria-label='Mobile Menu'
    @click='isOpen = false'>
      <div class='bg-gray-800 opacity-50 w-full h-full' @click='isOpen = false'></div>
      <div class='w-64 z-40 fixed overflow-y-auto z-40 top-0 bg-white dark:bg-gray-800 shadow h-full flex-col justify-between pb-4 transition duration-150 ease-in-out'>
        <div class='h-full flex flex-col h-full w-full divide-y'>
          <nav role='navigation' aria-label="Mobile-Menu">
            <Navigation class='block'/>
          </nav>
        </div>
      </div>
    </aside>
  </div>
</template>


<script>
import IconMenu from '@/assets/icons/menu.svg?inline'
import IconClose from '@/assets/icons/close.svg?inline'

export default {
  name: 'Header',
  components: {
    IconClose, IconMenu
  },
  data() {
    return {
      isOpen: false
    }
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen
    }
  }
}
</script>
