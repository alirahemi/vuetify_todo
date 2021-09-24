<template>
  <v-snackbar
      v-model="$store.state.snackbar.show"
    >
      <div class="ml-4">{{ $store.state.snackbar.text }}</div>

      <template v-slot:action="{ attrs }">
        <v-btn
          @click="$store.commit('hideSnackbar')"
          text
          v-bind="attrs"
          class="mr-4"
        >
          Close
        </v-btn>
      </template>
    </v-snackbar>
</template>

<script>
export default {

}
</script>

<style lang="sass">
  div.v-snack:not(.v-snack--absolute)
    height: 100%
</style>