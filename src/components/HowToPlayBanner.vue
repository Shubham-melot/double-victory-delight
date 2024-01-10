
<script setup>
const OYETALK_VERSION = "2.8.5"
</script>

<template>
    <div class="how-to-play-container">
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
                <div class="step-info">
                    Purchase <br>
                    Rebate Card
                </div>
            </div>
            <img class="arrow-next" src="../assets/images/picture_arrow1.png" alt="Next" />

            <div class="step">
                <div class="step-image-container">
                    <img src="../assets/images/how_to_play2.png" alt="Buy" />
                </div>
                <div class="step-info">
                    Activate <br>
                    Rebate Card
                </div>
            </div>
            <img class="arrow-next" src="../assets/images/picture_arrow1.png" alt="Next" />

            <div class="step">
                <div class="step-image-container">
                    <img src="../assets/images/how_to_play3.png" alt="Buy" />
                </div>
                <div class="step-info">
                    Start playing <br>
                    Royal Pattern
                </div>
            </div>
        </div>

        <div class="faq">
            <div class="question">
                What is Rebate cards?
            </div>
            <div class="answer">
                Exclusively available for OyeTalk Royal Pattern users, the Rebate Card is a premium in-game item. If you
                don't
                win a game <span>(by not betting on the winning seat)</span>, using the Rebate Card guarantees a
                <span>5%</span> bean
                rebate
                to reduce your losses.
                <br>
                <span>Please update to the latest version {{ OYETALK_VERSION }} of OyeTalk to enjoy this feature.</span>
            </div>
        </div>
    </div>
</template>

<style scoped>
.how-to-play-container {
    width: 90%;
    margin-inline: auto;
    margin-block: 20px;
    margin-bottom: 6px;
    background: linear-gradient(0deg, #FFBFC2, #FFFBF0);
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
    color: #DE0432;
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
    color: #B12A46;
}

.faq .answer {
    font-weight: 300;
    color: #B47973;
}

.answer span {
    color: #DE0432;
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
    color: #8D211A;
    font-weight: 300;
    font-size: 12px;
}

.arrow-next {
    height: 12px;
    margin-bottom: 34px;
}
</style>