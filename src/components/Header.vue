<template>
  <div>
    <b-navbar class="nav" toggleable="lg" type="dark">
      <b-navbar-brand href="#">Real estate</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item to="/">Buy</b-nav-item>
          <b-nav-item to="/rent">Rent</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<style lang="scss" scoped>
@import "src/assets/custom.scss";

#nav a.router-link-exact-active {
  color: white;
}
.navbar-dark {
  background-color: #f7976f;
}
</style>