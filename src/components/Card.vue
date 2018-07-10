<template>
    <div class="card">
        <div >
            <img class="cardmedia" :src="imgUrl"/>
        </div>
        <div class="cardcontent">
            {{rname}}
        </div>
    </div>
</template>

<script>

export default {
  name: 'Card',
  props: {
      rname: String,
      imgUrl: String
  }

}
</script>

<style scoped>

.card {

}
.cardmedia {
    width: 50px;
    height: 50px;
    border-radius: 5px;
    margin: auto;
    margin-top: 10px;

}

.cardcontent {

}
</style>
