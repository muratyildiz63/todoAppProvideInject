<template>
  <ul>
    <TudoItems
     
      v-for="item in tudoList.tudoList"
      :key="item.id"
      :items="item"
    />
  </ul>
</template>



<script>
import TudoItems from "@/components/TudoItems";
export default {
  components: {
    TudoItems,
  },

  inject: ["tudoList"],
};
</script>