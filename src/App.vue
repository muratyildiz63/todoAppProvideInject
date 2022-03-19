<template>
  <div class="container">
    <TudoInput />
    <TudoList  />

    <div>{{ tudoLists.tudoList.length }} item vardır</div>
  </div>
</template>

<script>
import TudoList from "@/components/TudoList";
import TudoInput from "@/components/TudoInput";

export default {
  components: {
    TudoList,
    TudoInput,
  },

  data() {
    return {
      addItem: "",
      tudoLists: {
        tudoList: [
          {
            id: "1",
            text: "Selam vue.js",
            case: false,
          },
          {
            id: "2",
            text: "Selam vue.js",
            case: false,
          },
          {
            id: "3",
            text: "Selam vue.js",
            case: false,
          },
          {
            id: "4",
            text: "Selam vue.js",
            case: false,
          },
          {
            id: "5",
            text: "Selam vue.js",
            case: false,
          },
        ],
      },
    };
  },

  provide() {
    return {
      tudoList: this.tudoLists,
      Mdelete: this.Mdelete,
      insert: this.insert,
    };
  },

  methods: {
    Mdelete(list) {
      this.tudoLists.tudoList = this.tudoLists.tudoList.filter((t) => t != list);
    },
    insert(event) {
      var TudoVal = event.target.value;
      if (TudoVal != "") {
        this.tudoLists.tudoList.push({
          id: new Date().getTime(),
          text: TudoVal,
          case: false,
        });
        this.addItem = "";
      } else {
        alert("Bu alan Boş Bırakılamaz");
      }
    },
  },
};
</script>