<template>
  <div class="crypto-table" :style="{ borderRadius: `${border}px` }">
    <table class="table">
      <thead>
        <tr>
          <th v-if="minimal" class="number">#</th>
          <th>Name</th>
          <th>Price</th>
          <th>Change</th>
          <th class="hide"><span v-if="!minimal">Price</span> Chart</th>
          <th v-if="!minimal" class="hide">Volume(24h)</th>
          <th class="market-cap hide" v-if="!minimal">
            Market Cap <span><img src="../assets/sort.svg" alt="" /></span>
          </th>
          <th v-if="!minimal" class="hide">Supply</th>
          <th class="hide">Trade</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(coin, id) in data" :key="coin.id">
          <td v-if="minimal" class="number">{{ id + 1 }}</td>
          <td>
            <div class="coin-name">
              <div class="icon">
                <img :src="coin.image" alt="" />
              </div>
              <div class="txt">
                <p class="name">
                  {{ coin.name }}
                </p>
                <p class="sym">
                  {{ coin.symbol.toUpperCase() }}
                </p>
              </div>
            </div>
          </td>
          <td>{{ currency }} {{ formatPrice(coin.current_price) }}</td>
          <td :class="`${percentColor(coin.price_change_percentage_24h)}`">
            {{ formatPercent(coin.price_change_percentage_24h) }}
          </td>
          <td class="hide" @load="drawSparklines(coin.sparkline_in_7d.price)">
            <svg
              :class="`sparkline ${percentColor(
                coin.price_change_percentage_24h
              )}`"
              width="100"
              height="30"
              stroke-width="1"
            ></svg>
          </td>
          <td v-if="!minimal" class="hide">
            {{ currency }} {{ formatSuffix(coin.total_volume) }}
          </td>
          <td v-if="!minimal" class="hide">
            {{ currency }} {{ formatSuffix(coin.market_cap * exchangeRate) }}
          </td>
          <td v-if="!minimal" class="hide">
            {{ formatSuffix(coin.circulating_supply) }}
          </td>
          <td class="hide">
            <button class="trade-btn" v-if="!minimal">Trade</button>
            <button class="trade-btn2" v-if="minimal">Buy</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
const numeral = require("numeral");
import sparkline from "@fnando/sparkline";

export default {
  mounted() {
    this.drawSparklines();
  },
  name: "Table",
  props: { data: Array, minimal: Boolean, border: Number },
  data() {
    return { exchangeRate: 6.17, currency: "GHS" };
  },
  methods: {
    formatPrice(price) {
      return numeral(price * this.exchangeRate).format("0,0.0");
    },
    formatSuffix(price) {
      return numeral(price).format("0.0a").toUpperCase();
    },
    formatPercent(percent) {
      percent = percent.toFixed(2);
      return percent > 0 ? `+${percent}%` : `${percent}%`;
    },
    percentColor(percent) {
      return percent > 0 ? "green" : "red";
    },
    drawSparklines() {
      let sparklines = document.querySelectorAll(".sparkline");
      let numbers = [];

      sparklines.forEach((el) => {
        for (var i = 0; i < 30; i += 1) {
          numbers.push(Math.floor(Math.random() * 20));
        }
        sparkline(el, numbers);
        numbers = [];
      });
    },
  },
};
</script>

<style scoped>
.sparkline {
  stroke: rgb(141, 124, 124);
  fill: white;
}
.crypto-table {
  border: 1px solid rgba(91, 97, 110, 0.2);
  /* box-shadow: 0 4px 12px 0 rgba(50, 53, 61, 0.1); */
}
.table {
  width: 100%;
  padding: 0px;
  background: white;
  border-spacing: 0px;
  border-collapse: separate;
  caption-side: top;
}
.table head {
  border: none;
}
.table thead tr:first-child {
  border-top: 1px solid rgba(91, 97, 110, 0.2);
}

.table thead tr {
  border-bottom: 1px solid rgba(91, 97, 110, 0.2);
}
.table thead th {
  padding: 16px 20px;
  font-weight: 400;
  font-size: 12px;
  color: rgb(91, 97, 110);
}

.table td {
  padding: 14px 24px;
  font-size: 16px;
}
.coin-name {
  display: flex;
  gap: 16px;
  align-items: center;
}
.coin-name .txt {
  display: flex;
  gap: 16px;
}
.icon {
  width: 32px;
  height: 32px;
}
.icon img {
  border-radius: 100%;
}
.green {
  color: rgb(9 133 81);
  stroke: rgb(9 133 81);
}
.red {
  color: rgb(207 32 47);
  stroke: rgb(207 32 47);
}
.market-cap {
  display: flex;
  align-items: center;
  gap: 5px;
}
.market-cap img {
  width: 8px;
  height: 10px;
}
.trade-btn2 {
  background-color: rgb(9 133 81);
  border-radius: 4px;
  color: white;
  cursor: pointer;
  padding: 8px 16px;
  font-size: 14px;
  border: 1px solid rgb(9 133 81);
  height: fit-content;
  margin: auto;
}
.trade-btn {
  border-radius: 4px;
  color: white;
  cursor: pointer;
  padding: 8px 16px;
  font-size: 14px;
  border: 1px solid var(--primary);
  background-color: var(--primary);
  height: fit-content;
  margin: auto;
}

@media screen and (max-width: 768px) {
  .number {
    display: none;
  }
  .coin-name .txt {
    flex-direction: column;
  }
  .hide {
    display: none;
  }
}
</style>
