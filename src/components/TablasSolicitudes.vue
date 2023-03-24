<template>
    <div>
      <v-container fluid>
        <v-row>
          <v-col class="col-md-4">
            <v-card>
              <v-card-title>Centro de Computo</v-card-title>
              <v-card-text>
                <table>
                  <tbody>
                    <tr>
                      <td>Enviadas</td>
                      <td>{{ computo.solicitudEnviada }}</td>
                    </tr>
                    <tr>
                      <td>En proceso</td>
                      <td>{{ computo.enProceso }}</td>
                    </tr>
                    <tr>
                      <td>Terminadas</td>
                      <td>{{ computo.terminadas }}</td>
                    </tr>
                    <tr>
                      <td>Liberadas</td>
                      <td>{{ computo.liberadas }}</td>
                    </tr>
                  </tbody>
                </table>
              </v-card-text>
            </v-card>
          </v-col>
          <v-col class="col-md-4">
            <v-card>
              <v-card-title>Mantenimiento</v-card-title>
              <v-card-text>
                <table>
                  <tbody>
                    <tr>
                      <td>Enviada</td>
                      <td>{{ mantenimiento.solicitudEnviada }}</td>
                    </tr>
                    <tr>
                      <td>En proceso</td>
                      <td>{{ mantenimiento.enProceso }}</td>
                    </tr>
                    <tr>
                      <td>Terminadas</td>
                      <td>{{ mantenimiento.terminadas }}</td>
                    </tr>
                    <tr>
                      <td>Liberadas</td>
                      <td>{{ mantenimiento.liberadas }}</td>
                    </tr>
                  </tbody>
                </table>
              </v-card-text>
            </v-card>
          </v-col>
          <v-col class="col-md-4">
            <v-card>
              <v-card-title>Recursos Materiales</v-card-title>
              <v-card-text>
                <table>
                  <tbody>
                    <tr>
                      <td>Enviada</td>
                      <td>{{ recursosMateriales.solicitudEnviada }}</td>
                    </tr>
                    <tr>
                      <td>En proceso</td>
                      <td>{{ recursosMateriales.enProceso }}</td>
                    </tr>
                    <tr>
                      <td>Terminadas</td>
                      <td>{{ recursosMateriales.terminadas }}</td>
                    </tr>
                    <tr>
                      <td>Liberadas</td>
                      <td>{{ recursosMateriales.liberadas }}</td>
                    </tr>
                  </tbody>
                </table>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </div>
</template>
  
  
<script>
  export default {
    data() {
      return {
        computo: {
          solicitudEnviada: 0,
          enProceso: 0,
          terminadas: 0,
          liberadas: 0,
        },
        mantenimiento: {
          solicitudEnviada: 0,
          enProceso: 0,
          terminadas: 0,
          liberadas: 0,
        },
        recursosMateriales: {
          solicitudEnviada: 0,
          enProceso: 0,
          terminadas: 0,
          liberadas: 0,
        },
      };
    },
    methods: {
      // Aquí puedes agregar los métodos necesarios para actualizar los contadores
      // cuando se agreguen o completen solicitudes en cada tabla
    },
  };
</script>
  