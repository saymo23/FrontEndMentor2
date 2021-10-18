<template>
  <div class="card" :style="[style]">
    <div class="inCard">
      <div class="title">
        {{title}}
        <div class="enfasis">
          <img :src="image7" alt="More...">
        </div><!-- /.enfasis -->
      </div><!-- /.title -->
      <div class="hours">
        {{time}}
      </div><!-- /.hours -->
      <div class="lastTime">{{lastTime}}</div><!-- /.lastTime -->
    </div><!-- /.inCard -->
  </div><!-- /.card -->
</template>

<script>
import image1 from '../assets/icon-work.svg'
import image2 from '../assets/icon-play.svg'
import image3 from '../assets/icon-study.svg'
import image4 from '../assets/icon-exercise.svg'
import image5 from '../assets/icon-social.svg'
import image6 from '../assets/icon-self-care.svg'
import image7 from '../assets/icon-ellipsis.svg'

export default {
  props: {
    primary: String,
    type: String,
    title: String,
    time: String,
    lastTime: String
  },
  data: function(){
    let types = new Array(image1, image2, image3, image4, image5, image6)
    
    return {
      types: types,
      image7: image7,
      style: {
        backgroundColor: this.primary, 
        'background-image': 'url('+ types[this.type] +')'
      }
    }
  }
}
</script>

<style>
.card{
  border-radius: var(--radius);
  background-color: #1d204b;
  overflow: hidden;
  background-image: url(../assets/icon-work.svg);
  background-position: right top;
  background-position-y: -1rem;
  background-position-x: 9rem;
  background-repeat: no-repeat;
}
.inCard{
  margin-top: 40px;
  background-color: #1d204b;
  padding: 0.5rem 1.8rem;
  height: 167px;
  border-radius: var(--radius) var(--radius) 0 0;
}
.title{
  display: flex;
  justify-content: space-between;
  font-weight: bold;
  font-size: 1rem;
  margin:1.2rem 0 1.5rem;
}
.enfasis{}
.hours{
  font-size: 3.2rem;
  font-weight: 100;
  margin-bottom: 0.3rem;
}
.lastTime{
  color: hsl(236, 100%, 87%);
  padding: 0.3rem 0 0.3rem;
  font-size: 0.85rem;
}
</style>