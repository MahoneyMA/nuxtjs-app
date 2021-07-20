<template>
  <div class="flex flex-col bg-black pb-2.5">
    <NavBar/>
    <div class="display">
      <img
        src="~/assets/me.jpg"
        height=144
        width=144
        alt="Matthew Mahoney"
        class="rounded-full"
      >
      <h1 class="text-4xl font-bold">Matthew Mahoney</h1>
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
