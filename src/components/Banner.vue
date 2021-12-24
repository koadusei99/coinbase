<template>
  <div class="banner">
    <div class="content">
      <div class="text">
        <h3>Earn up to $10 worth of crypto</h3>
        <p>
          Discover how specific cryptocurrencies work — and get a bit of each
          crypto to try out for yourself.
        </p>
        <button class="btn btn-primary">Start earning</button>
      </div>
      <div class="image"></div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.banner .content {
  display: flex;
  width: 100%;
  justify-content: space-between;
  padding-bottom: 50px;
  background-color: rgb(245, 248, 255);
}
.banner .text {
  max-width: 350px;
  margin-top: 130px;
  margin-left: 160px;
}
.banner .text h3 {
  line-height: 1.3;
  font-family: CoinbaseDisplay;
  font-size: 32px;
  font-weight: 500;
}
.banner .text p {
  font-size: 14px;
  line-height: 1.6;
  font-weight: 400;
  margin: 16px 0;
}
.banner .content .image {
  background-image: url("../assets/earn-upsell.jpg");
  background-position: right;
  background-size: cover;
  height: 411px;
  width: 700px;
}
.banner button {
  border-radius: 4px;
  color: white;
  cursor: pointer;
  padding: 12px 16px;
  font-size: 14px;
  border: 1px solid var(--primary);
  background-color: var(--primary);
}
@media screen and (max-width: 768px) {
  .banner .content {
    flex-direction: column;
    padding: 50px 0;
    background-color: rgb(17, 51, 85);
  }
  .banner .text {
    max-width: 290px;
    text-align: center;
    margin: 0 auto;
    color: white;
  }
  .banner .content .image {
    display: none;
  }
  .banner .text p {
    font-size: 16px;
  }
}
</style>
