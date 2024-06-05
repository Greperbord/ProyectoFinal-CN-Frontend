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
      <div class="row align-items-center" style="background-color: white;">
        <div class="col-12 col-md-7 offset-md-1">
          <div>
            <span>Escoge tus asientos de ida  </span>

            <div class="row">
              <div class="col-md-4">
                <div class=" d-flex justify-space-between">
                  <div>
                    <v-icon>mdi-square-rounded</v-icon>
                    <span>Ocupado</span>
                  </div>
                  <div>
                    <v-icon>
                      mdi-square-rounded-outline
                    </v-icon>
                    <span>Dispobile</span>
                  </div>
                </div>
                <div style="margin-top: 50px;">
                  <v-img :src="require('@/assets/images/van-front.png')" />
                </div>
                <div>
                  <v-card>
                    <v-img :src="require('@/assets/images/asientos.png')" />
                  </v-card>
                </div>
                <div>
                  <v-img :src="require('@/assets/images/van-back.png')" />
                </div>
              </div>

              <div class="col-md-8">
                <v-card elevation="0" style="margin-top: 220px">
                  <div>
                    <v-card-title>Usuarios</v-card-title>
                    <v-card-text>
                      <v-divider />
                      <div class=" d-flex justify-space-between" style="margin-right: 70px;">
                        <div>
                          <span>Usuario 1</span>
                        </div>
                        <div>
                          <span>Asiento</span>
                        </div>
                      </div>
                      <div class="row">
                        <div class="col-md-4">
                          <v-text-field v-model="campo1" rounded label="Nombre(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-5">
                          <v-text-field v-model="campo2" rounded label="Apellido(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-3">
                          <v-select
                            v-model="asientoSeleccionado"
                            :items="asientosDisponibles"
                            :rules="[requerido]"
                            outlined
                          />
                          <div style="margin-top:-70px; margin-left: 40px;">
                            <span style="font-size:20px;">{{ asientoSeleccionado }}</span>
                          </div>
                        </div>
                      </div>
                    </v-card-text>
                  </div>
                  <div v-if="tourInfo.usuarios==2 || tourInfo.usuarios>1" style="margin-top: -60px">
                    <v-card-text>
                      <div class=" d-flex justify-space-between" style="margin-right: 70px;">
                        <div>
                          <span>Usuario 2</span>
                        </div>
                        <div>
                          <span>Asiento</span>
                        </div>
                      </div>
                      <div class="row">
                        <div class="col-md-4">
                          <v-text-field rounded label="Nombre(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-5">
                          <v-text-field rounded label="Apellido(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-3">
                          <v-select
                            v-model="asientoSeleccionado2"
                            :items="asientosDisponibles"
                            :rules="[requerido]"
                            outlined
                          />
                          <div style="margin-top:-70px; margin-left: 40px;">
                            <span style="font-size:20px;">{{ asientoSeleccionado2 }}</span>
                          </div>
                        </div>
                      </div>
                    </v-card-text>
                  </div>
                  <div v-if="tourInfo.usuarios==3 || tourInfo.usuarios>2" style="margin-top: -60px">
                    <v-card-text>
                      <div class=" d-flex justify-space-between" style="margin-right: 70px;">
                        <div>
                          <span>Usuario 3</span>
                        </div>
                        <div>
                          <span>Asiento</span>
                        </div>
                      </div>
                      <div class="row">
                        <div class="col-md-4">
                          <v-text-field rounded label="Nombre(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-5">
                          <v-text-field rounded label="Apellido(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-3">
                          <v-select
                            v-model="asientoSeleccionado3"
                            :items="asientosDisponibles"
                            :rules="[requerido]"
                            outlined
                          />
                          <div style="margin-top:-70px; margin-left: 40px;">
                            <span style="font-size:20px;">{{ asientoSeleccionado3 }}</span>
                          </div>
                        </div>
                      </div>
                    </v-card-text>
                  </div>
                  <div v-if="tourInfo.usuarios==4" style="margin-top: -60px">
                    <v-card-text>
                      <div class=" d-flex justify-space-between" style="margin-right: 70px;">
                        <div>
                          <span>Usuario 4</span>
                        </div>
                        <div>
                          <span>Asiento</span>
                        </div>
                      </div>
                      <div class="row">
                        <div class="col-md-4">
                          <v-text-field rounded label="Nombre(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-5">
                          <v-text-field rounded label="Apellido(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-3">
                          <v-select
                            v-model="asientoSeleccionado4"
                            :items="asientosDisponibles"
                            :rules="[requerido]"
                            outlined
                          />
                          <div style="margin-top:-70px; margin-left: 40px;">
                            <span style="font-size:20px;">{{ asientoSeleccionado4 }}</span>
                          </div>
                        </div>
                      </div>
                    </v-card-text>
                  </div>
                </v-card>
              </div>
            </div>
          </div>

          <div v-if="tourInfo.redondo" style="margin-top: 50px;">
            <span>Escoge tus asientos de regreso </span>

            <div class="row">
              <div class="col-md-8">
                <v-card elevation="0" style="margin-top: 220px">
                  <div>
                    <v-card-title>Usuarios</v-card-title>
                    <v-card-text>
                      <v-divider />
                      <div class=" d-flex justify-space-between" style="margin-right: 70px;">
                        <div>
                          <span>Usuario 1</span>
                        </div>
                        <div>
                          <span>Asiento</span>
                        </div>
                      </div>
                      <div class="row">
                        <div class="col-md-4">
                          <v-text-field v-model="campo3" rounded label="Nombre(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-5">
                          <v-text-field v-model="campo4" rounded label="Apellido(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-3">
                          <v-select
                            v-model="asientoSeleccionado5"
                            :items="asientosDisponibles2"
                            :rules="[requerido]"
                            outlined
                          />
                          <div style="margin-top:-70px; margin-left: 40px;">
                            <span style="font-size:20px;">{{ asientoSeleccionado5 }}</span>
                          </div>
                        </div>
                      </div>
                    </v-card-text>
                  </div>
                  <div v-if="tourInfo.usuarios==2 || tourInfo.usuarios>1" style="margin-top: -60px">
                    <v-card-text>
                      <div class=" d-flex justify-space-between" style="margin-right: 70px;">
                        <div>
                          <span>Usuario 2</span>
                        </div>
                        <div>
                          <span>Asiento</span>
                        </div>
                      </div>
                      <div class="row">
                        <div class="col-md-4">
                          <v-text-field rounded label="Nombre(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-5">
                          <v-text-field rounded label="Apellido(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-3">
                          <v-select
                            v-model="asientoSeleccionado6"
                            :items="asientosDisponibles2"
                            :rules="[requerido]"
                            outlined
                          />
                          <div style="margin-top:-70px; margin-left: 40px;">
                            <span style="font-size:20px;">{{ asientoSeleccionado6 }}</span>
                          </div>
                        </div>
                      </div>
                    </v-card-text>
                  </div>
                  <div v-if="tourInfo.usuarios==3 || tourInfo.usuarios>2" style="margin-top: -60px">
                    <v-card-text>
                      <div class=" d-flex justify-space-between" style="margin-right: 70px;">
                        <div>
                          <span>Usuario 3</span>
                        </div>
                        <div>
                          <span>Asiento</span>
                        </div>
                      </div>
                      <div class="row">
                        <div class="col-md-4">
                          <v-text-field rounded label="Nombre(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-5">
                          <v-text-field rounded label="Apellido(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-3">
                          <v-select
                            v-model="asientoSeleccionado7"
                            :items="asientosDisponibles2"
                            :rules="[requerido]"
                            outlined
                          />
                          <div style="margin-top:-70px; margin-left: 40px;">
                            <span style="font-size:20px;">{{ asientoSeleccionado7 }}</span>
                          </div>
                        </div>
                      </div>
                    </v-card-text>
                  </div>
                  <div v-if="tourInfo.usuarios==4" style="margin-top: -60px">
                    <v-card-text>
                      <div class=" d-flex justify-space-between" style="margin-right: 70px;">
                        <div>
                          <span>Usuario 4</span>
                        </div>
                        <div>
                          <span>Asiento</span>
                        </div>
                      </div>
                      <div class="row">
                        <div class="col-md-4">
                          <v-text-field rounded label="Nombre(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-5">
                          <v-text-field rounded label="Apellido(s)" outlined :rules="[requerido]" />
                        </div>
                        <div class="col-md-3">
                          <v-select
                            v-model="asientoSeleccionado8"
                            :items="asientosDisponibles2"
                            :rules="[requerido]"
                            outlined
                          />
                          <div style="margin-top:-70px; margin-left: 40px;">
                            <span style="font-size:20px;">{{ asientoSeleccionado8 }}</span>
                          </div>
                        </div>
                      </div>
                    </v-card-text>
                  </div>
                </v-card>
              </div>
              <div class="col-md-4">
                <div class=" d-flex justify-space-between">
                  <div>
                    <v-icon>mdi-square-rounded</v-icon>
                    <span>Ocupado</span>
                  </div>
                  <div>
                    <v-icon>
                      mdi-square-rounded-outline
                    </v-icon>
                    <span>Dispobile</span>
                  </div>
                </div>
                <div style="margin-top: 50px;">
                  <v-img :src="require('@/assets/images/van-front.png')" />
                </div>
                <div>
                  <v-card>
                    <v-img :src="require('@/assets/images/asientos.png')" />
                  </v-card>
                </div>
                <div>
                  <v-img :src="require('@/assets/images/van-back.png')" />
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="col-12 col-md-3 pa-2 ma-2">
          <h2>Resumen del pedido</h2>
          <v-card style="background-color: #FFE77B;" elevation="0">
            <v-card-text>
              <v-icon>mdi-timer-sand</v-icon>
              <span>!No pierdas tus lugares!</span>
              <br>
              <span style="margin-left: 30px;">Tu orden estará disponible por {{ timerCountMinutes }}:{{ timerCountSeconds }}</span>
            </v-card-text>
          </v-card>

          <v-card style="background-color: #0dcaf0; margin-top: 20px;" elevation="0">
            <v-card-title>
              <v-card style="background-color: #CFF4FC;">
                <v-card-text>
                  <span>Esta reservación es de un viaje turístico, </span>
                  <strong style="white-space: nowrap">revisa el itinerario del tour</strong>
                  <span>. No incluye accesos a eventos y puntos de interés.</span>
                </v-card-text>
              </v-card>
            </v-card-title>
            <v-card-text>
              <v-img :src="require('@/assets/images/van1.png')">
                <v-card max-width="100px" max-height="100px" elevation="0" style="background-color: rgba(0, 0, 0, 0.5); margin-left: 230px;">
                  <v-card-text>
                    <span>Unidad 3, 17 lugares</span>
                  </v-card-text>
                </v-card>
              </v-img>
              <v-card v-if="tourInfo.origen.state=='León'" id="origenLeon">
                <v-container class="d-flex justify-space-between">
                  <span>
                    <v-icon>mdi-circle</v-icon>
                    Oxxo Gas Plaza Mayor
                  </span>
                  <span>
                    {{ tourInfo.fechaSalida }}
                  </span>
                </v-container>

                <h5 style="color: gray; margin-left: 30px;">
                  Duración: 4:45 hrs.
                </h5>

                <v-container class="d-flex justify-space-between">
                  <span>
                    <v-icon>mdi-square</v-icon>
                    Ciudad de México
                  </span>
                </v-container>

                <v-divider />

                <v-container>
                  <span>Itinerario:</span>
                  <br>
                  <v-icon>mdi-circle</v-icon>
                  <small style="color: gray;">Tepozotlán</small>
                  <br>
                  <div style="width: 1px; height: 20px; background-color: gray; margin-left: 11px;" />
                  <v-icon>mdi-minus</v-icon>
                  <small style="color: gray;">Hotel JW Marriot Frente Auditorio Nacional</small>
                  <br>
                  <div style="width: 1px; height: 20px; background-color: gray; margin-left: 11px;" />
                  <v-icon>mdi-minus</v-icon>
                  <small style="color: gray;">Templo Mayor</small>
                  <br>
                  <div style="width: 1px; height: 20px; background-color: gray; margin-left: 11px;" />
                  <v-icon>mdi-square</v-icon>
                  <small style="color: gray;">Hotel JW MarriotFrente Auditorio Nacional</small>
                </v-container>
              </v-card>
              <v-card v-if="tourInfo.origen.state=='Ciudad de México'" id="origenCDMX">
                <v-container class="d-flex justify-space-between">
                  <span>
                    <v-icon>mdi-circle</v-icon>
                    Hotel JW Marriott
                  </span>
                  <span>
                    {{ tourInfo.fechaRegreso }}
                  </span>
                </v-container>

                <h5 style="color: gray; margin-left: 30px;">
                  Duración: 4:45 hrs.
                </h5>

                <v-container class="d-flex justify-space-between">
                  <span>
                    <v-icon>mdi-square</v-icon>
                    León
                  </span>
                </v-container>

                <v-divider />

                <v-container>
                  <span>Itinerario:</span>
                  <br>
                  <v-icon>mdi-circle</v-icon>
                  <small style="color: gray;">Estacionamiento Hotel Hotsson Smart Centro Max</small>
                  <br>
                  <div style="width: 1px; height: 20px; background-color: gray; margin-left: 11px;" />
                  <v-icon>mdi-minus</v-icon>
                  <small style="color: gray;">OxxoGas Plaza Mayor</small>
                  <br>
                  <div style="width: 1px; height: 20px; background-color: gray; margin-left: 11px;" />
                  <v-icon>mdi-minus</v-icon>
                  <small style="color: gray;">Forum Cultural</small>
                  <br>
                  <div style="width: 1px; height: 20px; background-color: gray; margin-left: 11px;" />
                  <v-icon>mdi-square</v-icon>
                  <small style="color: gray;">OxxoGas Plaza Mayor</small>
                </v-container>
              </v-card>
            </v-card-text>
            <v-card-text v-if="tourInfo.redondo">
              <v-img :src="require('@/assets/images/van2.png')">
                <v-card max-width="100px" max-height="100px" elevation="0" style="background-color: rgba(0, 0, 0, 0.5); margin-left: 230px;">
                  <v-card-text>
                    <span>Unidad 3, 17 lugares</span>
                  </v-card-text>
                </v-card>
              </v-img>
              <v-card v-if="tourInfo.destino.state=='Ciudad de México'" id="destinoCDMX">
                <v-container class="d-flex justify-space-between">
                  <span>
                    <v-icon>mdi-circle</v-icon>
                    Hotel JW Marriott
                  </span>
                  <span>
                    {{ tourInfo.fechaRegreso }}
                  </span>
                </v-container>

                <h5 style="color: gray; margin-left: 30px;">
                  Duración: 4:45 hrs.
                </h5>

                <v-container class="d-flex justify-space-between">
                  <span>
                    <v-icon>mdi-square</v-icon>
                    León
                  </span>
                </v-container>

                <v-divider />

                <v-container>
                  <span>Itinerario:</span>
                  <br>
                  <v-icon>mdi-circle</v-icon>
                  <small style="color: gray;">Estacionamiento Hotel Hotsson Smart Centro Max</small>
                  <br>
                  <div style="width: 1px; height: 20px; background-color: gray; margin-left: 11px;" />
                  <v-icon>mdi-minus</v-icon>
                  <small style="color: gray;">OxxoGas Plaza Mayor</small>
                  <br>
                  <div style="width: 1px; height: 20px; background-color: gray; margin-left: 11px;" />
                  <v-icon>mdi-minus</v-icon>
                  <small style="color: gray;">Forum Cultural</small>
                  <br>
                  <div style="width: 1px; height: 20px; background-color: gray; margin-left: 11px;" />
                  <v-icon>mdi-square</v-icon>
                  <small style="color: gray;">OxxoGas Plaza Mayor</small>
                </v-container>
              </v-card>
              <v-card v-if="tourInfo.destino.state=='León'" id="destinoLeon">
                <v-container class="d-flex justify-space-between">
                  <span>
                    <v-icon>mdi-circle</v-icon>
                    Oxxo Gas Plaza Mayor
                  </span>
                  <span>
                    {{ tourInfo.fechaSalida }}
                  </span>
                </v-container>

                <h5 style="color: gray; margin-left: 30px;">
                  Duración: 4:45 hrs.
                </h5>

                <v-container class="d-flex justify-space-between">
                  <span>
                    <v-icon>mdi-square</v-icon>
                    Ciudad de México
                  </span>
                </v-container>

                <v-divider />

                <v-container>
                  <span>Itinerario:</span>
                  <br>
                  <v-icon>mdi-circle</v-icon>
                  <small style="color: gray;">Tepozotlán</small>
                  <br>
                  <div style="width: 1px; height: 20px; background-color: gray; margin-left: 11px;" />
                  <v-icon>mdi-minus</v-icon>
                  <small style="color: gray;">Hotel JW Marriot Frente Auditorio Nacional</small>
                  <br>
                  <div style="width: 1px; height: 20px; background-color: gray; margin-left: 11px;" />
                  <v-icon>mdi-minus</v-icon>
                  <small style="color: gray;">Templo Mayor</small>
                  <br>
                  <div style="width: 1px; height: 20px; background-color: gray; margin-left: 11px;" />
                  <v-icon>mdi-square</v-icon>
                  <small style="color: gray;">Hotel JW MarriotFrente Auditorio Nacional</small>
                </v-container>
              </v-card>
            </v-card-text>
          </v-card>

          <v-card style="background-color: #0dcaf0; margin-top: 20px;" elevation="0">
            <v-card-title>
              <v-icon>mdi-briefcase-outline</v-icon>
              <span style="color: black;">Lineamientos de Equipaje</span>
            </v-card-title>
            <v-card-text>
              <v-divider />

              <span style="color: black;">Dimensiones</span>
              <br>
              <span>57 x 40 x 33 y un equipaje de mano que se ajuste al portaequipaje interno de la unidad.</span>
              <br>
              <br>
              <a href="/ayuda">Conoce nuestros términos y condiciones.</a>
            </v-card-text>
            <v-card-title>
              <v-icon>mdi-file-document-outline</v-icon>
              <span style="color: black;">Política de cambios y cancelaciones</span>
            </v-card-title>
            <v-card-text>
              <v-divider />

              <span style="color: black">Cambios</span>
              <br>
              <span style="color: red">
                <v-icon>mdi-close</v-icon>
                Esta CONNEXIÓN no permite cambios
              </span>
              <br>
              <br>
              <span style="color: black">Cancelación</span>
              <br>
              <span style="color: red">
                <v-icon>mdi-close</v-icon>
                No hay devoluciones ni cancelaciones para reservaciones pagadas.
              </span>
              <br>
              <br>
              <a href="/ayuda">Conoce nuestra política de cambios y cancelaciones.</a>
            </v-card-text>
          </v-card>

          <v-card v-if="tourInfo.redondo && tourInfo.checkbox" id="redondoExtra" style="background-color: #1C1D31; margin-top: 50px;" elevation="0">
            <v-card-text style="color: white;">
              <div class="d-flex justify-space-between">
                <span style="font-size: 10px;">CONNEXIÓN REDONDO</span>
                <span style="font-size: 10px;">${{ 700*tourInfo.usuarios }}</span>
              </div>
              <div class="d-flex justify-space-between">
                <span style="font-size: 10px;">EQUIPAJE EXTRA</span>
                <span style="font-size: 10px;">${{ 200*tourInfo.usuarios }}</span>
              </div>
              <v-divider color="white" />
              <div class="d-flex justify-space-between">
                <span style="font-size: 10px;">SUB-TOTAL</span>
                <span style="font-size: 10px;">${{ (200*tourInfo.usuarios)+(700*tourInfo.usuarios) }}</span>
              </div>
            </v-card-text>
            <v-card-title style="color: white;">
              <v-divider color="white" />
              <div class="d-flex justify-space-between">
                <span>TOTAL  ${{ (200*tourInfo.usuarios)+(700*tourInfo.usuarios) }}</span>
              </div>
            </v-card-title>
          </v-card>

          <v-card v-if="tourInfo.redondo && !tourInfo.checkbox" id="redondo" style="background-color: #1C1D31; margin-top: 50px;" elevation="0">
            <v-card-text style="color: white;">
              <div class="d-flex justify-space-between">
                <span style="font-size: 10px;">CONNEXIÓN REDONDO</span>
                <span style="font-size: 10px;">${{ 700*tourInfo.usuarios }}</span>
              </div>
              <v-divider color="white" />
              <div class="d-flex justify-space-between">
                <span style="font-size: 10px;">SUB-TOTAL</span>
                <span style="font-size: 10px;">${{ 700*tourInfo.usuarios }}</span>
              </div>
            </v-card-text>
            <v-card-title style="color: white;">
              <v-divider color="white" />
              <div class="d-flex justify-space-between">
                <span>TOTAL  ${{ 700*tourInfo.usuarios }}</span>
              </div>
            </v-card-title>
          </v-card>

          <v-card v-if="!tourInfo.redondo && tourInfo.checkbox" id="simpleExtra" style="background-color: #1C1D31; margin-top: 50px;" elevation="0">
            <v-card-text style="color: white;">
              <div class="d-flex justify-space-between">
                <span style="font-size: 10px;">CONNEXIÓN SENCILLO</span>
                <span style="font-size: 10px;">${{ 350*tourInfo.usuarios }}</span>
              </div>
              <div class="d-flex justify-space-between">
                <span style="font-size: 10px;">EQUIPAJE EXTRA</span>
                <span style="font-size: 10px;">${{ 100*tourInfo.usuarios }}</span>
              </div>
              <v-divider color="white" />
              <div class="d-flex justify-space-between">
                <span style="font-size: 10px;">SUB-TOTAL</span>
                <span style="font-size: 10px;">${{ (100*tourInfo.usuarios)+(350*tourInfo.usuarios) }}</span>
              </div>
            </v-card-text>
            <v-card-title style="color: white;">
              <v-divider color="white" />
              <div class="d-flex justify-space-between">
                <span>TOTAL  ${{ (100*tourInfo.usuarios)+(350*tourInfo.usuarios) }}</span>
              </div>
            </v-card-title>
          </v-card>

          <v-card v-if="!tourInfo.redondo && !tourInfo.checkbox" id="simple" style="background-color: #1C1D31; margin-top: 50px;" elevation="0">
            <v-card-text style="color: white;">
              <div class="d-flex justify-space-between">
                <span style="font-size: 10px;">CONNEXIÓN SENCILLO</span>
                <span style="font-size: 10px;">${{ 350*tourInfo.usuarios }}</span>
              </div>
              <v-divider color="white" />
              <div class="d-flex justify-space-between">
                <span style="font-size: 10px;">SUB-TOTAL</span>
                <span style="font-size: 10px;">${{ 350*tourInfo.usuarios }}</span>
              </div>
            </v-card-text>
            <v-card-title style="color: white;">
              <v-divider color="white" />
              <div class="d-flex justify-space-between">
                <span>TOTAL  ${{ 350*tourInfo.usuarios }}</span>
              </div>
            </v-card-title>
          </v-card>

          <v-card>
            <a class="btn-custom-bg text-center" style="text-decoration: none; text-transform: none; background-color: #00E697;" :class="{ 'disabled': !todosCamposCumplen }" @click="generarPDF">
              <v-icon>mdi-check</v-icon>
              CONFIRMAR COMPRA
            </a>
          </v-card>
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
import html2canvas from 'html2canvas'
import JsPDF from 'jspdf'

export default {
  auth: true,
  data () {
    return {
      tourInfo: [],
      trayectoInfo: [],
      timerCountMinutes: 9,
      timerCountSeconds: 59,
      requerido: value => !!value || 'Requerido.',
      asientos: ['A08', 'A09', 'A10', 'A11', 'A12', 'A13', 'A14', 'A15', 'A16', 'A17'],
      asientos2: ['A08', 'A09', 'A10', 'A11', 'A12', 'A13', 'A14', 'A15', 'A16', 'A17'],
      asientoSeleccionado: '',
      asientoSeleccionado2: '',
      asientoSeleccionado3: '',
      asientoSeleccionado4: '',
      asientoSeleccionado5: '',
      asientoSeleccionado6: '',
      asientoSeleccionado7: '',
      asientoSeleccionado8: '',
      asientosSeleccionados: [],
      asientosSeleccionados2: [],
      todosCamposCumplen: false,
      campo1: '',
      campo2: '',
      campo3: '',
      campo4: ''
    }
  },
  computed: {
    asientosDisponibles () {
      return this.asientos.filter(asiento => !this.asientosSeleccionados.includes(asiento))
    },
    asientosDisponibles2 () {
      return this.asientos2.filter(asiento => !this.asientosSeleccionados2.includes(asiento))
    }
  },
  watch: {
    asientoSeleccionado (newAsiento, oldAsiento) {
      this.validarCampos()
      const index = this.asientosSeleccionados.indexOf(oldAsiento)
      if (index !== -1) {
        this.asientosSeleccionados.splice(index, 1, newAsiento)
      } else {
        this.asientosSeleccionados.push(newAsiento)
      }
    },
    asientoSeleccionado2 (newAsiento, oldAsiento) {
      const index = this.asientosSeleccionados.indexOf(oldAsiento)
      if (index !== -1) {
        this.asientosSeleccionados.splice(index, 1, newAsiento)
      } else {
        this.asientosSeleccionados.push(newAsiento)
      }
    },
    asientoSeleccionado3 (newAsiento, oldAsiento) {
      const index = this.asientosSeleccionados.indexOf(oldAsiento)
      if (index !== -1) {
        this.asientosSeleccionados.splice(index, 1, newAsiento)
      } else {
        this.asientosSeleccionados.push(newAsiento)
      }
    },
    asientoSeleccionado4 (newAsiento, oldAsiento) {
      const index = this.asientosSeleccionados.indexOf(oldAsiento)
      if (index !== -1) {
        this.asientosSeleccionados.splice(index, 1, newAsiento)
      } else {
        this.asientosSeleccionados.push(newAsiento)
      }
    },
    asientoSeleccionado5 (newAsiento, oldAsiento) {
      this.validarCampos()
      const index = this.asientosSeleccionados2.indexOf(oldAsiento)
      if (index !== -1) {
        this.asientosSeleccionados2.splice(index, 1, newAsiento)
      } else {
        this.asientosSeleccionados2.push(newAsiento)
      }
    },
    asientoSeleccionado6 (newAsiento, oldAsiento) {
      const index = this.asientosSeleccionados2.indexOf(oldAsiento)
      if (index !== -1) {
        this.asientosSeleccionados2.splice(index, 1, newAsiento)
      } else {
        this.asientosSeleccionados2.push(newAsiento)
      }
    },
    asientoSeleccionado7 (newAsiento, oldAsiento) {
      const index = this.asientosSeleccionados2.indexOf(oldAsiento)
      if (index !== -1) {
        this.asientosSeleccionados2.splice(index, 1, newAsiento)
      } else {
        this.asientosSeleccionados2.push(newAsiento)
      }
    },
    asientoSeleccionado8 (newAsiento, oldAsiento) {
      const index = this.asientosSeleccionados2.indexOf(oldAsiento)
      if (index !== -1) {
        this.asientosSeleccionados2.splice(index, 1, newAsiento)
      } else {
        this.asientosSeleccionados2.push(newAsiento)
      }
    },
    timerCountMinutes: {
      handler (value) {
        if (value > 0) {
          setTimeout(() => {
            this.timerCountMinutes--
          }, 60000)
        }
      },
      immediate: true // This ensures the watcher is triggered upon creation
    },
    timerCountSeconds: {
      handler (value) {
        if (value > 0) {
          setTimeout(() => {
            this.timerCountSeconds--
          }, 1000)
        } else {
          value = 59
        }
      },
      immediate: true // This ensures the watcher is triggered upon creation
    },
    campo1 (newValue) {
      this.validarCampos()
    },
    campo2 (newValue) {
      this.validarCampos()
    },
    campo3 (newValue) {
      this.validarCampos()
    },
    campo4 (newValue) {
      this.validarCampos()
    }
  },
  created () {
    this.loadTourInfo()
    this.loadTrayectoInfo()
  },
  methods: {
    loadTourInfo () {
      const tourInfo = JSON.parse(localStorage.getItem('tourInfo')) || []
      this.tourInfo = tourInfo
      this.redondo = tourInfo.redondo
      this.usuarios = tourInfo.usuarios
      this.fechaSalida = tourInfo.fechaSalida
      this.fechaRegreso = tourInfo.fechaRegreso
      this.origen = tourInfo.origen
      this.destino = tourInfo.destino
      this.checkbox = tourInfo.checkbox
    },
    loadTrayectoInfo () {
      const trayectoInfo = JSON.parse(localStorage.getItem('trayectoInfo')) || []
      this.trayectoInfo = trayectoInfo
      this.CDMXA = trayectoInfo.CDMXA
      this.CDMXA2 = trayectoInfo.CDMXA2
      this.CDMXB = trayectoInfo.CDMXB
      this.CDMXB2 = trayectoInfo.CDMXB2
      this.LeonA = trayectoInfo.LeonA
      this.LeonA2 = trayectoInfo.LeonA2
      this.LeonB = trayectoInfo.LeonB
      this.LeonB2 = trayectoInfo.LeonB2
    },
    generarPDF () {
      const pdf = new JsPDF('p', 'mm', 'a4')
      const text = 'Asientos ida: '
      const textj = 'Asientos regreso: '

      const text1 = `${this.asientoSeleccionado},`
      const text2 = `${this.asientoSeleccionado2},`
      const text3 = `${this.asientoSeleccionado3},`
      const text4 = `${this.asientoSeleccionado4}`

      const text5 = `${this.asientoSeleccionado5},`
      const text6 = `${this.asientoSeleccionado6},`
      const text7 = `${this.asientoSeleccionado7},`
      const text8 = `${this.asientoSeleccionado8}`

      pdf.text(text, 10, 10)

      pdf.text(text1, 20, 20)
      pdf.text(text2, 20, 30)
      pdf.text(text3, 20, 40)
      pdf.text(text4, 20, 50)

      pdf.text(textj, 130, 140)
      pdf.text(text5, 140, 150)
      pdf.text(text6, 140, 160)
      pdf.text(text7, 140, 170)
      pdf.text(text8, 140, 180)

      // Agregar imagen capturada
      const cardElement = document.getElementById('origenLeon')
      const cardElement2 = document.getElementById('destinoCDMX')

      const cardPagoRE = document.getElementById('redondoExtra')
      const cardPagoR = document.getElementById('redondo')
      const cardPagoSE = document.getElementById('simpleExtra')
      const cardPagoS = document.getElementById('simple')

      html2canvas(cardElement).then((canvas) => {
        const imgData = canvas.toDataURL('image/png')
        const imgWidth = 100
        const imgHeight = imgWidth * (canvas.height / canvas.width)
        pdf.addImage(imgData, 'PNG', 100, 0, imgWidth, imgHeight)

        html2canvas(cardElement2).then((canvas) => {
          const imgData = canvas.toDataURL('image/png')
          const imgWidth = 100
          const imgHeight = imgWidth * (canvas.height / canvas.width)
          pdf.addImage(imgData, 'PNG', 0, 130, imgWidth, imgHeight)

          if (this.tourInfo.redondo && this.tourInfo.checkbox) {
            html2canvas(cardPagoRE).then((canvas) => {
              const imgData = canvas.toDataURL('image/png')
              const imgWidth = 100
              const imgHeight = imgWidth * (canvas.height / canvas.width)
              pdf.addImage(imgData, 'PNG', 100, 240, imgWidth, imgHeight)
              pdf.save('ticket.pdf')
              this.$router.push({ name: 'thanks' })
            })
          }
          if (this.tourInfo.redondo && !this.tourInfo.checkbox) {
            html2canvas(cardPagoR).then((canvas) => {
              const imgData = canvas.toDataURL('image/png')
              const imgWidth = 100
              const imgHeight = imgWidth * (canvas.height / canvas.width)
              pdf.addImage(imgData, 'PNG', 100, 240, imgWidth, imgHeight)
              pdf.save('ticket.pdf')
              this.$router.push({ name: 'thanks' })
            })
          }
          if (!this.tourInfo.redondo && this.tourInfo.checkbox) {
            html2canvas(cardPagoSE).then((canvas) => {
              const imgData = canvas.toDataURL('image/png')
              const imgWidth = 100
              const imgHeight = imgWidth * (canvas.height / canvas.width)
              pdf.addImage(imgData, 'PNG', 100, 240, imgWidth, imgHeight)
              pdf.save('ticket.pdf')
              this.$router.push({ name: 'thanks' })
            })
          }
          if (!this.tourInfo.redondo && !this.tourInfo.checkbox) {
            html2canvas(cardPagoS).then((canvas) => {
              const imgData = canvas.toDataURL('image/png')
              const imgWidth = 100
              const imgHeight = imgWidth * (canvas.height / canvas.width)
              pdf.addImage(imgData, 'PNG', 100, 240, imgWidth, imgHeight)
              pdf.save('ticket.pdf')
              this.$router.push({ name: 'thanks' })
            })
          }
        })
      })
    },
    validarCampos () {
      this.todosCamposCumplen = !!this.campo1 && !!this.campo2 && !!this.asientoSeleccionado && !!this.campo3 && !!this.campo4 && !!this.asientoSeleccionado5
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
.btn-custom-bg {
    background-color: var(--green);
    border-color: var(--green);
    border: none;
    padding: 17px 30px;
    display: block;
    color: #333333;
    width: 100%;
    text-transform: uppercase;
    font-weight: bold;
}
.disabled {
  pointer-events: none;
  opacity: 0.5;
}
</style>
