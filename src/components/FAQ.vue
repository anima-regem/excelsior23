<script setup>

</script>

<template>
    <div class="container">
        <div class="headerContainer">
            <div class="headerText">FAQ</div>
        </div>
        <div class="faqContainer">
            <div class="faqLeft">
                <div class="faqHead">Who all can participate in the event ?</div>
                <div class="answerLeft faqAnswer">There is no specific criteria for participation. Anyone interested can
                    participate in the event.</div>
            </div>
            <div class="faqRight">
                <div class="faqHead">Should I register for each event separately ?</div>
                <div class="answerRight faqAnswer">It is your preference that matters. You can join for more than an event
                    in Excelsior'23 provided you abide by the terms and conditions. For the same reason we have provided
                    packages which is a mixture of events. You can choose package according to your taste and preference.
                </div>
            </div>
            <div class="faqLeft">
                <div class="faqHead">Will I be refunded if I decide to cancel my registration ?</div>
                <div class="answerLeft faqAnswer">Oops! There is no provision for refund. But you'll avail the benefit of
                    refund in case if you have registered yourself twice for the same event by some technical issues. The
                    technical issues must be informed to the Excelsior'23 team as soon as possible. Genuine reasons with
                    evidences will be accepted and refunded.</div>
            </div>
            <div class="faqRight">
                <div class="faqHead">Is food and accomodation provided?</div>
                <div class="answerRight faqAnswer">Yes, it is included in the ticket price</div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container {
    margin: 8rem auto 0 auto;
}

.headerContainer {
    margin-left: 5rem;
}

.headerBack {
    position: relative;
}

.headerText {
    margin: -4.8rem 0 0 4rem;
    color: #fff;
    font-family: 'Poppins', sans-serif;
    font-weight: 800;
    font-size: 70px;
}

.faqContainer {
    margin: 8rem 8rem;
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: start;
}

.faqLeft {
    margin-top: 0rem;
    align-self: start;
    width: 45%;
}

.faqRight {
    margin-top: 4rem;
    align-self: flex-end;
    width: 45%;
}

.faqHead {
    color: #fff;
    font-family: 'Poppins', sans-serif;
    font-size: 35px;
    font-weight: 600;
    line-height: 40px;
}

.faqAnswer {
    font-size: 16px;
    padding-top: 1rem;
    margin-top: 2rem;
    color: #fff;
    font-family: 'Montserrat', sans-serif;
    font-weight: 300;
    text-align: justify;
}

.answerLeft {
    border-left: 1px solid #fff;
    padding-left: 2rem;
}

.answerRight {
    border-right: 1px solid #fff;
    padding-right: 2rem;
}

@media only screen and (max-width: 768px) {
    .container {
        padding-top: 10rem;
        margin: 0 auto 0 0;
        width: 100vw;
    }

    .headerContainer {
        z-index: 98;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 97%;
        height: 100%;
        margin: 0 auto;
    }

    .headerBack {}

    .headerText {
        position: absolute;
        margin: 1.8rem 0 0 0;
        color: white;
        font-size: 60px;
        font-family: 'Poppins', sans-serif;
    }

    .faqContainer {
        margin: 2rem auto;
        display: flex;
        flex-direction: column;
        justify-content: start;
        align-items: center;
    }

    .faqLeft {
        margin-top: 4rem;
        align-self: center;
        width: 90%;
    }

    .faqRight {
        margin-top: 4rem;
        align-self: center;
        width: 90%;
    }

    .faqHead {
        color: #fff;
        font-family: 'Poppins', sans-serif;
        font-size: 30px;
        height: auto;
        font-weight: 600;
        line-height: 34px;
    }

    .faqAnswer {
        font-size: 13px;
        padding-top: 1rem;
        margin-top: 1rem;
        color: #fff;
        font-family: 'Montserrat', sans-serif;
        font-weight: 300;
        text-align: justify;
    }

    .answerLeft {
        border-left: none;
        padding-left: 0;
    }

    .answerRight {
        border-right: none;
        padding-right: 0;
    }
}</style>