<template>
  <div>
    <!-- Hero -->

    <div class="container py-5">
      <div
        class="row flex-lg-row-reverse align-items-center d-sm-flex justify-content-sm-center g-5 py-5"
      >
        <div class="col-10 col-sm-8 col-lg-6">
          <img
            src="../assets/img/covers/GestionTransporte.png"
            class="d-block mx-lg-auto img-fluid"
            alt="Bootstrap Themes"
            width="700"
            height="500"
            loading="lazy"
          />
        </div>
        <div class="col-lg-6 d-sm-flex justify-content-sm-center">
          <h1 class="display-5 fw-bold lh-1 mb-3">Gestión de Transporte</h1>
        </div>
      </div>
      <hr class="featurette-divider" />
    </div>

    <!-- Titulo -->

    <div class="container">
      <div class="row">
        <div class="col">
          <h1>Software para gestión de transporte</h1>
          <p>
            Aplicación web para el control de peso vehicular en las estaciones
            de pesaje del territorio nacional ajustados a la normatividad
            vigente.
          </p>
        </div>
      </div>
      <hr class="featurette-divider mb-5" />
    </div>

    <div class="container">
      <div class="row">
        <!-- Productos-->

        <div
          v-for="product in products"
          :key="product.id"
          class="col-12 col-sm-12 col-md-12 col-lg-12 col-xl-6 mb-4"
        >
          <div class="card_container">
            <div class="card_image">
              <img :src="API_URL + product.Image.url" alt="{{product.Name}}" />
            </div>
            <div class="card_title">
              {{ product.Name }}
            </div>
            <div class="card_text">
              <p>{{ product.Description }}</p>
            </div>
            <div class="card_footer">
              <div class="card_price">{{ product.Price }}</div>
              <div>
                <button class="btn btn-primary btn-sm">Agregar</button>
              </div>
            </div>
          </div>
        </div>

        <!-- G3 Control de Peso Vehicular (G3 CPV) -->

        <!-- <div class="col-12 col-sm-12 col-md-12 col-lg-6 mb-4">
          <div class="card_container">
            <div class="card_image">
              <img src="../assets/img/transporte/Pesaje.png" alt="Pesaje" />
            </div>
            <div class="card_title">G3 Control de Peso Vehicular (G3 CPV)</div>
            <div class="card_text">
              <p>
                Aplicación web para el control de peso vehicular en las
                estaciones de pesaje del territorio nacional ajustados a la
                normatividad vigente.
              </p>
            </div>
          </div>
        </div> -->

        <!-- G3 Gestión de distribución interurbana (G3 GDI) -->

        <!-- <div class="col-12 col-sm-12 col-md-12 col-lg-6 mb-4">
          <div class="card_container">
            <div class="card_image">
              <img src="../assets/img/transporte/Distribution.png" alt="Distribucion" />
            </div>
            <div class="card_title">
              G3 Gestión de distribución interurbana (G3 GDI)
            </div>
            <div class="card_text">
              <p>
                La distribución interurbana es uno de los grandes retos para las
                empresas de transporte. El principal obstáculo es la integración
                de los diversos actores de la cadena logística en un proceso
                único y articulado que genere flujos de información veraz y
                oportuna. Nuestra solución G3 GDI es ideal si su empresa
                involucra diversos destinos, trayectos largos entre ciudades y
                transferencias entre diferentes transportistas.
              </p>
            </div>
          </div>
        </div> -->

        <!-- G3 Gestión de última milla – distribución urbana (G3 GUM-DU) -->

        <!-- <div class="col-12 col-sm-12 col-md-12 col-lg-6 mb-4">
          <div class="card_container">
            <div class="card_image">
              <img src="../assets/img/transporte/UltimaMilla.png" alt="UltimaMilla" />
            </div>
            <div class="card_title">
              G3 Gestión de última milla – distribución urbana (G3 GUM-DU)
            </div>
            <div class="card_text">
              <p>
                El paso final en la cadena de distribución se ve obstaculizado
                con frecuencia por la complejidad de la logística urbana. El
                proceso requiere la entrega de múltiples paquetes en cortos
                períodos de tiempo para cumplir con los compromisos con sus
                clientes.
              </p>
            </div>
          </div>
        </div> -->

        <!-- G3 Gestión de flota de vehículos (G3 GFV) -->

        <!-- <div class="col-12 col-sm-12 col-md-12 col-lg-6 mb-4">
          <div class="card_container">
            <div class="card_image">
              <img src="../assets/img/transporte/Terminal.png" alt="Terminal" />
            </div>
            <div class="card_title">
              G3 Gestión de flota de vehículos (G3 GFV)
            </div>
            <div class="card_text">
              <p>
                Gestionar su propia flota de vehículos y la distribución de sus
                productos puede ser bastante complejo cuando este no es el
                centro de su negocio. Pensando en ello, G3 GFV ha incorporado
                todas las funcionalidades necesarias para que usted y su equipo
                de trabajo hagan el rastreo y las entregas de la manera más ágil
                y oportuna para sus clientes.
              </p>
            </div>
          </div>
        </div> -->

        <!-- G3 Transportista - Conductor - Repartidor (G3 TCR) -->

        <!-- <div class="col-12 col-sm-12 col-md-12 col-lg-6 mb-4">
          <div class="card_container">
            <div class="card_image">
              <img src="../assets/img/transporte/Delivery.png" alt="Delivery" />
            </div>
            <div class="card_title">
              G3 Transportista - Conductor - Repartidor (G3 TCR)
            </div>
            <div class="card_text">
              <p>
                Si trabaja para una o varias empresas de distribución de
                mercancías, a quienes debe informar sobre contratiempos, demoras
                o entregas realizadas, ahora cuenta con G3 TCR, la opción ideal
                para gestionar sus cargas y recibir oportunamente sus pagos. Una
                aplicación veloz y fácil de usar que le permite informar sobre
                el estado y novedades del viaje y la carga, y registrar de
                manera instantánea las entregas con evidencia fotográfica.
              </p>
            </div>
          </div>
        </div> -->
      </div>
    </div>

    <hr />
  </div>
</template>
<script>
import { ref, onMounted } from 'vue';
import { getProductByCatetory } from '../api/products';
import { API_URL } from '../utils/constants';

export default {
  setup() {
    let products = ref(null);

    onMounted(async () => {
      const response = await getProductByCatetory('2');
      products.value = response;
    });
    return {
      products,
      API_URL,
    };
  },
};
</script>
