<template>
  <div>
<b-form @submit="onSubmit" @reset="onReset" v-if="show">
      <b-form-group
        id="input-group-1" label="Name:" label-for="input-1">
        <b-form-input
          id="input-1"
          v-model="form.name"
          type="name"
          placeholder="Enter name"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="Todo task:" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.todo"
          placeholder="Enter todo"
          required
        ></b-form-input>
      </b-form-group>

      <b-button type="submit" variant="primary">Submit</b-button>
      <b-button type="reset" variant="danger">Reset</b-button>
    </b-form>
    <b-card class="mt-3" header="Form Data Result">
      <pre class="m-0">{{ form }}</pre>
    </b-card>
  </div>
    
</template>

<script>
import Header from "@/components/Header"

  export default {
    data() {
      return {
        form: {
          name: '',
          todo: '',
        }, 
      }
    },
    methods: {
      onSubmit(event) {
        event.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(event) {
        event.preventDefault()
        // Reset our form values
        this.form.name = ''
        this.form.todo = ''
      }
    },
  }
  </script>