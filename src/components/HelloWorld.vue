<template>

<div>
  <dir>
<input v-model="firstName" type="text" placeholder="firstName" />
<input v-model="lastName" type="text" placeholder="lastName" />
  </dir>
  <div>
      {{fullNameMethod()}}
      <!-- {{fullNameComputed}} -->
  </div>
  
  <div>

  <button @click="run()">click</button>
  <button @click="a++"> method A</button>
  <button @click="b++"> method B</button>
  <div>
    {{methodA()}}
    {{methodB()}}
  </div>

  <div>
    {{computedA}}
    {{computedB}}
  </div>
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
      mathData:Math.random(),
      data:'cool naim',
      firstName:'',
      lastName:'',
      yo:'yo man',
      a:0,
      b:0,
      age:20

    } 
 },
 methods:{
   
     randomMethod:function () {
               return this.data;  
     },
     run:function () {
       console.log('run method');
       
                this.data='yo man';
      },
      fullNameMethod(){
            return  this.firstName +' '+this.lastName+" "+this.yo ;
      },
      testMethod(){
         console.log('test method');
         return this.firstName +' ' +this.yo
                 
      },

      methodA(){
        console.log('method A');
        
        this.a+this.age
      },

      methodB(){
        console.log('method B');
        
        this.b+this.age
      }



 }
 ,
 computed:{
     
     myComputed:function () {
        return this.data; 
     },

     fullNameComputed(){
       return  this.firstName +' '+this.lastName ;

     },
    
      computedA(){
        console.log('computed A');
        
        this.a+this.age
      },
    computedB(){
        console.log('computed B');
        
        this.b+this.age
      }
 },
 watch:{
      value:function (e) {
         console.log('value changed',e);
          
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
