<script setup>
import facemask from "../assets/images/facemask.png"
import logo from "../assets/images/logo.png"
</script>

<template>
    <nav>
        <input type="checkbox" name="" id="check" />
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
    <section class="jumbatron">
        <img class="logo" :src="logo" alt="logo">
        <div class="content">
            <div class="date">
                <h2>28, 29, 30 April</h2>
            </div>
            <div class="facemask">
                <img :src="facemask" alt="mask">
            </div>
        </div>
    </section>
</template>


<style>
.jumbatron {
    position: relative;
    background-image: url("/background_spotted.png");
    background-size: contain;
    overflow: hidden;
}

.jumbatron::after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: hsla(0, 0%, 16%, 0.4);
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
    font-size: 2.5rem;
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

@media screen and (max-width: 450px) {
    .content {
        padding-top: 2rem;
        padding-bottom: 2rem;
        grid-template-columns: 1fr 1fr 1fr;
    }

    .date {
        grid-column: 1/3;
    }

    .date h2 {
        font-size: 1.25rem;
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



/* navbar */

* {
    padding: 0;
    margin: 0;
    text-decoration: none;
    list-style: none;
}

nav {
    background-color: #02071a;
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

nav ul {
    /* float: right;
    margin-right: 20px; */
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
        background-color: #2c3e50;
        top: 80px;
        left: -100%;
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

    #check:checked~ul {
        left: 0;
    }
}
</style>