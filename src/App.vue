<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer">
      <Menu />
    </v-navigation-drawer>
    <v-app-bar>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-app-bar-title>Aula 04</v-app-bar-title>
    </v-app-bar>
    <v-main>

      <v-container>

        <v-card v-if="confirmar">
          <v-card-title>Confirmação de Dados</v-card-title>
          <v-card-text>
            <v-list>
              <v-list-item>Nome: {{ nome }} </v-list-item>
              <v-list-item>Email: {{ email }}</v-list-item>
            </v-list>
          </v-card-text>
          <v-card-actions>
            <v-btn color="warning" @click="confirmar=false">Alterar</v-btn>
            <v-spacer />
            <v-btn color="success">Confirmar</v-btn>
          </v-card-actions>
        </v-card>

        <v-card v-else>
          <v-card-title>Cadastro</v-card-title>
          <v-card-text>
            <v-text-field variant="outlined" label="Nome Completo" v-model="nome" />
            <v-text-field variant="outlined" label="E-mail" v-model="email" />
          </v-card-text>
          <v-card-actions>
            <v-btn color="warning">Cancelar</v-btn>
            <v-spacer />
            <v-btn color="primary" @click="confirmar=true">Salvar</v-btn>
          </v-card-actions>
        </v-card>



      </v-container>
    </v-main>
  </v-app>
</template>
<script setup>
import { ref } from 'vue'
const drawer = ref(false)
const nome = ref('');
const email = ref('');
const confirmar = ref(false);
</script>