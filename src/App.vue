<template>
  <div id="app">
    <form>
      <div class="mb-3"> 
        <label class="form-label">Nombre</label> 
        <input class="form-control" v-model="usuario.nombre" /> 
      </div> 
      <div class="mb-3"> 
        <label class="form-label">Nacionalidad</label> 
        <select class="form-select" v-model="usuario.nacionalidad"> 
          <option value="chile">Chile</option> 
          <option value="extranjero">Extranjero</option> 
        </select> 
      </div> 
      <div class="mb-3"> 
        <label class="form-label">Genero</label> 
        <div class="d-flex gap-3"> 
          <div class="form-check"> 
            <input class="form-check-input" type="radio"name="flexRadioDefault" id="m" value="m" v-model="usuario.genero" /> 
            <label class="form-check-label fw-normal" for="m"> Masculino </label> 
          </div> 
          <div class="form-check"> 
            <input class="form-check-input" type="radio" name="flexRadioDefault" id="f" value="f" v-model="usuario.genero" /> 
            <label class="form-check-label fw-normal" for="f"> Femenino </label> 
          </div> 
        </div> 
      </div>
      <div class="mb-3">
        <label  class="form-label">Dirección</label>
        <input class="form-control" v-model="usuario.direccion">
      </div>
      <div class="mb-3">
        <label class="form-label">Estado civil</label>
        <div class="form-check">
          <input class="form-check-input" type="radio" name="flexRadioDefault" id="s" value="s" v-model="usuario.estado">
          <label class="form-check-label fw-normal" for="s">Soltero</label>
        </div>
        <div class="form-check">
          <input class="form-check-input" type="radio" name="flexRadioDefault" id="c" value="c" v-model="usuario.estado">
          <label class="form-check-label fw-normal" for="c">Casado</label>
        </div>
      </div>
      <div class="mb-3">
        <label class="form-label">Continentes que ha visitado</label>
        <div class="form-check">
          <input v-model="continentes" name="continentes" type="checkbox" v-model="usuario.continente" value="america">
          <label class="form-check-label fw-normal">america</label>
        </div>
        <div class="form-check">
          <input v-model="continentes" name="continentes" type="checkbox" v-model="usuario.continente" value="europa">
          <label class="form-check-label fw-normal">europa</label>
        </div>
        <div class="form-check">
          <input v-model="continentes" name="continentes" type="checkbox" v-model="usuario.continente" value="asia">
          <label class="form-check-label fw-normal">asia</label>
        </div>
        <div class="form-check">
          <input v-model="continentes" name="continentes" type="checkbox" v-model="usuario.continente" value="africa">
          <label class="form-check-label fw-normal">africa</label>
        </div>
        <div class="form-check">
          <input v-model="continentes" name="continentes" type="checkbox" v-model="usuario.continente" value="oceania">
          <label class="form-check-label fw-normal">oceania</label>
        </div>
      </div>
    </form>
    <div class="planilla text-center mt-5 w-75 mx-auto"> 
      <h1>Planilla de Usuario</h1> 
      <hr /> 
      <table class="table table-striped"> 
        <thead> 
          <tr> 
            <th>Nombre</th> 
            <th>Nacionalidad</th> 
            <th>Género</th>
          </tr>
        </thead> 
        <tbody> 
          <tr> 
            <td>{{ usuario.nombre }}</td> 
            <td>{{ usuario.nacionalidad }}</td> 
            <td>{{ usuario.genero }}</td>
          </tr>  
        </tbody> 
      </table>
      <table class="table table-striped">
        <thead>
          <tr>
            <th>Dirección</th>
            <th>Estado civil</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>{{ usuario.direccion }}</td>
            <td>{{ usuario.estado }}</td>
          </tr>
        </tbody>
      </table>
      <table class="table table-striped">
        <thead>
          <tr>
            <th>Continentes visitados</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>{{ usuario.continente }}</td>
          </tr>
        </tbody>
      </table> 
    </div>
  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      usuario: {
        nombre: "",
        nacionalidad: "",
        genero: "",
        direccion:"",
        estado:"",
        continente:"",
      },
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
