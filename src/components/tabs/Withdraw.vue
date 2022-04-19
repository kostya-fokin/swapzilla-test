<template>
  <div>
    <v-select
      :items="items"
      placeholder="Choose exchange"
      append-icon="expand_more"
      filled
      rounded
    />
    <v-select
      :items="items"
      append-icon="expand_more"
      placeholder="Choose currency"
      filled
      rounded
    />
    <v-text-field
      class="input-with-append"
      filled
      rounded
      placeholder="Withdraw amount"
      type="text"
    >
      <template v-slot:append>
        <v-chip
          color="label"
          text-color="white"
        >
          <strong>Max</strong>
        </v-chip>
      </template>
    </v-text-field>
    <v-btn
      color="primary"
      height="50"
      block
    >
      Withdraw
    </v-btn>
  </div>
</template>

<script>
export default {
  name: 'TabWithdraw',
  data() {
    return {
      items: ['Kraken','Kraken1']
    }
  }
}
</script>

<style lang="scss">
.input-with-append .v-input__append-inner {
    margin-top: 9px !important;
}
</style>