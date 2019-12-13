<template>
  <div>
    <p id="footer">Made with Vue</p>
  </div>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style lang="scss" scoped>
@import "src/assets/custom.scss";

#footer {
  position: sticky;
  right: 0;
  bottom: 0;
  left: 0;
  padding-top: 0.5rem;
  padding-right: 1rem;
  padding-bottom: 0.5rem;
  padding-left: 1rem;
  margin-bottom: 1rem;
  margin-left: 2rem;
  margin-right: 2rem;
  background-color: $primary;
  text-align: center;
}
</style>