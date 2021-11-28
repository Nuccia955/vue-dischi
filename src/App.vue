<template>
    <div id="app" class="d-flex flex-column h-100">
        <Header :genres="genres" @selectGenre="searchAlbums"/>

        <main class="flex-grow-1 overflow-auto">
            <CardList :list="filteredAlbumList"/>
        </main>
    </div>
</template>

<script>
import axios from 'axios'
import Header from '@/components/Header.vue'
import CardList from '@/components/CardList.vue'
export default {
    name: 'App',
    components: {
        Header,
        CardList,
    },
    data() {
        return {
            albums: null,
            searchedGenre: '',
            genres: [],
        }
    },
    created() {
        this.getAlbums();
    },
    computed: {
        filteredAlbumList() {
            if(this.searchedGenre === '') {
              return this.albums
            } else {
              return this.albums.filter(album => album.genre === this.searchedGenre)
            }
        },
    },
    methods: {
        getAlbums() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music').then(result => {
                this.albums = result.data.response;
                this.albums.forEach(album => {
                  if(!this.genres.includes(album.genre)) {
                      this.genres.push(album.genre);
                  }
                });
            }).catch(error => console.log(error));
        },
        searchAlbums(genre) {
          this.searchedGenre = genre;
          console.log(this.searchedGenre);
        }
    }
}
</script>

<style lang="scss">
@import '@/styles/colors.scss';

body {
  height: 100vh;
  #app {
    background-color: $bg_primary;
    img {
      max-width: 100%;
    }
    ul {
      list-style: none;
      margin: 0;
      padding: 0;
    }
  }
}
</style>
