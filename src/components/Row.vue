<template>
    <div class="rowcontainer">
        <Card :rname="reviewer.name" :imgUrl="reviewer.imgUrl"/>
        <div class="separator">
            <i class="material-icons">arrow_back</i>
        </div>
        <Card :rname="reviewed.name" :imgUrl="reviewed.imgUrl"/>
    </div>
</template>

<script>
import Card from "./Card";

export default {
  name: "Row",
  components: {
    Card
  },
  props: {
    reviewer: Object,
    reviewed: Object
  }
};
</script>

<style>
.rowcontainer {
  display: flex;
  align-items: center;
  padding: 25px;
  width: 500px;
  justify-content: space-around;
}

.separator {
  margin: 0 25px;
}
</style>
