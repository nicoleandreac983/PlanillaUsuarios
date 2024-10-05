<script>
export default {
  name: "App",
  data() {
    return {
      usuario: {
        nombre: "",
        nacionalidad: "",
        genero: "",
        direccion: "",
        estadocivil: "",
        continentes: [],
      },
    };
  },
};
</script>

<template>
  <div class="container w-50 mt-5">
    <div class="border p-4 rounded shadow bg-light">
      <form class="w-50 mx-auto p-4">
        <div class="mb-3">
          <label class="form-label">Nombre</label>
          <input class="form-control form-control-sm" v-model="usuario.nombre" />
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
              <input class="form-check-input" type="radio" name="flexRadioDefault" id="m" value="m"
                v-model="usuario.genero" />
              <label class="form-check-label fw-normal" for="m">
                Masculino
              </label>
            </div>
            <div class="form-check">
              <input class="form-check-input" type="radio" name="flexRadioDefault" id="f" value="f"
                v-model="usuario.genero" />
              <label class="form-check-label fw-normal" for="f"> Femenino </label>
            </div>
          </div>
        </div>
        <div class="mb-3">
          <label class="form-label">Dirección</label>
          <input class="form-control" v-model="usuario.direccion" />
        </div>

        <div class="mb-3">
          <label class="form-label">Estado Civil</label>
          <div class="d-flex gap-3">
            <div class="form-check">
              <input class="form-check-input" type="radio" name="flexRadioDefault" id="s" value="s"
                v-model="usuario.estadocivil" />
              <label class="form-check-label fw-normal" for="S">
                Soltero
              </label>
            </div>
            <div class="form-check">
              <input class="form-check-input" type="radio" name="flexRadioDefault" id="c" value="c"
                v-model="usuario.estadocivil" />
              <label class="form-check-label fw-normal" for="C"> Casado </label>
            </div>
          </div>
        </div>

        <div class="mb-3">
          <!-- //texbox de continentes visitdos -->

          <label class="form-label">Continentes Visitados </label>
          <br>
          <div class="form-check form-check-inline">
            <input class="form-check-input" type="checkbox" id="america" value="america"
              v-model="usuario.continentes" />
            <label class="form-check-label" for="america"> América </label>
          </div>
          <div class="form-check form-check-inline">
            <input class="form-check-input" type="checkbox" id="asia" value="asia" v-model="usuario.continentes" />
            <label class="form-check-label" for="asia"> Asia </label>
          </div>
          <div class="form-check form-check-inline">
            <input class="form-check-input" type="checkbox" id="africa" value="africa" v-model="usuario.continentes" />
            <label class="form-check-label" for="africa"> Africa </label>
          </div>
          <div class="form-check form-check-inline">
            <input class="form-check-input" type="checkbox" id="europa" value="europa" v-model="usuario.continentes" />
            <label class="form-check-label" for="europa"> Europa </label>
          </div>
          <div class="form-check form-check-inline">
            <input class="form-check-input" type="checkbox" id="oceania" value="oceania"
              v-model="usuario.continentes" />
            <label class="form-check-label" for="oceania"> Oceania </label>
          </div>
        </div>
      </form>
    </div>
  </div>

  <div class="planilla text-center mt-5 w-75 mx-auto">
    <h1>Planilla de Usuario</h1>
    <hr />
    <table class="table table-striped">
      <thead>
        <tr>
          <th>Nombre</th>
          <th>Nacionalidad</th>
          <th>Género</th>
          <th>Dirección</th>
          <th>Estado Civil</th>
          <th>Continentes visitados</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>{{ usuario.nombre }}</td>
          <td>{{ usuario.nacionalidad }}</td>
          <td>{{ usuario.genero }}</td>
          <td>{{ usuario.direccion }}</td>
          <td>{{ usuario.estadocivil }}</td>
          <td>{{ usuario.continentes.join(', ') }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
