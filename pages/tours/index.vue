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
      <section style="background-color: #f2f2f2; padding: 12px 0px;">
        <div class="container">
          <div class="row">
            <div class="col-md-5">
              <h5 style="font-weight: 700;">
                Selecciona tu horario de ida...
              </h5>
            </div>

            <div v-if="tourInfo.redondo" class="col-md-5 offset-md-2">
              <h5 style="font-weight: 700;">
                Selecciona tu horario de regreso...
              </h5>
            </div>
          </div>
        </div>
      </section>

      <section style="background-color: white; padding: 12px 0px;">
        <div class="container">
          <div class="row">
            <div class="col-md-5">
              <v-card elevation="0">
                <h5 style="font-weight: 700;">
                  {{ tourInfo.fechaSalida }}
                </h5>
                <h3 style="margin-top: 5px">
                  <span>Origen: </span>
                  <span style="color: #00E697;">{{ tourInfo.origen.state }}</span>
                  <v-icon style="margin-left: 50px; color: #03AA71;">
                    mdi-train-car-passenger
                  </v-icon>
                  <span style="margin-left: 50px;">Destino: </span>
                  <span style="color: #00E697;">{{ tourInfo.destino.state }}</span>
                </h3>
                <h5 style="margin-top: 20px">
                  <v-icon style="color: #00E697;">
                    mdi-check-circle
                  </v-icon>
                  <span>CONNEXIÓN</span>
                  <span v-if="tourInfo.redondo">
                    Redondo
                  </span>
                  <span v-else>
                    Sencillo
                  </span>
                  <span style="margin-left: 30px">
                    <v-icon>mdi-account-group-outline</v-icon>
                    <span>{{ tourInfo.usuarios }} usuario(s)</span>
                  </span>
                  <span style="margin-left: 30px">
                    <v-icon style="color: #00E697;">
                      mdi-check-circle
                    </v-icon>
                    <span v-if="tourInfo.checkbox">
                      Equipaje extra
                    </span>
                  </span>
                </h5>
              </v-card>
              <v-card v-if="tourInfo.origen.state=='León'" style="background-color: #1C1D31; color: white;" elevation="0">
                <v-card-title>
                  <span>PUNTO DE ENCUENTRO</span>
                  <v-spacer />
                  <span>Tour: </span>
                  <span>
                    <v-img :src="require('@/assets/images/tm.png')" /></span>
                </v-card-title>
                <v-card-text>
                  <v-card elevation="0" style="border-radius: 10px;">
                    <v-card-subtitle style="color: black">
                      <v-checkbox v-model="trayectoInfo.LeonA" style="color: #00E697;" label="Seleccionar" />

                      <v-container class="d-flex justify-space-between">
                        <span>
                          <v-icon>mdi-circle</v-icon>
                          Oxxo Gas Plaza Mayor
                        </span>
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          06:00 am
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
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          10:45 am
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
                    </v-card-subtitle>
                    <v-container class="d-flex justify-space-between" style="background-color: #333446; color: white">
                      <span>
                        Lugares disponibles: 10
                      </span>
                      <span>
                        $350 c/u
                      </span>
                    </v-container>
                  </v-card>
                  <v-card elevation="0" style="border-radius: 10px; margin-top: 30px;">
                    <v-card-subtitle style="color: black">
                      <v-checkbox v-model="trayectoInfo.LeonB" style="color: #00E697;" label="Seleccionar" />

                      <v-container class="d-flex justify-space-between">
                        <span>
                          <v-icon>mdi-circle</v-icon>
                          Oxxo Gas Plaza Mayor
                        </span>
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          10:00 am
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
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          02:45 pm
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
                    </v-card-subtitle>
                    <v-container class="d-flex justify-space-between" style="background-color: #333446; color: white">
                      <span>
                        Lugares disponibles: 10
                      </span>
                      <span>
                        $350 c/u
                      </span>
                    </v-container>
                  </v-card>
                </v-card-text>
              </v-card>
              <v-card v-if="tourInfo.origen.state=='Ciudad de México'" style="background-color: #1C1D31; color: white;" elevation="0">
                <v-card-title>
                  <span>PUNTO DE ENCUENTRO</span>
                  <v-spacer />
                  <span>Tour: </span>
                  <span>
                    <v-img :src="require('@/assets/images/fc.png')" />
                  </span>
                </v-card-title>
                <v-card-text>
                  <v-card elevation="0" style="border-radius: 10px;">
                    <v-card-subtitle style="color: black">
                      <v-checkbox v-model="trayectoInfo.CDMXA" style="color: #00E697;" label="Seleccionar" />
                      <v-container class="d-flex justify-space-between">
                        <span>
                          <v-icon>mdi-circle</v-icon>
                          Hotel JW Marriott
                        </span>
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          09:00 am
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
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          01:45 pm
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
                    </v-card-subtitle>
                    <v-container class="d-flex justify-space-between" style="background-color: #333446; color: white">
                      <span>
                        Lugares disponibles: 10
                      </span>
                      <span>
                        $350 c/u
                      </span>
                    </v-container>
                  </v-card>
                  <v-card elevation="0" style="border-radius: 10px; margin-top: 30px;">
                    <v-card-subtitle style="color: black">
                      <v-checkbox v-model="trayectoInfo.CDMXB" style="color: #00E697;" label="Seleccionar" />
                      <v-container class="d-flex justify-space-between">
                        <span>
                          <v-icon>mdi-circle</v-icon>
                          Hotel JW Marriott
                        </span>
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          01:00 pm
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
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          05:45 pm
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
                    </v-card-subtitle>
                    <v-container class="d-flex justify-space-between" style="background-color: #333446; color: white">
                      <span>
                        Lugares disponibles: 10
                      </span>
                      <span>
                        $350 c/u
                      </span>
                    </v-container>
                  </v-card>
                </v-card-text>
              </v-card>
            </div>

            <div v-if="tourInfo.redondo" class="col-md-5 offset-md-2">
              <v-card elevation="0">
                <h5 style="font-weight: 700;">
                  {{ tourInfo.fechaRegreso }}
                </h5>
                <h3>
                  <span>Origen: </span>
                  <span style="color: #00E697;">{{ tourInfo.destino.state }}</span>
                  <v-icon style="margin-left: 50px; color: #03AA71">
                    mdi-train-car-passenger
                  </v-icon>
                  <span style="margin-left: 50px;">Destino: </span>
                  <span style="color: #00E697;">{{ tourInfo.origen.state }}</span>
                </h3>
                <h5 style="margin-top: 20px">
                  <v-icon style="color: #00E697;">
                    mdi-check-circle
                  </v-icon>
                  <span>CONNEXIÓN</span>
                  <span v-if="tourInfo.redondo">
                    Redondo
                  </span>
                  <span v-else>
                    Sencillo
                  </span>
                  <span style="margin-left: 30px">
                    <v-icon>mdi-account-group-outline</v-icon>
                    <span>{{ tourInfo.usuarios }} usuario(s)</span>
                  </span>
                  <span style="margin-left: 30px">
                    <span v-if="tourInfo.checkbox">
                      Equipaje extra
                    </span>
                  </span>
                </h5>
              </v-card>
              <v-card v-if="tourInfo.destino.state=='Ciudad de México'" style="background-color: #1C1D31; color: white;" elevation="0">
                <v-card-title>
                  <span>PUNTO DE ENCUENTRO</span>
                  <v-spacer />
                  <span>Tour: </span>
                  <span>
                    <v-img :src="require('@/assets/images/fc.png')" />
                  </span>
                </v-card-title>
                <v-card-text>
                  <v-card elevation="0" style="border-radius: 10px;">
                    <v-card-subtitle style="color: black">
                      <v-checkbox v-model="trayectoInfo.CDMXA2" style="color: #00E697;" label="Seleccionar" />
                      <v-container class="d-flex justify-space-between">
                        <span>
                          <v-icon>mdi-circle</v-icon>
                          Hotel JW Marriott
                        </span>
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          09:00 am
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
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          01:45 pm
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
                    </v-card-subtitle>
                    <v-container class="d-flex justify-space-between" style="background-color: #333446; color: white">
                      <span>
                        Lugares disponibles: 10
                      </span>
                      <span>
                        $350 c/u
                      </span>
                    </v-container>
                  </v-card>
                  <v-card elevation="0" style="border-radius: 10px; margin-top: 30px;">
                    <v-card-subtitle style="color: black">
                      <v-checkbox v-model="trayectoInfo.CDMXB2" style="color: #00E697;" label="Seleccionar" />
                      <v-container class="d-flex justify-space-between">
                        <span>
                          <v-icon>mdi-circle</v-icon>
                          Hotel JW Marriott
                        </span>
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          12:00 pm
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
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          04:45 pm
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
                    </v-card-subtitle>
                    <v-container class="d-flex justify-space-between" style="background-color: #333446; color: white">
                      <span>
                        Lugares disponibles: 10
                      </span>
                      <span>
                        $350 c/u
                      </span>
                    </v-container>
                  </v-card>
                </v-card-text>
              </v-card>
              <v-card v-if="tourInfo.destino.state=='León'" style="background-color: #1C1D31; color: white;" elevation="0">
                <v-card-title>
                  <span>PUNTO DE ENCUENTRO</span>
                  <v-spacer />
                  <span>Tour: </span>
                  <span>
                    <v-img :src="require('@/assets/images/tm.png')" /></span>
                </v-card-title>
                <v-card-text>
                  <v-card elevation="0" style="border-radius: 10px;">
                    <v-card-subtitle style="color: black">
                      <v-checkbox v-model="trayectoInfo.LeonA2" style="color: #00E697;" label="Seleccionar" />

                      <v-container class="d-flex justify-space-between">
                        <span>
                          <v-icon>mdi-circle</v-icon>
                          Oxxo Gas Plaza Mayor
                        </span>
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          06:00 am
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
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          10:45 am
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
                    </v-card-subtitle>
                    <v-container class="d-flex justify-space-between" style="background-color: #333446; color: white">
                      <span>
                        Lugares disponibles: 10
                      </span>
                      <span>
                        $350 c/u
                      </span>
                    </v-container>
                  </v-card>
                  <v-card elevation="0" style="border-radius: 10px; margin-top: 30px;">
                    <v-card-subtitle style="color: black">
                      <v-checkbox v-model="trayectoInfo.LeonB2" style="color: #00E697;" label="Seleccionar" />

                      <v-container class="d-flex justify-space-between">
                        <span>
                          <v-icon>mdi-circle</v-icon>
                          Oxxo Gas Plaza Mayor
                        </span>
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          09:00 am
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
                        <span>
                          <v-icon>mdi-clock-time-five-outline</v-icon>
                          01:45 pm
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
                    </v-card-subtitle>
                    <v-container class="d-flex justify-space-between" style="background-color: #333446; color: white">
                      <span>
                        Lugares disponibles: 10
                      </span>
                      <span>
                        $350 c/u
                      </span>
                    </v-container>
                  </v-card>
                </v-card-text>
              </v-card>
            </div>
          </div>
        </div>
      </section>

      <div class="checkout-confirm">
        <div class="container">
          <div class="row">
            <div class="col-md-4 offset-md-4 text-center mt-5">
              <div class="trip-info d-flex align-items-center justify-content-between" style="display:none; box-shadow: 0px -5px 20px rgba(0,0,0,0.4);">
                <p class="mb-0">
                  <v-icon>mdi-account-group-outline</v-icon>
                  {{ tourInfo.usuarios }} usuario(s)
                </p>
                <p v-if="isSelected1 && isSelected2 && tourInfo.redondo" style="margin-left: 185px;">
                  $ {{ 700*tourInfo.usuarios }}
                </p>
                <p v-if="isSelected1 && isSelected2 && tourInfo.sencillo && !tourInfo.redondo" style="margin-left: 185px;">
                  $ {{ 350*tourInfo.usuarios }}
                </p>
              </div>

              <a v-if="((trayectoInfo.LeonA || trayectoInfo.LeonB) || (trayectoInfo.CDMXA || trayectoInfo.CDMXB)) && ((trayectoInfo.LeonA2 || trayectoInfo.LeonB2) || (trayectoInfo.CDMXA2 || trayectoInfo.CDMXB2)) && tourInfo.redondo" href="/payment" class="btn-custom-bg text-center" style="text-decoration: none; text-transform: none; background-color: #00E697;" @click="saveAndGoToPayment">
                Continuar con mi selección
              </a>
              <a v-if="((trayectoInfo.LeonA || trayectoInfo.LeonB) || (trayectoInfo.CDMXA || trayectoInfo.CDMXB)) && ((trayectoInfo.LeonA2 || trayectoInfo.LeonB2) || (trayectoInfo.CDMXA2 || trayectoInfo.CDMXB2)) && !tourInfo.redondo" href="/payment" class="btn-custom-bg text-center" style="text-decoration: none; text-transform: none; background-color: #00E697;" @click="saveAndGoToPayment">
                Continuar con mi selección
              </a>
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
  auth: true,
  data () {
    return {
      tourInfo: [],
      trayectoInfo: {
        LeonA: false,
        LeonB: false,
        LeonA2: false,
        LeonB2: false,
        CDMXA: false,
        CDMXB: false,
        CDMXA2: false,
        CDMXB2: false
      }
    }
  },
  created () {
    this.loadTourInfo()
    const savedTrayectoInfo = localStorage.getItem('trayectoInfo')
    if (savedTrayectoInfo) {
      this.trayectoInfo = JSON.parse(savedTrayectoInfo)
    }
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
    saveAndGoToPayment () {
      this.saveTrayectoInfo()
      this.goToPayment()
    },
    saveTrayectoInfo () {
      const trayectoInfo = JSON.stringify(this.trayectoInfo)
      localStorage.setItem('trayectoInfo', trayectoInfo)
    },
    goToPayment () {
      this.$router.push({ name: 'payment', query: { ...this.trayectoInfo } })
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
.checkout-confirm {
    position: fixed;
    bottom: -11px;
    width: 100%;
    z-index: 99;
}
.row {
    --bs-gutter-x: 1.5rem;
    --bs-gutter-y: 0;
    display: flex;
    flex-wrap: wrap;
    margin-top: calc(-1* var(--bs-gutter-y));
    margin-right: calc(-.5* var(--bs-gutter-x));
    margin-left: calc(-.5* var(--bs-gutter-x));
}
.text-center {
    text-align: center !important;
}
.trip-info {
    background-color:white;
    color: black;
    padding: 10px 15px;
    border-radius: 15px 15px 0px 0px;
    position: relative;
    z-index: 2;
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
</style>
