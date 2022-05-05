<template>
  <div class="example">
      {{ message }}
      <img class="helloimg" src="https://images.vectorhq.com/images/previews/1ba/bart-and-lisa-psd-446281.png" />
  </div>
</template>

<script>
export default {
  name: 'example',
  props: {
    message: String,
  },
  // data: () => ({
  //   message: 'Soy el componente Example'
  // })
}
</script>

<style>
.example {
  display: flex;
  flex-flow: column nowrap;
  padding: 100px 0 0 0;
}

.helloimg {
  width: 25%;
  height: 25%;
}
</style>