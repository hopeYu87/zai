<script setup>
const basket = useState('basket')
const basketCount = computed(() => basket.value ? basket.value.length : '')
</script>

<template>
  <header class="header_section">
    <nav class="navbar navbar-expand-lg custom_nav-container ">
      <a class="navbar-brand" href="index.html">
          <span>
            Giftos
          </span>
      </a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class=""></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav  ">
          <li class="nav-item active">
            <NuxtLink to="/" class="nav-link">Home <span class="sr-only">(current)</span></NuxtLink>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="shop.html">
              Shop
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="why.html">
              Why Us
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="testimonial.html">
              Testimonial
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="contact.html">Contact Us</a>
          </li>
        </ul>
        <div class="user_option">
          <a href="">
            <i class="fa fa-user" aria-hidden="true"></i>
            <span>
                Login
              </span>
          </a>
          <NuxtLink to="/card">
            <i class="fa fa-shopping-bag" aria-hidden="true">{{ basketCount }}</i>
            </NuxtLink>

          <form class="form-inline ">
            <button class="btn nav_search-btn" type="submit">
              <i class="fa fa-search" aria-hidden="true"></i>
            </button>
          </form>
        </div>
      </div>
    </nav>
  </header>
  <!-- end header section -->
</template>

<style scoped>

</style>