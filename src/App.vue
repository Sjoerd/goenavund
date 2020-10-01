<template>
  <div class="bg-gray-300 min-h-screen bg-cover">
    <div class="md:max-w-3xl px-3 pb-8 mx-auto">
      
      <Logo />


      <transition
        enter-active-class="transition-all transition-75 ease-out"
        leave-active-class="transition-all transition-100 ease-in"
        enter-class="opacity-0 scale-70"
        enter-to-class="opacity-100 scale-100"
        leave-class="opacity-100 scale-100"
        leave-to-class="opacity-0 scale-70"
      >
        <div class="sm:grid grid-cols-3 md:grid-cols-3 gap-4">
          <SoundButton v-for="i in 15" :key="i" />
        </div>
      </transition>


    </div>
  </div>
</template>

<script>
import SoundButton from './components/SoundButton.vue'
import Logo from './components/Logo.vue'

export default {
  name: 'App',
  components: {
    Logo,
    SoundButton
  }
}
</script>
