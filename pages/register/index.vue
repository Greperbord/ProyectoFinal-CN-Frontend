<template>
  <v-app id="inspire">
    <v-main class="grey lighten-2">
      <div class="row align-items-center" style="background-color: white;">
        <div class="col-6 col-md-5 offset-md-1">
          <div style="margin-top: 100px;">
            <small class="text-uppercase">Beneficios para miembros</small>
            <h1>Crear una cuenta</h1>

            <v-icon color="green">
              mdi-check-circle
            </v-icon>
            <span>Cancelaciones con un solo click</span>
            <v-spacer />
            <v-icon color="green">
              mdi-check-circle
            </v-icon>
            <span>CONNEXIONES gratis</span>
            <v-spacer />
            <v-icon color="green">
              mdi-check-circle
            </v-icon>
            <span>Tarifas especiales y promociones</span>
            <v-spacer />
            <v-icon color="green">
              mdi-check-circle
            </v-icon>
            <span>Seguro de viajero extendido</span>
            <v-spacer />
            <v-icon color="green">
              mdi-check-circle
            </v-icon>
            <span>Modificaciones a tu itinerario</span>
          </div>

          <div class="d-flex align-items-center app-store-logos">
            <a href="https://apps.apple.com/cz/app/connectando/id1628111517"><img src="https://www.connectando.mx/img/apple-store.svg" alt="Descarga en la App Store" class="me-3"></a>
            <a href="https://play.google.com/store/apps/details?id=mx.modumcab.connectapp"><img src="https://www.connectando.mx/img/android-store.svg" alt="Descarga en la Google Play Store"></a>
          </div>
        </div>

        <div class="col-6 col-md-5" style="margin-top: 100px;">
          <v-card rounded color="white" style="height: 50%!important;" elevation="0" max-width="600">
            <v-row style="max-height: 30px; max-width: 500px">
              <v-col>
                <span style="font-size: 15px !important;">NOMBRE*</span>
                <v-row class="ma-2">
                  <v-text-field v-model="nombre" rounded outlined />
                </v-row>
              </v-col>
            </v-row>
            <v-row style="max-height: 30px; max-width: 500px; margin-top: 80px !important;">
              <v-col>
                <label style="font-size: 15px !important;">APELLIDO*</label>
                <v-row class="ma-2">
                  <v-text-field
                    v-model="apellido"
                    rounded
                    outlined
                  />
                </v-row>
              </v-col>
            </v-row>
            <v-row style="max-height: 30px; max-width: 500px; margin-top: 80px !important;">
              <v-col>
                <label style="font-size: 15px !important;">TELEFONO*</label>
                <v-row class="ma-2">
                  <v-text-field
                    v-model="telefono"
                    rounded
                    outlined
                  />
                </v-row>
              </v-col>
            </v-row>
            <v-row style="max-height: 30px; max-width: 500px; margin-top: 80px !important;">
              <v-col>
                <label style="font-size: 15px !important;">EDAD*</label>
                <v-row class="ma-2">
                  <v-text-field
                    v-model="edad"
                    rounded
                    outlined
                  />
                </v-row>
              </v-col>
            </v-row>
            <v-row style="max-height: 30px; max-width: 500px; margin-top: 80px !important;">
              <v-col>
                <label style="font-size: 15px !important;">CORREO ELECTRÓNICO*</label>
                <v-row class="ma-2">
                  <v-text-field
                    v-model="email"
                    rounded
                    outlined
                  />
                </v-row>
              </v-col>
            </v-row>
            <v-row style="max-height: 130px; max-width: 500px; margin-top: 80px !important;">
              <v-col>
                <label style="font-size: 15px !important;">CONTRASEÑA*</label>
                <v-row class="ma-2">
                  <v-text-field
                    v-model="password"
                    type="password"
                    rounded
                    outlined
                  />
                </v-row>
              </v-col>
            </v-row>

            <v-card-actions>
              <v-col cols="12">
                <v-row align="center" style="max-width: 500px">
                  <v-checkbox
                    v-model="checkbox"
                  />
                  <span style="font-size: 12px !important;">Al registrar tu cuenta con nosotros aceptas nuestro TÉRMINOS Y CONDICIONES.</span>
                  <span style="font-size: 12px !important; margin-top: -15px !important; margin-left: 30px;">Solo mandamos correos de notificación de compra o seguimiento de tu reservación.</span>
                </v-row>
                <v-row class="rowCard">
                  <v-btn block class="pa-2" color="#00e697" rounded @click="registrarUsuario">
                    <span style="text-transform: none; color: black;">REGISTRAR TU CUENTA</span>
                  </v-btn>
                </v-row>
              </v-col>
            </v-card-actions>
          </v-card>
        </div>
      </div>
    </v-main>
  </v-app>
</template>

<script>
export default {
  auth: false,
  checkbox: false,
  data () {
    return {
      email: null,
      password: null,
      nombre: null,
      apellido: null,
      telefono: null,
      edad: null
    }
  },
  methods: {
    registrarUsuario () {
      const url = '/register'
      const data = {
        email: this.email,
        password: this.password,
        nombre: this.nombre,
        apellido: this.apellido,
        telefono: this.telefono,
        edad: this.edad
      }
      this.$axios.post(url, data).then((res) => {
        console.log('@@@ res => ', res)
        if (res.data.message === 'User registered successfully') {
          this.showDialog = false
          this.$router.push('/')
        }
      })
        .catch((error) => {
          console.log('@@@ error => ', error)
        })
    }
  }
}
</script>

<style scoped>
.rowCard {
  width: 500px;
  display: flex;
  justify-content: center;
}
.logo {
    width: 250px;
    mix-blend-mode: multiply;
    margin-right: 30px;
    margin-top: 50px;
}
</style>
