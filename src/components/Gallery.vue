<template>
  <div>
    <div style="margin-bottom:50px">  Objekte geladen : {{photos.length}}</div>
    <div class="frame">
      <div v-for="(photo) in photos" :key="photo.id">
        <GalleryItem :photo="photo" />
      </div>
      <div class="buttons">
        <button @click="getPhotos()">8 weitere laden</button>
        <button @click="getPhotos(20)">20 weitere laden</button>
      </div>
    </div>
  </div>

</template>

<script>
  import GalleryItem from './GalleryItem.vue'
  export default {
    components: {
      GalleryItem
    },
    data() {
      return {
        photos: [],
      };
    },
    created() {
      this.getPhotos()
    },
    methods: {
      getPhotos(limit = 8)
       {
        this.axios.get(`https://jsonplaceholder.typicode.com/photos?_start=${this.photos.length}&_limit=${limit}`).then((response) => {
          response.data.forEach(item => this.photos.push(item));});
      }
    },
  }
</script>


<style scoped>
  .frame {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    padding: 0px;
    gap: 10px;
    width: 1076px;
    height: 111px;

    /* Extra */
    flex-flow: wrap;
    margin: auto;
  }


  .buttons {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: flex-start;
    padding: 0px;
    gap: 10px;
    width: 1076px;
    height: 37px;
    margin-top: 50px;
  }

  .buttons button {
    width: 167px;
    height: 37px;
    color: white;
    background: #05B7F1;
    border-radius: 100px;
    border: none;
  }
</style>