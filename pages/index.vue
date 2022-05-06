<template>
  <div>
    <section class="hero-section reference">
      <div class="container-1140">
        Something
      </div>
    </section>
  </div>
</template>

<script>
export default {
  async asyncData({$http, params}) {
    const references = await $http.$get(`https://v2.jokeapi.dev/joke/Any?safe-mode`)

    return {
      references: references
    }
  },
}
</script>