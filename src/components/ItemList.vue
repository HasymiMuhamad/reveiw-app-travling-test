<template>
    <div class="content-2">
        <div class="sub-content-list">
            <div class="list-id">
                <img class="icon-profile" :src="avatar"/>
                <div class="username">
                    <p class="content-username">{{author}}</p>
                    <p class="content-date">{{commentDate}}</p>
                    <div class="icon">
                        <img class="star-icon" :src="starIcon">
                        <img class="star-icon" :src="starIcon">
                        <img class="star-icon" :src="starIcon">
                        <img class="star-icon" :src="starIcon">
                        <img class="star-icon" :src="starIcon">
                    </div>
                </div>
                <img :class="mobileView" :src="moreIcon">
            </div>
            <div class="comment">
                <p>{{comment}}</p>
                <div class="comment-flex">
                    <img class="comment-image" :src="imageContent">
                    <div v-if="imageContentAlt">
                        <img class="comment-image" :src="imageContentAlt">
                    </div>
                    <div v-else> </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import boyPhoto from '../assets/ali-yahya.jpg'
import moreIcon from '../assets/more.svg'
import starIcon from '../assets/star.svg'
import imageComment from '../assets/mountainView.jpg'
import imageComment2 from '../assets/mountainView2.jpg'
import { isMobile } from 'mobile-device-detect';


export default {
  name: 'ItemList',
  props: ["comment","author","imageContent","imageContentAlt","avatar","commentDate"],
  data(){
    return {
      boyPhoto,
      moreIcon,
      starIcon,
      imageComment,
      imageComment2,
      mobileView : isMobile ? "more-icon" : "more-icon-general"
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.content-2 {
    position: relative;
    left: 0;
    right: 0;
    bottom: 0;
}

.content-2 .sub-content-list{
    width: 90%;
    height: 216px;
    background-color: rgb(244, 243, 248);
    border-radius: 6px;
    position: relative;
    right: 0;
    left: 0;
    margin-top: 10px;
    margin-right: auto;
    margin-bottom: auto;
    margin-left: auto;
    display:flex;
    flex-direction: column;
    box-shadow: 0px 3px 6px -1px rgba(0,0,0,0.1);

}

.content-2 .sub-content-list .list-id{
    display: flex;
    flex-direction: row;
    background-color: white;
    border-radius: 6px;
    height: 64px;
}

.content-2 .sub-content-list .list-id .more-icon{
    position: relative;
    left: 20px;
}

.content-2 .sub-content-list .list-id .more-icon-general {
    position: relative;
    left: 346px;
}

.content-2 .sub-content-list .list-id .username {
    display: flex;
    flex-direction: column;
    font-size: 16px;
    line-height: 0.75em;
    font-family: Arial;
    margin-left: 2px;
    margin-top: 7px;
}

.content-2 .sub-content-list .list-id .username .content-username{
    position: relative;
    bottom: 0.7em;
    font-size: 14px;
    text-align: left;
}

.content-2 .sub-content-list .list-id .username .content-date{
    position: relative;
    bottom: 3.02em;
    font-size: 11px;
    text-align: left;
}

img {
    border-radius: 50%;
    width: 30px;
    height: 30px;
    margin-top: 9px;
    margin-left: 11px;
    margin-right: 10px;
}

.icon {
    width: 186px;
    position: relative;
    margin-top: 25px;
    right: 46px;
    bottom: 74px;
}

.icon .star-icon {
    width: 15px;
    height: 15px;
    margin-left: 0px;
    margin-right: 4px;
}

.icon-profile {
    margin-top:18px
}

.comment {
    text-align: left;
    margin-left: 51px;
    line-height: 0px;
}

.comment .comment-image {
    width: 100px;
    height: 100px;
    border-radius: 20%;
    margin-left: 0px;
    margin-top: 0px;
}

.comment .comment-flex {
    display: flex;
    flex-direction: row;
}

</style>
