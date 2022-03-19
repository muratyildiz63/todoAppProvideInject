<template>
  <input
    type="text"
    placeholder="Text Giriniz"
    @keydown.enter="insert"
    class="col-12"
  />
</template>

<script>
export default {
   inject:["insert"]
};
</script>