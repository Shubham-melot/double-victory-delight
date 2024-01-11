<script setup>
import BuyButton from './components/BuyButton.vue'
import EventTimer from './components/EventTimer.vue'
import Header from './components/Header.vue'
import HowToPlayBanner from './components/HowToPlayBanner.vue'
import Leaderboard from './components/Leaderboard.vue'
import Footer from './components/Footer.vue'
import Feedback from './components/Feedback.vue'
import { onMounted } from 'vue'

const today = new Date()
const eventDate = new Date(2024, 0, today.getDate() + 10, 1, 0, 0)

const eventDateRange = `${today.getDate()}/${today.getMonth() + 1} - ${eventDate.getDate()}/${
  eventDate.getMonth() + 1
}`

// eslint-disable-next-line no-unused-vars
const onFeedbackButtonClick = (_event) => {
  console.log('Feedback button click')
}

onMounted(() => {
  const textElements = document.querySelectorAll('html [lang]')
  textElements.forEach((element) => (element.style.display = 'none'))

  document
    .querySelectorAll('html [lang="en"]')
    .forEach((element) => (element.style.display = 'block'))
})
</script>

<template>
  <Header :event-date="eventDateRange" />
  <main>
    <EventTimer :event-end-date="eventDate" />
    <Feedback @click="onFeedbackButtonClick" />
    <HowToPlayBanner />
    <BuyButton />
    <Leaderboard />
  </main>
  <Footer />
</template>

<style scoped>
main {
  position: relative;
}
</style>
