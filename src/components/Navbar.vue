<script setup>
import { ref } from 'vue';
let menuOpen = ref(false)
</script>


<template>
    <div :style="menuOpen ? 'display: block;' : ''" class="margin"></div>
    <nav :style="menuOpen ? 'position: fixed;top: 0;' : ''">
        <input v-model="menuOpen" type="checkbox" name="" id="check" />
        <label for="check" class="checkbtn">
            <i class="fas fa-bars"></i>
        </label>
        <img src="../assets/logo.svg" alt="">
        <ul>
            <li><a href="#">About</a></li>
            <li><a href="#">Sponsors</a></li>
            <li><a href="#">Contact</a></li>
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

.margin {
    height: 80px;
    width: 100%;
    display: none;
}

nav {
    background-color: #191928;
    width: 100%;
    height: 80px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    z-index: 10;
}

label.logo {
    color: white;
    font-size: 35px;
    line-height: 80px;
    font-weight: bold;
    padding-left: 100px;
}

nav ul {
    float: right;
    margin-right: 20px;
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
        background-color: #303545;
        top: 80px;
        left: -100%;
        z-index: 100;
        text-align: center;
        transition: all 0.5s;
    }

    nav ul li {
        display: block;
        margin: 50px 0;
        line-height: 30px;
    }

    nav ul li a {
        font-size: 20px;
    }

    a:hover,
    a.active {
        background: none;
        color: #0082e6;
    }

    #check:checked~ul {
        left: 0;
    }
}
</style>