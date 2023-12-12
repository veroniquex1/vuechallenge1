<template>
  <div class="packet">
  <select name="" id="">
    <option value="">Sort</option>
    <option value="">Fiction</option>
    <option value="">Non-Fiction</option>
  </select>
</div>
    <div class="row" v-show="books">
      <div class="card"  v-for="book in books" :key="book.category">
        <div class="card-head">
          <h4>{{ book.name }}</h4>

        </div>
        <div class="card-body">
          <img :src="book.image" alt="" loading="lazy">
          <h6>{{ book.category }}</h6>
          <p>R{{ book.cost }}</p>

        </div>
        <div class="card-footer">

        </div>
      </div>
    </div>
  <!-- </div> -->
</template>

<script>
export default {
  name: 'vueChallenge1',
  components: {},
  data(){
    return{
      books: [{
        id: 1,
        name: 'The Lives Inside Your Head',
        category: 'Non-Fiction',
        cost: 180,
        image: 'https://i.postimg.cc/Yq0hmFRP/book1.png'
    },
    {
        id: 2,
        name: 'Physics for Science and Engineering Student',
        category: 'Non-Fiction',
        cost: 1300,
        image: 'https://i.postimg.cc/bvwPhwtf/download-1.jpg'
    },
    // {
    //     id: 3,
    //     name: 'Harry Potter and the Philosopher\'s Stone',
    //     category: 'Fiction',
    //     cost: 200,
    //     image: 'https://i.postimg.cc/mkJs73jg/hp1.jpg'
    // },
    {
        id: 4,
        name: 'Harry Potter and the Chamber of Secrets',
        category: 'Fiction',
        cost: 200,
        image: 'https://i.postimg.cc/nhn3vZpQ/hp2.webp'
    },
    {
        id: 5,
        name: 'Gray\'s Anatomy',
        category: 'Non-Fiction',
        cost: 1500,
        image: 'https://i.postimg.cc/ZnJwyCFw/download-3.jpg'
    },]
  }
},

  methods: {
    
  },

  computed: {
    genre() {
      return this.books.filter((item) => item.category == 'Fiction' || item.category == 'Non-Fiction' )}

  },
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.packet .row {
  display: flex;
  /* flex-wrap: wrap; */
}
.card{
  width: 15rem;
}

.card-body img(

)

.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  padding: 12px 16px;
  /* z-index: 1; */
}

.dropdown:hover .dropdown-content {
  display: block;
}
</style>
