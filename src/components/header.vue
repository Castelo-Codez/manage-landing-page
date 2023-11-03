<script setup>
import {ref, computed, onMounted, watch} from "vue";
import getStartedBtn from "./Getstarted.vue";
const ulState = ref(false);
const classObj = computed(() => {
    return {
        active: ulState.value,
    };
});
watch(ulState, (newva) =>
    newva
        ? document.body.classList.add("de-overflow")
        : document.body.classList.remove("de-overflow")
);
</script>
<template>
    <header>
        <div class="container">
            <a href="#">
                <img src="../assets/images/logo.svg" alt="logo.svg" />
            </a>
            <ul role="listbox">
                <li role="listitem">
                    <a href="#" role="link">Pricing</a>
                </li>
                <li role="listitem">
                    <a href="#" role="link">Product</a>
                </li>
                <li role="listitem">
                    <a href="#" role="link"> About Us</a>
                </li>
                <li role="listitem">
                    <a href="#" role="link"> Careers</a>
                </li>
                <li role="listitem">
                    <a href="#" role="link"> Community</a>
                </li>
            </ul>
            <ul role="listbox" :class="['tab-sm-ul', classObj]">
                <li role="listitem">
                    <a href="#" role="link">Pricing</a>
                </li>
                <li role="listitem">
                    <a href="#" role="link">Product</a>
                </li>
                <li role="listitem">
                    <a href="#" role="link"> About Us</a>
                </li>
                <li role="listitem">
                    <a href="#" role="link"> Careers</a>
                </li>
                <li role="listitem">
                    <a href="#" role="link"> Community</a>
                </li>
            </ul>
            <getStartedBtn text="Get started" />
            <button
                role="button"
                @click="ulState = !ulState"
                class="list-opener"
            >
                <span class="icon">
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="25"
                        height="18"
                    >
                        <g fill="#242D52" fill-rule="evenodd">
                            <path d="M0 0h25v4H0zM0 7h25v4H0zM0 14h25v4H0z" />
                        </g>
                    </svg>
                </span>
            </button>
        </div>
    </header>
    <div :class="[classObj, 'overlay-theme']" @click="ulState = false"></div>
</template>

<style scoped lang="scss">
%main-transition {
    transition: 0.3s ease-in-out;
}
header {
    padding-top: 40px;
    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        position: relative;
        z-index: 10;
        a {
            img {
                width: 100%;
            }
        }
        ul:not(.tab-sm-ul) {
            display: none;
            align-items: center;
            li {
                a {
                    display: block;
                    padding: 0px 15px;
                    font-size: 13.5px;
                    color: var(--Neutral-VeryDarkBlue);
                    text-transform: capitalize;
                    font-weight: 500;
                    @extend %main-transition;
                    &:hover {
                        color: var(--Neutral-DarkGrayishBlue);
                    }
                }
            }
            @media (min-width: 992px) {
                display: flex;
            }
        }
        .tab-sm-ul {
            position: absolute;
            top: calc(100% + 36px);
            background-color: var(--Neutral-VaryLightGray);
            width: 90%;
            transform: scale(0);
            transform-origin: top right;
            left: 5%;
            padding: 40px 0px;
            text-align: center;
            transition: 0.2s;
            border-radius: 20px;
            &.active {
                transform: scale(1);
                @media (min-width: 992px) {
                    display: none;
                }
            }
            li {
                margin-bottom: 10px;
                a {
                    color: var(--Neutral-VeryDarkBlue);
                    font-weight: 600;
                    &:hover {
                        text-decoration: underline;
                    }
                }
            }
        }
        .list-opener {
            display: block;
            border: none;
            cursor: pointer;
            @media (min-width: 992px) {
                display: none;
            }
        }
    }
}
.overlay-theme {
    position: absolute;
    width: 100%;
    height: 100%;
    display: none;
    top: 0;
    left: 0;
    z-index: 3;
    background-image: linear-gradient(
        14deg,
        var(--Neutral-VeryDarkBlue),
        transparent
    );

    &.active {
        display: block;
        @media (min-width: 992px) {
            display: none;
        }
    }
}
</style>
