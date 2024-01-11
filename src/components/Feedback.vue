<template>
  <button v-bind="$attrs" />
</template>

<style scoped>
button {
  --size: 44px;
  border: none;
  box-shadow: none;
  outline: none;
  position: absolute;
  background: url('../assets/images/button_feedback.png') center / 100% 100% no-repeat;
  height: var(--size);
  width: var(--size);
  right: 14px;
  top: -14px;
}
</style>
