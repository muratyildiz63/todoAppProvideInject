<template>
    <!--  <li class="box d-flex j-between"  >
      <label :for="'inputs' + items.id" class="col-12 d-flex">
        <input type="checkbox" :id="'inputs' + items.id" v-model="items.case" />
        {{ items.text }}  
      </label>
      
      <button class="fr" @click="Mdelete(items)">Sil</button>
    </li>
    -->

    <li class="box d-flex j-between"  >
      <label  class="col-12 d-flex">
        <input type="checkbox" />
        {{ items.text }}  
      </label>
      
      <button class="fr" @click="Mdelete(items)">Sil</button>
    </li>


</template>


<script>
export default {
  props: ["items"],
  inject:["Mdelete"]
}
</script>