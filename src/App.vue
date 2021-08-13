<template>
  <div class="container mt-5">
    <h2 class="my-3 row justify-content-center">Tabla de Usuarios</h2>
    <table class="table table-bordered table-hover">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">Nombre</th>
          <th scope="col">Apellido</th>
          <th scope="col">RUN</th>
          <th scope="col">Fecha de Nacimiento</th>
          <th scope="col">Edad</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(persona, $index) in personas" :key="$index">
          <td>{{ $index + 1 }}</td>
          <td>{{ persona.nombre }}</td>
          <td>{{ persona.apellido }}</td>
          <td>{{ persona.run }}</td>
          <td>{{ persona.fechaDeNacimiento }}</td>
          <td>{{ persona.edad }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    personas: [
      {
        nombre: 'Jaime',
        apellido: 'Lizama',
        run: '1.234.567-8',
        fechaDeNacimiento: '01-01-2020',
        edad: 20
      },
      {
        nombre: 'Coté',
        apellido: 'Pop',
        run: '1.234.567-8',
        fechaDeNacimiento: '01-01-2020',
        edad: 20
      }
    ]
  })
}
</script>

<style scoped></style>
