<template>
  <section>
    <div class="jambotrom">
        <div class="titolo text-center p-5 rounded">
            <div class="etichetta p-2 rounded">
                <span>today's pick</span>
            </div>
          <a href="#"><h1>Food Corner: Top Japanese Restaurants for Sushi</h1></a>
          <h5>March 25, 2019</h5>
        </div>
    </div>
    <div class="cardcontainer">
        <div class="card container p-5 border-0 rounded-0">
          <div class="row text-center">
            <h3>FOODIE JOURNAL</h3>
            <div class="col-4 mt-3" v-for="(item,index) in ArrayCard" :key="index">
                <CardJambotrom :dettagli="item"/>
            </div>
          </div>
        </div>
    </div>
  </section>
</template>

<script>
import CardJambotrom from '@/components/CardJambo.vue';
import ArrayCard from '@/data/ArrayCardJumbo.js'
export default {
    name: 'Jambotrom',
    components:{
        CardJambotrom
    },
    data(){
        return{
            ArrayCard: ArrayCard
        }
    }
}
</script>

<style lang="scss" scoped>
.jambotrom{
    height: 600px;
    background-image: url('~@/assets/single-post-img3.jpg');
    background-position: center;
    background-size: cover;
    position: relative;

    .titolo{
        width: 600px;
        background-color: white;
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%,-50%);

        a{
            text-decoration: none;
            color: black;

            &:hover{
                color: #FC7523;
            }
        }

        h5{
            color: gray;
        }

        .etichetta{
            width: 150px;
            background-color: #FC7523;
            color: white;
            text-transform: uppercase;
            position: absolute;
            left: 40%;
            bottom: 95%;
        }
    }
}
.cardcontainer{
    height: 600px;
    .card{
    position: absolute;
    top: 800px;
    left: 50%;
    transform: translate(-50%);
    }
}
</style>