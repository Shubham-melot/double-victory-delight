<script setup>
import LangSelect from './LangSelect.vue';

const props = defineProps({
    eventDate: String,
})
</script>

<template>
    <header>
        <span class="event-date" id="eventDate">{{ props.eventDate || "10/11 - 30/11" }}</span>
        <LangSelect />
    </header>
</template>

<style scoped>
header {
    background: url("../assets/images/header.jpg") center / 100% 100% no-repeat;
    width: 100%;
    min-height: 300px;
    position: relative;
}

.event-date {
    display: grid;
    place-items: center;
    position: absolute;
    bottom: 22px;
    left: 50%;
    transform: translateX(-50%);
    background-color: var(--color-accent);
    color: var(--color-white);
    border-radius: 20px;
    padding: 4px 6px;
}
</style>