<template>
  <div class="header">
    <div class="header__search">
      <div class="search__container">
        <h1>IP Address Tracker</h1>
        <div class="search__input">
          <input type="text">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {},
};
</script>

<style lang="scss">
.header {
  display: flex;
  flex-direction: column;
  height: 25vh;
  max-height: 25vh;
  background-image: url('~@/assets/pattern-bg.png');
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
  h1 {
    color: #fff;
    text-align: center;
    font-size: 32px;
    padding-bottom: 4px;
    font-weight: 200;
  }


</style>
