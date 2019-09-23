<template>
 <div class="main-div">
 <div :class="'main-div'">
   hello 
 <span v-if="dataIf">data with condition</span>
 </div>
  
  <div>
  naim
  <button v-on:[eventName]="run()"> click</button>
  <button v-bind:[key]="value"></button>
  </div> 
 
  </div> 
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
 data () {
    return{
      rawHtml:'<b>cool</b>',
      bindedData:'binded data',
      inputData:'yo man',
      dataIf:true,
      eventName:'focus',
      key:'cool',
      value:'main-div'

    } 
 },
 methods:{
     run:function () {
        // dataIf=false;
        this.dataIf=false;
     }
 }



}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >

.main-div{
  display:'flex';
  justify-content:center;
  /* align-items: center; */
  align-content: center;
  flex-direction: column-reverse;
  height: 100px;

  border: 1px solid black;
}

</style>
