<template>
  <v-app id="inspire">
    <v-system-bar app color="rgba(0, 0, 0, 1)">
      <a href="https://www.facebook.com/modumcabmx">
        <v-icon color="white">
          mdi-facebook
        </v-icon>
      </a>

      <a href="https://www.instagram.com/modumtoursofficial/">
        <v-icon color="white">
          mdi-instagram
        </v-icon>
      </a>

      <v-spacer />

      <li class="list-inline-item">
        <a href="mailto:hola@connectando.mx" style="text-decoration: none; color: white;">
          <v-icon color="white">mdi-mail</v-icon>
          <span>hola@connectando.mx</span>
        </a>
      </li>

      <li class="list-inline-item">
        <span style="color: white;">|</span>
      </li>

      <li class="list-inline-item">
        <a href="tel:4775696726" style="text-decoration: none; color: white;">
          <v-icon color="white">mdi-phone</v-icon>
          <span>477 569 6726</span>
        </a>
      </li>

      <li class="list-inline-item">
        <a href="https://api.whatsapp.com/send?phone=+5214775696726&text=%C2%A1Buen%20d%C3%ADa,%20tengo%20preguntas%20de%20su%20servicio!" style="text-decoration: none; color: white;">
          <v-icon color="white">mdi-whatsapp</v-icon>
          <span>477 569 6726</span>
        </a>
      </li>
    </v-system-bar>

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
      <div fluid>
        <v-img :src="require('@/assets/images/banner.png')">
          <v-row no-gutters>
            <v-col cols="7">
              <v-card max-width="300px" style="margin-top: 100px; margin-left: 100px;" color="#12F901" align="center">
                <v-card-title>TÉRMINOS Y CONDICIONES</v-card-title>
                <v-card-subtitle>TE RECOMENDAMOS REVISAR NUESTROS TERMINOS Y CONDICIONES ANTES DE RESERVAR. EVITA CONTRATIEMPOS.</v-card-subtitle>
              </v-card>
            </v-col>
            <v-col>
              <v-card align="center" class="ma-2" style="background-color: #1C1D31; border-radius: 20px">
                <v-img style="border-radius: 100px; max-width: 90px; margin-left: -610px;" :src="require('@/assets/images/hand_wave.png')" />
                <v-card-title style="color: white; margin-left: 90px;">
                  Bienvenido
                </v-card-title>
                <v-card-subtitle style="color: white; margin-left: 90px;" align="left">
                  ¿A donde viajaremos hoy?
                </v-card-subtitle>
                <v-card-actions style="margin-left: 100px;">
                  <v-btn style="border-radius: 20px;">
                    <v-icon>mdi-cached</v-icon>
                    <span>Redondo</span>
                  </v-btn>
                  <v-btn style="border-radius: 20px;">
                    <v-icon>mdi-ray-start-arrow</v-icon>
                    <span>Sencillo</span>
                  </v-btn>
                </v-card-actions>
                <v-card max-width="400" style="border-radius: 20px;" class="pa-2 ma-2">
                  <v-row>
                    <v-row class="pa-2 ma-2" style="max-height: 30px;">
                      <v-icon style="margin-top: -15px; margin-left: 20px;">
                        mdi-circle-outline
                      </v-icon>
                      <v-select
                        v-model="select"
                        style="max-width: 300px;"
                        class="ma-2 pa-2"
                        :hint="`${select.state}`"
                        :items="items"
                        item-text="state"
                        label="Selecciona el origen:"
                        persistent-hint
                        return-object
                        single-line
                      />
                    </v-row>
                    <v-row class="pa-2 ma-2" style="max-height: 85px;">
                      <v-icon style="margin-top: -15px; margin-left: 20px;">
                        mdi-square-outline
                      </v-icon>
                      <v-select
                        v-model="select"
                        style="max-width: 300px;"
                        class="ma-2 pa-2"
                        :hint="`${select.state}`"
                        :items="items"
                        item-text="state"
                        label="Selecciona el destino:"
                        persistent-hint
                        return-object
                        single-line
                      />
                    </v-row>
                  </v-row>
                </v-card>
                <v-card-actions style="margin-left: 94px; color: white; margin-right: 100px">
                  <v-row>
                    <v-col cols="6">
                      <span>Salida</span>
                      <v-btn style="overflow: hidden; background-color: #333446; border-radius: 50px;" outlined color="white">
                        <v-menu
                          ref="menu"
                          v-model="menu"
                          :close-on-content-click="false"
                          :return-value.sync="date"
                          transition="scale-transition"
                          min-width="auto"
                        >
                          <template #activator="{ on, attrs }">
                            <v-text-field
                              v-model="date"
                              style="color: white; margin-left: 20px;"
                              readonly
                              v-bind="attrs"
                              v-on="on"
                            />
                          </template>
                          <v-date-picker
                            v-model="date"
                            no-title
                            scrollable
                            style="color: white;"
                          >
                            <v-spacer />
                            <v-btn
                              text
                              color="primary"
                              @click="menu = false"
                            >
                              Cancel
                            </v-btn>
                            <v-btn
                              text
                              color="primary"
                              @click="$refs.menu.save(date)"
                            >
                              OK
                            </v-btn>
                          </v-date-picker>
                        </v-menu>
                      </v-btn>
                    </v-col>
                    <v-col cols="6">
                      <span>Regreso</span>
                      <v-btn style="overflow: hidden; background-color: #333446; border-radius: 50px; margin-left: -10px;" outlined color="white">
                        <v-menu
                          ref="menu2"
                          v-model="menu2"
                          :close-on-content-click="false"
                          :return-value.sync="date"
                          transition="scale-transition"
                          min-width="auto"
                        >
                          <template #activator="{ on, attrs }">
                            <v-text-field
                              v-model="date"
                              style="color: white; margin-left: 20px;"
                              readonly
                              v-bind="attrs"
                              v-on="on"
                            />
                          </template>
                          <v-date-picker
                            v-model="date"
                            no-title
                            scrollable
                            style="color: white;"
                          >
                            <v-spacer />
                            <v-btn
                              text
                              color="primary"
                              @click="menu2 = false"
                            >
                              Cancel
                            </v-btn>
                            <v-btn
                              text
                              color="primary"
                              @click="$refs.menu2.save(date)"
                            >
                              OK
                            </v-btn>
                          </v-date-picker>
                        </v-menu>
                      </v-btn>
                    </v-col>
                    <v-col>
                      <v-col>
                        Usuarios
                      </v-col>
                      <v-btn style="background-color: #333446; border-radius: 20px; width: 397px;" outlined color="white">
                        <v-select
                          :items="items2"
                        />
                      </v-btn>
                    </v-col>
                    <v-col>
                      <v-row align="center">
                        <v-checkbox
                          v-model="checkbox"
                        />
                        <span>Equipaje Extra</span>
                        <v-spacer />
                        <span>* Costo adicional por trayecto</span>
                      </v-row>
                    </v-col>
                    <v-col>
                      <v-btn style="background-color: #00E697; border-radius: 20px; width: 397px; height: 50px;" outlined color="black">
                        <span>Buscar Tours</span>
                      </v-btn>
                    </v-col>
                  </v-row>
                </v-card-actions>
              </v-card>
            </v-col>
          </v-row>
        </v-img>
      </div>
      <v-spacer />
      <div>
        <v-card style="" color="#F1F6FB" align="center" elevation="0">
          <v-card-title class="justify-center">
            Beneficios
          </v-card-title>
          <v-img :src="require('@/assets/images/beneficios.png')" />
        </v-card>
      </div>

      <div class="row align-items-center" style="background-color: white;">
        <div class="col-12 col-md-4 offset-md-1">
          <div style="margin-top: 150px;">
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

        <div class="col-12 col-md-6">
          <img src="https://www.connectando.mx/img/call-to-action.png" class="img-fluid" alt="">
        </div>
      </div>

      <div style="background-color: white;">
        <div class="row" style="margin-left: 100px; margin-right: 100px;">
          <div class="col-md-4">
            <div>
              <v-icon>mdi-truck</v-icon>
              <h3>Quiénes Somos</h3>
              <p>Descubre más de nuestra visión, lo que nos mueve y como queremos cambiar la forma en la que tu viajas por el país</p>

              <a href="" style="text-transform: none; color: gray">Conoce más de Connectando</a>
            </div>
          </div>

          <div class="col-md-4">
            <div>
              <v-icon>mdi-web</v-icon>
              <h3>Medio Ambiente</h3>
              <p> Por cada CONNEXIÓN se evita, al menos, el víaje de 5 autos privados, ahorrando así emisiones equivalentes a más de 500 mil kilómetros anuales. </p>
            </div>
          </div>

          <div class="col-md-4">
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
  data () {
    return {
      select: { state: '' },
      items: [
        { state: 'León' },
        { state: 'Ciudad de México' }
      ],
      date: (new Date(Date.now() - (new Date()).getTimezoneOffset() * 60000)).toISOString().substr(0, 10),
      menu: false,
      modal: false,
      menu2: false,
      items2: ['1', '2', '3', '4'],
      checkbox: false
    }
  }
}
</script>

<style scoped>
.logo {
    width: 250px;
    mix-blend-mode: multiply;
    margin-right: 30px;
    margin-top: 50px;
}
</style>
