<template>
  <div>
    <!-- :img-src="require('/home/vilmos/Flow/Vue/house/src/assets/house2.jpg')" -->
    <!-- :title="name" -->
    <b-col>
      <b-card
        :img-src="image"
        img-alt="info"
        img-top
        tag="article"
        style="max-width:20rem"
        class="mb-2"
        border-variant="primary"
      >
        <b-card class="usercard">
          <b-card-title id="username">{{ username }}</b-card-title>
          <b-card-sub-title id="userstatus">{{ status }}</b-card-sub-title>
          <div id="rating">
            <i v-if="rating === 1" class="fa fa-star"></i>
            <i v-if="rating === 2" class="fa fa-star"></i>
            <i v-if="rating === 2" class="fa fa-star"></i>
            <i v-if="rating === 3" class="fa fa-star"></i>
            <i v-if="rating === 3" class="fa fa-star"></i>
            <i v-if="rating === 3" class="fa fa-star"></i>
            <i v-if="rating === 4" class="fa fa-star"></i>
            <i v-if="rating === 4" class="fa fa-star"></i>
            <i v-if="rating === 4" class="fa fa-star"></i>
            <i v-if="rating === 4" class="fa fa-star"></i>
            <i v-if="rating === 5" class="fa fa-star"></i>
            <i v-if="rating === 5" class="fa fa-star"></i>
            <i v-if="rating === 5" class="fa fa-star"></i>
            <i v-if="rating === 5" class="fa fa-star"></i>
            <i v-if="rating === 5" class="fa fa-star"></i>
          </div>
        </b-card>
        <b-card-title>{{ name }}</b-card-title>
        <b-card-sub-title>
          <i class="fa fa-map-marker" aria-hidden="true"></i>
          {{ address }}
        </b-card-sub-title>
        <b-card-text class="container">
          <div class="item">
            <i class="fa fa-bed fa-3x" aria-hidden="true"></i>
          </div>
          <div class="item">
            <i class="fa fa-bath fa-3x" aria-hidden="true"></i>
          </div>
          <div class="item">
            <i class="fa fa-drafting-compass fa-3x" aria-hidden="true"></i>
          </div>
          <div class="item number">{{ bedroom }}</div>
          <div class="item number">{{ bathroom }}</div>
          <div class="item number">{{ area }}</div>
          <div class="item">BEDROOM</div>
          <div class="item">BATHROOM</div>
          <div class="item">AREA SQFT</div>
        </b-card-text>
        <div>
          <span id="price">${{ price }}</span>
          <b-button pill class="button">Negotiable</b-button>
        </div>
      </b-card>
    </b-col>
  </div>
</template>

<script>
export default {
  props: [
    "name",
    "rating",
    "image",
    "username",
    "status",
    "address",
    "price",
    "bedroom",
    "area",
    "bathroom"
  ]
};
</script>

<style lang="scss" scoped>
@import "src/assets/custom.scss";

.fa-star {
  color: $primary;
}
.fa-map-marker {
  color: $primary;
}
.border-primary {
  border-color: $primary !important;
}
.button {
  background-color: $primary;
  border-color: $primary;
  float: right;
}
.usercard {
  text-align: left;
  border: 0em;
}
#username {
  font-size: 1em;
}
#userstatus {
  font-size: 0.8em;
}
#price {
  font-size: 1.5em;
  font-weight: bold;
  float: left;
  padding-left: 0.5em;
}
.container {
  display: flex;
  flex-wrap: wrap;
  margin-top: 2rem;
  margin-bottom: 2rem;
}
.item {
  flex: 0 0 32%;
  font-size: 0.7em;
  font-weight: bold;
}
.number {
  font-size: 1em;
  margin-top: 1rem;
  margin-bottom: 1rem;
}
</style>