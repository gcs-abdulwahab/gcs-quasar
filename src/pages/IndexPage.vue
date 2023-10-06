<template>
  <q-page class="flex flex-center column">

    <q-input v-model="name" label="Name" />
    <!-- create button with the label Notify me with icon message -->

    <q-btn class="q-mt-md" color="primary" size="xl" label="Notify me" icon="send" @click="notifyMe" />


  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage',
  // write the handle of notify me

  methods: {

    notifyMe() {
      this.$q.notify({
        message: `Hello ${this.name}`,
        color: 'positive',
        icon: 'announcement',
        position: 'top',
        timeout: 2000
      })

    }


  },



  data() {
    return {
      name: ''
    }
  }

})
</script>
