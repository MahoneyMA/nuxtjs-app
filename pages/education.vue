<template>
  <div>
    <div class="container">
      <h1>Education</h1>
      <img
        src="~/assets/diploma.jpg"
        height="40%"
        width="40%"
        :alt=name
      >
      </img>
      <p>
        You can validate the diploma by clicking
        <a
          href="https://registrar.vanderbilt.edu/cecredential/validate.php"
          target="_blank"
          rel="noopener noreferrer"
        >
          here
        </a>
        and entering the code
        <u id="code" type="text">191X-MQ4L-MGYH</u>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Education',
  data () {
    return {
      name: 'Matthew\'s Diploma',
      title: 'Matthew Mahoney | Education'
    }
  },
  head () {
    return {
      title: this.title
    }
  },
  methods: {
    copyToClipboard: () => {
      const el = document.createElement('textarea')
      el.value = '191X-MQ4L-MGYH'
      el.setAttribute('readonly', '')
      el.style.position = 'absolute'
      el.style.left = '-9999px'
      document.body.appendChild(el)
      el.select()
      document.execCommand('copy')
      document.body.removeChild(el)
    }
  }
}
</script>

<style scoped>
.container{
  display:flex;
  flex-direction:column;
  text-align:center;
  align-items:center;
}
</style>
