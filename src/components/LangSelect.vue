<script setup>
const onLanguageChange = (event) => {
  document.querySelectorAll('html [lang]').forEach((element) => (element.style.display = 'none'))
  document
    .querySelectorAll(`html [lang="${event.target.value}"]`)
    ?.forEach((element) => (element.style.display = 'block'))
}
</script>

<template>
  <div class="lang-select">
    <select @change="onLanguageChange" title="Change language" name="lang" id="lang">
      <option value="en">English</option>
      <option value="hi">हिंदी</option>
    </select>
    <div class="lang-select-button">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="100%"
        height="100%"
        viewBox="0 0 24 24"
        fill="none"
      >
        <path
          d="M17.9188 8.17969H11.6888H6.07877C5.11877 8.17969 4.63877 9.33969 5.31877 10.0197L10.4988 15.1997C11.3288 16.0297 12.6788 16.0297 13.5088 15.1997L15.4788 13.2297L18.6888 10.0197C19.3588 9.33969 18.8788 8.17969 17.9188 8.17969Z"
          fill="#FFFFFF"
        />
      </svg>
    </div>
  </div>
</template>

<style scoped>
.lang-select {
  --color: #ff9313;
  position: absolute;
  top: 10px;
  right: 14px;
  border: 0.4vw solid var(--color);
  border-radius: 20vw;
  display: flex;
  overflow: hidden;
}

.lang-select select {
  /* appearance: none;
  -webkit-appearance: none; */
  /* -moz-appearance: none; */
  text-indent: 1px;
  font-size: 12px;
  flex: 1;
  padding: 4px 8px;
  padding-right: 24px;
  outline: none;
  border: none;
}

.lang-select select:focus {
  outline: none;
}

.lang-select-button {
  all: unset;
  position: absolute;
  top: 0;
  right: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: var(--color);
  width: 24px;
  height: 100%;
  pointer-events: none;
}
</style>
