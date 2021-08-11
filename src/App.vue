<template>
  <div>
    <div class="container mt-5">
      <table class="table">
        <thead class="theadEstiloso">
          <tr>
            <th scope="col">id</th>
            <th scope="col">Nombre</th>
            <th scope="col">Apellido</th>
            <th scope="col">Rut</th>
            <th scope="col">Edad</th>
            <th scope="col">Fecha de Nacimineto</th>
          </tr>
        </thead>
        <tbody class="tbodyEstiloso">
          <!-- Puedes usar in o of despues del v-for o cualquier directiva q uses-->
          <tr v-for="(persona, $index) in personas" :key="$index">
            <td>{{ $index }}</td>
            <td>{{ persona.nombre }}</td>
            <td>{{ persona.apellido }}</td>
            <td>{{ persona.rut }}</td>
            <td>{{ persona.edad }}</td>
            <td>{{ persona.fechaDeNacimiento }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    personas: [
      {
        nombre: 'Angela',
        apellido: 'Vidal',
        rut: '1.234.567-8',
        edad: 20,
        fechaDeNacimiento: '01-01-2000'
      },
      {
        nombre: 'Gonzalo',
        apellido: 'Trujillo',
        rut: '1.234.567-8',
        edad: 20,
        fechaDeNacimiento: '01-01-2000'
      },
      {
        nombre: 'Luca',
        apellido: 'Biotti',
        rut: '1.234.567-8',
        edad: 20,
        fechaDeNacimiento: '01-01-2000'
      }
    ]
  })
}
</script>

<style>
.theadEstiloso {
  background: rgba(80, 200, 167, 0.7);
  box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
  backdrop-filter: blur(9px);
  -webkit-backdrop-filter: blur(9px);
  border-radius: 10px;
  border: 1px solid rgba(255, 255, 255, 0.18);
}

.tbodyEstiloso {
  background: rgba(145, 251, 224, 0.7);
  box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
  backdrop-filter: blur(9px);
  -webkit-backdrop-filter: blur(9px);
  border-radius: 10px;
  border: 1px solid rgba(255, 255, 255, 0.18);
  font-weight: 400;
}
</style>
