<template>
    <!-- <div class='card__container rounded__card__container'>
          <div class="card__img__container">
              <img  :src="image" :alt="`${name}'s image`" />
          </div>
          <div class="card__text__container">
              <h3 class='card__text prim__text'> {{name}}</h3>
              <h4 class='card__text sec__text'>  <div class="wrap__text">{{ position }} </div> </h4>
          </div>
    </div> -->


    <div class="card_container">
        <div class="details">
            <img :src="image" alt="Card Image">
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
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border-radius: 12px;
}

.details {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    gap: 16px;
}

.details>img {
    width: 282.69px;
    height: 282.69px;
    object-fit: cover;
    object-position: center;
    border-radius: 12px;
}

.details>h2 {
    font-style: normal;
    font-weight: 700;
    font-size: 23.6559px;
    line-height: 29px;
    color: #FFFFFF;
}

.details>p {
    font-style: normal;
    font-weight: 500;
    font-size: 18.9247px;
    line-height: 23px;
    color: #FFFFFF;
}

@media(max-width:430px) {
    .card_container {
        width: 146.94px;
        height: 206.46px;
        border-radius: 5px;
    }

    .details {
        gap: 10px;
        justify-content: space-evenly;
    }

    .details>img {
        width: 125.88px;
        height: 125.88px;
        border-radius: 5px;
    }

    .details>h2 {
        font-size: 11px;
        line-height: 12px;
    }

    .details>p {
        font-size: 9px;
        line-height: 10px;
    }

}
</style>


