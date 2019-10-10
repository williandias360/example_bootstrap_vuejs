<template>
  <div class="container">
    <div class="row">
      <div class="col-12 col-md-6 col-lg-6 col-xl-4" v-for="card in cards" v-bind:key="card">
        <div class="card text-white mb-3" v-bind:class="{'bg-danger' :aguardando, 'bg-success':encaminhado, 'bg-secondary':finalizado}" style="max-width: 30rem;" v-on:click="clickOnCard(card)">
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
      aguardando:true,
      encaminhado:true,
      finalizado:true,
      cards: [
        "Descrição 1",
        "Descrição 2",
        "Descrição 3",
        "Descrição 4",
        "Descrição 5",
        "Descrição 6",
        "Descrição 7",
        "Descrição 8",
        "Descrição 9",
        "Descrição 10",
        "Descrição 11",
        "Descrição 12",
        "Descrição 13",
        "Descrição 14",
        "Descrição 15",
        "Descrição 16",
        "Descrição 17",
        "Descrição 18",
        "Descrição 19",
        "Descrição 20",
        "Descrição 21",
        "Descrição 22",
      ]
    };
  },
  methods: {
    clickOnCard(card){
      alert(`Clicou no card ${card}`);
    }
  }
};
</script>