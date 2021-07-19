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
  </section>
</template>

<script>
export default {
    name: 'Jambotrom'
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
</style>