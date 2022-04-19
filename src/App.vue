<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <FormWithTabs/>
    </v-main>
  </v-app>
</template>

<script>
import FormWithTabs from './components/FormWithTabs';

export default {
  name: 'App',

  components: {
    FormWithTabs,
  },

  data: () => ({
    //
  }),
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;700&display=swap');
$body-font-family: 'Open Sans';

* {
  text-transform: none !important;
}

.v-application {
  font-family: $body-font-family, sans-serif !important;
  font-weight: 400 !important;
}

.v-tab {
  font-weight: 400;
  font-size: 20px;
  letter-spacing: 0;
}

.v-select {
  .v-input__slot:before {
    border: 0 !important;
  }
}

.v-btn {
  font-weight: 700;
  font-size: 14px;
  letter-spacing: 0;
}

.v-chip {
  border-radius: 3px !important;
  font-size: 12px !important;
  cursor: pointer;
}

.v-select {
  border-radius: 5px !important;
}

.v-text-field {
  border-radius: 5px !important;
}

.v-card__title {
  padding: 30px 30px 10px !important;
}

.v-tab {
  padding: 0;
  margin-right: 40px;
  min-width: 0;
  padding-bottom: 20px;
}

.v-tabs-slider-wrapper {
  height: 4px !important;
}

.v-input {
  font-size: 14px;
}

.v-text-field--rounded > .v-input__control > .v-input__slot {
  padding: 0 18px;
}

.v-text-field--filled > .v-input__control > .v-input__slot, .v-text-field--full-width > .v-input__control > .v-input__slot, .v-text-field--outlined > .v-input__control > .v-input__slot {
    min-height: 50px;
}

.v-input__slot {
  margin-bottom: 0;
}

.v-text-field--full-width .v-input__prepend-outer, .v-text-field--full-width .v-input__prepend-inner, .v-text-field--full-width .v-input__append-inner, .v-text-field--full-width .v-input__append-outer, .v-text-field--enclosed .v-input__prepend-outer, .v-text-field--enclosed .v-input__prepend-inner, .v-text-field--enclosed .v-input__append-inner, .v-text-field--enclosed .v-input__append-outer {
  margin-top: 14px;
}

.v-application--is-ltr .v-text-field .v-input__append-inner {
  margin-top: 13px;
}

.v-text-field--outlined fieldset {
  border-width: 0;
}

.v-window {
  overflow: visible;
}
</style>