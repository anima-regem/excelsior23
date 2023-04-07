<script setup>

</script>

<template>
    <main>
        <div class="left">
            <div class="excelsior_name">EXCELSIOR'23</div>
            <div class="excelsior_bg"></div>
        </div>

        <div class="right">
            <div class="tagline">RISE ABOVE THE REST</div>
            <div class="more_info">
                Excelsior 2022 is the fourth iteration of the flagship event of IEEE SB GEC Palakkad. It is conducted at
                Government Engineering College Sreekrishnapuram, Palakkad, and lasts for about 3 days. The participation of
                active and enthusiast engineering students all over Kerala marks the major attraction of the occasion.

                The tech fest comprises the coalesce of different technological workshops and interactive disquisitions by
                proficient personalities according to each student's passion in their respective fields.Excelsior’22 offers
                a platform for learning and augmenting technical virtuosity, and knowledge, without bound and in annex lots
                of fun and entertainment ingredients to boost up the spirit of vibrant technophiles.

            </div>
        </div>
    </main>
</template>

<style scoped>
    main {
        height: 100%;
        width: 100%;
    }

    .left {
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
        width: 50%;
        float: left;
    }

    .excelsior_name {
        font-size: 5rem;
        font-weight: 700;
        color: #f5f5f5;
        padding: 10%;
    }

    .excelsior_bg {
        position: absolute;
        background-image: url("../assets/excelsior_bg.svg");
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
        width: 100%;
        height: 100%;
        z-index: -1;
    }

    .right {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 50%;
        float: right;
    }
</style>