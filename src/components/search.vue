<template>
  <div class="container my-3">
    <div class="row">
      <div class="col-md-6 card py-3">
        <nav class="navbar col-12">
          <form class="d-flex col-12">
            <input
              class="form-control mr-sm-2"
              type="search"
              placeholder="Search"
              aria-label="Search"
              v-model="name">
          </form>
        </nav>
        <div class="mt-3">
          <div class="jumbotron content-search mb-0 py-3">
            <div
              v-for="(item, index) in searchNoticia"
              :key="index">
              <div class="content-art row align-items-center justify-content-around py-2"
                @click="selectItem(item)">
                <div class="col-md-4 col-12 content-img">
                  <img :src="item.image" class="img-fluid img-artist" alt="img">
                </div>
                <div class="col-md-8 col-12 title">
                  <b>{{item.name}}</b>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div> 
      <div class="col-md-6 detail">
        <div class="card p-3 detail-card">
          <div class="col-12 d-flex flex-column justify-content-center">
            <img :src="artist.image" class="img-detail" alt="">
            <h1 class="text-center my-3">
              {{artist.name}}
            </h1>
          </div>
          <div>
            <span>
              {{artist.description}}
            </span>
          </div>
        </div>
        
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      top: [
        {
          image: "https://picsum.photos/300/300",
          name: "Zurdok",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta "
        },
        {
          image: "https://picsum.photos/300/300",
          name: "Los Victorios",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta"
        },
        {
          image: "https://picsum.photos/300/300",
          name: "The Strokes",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dictaLorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta "
        },
        {
          image: "https://picsum.photos/300/300",
          name: "System of A down",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dictaLorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta "
        },
        {
          image: "https://picsum.photos/300/300",
          name: "Raimstein",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dictaLorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta "
        },
        {
          image: "https://picsum.photos/300/300",
          name: "The Who",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta"
        },
        {
          image: "https://picsum.photos/300/300",
          name: "AFI",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dictaLorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta "
        },
        {
          image: "https://picsum.photos/300/300",
          name: "Los de abajo",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta"
        },
        {
          image: "https://picsum.photos/300/300",
          name: "Satelit Kingston",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dictaLorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta "
        },
        {
          image: "https://picsum.photos/300/300",
          name: "Babasonicos",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio unde, optio nulla, perferendis nam dicta"
        }
      ],
      name: '',
      artist:{},
    };
  },
  computed: {
    searchNoticia: function() {
      return this.top.filter(item => {
        return (
          item.name
            .toLowerCase()
            .includes(this.name.toLowerCase()) ||
          item.name
            .toLowerCase()
            .includes(this.name.toLowerCase())
          
        );
      });
    }
  },
  methods: {
    selectItem: function(item) {
      this.artist = item
    }
  }
};
</script>

