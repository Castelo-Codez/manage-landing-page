<script setup>
defineProps({
    text: String,
});
</script>

<template>
    <button role="button">{{ text }}</button>
</template>

<style lang="scss" scoped>
button {
    border-radius: 35px;
    border: none;
    background-color: var(--primary-BrightRed);
    color: var(--Neutral-VaryLightGray);
    cursor: pointer;
    display: none;
    padding: 15px 30px;
    font-weight: 700;
    transition: 0.4s;
    &:hover {
        filter: brightness(1.5);
    }
    @media (min-width: 992px) {
        display: block;
    }
}
</style>
