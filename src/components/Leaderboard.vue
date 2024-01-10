
<template>
    <div class="leaderboard-container">
        <div class="header">
            <img class="left" src="../assets/images/picture_title2.png" alt="arrow" />
            <span class="title">Leaderboard</span>
            <img src="../assets/images/picture_title2.png" alt="arrow" />
        </div>
        <div class="info">
            The top 10 Rebate Card users with the most beans get extra rewards.
        </div>
        <div class="table-header">
            <div>USER</div>
            <div>Rebate beans</div>
            <div>Reward</div>
        </div>
    </div>
</template>

<style scoped>
.leaderboard-container {
    background: url("../assets/images/background_leaderboard.png") top /100% no-repeat;
    display: flex;
    flex-direction: column;
    gap: 12px;
    width: 100%;
    padding-inline: 16px;
    min-height: 90dvh;
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
    color: #FFFFFF;
}

.info {
    background-color: rgba(255, 152, 161, 0.3);
    padding: 10px 12px;
    border-radius: 10px;
    color: var(--color-white);
    font-size: 14px;
    text-align: center;
}

.table-header {
    display: flex;
    color: rgba(255, 255, 255, 0.5);
    justify-content: space-around;
    font-size: 14px;
}

.table-header div:first-child {
    flex: 0.6;
    padding-left: 18px;
}
</style>