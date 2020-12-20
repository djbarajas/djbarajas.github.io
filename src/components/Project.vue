<template>
  <div class="columns is-vcentered is-centered">
    <div class="column">
  <div class="card mx-5">
    <div class="card-content">
      <div class="media is-block-mobile">
        <div class="media-left mb-5">
          <figure class="image is-50x50">
            <img :src="image" style="max-width: 200px; margin: auto;">
          </figure>
        </div>
          <div class="content">
          <p class="title is-4">{{ title }}</p>
          <slot name="text"></slot>
          </div>
        </div>
    </div>
  </div>
  </div>
  </div>
</template>

<script>
export default {
  name: 'Project',
  props: {
    title: String,
    image: String,
  },
};
</script>

<style scoped>

</style>
