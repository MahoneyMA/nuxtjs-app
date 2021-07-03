<template>
  <div>
    <Header />
    <div class="container">
      <p class="heading2Xl">
        Hi I'm Matthew.
      </p>
      <p class="headingLg">
        I am a recent college graduate and aspiring sofware engineer and
        web developer. I am currently updating this website as a means of
        improving my web development skills and centralizing a place where I
        can explore and enjoy some of my hobbies.
      </p>
      <p class="headingLg">
        If you are a potential employer, You can find more details or contact
        me on
        <a href="https://www.linkedin.com/in/matthew-mahoney-4275b6190/">LinkedIn</a>
        or
        <a href="https://github.com/MahoneyMA"> Github</a>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'Matthew\'s nuxt website'
    }
  },
  head () {
    return {
      title: this.title
    }
  }
}
</script>

<style scoped>
.container {
  margin: 0 auto;
  width:70%;
  min-height: 100vh;
  display: block;
  justify-content: center;
  align-items: center;
}
.container a{
  color:inherit;
}
.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
.heading2Xl {
  font-size: max(2rem,30px);
  line-height: 1.2;
  font-weight: 800;
  letter-spacing: -0.05rem;
  margin: 1rem 0;
}

.headingXl {
  font-size: max(1.7rem, 28px);
  line-height: 1.3;
  font-weight: 800;
  letter-spacing: -0.05rem;
  margin: 1rem 0;
}

.headingLg {
  font-size: max(1.5rem,26px);
  line-height: 1.4;
  margin: 1rem 0;
}

.headingMd {
  font-size: max(1rem, 24px);
  line-height: 1.5;
}
</style>
