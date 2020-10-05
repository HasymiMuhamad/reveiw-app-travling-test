<template>
    <div class="list">
         <!-- <div v-for="item in reviewData.reviews.most_recent" :key="item.content">
            <li>{{item.content}}</li>
        </div> -->
        <ItemList/> 
        <ItemList/>
        <ItemList/>
        <ItemList/>
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
          console.log('response get data', response.data.reviews)
          console.log('response get data content', response.data.reviews.most_recent[0].content)
            // console.table('res table', response.data.reviews.most_recent)
          this.reviewData = response.data
          console.log('response get data this', this.reviewData.reviews.most_recent[0].content)

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
