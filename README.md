<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Restaurant Menu</title>
  <script src="https://cdn.jsdelivr.net/npm/vue@3/dist/vue.global.js"></script>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://unpkg.com/aos@2.3.4/dist/aos.css" rel="stylesheet">
  <style>
    body {
      font-family: 'Inter', sans-serif;
    }
  </style>
</head>
<body class="bg-gray-100">
  <div id="app" class="min-h-screen bg-gray-100">
    <!-- Categories -->
    <div v-if="view === 'categories'" class="p-6 space-y-6">
      <div
        v-for="category in categories"
        :key="category.name"
        class="bg-white rounded-lg shadow-lg overflow-hidden cursor-pointer"
        @click="loadProducts(category.name)"
        data-aos="fade-up"
        data-aos-duration="600"
      >
        <img :src="category.image" :alt="category.name" class="w-full h-40 object-cover">
        <div class="p-4">
          <h2 class="text-lg font-bold capitalize">{{ category.name }}</h2>
        </div>
      </div>
    </div>

    <!-- Products List -->
    <div v-else-if="view === 'products'" class="p-6 space-y-6">
      <button @click="backToCategories" class="mb-4 bg-red-500 text-white py-2 px-4 rounded-lg">
        Înapoi la Categorii
      </button>
      <div
        v-for="product in currentProducts"
        :key="product.title"
        class="bg-white rounded-lg shadow-lg overflow-hidden cursor-pointer"
        @click="showProductDetails(product)"
        data-aos="fade-up"
        data-aos-duration="600"
      >
        <img :src="product.image" :alt="product.title" class="w-full h-40 object-cover">
        <div class="p-4">
          <h2 class="text-lg font-bold">{{ product.title }}</h2>
          <p class="text-red-500 font-bold">{{ product.price }}</p>
        </div>
      </div>
    </div>

    <!-- Product Details -->
    <div v-else-if="view === 'details'" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center">
      <div class="bg-white rounded-lg shadow-lg w-11/12 sm:w-3/4 lg:w-1/2">
        <div class="relative">
          <button
            class="absolute top-4 right-4 text-gray-500 text-2xl"
            @click="view = 'products'"
          >
            &times;
          </button>
          <img :src="currentProduct.image" :alt="currentProduct.title" class="w-full h-64 object-cover">
        </div>
        <div class="p-6">
          <h2 class="text-xl font-bold mb-2">{{ currentProduct.title }}</h2>
          <p class="text-red-500 text-lg font-bold mb-2">{{ currentProduct.price }}</p>
          <p class="text-gray-700 text-sm mb-4">{{ currentProduct.description }}</p>
          <button class="bg-red-500 text-white py-2 px-4 rounded-lg" @click="view = 'products'">
            Închide
          </button>
        </div>
      </div>
    </div>
  </div>

  <!-- Include AOS Library -->
  <script src="https://unpkg.com/aos@2.3.4/dist/aos.js"></script>

  <script>
    // Initialize AOS
    AOS.init();

    // Vue App
    const app = Vue.createApp({
      data() {
        return {
          view: 'categories',
          categories: [
            { name: 'brunch', image: 'https://i.giphy.com/9qZEmFR8fs7CrCgy4T.webp' },
            { name: 'soups', image: 'https://bistropoint.ro/wp-content/uploads/2021/12/Ciorba-de-Burta-380gr.jpg' },
            { name: 'pasta', image: 'https://i.giphy.com/dZRlFW1sbFEpG.webp' },
            { name: 'main', image: 'https://i.giphy.com/NRS40PZGqScW4Tm2F5.webp' },
            { name: 'desserts', image: 'https://i.giphy.com/L2mf2cMkd2m7BJCjX7.webp' },
          ],
          products: {
            brunch: [
              { title: 'Avocado Toast', description: 'Avocado, toast, ouă poșate, roșii cherry.', price: '25 Lei', image: 'https://i.giphy.com/9qZEmFR8fs7CrCgy4T.webp' },
              { title: 'Eggs Benedict', description: 'Ouă poșate, sos hollandaise, șuncă.', price: '30 Lei', image: 'https://i.giphy.com/X3E37CTy55jNK.webp' },
              { title: 'Pancakes', description: 'Clătite, sirop de arțar, fructe proaspete.', price: '20 Lei', image: 'https://i.giphy.com/5zu5JovduWFBS.webp' },
            ],
            soups: [
              { title: 'Ciorbă de burtă', description: 'Tradițională, smântână, ardei iute.', price: '18 Lei', image: 'https://bistropoint.ro/wp-content/uploads/2021/12/Ciorba-de-Burta-380gr.jpg' },
              { title: 'Supă cremă de roșii', description: 'Roșii proaspete, crutoane, busuioc.', price: '15 Lei', image: 'https://www.lalena.ro/images/uploaded/600x_Supa-crema-de-rosii-108.jpg' },
              { title: 'Ciorbă de legume', description: 'Legume proaspete, zeamă de lămâie.', price: '12 Lei', image: 'https://www.prestij.ro/uploads/produse/1440/94--ciorba-taraneasca-de-legume.jpg' },
            ],
            pasta: [
              { title: 'Spaghetti Carbonara', description: 'Spaghetti, bacon, parmezan, ouă.', price: '28 Lei', image: 'https://i.giphy.com/dZRlFW1sbFEpG.webp' },
              { title: 'Penne Arrabbiata', description: 'Penne, sos de roșii picant, usturoi.', price: '25 Lei', image: 'https://i.giphy.com/f0N7csaAc6t60OmXkm.webp' },
              { title: 'Tagliatelle Alfredo', description: 'Tagliatelle, sos Alfredo, pui.', price: '30 Lei', image: 'https://i.giphy.com/xOML6s8aBmAtlLwujM.webp' },
            ],
            main: [
              { title: 'Muschiuleț de porc', description: 'Muschiuleț, cartofi copți, mozzarella, bacon.', price: '45 Lei', image: 'https://i.giphy.com/NRS40PZGqScW4Tm2F5.webp' },
              { title: 'Tomahawk porc', description: 'Carne de porc, cartofi, sos brun.', price: '41 Lei', image: 'https://i.giphy.com/KDskfOILt91T2.webp' },
              { title: 'Ceafă sfărâmată', description: 'Ceafă, piure de cartofi, ardei copți.', price: '36 Lei', image: 'https://i.giphy.com/l378puWI9Fpi4OApO.webp' },
            ],
            desserts: [
              { title: 'Tiramisu', description: 'Prăjitură italiană cu cafea, mascarpone.', price: '20 Lei', image: 'https://i.giphy.com/L2mf2cMkd2m7BJCjX7.webp' },
              { title: 'Pavlova', description: 'Bezea, frișcă, fructe de pădure.', price: '18 Lei', image: 'https://i.giphy.com/iiwu9bTOZ1HiM.webp' },
              { title: 'Cheesecake', description: 'Cheesecake cu dulceață de căpșuni.', price: '22 Lei', image: 'https://i.giphy.com/Xi2UAW7kTQvHa.webp' },
            ],
          },
          currentProducts: [],
          currentProduct: null,
        };
      },
      methods: {
        loadProducts(category) {
          this.currentProducts = this.products[category];
          this.view = 'products';
        },
        showProductDetails(product) {
          this.currentProduct = product;
          this.view = 'details';
        },
        backToCategories() {
          this.view = 'categories';
        },
      },
    });

    app.mount('#app');
  </script>
</body>
</html>
