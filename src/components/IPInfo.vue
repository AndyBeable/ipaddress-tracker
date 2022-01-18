<template>
<div class="results">
  <div class="stat">
    <h3>IP Address</h3>
    <span>8.8.8.8</span>
  </div>
  <div class="stat">
    <h3>Location</h3>
    <span>London</span>
  </div>
  <div class="stat">
    <h3>Timezone</h3>
    <span>UTC 07:00</span>
  </div>
  <div class="stat">
    <h3>ISP</h3>
    <span>Google</span>
  </div>
</div>
</template>

<script>
export default {
  name: "IPInfo"
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
}

.stat {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 1rem;

  h3 {
    text-transform: uppercase;
    color: #969696;
    font-weight: 500;
    font-size: 12px;
    margin-bottom: .5rem;
  }
  span {
    font-weight: 500;
    font-size: 23px;
    margin-bottom: .5rem;
  }
}
</style>
