<template>
  <div id="myTopNav" class="topnav">
    <div class="navigation">
      <NuxtLink to="/">
        Home page
      </NuxtLink>
      <NuxtLink to="/education">
        Education
      </NuxtLink>
      <NuxtLink to="/interests">
        Interests
      </NuxtLink>
    </div>
    <div class="links">
      <a href="https://www.linkedin.com/in/mahoney-matthew">
        <img
          src="~/assets/linkedin-logo.png"
          height="40"
          width="40"
        >
        </img>
      </a>
      <a href="https://github.com/MahoneyMA">
        <img
          src="~/assets/github-logo.png"
          height="40"
          width="40"
        >
        </img>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavBar'
}
</script>

<style>
.topnav{
  display: block;
}
.navigation a{
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 5px 16px;
  text-decoration: none;
  font-size: 17px;
  transition: .3s;
}
.navigation a:hover {
  background-color: #ddd;
  color: black;
}
.links{
  float: right;
  border-right :none;
}
.links a {
  padding: 5px 5px;
}
</style>
