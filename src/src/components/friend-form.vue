<template>
  <div class="friend-form">
    <input type="firstname" placeholder="First Name" v-model="firstname">
    <input type="lastname" placeholder="Last Name" v-model="lastname">
    <input type="comment" placeholder="Comment" v-model="comment">
    <br>
    <button @click="add" class="btn">ADD</button>
  </div >
  <Frinedcard :friends="friends"/>
</template>

<script>
import Frinedcard from "./friend-card.vue"
export default {
  components:{
    Frinedcard,
  },
  data(){
      return {
        firstname:"",
        lastname:"",
        comment :"",
        friends: [],
      }
    },

  methods:{
    add(){
      let friendList = {};
      friendList.firstname = this.firstname.toUpperCase();
      friendList.lastname = this.lastname.toUpperCase();
      friendList.comment = this.comment;
      if(this.firstname!="" && this.lastname!="" && this.comment!=""){
        this.friends.push(friendList)
      }
      this.firstname = "" ;
      this.lastname = "" ;
      this.comment = "";
    }
  }
}
</script>

<style>
    .friend-form{
        width:60%;
        margin:0 auto;
        align-items: center;
        justify-content: center;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 50px 100px -20px, rgba(0, 0, 0, 0.3) 0px 30px 60px -30px, rgba(10, 37, 64, 0.35) 0px -2px 6px 0px inset;
    }
    input,.btn{
        width:80%;
        margin:4px;
        height:30px;
        align-items: center;
    }
    .btn{
        width:82%;
        height:35px;
        background: hsl(193, 36%, 57%);
        border:none;
        border-radius:4px;
    }
</style>