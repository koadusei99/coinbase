<template>
  <div class="footer">
    <div class="content">
      <div class="left">
        <div class="logo">
          <img src="../assets/logo.svg" alt="" />
        </div>
        <select name="languages" id="language">
          <option value="English">English</option>
          <option value="French">French</option>
        </select>

        <p class="copyright">© 2021 Coinbase</p>

        <ul class="socials">
          <li>Blog</li>
          <li>Twitter</li>
          <li>Facebook</li>
        </ul>
      </div>

      <div class="right">
        <div class="col">
          <div>
            <h4>Company</h4>
            <ul>
              <li>About</li>
              <li>Careers</li>
              <li>Affiliates</li>
              <li>Blog</li>
              <li>Press</li>
              <li>Investors</li>
              <li>Legal & privacy</li>
              <li>Cookie Policy</li>
              <li>Cookie Preferences</li>
            </ul>
          </div>

          <div>
            <h4>Learn</h4>
            <ul>
              <li>Browse crypto prices</li>
              <li>Coinbase Bytes newsletter</li>
              <li>Crypto basics</li>
              <li>Tips and tutorials</li>
              <li>Market Updates</li>
              <li>What is Bitcoin?</li>
              <li>What is Crypto?</li>
              <li>What is Blockchain?</li>
              <li>How to set up a Crypto wallet</li>
              <li>How to send taxes</li>
            </ul>
          </div>
        </div>
        <div class="col">
          <div>
            <h4>Individuals</h4>
            <ul>
              <li>Buy & sell</li>
              <li>Earn free crypto</li>
              <li>Wallet</li>
              <li>Card</li>
            </ul>
          </div>
          <div>
            <h4>Businesses</h4>
            <ul>
              <li>Prime</li>
              <li>Custody</li>
              <li>asset hub</li>
              <li>commerce</li>
            </ul>
          </div>
          <div>
            <h4>Developers</h4>
            <ul>
              <li>Coinbase cloud</li>
              <li>connect</li>
              <li>commerce</li>
              <li>pro</li>
              <li>bison trails</li>
              <li>walletLink</li>
              <li>Roseta</li>
              <li>USDC</li>
            </ul>
          </div>
        </div>

        <div class="col">
          <div>
            <h4>Support</h4>
            <ul>
              <li>help center</li>
              <li>contact us</li>
              <li>create account</li>
              <li>ID verification</li>
              <li>Account information</li>
              <li>payment methods</li>
              <li>Account access</li>
              <li>Supported crypto</li>
              <li>supported countries</li>
              <li>status</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
.footer {
  padding-top: 100px;
}
.footer .content {
  display: flex;
  max-width: 1180px;
  padding: 24px;
  margin: 0 auto;
  font-size: 16px;
  line-height: 1.3;
  /* opacity: 0.7; */
  color: rgb(17, 51, 85);
}
.logo {
  margin-bottom: 32px;
}
.logo img {
  width: 112px;
}
.content .left {
  width: 377px;
}
.content .left select {
  padding: 4px;
  border-radius: 4px;
  background-color: white;
  border: 1px solid rgb(238, 240, 243);
  width: 212px;
  font-size: 1rem;
  font-family: CoinbaseSans;
  margin-bottom: 20px;
}
.content .right {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
}
.content .right .col {
  padding: 0 4px;
  display: flex;
  flex-direction: column;
  gap: 30px;
}
ul,
ol {
  list-style: none;
}
li,
p {
  opacity: 0.7;
}
.right ul {
  display: flex;
  flex-direction: column;
  gap: 8px;
}
.content .right h4 {
  margin-bottom: 12px;
  font-size: 16px;
  font-weight: 500;
  opacity: 1;
}
.socials {
  margin-top: 10px;
  display: flex;
  align-items: center;
}
.socials li::before {
  content: "•";
}
.socials li:first-of-type::before {
  content: "";
}
@media screen and (max-width: 768px) {
  .footer .content {
    flex-direction: column;
    gap: 50px;
  }
  .content .right {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 30px;
  }
}
</style>
