<template>
  <b-carousel-list v-model="test" :data="items" :items-to-show="2">
    <template slot="item" slot-scope="list">
      <div class="card">
        <div class="card-image">
          <figure class="image is-5by4">
            <a @click="info(list.index)"><img :src="list.image"></a>
          </figure>
          <b-tag type="is-danger" rounded style="position: absolute; top: 0;"><b>50%</b></b-tag>
        </div>
        <div class="card-content">
          <div class="content">
            <p class="title is-6">{{ list.title }}</p>
            <p class="subtitle is-7">@johnsmith</p>
            <div class="field is-grouped">
              <p class="control" style="margin-left: auto">
                <button class="button is-small is-danger is-outlined">
                    <b-icon size="is-small" icon="heart"/></button>
                  </p>
            </div>
          </div>
        </div>
      </div>
    </template>
  </b-carousel-list>
</template>

<script>
export default {
  data() {
    return {
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
