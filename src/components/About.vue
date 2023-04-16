<script setup>

</script>




<template>
    <section id="about">
        <h2 class="excelsior_name">EXCELSIOR'23</h2>

        <div class="more_info">
            <p>
                Excelsior 2022 is the fourth iteration of the flagship event of IEEE SB GEC Palakkad. It is conducted at
                Government Engineering College Sreekrishnapuram, Palakkad, and lasts for about 3 days. The participation of
                active and enthusiast engineering students all over Kerala marks the major attraction of the occasion.
            </p>
            <p>

                The tech fest comprises the coalesce of different technological workshops and interactive disquisitions by
                proficient personalities according to each student's passion in their respective fields.Excelsior’22 offers
                a platform for learning and augmenting technical virtuosity, and knowledge, without bound and in annex lots
                of fun and entertainment ingredients to boost up the spirit of vibrant technophiles.
            </p>
        </div>
        <div class="tagline">rise above the rest</div>
    </section>
</template>

<style scoped>
section {
    --font-large: 7vw;
    --font-medium: 2vw;
    --font-large: clamp(0.8rem, 7vw, 5rem);
    --font-medium: clamp(0.7rem, 2vw, 2rem);
    position: relative;
    /* height: 100vh; */
    display: flex;
    align-items: center;
    margin: 5rem auto;
    padding: 0 2rem;
    max-width: 80rem;
    gap: 1rem;
}




.excelsior_name {
    writing-mode: vertical-lr;
    transform: rotate(180deg);
    font-weight: 700;
    font-size: var(--font-large);


}

.more_info {
    font-size: var(--font-medium);
    font-weight: 500;
    flex-grow: 1000;
}

.more_info>p:first-child {
    margin: 1.75rem 0;
}

.tagline {
    font-weight: bolder;
    text-align: right;
    font-size: var(--font-large);
    color: hsla(0, 0%, 100%, 0.1);

}

@media screen and (max-width: 700px) {
    section {

        margin: 3rem auto;
        padding: 0 2rem;
    }
}

@media screen and (max-width: 500px) {
    section {
        --font-medium: clamp(0.7rem, 3vw, 2rem);
        margin: 2rem auto;
        padding: 0 2rem;
        flex-direction: column;
    }

    .excelsior_name {
        writing-mode: horizontal-tb;
        transform: rotate(0deg);
    }

    .more_info {
        text-align: center;
    }

    .more_info>p:first-child {
        margin: 1rem 0;
    }


}
</style>
