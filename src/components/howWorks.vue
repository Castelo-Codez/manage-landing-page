<script setup>
import Getstarted from "./Getstarted.vue";
</script>
<template>
    <section>
        <div class="container">
            <div class="left">
                <h4>Simplify how your team works today.</h4>
            </div>
            <div class="right">
                <Getstarted text="Get started" />
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
section {
    padding: 40px;
    background: var(--primary-BrightRed);
    position: relative;
    z-index: 6;
    &::before {
        content: "";
        position: absolute;
        width: 634px;
        height: 114%;
        top: -27px;
        left: 4%;
        background-image: url(/src/assets/images/bg-tablet-pattern.svg);
        background-size: cover;
        background-repeat: no-repeat;
        opacity: 0.1;
        z-index: -1;
        @media (max-width: 992px) {
            display: none;
        }
    }

    &::after {
        content: "";
        position: absolute;
        background-image: url(/src/assets/images/bg-tablet-pattern.svg);
        background-size: cover;
        z-index: -1;
        width: 500px;
        top: -2rem;
        opacity: 0.1;
        height: 100%;
        background-repeat: no-repeat;
        right: -18rem;
        transform: rotate(190deg);
        @media (max-width: 992px) {
            left: -22rem;
            transform: rotate(44deg);
            top: -4rem;
        }
    }
    .container {
        display: flex;
        flex-direction: column;
        row-gap: 15px;
        @media (min-width: 992px) {
            flex-direction: row;
            align-items: center;
            row-gap: 0px;
            > div {
                flex: 1;
            }
        }
    }
    .left {
        h4 {
            text-align: center;
            font-size: 32px;
            line-height: 1.5;
            font-weight: 700;
            color: var(--Neutral-VaryLightGray);
            @media (min-width: 992px) {
                text-align: left;
                max-width: 400px;
            }
        }
    }
    .right {
        display: flex;
        justify-content: center;
        align-items: center;
        @media (min-width: 992px) {
            justify-content: flex-end;
        }
        button {
            background-color: var(--Neutral-VaryLightGray);
            color: var(--primary-BrightRed);
            display: block;
        }
    }
}
</style>
