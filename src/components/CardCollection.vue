<template>
  <section>
      <a href="#"><img :src="require(`@/assets/${dettagli.img}`)" :alt="dettagli.img"></a>
      <a href="#"><h4 class="mt-2 mb-2 p-2">{{dettagli.title}}</h4></a>
  </section>
</template>

<script>
export default {
    name: 'CardCollection',
    props:["dettagli"]
}
</script>

<style lang="scss" scoped>
img{
    width: 100px;
}
a{
    text-decoration: none;
    color: black;
    h4{
        font-size: 16px;
        text-transform: uppercase;

        &:hover{
            background-color: #FC7523;
            color: white;
        }
    }
}
</style>