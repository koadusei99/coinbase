<template>
  <div class="home">
    <Hero />
    <div class="table" v-if="fetched"><Table minimal :data="crypto" /></div>
    <div class="stellar">
      <div class="left">
        <h2>Earn up to $10 worth of crypto</h2>
        <p>
          Discover how specific cryptocurrencies work — and get a bit of each
          crypto to try out for yourself.
        </p>
        <button class="btn btn-primary">Start earning</button>
      </div>
      <div class="right">
        <div class="card">
          <div class="top">
            <div>
              <img src="../assets/stellar.svg" alt="" />
              <p class="fold">Stellar <span>Lumens</span></p>
              <p class="hide">XLM</p>
            </div>
            <p class="earn">Earn $10 XLM</p>
          </div>
          <div class="bottom">
            <p>View more ></p>
          </div>
        </div>
      </div>
    </div>
    <section class="portfolio">
      <div class="headers">
        <h2>Create your cryptocurrency portfolio today</h2>
        <p>
          Coinbase has a variety of features that make it the best place to
          start trading
        </p>
      </div>
      <div class="disp">
        <div class="txt">
          <div class="di">
            <div class="icon">
              <svg width="30" height="32" viewBox="0 0 30 32">
                <g fill="none" fill-rule="evenodd">
                  <path fill="#D4EEFF" d="M10 32h10V10H10z"></path>
                  <path fill="#1752F0" d="M20 32h10V0H20z"></path>
                  <path fill="#55B4FC" d="M0 32h10V19H0z"></path>
                </g>
              </svg>
            </div>
            <div class="text">
              <h3>Manage your portfolio</h3>
              <p>
                Buy and sell popular digital currencies, keep track of them in
                the one place.
              </p>
            </div>
          </div>
          <div class="di">
            <div class="icon">
              <svg width="36" height="38" viewBox="0 0 36 38">
                <g fill="none" fill-rule="evenodd">
                  <path
                    d="M17.813 9.5a2.375 2.375 0 002.375-2.375v-4.75a2.375 2.375 0 00-4.75 0v4.75A2.375 2.375 0 0017.811 9.5M29.688 9.5a2.375 2.375 0 002.375-2.375v-4.75a2.375 2.375 0 00-4.75 0v4.75A2.375 2.375 0 0029.688 9.5"
                    fill="#D4EEFF"
                  ></path>
                  <path fill="#D4EEFF" d="M0 38h35.625V4.75H0z"></path>
                  <path fill="#55B4FC" d="M0 11.875h35.625V4.75H0z"></path>
                  <path
                    d="M5.938 9.5a2.375 2.375 0 002.375-2.375v-4.75a2.375 2.375 0 00-4.75 0v4.75A2.375 2.375 0 005.937 9.5"
                    fill="#D4EEFF"
                  ></path>
                  <path
                    d="M27.313 4.75v2.375a2.375 2.375 0 004.75 0V4.75h-4.75zM5.938 9.5a2.375 2.375 0 002.375-2.375V4.75h-4.75v2.375A2.375 2.375 0 005.937 9.5"
                    fill="#1752F0"
                  ></path>
                  <path
                    d="M17.813 9.5a2.375 2.375 0 002.375-2.375v-4.75a2.375 2.375 0 00-4.75 0v4.75A2.375 2.375 0 0017.811 9.5"
                    fill="#D4EEFF"
                  ></path>
                  <path
                    d="M17.813 9.5a2.375 2.375 0 002.375-2.375V4.75h-4.75v2.375A2.375 2.375 0 0017.811 9.5"
                    fill="#1752F0"
                  ></path>
                  <path fill="#FFF" d="M4.75 34.438h26.125V11.875H4.75z"></path>
                  <path
                    fill="#1752F0"
                    d="M12.69 26.329l3.359 3.359L26.125 19.61l-3.358-3.359z"
                  ></path>
                  <path
                    fill="#1752F0"
                    d="M16.049 29.688l3.359-3.36-6.244-6.243-3.359 3.36z"
                  ></path>
                </g>
              </svg>
            </div>
            <div class="text">
              <h3>Recurring buys</h3>
              <p>
                Invest in cryptocurrency slowly over time by scheduling buys
                daily, weekly, or monthly.
              </p>
            </div>
          </div>
          <div class="di">
            <div class="icon">
              <svg width="36" height="36" viewBox="0 0 36 36" fill="none">
                <path d="M36 2.25H0v31.5h36V2.25z" fill="#D4EEFF"></path>
                <path
                  d="M28.125 36H7.875a1.128 1.128 0 01-1.125-1.125V1.125C6.75.506 7.256 0 7.875 0h20.25c.618 0 1.125.506 1.125 1.125v33.75c0 .619-.507 1.125-1.125 1.125z"
                  fill="#56B4FC"
                ></path>
                <path
                  d="M29.25 2.25H6.75v31.5h22.5V2.25z"
                  fill="#1652F0"
                ></path>
                <path
                  d="M23 15.137L21.889 14l-6.667 6.822 1.11 1.137L23 15.137z"
                  fill="#fff"
                ></path>
                <path
                  d="M16.334 22l1.11-1.137-3.333-3.411-1.11 1.137L16.333 22z"
                  fill="#fff"
                ></path>
                <path
                  d="M23.625 3.375h-11.25a1.128 1.128 0 01-1.124-1.125V1.125h13.5V2.25c0 .619-.507 1.125-1.126 1.125z"
                  fill="#56B4FC"
                ></path>
                <path
                  d="M15.75 32.063c0 .337.226.562.563.562h3.375c.338 0 .563-.225.563-.562 0-.338-.226-.563-.563-.563h-3.375c-.337 0-.562.225-.562.563z"
                  fill="#fff"
                ></path>
              </svg>
            </div>
            <div class="text">
              <h3>Mobile apps</h3>
              <p>
                Stay on top of the markets with the Coinbase app for
                <a href="as">Android</a> or <a href="ds">iOS</a>.
              </p>
            </div>
          </div>
        </div>
        <div class="image">
          <img src="../assets/portfolio.jpg" alt="" />
        </div>
      </div>
    </section>
    <div class="divider"></div>
    <section class="trusted">
      <div class="headers">
        <h2>The most trusted cryptocurrency platform</h2>
        <p>Here are a few reasons why you should choose Coinbase</p>
      </div>
      <div class="features">
        <div class="feature">
          <div class="icon">
            <svg width="64" height="64" viewBox="0 0 64 64" fill="none">
              <path d="M56 0H8v50h48V0z" fill="#BFE9FF"></path>
              <path d="M64 10H0v48h64V10z" fill="#56B4FC"></path>
              <path d="M56 10H8v40h48V10z" fill="#1652F0"></path>
              <path d="M10 16H6v8h4v-8zM10 36H6v8h4v-8z" fill="#1652F0"></path>
              <path d="M64 58h-8v6h8v-6zM8 58H0v6h8v-6z" fill="#56B4FC"></path>
              <path
                d="M41.19 20.81c-5.07-5.07-13.32-5.07-18.38 0-5.06 5.07-5.07 13.32 0 18.38 2.53 2.53 5.86 3.8 9.19 3.8 3.33 0 6.66-1.27 9.19-3.8 5.07-5.07 5.07-13.31 0-18.38zM32 19c2.5 0 5 .85 7.04 2.55l-2.85 2.85A6.99 6.99 0 0032 23c-1.53 0-2.98.5-4.19 1.4l-2.85-2.85A11.03 11.03 0 0132 19zm3.54 14.54c-.95.94-2.2 1.46-3.54 1.46-1.34 0-2.59-.52-3.54-1.46A4.952 4.952 0 0127 30c0-1.33.52-2.59 1.46-3.54.94-.95 2.2-1.46 3.54-1.46 1.34 0 2.59.52 3.54 1.46.95.94 1.46 2.21 1.46 3.54s-.52 2.59-1.46 3.54zM23.55 22.96l2.85 2.85A6.99 6.99 0 0025 30c0 1.53.5 2.98 1.4 4.19l-2.85 2.85a11.018 11.018 0 010-14.08zm1.41 15.49l2.85-2.85a6.969 6.969 0 008.38 0l2.85 2.85a11.018 11.018 0 01-14.08 0zm15.49-1.41l-2.85-2.85c.9-1.2 1.4-2.65 1.4-4.19 0-1.53-.5-2.98-1.4-4.19l2.85-2.85a11.018 11.018 0 010 14.08z"
                fill="#fff"
              ></path>
            </svg>
          </div>
          <div class="txt">
            <h3>Secure storage</h3>
            <p>
              We store the vast majority of the digital assets in secure offline
              storage.
            </p>
            <a href=""
              >Learn how Coinbase keeps your funds safe and secure
              <span>></span></a
            >
          </div>
        </div>
        <div class="feature">
          <div class="icon">
            <svg width="64" height="64" viewBox="0 0 64 64" fill="none">
              <path
                d="M56 56h-8v8h8c4.42 0 8-3.58 8-8h-8z"
                fill="#BFE9FF"
              ></path>
              <path
                d="M48 56V0H0v56c0 4.42 3.58 8 8 8h48c-4.42 0-8-3.58-8-8z"
                fill="#56B4FC"
              ></path>
              <path
                d="M48 56H0c0 4.42 3.58 8 8 8h48c-4.42 0-8-3.58-8-8z"
                fill="#1652F0"
              ></path>
              <path
                d="M40 30H8v2h32v-2zM40 36H8v2h32v-2zM40 42H8v2h32v-2zM32 48H16v2h16v-2zM23.5 24.66l-3.24-5.92-5.92-3.24 5.92-3.24 3.24-5.92 3.24 5.92 5.92 3.24-5.92 3.24-3.24 5.92zm-4.99-9.16l3.22 1.76 1.76 3.22 1.76-3.22 3.22-1.76-3.22-1.76-1.76-3.22-1.76 3.22-3.22 1.76z"
                fill="#fff"
              ></path>
            </svg>
          </div>
          <div class="txt">
            <h3>Protected by insurance</h3>
            <p>
              Coinbase maintains crypto insurance and all USD cash balances are
              covered by FDIC insurance, up to a maximum of $250,000.
            </p>
            <a href=""
              >Learn how your crypto is covered by our insurance policy
              <span>></span></a
            >
          </div>
        </div>
        <div class="feature">
          <div class="icon">
            <svg width="56" height="64" viewBox="0 0 56 64" fill="none">
              <path d="M56 0H24v64h32V0z" fill="#BFE9FF"></path>
              <path
                d="M0 8v28c0 13.25 24 24 24 24s24-10.75 24-24V8H0z"
                fill="#56B4FC"
              ></path>
              <path d="M24 8v52s24-10.75 24-24V8H24z" fill="#1652F0"></path>
              <path
                d="M7 15v21c0 4.92 8.57 11.72 16.53 15.97l.47.25.47-.25C32.43 47.72 41 40.92 41 36V15H7zm32 2v6H9v-6h30zM24 49.95C15.55 45.35 9 39.28 9 36V25h30v11c0 3.28-6.55 9.35-15 13.95z"
                fill="#fff"
              ></path>
            </svg>
          </div>
          <div class="txt">
            <h3>Industry best practices</h3>
            <p>
              Coinbase supports a variety of the most popular digital
              currencies.
            </p>
            <a href=""
              >Learn how we implement industry best practices for account
              security <span>></span></a
            >
          </div>
        </div>
      </div>
    </section>
    <div class="stats">
      <div class="content">
        <div>
          <p>$327B</p>
          <p>Quarterly volume traded</p>
        </div>
        <div>
          <p>$100+</p>
          <p>Countries supported</p>
        </div>
        <div>
          <p>$73+M</p>
          <p>Verified users</p>
        </div>
      </div>
    </div>
    <section class="started">
      <div class="headers">
        <h2>Get started in a few minutes</h2>
        <p>
          Coinbase supports a variety of the most popular digital currencies.
        </p>
      </div>
      <div class="content">
        <div>
          <div class="icon">
            <svg width="64" height="60" viewBox="0 0 64 60" fill="none">
              <path
                d="M32 16a8 8 0 100-16 8 8 0 000 16zM32 20c-11.05 0-20 7.16-20 16v18h40V36c0-8.84-8.95-16-20-16z"
                fill="#56B4FC"
              ></path>
              <path d="M64 36H0v24h64V36z" fill="#BFE9FF"></path>
              <path d="M52 36H12v24h40V36z" fill="#1652F0"></path>
              <path d="M33 42h-2v12h2V42z" fill="#fff"></path>
              <path d="M38 49v-2H26v2h12z" fill="#fff"></path>
            </svg>
          </div>
          <p>Create an account</p>
        </div>
        <div class="line"></div>
        <div>
          <div class="icon">
            <svg width="65" height="56" viewBox="0 0 65 56" fill="none">
              <path d="M57.03 20h-50v24h50V20z" fill="#BFE9FF"></path>
              <path
                d="M60.03 52v-4h-8V16.06L64 16.1l.01-4.1L32.06 0 .01 12 0 15.9l12.03.04V48h-8v4h-4v4h64v-4h-4zm-16-4h-8V16.01l8 .03V48zm-24-32.04l8 .03V48h-8V15.96z"
                fill="#56B4FC"
              ></path>
              <path d="M52.03 20h-40v24h40V20z" fill="#1652F0"></path>
              <path
                d="M36.41 34.38c0-2.34-1.42-3.12-4.17-3.5-2.03-.29-2.42-.77-2.42-1.72 0-.9.69-1.54 2.01-1.54 1.34 0 2.04.52 2.26 1.75h1.99c-.19-1.86-1.26-2.96-3.06-3.28V24h-2v2.05c-1.98.28-3.26 1.6-3.26 3.29 0 2.19 1.32 3.04 4.12 3.42 1.9.31 2.44.72 2.44 1.8s-.92 1.8-2.21 1.8c-1.98 0-2.45-.98-2.6-2.16h-2.09c.14 1.94 1.2 3.4 3.61 3.72V40h2v-2.08c2.06-.33 3.38-1.77 3.38-3.54z"
                fill="#fff"
              ></path>
            </svg>
          </div>
          <p>Link your bank account</p>
        </div>
        <div class="line"></div>

        <div>
          <div class="icon">
            <svg width="64" height="60" viewBox="0 0 64 60" fill="none">
              <path
                d="M32 16a8 8 0 100-16 8 8 0 000 16zM32 20c-11.05 0-20 7.16-20 16v18h40V36c0-8.84-8.95-16-20-16z"
                fill="#56B4FC"
              ></path>
              <path d="M64 36H0v24h64V36z" fill="#BFE9FF"></path>
              <path d="M52 36H12v24h40V36z" fill="#1652F0"></path>
              <path d="M33 42h-2v12h2V42z" fill="#fff"></path>
              <path d="M38 49v-2H26v2h12z" fill="#fff"></path>
            </svg>
          </div>
          <p>Start buying & selling</p>
        </div>
      </div>
    </section>
    <Banner />
    <Footer />
  </div>
</template>

<script>
import Banner from "../components/Banner.vue";
import Footer from "../components/Footer.vue";
import Hero from "../components/Hero.vue";
import Table from "../components/Table.vue";
const axios = require("axios").default;

export default {
  async created() {
    this.getCrypto();
  },
  name: "Home",
  data() {
    return { crypto: [], fetched: false };
  },
  components: {
    Table,
    Hero,
    Banner,
    Footer,
  },
  methods: {
    async getCrypto() {
      try {
        const response = await axios.get(
          "https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=4&page=1&sparkline=false"
        );
        console.log(response);
        this.crypto = response.data;
        this.fetched = true;
      } catch (error) {
        console.error(error);
      }
    },
  },
};
</script>
<style scoped>
.table {
  margin-top: 50px;
  max-width: 1142px;
  margin-inline: auto;
}
.divider {
  width: 100%;
  height: 1px;
  background-color: rgb(238, 240, 243);
}
.stellar {
  max-width: 1142px;
  margin: 24px auto;
  display: flex;
  justify-content: space-between;
}
.left {
  display: flex;
  flex-direction: column;
  max-width: 350px;
  justify-content: center;
  z-index: 1;
  min-width: 250px;
  gap: 16px;
}
.left h2 {
  line-height: 1.3;
  color: rgb(var(--gray100));
  font-size: 32px;
  font-weight: 500;
  font-family: CoinbaseDisplay;
}
.left p {
  font-size: 14px;
  line-height: 1.6;
  color: rgb(var(--gray100));
}
.left .btn {
  width: fit-content;
  padding: 12px 16px;
  font-size: 14px;
}
.right {
  width: 566px;
}
.right .top {
  display: flex;
  justify-content: space-between;
  line-height: 1.3;
  color: rgb(var(--gray100));
  font-size: 22px;
  font-weight: 500;
  align-items: center;
}
.right .top .earn {
  font-size: 16px;
  color: var(--positive);
  font-weight: 500;
}
.right .top > div {
  display: flex;
  gap: 16px;
  align-items: center;
}
.right img {
  width: 38px;
}
.card .top {
  background: white;
  border-radius: 8px;
  box-shadow: rgba(0, 0, 0, 0.08) 0px 0px 0px;
  transition: box-shadow 500ms ease 0s, opacity 500ms ease 0s,
    z-index 0ms ease-out 500ms;
  cursor: pointer;
  opacity: 0.9;
  margin-bottom: 0px;
  margin-top: -1px;
  display: flex;
  width: 100%;
  padding: 24px;
  white-space: nowrap;
  border: medium none;
}
.card .top:hover {
  box-shadow: rgba(0, 0, 0, 0.12) 0px 8px 24px;
  opacity: 1;
  z-index: 1;
}
.card .bottom > p {
  color: var(--primary);
  display: block;
  margin: 16px 0 0 24px;
  font-weight: 500;
}
.headers {
  text-align: center;
}
.headers h2 {
  font-size: 40px;
  font-weight: 500;
  margin-bottom: 8px;
  font-family: CoinbaseDisplay;
}
.headers p {
  color: rgb(var(--gray60));
  margin: 14px 0;
}
.portfolio {
  max-width: 1180px;
  margin: 70px auto 0;
  padding: 24px;
  padding-bottom: 64px;
}
.portfolio .disp {
  margin-top: 80px;
  display: flex;
  align-items: center;
}
.portfolio .disp .txt {
  display: flex;
  flex-direction: column;
  gap: 40px;
}

.portfolio .disp .image img {
  width: 700px;
}
.portfolio .disp .di {
  display: flex;
  align-items: flex-start;
  gap: 32px;
}
.portfolio .di .text h3 {
  font-size: 20px;
  font-weight: 500;
}
.portfolio .di .text p {
  line-height: 1.6;
  color: rgb(91, 97, 110);
}
.portfolio .di .text a {
  color: var(--primary);
  text-decoration: none;
}

.portfolio .disp .di .icon {
  width: 72px;
  height: 72px;
  border-radius: 100%;
  flex: 0 0 auto;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: rgba(218, 225, 233, 0.557) 0px 8px 16px;
}
.trusted {
  padding: 100px 24px;
  max-width: 1180px;
  margin: 0 auto;
}
.trusted .features {
  max-width: 1084px;
  margin-top: 100px;
  display: flex;
  width: 100%;
  margin-inline: auto;
  justify-content: space-between;
  padding-inline: 24px;
}

.trusted .feature {
  max-width: 350px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  gap: 24px;
}

.trusted .feature h3 {
  font-size: 20px;
  font-weight: 500;
}
.trusted .feature p {
  color: rgb(var(--gray60));
  line-height: 24px;
  font-size: 16px;
  max-width: 305px;
  height: 110px;
}
.trusted .feature a {
  display: block;
  cursor: pointer;
  font-size: 14px;
  font-weight: 500;
  text-decoration: none;
  line-height: 28px;
  color: var(--primary);
  margin-top: 50px;
  max-width: 305px;
}
.trusted .feature a span {
  font-size: 10px;
}
.stats {
  background-color: var(--primary);
  margin-top: 40px;
}
.stats .content {
  max-width: 1180px;
  padding: 24px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 66px 24px;
  text-align: center;
}
.stats .content p:first-of-type {
  margin-bottom: 16px;
  line-height: 48px;
  font-size: 56px;
  font-weight: 500;
  color: white;
  font-family: CoinbaseDisplay;
}
.stats .content p:last-of-type {
  line-height: 24px;
  font-size: 16px;
  opacity: 0.7;
  color: white;
}
.stats .content > div {
  width: 377px;
}
.started {
  padding: 100px 0;
}
.started .content {
  max-width: 905px;
  margin: 0 auto;
  padding: 24px;
  display: flex;
  align-items: center;
}

.started .content > div {
  text-align: center;
}
.started .content p {
  margin-top: 32px;
  margin-bottom: 16px;
  font-size: 20px;
  color: var(--gray100);
  font-weight: 500;
}
.started .content .line {
  flex: 1 1 0%;
  height: 1px;
  margin-top: -60px;
  background-color: rgba(91, 97, 110, 0.66);
}
@media screen and (max-width: 768px) {
  .stellar {
    flex-direction: column;
    padding: 24px;
  }
  .stellar .left {
    text-align: center;
    align-items: center;
    justify-content: center;
    max-width: 250px;
    margin: 0 auto;
  }
  .stellar .left,
  .stellar .right {
    width: 100%;
  }
  .stellar .right .card .top {
    border: 1px solid rgba(91, 97, 110, 0.2);
    border-radius: 0;
    margin-top: 30px;
  }
  .portfolio .disp {
    flex-direction: column-reverse;
  }
  .portfolio .disp .image {
    max-width: 100%;
  }
  .portfolio .disp .image img {
    max-width: 100%;
  }
  .trusted .features {
    flex-direction: column;
    justify-content: center;
    max-width: fit-content;
    gap: 30px;
  }

  .trusted .feature p {
    height: fit-content;
  }
  .trusted .feature a {
    margin-top: 10px;
  }
  .started .content {
    flex-direction: column;
    gap: 50px;
  }
  .stats .content {
    flex-direction: column;
    gap: 60px;
  }
  .fold {
    display: flex;
    flex-direction: column;
  }
  .hide {
    display: none;
  }
}
</style>
