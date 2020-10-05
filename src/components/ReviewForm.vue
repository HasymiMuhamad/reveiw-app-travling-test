<template>
    <div class="content-1">
        <div class="sub-content">
            <div class="sub-content-title">
                <p class="title">Review</p>
                <div :class="ratingView">
                    <img class="star-icon" :src="starIcon">
                    <img class="star-icon" :src="starIcon">
                    <img class="star-icon" :src="starIcon">
                    <img class="star-icon" :src="starIcon">
                    <img class="star-icon" :src="starIcon">
                </div>
            </div>
            <div class="content-form">
                <form class="form-data">
                    <input class="input-form" 
                        placeholder="Tulis Nama Kamu"
                    >
                    <input class="input-form-textarea" 
                        placeholder="Tulis Review Terbaik kamu"
                    >
                </form>
            </div>
            <div class="submit-button">
                <div class="upload-image">
                    <p>Upload Gambar</p>
                </div>
                <div class="send">
                    <p>Kirim</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import starIcon from '../assets/star.svg'
import { isMobile } from 'mobile-device-detect';


export default {
  name: 'ReviewForm',
  data(){
    return {
      starIcon,
      ratingView : isMobile ? 
        "icon" : "icon-rating-general"
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.content-1 {
    width: 100%;
    height: 308px;
    position: relative;
    left: 0;
    right: 0;
    top: 0;
}

.content-1 .sub-content{
    width: 90%;
    height: 302px;
    background-color: rgb(244, 243, 248);
    position: relative;
    right: 0;
    left: 0;
    margin: auto;
    border-radius: 6px;
    box-shadow: 0 3px 1px -2px rgba(0,0,0,.2),0 2px 2px 0 rgba(0,0,0,.14),0 1px 5px 0 rgba(0,0,0,.12)
}

.content-1 .sub-content .submit-button {
    width: 100%;
    height: 45px;
    background-color: #50D1AD;
    margin-top: 19px;
    border-radius: 0 0 6px 6px;
    display :flex;
    flex-basis: row;
    position: relative;
    bottom : 72px;
}

.content-1 .sub-content .submit-button .upload-image {
    width: 50%;
    height: 45px;
    background-color: transparent;
    color: white;
    border-right: 2px solid white;
}

.content-1 .sub-content .submit-button .send {
    width: 50%;
    height: 45px;
    background-color: transparent;
    color: white;
    float: right;
}

.content-1 .sub-content .content-form {
    margin-top: 79px;
    border-radius: 6px;
    margin-left: 10px;
    margin-right: 10px;
}

.content-1 .sub-content .content-form .form-data{
    position: relative;
    bottom: 63px;
}

.content-1 .sub-content .content-form .input-form{
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    box-sizing: border-box;
    border: 2px solid #51D1AD;
    border-radius: 6px;
}

.content-1 .sub-content .content-form .input-form-textarea{
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    box-sizing: border-box;
    border: 2px solid #51D1AD;
    border-radius: 6px;
    height: 95px;
}

.content-1 .sub-content .sub-content-title{
    width: 100%;
    height: 63px;
    background-color: white;
    position: relative;
    left: 0px;
    right: 0px;
    border-radius: 6px 6px 0 0;
    display: flex;
    flex-direction: row;
    box-shadow: 0px 3px 6px -1px rgba(0,0,0,0.1);
}

.content-1 .sub-content .sub-content-title .icon{
    flex-direction: row;
    display: flex;
    align-items: flex-start;
    flex-wrap: nowrap;
    margin-top: 30px;
    margin-left: 45px;
    justify-content: space-around;
    margin-right: 16px;
}

.content-1 .sub-content .sub-content-title .icon-rating-general{
    flex-direction: row;
    display: flex;
    align-items: flex-start;
    flex-wrap: nowrap;
    margin-top: 12px;
    margin-left: 45px;
    justify-content: space-around;
    margin-right: 17px;
    width: 206px;
    position: relative;
    left: 234px;
}

.content-1 .sub-content .sub-content-title .title{
    left: 17px;
    font-size: 36px;
    margin-top: 10px;
    margin-left: 15px;
}

.content-1 .sub-content .sub-content-title .star-icon{
    width: 40%;
    padding-left: 10px;
}

</style>
