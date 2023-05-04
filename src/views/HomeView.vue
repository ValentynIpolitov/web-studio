<script setup>
import FirstSection from '../components/FirstSection.vue'
import OurServices from '../components/OurServices.vue'
import Technologies from '../components/Technologies.vue'
import DealProcess from '../components/DealProcess.vue'
import SetUpACall from '../components/SetUpACall.vue'
</script>

<template>
  <main>
    <FirstSection />
    <OurServices id="our_services"/>
    <SetUpACall />
    <Technologies id="set_up_a_call" />
    <DealProcess />
  </main>
</template>

<style lang="scss">
@media (min-width: 1024px) {
  main {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    align-items: center;
  }
}
</style>
