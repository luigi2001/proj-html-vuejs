<template>
  <section>
      <h3 class="text-center mt-5">CULINARY COLLECTION</h3>
      <p class="text-center">Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.</p>
          <div class="row mt-5">
              <div class="col-3 text-center" v-for="(item,index) in ArrayCollection" :key="index">
                  <div class="bg-white mb-3 p-2">
                      <CardCollection :dettagli="item"/>
                  </div>
              </div>
          </div>
  </section>
</template>

<script>
import CardCollection from '@/components/CardCollection.vue';
import ArrayCollection from '@/data/ArrayCardCollection.js'
export default {
    name: 'SectionCulinaryCollection',
    components:{
        CardCollection
    },
    data(){
        return{
            ArrayCollection: ArrayCollection
        }
    }
}
</script>

<style lang="scss" scoped>

</style>