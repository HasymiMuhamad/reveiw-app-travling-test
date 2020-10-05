<template>
    <div class="list">
         <div v-for="item in reviewData.reviews.most_recent" :key="item.content">
            <ItemList 
                v-bind:comment="item.content"
                v-bind:author="item.author"
                v-bind:imageContent="item.image"
                v-bind:imageContentAlt="item.imageAlt"
                v-bind:avatar="item.avatar"
                v-bind:commentDate="item.date"
            /> 
        </div>
    </div>
</template>

<script>
import ItemList from './ItemList'
import axios from 'axios'

var endPointGetReviewData = 'https://mock-review-api-travling.getsandbox.com:443/reviews'



export default {
  name: 'ReviewList',
  components:{
      ItemList
  },
  data (){
      return {
          reviewData : {}
      }
  },
  mounted (){
      axios
      .post(endPointGetReviewData, {})
      .then(response => {
          this.reviewData = response.data
      })
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.list{ 
    overflow-y: scroll;
}

</style>
