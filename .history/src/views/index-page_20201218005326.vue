<template>
  <section class="section">
    <div class="container is-fluid">
      <b-carousel>
        <b-carousel-item v-for="(carousel, i) in carousels" :key="i">
          <section :class="`hero is-large is-${carousel.color}`">
            <div class="hero-body has-text-centered">
              <h1 class="title">{{ carousel.text }}</h1>
            </div>
          </section>
        </b-carousel-item>
      </b-carousel>
    </div>
    <hr class="horizontal-line">
    <div>
      <b-carousel-list v-model="test" :data="items" :items-to-show="2">
        <template slot="item" slot-scope="list">
          <div class="card">
            <div class="card-image">
              <figure class="image is-5by4">
                <a @click="info(list.index)"><img :src="list.image"></a>
              </figure>
            </div>
            <div class="card-content">
              <div class="content">
                <p class="title is-6">{{ list.title }}</p>
                <p class="subtitle is-7">Image</p>
              </div>
            </div>
          </div>
        </template>
      </b-carousel-list>
    </div>
    <hr class="horizontal-line">
    <div class="container">
      <div class="box">
        <article class="media-content">
          <div class="class">
            <p>
              <strong>The title of the article</strong>
              <br>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean efficitur sit amet massa fringilla egestas. Nullam condimentum luctus turpis.
            </p>
          </div>
          <nav class="level is-mobile">
            <div class="level-left">
              <a class="level-item" aria-label="comment">
                <span class="icon is-small">
                  <i class="far fa-comment" aria-hidden="true" />
                </span>
              </a>
              <a class="level-item" aria-label="share">
                <span class="icon is-small">
                  <i class="fas fa-share" aria-hidden="true" />
                </span>
              </a>
              <a class="level-item" aria-label="like">
                <span class="icon is-small">
                  <i class="fad fa-like" aria-hidden="true" />
                </span>
              </a>
            </div>
          </nav>
        </article>
      </div>
    </div>
    <hr class="horizontal-line">
    <div class="container">
      <div class="box">
        <article class="media-content">
          <div class="class">
            <p>
              <strong>The title of the article</strong>
              <br>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean efficitur sit amet massa fringilla egestas. Nullam condimentum luctus turpis.
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean efficitur sit amet massa fringilla egestas. Nullam condimentum luctus turpis.
            </p>
          </div>
          <nav class="level is-mobile">
            <div class="level-left">
              <a class="level-item" aria-label="comment">
                <span class="icon is-small">
                  <i class="far fa-comment" aria-hidden="true" />
                </span>
              </a>
              <a class="level-item" aria-label="share">
                <span class="icon is-small">
                  <i class="fas fa-share" aria-hidden="true" />
                </span>
              </a>
              <a class="level-item" aria-label="like">
                <span class="icon is-small">
                  <i class="fad fa-like" aria-hidden="true" />
                </span>
              </a>
            </div>
          </nav>
        </article>
      </div>
    </div>
    <hr class="horizontal-line">
    <div class="container">
      <div class="box">
        <article class="media-content">
          <div class="class">
            <p>
              <strong>The title of the article</strong>
              <br>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean efficitur sit amet massa fringilla egestas. Nullam condimentum luctus turpis.
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean efficitur sit amet massa fringilla egestas. Nullam condimentum luctus turpis.
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean efficitur sit amet massa fringilla egestas. Nullam condimentum luctus turpis.
            </p>
          </div>
          <nav class="level is-mobile">
            <div class="level-left">
              <a class="level-item" aria-label="comment">
                <span class="icon is-small">
                  <i class="far fa-comment" aria-hidden="true" />
                </span>
              </a>
              <a class="level-item" aria-label="share">
                <span class="icon is-small">
                  <i class="fas fa-share" aria-hidden="true" />
                </span>
              </a>
              <a class="level-item" aria-label="like">
                <span class="icon is-small">
                  <i class="fad fa-thumbs-up" aria-hidden="true" />
                </span>
              </a>
            </div>
          </nav>
        </article>
      </div>
    </div>
  </section>
</template>

<script>
import ContentCards from "../components/content-cards.vue"
export default {
  name: "Index",
  component: {
    ContentCards,
  },
  data() {
    return {
      carousels: [
        { text: "Slide 1", color: "primary" },
        { text: "Slide 2", color: "info" },
        { text: "Slide 3", color: "success" },
        { text: "Slide 4", color: "warning" },
        { text: "Slide 5", color: "danger" },
      ],

      test: 0,
      items: [
        {
          title: "Slide 1",
          image: "https://buefy.org/static/img/placeholder-1280x960.png",
        },
        {
          title: "Slide 2",
          image: "https://buefy.org/static/img/placeholder-1280x960.png",
        },
        {
          title: "Slide 3",
          image: "https://buefy.org/static/img/placeholder-1280x960.png",
        },
        {
          title: "Slide 4",
          image: "https://buefy.org/static/img/placeholder-1280x960.png",
        },
        {
          title: "Slide 5",
          image: "https://buefy.org/static/img/placeholder-1280x960.png",
        },
        {
          title: "Slide 6",
          image: "https://buefy.org/static/img/placeholder-1280x960.png",
        },
        {
          title: "Slide 7",
          image: "https://buefy.org/static/img/placeholder-1280x960.png",
        },
        {
          title: "Slide 8",
          image: "https://buefy.org/static/img/placeholder-1280x960.png",
        },
      ],
    }
  },
  methods: {
    info(value) {
      this.test = value
    },
  },
}
</script>

<style lang="scss" scoped></style>
