<template>
      <v-navigation-drawer permanent>

        <v-list
          dense
          nav
        >
          <v-list-item link>
            <router-link to="/home">
                <v-list-item-title> <v-icon>mdi-home-city </v-icon> VISÃO GERAL </v-list-item-title>
            </router-link>
          </v-list-item>
          <v-list-item link>
            
            <router-link to="/cadastro">
                <v-list-item-title> <v-icon>mdi-store </v-icon> CADASTRO </v-list-item-title>
            </router-link>
          </v-list-item>

          <v-list-item link>
          <router-link to="/venda">
                <v-list-item-title> <v-icon>mdi-cash-register </v-icon> VENDAS </v-list-item-title>
            </router-link>
          </v-list-item>

          
        </v-list>
      </v-navigation-drawer>
  </template>

<script>
export default {
    name: 'SideNav',
    }
</script>