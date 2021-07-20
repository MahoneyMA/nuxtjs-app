<template>
  <span id="myTopNav" class="block w-full">
    <NuxtLink to="/" class="float-left block text-white text-center px-4 py-1.5 no-underline text-lg hover:bg-gray-50 hover:text-black ease duration-300">
      Home page
    </NuxtLink>
    <NuxtLink to="/education" class="float-left block text-white text-center px-4 py-1.5 no-underline text-lg hover:bg-gray-50 hover:text-black ease duration-300">
      Education
    </NuxtLink>
    <NuxtLink to="/interests" class="float-left block text-white text-center px-4 py-1.5 no-underline text-lg hover:bg-gray-50 hover:text-black ease duration-300">
      Interests
    </NuxtLink>
      <a href="https://www.linkedin.com/in/mahoney-matthew" class="float-right">
        <img
          src="~/assets/linkedin-logo.png"
          height="40"
          width="40"
        >
        </img>
      </a>
      <a href="https://github.com/MahoneyMA" class="float-right">
        <img
          src="~/assets/github-logo.png"
          height="40"
          width="40"
        >
        </img>
      </a>
  </span>
</template>

<script>
export default {
  name: 'NavBar'
}
</script>

<style>

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
