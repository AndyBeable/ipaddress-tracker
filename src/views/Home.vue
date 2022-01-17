<template>
  <div class="header">
    <div class="header__search">
      <div class="search__container">
        <h1>IP Address Tracker</h1>
        <div class="search__input">
          <input type="text" placeholder="Search for any IP address or leave empty to get your ip info"/>
          <i class="fas fa-chevron-right chevron"></i>
        </div>
        <IPInfo />
      </div>
    </div>
  </div>
</template>

<script>
import IPInfo from "@/components/IPInfo";

export default {
  name: "Home",
  components: { IPInfo },
};
</script>

<style lang="scss">
.header {
  display: flex;
  flex-direction: column;
  height: 30vh;
  max-height: 30vh;
  background-image: url("~@/assets/pattern-bg.png");
  background-size: cover;
  padding-top: 10px;
}

.search__container {
  width: 500px;
  margin: 0 auto;
}

.search__input {
  display: flex;
  justify-content: center;
  position: relative;
}

input {
  width: 100%;
  padding: 3px 2px;
  border: none;
  border-top-left-radius: 5px;
  border-bottom-left-radius: 5px;
  height: 30px;
}
input:focus {
  outline: none;
}

input::placeholder {
  padding-left: 5px;
  font-size: 16px;
  color: #b0afaf;
}
h1 {
  color: #fff;
  text-align: center;
  font-size: 28px;
  padding-bottom: 10px;
  font-weight: 200;
}

.chevron {
  cursor: pointer;
  background: #000;
  color: #fff;
  padding-left: 4px;
  padding-right: 4px;
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
  display: flex;
  align-items: center;
}
</style>
