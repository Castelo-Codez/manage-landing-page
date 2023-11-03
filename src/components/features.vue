<template>
    <section class="features">
        <div class="container">
            <div class="left">
                <div class="text">
                    <h2>What's different about Manage?</h2>
                    <p>
                        Manage provides all the functionality your team needs,
                        without the complexity. Our software is tailor-made for
                        modern digital product teams.
                    </p>
                </div>
            </div>
            <div class="right">
                <ul role="listbox">
                    <li role="listbox">
                        <span class="num">01</span>
                        <div class="text">
                            <h3>Track company-wide progress</h3>
                            <p>
                                See how your day-to-day tasks fit into the wider
                                vision. Go from tracking progress at the
                                milestone level all the way done to the smallest
                                of details. Never lose sight of the bigger
                                picture again.
                            </p>
                        </div>
                    </li>
                    <li role="listbox">
                        <span class="num">02</span>
                        <div class="text">
                            <h3>Advanced built-in reports</h3>
                            <p>
                                Set internal delivery estimates and track
                                progress toward company goals. Our customisable
                                dashboard helps you build out the reports you
                                need to keep key stakeholders informed.
                            </p>
                        </div>
                    </li>
                    <li role="listbox">
                        <span class="num">03</span>
                        <div class="text">
                            <h3>Everything you need in one place</h3>
                            <p>
                                Stop jumping from one service to another to
                                communicate, store files, track tasks and share
                                documents. Manage offers an all-in-one team
                                productivity solution.
                            </p>
                        </div>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
.features {
    padding-top: 70px;
    .container {
        display: flex;
        flex-wrap: wrap;
        row-gap: 30px;
        @media (min-width: 992px) {
            column-gap: 50px;
        }
        > div {
            flex-basis: 100%;
            @media (min-width: 992px) {
                flex: 1;
            }
        }
        .left {
            text-align: center;
            @media (min-width: 992px) {
                text-align: left;
            }
            .text {
                @media (min-width: 992px) {
                    max-width: 500px;
                }
            }
            h2 {
                color: var(--primary-DarkBlue);
                font-size: 34px;
                font-weight: 700;
                margin-bottom: 10px;
                & + p {
                    color: var(--Neutral-DarkGrayishBlue);

                    line-height: 1.6;
                    @media (min-width: 992px) {
                        max-width: 360px;
                    }
                }
            }
        }
        .right {
            ul {
                li {
                    display: flex;
                    gap: 40px;
                    flex-direction: column;
                    text-align: center;
                    align-items: center;
                    margin-bottom: 40px;
                    span {
                        padding: 10px 30px;
                        display: block;
                        background-color: var(--primary-BrightRed);
                        color: var(--Neutral-VeryPaleRed);
                        border-radius: 27px;
                        font-weight: 700;
                    }
                    .text {
                        h3 {
                            font-weight: 700;
                            color: var(--primary-DarkBlue);
                            margin-bottom: 20px;
                            & + p {
                                line-height: 1.6;
                                color: var(--Neutral-DarkGrayishBlue);
                                @media (min-width: 992px) {
                                    max-width: 450px;
                                }
                            }
                        }
                    }
                    @media (min-width: 992px) {
                        flex-direction: row;
                        align-items: flex-start;
                        text-align: left;
                        column-gap: 25px;
                    }
                }
            }
        }
    }
}
</style>
