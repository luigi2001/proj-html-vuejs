<template>
    <footer class="bg-white">
        <section class="mt-5 container p-5">
          <div class="row">
            <div class="logo col-3 border-end text-center">
              <a href="#"><img :src="require('@/assets/avada-food-logo-mob.png')" alt="logo ava food"></a>
                <div class="social mt-5">
                   <a href="#"><i class="fab fa-facebook-f me-3"></i></a>
                   <a href="#"><i class="fab fa-instagram me-3"></i></a>
                   <a href="#"><i class="fab fa-twitter me-3"></i></a>
                   <a href="#"><i class="fab fa-youtube me-3"></i></a>
                </div>
            </div>
          <div class="lista col-3 border-end">
              <ul>
                  <li class="mt-3" v-for="(item,index) in list" :key="index"><a href="item.url">{{item.text}}</a></li>
              </ul>
          </div>
          <div class="contatti col-3 border-end">
              <h6>contact</h6>
              <ul>
                  <li class="mt-3"><i class="fas fa-map-marker-alt"></i> <span>775 New York Ave, Brooklyn, Kings, New York 11203</span></li>
                  <li class="mt-3"><i class="fas fa-phone"></i> <span><a href="#">+ 0100-505-0000</a></span></li>
                  <li class="mt-3"><i class="fas fa-envelope"></i> <span><a href="#">info@your-domain.com</a></span></li>
              </ul>
          </div>
          <div class="app col-3">
              <h6>get our app!</h6>
              <a href="#"><img class="mt-3" :src="require('@/assets/download-android.png')" alt="logo google play"></a>
              <a href="#"><img class="mt-3" :src="require('@/assets/download-app-store.png')" alt="logo app store"></a>
          </div>
         </div>
        </section>
    </footer>
</template>

<script>
import list from '@/data/Arrayfooter.js';
export default {
    name: 'Footer',
    data(){
        return{
            list: list
        }
    }
}
</script>

<style lang="scss" scoped>
footer{
    height: 350px;
    .logo{
        .social{
            a{
                color: #9C9894;
            }
        }
    }
    ul{
        list-style: none;
        li{
            a{
            text-decoration: none;

            &:hover{
                color: #FC7523;
            }
            }
        }
    }    
    .lista{
        a{
            color: black;
        }
    }
    h6{
        text-transform: uppercase;
        color: #FC7523;
    }
    .contatti{
        li{
            color: gray;
            a{
                color: gray;
            }
        }
    }
}
</style>