<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app clipped>

        <v-list-item link  >
          <v-list-item-action>
            <v-icon class="ma-2" tile  color="teal">mdi-vuetify</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Vue.js</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link href="/">
          <v-list-item-action>
            <v-icon>mdi-home-city</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
<!--
        <v-list-item link href="/apisback">
          <v-list-item-action>
            <v-icon>mdi-cog</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>ApisBack</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link href=/apis>
          <v-list-item-action>
            <v-icon>mdi-code-tags</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Apis</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link href="/publicaciones">
          <v-list-item-action>
            <v-icon>mdi-image</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Publicaciones</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
-->
  
        <v-list-item link href="/login">
          <v-list-item-action>
            <v-icon>mdi-account</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Account Login</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link href="/registro">
          <v-list-item-action >
            <v-icon>mdi-plus</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Registro</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link href="/contacto">
          <v-list-item-action>
            <v-icon>mdi-email</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Contacto</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
<!--link href="/perfil/" -->
        <v-list-item   link href="/perfil" >
          <v-list-item-action>
            <v-icon>mdi-account</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Perfil </v-list-item-title>
          </v-list-item-content>
        </v-list-item>

         <v-list-item link href="/perfil/usuarios">
          <v-list-item-action>
            <v-icon>mdi-account-group-outline</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Tabla Users</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link href="/perfil/tablavideos">
          <v-list-item-action >
            <v-icon>mdi-television</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Tabla Videos</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-view-dashboard</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Dashboard</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <hr color="#145A32">

        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-home-city</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>City Home</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-account</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Account</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-account-group-outline</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Users</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <hr color="#145A32">

        <v-list-item link>
          <v-list-item-icon>
               <v-icon>mdi-account-multiple</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Shared with me</v-list-item-title>
        </v-list-item>

        <v-list-item link>
          <v-list-item-icon>
           <v-icon>mdi-star</v-icon>
          </v-list-item-icon>
            <v-list-item-title>Starred</v-list-item-title>
            </v-list-item>

      

        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-cog</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Settings</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <hr color="#145A32">

        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-email</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Mail</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-cloud-upload</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Cloud-Upload</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link >
          <v-list-item-action>
            <v-icon>mdi-code-tags</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Code tags</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-wrench</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Wrench</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-action >
            <v-icon>mdi-format-list-bulleted-square</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>List Square</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-action >
            <v-icon>mdi-plus</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Plus</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

         <v-list-item link>
          <v-list-item-action >
            <v-icon>mdi-pencil</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Pencil</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-action >
            <v-icon>mdi-television</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>TV</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        
        <v-list-item link>
          <v-list-item-action >
            <v-icon>mdi-cog</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Settings</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <router-link :to="{ path: 'login' }" class="none">
            <v-list-item link >
              <v-list-item-action>
                <v-icon>mdi-help-box</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>Help Box</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
        </router-link>

   
    </v-navigation-drawer>

    <v-app-bar app clipped-left>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        <v-toolbar-title link href="/" > <v-icon hover class="mr-2 large hover" color="#145A32" x-large  >mdi-television</v-icon>GreenTube</v-toolbar-title> 
      <v-spacer></v-spacer>
      <strong > </strong>
        <!--<v-col  class="hidden-xs-only"  sm="5"  md="3" >
                <strong >mmmmmmmmmmmm</strong>
          </v-col> -->
      <v-avatar color="indigo">
        <v-icon dark>mdi-account-circle</v-icon>
      </v-avatar>

      <v-menu left bottom>
        <template v-slot:activator="{ on, attrs }">
          <v-btn  icon v-bind="attrs"   v-on="on" >
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
            <v-list-item link href="/perfil"
              @click="() => {}">
              <v-list-item-title>Perfil</v-list-item-title>
            </v-list-item>
            
            <v-list-item link href="/home"
              @click="logout">
              <v-list-item-title>Cerrar Sesion</v-list-item-title>
            </v-list-item> 

        </v-list>
      </v-menu>
<!----
      <v-row justify="space-around">
        
        <v-icon large color="green darken-2">mdi-domain</v-icon>
        <v-icon large color="blue darken-2">mdi-message-text</v-icon>
        <v-icon large color="purple darken-2">mdi-dialpad</v-icon>
        <v-icon large color="teal darken-2">mdi-email</v-icon>
        <v-icon large color="blue-grey darken-2">mdi-call-split</v-icon>
        <v-icon large color="orange darken-2">mdi-arrow-up-bold-box-outline</v-icon>
        
      </v-row>-->

    </v-app-bar>


    <v-main>
         <!-- el que se muestra independiente de la ruta-->
         <!-- el que se muestra independiente de la ruta-->

      <router-view>
        <router-link to="/publicaciones">Home</router-link> 
      </router-view>
    </v-main>
  
    <v-footer app>
      <span>&copy; 2020</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  props: {
    source: String,
  },
  data: () => ({
    drawer: null,
    perfil:{}
  }),
  created() {
    this.$vuetify.theme.dark = true;
    
  },

  methods:{
   async logout(){
      await this.$store.dispatch("auth/logout")
    }
  },
  
  computed: {
    User() {
                                //moduolo
    console.log('algo computed',this.$store.getters["auth/getAuth"]);
    return this.$store.getters["auth/getAuth"];
    }
  },

  mounted() {
      console.log('algo mounteeddd',this.$store.getters["auth/getAuth"]);
       this.$store.getters["auth/getAuth"];
      this.perfil = window.localStorage.getItem('auth')
    console.log('get auth mounted',this.perfil);
    //this.getTodos();
  }
};
</script>
