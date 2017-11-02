<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <form name="myForm">
      <div class="panel panel-default">
        <div class="panel-heading">
          <div class="panel-title">
            Mi formulario
          </div>
        </div>
        <div class="panel-body">
          <div class="row">
            <div class="col-md-6">
              <div class="form-group">
                <label for="names">Nombres:</label>
                <input type="text" class="form-control" v-model="form.names" name="names">
              </div>
            </div>
            <div class="col-md-6">
              <div class="form-group">
                <label for="names">Nombres:</label>
                <input type="text" class="form-control" v-model="form.lastnames" name="lastnames">
              </div>
            </div>

            <div class="col-md-6">
              <label for="gender">Sexo:</label><br>
              <label class="radio-inline">
                <input type="radio" name="inlineRadioOptions" id="inlineRadio1" value="Hombre" v-model="form.gender"> Hombre
              </label>
              <label class="radio-inline">
                <input type="radio" name="inlineRadioOptions" id="inlineRadio2" value="Mujer" v-model="form.gender"> Mujer
              </label>
            </div>

            <div class="clearfix"></div> <br>
            <div class="col-md-12">
              <pre>{{ $data.form }}</pre>
            </div>

            <div class="col-md-12">
              <button type="button" class="btn btn-success pull-right" v-on:click="signUp()">Registrarse</button>
            </div>
          </div>
        </div>

        <div class="panel-footer">
          
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Ejercicio nro. 3 - Uso de eventos',
      form: {}
    }
  },
  mounted () {
    console.log('Carga del proyecto')
  },
  methods: {
    signUp: function () {
      console.log('Procesando datos')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
