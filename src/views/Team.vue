<template>
  <div class="team">

    <div class="container">
      <h1 class="heading white--text">Team</h1>

      <v-container fluid class="my-5">

        <v-layout row wrap>
          <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
            <v-card flat class="text-xs-center ma-3">

              <v-responsive class="pt-4">
                images
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
                  { name:'Dedsec', role:'System Architecture'},
                  { name:'Taylor Otwell', role:'Web Developer'},
                  { name:'Paula Scher', role:'Graphic Designer'},
                  { name:'Arash', role:'HR Manager'},
                  { name:'T-bone', role:'Cloud Support Engineer'},
              ]
          }
      }
    }
</script>
