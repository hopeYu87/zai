<script setup lang="ts">
const product: any[] = []
const newsletter: string = ref('');
const basket = useState('basket', () => product)
const products = ref([
  {
    id: 1,
    img: 'http://localhost:3000/images/p1.png',
    name: 'Ring',
    price: '$200',
    new: true
  },
  {
    id: 2,
    img: 'http://localhost:3000/images/p2.png',
    name: 'Watch',
    price: '$300',
    new: true
  },
  {
    id: 3,
    img: 'http://localhost:3000/images/p3.png',
    name: 'Teddy Bear',
    price: '$95',
    new: true
  },
  {
    id: 4,
    img: 'http://localhost:3000/images/p4.png',
    name: 'Flower Bouquet',
    price: '$45',
    new: true
  },
  {
    id: 5,
    img: 'http://localhost:3000/images/p5.png',
    name: 'Teddy Bear',
    price: '$95',
    new: false
  },
  {
    id: 6,
    img: 'http://localhost:3000/images/p6.png',
    name: 'Flower Bouquet',
    price: '$70',
    new: true
  },
  {
    id: 7,
    img: 'http://localhost:3000/images/p7.png',
    name: 'Watch',
    price: '$400',
    new: true
  },
  {
    id: 8,
    img: 'http://localhost:3000/images/p8.png',
    name: 'Ring',
    price: '$450',
    new: true
  }
])

const addToBasket = (product) => {
  basket.value.push(product)
  console.log(basket.value)
}

console.log(products.value)
console.log(basket.value)
</script>

<template>
  <div>
    <section class="slider_section">
      <div class="slider_container">
        <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
          <div class="carousel-inner">
            <div class="carousel-item active">
              <div class="container-fluid">
                <div class="row">
                  <div class="col-md-7">
                    <div class="detail-box">
                      <h1>
                        Welcome To Our <br>
                        Gift Shop
                      </h1>
                      <p>
                        Sequi perspiciatis nulla reiciendis, rem, tenetur impedit, eveniet non necessitatibus error distinctio mollitia suscipit. Nostrum fugit doloribus consequatur distinctio esse, possimus maiores aliquid repellat beatae cum, perspiciatis enim, accusantium perferendis.
                      </p>
                      <a href="">
                        Contact Us
                      </a>
                    </div>
                  </div>
                  <div class="col-md-5 ">
                    <div class="img-box">
                      <img src="~/assets/images/slider-img.png" alt="" />
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="carousel-item ">
              <div class="container-fluid">
                <div class="row">
                  <div class="col-md-7">
                    <div class="detail-box">
                      <h1>
                        Welcome To Our <br>
                        Gift Shop
                      </h1>
                      <p>
                        Sequi perspiciatis nulla reiciendis, rem, tenetur impedit, eveniet non necessitatibus error distinctio mollitia suscipit. Nostrum fugit doloribus consequatur distinctio esse, possimus maiores aliquid repellat beatae cum, perspiciatis enim, accusantium perferendis.
                      </p>
                      <a href="">
                        Contact Us
                      </a>
                    </div>
                  </div>
                  <div class="col-md-5 ">
                    <div class="img-box">
                      <img src="~/assets/images/slider-img.png" alt="" />
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="carousel-item ">
              <div class="container-fluid">
                <div class="row">
                  <div class="col-md-7">
                    <div class="detail-box">
                      <h1>
                        Welcome To Our <br>
                        Gift Shop
                      </h1>
                      <p>
                        Sequi perspiciatis nulla reiciendis, rem, tenetur impedit, eveniet non necessitatibus error distinctio mollitia suscipit. Nostrum fugit doloribus consequatur distinctio esse, possimus maiores aliquid repellat beatae cum, perspiciatis enim, accusantium perferendis.
                      </p>
                      <a href="">
                        Contact Us
                      </a>
                    </div>
                  </div>
                  <div class="col-md-5 ">
                    <div class="img-box">
                      <img src="~/assets/images/slider-img.png" alt="" />
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="carousel_btn-box">
            <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
              <i class="fa fa-arrow-left" aria-hidden="true"></i>
              <span class="sr-only">Previous</span>
            </a>
            <img src="~/assets/images/line.png" alt="" />
            <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
              <i class="fa fa-arrow-right" aria-hidden="true"></i>
              <span class="sr-only">Next</span>
            </a>
          </div>
        </div>
      </div>
    </section>
    <section class="shop_section layout_padding">
      <div class="container">
        <div class="heading_container heading_center">
          <h2>
             Products
          </h2>
        </div>
        <div class="row">

          <div class="col-sm-6 col-md-4 col-lg-3" v-for="(value, index) in products" :key="index">
            <div class="box">
                <div class="img-box">
                  <img :src="value.img" alt="">
                </div>
                <div class="detail-box">
                  <h6>
                    {{ value.name }}
                  </h6>
                  <h6>
                    Cena:
                    <span>
                    {{ value.price }}
                  </span>
                  </h6>
                </div>
                <div class="new" v-if="value.new">
                <span>
                  Nowość
                </span>
                </div>
                <button @click="addToBasket(value)" type="button">
                  Add to basket
                </button>
              <button @click="counter++">
                +
              </button>
              <button @click="counter--">
                -
              </button>
            </div>
          </div>


        </div>
      </div>
      {{ newsletter}} <br/>
      <input v-model="newsletter">
      <button @click="console.log(newsletter)">Zapisz</button>
    </section>
  </div>

</template>

<style scoped>

</style>