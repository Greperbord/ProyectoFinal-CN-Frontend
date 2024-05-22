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
      <div style="background-color: white;">
        <div class="row align-items-center">
          <div class="col-md-10 offset-md-1">
            <h4 class="mb-1 mt-4">
              <v-icon color="black">
                mdi-calendar
              </v-icon>
              Eventos Próximos
            </h4>
            <p>Descubre los mejores eventos en nuestros destinos.</p>
            <hr>

            <div class="row mb-5">
              <div class="col-md-4">
                <div class="event-card event-card-7">
                  <div class="date-detail">
                    <p>30</p>
                    <p>nov.</p>
                  </div>

                  <div class="content">
                    <div class="d-flex align-items-center justify-content-between">
                      <p>
                        <v-icon style="color: white;">
                          mdi-calendar-month-outline
                        </v-icon> 30 nov. - 2023
                      </p>
                      <p>
                        <v-icon style="color: white">
                          mdi-clock-time-eight-outline
                        </v-icon> 10:00
                      </p>
                    </div>

                    <h4>MUSEO JUMEX</h4>
                    <p class="mb-0">
                      Colección JUMEX: Todo se vuelve más ligero. Instalación de obra de Abraham Cruzvillegas
                      Exposición gratuita
                      del 18 de noviembre 2023
                      y hasta el 11 de febrero 2024
                    </p>

                    <hr>

                    <v-btn style="background-color: white; color: black; margin-top: 20px;">
                      <a href="https://www.fundacionjumex.org/es/exposiciones/288-coleccion-jumex-todo-se-vuelve-mas-ligero" style="text-decoration: none; text-transform: none; color: black;">
                        <v-icon style="color: black;">mdi-link</v-icon>
                        visitar sitio
                      </a>
                    </v-btn>
                  </div>
                  <div class="overlay" />
                </div>
              </div>

              <style>
                .event-card-7{
                background: url(https://www.connectando.mx/img/events/event_1701358859.jpeg);
                background-size: cover;
                background-position: center center;
                }
              </style>
              <div class="col-md-4">
                <div class="event-card event-card-8">
                  <div class="date-detail">
                    <p>30</p>
                    <p>nov.</p>
                  </div>

                  <div class="content">
                    <div class="d-flex align-items-center justify-content-between">
                      <p>
                        <v-icon style="color: white;">
                          mdi-calendar-month-outline
                        </v-icon> 30 nov. - 2023
                      </p>
                      <p>
                        <v-icon style="color: white">
                          mdi-clock-time-eight-outline
                        </v-icon> 11:00
                      </p>
                    </div>

                    <h4>MUSEO FRIDA KAHLO</h4>
                    <p class="mb-0">
                      Este año conmemoramos el 65º aniversario del Museo Frida Kahlo, la Casa Azul. Cuenta con una colección única de objetos personales, obras de arte y fotografías que ofrecen una visión íntima de la vida de Frida Kahlo.
                    </p>

                    <hr>

                    <v-btn style="background-color: white; color: black; margin-top: 20px;">
                      <a href="https://www.museofridakahlo.org.mx/" style="text-decoration: none; text-transform: none; color: black;">
                        <v-icon style="color: black;">mdi-link</v-icon>
                        visitar sitio
                      </a>
                    </v-btn>
                  </div>
                  <div class="overlay" />
                </div>
              </div>

              <style>
                .event-card-8{
                background: url(https://www.connectando.mx/img/events/event_1701359622.jpeg);
                background-size: cover;
                background-position: center center;
                }
              </style>
              <div class="col-md-4">
                <div class="event-card event-card-9">
                  <div class="date-detail">
                    <p>17</p>
                    <p>nov.</p>
                  </div>

                  <div class="content">
                    <div class="d-flex align-items-center justify-content-between">
                      <p>
                        <v-icon style="color: white;">
                          mdi-calendar-month-outline
                        </v-icon> 17 nov. - 2023
                      </p>
                      <p>
                        <v-icon style="color: white">
                          mdi-clock-time-eight-outline
                        </v-icon> 15:00
                      </p>
                    </div>

                    <h4>GUANAJUATO BRILLA</h4>
                    <p class="mb-0">
                      Guanajuato brilla:  Del 17 de noviembre de 2023 al 7 de enero de 2024.
                      Parque Guanajuato Bicentenario te espera de 3 p.m. a 11 p.m. 🕒
                      Acceso  $140.
                    </p>

                    <hr>

                    <v-btn style="background-color: white; color: black; margin-top: 20px;">
                      <a href="https://agendacultural.guanajuato.gob.mx/evento/guanajuato-brilla/" style="text-decoration: none; text-transform: none; color: black;">
                        <v-icon style="color: black;">mdi-link</v-icon>
                        visitar sitio
                      </a>
                    </v-btn>
                  </div>
                  <div class="overlay" />
                </div>
              </div>

              <style>
                .event-card-9{
                background: url(https://www.connectando.mx/img/events/event_1701359981.jpg);
                background-size: cover;
                background-position: center center;
                }
              </style>
              <div class="col-md-4">
                <div class="event-card event-card-10">
                  <div class="date-detail">
                    <p>30</p>
                    <p>nov.</p>
                  </div>

                  <div class="content">
                    <div class="d-flex align-items-center justify-content-between">
                      <p><ion-icon name="calendar-outline" role="img" class="md hydrated" aria-label="calendar outline" /> 30 nov. - 2023</p>
                      <p><ion-icon name="time-outline" role="img" class="md hydrated" aria-label="time outline" /> </p>
                    </div>

                    <h4>EXPOSICIÓN TEMPORAL ARTE EXTRAMUROS «PERSPECTIVAS SIMULTÁNEAS. MIRADAS MEXICANAS»</h4>
                    <p class="mb-0">
                      Inicio:noviembre 24
                      Final:17 marzo, 2024
                      Costo:
                      Gratuito
                      Evento Categorías:200 anios GTO, Artes visuales
                      Museo de Arte e Historia de Guanajuato
                    </p>

                    <hr>

                    <v-btn style="background-color: white; color: black; margin-top: 20px;">
                      <a href="https://agendacultural.guanajuato.gob.mx/evento/exposicion-temporal-arte-extramuros-perspectivas-simultaneas-miradas-mexicanas/" style="text-decoration: none; text-transform: none; color: black;">
                        <v-icon style="color: black;">mdi-link</v-icon>
                        visitar sitio
                      </a>
                    </v-btn>
                  </div>
                  <div class="overlay" />
                </div>
              </div>

              <style>
                .event-card-10{
                background: url(https://www.connectando.mx/img/events/event_1701361272.jpg);
                background-size: cover;
                background-position: center center;
                }
              </style>
            </div>
          </div>
        </div>
      </div>

      <div>
        <v-card style="" color="#F1F6FB" align="center" elevation="0">
          <v-card-title class="justify-center">
            Beneficios
          </v-card-title>
          <v-img :src="require('@/assets/images/beneficios.png')" />
        </v-card>
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
  auth: false
}
</script>

<style scoped>
.align-items-center {
    align-items: center !important;
}
.event-card {
    position: relative;
    width: 100%;
    height: 550px;
    overflow: hidden;
    border-radius: 10px;
    color: #FFFFFF;
    margin-bottom: 30px;
}
.date-detail {
    position: absolute;
    top: 15px;
    right: 15px;
    color: black;
    background-color: white;
    padding: 10px;
    text-align: center;
    border-radius: 5px;
}
.content {
    position: absolute;
    bottom: 0px;
    left: 0px;
    width: 100%;
    padding: 30px;
}
.logo {
    width: 250px;
    mix-blend-mode: multiply;
    margin-right: 30px;
    margin-top: 50px;
}
</style>
