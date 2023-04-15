<script>

</script>

<template>
    <div class="container">
        <h1>SCHEDULE</h1>
        <div class="schedule_wrapper">
            <img src="../assets/images/schedule.svg" alt="">
            <img src="../assets/images/schedule.svg" alt="">
            <img src="../assets/images/schedule.svg" alt="">
        </div>
    </div>
</template>

<style scoped>
.container {
    padding: 0 10%;
    margin-top: 70px;
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

.schedule_wrapper {
    margin-top: 70px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    gap: 50px;
}

@media(max-width:430px) {
    .container>h1 {
        font-size: 40px;
        letter-spacing: 0.01em;
    }
    .schedule_wrapper {
        margin-top: 25px;
    }
}
</style>