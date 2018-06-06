<template>
  <q-layout view="lHh Lpr lFf">
    <q-layout-header>
      <q-toolbar color="primary">

        <q-toolbar-title>
          Out of Time Color Picker
          <div slot="subtitle">Running on Quasar v{{ $q.version }}</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-layout-header>

    <q-page-container class="bg">

      <q-color-picker v-model="modelHex" class="absolute-center"/>
    </q-page-container>
  </q-layout>

</template>

<script>
import { colors } from 'quasar'
export default {
  data: () => ({
    modelHex: '#C7044B'
  }),
  watch: {
    modelHex: function (val, oldVal) {
      colors.setBrand('primary', val)
    }
  }
}
</script>
