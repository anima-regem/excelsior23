<template>
    <div class="card_container">
        <div class="details">
            <img src="../assets/images/spkr1.png" alt="Card Image">
            <h2>{{ name }}</h2>
            <p>{{ position }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "card",
    props: ['image', 'name', 'position'],
}
</script>



<style scoped>
.card_container {
    width: 330px;
    height: 465px;
    background-color: #262626;
    box-shadow: 7.09677px 7.09677px 9.46237px -1.1828px rgba(0, 0, 0, 0.12);
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
}

.details {
    display: flex;
    flex-direction: column;
    gap: 25px;
}

.details>img {
    width: 282.69px;
    height: 282.69px;
    object-fit: cover;
    object-position: center;
}

.details {
    gap: 8px;
}

.details>h2 {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 700;
    font-size: 23.6559px;
    line-height: 29px;
    color: #FFFFFF;
}

.details>p {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 500;
    font-size: 18.9247px;
    line-height: 23px;
    color: #FFFFFF;
}

@media(max-width:430px) {
    .card_container {
        width: 160px;
        height: 200.23px;
        border-radius: 5px;
    }

    .details>img {
        width: 140px;
        height: 100px;
        border-radius: 5px;
    }

    .details>h2 {
        font-size: 10.6508px;
    }
    .details>p {
        font-size: 8.88109px;
    }

}
</style>