<template>
  <div class="container">
    <div class="row" >
      <div class="col-12 col-sm-6 col-md-4 col-lg-3 justify-content-center"  v-for="card in cards"
          v-bind:key="card">
        <div
          class="card text-white bg-primary mb-3" style="max-width: 18rem;">
          <div class="card-header">Header</div>
          <div class="card-body">
            <h5 class="card-title">Primary card title</h5>
            <p class="card-text">{{ card }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Cards",
  data: function() {
    return {
      cards: ["Descrição 1", "Descrição 2", "Descrição 3", "Descrição 4",
      "Descrição 5", "Descrição 6", "Descrição 7", "Descrição 8", "Descrição 9", "Descrição 10"]
    };
  },
  methods: {}
};
</script>