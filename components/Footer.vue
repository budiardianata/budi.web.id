<template>
  <footer class='mx-auto container py-6 px-4 overflow-hidden space-y-8 '>
    <nav class="-mx-5 -my-2" aria-label="Footer">
      <Navigation class='flex'/>
    </nav>
    <div class="flex justify-center space-x-6">
      <a
        href="https://twitter.com/budiardianata"
        aria-label="twitter"
        title='twitter'
        target="_blank"
        rel="nofollow noopener noreferrer"
      >
        <IconTwitter class="h-10 w-10 fill-current" />
      </a>

      <a
        href="https://www.linkedin.com/in/budiardianata"
        target="_blank"
        title='linkedIn'
        rel="nofollow noopener noreferrer"
        aria-label="linkedIn"
      >
        <IconLinkedIn class="h-10 w-10 fill-current" />
      </a>

      <a href="https://github.com/budiardianata"
        aria-label="github"
        target="_blank"
        rel="nofollow noopener noreferrer">
        <IconGithub class="h-10 w-10 fill-current" />
      </a>

      <a href="https://www.buymeacoffee.com/budiardianata"
        aria-label="buy me a coffee"
        title='buy me a coffee'
        target="_blank"
        rel="nofollow noopener noreferrer">
        <IconCoffee class="h-10 w-10 fill-current" />
      </a>
    </div>
    <div class='w-full inline-flex items-center justify-center space-x-2 text-center md:divide-x text-sm'>
      <p>
        Copyright &copy; <nuxt-link to='/'>Budi.web.id</nuxt-link>
      </p>
      <p class='inline-flex space-x-1 pl-2 items-center justify-center'>
        <span>Build with </span>
        <span class='text-red-500'>&hearts;</span>
        <a href="https://nuxtjs.org/"
           aria-label="Nuxt Js"
           title="Nuxt Js"
           target="_blank"
           rel="nofollow noopener noreferrer">
          <IconNuxt class="h-4 w-4 fill-current" />
        </a>
        <a href="https://tailwindcss.com/"
           aria-label="Tailwind Css"
           title="Tailwind Css"
           target="_blank"
           rel="nofollow noopener noreferrer">
          <IconTailwind class="h-4 w-4 fill-current" />
        </a>
        <span>in</span>
        <a href="https://indonesia.go.id/"
           aria-label="Indonesia"
           target="_blank"
           rel="nofollow noopener noreferrer">
          Indonesia
        </a>

      </p>
    </div>
  </footer>
</template>
<script>
import IconGithub from '@/assets/icons/github.svg?inline'
import IconTwitter from '@/assets/icons/twitter.svg?inline'
import IconLinkedIn from '@/assets/icons/linkedIn.svg?inline'
import IconNuxt from '@/assets/icons/nuxt.svg?inline'
import IconCoffee from '@/assets/icons/coffee.svg?inline'
import IconTailwind from '@/assets/icons/tailwind.svg?inline'
export default {
  components: {
    IconGithub,
    IconTwitter,
    IconLinkedIn,
    IconCoffee,
    IconNuxt,
    IconTailwind
  }
}
</script>

