<template>
  <div class="wingpanel">
    <div>Applications</div>
    <div>Date and Time</div>
    <div>Tray</div>
  </div>
</template>

<script>
export default {
  name: "Wingpanel",
};
</script>

<style scoped>
.wingpanel {
  display: flex;
  justify-content: space-between;
  padding: 4px;
  color: white;
  font-weight: 700;
  font-size: 1.25em;
}
</style>