<template>
<section id="footer">
      <div class="info container">
        <div class="info-item" id="discover-item">
          <h4 class="text-white">Discover</h4>
          <div class="cities">
            <a href="index.html" class="city"
              ><i class="bi bi-caret-right"></i> Durban</a
            >
            <a href="index.html" class="city"
              ><i class="bi bi-caret-right"></i> Cape Town</a
            >
            <a href="index.html" class="city"
              ><i class="bi bi-caret-right"></i> Johannesburg</a
            >
            <a href="index.html" class="city"
              ><i class="bi bi-caret-right"></i> East London</a
            >
          </div>
        </div>
        <div class="info-item">
          <h4 class="text-white" id="contact-header">Contact Us</h4>
          <div class="contact">
            <div class="contact-item">
              <i class="bi bi-geo"></i> 1590 Cheriton Dr Port Shepstone, KZN
              4243
            </div>
            <div class="contact-item">
              <i class="bi bi-telephone"></i> 085 783 8992
            </div>
            <div class="contact-item">
              <i class="bi bi-envelope"></i> help@sterlingholdings.co.za
            </div>
          </div>
        </div>
        <div class="info-item" id="newsletter-wrapper">
          <div>
            <h4 class="text-white">Newsletter</h4>
          </div>
          <div id="newsletter">
            <input
              type="email"
              id="email-input"
              placeholder="Enter your email"
            />
            <button type="submit" id="email-btn">Submit</button>
          </div>
          <div>
            <p class="fw-light text-white" id="newsletter-notice">
              sign up for our news letter to get alerted whenever a new property
              goes on the market.
            </p>
          </div>
        </div>
      </div>
      <footer id="footer-container">
        <span class="rights text-white"> © Sterling - All rights reserved</span>
        <img src="https://raw.githubusercontent.com/0xjoshva/RealEstate-Website/main/assets/realLOGO2.png" alt="logo" id="logo-footer" />
        <div class="socials-wrapper">
          <div class="linkedin text-white">
            <i class="bi bi-linkedin"></i>
          </div>
          <div class="twitter text-white">
            <i class="bi bi-twitter"></i>
          </div>
          <div class="facebook text-white">
            <i class="bi bi-facebook"></i>
          </div>
          <div class="instagram text-white">
            <i class="bi bi-instagram"></i>
          </div>
        </div>
      </footer>
    </section>
</template>

<style>
footer {
  width: 100% !important;
}

#footer-container {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  width: 100% !important;
  height: fit-content;
  background-color: #171616;
}

#footer {
  background-color: #222222;
}
.info {
  height: 550px;
  background-color: #222222;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  width: 100%;
}

.info h4 {
  font-family: "Roboto", sans-serif;
  font-weight: 400;
  font-size: 18px;
}
.socials-wrapper {
  display: flex;
  flex-direction: row;
  width: fit-content;
  vertical-align: middle;
  align-self: center;
  letter-spacing: 10px;
}

#logo-footer {
  width: auto;
  height: 120px;
}

.rights {
  align-self: center;
  font-weight: lighter;
  font-family: "Roboto", sans-serif;
}

.bi-facebook:hover {
  color: rgb(199, 199, 199);
}
.bi-twitter:hover {
  color: rgb(199, 199, 199);
}
.bi-instagram {
  color: rgb(199, 199, 199);
}
.bi-linkedin {
  color: rgb(199, 199, 199);
}

a,
a:hover,
a:focus,
a:active {
  text-decoration: none !important;
  color: white !important;
}

.cities {
  display: flex;
  flex-direction: column;
  text-decoration: none;
  row-gap: 10px;
}
.bi-caret-right {
  font-size: 10px;
}

.city {
  font-family: "Roboto", sans-serif;
  font-weight: 500;
  font-size: 14px;
}

.city:hover {
  color: silver;
}

.contact {
  display: flex;
  flex-direction: column;
  row-gap: 10px;
  color: white;
  font-family: "Roboto", sans-serif;
  font-weight: lighter;
  font-size: 14px;
}

#email-input {
  border: none;
  background-color: white;
  resize: none;
  outline: none;
  border-radius: 3px 3px;
  height: 36px;
  width: 300px;
}

#email-btn {
  width: 150px;
  height: 38px;
  color: white;
  background-color: #4a4a4a;
  border: none;
  border-radius: 3px 3px;
  font-size: 15px;
  font-weight: 600;
}
#newsletter {
  display: flex;
  flex-direction: row;
  row-gap: 10px;
  column-gap: 30px;
}

#newsletter-wrapper {
  display: flex;
  flex-direction: column;
}
#newsletter-notice {
  font-size: 12px;
  width: 300px;
  padding-top: 1%;
}
</style>