<template>
  <footer>
    <span>Have any questions? We'd love to hear from you.</span>
    <span>Please contact us via WhatsApp.</span>
    <span>
      Roman & English:
      <a class="tel" href="tel:+1(442)228-3245">+1(442)228-3245</a>. Thank you!
    </span>
    <hr />
    <span class="copyright">ALL rights reserved by Oyetalk</span>

    <img class="chip" src="../assets/images/background_chip.png" alt="chip" role="presentation" />
    <img
      class="poker"
      src="../assets/images/background_poker.png"
      alt="poker"
      role="presentation"
    />
  </footer>
</template>

<style scoped>
footer {
  position: relative;
  padding-block: 24px;
  margin-bottom: 8px;
  display: flex;
  flex-direction: column;
  align-items: center;
  color: var(--color-white);
  font-size: 12px;
  overflow: hidden;
}

.tel {
  color: var(--color-yellow);
  text-decoration: none;
}

span {
  margin-block: 1px;
}

hr {
  border: none;
  height: 1px;
  opacity: 0.4;
  background-color: var(--color-white);
  margin-block: 10px;
  width: 60%;
}

.copyright {
  opacity: 0.8;
}

.chip {
  position: absolute;
  left: 10px;
  bottom: 10px;
  max-width: 48px;
  opacity: 0.5;
}

.poker {
  position: absolute;
  top: 20px;
  right: -6px;
  max-width: 48px;
  opacity: 0.8;
}
</style>
