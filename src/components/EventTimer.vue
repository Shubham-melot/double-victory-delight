<script setup>
import { onMounted, reactive } from 'vue'

const props = defineProps({
  eventEndDate: Date
})
const { eventEndDate } = props

const remaining = reactive({
  days: 0,
  hours: 0,
  minutes: 0,
  seconds: 0
})

const MS = 1000
const SEC = 60
const MIN = 60
const HOUR = 24

const updateCountdown = () => {
  const currentDate = new Date()
  const timeDifference = eventEndDate - currentDate

  if (timeDifference > 0) {
    remaining.days = Math.floor(timeDifference / (MS * MIN * SEC * HOUR))
    remaining.hours = Math.floor((timeDifference % (MS * MIN * SEC * HOUR)) / (MS * MIN * SEC))
    remaining.minutes = Math.floor((timeDifference % (MS * SEC * SEC)) / (MS * SEC))
    remaining.seconds = Math.floor((timeDifference % (MS * SEC)) / MS)
  }

  setTimeout(updateCountdown, MS)
}

onMounted(() => updateCountdown())
</script>

<template>
  <div class="event-timer-container">
    <div class="days-container">
      <span>{{ remaining.days.toString().padStart(2, '0') }}</span>
      <span>D</span>
    </div>
    <div class="time-container">
      <span>{{ remaining.hours.toString().padStart(2, '0') }}</span>
      :
      <span>{{ remaining.minutes.toString().padStart(2, '0') }}</span>
      :
      <span>{{ remaining.seconds.toString().padStart(2, '0') }}</span>
    </div>
    <img class="chip" src="../assets/images/background_chip.png" alt="chip" role="presentation" />
  </div>
</template>

<style scoped>
.event-timer-container {
  position: relative;
  margin-top: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 8px;
}

.days-container {
  display: flex;
  gap: 4px;
}

div {
  display: flex;
  gap: 2px;
  align-items: center;
  color: #cd0215;
  font-weight: 500;
}

span {
  --size: 35px;
  display: grid;
  place-items: center;
  background-color: var(--color-secondary);
  border-radius: 8px;
  width: var(--size);
  height: var(--size);
}

.chip {
  position: absolute;
  left: 14px;
  max-width: 48px;
  opacity: 0.5;
}
</style>
