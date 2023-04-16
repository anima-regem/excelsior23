<script setup>
import { ref } from 'vue';
let menuOpen = ref(false)

function close() {
    document.getElementById('check').checked = false;
}

</script>


<template>
    <div :style="menuOpen ? 'display: block;' : ''" class="margin"></div>
    <nav>
        <input type="checkbox" name="" id="check" />
        <label for="check" class="checkbtn">
            <i class="fas fa-bars"></i>
        </label>
        <img src="../assets/logo.svg" alt="">
        <ul>
            <li><a href="#about" @click="close">About</a></li>
            <li><a href="#speakers" @click="close">Speakers</a></li>
            <li><a href="#footer" @click="close">Contact</a></li>
        </ul>
    </nav>
</template>


<style scoped>
* {
    padding: 0;
    margin: 0;
    text-decoration: none;
    list-style: none;
}

nav {
    background-color: #151B30;
    width: 100%;
    height: 80px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    z-index: -4;
}

label.logo {
    color: white;
    font-size: 35px;
    line-height: 80px;
    font-weight: bold;
    padding-left: 100px;
}



nav ul li {
    display: inline-block;
    line-height: 80px;
    margin-left: 5px;
}


nav ul li a {
    color: white;
    font-size: 17px;
    text-transform: uppercase;
    padding: 7px 13px;
    border-radius: 3px;
}

.checkbtn {
    font-size: 30px;
    color: white;
    float: right;
    line-height: 80px;
    margin-right: 40px;
    cursor: pointer;
    display: none;
}

#check {
    display: none;
}

@media (max-width: 952px) {
    label.logo {
        font-size: 30px;
        padding-left: 50px;
    }

    nav ul li a {
        font-size: 16px;
    }
}

@media (max-width: 715px) {
    .checkbtn {
        display: block;
    }

    img {
        width: 50vw;
    }

    ul {
        position: fixed;
        width: 100%;
        height: 100vh;
        z-index: 100;
        background-color: hsla(210, 30%, 24%, 0.756);
        top: 80px;
        left: -100%;
        text-align: center;
        transition: all 0.1s;
    }

    nav ul li {
        display: block;
        margin: 50px 0;
        line-height: 30px;
    }

    nav ul li a {
        font-size: 20px;
    }

    #check:checked~ul {
        left: 0;
    }
}
</style>
  