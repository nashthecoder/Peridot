<template>
  <section class="section">
    <div class="container">
      <b-carousel>
        <b-carousel-item v-for="(carousel, i) in carousels" :key="i">
          <section :class="`hero is-medium is-${carousel.color}`">
            <div class="hero-body has-text-centered">
              <h1 class="title">{{ carousel.text }}</h1>
            </div>
            <br><br/>
            <div>
              <content-cards />
            </div>
          </section>
        </b-carousel-item>
      </b-carousel>
    </div>
  </section>
</template>

<script>
import ContentCards from "../components/content-cards.vue"
export default {
  name: "Index",
  components: { ContentCards },
  data(){
    return {
      carousels: [
        { text: "Slide 1", color: "primary" },
        { text: "Slide 2", color: "info" },
        { text: "Slide 3", color: "success" },
        { text: "Slide 4", color: "warning" },
        { text: "Slide 5", color: "danger" }
      ],
    },
  }
}
</script>

<style lang="scss" scoped></style>
