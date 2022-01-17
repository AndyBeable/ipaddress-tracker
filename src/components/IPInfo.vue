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
  position: absolute;
  display: flex;
  background-color: #fff;
  gap: 5px;
  padding: 8px 8px 12px 8px;
}

.stat {
  display: flex;
  flex-direction: column;
}
</style>
