<script setup>
import Splide from "@splidejs/splide";
import {AutoScroll} from "@splidejs/splide-extension-auto-scroll";
import {onMounted} from "vue";
import Getstarted from "./Getstarted.vue";
onMounted;
onMounted(() => {
    let splide = new Splide(".splide", {
        type: "loop",
        focus: "center",
        perPage: 1,
        arrows: false,
        autoScroll: false,
        gap: 50,
        mediaQuery: "min",
        breakpoints: {
            768: {
                perPage: 3,
                autoScroll: true,
            },
            992: {
                gap: 180,
            },
        },
    });
    splide.mount({AutoScroll});
});
</script>
<template>
    <section>
        <h3>What they've said</h3>
        <div class="splide" role="group" aria-label="Splide Basic HTML Example">
            <div class="splide__track">
                <ul class="splide__list">
                    <li class="splide__slide">
                        <div class="content">
                            <div class="image">
                                <img
                                    src="../assets/images/avatar-ali.png"
                                    alt="avatar-ali"
                                />
                            </div>
                            <h4>Ali Bravo</h4>
                            <p>
                                “We have been able to cancel so many other
                                subscriptions since using Manage. There is no
                                more cross-channel confusion and everyone is
                                much more focused.”
                            </p>
                        </div>
                    </li>
                    <li class="splide__slide">
                        <div class="content">
                            <div class="image">
                                <img
                                    src="../assets/images/avatar-anisha.png"
                                    alt="avatar-anisha"
                                />
                            </div>
                            <h4>Anisha Ali</h4>
                            <p>
                                “Manage has supercharged our team’s workflow.
                                The ability to maintain visibility on larger
                                milestones at all times keeps everyone
                                motivated.”
                            </p>
                        </div>
                    </li>
                    <li class="splide__slide">
                        <div class="content">
                            <div class="image">
                                <img
                                    src="../assets/images/avatar-richard.png"
                                    alt="avatar-richard"
                                />
                            </div>
                            <h4>Richard Watts</h4>
                            <p>
                                “Manage allows us to provide structure and
                                process. It keeps us organized and focused. I
                                can’t stop recommending them to everyone I talk
                                to!”
                            </p>
                        </div>
                    </li>
                    <li class="splide__slide">
                        <div class="content">
                            <div class="image">
                                <img
                                    src="../assets/images/avatar-shanai.png"
                                    alt="avatar-shanai"
                                />
                            </div>
                            <h4>Shanai Gough</h4>
                            <p>
                                “Their software allows us to track, manage and
                                collaborate on our projects from anywhere. It
                                keeps the whole team in-sync without being
                                intrusive.”
                            </p>
                        </div>
                    </li>
                </ul>
            </div>
        </div>
        <Getstarted text="Get Started" />
    </section>
</template>
<style scoped lang="scss">
section {
    padding: 60px 0px 220px;
    position: relative;
    h3 {
        text-align: center;
        color: var(--primary-DarkBlue);
        font-size: 31px;
        margin-bottom: 100px;
    }
    > button {
        display: block;
        position: absolute;
        bottom: 5rem;
        transform: translateX(-50%);
        left: 50%;
    }
    .splide {
        .splide__slide {
            .content {
                display: flex;
                align-items: center;
                flex-direction: column;
                row-gap: 30px;
                .image {
                    max-width: 60px;
                    img {
                        width: 100%;
                    }
                }
                h4 {
                    color: var(--primary-DarkBlue);
                    font-weight: 700;
                    & + p {
                        line-height: 1.7;
                        text-align: center;
                        color: var(--Neutral-DarkGrayishBlue);
                    }
                }
            }
        }
        .splide__list {
            transition-timing-function: linear;
        }
    }
}
</style>
