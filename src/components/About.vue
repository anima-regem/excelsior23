<script setup>

</script>

<template>
    <main>
        <div class="left">
            <div class="excelsior_name">EXCELSIOR'23</div>
            <!-- <img src="../assets/excelsior_bg.svg" class="excelsior_bg"/> -->
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
    position: relative;
    height: 100vh;
    width: 100%;
    overflow-x: hidden;
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
    font-size: 5vw;
    font-weight: 700;
    color: #f5f5f5;
    padding: 10%;
    padding-top: 20%;
}

.excelsior_name::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    background-image: url('../assets/excelsior_bg.svg');
    background-size: contain;
    background-repeat: no-repeat;
}

.right {
    padding-top: 12.5%;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 50%;
    float: right;
}

.more_info {
  white-space: normal;
  padding: 10%;
}

.tagline {
    font-size: 2vw;
    letter-spacing: 1rem;
    white-space: nowrap;
    font-weight: 500;
    padding-bottom: 5%;
}

@media (max-width: 768px) {
  .left, .right {
    width: 100%;
    float: none;
    /* word-wrap: normal; */
  }
  .left {
    order: 2;
  }
  .tagline {
    font-size: 3vw;
    letter-spacing: 2vw;
    white-space: nowrap;
    font-weight: 500;
    padding-bottom: 5%;
}

}
</style>
