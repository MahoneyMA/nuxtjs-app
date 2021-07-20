<template>
  <div class="m-auto w-2/3 min-h-full flex flex-col self-center justify-center items-center">
    <span class="flex flex-row space-x-5 m-4">
    <InfoCard
      image="4.jpg"
      title="Card 1"
      body="more text"
      link="/"
    />
    <InfoCard
      image="4.jpg"
      title="Card 2"
      body="more text"
      link="/"
    />
    <InfoCard
      image="4.jpg"
      title="Card 3"
      body="more text"
      link="/"
    />
    </span>
    <p class="text-4xl font-bold tracking-normal m-4">
      Hi, I'm Matthew.
    </p>
    <p class="text-2xl tracking-normal m-4">
      I am a recent college graduate and aspiring sofware engineer and
      web developer. I am currently updating this website as a means of
      improving my web development skills and centralizing a place where I
      can explore and enjoy some of my hobbies.
    </p>
    <p class="text-2xl tracking-normal m-4">
      If you are a potential employer, You can find more details or contact
      me on
      <a href="https://www.linkedin.com/in/matthew-mahoney-4275b6190/">LinkedIn</a>
      or
      <a href="https://github.com/MahoneyMA"> Github</a>
    </p>
    <h1>Blog Posts</h1>
    <ul class="list-disc">
      <li v-for="article of articles" :key="article.slug">
        <NuxtLink :to="{ name: 'blog-slug', params: { slug: article.slug } }">
          <div>
            <h2 class="text-2xl">{{ article.title }}</h2>
            <p>{{ article.description }}</p>
          </div>
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const articles = await $content('articles')
      .only(['title', 'description', 'img', 'slug', 'author'])
      .sortBy('createdAt', 'asc')
      .fetch()
    return {
      articles
    }
  },
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
