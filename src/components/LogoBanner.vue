<template>
    <section class="logo-container">
        <div class="logos">
            <img :src="IESBLogo" alt="IESBLogo">
            <img :src="CSLogo" alt="CSLogo">
            <img :src="IASLogo" alt="IASLogo">
            <img :src="comsocLogo" alt="comsocLogo">
            <img :src="WIELogo" alt="WIELogo">
            <img :src="IEEELogo" alt="IEEELogo">
        </div>
        <div class="cloud"></div>
    </section>
</template>

<script setup>
import IEEELogo from '../assets/images/IEEELogo.png';
import IASLogo from '../assets/images/IASLogo.png';
import IESBLogo from '../assets/images/IESBLogo.png';
import WIELogo from '../assets/images/WIELogo.png';
import CSLogo from '../assets/images/CSLogo.png';
import comsocLogo from '../assets/images/comsocLogo.png';
</script>

<style scoped>

.logo-container {
    background-color: hsla(0, 0%, 100%, 24%);
    padding: 1rem 0;
    -webkit-backdrop-filter: blur(5px);
    -moz-backdrop-filter: blur(5px);
    -o-backdrop-filter: blur(5px);
    -ms-backdrop-filter: blur(5px);
    backdrop-filter: blur(5px);
    position: relative;

}


.logos {
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    gap: 1.25rem 2rem;
    flex-wrap: wrap;
    margin: 1rem 2rem;
}

.logos img {
    width: 9%;
    min-width: 60px;
    vertical-align: middle;
}

.logos img[alt="WIELogo"] {
    min-width: 36px;
    width: 6%;
}

.logos img[alt="IEEELogo"] {
    width: 15%;
    min-width: 90px;
}

@media screen and (max-width:732px) {

    .logos {
        margin: 0.5rem 2rem;
    }

    /* .logos img {
        width: 10%;
    } */
}


@media screen and (max-width:543px) {

    .logos {
        margin: 0.5rem 1rem;
    }

}

@media screen and (max-width:420px) {

    .logos {
        margin: 0.35rem 1rem;
        gap: 0.5rem 2rem;
    }

}
</style>