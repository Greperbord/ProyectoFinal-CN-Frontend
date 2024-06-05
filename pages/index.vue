<template>
  <v-app id="inspire">
    <v-main class="white">
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
          <v-card max-width="500" style="background-color: #fff3cd">
            <v-card-title>
              <v-icon>mdi-alert-circle-outline</v-icon>
              <strong>CLIENTES MODUM:</strong>
            </v-card-title>
            <v-card-text>
              <p> Para recuperar tu cuenta registrada da click en el botón ¿Olvidaste contraseña? Para establecer un nuevo acceso.</p>
            </v-card-text>
          </v-card>
          <v-card rounded color="white" style="height: 50%!important;" elevation="0" max-width="600">
            <v-row style="max-height: 30px; max-width: 500px">
              <v-col>
                <label>CORREO ELECTRÓNICO</label>
                <v-row class="ma-2">
                  <v-icon style="margin-top: -25px">
                    mdi-email-outline
                  </v-icon>
                  <v-text-field v-model="email" style="margin-left: 20px !important;" rounded label="Ingresa tu correo" outlined />
                </v-row>
              </v-col>
            </v-row>
            <v-row style="max-height: 130px; max-width: 500px; margin-top: 80px !important;">
              <v-col>
                <label>CONTRASEÑA</label>
                <v-row class="ma-2">
                  <v-icon style="margin-top: -25px">
                    mdi-account-outline
                  </v-icon>
                  <v-text-field
                    v-model="password"
                    style="margin-left: 20px !important;"
                    rounded
                    label="Ingresa tu contraseña"
                    type="password"
                    outlined
                  />
                </v-row>
              </v-col>
            </v-row>

            <v-card-actions>
              <v-col cols="12">
                <v-row align="center" style="max-width: 500px">
                  <a href="" style=" text-decoration: none !important; color: black;">
                    <v-icon>
                      mdi-account-outline
                    </v-icon>
                    <span style="font-size: 12px !important;">¿OLVIDASTE LA CONTRASEÑA?</span>
                  </a>
                </v-row>
                <v-row class="rowCard">
                  <v-btn block class="pa-2" color="#00e697" rounded @click="login">
                    <span style="text-transform: none; color: black;">INICIAR SESIÓN</span>
                  </v-btn>
                </v-row>
                <v-row class="rowCard">
                  <v-btn
                    block
                    class="pa-2"
                    style="margin-top: 20px;"
                    color="#00e697"
                    rounded
                    href="/register"
                  >
                    <span style="text-transform: none; color: black;">REGISTRARSE</span>
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
  data () {
    return {
      email: null,
      password: null
    }
  },
  methods: {
    async login () {
      const sendData = {
        email: this.email,
        password: this.password
      }
      await this.$auth.loginWith('local', {
        data: sendData
      }).then(async (res) => {
        const result = await res.data
        if (result.message === 'success') {
          this.$store.commit('setToken', result.token)
          this.$router.push('/principal')
        }
      }).catch((err) => {
        console.log('@@@ error => ', err)
      })
    }
  }
}
</script>
