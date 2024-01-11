<template>
  <div class="button-container">
    <img class="left" src="../assets/images/picture_arrow2.png" alt="picture" />
    <button v-bind="$attrs">GO Buy</button>
    <img src="../assets/images/picture_arrow2.png" alt="picture" />
  </div>
</template>

<style scoped>
.button-container {
  display: flex;
  align-items: center;
  width: 100%;
  justify-content: space-between;
}

button {
  all: unset;
  color: #934f13;
  background: url('../assets/images/button.png') center / 100% 100% no-repeat;
  font-weight: 800;
  width: 100%;
  padding-block: 12px;
  display: grid;
  place-items: center;
}

img {
  width: 80px;
}

.left {
  transform: scaleX(-1);
}
</style>
