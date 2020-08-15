<template>
  <div class="modal-container">
    <div>
      <div class="pl-2 pt-2">
        <span style="font-size: 20px">Some Title</span>
        <span
          class="float-right pr-3"
          style="cursor:pointer;"
          @click="$emit('close')"
        >
          <strong>x</strong>
        </span>
      </div>
    </div>

    <div class="row pt-5 scaled-images">
      <div
        v-for="index in 5"
        :key="index"
      >
        <div class="col-md-5 col-12 mb-5">
          <img src="https://source.unsplash.com/random/2X2">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.scaled-images {
  transform: scale(0.5);
  transform-origin: 0 0;
  width: 240%;
  height: 50%;
}

.modal-container {
  overflow-y: auto !important;
  padding: 20px;
  height: 600px;
  overflow-x: hidden;
}
</style>