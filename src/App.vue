<template>
  <div id="app">
    <lingallery
      :mobileHeight="200"
      :width="600"
      :height="400"
      @index="onIndexChanged"
      :items="items"
    />
    <p>Current gallery image index: {{wurst}}</p>
  </div>
</template>

<script>
import Lingallery from "./components/Lingallery.vue";

export default {
  name: "App",
  data() {
    return {
      wurst: -1,
      items: [
        {
          src: "https://picsum.photos/600/600/?image=0",
          thumbnail: "https://picsum.photos/64/64/?image=0",
          caption: "Some Caption"
        },
        {
          src: "https://picsum.photos/600/400/?image=10",
          thumbnail: "https://picsum.photos/64/64/?image=10",
          caption: "Another Caption"
        },
        {
          src: "https://picsum.photos/400/600/?image=20",
          thumbnail: "https://picsum.photos/64/64/?image=20"
        },
        {
          src: "https://picsum.photos/600/400/?image=30",
          thumbnail: "https://picsum.photos/64/64/?image=30"
        },
        {
          src: "https://picsum.photos/600/400/?image=40",
          thumbnail: "https://picsum.photos/64/64/?image=40"
        },
        {
          src: "https://picsum.photos/600/400/?image=50",
          thumbnail: "https://picsum.photos/64/64/?image=50"
        },
        {
          src: "https://picsum.photos/400/600/?image=60",
          thumbnail: "https://picsum.photos/64/64/?image=60"
        },
        {
          src: "https://picsum.photos/600/400/?image=70",
          thumbnail: "https://picsum.photos/64/64/?image=70"
        },
        {
          src: "https://picsum.photos/600/400/?image=80",
          thumbnail: "https://picsum.photos/64/64/?image=80"
        },
        {
          src: "https://picsum.photos/600/400/?image=90",
          thumbnail: "https://picsum.photos/64/64/?image=90"
        },
        {
          src: "https://picsum.photos/600/400/?image=100",
          thumbnail: "https://picsum.photos/64/64/?image=100"
        }
      ]
    };
  },
  components: {
    Lingallery
  },
  methods: {
    onIndexChanged(idx) {
      this.wurst = idx;
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
