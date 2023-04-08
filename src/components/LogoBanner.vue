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
    background-color: hsla(0, 0%, 16%, 1);
    padding: 1rem 0;
    -webkit-backdrop-filter: blur(5px);
    -moz-backdrop-filter: blur(5px);
    -o-backdrop-filter: blur(5px);
    -ms-backdrop-filter: blur(5px);
    backdrop-filter: blur(5px);
    position: relative;

}

.cloud {
    --height: 400px;
    --blur: 150px;
    position: absolute;
    top: calc(-1 * (var(--height) - 100%) / 2);
    left: 15%;
    z-index: -2;
    background-image: linear-gradient(180deg, rgba(7, 55, 195, 0.4) 0%, rgba(20, 245, 127, 0.4) 100%);
    height: var(--height);
    width: 250px;
    -webkit-filter: blur(var(--blur));
    -moz-filter: blur(var(--blur));
    -o-filter: blur(var(--blur));
    -ms-filter: blur(var(--blur));
    filter: blur(var(--blur));
}

.logos {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1.25rem 2rem;
    flex-wrap: wrap;
    margin: 1rem 2rem;
}

.logos img {
    width: 13%;
}

.logos img[alt="WIELogo"] {
    width: 11%;
}

@media screen and (max-width:732px) {

    .logos {
        margin: 0.5rem 2rem;
    }

    .logos img {
        width: 20%;
    }
}


@media screen and (max-width:543px) {

    .logos {
        margin: 0.5rem 1rem;
    }

    .logos img {
        width: 16%;
    }
}

@media screen and (max-width:420px) {

    .logos {
        margin: 0.35rem 1rem;
        gap: 0.5rem 2rem;
    }
}
</style>