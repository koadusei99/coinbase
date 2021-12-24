<template>
  <div id="app">
    <Navbar />
    <router-view class="app-main" />
  </div>
</template>
<script>
import Navbar from "@/components/Navbar.vue";
export default {
  name: "App",
  components: {
    Navbar,
  },
};
</script>
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.btn {
  border: none;
  padding: 10px 12px;
  font-family: CoinbaseSans;
  font-weight: 500;
  font-size: 16px;
  border-radius: var(--btn-radius);
  cursor: pointer;
}
.btn-primary {
  border: 1px solid rgb(0, 82, 255);
  background-color: var(--primary);
  padding: 10px 12px;
  color: white;
}
.btn-secondary {
  border: 2px solid var(--primary);
  color: var(--primary);
  background-color: white;
}
.list {
  list-style: none;
}
.app-main {
  padding: 100px 0 0;
  width: 100%;
}
</style>
