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
  height: 245px;
  background-image: url("~@/assets/pattern-bg.png");
  background-size: cover;
  background-repeat: no-repeat;
  padding-top: 10px;

  h1 {
    color: #fff;
    text-align: center;
    font-size: 29px;
    font-weight: 500;
  }
}

.search__container {
  margin: 1rem 2rem;
}

.search__input {
  display: flex;
  justify-content: center;
  position: relative;
  max-width: 500px;
  margin: 1.5rem auto;
}

input {
  width: 100%;
  padding: 28px 0px 28px 21px;
  border: none;
  border-top-left-radius: 16px;
  border-bottom-left-radius: 16px;
  height: 30px;
}
input:focus {
  outline: none;
}

input::placeholder {
  font-size: 16px;
  color: #b0afaf;
}


.chevron {
  cursor: pointer;
  background: #000;
  color: #fff;
  padding: 20.5px;
  border-top-right-radius: 16px;
  border-bottom-right-radius: 16px;
  display: flex;
  align-items: center;
}
</style>
