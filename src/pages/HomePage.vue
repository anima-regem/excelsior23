<script setup>
import FAQ from "../components/FAQ.vue";
import Footer from "../components/Footer.vue";
import Jumbotron from "../components/Jumbotron.vue";
import About from "../components/About.vue";
import LogoBanner from "../components/LogoBanner.vue";
import Speakers from "../components/Speakers.vue";
import Schedule from '../components/Schedule.vue'
import Navbar from "../components/Navbar.vue";
</script>

<template>
    <Navbar />
    <Jumbotron />
    <LogoBanner />
    <About />

    <Speakers />
    <Schedule />
    <FAQ />
    <Footer />
</template>