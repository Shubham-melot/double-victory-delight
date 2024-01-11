<script setup>
const props = defineProps({
  index: Number,
  avatar: String,
  username: String,
  beansAmount: Number,
  rewardIcon: String,
  rewardAmount: String
})
let topIcon = null
if (props.index <= 3) {
  switch (props.index) {
    case 1:
      topIcon = '/src/assets/images/picture_top1.png'
      break
    case 2:
      topIcon = '/src/assets/images/picture_top2.png'
      break
    case 3:
      topIcon = '/src/assets/images/picture_top3.png'
      break
  }
}
</script>

<template>
  <div class="list-item-container">
    <div>
      <img class="top-icon" v-if="topIcon" :src="topIcon" :alt="index" />
      <span class="top-index" v-else>{{ index }}</span>
      <img class="avatar" :src="avatar" :alt="username" />
      <span class="username">{{ username }}</span>
    </div>

    <div class="beans-container">
      <img class="beans-img" src="../assets/images/beans.png" alt="beans" />
      <span class="beans-amount">{{ beansAmount }}</span>
    </div>

    <div class="rewards-container">
      <img class="reward-icon" v-if="rewardIcon" :src="rewardIcon" alt="reward" />
      <img class="beans-img" v-else src="../assets/images/beans.png" alt="beans" />
      <span class="reward-amount">{{ rewardAmount }}</span>
    </div>
  </div>
</template>

<style scoped>
.list-item-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 10px;
  padding: 10px;
  font-size: 14px;
  background: linear-gradient(0deg, #ffc290, #ffa3bf);
  outline: 1px solid #ffc3ae;
  outline-offset: -1px;
  border-radius: 10px;
}

.list-item-container > div {
  display: flex;
  align-items: center;
  gap: 4px;
  color: #8d211a;
}

.list-item-container:first-child {
  background: url('../assets/images/background_top1.png') center / 100% 100% no-repeat;
  outline-color: transparent;
}

.list-item-container:nth-child(2) {
  background: url('../assets/images/background_top2.png') center/100% 100% no-repeat;
  outline-color: transparent;
}

.top-icon {
  max-width: 24px;
}

.top-index {
  opacity: 0.6;
  width: 24px;
  display: grid;
  place-items: center;
}

.avatar {
  max-width: 34px;
  margin-right: 4px;
}

.username {
  font-weight: 500;
}

.beans-amount {
  opacity: 0.8;
}

.beans-img {
  max-width: 12px;
}

.beans-container,
.rewards-container {
  gap: 0;
  margin-right: 10px;
}
</style>
