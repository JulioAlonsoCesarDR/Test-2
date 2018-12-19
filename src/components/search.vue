<template>
  <div class="container my-3">
    <div class="col-md-6 card">
      <nav class="navbar col-12">
        <form class="d-flex col-12">
          <input
            class="form-control mr-sm-2"
            type="search"
            placeholder="Search"
            aria-label="Search"
            v-model="nameTop">
          <button @click="getFilter(nameTop)" class="btn btn-outline-info my-2 my-sm-0" type="submit">Search</button>
        </form>
      </nav>
      <div class="my-3">
        <div class="jumbotron">
          <div v-for="(art, index) in topResult" :key="index" class="d-flex justify-content-between">
            {{name}}
          </div>
        </div>
      </div>
    </div>
    <div class="col-md-6"></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      top: [
        {
            image: "https://picsum.photos/50/50",
            name: "Eminem",
            description:"Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta"
        },
        {
            image: "https://picsum.photos/50/50",
            name: "Los Victorios",
            description:"Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta"
        },
        {
            image: "https://picsum.photos/50/50",
            name: "The Strokes",
            description:"Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta"
        },
        {
            image: "https://picsum.photos/50/50",
            name: "System of A down",
            description:"Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta"
        },
        {
            image: "https://picsum.photos/50/50",
            name: "Raimstein",
            description:"Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta"
        },
        {
            image: "https://picsum.photos/50/50",
            name: "The Who",
            description:"Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta"
        },
        {
            image: "https://picsum.photos/50/50",
            name: "AFI",
            description:"Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta"
        },
        {
            image: "https://picsum.photos/50/50",
            name: "Los de abajo",
            description:"Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta"
        },
        {
            image: "https://picsum.photos/50/50",
            name: "Satelit Kingston",
            description:"Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta"
        },
        {
            image: "https://picsum.photos/50/50",
            name: "Babasonicos",
            description:"Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta"
        },
      ], 
      nameTop: '',
      topResult: [],
    };
  },
  methods: {
    getFilter: function(name){
      const result = this.top.filter(artist => artist.name === name);
      debugger
      this.topResult = result
      console.log(result)
    }
  }
};
</script>

