<template>
  <div class="prices">
    <div class="search">
      <div class="left">
        <p>In the past 24 hours</p>
        <p>Market is down <span>1.25%</span></p>
      </div>
      <div class="right">
        <div class="bar">
          <div class="ico">
            <svg
              fill="none"
              height="20"
              viewBox="0 0 26 26"
              width="20"
              aria-hidden="true"
            >
              <g stroke="#7d95b6" stroke-miterlimit="10" stroke-width="2">
                <path d="M25 25l-7.034-7.035"></path>
                <path
                  d="M10.931 20.862c5.485 0 9.931-4.446 9.931-9.931C20.862 5.446 16.416 1 10.931 1 5.446 1 1 5.446 1 10.931c0 5.485 4.446 9.931 9.931 9.931z"
                  stroke-linecap="square"
                ></path>
              </g>
            </svg>
          </div>
          <input type="text" placeholder="Search" />
        </div>
      </div>
    </div>
    <ul class="market">
      <li>
        <h3>Top Gainer</h3>
        <div class="ico"><img src="../assets/gainer.png" alt="" /></div>
        <div class="txt">
          <h3>Top Gainer</h3>
          <p class="name">Near Protocol</p>
          <p><span>+28.38%</span> price change</p>
        </div>
      </li>
      <li>
        <h3>New Listing</h3>
        <div class="ico"><img src="../assets/listing.png" alt="" /></div>
        <div class="txt">
          <h3>New Listing</h3>
          <p class="name">Decentralized Social</p>
          <p>Added <span>Dec 13</span></p>
        </div>
      </li>
      <li>
        <h3>Most Visited</h3>
        <div class="ico"><img src="../assets/visited.png" alt="" /></div>
        <div class="txt">
          <h3>Most Visited</h3>
          <p class="name">GitCoin</p>
          <p><span>+3,625.32%</span> views</p>
        </div>
      </li>
      <li>
        <h3>Most Traded</h3>
        <div class="ico"><img src="../assets/bitcoin.png" alt="" /></div>
        <div class="txt">
          <h3>Most Traded</h3>
          <p class="name">BitCoin</p>
          <p><span>GHS 146B</span> volume(24h)</p>
        </div>
      </li>
      <li>
        <h3>Free Crypto</h3>
        <div class="ico"><img src="../assets/stellar.png" alt="" /></div>
        <div class="txt">
          <h3>Free Crypto</h3>
          <p class="name">Stellar Lumens</p>
          <p><span>Earn $10</span></p>
        </div>
      </li>
    </ul>
    <div class="table">
      <div class="filters">
        <ul>
          <li>All Assets</li>
          <li>Tradable</li>
          <li>Gainers</li>
          <li>Losers</li>
        </ul>
        <ul>
          <li>1H</li>
          <li>1D</li>
          <li>1W</li>
          <li>1M</li>
          <li>1Y</li>
        </ul>
      </div>
      <Table v-if="fetched" :data="data" :border="12" />
      <div class="pagination">
        <ul class="pages">
          <li @click="paginate(1)">1</li>
          <li @click="paginate(2)">2</li>
          <li @click="paginate(3)">3</li>
          <li>...</li>
          <li>287</li>
          <li @click="nextPage">
            <svg width="16" height="16" viewBox="0 0 16 16" fill="none">
              <path
                d="M4.61 3.05L9.56 8l-4.95 4.95 1.42 1.41L12.39 8 6.03 1.64 4.61 3.05z"
                fill="#6F8598"
              ></path>
            </svg>
          </li>
        </ul>
        <p>1-30 of 3855 assets</p>
      </div>
    </div>
    <Banner />
    <Footer />
  </div>
</template>

<script>
import Banner from "../components/Banner.vue";
import Footer from "../components/Footer.vue";
import Table from "../components/Table.vue";
const axios = require("axios").default;

export default {
  async created() {
    this.getCrypto();
  },
  components: { Table, Banner, Footer },
  data() {
    return { crypto: [], data: [], fetched: false, page: 1 };
  },
  methods: {
    async getCrypto() {
      try {
        const response = await axios.get(
          "https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=100&page=1&sparkline=true"
        );
        this.crypto = response.data;
        this.fetched = true;
        this.data = response.data.slice(0, 30);
      } catch (error) {
        console.error(error);
      }
    },
    paginate(page) {
      this.data = this.crypto.slice(30 * (page - 1), 30 * page);
      this.page = page;
    },
    nextPage() {
      this.data = this.crypto.slice(30 * (this.page - 1), 30 * (this.page + 1));
      this.page++;
    },
  },
};
</script>

<style scoped>
.table {
  max-width: 1180px;
  padding: 0 24px;
  margin: 0 auto;
}
.search {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  max-width: 1180px;
  padding: 0 24px;
  margin: 0 auto;
}
.search .bar {
  display: flex;
  box-shadow: rgba(50, 53, 61, 0.02) 0px 4px 12px 0px;
  height: 48px;
  padding: 0px 16px;
  border: 1px solid var(--line);
  align-items: center;
  border-radius: 4px;
}
.search .bar .ico {
  display: grid;
  place-items: center;
  margin-right: 16px;
}
.search .bar input {
  border: none;
  width: 100%;
  height: 100%;
  font-size: 16px;
  font-family: CoinbaseSans;
}
.search .left p:first-of-type {
  font-size: 14px;
  font-weight: 500;
  color: rgb(91, 97, 110);
}
.search .left p:last-of-type {
  font-size: 24px;
  font-weight: 500;
}
.search .left p:last-of-type span {
  color: rgb(207, 32, 47);
  font-size: 24px;
  font-weight: 500;
  margin-left: 6px;
}
.market {
  max-width: 1180px;
  padding: 0 24px;
  margin: 16px auto 40px;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(198px, 1fr));
  list-style: none;
  overflow: hidden;
  gap: 15px;
}
.market li {
  border-radius: 12px;
  border: 1px solid var(--line);
  padding: 0px 16px 20px;
}
.market li h3 {
  font-size: 14px;
  font-weight: 500;
  padding: 20px 0px 16px;
}
.market li .name {
  margin-bottom: 5px;
  color: rgb(91, 97, 110);
  font-size: 16px;
  font-weight: 500;
  line-height: 22px;
  color: var(--text);
}
.market li p:last-of-type span {
  color: var(--primary);
}
.market li p:last-of-type {
  line-height: 22px;
  color: rgb(91, 97, 110);
}
.market li .ico img {
  width: 40px;
  margin-bottom: 10px;
}
.market .txt h3 {
  display: none;
}
.filters {
  display: flex;
  justify-content: space-between;
  margin-bottom: 10px;
}
.filters > ul {
  display: flex;
  list-style: none;
}
.filters li {
  padding: 6px 24px;
  border-radius: 100px;
  cursor: pointer;
  font-size: 14px;
  font-weight: 500;
}
.filters ul:first-of-type li:first-of-type {
  color: rgb(0, 82, 255);
  background-color: rgb(241, 245, 254);
}
.filters ul:last-of-type li:nth-of-type(2) {
  color: rgb(0, 82, 255);
}
.filters ul:last-of-type li {
  color: rgb(88, 112, 136);
}
.pagination {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 20px;
}
.pagination ul {
  display: flex;
  gap: 5px;
  list-style: none;
  margin: 10px auto;
}
.pagination li {
  width: 32px;
  height: 32px;
  border-radius: 16px;
  display: grid;
  place-items: center;
}
.pagination li:hover {
  border: 1px solid var(--line);
}
.pagination p {
  line-height: 1.5;
  font-size: 12px;
  color: rgb(var(--gray60));
}
@media screen and (max-width: 768px) {
  .market {
    margin: 0 24px;
    border: 1px solid var(--line);
    border-radius: 12px;
    padding: 24px;
    margin-bottom: 50px;
  }
  .market .txt h3 {
    display: block;
    font-size: 16px;
    margin-bottom: 0px;
    line-height: 24px;
    font-weight: 400;
  }
  .market li > h3 {
    display: none;
  }
  .market li {
    width: 100%;
    padding: 0;
    border: none;
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 20px;
    padding: 0 10px;
  }
  .market li h3 {
    padding: 0;
  }

  .market li .ico img {
    width: 32px;
    height: 32px;
    margin-bottom: 0;
    border-radius: 100%;
  }
  .market li .name {
    font-size: 13px;
    line-height: 16px;
    font-weight: 400;
    color: rgb(91, 97, 110);
  }
  .market .txt {
    color: rgb(91, 97, 110);
    font-size: 13px;
    line-height: 16px;
  }
  .market .txt p {
    display: inline;
    margin-right: 5px;
  }
  .filters ul:last-of-type {
    display: none;
  }
  .filters li {
    font-size: 13px;
    padding: 8px 12px;
  }
}
</style>
