<script setup>
import facemask from "../assets/images/facemask.png"
import logo from "../assets/images/logo.png"
</script>

<template>
    <div class="jumbatron">
        <img class="logo" :src="logo" alt="logo">
        <div class="content">
            <div class="date">
                <h2>28, 29, 30 April</h2>
            </div>
            <div class="facemask"><img :src="facemask" alt="mask"></div>
        </div>
    </div>
</template>


<style scoped>
nav {
    height: 4rem;
}

.jumbatron {
    position: relative;
    background-image: url("/background_spotted.png");
    background-size: contain;
}

.logo {
    position: absolute;
    width: 61%;
    left: 5%;
    top: 5%;
}

.content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding-top: 5rem;
    padding-bottom: 3rem;
}

.date {
    display: grid;
    place-content: center;
}

.date h2 {
    font-size: 3rem;
}

.facemask img {
    width: 100%;
    transform: translateX(-15%);
}

@media screen and (max-width:900px) {
    .content {
        padding-top: 4rem;
        padding-bottom: 2.5rem;
    }

    .date h2 {
        font-size: 2rem;
    }

    .facemask img {
        transform: translateX(-10%);
    }

}

@media screen and (max-width: 600px) {
    .content {
        padding-top: 3rem;
        padding-bottom: 2rem;
    }

    .date h2 {
        font-size: 1.5rem;
    }

    .facemask img {
        transform: translateX(-5%);
    }

}
</style>