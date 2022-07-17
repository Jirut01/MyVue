<template>
  <section>
<form @submit.prevent="saveData">
  <label>ป้อนเพศ:</label>
  <input type="text" v-on:input="setgender"><br/>
  <button type="submit">บันทึก</button>
<br/></form>
<form @submit.prevent="saveDataname">
   <label>ป้อนชื่อ:</label>
  <input type="text" ref="Nm"><br/>
  <button type="submit">บันทึก</button>
  </form>

    <h1>{{name}}</h1>
    <br/>
    <h1>{{aeg}}</h1>
    <button @click="showdata">แจ้งเตือน</button>
    <br/>
    <p>เพศ : {{gender}}</p>
    <button @click="increat">เพิ่ม</button>
    <button @click.middle="increatt(10)">เพิ่มทีละสิบ</button>  //คลิกเม้ากลาง
  </section>
  
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      name:"่jirut",
      nickname:"ball",
      aeg:20,
      gender:""
    }
  },
  methods:{
    showdata(){
      alert(this.name + this.nickname)
    },
    setgender(event){
      this.gender=event.target.value
    },
    increat(){
      this.aeg++
    },
     increatt(value){
      this.aeg+=value
    },
    saveData(e){
      e.preventDefault();
      alert("บันทึกเรียบร้อย");
    },
     saveDataname(){
    this.name=this.$refs.Nm.value;
  }
  
}
}
</script>

<style>
</style>
