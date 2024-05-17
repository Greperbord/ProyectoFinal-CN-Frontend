<template>
  <v-app id="inspire">
    <v-system-bar app color="rgba(0, 0, 0, 1)">
      <v-icon color="white">
        mdi-facebook
      </v-icon>

      <v-icon color="white">
        mdi-instagram
      </v-icon>

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

    <v-app-bar extended app color="white">
      <a href="/" align="center">
        <v-img style="border-radius: 50px; margin-top: 52px;" :width="100" :src="require('@/assets/images/connectando.jpg')" />
      </a>
      <v-toolbar-title style="margin-top: 45px;">
        <a href="/" style="text-decoration: none; color: black;">
          <span>CO</span>
          <span style="color: green; margin-left: -5px;">NN</span>
          <span style="margin-left: -5px;">ECTANDO</span>
        </a>
      </v-toolbar-title>

      <v-spacer />

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <a href="" style="text-decoration: none; color: #1C1D31;">
          <span>Inicio</span>
        </a>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <span style="color: white;">|</span>
      </li>

      <li class="list-inline-item" style="margin-top: 52px; color: white;">
        <a href="" style="text-decoration: none; color: #1C1D31;">
          <v-icon color="black">mdi-calendar</v-icon>
          <span>Eventos y sitios</span>
        </a>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <span style="color: white;">|</span>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <a href="/beneficios/index.vue" style="text-decoration: none; color: #1C1D31;">
          <span>Beneficios</span>
        </a>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <span style="color: white;">|</span>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <a href="" style="text-decoration: none; color: #1C1D31;">
          <span>Nosotros</span>
        </a>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <span style="color: white;">|</span>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <a href="" style="text-decoration: none; color: #1C1D31;">
          <span>Ayuda</span>
        </a>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <span style="color: white;">|</span>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <v-btn style="border-radius: 20px; text-transform: none; height: 40px;">
          <v-icon>mdi-account-outline</v-icon>
          <span style="color: #1C1D31;">
            Inicio Sesión
          </span>
        </v-btn>
      </li>

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <v-btn style="border-radius: 20px; text-transform: none; background-color: #00E697; height: 40px;">
          <span style="color: #1C1D31;">
            Registrate gratis
          </span>
        </v-btn>
      </li>
    </v-app-bar>

    <v-main class="grey lighten-2">
      <div>
        <v-card style="" color="#F1F6FB" align="center">
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

              <a href="">Conoce más de Connectando</a>
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
                    <li><a href="https://www.connectando.mx/nosotros" style="color: white; text-decoration: none;">Nosotros</a></li>
                    <li><a href="https://www.connectando.mx/contacto" style="color: white; text-decoration: none;">Contacto</a></li>
                    <li><a href="https://www.connectando.mx/login" style="color: white; text-decoration: none;">Inicio Sesión</a></li>
                    <li><a href="https://www.connectando.mx/register" style="color: white; text-decoration: none;">Regístrate gratis</a></li>
                    <li><a href="https://www.connectando.mx/beneficios" style="color: white; text-decoration: none;">Beneficios</a></li>
                  </ul>
                </div>
                <div class="col-md-3">
                  <ul class="list-unstyled">
                    <li class="list-title" style="color: #333446">
                      <h3 style="color: white;">
                        Información Legal
                      </h3>
                    </li>
                    <li><a href="https://www.connectando.mx/soporte" style="color: white; text-decoration: none;">Preguntas Frecuentes</a></li>
                    <li><a href="https://www.connectando.mx/legals/terminos-y-condiciones" style="color: white; text-decoration: none;">TÉRMINOS Y CONDICIONES</a></li>
                    <li><a href="https://www.connectando.mx/legals/aviso-de-privacidad" style="color: white; text-decoration: none;">AVISO DE PRIVACIDAD</a></li>
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
  auth: 'false'
}
</script>
