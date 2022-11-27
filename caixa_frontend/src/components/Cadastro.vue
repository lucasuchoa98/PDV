<template>
    <div>
      <v-form v-model="valid">
        <v-container>
          <v-row>
            <v-col cols="12" md="4">
              <v-text-field v-model="nome" :counter="10" label="Nome do produto" required></v-text-field>
            </v-col>
            <v-col cols="12" md="4">
              <v-text-field v-model="descricao" :counter="10" label="Descrição" required></v-text-field>
            </v-col>
            <v-col cols="12" md="4">
              <v-text-field v-model="preco" label="Preço" prefix="R$" type="number" required></v-text-field>
            </v-col>
            <v-checkbox
              v-model="disponivel"
              label="Disponível?"
            ></v-checkbox>
            <v-btn
              :disabled="!valid"
              color="success"
              class="mr-4"
              @click="validate"

              v-on:click="addItem"
            >
              Cadastrar
            </v-btn>
          </v-row>
        </v-container>
      </v-form>
    </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'CadastroComponent',
  data: () => ({
    nome:"",
    descricao:"",
    preco:0,
    disponivel:false
  }),
  methods:{
    async addItem(){
      let result = await axios.post("http://127.0.0.1:8000/itens/",{
        nome:this.nome,
        descricao:this.descricao,
        preco:this.preco,
        disponivel:this.disponivel
      })
      console.log(result)
    }
  }
}
</script>