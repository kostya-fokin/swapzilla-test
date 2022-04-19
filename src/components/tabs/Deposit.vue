<template>
  <div>
    <v-select
      :items="items"
      value="Kraken"
      append-icon="expand_more"
      rounded
      filled
    />
    <v-select
      :items="items"
      append-icon="expand_more"
      placeholder="Choose currency"
      filled
      rounded
    />
    <div class="form__qr-container">
      <img
        class="form__qr-pic"
        :src="require('@/assets/qr.png')"
        width="119"
      />
      FGBfvcnkfdnvkk74365832ybvcvdfvfvb
    </div>
    <v-btn
      color="primary"
      height="50"
      block
    >
      Copy
    </v-btn>
  </div>
</template>

<script>
export default {
  name: 'TabDeposit',
  data() {
    return {
      items: ['Kraken','Kraken1']
    }
  }
}
</script>

<style lang="scss" scoped>
.form {
  &__qr-container {
    display: flex;
    margin-top: 16px;
    margin-bottom: 29px;
    flex-direction: column;
    align-items: center;
  }

  &__qr-pic {
    margin-bottom: 27px;
  }
}
</style>