<script setup>
    // import instagramLogo from "../assets/icon/instagram.svg";
    // import linkedinLogo from "../assets/icon/linkedin.svg";
</script>

<template>
  <footer class="section footer__container" id="footer">
    <section class="footer__useful-links">
      <h4 class="footer__heading footer__heading__useful">
        USEFUL LINKS
      </h4>
      <ul class="footer__list_container">
        <li class="footer__useful__link">
          <a class="footer__link" href="https://www.instagram.com/ieeesbgecpkd/" target="_blank">
            @ieeesbgecpkd
          </a>
        </li>
        <li class="footer__useful__link">
          <a class="footer__link" href="https://linkedin.com/company/ieeesbgecpkd" target="_blank">
            ieeesbgecpkd
          </a>
        </li>
        <li class="footer__useful__link">
          <a class="footer__link" href="https://ieee.org" target="_blank">
            IEEE
          </a>
        </li>
      </ul>
    </section>
    <section class="section footer__contact">
      <h4 class="footer__heading">CONTACT US</h4>
      <ul class="footer__link__container">
        <li>
          <a class="footer__link" href="tel:+919495951143">
            Sanju: +91 9495951143
          </a>
        </li>
        <li>
          <a class="footer__link" href="tel:+919895645290">
            Thamanna: +91 9895645290
          </a>
        </li>
        <li>
          <a class="footer__link" href="mailto:ieee@gecskp.ac.in" target="_blank">
            Email: ieee@gecskp.ac.in
          </a>
        </li>
      </ul>
    </section>
    <section class="section footer__about">
      <h4 class="footer__heading">ABOUT IEEE SB GEC PKD</h4>
      <p class="footer__about__para">
        The IEEE Students branch of Government Engineering College
        Palakkad, work for providing an ideal platform for young minds to
        nourish their technical skills as an engineer by providing a
        technical home. The SB comprises actively working with an IAS,
        ComSoc, and Computer Society and also the WiE affinity group in
        association for achieving the objectives.
      </p>
    </section>
    <section class="section footer__end">
      <p>Copyright &copy; 2022 IEEE SB GECPKD. All Rights Reserved</p>
      <div class="footer__socials">
        <a href="https://www.instagram.com/ieeesbgecpkd/" target="_blank">
          <!-- <img :src="instagramLogo" alt="instagram_logo" /> -->
        </a>
        <a href="https://linkedin.com/company/ieeesbgecpkd" target="_blank">
          <!-- <img :src="linkedinLogo" alt="linkedin_logo" /> -->
        </a>
      </div>
    </section>
  </footer>
</template>

<style scoped>
footer {
  margin-top: 70px;
  padding: 5rem;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  row-gap: 3rem;
  font-family: 'Montserrat', sans-serif;
  color: #fff;
  font-size: 1.2rem;
  font-weight: 400;
}

ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.footer__about__para {
  line-height: 1.5;
}

.footer__link:link,
.footer__link:visited {
  opacity: 1;
  text-decoration: none;
  color: #fff;
}

.footer__heading {
  margin-bottom: 1.1rem;
}

.footer__heading__useful {
  margin-bottom: 1.1rem;
}

.section {
  text-align: left;
}

.footer__useful__link:not(:last-child) {
  margin-bottom: 1.2rem;
}

.footer__useful__link::before {
  vertical-align: middle;
  background-color: #2CB774;
  border-radius: 50%;
  -webkit-border-radius: 50%;
  -moz-border-radius: 50%;
  -ms-border-radius: 50%;
  -o-border-radius: 50%;
  content: "";
  display: inline-block;
  width: 0.6rem;
  height: 0.6rem;
  margin-right: 10px;
  margin-bottom: 4px;
}

.footer__end {
  grid-column: 1/-1;
  display: flex;
}

.footer__socials {
  margin-left: auto;
  display: flex;
  gap: 1.2rem;
  position: relative;
}

.clip {
  cursor: pointer;
}

.clip:hover:before {
  position: absolute;
  transform: translate(-30%, -100%);
  font-size: 0.9rem;
  padding: 0.5rem;
  border-radius: 10px;
  content: attr(data-copy-status);
  display: inline-block;
  background-color: #000;
  color: #fff;
  -webkit-transform: translate(-30%, -100%);
  -moz-transform: translate(-30%, -100%);
  -ms-transform: translate(-30%, -100%);
  -o-transform: translate(-30%, -100%);
  -webkit-border-radius: 10px;
  -moz-border-radius: 10px;
  -ms-border-radius: 10px;
  -o-border-radius: 10px;

}

@media (max-width: 950px) {
  footer {
    padding: 4rem;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 0.3fr 1fr 0.5fr;
    row-gap: 2.9rem;
  }

  .footer__contact {
    justify-self: end;
  }

  .footer__socials {
    margin: 1rem 0;
  }

  .footer__end {
    flex-direction: column;
  }
}


@media (max-width: 723px) {
  footer {
    padding: 2.5rem;
    grid-template-columns: 1fr;
    grid-template-rows: 0.3fr 0.1fr 1fr;
    row-gap: 1rem;
    font-size: 0.8rem;
  }

  .footer__contact {
    justify-self: start;
  }

  .section {
    width: fit-content;
  }

  .footer__socials {
    margin: 1rem 0;
  }

  .footer__end {
    flex-direction: column;
  }

  .footer__useful__link:not(:last-child) {
    margin-bottom: 0.6rem;
  }

  .footer__heading {
    font-size: 1.3rem;
    font-weight: bold;
  }

  .clip:hover:before {
    transform: translate(-20%, -100%);
    -webkit-transform: translate(-20%, -100%);
    -moz-transform: translate(-20%, -100%);
    -ms-transform: translate(-20%, -100%);
    -o-transform: translate(-20%, -100%);
  }
}

@media (max-width: 430px) {
  footer {
    margin-top: 50px;
  }
}

@media (max-width: 400px) {
  footer {
    padding: 2rem;
    font-size: 0.81rem;
  }

  .footer__heading {
    font-size: 1rem;
  }
}
</style>