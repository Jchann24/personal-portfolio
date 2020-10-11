<template>
  <div class="bg-image">
    <img
      src="https://images.unsplash.com/photo-1550439062-609e1531270e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80"
      class="img-fluid hero-image"
      alt="Sample"
    />
    <div class="mask" style="background-color: rgba(0, 0, 0, 0.8);">
      <div class="d-flex justify-content-center align-items-center h-100">
        <vue-typed-js
          :loop="true"
          :back-speed="20"
          :strings="[
            `<span>Hello, my name is</span>`,
            `&lt;<span style='color: #F286C4;'> JSON </span>/&gt;`,
            `<span>I'm a full stack web developer.</span>`
          ]"
          :content-type="'html'"
        >
          <h2 class="typing"></h2>
        </vue-typed-js>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero'
}
</script>

<style scoped>
.hero-image {
  width: 100%;
  height: 100vh;
  object-fit: cover;
  object-position: center;
}
</style>
