<template>
    <div class="container">
        <h1>SPEAKERS</h1>
        <div class="speaker_section">
            <Card v-for="speaker in speakerdata" :image="speaker.image" :name="speaker.name" :position="speaker.position" />
        </div>
    </div>
</template>

<script setup>
import Card from './Card.vue';
import speakerdata from '../assets/data/speakers.json'

</script>


<style scoped>
.container {
    padding: 0 10%;
}

.container>h1 {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 800;
    font-size: 70.3536px;
    line-height: 86px;
    letter-spacing: 0.01em;
    color: #FFFFFF;
    text-shadow: 5.47692px 4.38154px 5.47692px rgba(0, 0, 0, 0.25);
}

.speaker_section {
    margin-top: 70px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    gap: 50px;
}

@media(max-width:430px) {
    .container{
        padding: 0 5%;
    }
    .container>h1 {
        font-size: 40px;
        letter-spacing: 0.01em;
    }

    .speaker_section {
        margin-top: 25px;
        justify-content: space-evenly;
        gap: 20px;
    }
}
</style>