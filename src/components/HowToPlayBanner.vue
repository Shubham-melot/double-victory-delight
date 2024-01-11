<script setup>
const OYETALK_VERSION = '2.8.5'
</script>

<template>
  <section class="how-to-play-container">
    <div class="header">
      <img class="left" src="../assets/images/picture_title1.png" alt="arrow" />
      <span class="title">How to play</span>
      <img src="../assets/images/picture_title1.png" alt="arrow" />
    </div>

    <div class="process-container">
      <div class="step">
        <div class="step-image-container">
          <img src="../assets/images/how_to_play1.png" alt="Buy" />
        </div>
        <div lang="en" class="step-info">
          Purchase <br />
          Rebate Card
        </div>

        <div lang="hi" class="step-info">
          रिबेट कार्ड <br />
          खरीदें
        </div>
      </div>
      <img class="arrow-next" src="../assets/images/picture_arrow1.png" alt="Next" />

      <div class="step">
        <div class="step-image-container">
          <img src="../assets/images/how_to_play2.png" alt="Buy" />
        </div>
        <div lang="en" class="step-info">
          Activate <br />
          Rebate Card
        </div>

        <div lang="hi" class="step-info">
          रिबेट कार्ड <br />
          सक्रिय करें
        </div>
      </div>
      <img class="arrow-next" src="../assets/images/picture_arrow1.png" alt="Next" />

      <div class="step">
        <div class="step-image-container">
          <img src="../assets/images/how_to_play3.png" alt="Buy" />
        </div>
        <div lang="en" class="step-info">
          Start playing <br />
          Royal Pattern
        </div>

        <div lang="hi" class="step-info">
          रॉयल पैटर्न <br />
          खेलना शुरू करें
        </div>
      </div>
    </div>

    <div class="faq">
      <div lang="en" class="question">What is Rebate cards?</div>
      <div lang="hi" class="question">रिबेट कार्ड क्या है?</div>

      <div lang="en" class="answer">
        Exclusively available for OyeTalk Royal Pattern users, the Rebate Card is a premium in-game
        item. If you don't win a game <span>(by not betting on the winning seat)</span>, using the
        Rebate Card guarantees a <span>5%</span> bean rebate to reduce your losses.
        <br />
        <span
          >Please update to the latest version {{ OYETALK_VERSION }} of OyeTalk to enjoy this
          feature.</span
        >
      </div>
      <div lang="hi" class="answer">
        ओएटॉक रॉयल पैटर्न उपयोगकर्ताओं के लिए विशेष रूप से उपलब्ध, रिबेट कार्ड एक प्रीमियम इन-गेम
        आइटम है। यदि आप कोई गेम नहीं जीतते हैं <span>(जीतने वाली सीट पर दांव न लगाकर)</span>, तो
        रिबेट कार्ड का उपयोग करने से आपके नुकसान को कम करने के लिए <span>5%</span> सेम छूट की गारंटी
        मिलती है।
        <br />
        कृपया इस सुविधा का आनंद लेने के लिए OyeTalk के नवीनतम संस्करण
        {{ OYETALK_VERSION }} में अपडेट करें।
      </div>
    </div>
  </section>
</template>

<style scoped>
.how-to-play-container {
  width: 90%;
  margin-inline: auto;
  margin-block: 20px;
  margin-bottom: 6px;
  background: linear-gradient(0deg, #ffbfc2, #fffbf0);
  /* border: 2px solid #FBE8FF; */
  border-radius: 20px;
  padding-top: 18px;
  overflow: hidden;
}

.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 80%;
  margin-inline: auto;
}

.header img {
  max-width: 60px;
  user-select: none;
  pointer-events: none;
}

.header img.left {
  transform: scaleX(-1);
}

.title {
  font-weight: 600;
  font-size: 18px;
  color: #de0432;
}

.faq {
  padding: 20px;
  margin-top: 10px;
  display: flex;
  flex-direction: column;
  gap: 10px;
  background-color: rgba(255, 255, 255, 0.2);
}

.faq .question {
  font-size: 18px;
  font-weight: 500;
  color: #b12a46;
}

.faq .answer {
  font-weight: 300;
  color: #b47973;
}

.answer span {
  color: #de0432;
  font-weight: 400;
}

.process-container {
  padding-block: 10px;
  margin-top: 10px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-inline: 30px;
}

.step {
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 8px;
}

.step-image-container {
  --size: 54px;
  background: linear-gradient(0deg, rgb(249, 153, 151, 0.4), rgba(246, 179, 213, 0.4));
  border-radius: 100px;
  width: var(--size);
  height: var(--size);
  display: grid;
  place-items: center;
}

.step-image-container img {
  width: 88%;
}

.step-info {
  text-align: center;
  color: #8d211a;
  font-weight: 300;
  font-size: 12px;
}

.arrow-next {
  height: 12px;
  margin-bottom: 34px;
}
</style>
