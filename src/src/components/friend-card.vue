<template>
  <div class="card" v-for="friend in friends" :key="friend">
    <div class="friendp-card">
        <h3>{{friend.firstname}} {{friend.lastname}}</h3>
    </div>
     <div class="friendp-card">
        <p>{{friend.comment}}</p>
    </div>
  </div>
</template>

<script>
export default {
    props:[
        "friends"
    ]
    
}
</script>

<style>
    .card{
        width:60%;
        margin:0 auto;
        padding: 1.5px;
        margin-top:8px; 
        box-shadow: rgba(174, 174, 183, 0.25) 0px 50px 100px -20px, rgb(222, 219, 219) 0px 30px 60px -30px, rgba(181, 187, 194, 0.781) 0px -2px 6px 0px inset;
    }
    .friendp-card{
        display: flex;
        justify-content: flex-start;  
    }
    h3,p{
        padding-left: 10px;
    }
</style>
