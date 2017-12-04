<template>
  <div>
    <h1>Funcionários</h1>
    <b-form inline>
      <b-input class="mb-2 mr-sm-2 mb-sm-0" id="inlineFormInputName" placeholder="Name" />
      <b-input class="mb-2 mr-sm-2 mb-sm-0" id="inlineFormInputEmail" placeholder="Email" />
      <b-button variant="primary">Inserir</b-button>
    </b-form>
    <br>
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
            <button type="button" class="btn btn-danger btn-xs">Excluir</button>
          </td>
        </tr>
      </tbody>
    </table>
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
}

a {
  color: #42b983;
}
</style>
