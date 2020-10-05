<template>
  <div class="container">
    <div class="review-content">
        <div class="review-content-form">
             <ReviewForm/>
        </div>
        <div class="devider"></div> 
        <div class="review-content-list">
             <ReviewList/> 
        </div>
    </div>
  </div>
</template>

<script>
import ReviewForm from './ReviewForm'
import ReviewList from './ReviewList'



export default {
  name: 'BasicLayout',
  components: {
      ReviewForm,
      ReviewList
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
.review-content{
    display: flex;
    flex-direction: column;
}

.review-content-form {
  overflow: hidden;
}

.review-content-list{
  overflow: scroll;
}

.devider{
    width: 90%;
    height: 5px;
    background-color: white;
    position: relative;
    left: 0;
    right: 0;
    margin-right: auto;
    margin-bottom: 22px;
    margin-left: auto;
    overflow: hidden;
    top: 14px
}

body {
    background-color: #855876;
}

</style>
