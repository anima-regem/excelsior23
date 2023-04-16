<script setup>
import facemask from "../assets/images/facemask.png"
import logo from "../assets/images/logo.png"
import jumbatronHeader from '../assets/logo.svg'
import excelsiorLogo from '../assets/images/ExcelsiorLogoLinear.svg'
</script>

<template>
    <section class="jumbatron">
        <img class="logo" :src="logo" alt="logo">
        <div class="content">
            <div class="date">
                <img :src="jumbatronHeader" alt="" class="title">
                <img :src="excelsiorLogo" alt="" class="content-logo">
                <h2>28<span class="thin">|</span>29<span class="thin">|</span>30 APRIL 2023</h2>
                <a href="/" class="reg-btn">Register</a>
            </div>
            <div class="facemask">
                <img :src="facemask" alt="mask">
            </div>
        </div>
    </section>
</template>


<style>
.jumbatron {
    --font-large: 4vw;
    --font-btn: 2vw;
    --font-large: clamp(0.8rem, 4vw, 3rem);
    --font-btn: clamp(0.7rem, 2vw, 2rem);
    position: relative;
    background-image: url("/background_spotted.png");
    background-size: contain;
    overflow: hidden;
}

.thin {
    font-weight: 100;
    color: hsl(0, 0%, 50%);
}

.title {
    width: 40%;
}

@supports (background: paint(something)) {
    @property --left-clr {
        syntax: '<color>';
        inherits: true;
        initial-value: #55D5D7;
    }

    @property --middle-clr {
        syntax: '<color>';
        inherits: true;
        initial-value: #007A68;
    }

    @property --right-clr {
        syntax: '<color>';
        inherits: true;
        initial-value: #022BA1;
    }

    .reg-btn:hover,
    .reg-btn:focus-visible {
        --left-clr: #022BA1;
        --middle-clr: #022BA1;
        --right-clr: #022BA1;
    }


}

@supports not (background: paint(something)) {

    .reg-btn:hover,
    .reg-btn:focus-visible {
        transform: translateY(-3px);
    }
}

.reg-btn {
    --left-clr: #55D5D7;
    --middle-clr: #007A68;
    --right-clr: #022BA1;
    text-decoration: none;
    color: white;
    background-image: linear-gradient(98.55deg, var(--left-clr) 0.36%, var(--middle-clr) 52.55%, var(--right-clr) 99.96%);
    ;
    width: fit-content;
    padding: 0.75em 1.75em;
    margin-top: 0.5rem;
    border-radius: 2em;
    font-weight: 500;
    font-size: var(--font-btn);
    transition: --right-clr 150ms,
        --middle-clr 300ms 150ms,
        --left-clr 300ms 150ms,
        transform 500ms ease-in-out;
}



.content-logo {
    width: 60%;
}

.jumbatron::after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -10;
    /* background-color: hsla(0, 0%, 16%, 0.4); */
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
    padding-left: 2rem;
}

.date h2 {
    font-size: var(--font-large);
    font-weight: 600;
    margin: 0;
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



    .facemask img {
        transform: translateX(-10%);
    }

}

@media screen and (max-width: 600px) {
    .content {
        padding-top: 3rem;
        padding-bottom: 2rem;
    }



    .facemask img {
        transform: translateX(-5%);
    }

}

@media screen and (max-width: 450px) {
    .content {
        padding-top: 2rem;
        padding-bottom: 2rem;
        grid-template-columns: 1fr 1fr 1fr;
    }

    .date {
        grid-column: 1/3;
    }

    .facemask img {
        width: 150%;
        transform: translateX(-30%);
    }

    .logo {
        width: 50%;
        left: 13%;
        top: 5%;
    }
}

@media screen and (max-width: 375px) {
    .content {
        padding-top: 1.5rem;
        padding-bottom: 2rem;
    }
}
</style>