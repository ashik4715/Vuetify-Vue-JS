<template>
  <div class="team">

    <div class="container">
      <h1 class="heading white--text">Team</h1>

      <v-container fluid class="my-5">

        <v-layout row wrap>
          <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
            <v-card flat class="text-xs-center ma-3">

              <v-responsive class="pt-4">
                <v-avatar size="300" class="grey lighten-2">
                  <img :src="person.avatar" alt="">
                </v-avatar>
              </v-responsive>

              <v-card-text>
                <div class="subheading">{{ person.name }}</div>
                <div class="teal--text">{{ person.role }}</div>
              </v-card-text>

              <v-card-actions>
                <v-btn flat color="light-green accent-4">
                  <v-icon small left>message</v-icon>
                  <span class="text-lowercase">Message</span>
                </v-btn>
              </v-card-actions>

            </v-card>
          </v-flex>
        </v-layout>

      </v-container>

    </div>

  </div>
</template>

<script>
    export default {
      data(){
          return{
              team: [
                  { name:'Taylor Otwell', role:'Web Developer', avatar:'/avatar-1.jpg'},
                  { name:'Paula Scher', role:'Graphic Designer', avatar:'/avatar-2.jpg'},
                  { name:'Yuriy Garnaev', role:'HR Manager', avatar:'/avatar-3.jpg'},
                  { name:'Karina Carvalho', role:'Cloud Support Engineer', avatar:'/avatar-4.jpg'},
                  { name:'Brooke Lark ', role:'Photographer', avatar:'/avatar-5.jpg'},
              ]
          }
      }
    }
</script>
