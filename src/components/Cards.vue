<template>
  <div class="container">
    <div class="row">
      <div class="col-12 col-md-6 col-lg-6 col-xl-4" v-for="card in cards" v-bind:key="card.CodigoAtendimento">
        <div
          class="card text-white mb-3"
          v-bind:class="[card.Situacao == 'Aguardando' ? 'bg-danger' : card.Situacao == 'Encaminhado' ? 'bg-success' : 'bg-secondary']"
          style="max-width: 30rem;"
          v-on:click="clickOnCard(card)"
        >
          <div class="card-header">{{card.Situacao}}</div>
          <div class="card-body">
            <h5 class="card-title">{{card.Titulo}}</h5>
            <p class="card-text">{{ card.Descricao }}</p>
            <p class="card-text">{{ card.DataSolicitacao }}</p>
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
      cards: [
        {
          CodigoAtendimento: 1,
          Titulo: "Titulo do atendimento",
          Descricao: "Descrição do atendimento",
          Situacao: "Aguardando",
          DataSolicitacao: Date()
        },
        {
          CodigoAtendimento: 2,
          Titulo: "Titulo do atendimento2",
          Descricao: "Descrição do atendimento2",
          Situacao: "Aguardando",
          DataSolicitacao: Date()
        },
        {
          CodigoAtendimento: 3,
          Titulo: "Titulo do atendimento3",
          Descricao: "Descrição do atendimento3",
          Situacao: "Encaminhado",
          DataSolicitacao: Date()
        },
        {
          CodigoAtendimento: 4,
          Titulo: "Titulo do atendimento4",
          Descricao: "Descrição do atendimento4",
          Situacao: "Encaminhado",
          DataSolicitacao: Date()
        },
        {
          CodigoAtendimento: 5,
          Titulo: "Titulo do atendimento5",
          Descricao: "Descrição do atendimento5",
          Situacao: "Finalizado",
          DataSolicitacao: Date()
        },
        {
          CodigoAtendimento: 6,
          Titulo: "Titulo do atendimento6",
          Descricao: "Descrição do atendimento6",
          Situacao: "Finalizado",
          DataSolicitacao: Date()
        }
      ]
    };
  },
  methods: {
    clickOnCard(card) {
      alert(`Clicou no card ${card}`);
    }
  }
};
</script>