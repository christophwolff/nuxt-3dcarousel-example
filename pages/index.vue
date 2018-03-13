<template>
  <section class="container">
    <app-logo/>
    <h1 class="title">
      3D Carousel Example
    </h1>
    <no-ssr>
      <carousel-3d>
        <slide v-for="(slide, i) in slides" :key="i" :index="i">
          <img src="https://placehold.it/360x270">
        </slide>
      </carousel-3d>
    </no-ssr>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'
export default {
  data () {
    return {
      slides: 7
    }
  },
  components: {
    AppLogo
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  flex-direction: column;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
