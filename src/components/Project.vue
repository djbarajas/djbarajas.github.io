<template>
  <div class="columns is-vcentered is-centered">
    <div class="column">
  <div class="card mx-5">
    <div class="card-content">
      <div class="media">
        <div class="media-left">
          <figure class="image is-50x50">
            <img :src="image" style="max-width: 200px">
          </figure>
        </div>
        <div class="media-content">
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
