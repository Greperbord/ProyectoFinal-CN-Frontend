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
      <a href="/principal" align="center" class="logo">
        <v-img src="https://www.connectando.mx/img/logo.svg" />
      </a>

      <v-spacer />

      <li class="list-inline-item" style="margin-top: 50px; color: white;">
        <a href="/principal" style="text-decoration: none; color: #1C1D31;">
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
    </v-app-bar>

    <v-main class="grey lighten-2">
      <section style="background-color: white; padding: 12px 0px;">
        <div class="container">
          <div class="row">
            <v-card elevation="0">
              <v-card elevation="2">
                <v-container fluid>
                  <v-card-title style="margin: 0 auto; width: fit-content;">
                    <h1 class="medium-m-heading text-center">
                      Detalles de pago
                    </h1>
                  </v-card-title>
                  <v-card-subtitle class="text-center">
                    <v-img :src="require('@/assets/images/check.svg')" style="max-width: 100px; max-height: 100px; margin-left: 46%;" />
                    <h2 style="color: black">
                      Pago confirmado
                    </h2>
                    <h3 style="color: rgba(86, 178, 128, 1);">
                      ORDEN #23039
                    </h3>
                  </v-card-subtitle>

                  <v-card-text class="text-center">
                    <span>
                      ¡Gracias por elegir viajar con nosotros!

                      Apreciamos sinceramente tu elección de viajar con nuestra compañía de autobuses. Esperamos que tu viaje sea cómodo, seguro y lleno de momentos inolvidables.

                      Si tienes alguna pregunta o necesitas ayuda adicional, no dudes en comunicarte con nuestro equipo de atención al cliente. Estamos aquí para hacer que tu experiencia de viaje sea lo más placentera posible.

                    </span>
                    <br>
                    <strong>Se envió un mensaje a tu correo con los detalles de tu compra.</strong>
                    <br>
                    <span>
                      ¡Buen viaje y gracias por confiar en nosotros!
                    </span>
                    <br>
                    <span style="color: #00E697;">
                      Atentamente,
                      CONNECTANDO.
                    </span>
                  </v-card-text>
                  <v-card-actions>
                    <v-col>
                      <v-row justify="center" align="center">
                        <v-btn style="background-color: rgba(86, 178, 128, 1); color: white">
                          <a href="/principal" style="text-decoration: none; color: white;">
                            <span>Inicio</span>
                          </a>
                        </v-btn>
                      </v-row>
                    </v-col>
                  </v-card-actions>
                </v-container>
              </v-card>
            </v-card>
          </div>
        </div>
      </section>

      <div style="background-color: white;">
        <div class="row" style="margin-left: 100px; margin-right: 100px;">
          <div class="col-md-4">
            <div>
              <v-icon>mdi-truck</v-icon>
              <h3>Quiénes Somos</h3>
              <p>Descubre más de nuestra visión, lo que nos mueve y como queremos cambiar la forma en la que tu viajas por el país</p>

              <a href="" style="color: gray">Conoce más de Connectando</a>
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
  auth: true
}
</script>

<style scoped>
.text-decoration-none {
  text-decoration: none;
}
.logo {
    width: 250px;
    mix-blend-mode: multiply;
    margin-right: 30px;
    margin-top: 50px;
}
</style>
