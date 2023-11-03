<script setup>
import getStartedBtn from "./Getstarted.vue";
</script>
<template>
    <section class="landing">
        <div class="container">
            <div class="left-side">
                <h1>Bring everyone together to build better products.</h1>
                <p>
                    Manage makes it simple for software teams to plan day-to-day
                    tasks while keeping the larger team goals in view.
                </p>
                <getStartedBtn text="Get started" />
            </div>
            <div class="right-side">
                <div class="image">
                    <img
                        src="../assets/images/illustration-intro.svg"
                        alt="illustration-intro"
                    />
                </div>
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
section {
    padding-top: 100px;
    .container {
        display: flex;
        flex-direction: column;
        @media (min-width: 768px) {
            flex-direction: row;
            align-items: center;
        }
        gap: 20px;
        column-gap: 20px;
        .left-side {
            > *:not(:last-child) {
                margin-bottom: 30px;
                text-align: center;
                @media (min-width: 768px) {
                    text-align: left;
                }
            }
            h1 {
                font-size: 30px;
                font-weight: 700;
                color: var(--primary-DarkBlue);
                @media (min-width: 992px) {
                    font-size: 60px;
                }
                & + p {
                    max-width: 350px;

                    line-height: 1.6;
                    color: var(--Neutral-DarkGrayishBlue);
                    margin: {
                        left: auto;
                        right: auto;
                    }
                    @media (min-width: 768px) {
                        margin: 0;
                    }
                }
            }
            button {
                display: block;
                margin: {
                    left: auto;
                    right: auto;
                }
                @media (min-width: 768px) {
                    margin: 0;
                }
            }
        }
        .right-side {
            order: -1;
            @media (min-width: 768px) {
                order: 2;
            }
            .image {
                img {
                    width: 100%;
                }
            }
        }
        @media (min-width: 768px) {
            > div {
                flex: 1;
            }
        }
    }
}
</style>
