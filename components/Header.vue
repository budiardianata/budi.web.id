<template>
  <div role='navigation' class='block'>
    <header class='mx-auto container px-6 py-2 xl:py-0'>
      <div class='flex items-center justify-between'>
        <nuxt-link to='/'>
          <div class='flex items-center'>
            <svg id='logo' height='44' viewBox='0 0 300 300' width='43' xmlns='http://www.w3.org/2000/svg'
                 xmlns:xlink='http://www.w3.org/1999/xlink'>
              <g>
                <path
                  fill='#4c51bf'
                  d='m234.735 35.532c-8.822 0-16 7.178-16 16s7.178 16 16 16 16-7.178 16-16-7.178-16-16-16zm0 24c-4.412 0-8-3.588-8-8s3.588-8 8-8 8 3.588 8 8-3.588 8-8 8zm-62.529-14c0-2.502 2.028-4.53 4.53-4.53s4.53 2.028 4.53 4.53c0 2.501-2.028 4.529-4.53 4.529s-4.53-2.027-4.53-4.529zm89.059 60c0 2.501-2.028 4.529-4.53 4.529s-4.53-2.028-4.53-4.529c0-2.502 2.028-4.53 4.53-4.53s4.53 2.029 4.53 4.53zm-40.522-5.459-88-51.064c-1.242-.723-2.773-.723-4.016 0l-88 51.064c-1.232.715-1.992 2.033-1.992 3.459v104c0 1.404.736 2.705 1.938 3.428l88 52.936c.635.381 1.35.572 2.062.572s1.428-.191 2.062-.572l88-52.936c1.201-.723 1.938-2.023 1.938-3.428v-104c0-1.426-.76-2.744-1.992-3.459zm-90.008-42.98 80.085 46.47-52.95 31.289-23.135-13.607v-21.713c0-2.209-1.791-4-4-4s-4 1.791-4 4v21.713l-26.027 15.309c-1.223.719-1.973 2.029-1.973 3.447v29.795l-52 30.727v-94.688zm0 198.707-80.189-48.237 51.467-30.412 24.723 14.539v19.842c0 2.209 1.791 4 4 4s4-1.791 4-4v-19.842l26.027-15.307c1.223-.719 1.973-2.029 1.973-3.447v-31.667l52-30.728v94.729z'
                />
              </g>
            </svg>
            <h2 class='hidden sm:block text-base text-gray-700 font-bold leading-normal px-3'>The North</h2>
          </div>
        </nuxt-link>
        <div class='flex items-center space-x-4'>
          <nav class='hidden md:flex'>
            <ul class='inline-flex'>
              <li>
                <nuxt-link to='/blog' class='flex items-center rounded-xl px-4 py-4 hover:bg-gray-100 dark:hover:bg-gray-700'
                           @click='isOpen = false'>
                  <p tabindex='0' class='text-base'>Dashboard</p>
                </nuxt-link>
              </li>
              <li>
                <nuxt-link to='/blog2'
                           class='flex items-center px-4 py-4 hover:bg-gray-100 dark:hover:bg-gray-700'>
                  Blod
                </nuxt-link>
              </li>
            </ul>
          </nav>
          <div class='flex items-center'>
            <div class='relative md:mr-6 my-2'>
              <button class='focus:ring-2 focus:ring-offset-2 focus:ring-indigo-700 focus:text-indigo-700 focus:outline-none bg-gray-100 border-gray-300 border transition duration-150 ease-in-out hover:bg-gray-300 rounded text-gray-600 px-5 py-2 text-xs'>
                Manage
              </button>
            </div>
          </div>
          <button aria-label="open menu" class='pl-4 py-4' @click='toggle'>
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
           aria-label='Mobile Menu'>
      <div class='bg-gray-800 opacity-50 w-full h-full' @click='isOpen = false'></div>
      <div class='w-64 z-40 fixed overflow-y-auto z-40 top-0 bg-white shadow h-full flex-col justify-between pb-4 transition duration-150 ease-in-out'>
        <div class='h-full flex flex-col h-full w-full divide-y'>
          <nav>
            <ul class='space-y-2'>
              <li>
                <nuxt-link to='/blog' class='flex items-center px-2 py-4' @click='isOpen = false'>
                    <span class='w-6 h-6 md:w-8 md:h-8'>
                      <svg xmlns='http://www.w3.org/2000/svg' class='icon icon-tabler icon-tabler-grid'
                           viewBox='0 0 24 24' stroke-width='1.5' stroke='currentColor' fill='none'
                           stroke-linecap='round' stroke-linejoin='round'>
                        <path stroke='none' d='M0 0h24v24H0z'></path>
                        <rect x='4' y='4' width='6' height='6' rx='1'></rect>
                        <rect x='14' y='4' width='6' height='6' rx='1'></rect>
                        <rect x='4' y='14' width='6' height='6' rx='1'></rect>
                        <rect x='14' y='14' width='6' height='6' rx='1'></rect>
                      </svg>
                    </span>
                  <p tabindex='0' class=' text-base ml-3'>Dashboard</p>
                </nuxt-link>
              </li>
              <li>
                <a class='cursor-pointer'>
                  <div class='text-gray-800 pt-8'>
                    <div class='flex items-center justify-between'>
                      <div class='flex items-center'>
                        <div class='w-6 h-6 md:w-8 md:h-8 text-gray-800'>
                          <svg xmlns='http://www.w3.org/2000/svg' class='icon icon-tabler icon-tabler-puzzle'
                               viewBox='0 0 24 24' stroke-width='1.5' stroke='currentColor' fill='none'
                               stroke-linecap='round' stroke-linejoin='round'>
                            <path stroke='none' d='M0 0h24v24H0z'></path>
                            <path
                              d='M4 7h3a1 1 0 0 0 1 -1v-1a2 2 0 0 1 4 0v1a1 1 0 0 0 1 1h3a1 1 0 0 1 1 1v3a1 1 0 0 0 1 1h1a2 2 0 0 1 0 4h-1a1 1 0 0 0 -1 1v3a1 1 0 0 1 -1 1h-3a1 1 0 0 1 -1 -1v-1a2 2 0 0 0 -4 0v1a1 1 0 0 1 -1 1h-3a1 1 0 0 1 -1 -1v-3a1 1 0 0 1 1 -1h1a2 2 0 0 0 0 -4h-1a1 1 0 0 1 -1 -1v-3a1 1 0 0 1 1 -1'></path>
                          </svg>
                        </div>
                        <p tabindex='0'
                           class='focus:outline-none focus:text-indigo-600 text-gray-800 xl:text-base md:text-2xl text-base ml-3'>
                          Products</p>
                      </div>
                    </div>
                  </div>
                </a>
              </li>
              <li>
                <a class='cursor-pointer'>
                  <div class='text-gray-800 pt-8'>
                    <div class='flex items-center'>
                      <div class='w-6 h-6 md:w-8 md:h-8 text-gray-800'>
                        <svg xmlns='http://www.w3.org/2000/svg' class='icon icon-tabler icon-tabler-compass'
                             viewBox='0 0 24 24' stroke-width='1.5' stroke='currentColor' fill='none'
                             stroke-linecap='round' stroke-linejoin='round'>
                          <path stroke='none' d='M0 0h24v24H0z'></path>
                          <polyline points='8 16 10 10 16 8 14 14 8 16'></polyline>
                          <circle cx='12' cy='12' r='9'></circle>
                        </svg>
                      </div>
                      <p tabindex='0'
                         class='focus:outline-none focus:text-indigo-600 text-gray-800 xl:text-base md:text-2xl text-base ml-3'>
                        Performance</p>
                    </div>
                  </div>
                </a>
              </li>
              <li class='text-gray-800 pt-8 cursor-pointer'>
                <div class='flex items-center justify-between'>
                  <div class='flex items-center'>
                    <div class='w-6 h-6 md:w-8 md:h-8 text-gray-800'>
                      <svg xmlns='http://www.w3.org/2000/svg' class='icon icon-tabler icon-tabler-code'
                           viewBox='0 0 24 24' stroke-width='1.5' stroke='currentColor' fill='none'
                           stroke-linecap='round' stroke-linejoin='round'>
                        <path stroke='none' d='M0 0h24v24H0z'></path>
                        <polyline points='7 8 3 12 7 16'></polyline>
                        <polyline points='17 8 21 12 17 16'></polyline>
                        <line x1='14' y1='4' x2='10' y2='20'></line>
                      </svg>
                    </div>
                    <p tabindex='0'
                       class='focus:outline-none focus:text-indigo-600 text-gray-800 xl:text-base md:text-2xl text-base ml-3'>
                      Deliverables</p>
                  </div>
                </div>
              </li>
            </ul>
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
