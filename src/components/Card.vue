<template>
    <div class='card__container rounded__card__container'>
          <div class="card__img__container">
              <img  :src="image" :alt="`${name}'s image`" />
          </div>
          <div class="card__text__container">
              <h3 class='card__text prim__text'> {{name}}</h3>
              <h4 class='card__text sec__text'>  <div class="wrap__text">{{ position }} </div> </h4>
          </div>
    </div>

<!-- 

    <div class="card_container">
        <div class="details">
            <img :src="image" alt="Card Image">
            <h2>{{ name }}</h2>
            <p>{{ position }}</p>
        </div>
    </div> -->
</template>
  
<script>
export default {
    name: "card",
    props: ['image', 'name', 'position'],
}
</script>
  


<style scoped>
:root {
    --rounded-card-height: 19rem;
    --rounded-card-mobile-height: 8.4rem;
    --rounded-card-width: 14rem;
    --rounded-card-mobile-width: 6.25rem;
    --card-mobile-height: 12rem;
    --card-mobile-width: 9.1rem;
}

.card__container {
    color: #fff;
    background: #262626;
    display: flex;
    flex-direction: column;
    width: 20.6rem;
    height: 30rem;
    border-radius: 0.5rem;
    padding: 1rem;
    box-shadow: rgba(0, 0, 0, 0.24) 0 3px 8px;
}

.rounded__card__container {
    width: 20rem;
}

.card__img__container {
    overflow: hidden;
    height: 18.6rem;
    width: 100%;
    position: relative;
    margin-bottom: 1rem;
}

.wrap__text {
    display: flex;
}


.card__img__container img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
    position: absolute;
    inset: 0;
    border-radius: 0.2rem;
    -webkit-border-radius: 0.2rem;
    -moz-border-radius: 0.2rem;
    -ms-border-radius: 0.2rem;
    -o-border-radius: 0.2rem;
}

.card__text__container {
    display: flex;
    flex-direction: column;
}

.card__text {
    font-weight: 700;
}

.prim__text {
    font-size: 1.5rem;
}

.sec__text {
    line-height: 2rem;
    font-size: 1.1rem;
    font-style: italic;
}

@media (max-width: 1000px) {
    .card__container {
        height: calc(var(--card-mobile-height) + 10rem);
        width: calc(var(--card-mobile-width) + 6rem);
    }

    .rounded__card__container {
        height: calc(var(--card-mobile-height) + 13.3rem);
        width: calc(var(--card-mobile-width) + 7rem);
    }

    .card__img__container {
        height: 13.8rem;
        flex-shrink: 0;
    }

    .wrap__text {
        width: 105%;
    }
}

@media(max-width: 570px) {
    .card__container {
        gap: 0;
        padding: 0.7rem 0.5rem;
        height: calc(var(--card-mobile-height) + 6rem);
        width: calc(var(--card-mobile-width) + 3rem);
    }

    .card__img__container {
        height: 10.8rem;
        flex-shrink: 0;
    }

    .card__img__container img {
        object-fit: cover;
        height: 100%;
    }

    .card__text {
        font-size: 1rem;
    }

    .card__text__container {
        padding: 0;
    }

    .sec__text {
        font-size: 0.8rem;
        line-height: 1rem;
    }

    .rounded__card__container {
        height: calc(var(--card-mobile-height) + 6.3rem);
        width: calc(var(--card-mobile-width) + 2rem);
    }

}

@media (max-width: 474px) {
    .card__container {
        height: calc(var(--card-mobile-height) + 3.1rem);
        width: calc(var(--card-mobile-width) + 0.1rem);
    }

    .card__img__container {
        height: 7.8rem;
    }

    .sec__text {
        line-height: 0.75rem;
        font-size: 0.6rem;
    }

    .wrap__text {
        width: 103%;
    }
}

@media (max-width: 370px) {


    .card__container {
        height: calc(var(--card-mobile-height) + 1rem);
        width: calc(var(--card-mobile-width) - 1rem);
    }

    .rounded__card__container {
        height: calc(var(--card-mobile-height) + 3rem);
        width: calc(var(--card-mobile-width) - 0.7rem);
    }


    .prim__text {
        font-size: 1rem;
    }
}

@media (max-width: 320px) {
    .card__container {
        height: calc(var(--card-mobile-height) + 4rem);
        width: calc(var(--card-mobile-width) + 0rem);
    }

    .rounded__card__container {
        height: calc(var(--card-mobile-height) + 3rem);
        width: calc(var(--card-mobile-width) + 0.2rem);
    }
}
</style>