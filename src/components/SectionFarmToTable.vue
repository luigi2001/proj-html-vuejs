<template>
  <section>
        <h3 class="mt-5 mb-3">FARM TO TABLE</h3>
        <button class="float-end p-2 border-0">Read our blog <i class="fas fa-map-marked"></i> </button>
        <p>Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.</p>
        <div class="row mt-5">
            <div class="col-8">
                <div class="box bg-white">
                    <img @mouseover="hover = true" @mouseleave="hover = false" :src="require('@/assets/single-post-img3.jpg')" alt="post img3">
                    <div class="hover text-center" v-if="hover">
                       <i class="fas fa-link bg-white p-3 rounded-circle"></i>
                       <h3>Food Corner: Top Japanese Restaurants for Sushi</h3>
                    </div>
                    <div class="descrizione p-4">
                        <h3>Food Corner: Top Japanese Restaurants for Sushi</h3>
                        <p class="border-bottom pb-3">By <span>admin</span>|March 25th, 2019</p>
                        <p>Suspendisse at semper odio. Nam fringilla scelerisque tincidunt. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec tincidunt posuere ornare. Phasellus placerat odio non feugiat sollicitudin. Integer vitae elementum ex.</p>
                        <h6>Read More ></h6>
                    </div>
                </div>
                <div class="row mt-5">
                    <div class="col-6 p-3" v-for="(item,index) in ArrayCardFarm" :key="index">
                        <div class="card rounded-0 border-0">
                            <CardJambo :dettagli="item"/>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-4"></div>
        </div>
  </section>
</template>

<script>
import CardJambo from '@/components/CardJambo.vue';
import ArrayCardFarm from '@/data/ArrayCardFarm.js'
export default {
    name: 'SectionFarmToTable',
    components:{
        CardJambo
    },
    data(){
        return{
            ArrayCardFarm: ArrayCardFarm,
            hover: false
        }
    }
}
</script>

<style lang="scss" scoped>
button{
    text-transform: uppercase;
    background-color: #FC7523;
    color: white;
}
.box{
    position: relative;
    img{
        width: 100%;
        height: 50%;
    }
    .descrizione{
        h3{
            cursor: pointer;

            &:hover{
                color: #FC7523;
            }
        }
        p{
            span{
                cursor: pointer;

                &:hover{
                    color: #FC7523;
                }
            }
        }
        h6{
            &:hover{
                cursor: pointer;
                color: #FC7523;
            }
        }
    }
}
.hover{
    font-size: 50px;
    position: absolute;
    left: 50%;
    top: 25%;
    transform: translate(-50%,-25%);
    h3{
        cursor: pointer;
        font-size: 16px;
        color: white;
    }
}
</style>