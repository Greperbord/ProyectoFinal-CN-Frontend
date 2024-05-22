<template>
  <v-app id="inspire">
    <v-app-bar extended app color="white" elevation="0">
      <a href="/" align="center" class="logo">
        <v-img src="https://www.connectando.mx/img/logo.svg" />
      </a>

      <v-spacer />

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <a href="/" style="text-decoration: none; color: #1C1D31;">
          <span>Inicio</span>
        </a>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <span style="color: white;">|</span>
      </li>

      <li class="list-inline-item" style="margin-top: 52px; color: white;">
        <a href="/eventos" style="text-decoration: none; color: #1C1D31;">
          <v-icon color="black">mdi-calendar</v-icon>
          <span>Eventos y sitios</span>
        </a>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <span style="color: white;">|</span>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <a href="/beneficios" style="text-decoration: none; color: #1C1D31;">
          <span>Beneficios</span>
        </a>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <span style="color: white;">|</span>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <a href="/nosotros" style="text-decoration: none; color: #1C1D31;">
          <span>Nosotros</span>
        </a>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <span style="color: white;">|</span>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <a href="/ayuda" style="text-decoration: none; color: #1C1D31;">
          <span>Ayuda</span>
        </a>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <span style="color: white;">|</span>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <v-btn style="border-radius: 20px; text-transform: none; height: 40px;">
          <v-icon>mdi-account-outline</v-icon>
          <a href="/login" style="text-decoration: none; color: #1C1D31;">
            <span>Inicio Sesión</span>
          </a>
        </v-btn>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <v-btn style="border-radius: 20px; text-transform: none; background-color: #00E697; height: 40px;">
          <a href="/register" style="text-decoration: none; color: #1C1D31;">
            <span>Registrate gratis</span>
          </a>
        </v-btn>
      </li>
    </v-app-bar>

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
          <v-card max-width="500" style="background-color: #fff3cd">
            <v-title>
              <v-icon>mdi-alert-circle-outline</v-icon>
              <strong>CLIENTES MODUM:</strong>
            </v-title>
            <v-text>
              <p> Para recuperar tu cuenta registrada da click en el botón ¿Olvidaste contraseña? Para establecer un nuevo acceso.</p>
            </v-text>
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
                  <v-checkbox
                    v-model="checkbox"
                  />
                  <span style="font-size: 12px !important;">RECORDAR CUENTA</span>
                  <v-spacer />
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
              </v-col>
            </v-card-actions>
          </v-card>
        </div>
      </div>

      <div style="background-color: white;">
        <div class="row" style="margin-left: 100px; margin-right: 100px;">
          <div class="col-md-4" style=" margin-top: 100px">
            <div>
              <v-icon>mdi-truck</v-icon>
              <h3>Quiénes Somos</h3>
              <p>Descubre más de nuestra visión, lo que nos mueve y como queremos cambiar la forma en la que tu viajas por el país</p>

              <a href="" style="color: gray">Conoce más de Connectando</a>
            </div>
          </div>

          <div class="col-md-4" style=" margin-top: 100px">
            <div>
              <v-icon>mdi-web</v-icon>
              <h3>Medio Ambiente</h3>
              <p> Por cada CONNEXIÓN se evita, al menos, el víaje de 5 autos privados, ahorrando así emisiones equivalentes a más de 500 mil kilómetros anuales. </p>
            </div>
          </div>

          <div class="col-md-4" style=" margin-top: 100px">
            <div>
              <v-icon>mdi-account-outline</v-icon>
              <h3>Seguridad</h3>
              <p>Contamos con conductores capacitados disminuyendo de esta forma el riesgo de accidentes. </p>
            </div>
          </div>
        </div>
      </div>

      <div style="background-color: #333446;">
        <div class="row" style="margin-left: 100px; margin-right: 100px;">
          <div class="row">
            <div class="col-md-4">
              <img src="https://www.connectando.mx/img/logo-small.svg" width="100" alt="Connectando">
              <li class="list-inline-item" style="color: #333446">
                <a href="https://www.facebook.com/modumcabmx">
                  <v-icon style="color: white">mdi-facebook</v-icon>
                </a>
              </li>
              <li class="list-inline-item" style="color: #333446">
                <a href="https://www.instagram.com/modumtoursofficial/">
                  <v-icon style="color: white">mdi-instagram</v-icon>
                </a>
              </li>
            </div>
            <div class="col-md-8">
              <div class="row">
                <div class="col-md-3" />
                <div class="col-md-3" />
                <div class="col-md-3">
                  <ul class="list-unstyled">
                    <li class="list-title" style="color: #333446">
                      <h3 style="color: white;">
                        Ayuda
                      </h3>
                    </li>
                    <li><a href="/nosotros" style="color: white; text-decoration: none;">Nosotros</a></li>
                    <li><a href="/contacto" style="color: white; text-decoration: none;">Contacto</a></li>
                    <li><a href="/login" style="color: white; text-decoration: none;">Inicio Sesión</a></li>
                    <li><a href="/register" style="color: white; text-decoration: none;">Regístrate gratis</a></li>
                    <li><a href="/beneficios" style="color: white; text-decoration: none;">Beneficios</a></li>
                  </ul>
                </div>
                <div class="col-md-3">
                  <ul class="list-unstyled">
                    <li class="list-title" style="color: #333446">
                      <h3 style="color: white;">
                        Información Legal
                      </h3>
                    </li>
                    <li><a href="/ayuda" style="color: white; text-decoration: none;">Preguntas Frecuentes</a></li>
                    <li><a href="/terminos-y-condiciones" style="color: white; text-decoration: none;">TÉRMINOS Y CONDICIONES</a></li>
                    <li><a href="/aviso-de-privacidad" style="color: white; text-decoration: none;">AVISO DE PRIVACIDAD</a></li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </v-main>
  </v-app>
</template>

<script>
export default {
  auth: false,
  checkbox: false
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
