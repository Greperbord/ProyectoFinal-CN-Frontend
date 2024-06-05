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

    <v-main class="white">
      <section style="background-color: white">
        <div class="container mt-5" style="text-align: center">
          <div>
            <small style="text-transform: uppercase !important;">Ayuda y Soporte</small>
            <h3>Preguntas Frecuentes</h3>
          </div>
        </div>

        <div class="container" style="background-color: white;">
          <v-expansion-panels accordion>
            <v-expansion-panel>
              <v-expansion-panel-header>¿QUIENES SOMOS?</v-expansion-panel-header>
              <v-expansion-panel-content>
                Somos una empresa 100% mexicana de base tecnológica, que coordina grupos de personas con un mismo interés y destino, las connectamos con empresas de transporte turístico para la prestación de los servicios de traslado. En CONNECTANDO, cuidamos que todas las unidades afiliadas a la plataforma cuenten con un mismo estándar de calidad y servicio, ofreciendo cobertura de seguro de viajero, unidades de 18 pasajeros equipadas con A/C, sistema de entretenimiento durante el trayecto y conductores capacitados que harán de su viaje la mejor experiencia.
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>¿CÓMO RESERVO? (Necesito registrarme para reservar?)</v-expansion-panel-header>
              <v-expansion-panel-content>
                Hay dos formas de reservar. Como “USUARIO REGISTRADO” y como “INVITADO”. USUARIO: Los usuarios tienen todos los beneficios a diferencia de los invitados. Los usuarios registrados tienen la opción de: Elegir el asiento en el que quieren viajar, pagar en efectivo al momento de abordar, editar las fechas de su viaje todas las veces que necesiten sin costos o penalizaciones solo respetando los tiempos que establecen nuestros “Términos y Condiciones”; además pueden participar en promociones como “Viajero Frecuente” donde después de la quinta reservación pagada reciben un viaje gratis. Si eres usuario ingresa a nuestra página web www.connectando.mx o a nuestra App CONNECTANDO, pon tu usuario (correo electrónico), contraseña para ingresar a tu perfil. Ya adentro comienza el proceso de reservación. INVITADO: Los invitados no necesitan registrarse, solo deben ingrsar a la página web www.connectando.mx y realiza el proceso de reservación.
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>¿CÓMO ME REGISTO?</v-expansion-panel-header>
              <v-expansion-panel-content>
                1.- Entra a www.connectando.mx y dale clic a “Registrarse" , llena el formulario, registra tu tarjeta de débito/crédito y listo (se aceptan todas las tarjetas bancarias excepto Visa Electrón). 2.- Baja nuestra APP “CONNECTANDO”. Y dale clic en “Regístrate”, registra tu tarjeta de débito/crédito y listo (se aceptan todas las tarjetas bancarias excepto Visa Electrón). O al momento de hacer tu proceso de reservación en uno de los pasos te aparecerá la opción de registrarte.
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>EQUIPAJE PERMITIDO Y EXTRA EQUIPAJE</v-expansion-panel-header>
              <v-expansion-panel-content>
                Cada pasajero podrá llevar como equipaje permitido una maleta, ésta deberá ir sin excepción en el compartimento de equipaje y no deberá exceder las siguientes medidas: 60x42x33. También podrá llevar una mochila del tamaño escolar o bolsa de mano que se ajuste al porta-equipaje interno. EXTRA-EQUIPAJE El extra equipaje tiene un costo adicional a la reservación y se tiene que REPORTAR seleccionando la opción al reservar. Puede seleccionar solo una de las dos opciones de extra equipaje. 1) En caso de llevar equipaje más grande del permitido se tomará como extra equipaje y la medida de maleta solo podrá pasar a la medida siguiente que es 70X46X35. 2) Si tiene la necesidad de llevar equipaje adicional, se debe ajustar a medida permitida y además se hará un cobro de extra equipaje; si pre-paga el extra equipaje al momento de reservar, el costo será de $100 (cien pesos) en medida permitida o maleta extra. En caso de llevar otra maleta solo se permitirá si se ajusta a la maleta permitida que es 60x42x33, no se podrá en este caso llevar maleta más grande a estas medidas. Hacemos de su conocimiento que por Tour solo está permitido que dos reservaciones lleven extra equipaje en cualquiera de sus modalidades, por lo que se recomienda seleccionarlo al reservar. Al seleccionar el extra equipaje desde el momento de reservar el costo es de $100 (cien pesos), si no se selecciona y paga al reservar, al llegar su salida el costo será el doble de lo estipulado $200 y además estará sujeto a disponibilidad de espacio. Por ningún motivo podrá el usuario llevar el equipaje en el interior de la cabina. En caso de no aceptar estas condiciones, el usuario no podrá llevar el equipaje excedente, y si no quiere viajar con esas condiciones perderá su reservación y no se realizará ningún reembolso.
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>VIAJE CON MASCOTAS</v-expansion-panel-header>
              <v-expansion-panel-content>
                Para la transportación de mascotas, estas deberán ser de razas pequeñas (perros o gatos de tamaño pequeño, cuyo peso adulto no excede 10 kg), deberán ir en caja transportadora rígida chica con medidas 53 x 41 x Alt. 38 cm y preferentemente tranquilizados (checarlo con su veterinario) Las mascotas viajarán en la zona de equipaje de la unidad, sin excepción. Solo las mascotas de compañía o asistencia emocional podrán estar con sus dueños, previa presentación en original del certificado médico que así lo acredite; necesitarán además hacer una reservación para la mascota y que vaya junto al usuario que lo lleve. Deberá el dueño hacerse responsable de la limpieza del espacio que ocupe la mascota (pelos, vómito, orina) por lo anterior hay que llevar de manera obligatoria un protector para el asiento, hay que tomar en cuenta que viajan más usuarios. En caso de que no se lleve el protector se hará un cobro extraordinario de $150 ciento cincuenta pesos para poder dar limpieza al asiento. Los usuarios o invitados podrán llevar su mascota en una caja transportadora. En caso de llevar más de una caja transportadora, deberán consultar la viabilidad en el número de atención y estará sujeto su traslado a que haya espacio, se cobrará además un costo extraordinario de $250. En caso de no encontrar espacio, la caja transportadora con la mascota no podrá viajar y por ningún motivo podrá el usuario llevarlo consigo en el interior de la cabina. Si el usuario o invitado no aceptar estas condiciones, se perderá su reservación y no se realizará ningún reembolso.
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>¿LOS NIÑOS Y ADULTOS MAYORES PAGAN LO MISMO?</v-expansion-panel-header>
              <v-expansion-panel-content>
                No manejamos costos diferenciados. Por seguridad todos los viajantes deben ocupar un asiento. Por lo anterior, los niños de cualquier edad y personas de la tercera edad deberán tener su reservación para poder viajar. El costo será el establecido en viaje sencillo o redondo. Lo invitamos a leer nuestros términos y condiciones
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>ENVIOS</v-expansion-panel-header>
              <v-expansion-panel-content>
                ¿Se te olvidó algo? Envíalo con nosotros a un costo muy accesible. (Leer hasta el final) Solo necesitas confirmarnos por WhatsApp: El tamaño de tu envío, nombre de quien envía, día de envío, hora, punto de encuentro y qué envías. Hay que entregar además al conductor una tarjeta con el nombre y teléfono de quién manda y recibe. Se entregan los artículos o sobres en la salida de las unidades y se recogen en la llegada en los puntos de encuentro establecidos. El pago se hace en efectivo al conductor al momento de entregar el paquete para ser enviado. Es importante recalcar que la puntualidad o no de las llegadas de las unidades, depende de las circunstancias de tránsito o percances que encuentren en las vialidades en la ciudad o carretera; estas situaciones están fuera de nuestras manos controlar, por lo que es decisión del usuario elegir ésta opción de servicio. Es responsabilidad completamente de los usuarios el NO recoger en tiempo y forma de acuerdo a lo establecido los envíos. Tendrán 1 un mes para recoger el envíos que no hayan recogido previa confirmación de la empresa de que tiene en resguardo el objeto. De no hacerlo así los objetos serán tirados o donados dependiendo el caso. Los artículos perecederos se desechará de inmediato. La empresa decidirá la, las instituciones o personas a quién se donará los objetos. Es también responsabilidad de los usuarios leer esta información, al aceptar este servicio acepta también que leyó y aceptó la política y metodología de este servicio.
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>OBJETOS OLVIDADOS</v-expansion-panel-header>
              <v-expansion-panel-content>
                La empresa no se hace responsable de objetos olvidados en nuestras unidades. En caso de que los operadores encuentren algún objeto olvidado, lo reportarán y entregarán en nuestra oficina "Lobby café" ubicado en: Centro Max ( Junto al hotel Hotsson Smart. Blvd. Adolfo López Mateos 2510. Jardines de Jerez). Los artículos perecederos serán desechados de inmediato. Los demás artículos serán resguardados solo un mes a partir de la notificación. Desafortunadamente no contamos con espacio para dejar más tiempo los artículos olvidados. Por lo que después de este tiempo la empresa los desechará o en su caso donará.
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>DATOS DE CONTACTO</v-expansion-panel-header>
              <v-expansion-panel-content>
                Teléfono y Whatsapp : 4775696726 correo: hola@connectando.mx instagram y facebook: connectando mx
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>¿CÓMO FACTURO?</v-expansion-panel-header>
              <v-expansion-panel-content>
                Solo se facturas reservaciones hechas y pagadas en el mes corriente. Para solicitar su factura electrónica, es necesario envíe por WhatsApp al número de atención 4775696726 su petición incluyendo: imagen de la reservación que desea facturar, datos fiscales completos en caso de ser la primera vez, razón social si ya se ha facturado, uso del CFDI, correo electrónico. El horario de solicitud es hasta las 5:00 pm del ultimo día hábil (lunes a viernes de 9:00 am a 17:00 pm) del mes. Una vez emitida la factura ya no se podrá hacer ningún cambio o cancelación en la misma. En caso de que su viaje sea en fin de semana y últimos días de mes le recomendamos elija una opción de prepago y solicite su factura dentro de los tiempos antes mencionados. Las facturas se envían al correo electrónico proporcionado y se pueden y se emiten de dos a tres días hábiles en horarios de oficina.
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>¿PUNTOS DE ENCUENTRO PARA SUBIR, BAJAR y TIEMPO DE VIAJE?</v-expansion-panel-header>
              <v-expansion-panel-content>
                TIEMPOS DE VIAJE 4:20 hrs aproximadamente. Es importante comentar que siendo puntos de encuentro la unidad se puede estacionar en un punto distinto, depende de la viabilidad por lo anterior se informará a través del centro de mensajes en la App o web y en la notificación de llegada del conductor en la App con el mapa de ubicación. Si hay alguna duda se pueden comunicar en tiempo con el área de atención a clientes para su apoyo. Los puntos de encuentro para subir o bajar en CDMX-León-Guadalajara son los mismos. En León: Plaza Mayor – Oxxo Gas frente a wallmart (Blvd. Cloutier esquina Blvd. Cerro Gordo Centro Max - Estacionamiento del hotel Hotsson Smart (Blvd. Adolfo López Mateos 2510. Jardines de Jerés) CDMX: JW Marriott frente al Auditorio Nacional (Andrés Bello 29, Polanco V secc. Miguel Hidalgo) Tepozotlán. Burger King que está antes de la caseta (Autopista México-Querétaro, Km 42.5 s/n Texcacoa Tepozotlán. GUADALAJARA: Oxxo a un lado del Hotel Ríu (Av. Lázaro Cárdenas esquina Av. Adolfo López Mateos)
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>¿QUÉ PASA SI VENCE LA VIGENCIA DE LA REFERENCIA DE VIAJE?</v-expansion-panel-header>
              <v-expansion-panel-content>
                Todas las referencias de pago en tiendas (oxxo) o bancos (transferencia SPEI) tienen una fecha y hora de vencimiento, si no se hace el pago en este tiempo, el sistema automáticamente cancelará la reservación, los lugares serán liberados y puestos disponibles.
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>¿SE PUEDE CANCELAR LA RESERVACIÓN?</v-expansion-panel-header>
              <v-expansion-panel-content>
                Solo se pueden cancelar las reservaciones que no estén pagadas. Debes hacerlo dentro de los tiempos que establecen los “términos y condiciones” que es por lo menos 12 horas antes del viaje programado, después de este tiempo ya no se podrá cancelar la reservación. Solo entra a tu usuario, menú, mi cuenta, seleccionar la reservación, en la parte superior derecha están 3 puntos que es un submenú-clic y cancelar. Debe aparecer el mensaje de que la cancelación fué exitosa.
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>¿PUEDO CAMBIAR LAS FECHAS DE VIAJE?</v-expansion-panel-header>
              <v-expansion-panel-content>
                Solo si eres USUARIO REGISTRADO y la reservación se hizo desde el perfil de usuario tienen la posibilidad de hacer cambios en las fechas y hora de viaje. No en el origen-destino. Entra a www.connectando.mx, o App CONNECTANDO. Hay que entrar al perfil de usuario, después en tu administrador (íconos en la parte superior derecha), tus connexiones (web o App), identificar la reservación y darle clic en el submenú (tres puntos en la parte superior derecha) cambiar viaje. Debes hacerlo dentro de los tiempos que establecen los “términos y condiciones” que es por lo menos 12 horas antes del viaje programado, después de este tiempo ya no se podrá editar el viaje. Muy importante comentar que las reservaciones hechas como INVITADO no podrán hacer modificaciones en su viaje. De ahí la importancia y la invitación a que generar su registro de usuario y reserven siempre desde su perfil.
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>TOLERANCIA EN SALIDAS</v-expansion-panel-header>
              <v-expansion-panel-content>
                RECOMENDAMOS QUE ESTÉN 10 MINUTOS ANTES DE LA SALIDA MARCADA EN SU RESERVACIÓN. La tolerancia en las salidas es de 5 minutos en los puntos de encuentro en León (Oxxo gas Plaza Mayor y estacionamiento del hotel Hotsson Smart-Centro Max) y de 10 minutos en el punto de encuentro en CDMX (JW Marriott). Importante comentar que en Tepozotlan no hay tolerancia. Es muy importante resaltar la importancia de la puntualidad en la salida, eso beneficia a todos para llegar a tiempo a nuestro destino.
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-header>¿CÓMO SE USA EL CUPÓN DE VIAJE GRATIS?</v-expansion-panel-header>
              <v-expansion-panel-content>
                Es un beneficio exclusivo de los USUARIOS REGISTRADOS. Los cupones de viaje gratis no son cupones de descuento, se aplican para que tengan el beneficio de un viaje gratis derivado de completar 5 reservaciones pagadas. Debes hacer una reservación en viaje sencillo, para una persona, desde el usuario que se hizo acreedor el código de promoción. En los métodos de pago seleccionar la opción que dice " CÓDIGO PROMOCIONAL" escribir los caracteres del código que llegó y aplicarlo. * LOS CÓDIGOS NO SON ACUMULABLES Y SI SE JUNTAN DOS CÓDIGOS EL MÁS ANTIGUO QUEDARÁ SIN VALIDEZ. Revisa Términos y condiciones
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
        </div>

        <div class="container mt-5" style="text-align: center;">
          <div>
            <small class="text-uppercase">Información Legal</small>
            <h3>Información Legal</h3>
          </div>

          <div class="row mt-6 mb-5">
            <div class="col-md-6">
              <div>
                <h5>TÉRMINOS Y CONDICIONES</h5>
                <p>
                  El servicio que brinda
                  <strong>
                    OPERADORA TURÍSTICA MODUM S.A. DE C.V.
                  </strong>&nbsp;(en adelante&nbsp;
                  <strong>
                    CONNECTANDO
                  </strong>)
                  consiste en la organizac...
                </p>

                <a href="https://www.connectando.mx/legals/terminos-y-condiciones" style="text-transform: none; color: green;">
                  Lee el documento &gt;
                </a>
              </div>
            </div>
            <div class="col-md-6">
              <div>
                <h5>AVISO DE PRIVACIDAD</h5>
                <p>
                  En cumplimiento a lo establecido por la Ley Federal de Protección de Datos Personales y el Reglamento de Ley Federal de Protección de...
                </p>

                <a href="https://www.connectando.mx/legals/aviso-de-privacidad" style="text-transform: none; color: green;">
                  Lee el documento &gt;
                </a>
              </div>
            </div>
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
  auth: true
}
</script>

<style scoped>
.card {
    background: var(--light);
    border: none;
    border-radius: 10px;
    color: var(--black);
}
.accordion-button {
    position: relative;
    display: flex;
    align-items: center;
    width: 100%;
    padding: 1rem 1.25rem;
    font-size: 1rem;
    color: #212529;
    text-align: left;
    background-color: #fff;
    border: 0;
    border-radius: 0;
    overflow-anchor: none;
    transition: color .15s ease-in-out, background-color .15s ease-in-out, border-color .15s ease-in-out, box-shadow .15s ease-in-out, border-radius .15s ease;
}
.logo {
    width: 250px;
    mix-blend-mode: multiply;
    margin-right: 30px;
    margin-top: 50px;
}
</style>
