<template>
  <div id="list" class="row">
      <div class="table-responsive col-md-12">
          <table class="table table-striped table-condensed" cellspacing="0" cellpadding="0">
              <thead>
                <tr>
                    <th>Nome</th>
                    <th>Email</th>
                    <th class="actions">Ações</th>
                </tr>
              </thead>
              <tbody>
                  <tr v-for="employee in employees" :key="employee.name">
                    <td>{{ employee.name }}</td>
                    <td>{{ employee.email }}</td>
                    <td>
                        <button type="button" class="btn btn-warning btn-xs">Editar</button>
                        <b-button variant="success" type="button" class="btn btn-danger btn-xs">Excluir</b-button>
                    </td>
                  </tr>
              </tbody>
          </table>
      </div>
  </div>
</template>

<script>
import employees from '../../static/employees.json'
export default {
  name: 'HelloWorld',
  data () {
    return {
      employees: employees
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
