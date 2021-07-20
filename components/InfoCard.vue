<template>
  <div class="flex items-center justify-center">
    <figure class="relative max-w-xs cursor-pointer">
      <img class=" shadow-xl hover:shadow-2xl hover:opacity-50 duration-300" :src=image>
      <figcaption class="absolute text-lg -mt-16 text-white px-4">
        <div>
          <h1><b>{{ title }}</b></h1>
        </div>
        <div>
          <h1 class="h-0 hover:h-full">{{ body }}</h1>
        </div>
      </figcaption>
    </figure>
  </div>
</template>

<script>
export default {
  name: 'InfoCard',
  props: {
    image: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    body: {
      type: String,
      required: true
    }
  }
}
</script>
