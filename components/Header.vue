<template>
  <div class="header">
    <NavBar/>
    <div class="display">
      <img
        src="~/assets/me.jpg"
        height=144
        width=144
        alt="Matthew Mahoney"
        class="profilePic"
      >
      <h1>Matthew Mahoney</h1>
  </div>
  </div>
</template>
<script>
import NavBar from './NavBar'
export default {
  name: 'Header',
  components: {
    NavBar
  }
}
</script>
<style>
.header{
  display: flex;
  flex-direction:column;
  background-color:black;
  border-bottom:1px;
  padding:0px 0px  10px 0px;
}
.header a{
  color:white;
  text-decoration:none;
}
.display{
  display:flex;
  flex-direction: column;
  align-items:center;
  margin: 10px;
  color:white;
}
.profilePic{
  border-radius: 9999px;
}
</style>
