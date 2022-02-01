<template>
  <div class="results">
    <div class="stat">
      <h3>IP Address</h3>
      <span>{{ ipInfo.address }}</span>
    </div>
    <div class="stat">
      <h3>Location</h3>
      <span>{{ ipInfo.state }}</span>
    </div>
    <div class="stat">
      <h3>Timezone</h3>
      <span>UTC {{ ipInfo.timezone }}</span>
    </div>
    <div class="stat">
      <h3>ISP</h3>
      <span>{{ ipInfo.isp }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "IPInfo",
  props: ["ipInfo"],
};
</script>

<style lang="scss" scoped>
.results {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #fff;
  gap: 5px;
  padding: 8px 8px 12px 8px;
  border-radius: 16px;
  z-index: 2;
}

.stat {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1rem 0.5rem 0rem 0.5rem;

  h3 {
    text-transform: uppercase;
    color: #969696;
    font-weight: 500;
    font-size: 12px;
    margin-bottom: 0.5rem;
  }
  span {
    font-weight: 500;
    font-size: 23px;
    margin-bottom: 0.5rem;
  }
}
</style>
