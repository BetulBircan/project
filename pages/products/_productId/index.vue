<template>
    <div class="container">
      <h3 class="title">Ürün Özeti</h3>
      <p class="subtitle"> Ürün ID Bilgisi : {{ $route.params.productId }}</p>
  
      <div class="button-container">
          <nuxt-link  to="/products" tag="a" class="button--green">Geri Dön</nuxt-link>
          <button @click="showEdit" class="button--green">Düzenle</button>
      </div>
    </div>
  </template>
  <script>
      export default {
          data() {
              return {
                  productId : null
              }
          },
          methods : {
              showEdit() {
                  this.$router.push(+ this.$route.params.productId + "/edit/" )
              }
          }
      }
  </script>
  <style scoped>
    .title {
      font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
      'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
      display: block;
      font-weight: 300;
      font-size: 100px;
      color: #35495e;
      letter-spacing: 1px;
    }
  
    .subtitle {
      margin-top: 10px;
      font-weight: 300;
      font-size: 42px;
      color: #526488;
      word-spacing: 5px;
      padding-bottom: 15px;
    }
    .container {
      min-height: 100vh;
      text-align: center;
      margin-top: 50px;
    }
    .button-container{
      margin-top: 50px;
      border: 1px solid #392;
      background-color: #dedede;
      padding: 10px;
      box-shadow: 2px 3px 8px rgba(0,0,0,.1);
      display: flex;
      justify-content: center;
    }
  </style>
  
  