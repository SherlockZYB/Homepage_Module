<template>
  <v-app>
    <v-app-bar color="grey-lighten-2" v-if="windowSize<900">
      <template v-slot:prepend>
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      </template>

      <v-app-bar-title>Zhou Yubo's Homepage</v-app-bar-title>

      <template v-slot:append>
        <v-btn icon="mdi-dots-vertical"></v-btn>
      </template>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" color="grey-darken-2" bottom width="380">
      <v-list>
        <v-list-item
                prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
                title="Sandra Adams"
                subtitle="sandra_a88@gmailcom"
        ></v-list-item>
      </v-list>

      <v-divider></v-divider>

      <v-list density="compact" nav>
        <v-list-item prepend-icon="mdi-folder" title="My Files" value="myfiles"></v-list-item>
        <v-list-item prepend-icon="mdi-account-multiple" title="Shared with me" value="shared"></v-list-item>
        <v-list-item prepend-icon="mdi-star" title="Starred" value="starred"></v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container class="text-center" style="height: 300px">
        <v-row style="background-color: aliceblue">
          <v-col>
            <v-avatar size="100">
              <img src="https://cdn.vuetifyjs.com/images/john.jpg">
            </v-avatar>
            <h1>Zhou Yubo</h1>
            <router-link to="/">English</router-link>|<router-link to="/zh-cn">简体中文</router-link>
          </v-col>
        </v-row>
      </v-container>

    </v-main>
  </v-app>
</template>

<script>
import { defineComponent,ref } from 'vue';

// Components
import HelloWorld from '../components/HelloWorld.vue';

export default defineComponent({
  name: 'HomeView',
  components: {
  },
  setup(){
    let windowSize=ref(document.body.clientWidth)
    let drawer=ref(true)
    window.onresize=()=>{
      windowSize.value=document.body.clientWidth
      if(windowSize.value>900){
        drawer.value=true
      }else {
        drawer.value=false
      }
    }


    return {windowSize,drawer}
  }
});
</script>
