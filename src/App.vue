<script setup>
import BuyButton from './components/BuyButton.vue';
import EventTimer from './components/EventTimer.vue';
import Header from './components/Header.vue';
import HowToPlayBanner from './components/HowToPlayBanner.vue';
import Leaderboard from './components/Leaderboard.vue';

const today = new Date()
const eventDate = new Date()
eventDate.setDate(today.getDate() + 10)

const eventDateRange = `${today.getDate()}/${today.getMonth() + 1} - ${eventDate.getDate()}/${eventDate.getMonth() + 1}`
</script>

<template>
  <Header :event-date="eventDateRange" />
  <main>
    <EventTimer :event-end-date="eventDate" />
    <HowToPlayBanner />
    <BuyButton />
    <Leaderboard />
  </main>
</template>

<style scoped></style>
