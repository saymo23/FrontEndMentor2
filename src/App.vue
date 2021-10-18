<template>
  <div class="container">
    <div class="content">
      <div class="card first">
        <div class="name">
          <div class="photo"></div><!-- /.photo -->
          <h3>Report for</h3>
          <h1>
            Jeremy <br>
            Robson
          </h1>
        </div><!-- /.name -->
        <div class="time">
          <ul>
            <li>Daily</li>
            <li class="active">Weekly</li>
            <li>Monthly</li>  
          </ul>  
        </div><!-- /.time -->
      </div>
      <Card primary='#ff8b64' :type='0' :title='"Work"' :time='"32hrs"'     :lastTime='"Last Week - 36hrs"' />
      <Card primary='#56c2e6' :type='1' :title='"Play"' :time='"10hrs"'     :lastTime='"Last Week - 10hrs"' />
      <Card primary='#ff5e7d' :type='2' :title='"Study"' :time='"4hrs"'     :lastTime='"Last Week - 10hrs"' />
      <Card primary='#4bcf83' :type='3' :title='"Exercise"' :time='"4hrs"'  :lastTime='"Last Week - 10hrs"' />
      <Card primary='#7235d1' :type='4' :title='"Social"' :time='"5hrs"'    :lastTime='"Last Week - 10hrs"' />
      <Card primary='#f1c75b' :type='5' :title='"Self Care"' :time='"2hrs"' :lastTime='"Last Week - 10hrs"' />
    </div><!-- /.content -->
  </div><!-- /.container -->
</template>

<script>
import Card from './components/Card.vue'

export default {
  name: 'App',
  components: {
    Card
  }
}
</script>

<style  >
@import url('https://fonts.googleapis.com/css2?family=Rubik:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&display=swap');
body{
  --radius: 0.9rem;
  --inactive: #c2baff;
  --inactive2: #777bbb;
  font-size: 18px;
}
.container{
  font-family: 'Rubik', sans-serif;
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: hsl(226, 43%, 10%);
  color: white;
}
.content{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  gap: 30px;
  grid-template-areas:
    "a b c d"
    "a e f g";
}
.card{
  width: 255px;
  height: 100%;
  border-radius: var(--radius);
  background-color: #1d204b;
  overflow: hidden;
}
.first{
  grid-area: a;
  padding: 0rem;
  height: 100%;
}
.name{
  background-color: #5746ea;
  border-radius: var(--radius);
  padding: 2rem 1.8rem;
}
.photo{
  background-image: url(./assets/image-jeremy.png);
  background-repeat: no-repeat;
  background-size: contain;
  background-position: center;
  width: 4.5rem;
  height: 4.5rem;
  border-radius: 99rem;
  border: 3px solid white;
  margin-bottom: 2.5rem;
}
.time{
  display: flex;
  padding: 1rem 1.8rem;
}
.time ul{
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100%;
  list-style: none;
  margin: 0;padding: 0;
}
.time li{
  margin: 0;
  list-style-position: unset;
  margin-bottom: 0.5rem;
  color: var(--inactive2);
  padding: 0.3rem 0;
  font-size: 1rem;
}
.time li.active{
  color: white;
}
.second{
  background-color: #ff8b64;
}

h1{
  margin: 0;padding: 0;
  font-size: 2.3rem;
  font-weight: 100;
  margin-bottom: 2.8rem;
}
h3{
  margin: 0;padding: 0;
  font-size: 0.9rem;
  font-weight: 400;
  color: var(--inactive);
  margin-bottom: 5px;
}
/*! normalize.css v8.0.1 | MIT License | github.com/necolas/normalize.css */html{line-height:1.15;-webkit-text-size-adjust:100%}body{margin:0}main{display:block} hr{box-sizing:content-box;height:0;overflow:visible}pre{font-family:monospace,monospace;font-size:1em}a{background-color:transparent}abbr[title]{border-bottom:none;text-decoration:underline;text-decoration:underline dotted}b,strong{font-weight:bolder}code,kbd,samp{font-family:monospace,monospace;font-size:1em}small{font-size:80%}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}sub{bottom:-.25em}sup{top:-.5em}img{border-style:none}button,input,optgroup,select,textarea{font-family:inherit;font-size:100%;line-height:1.15;margin:0}button,input{overflow:visible}button,select{text-transform:none}[type=button],[type=reset],[type=submit],button{-webkit-appearance:button}[type=button]::-moz-focus-inner,[type=reset]::-moz-focus-inner,[type=submit]::-moz-focus-inner,button::-moz-focus-inner{border-style:none;padding:0}[type=button]:-moz-focusring,[type=reset]:-moz-focusring,[type=submit]:-moz-focusring,button:-moz-focusring{outline:1px dotted ButtonText}fieldset{padding:.35em .75em .625em}legend{box-sizing:border-box;color:inherit;display:table;max-width:100%;padding:0;white-space:normal}progress{vertical-align:baseline}textarea{overflow:auto}[type=checkbox],[type=radio]{box-sizing:border-box;padding:0}[type=number]::-webkit-inner-spin-button,[type=number]::-webkit-outer-spin-button{height:auto}[type=search]{-webkit-appearance:textfield;outline-offset:-2px}[type=search]::-webkit-search-decoration{-webkit-appearance:none}::-webkit-file-upload-button{-webkit-appearance:button;font:inherit}details{display:block}summary{display:list-item}template{display:none}[hidden]{display:none}
/*# sourceMappingURL=normalize.min.css.map */
</style>
