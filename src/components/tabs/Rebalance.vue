<template>
  <div>
    <div class="form__title">
      From
    </div>
    <v-select
      :items="items"
      placeholder="Choose exchange"
      append-icon="expand_more"
      filled
    />
    <div class="form__title">
      To
    </div>
    <v-select
      :items="items"
      placeholder="Choose exchange"
      append-icon="expand_more"
      filled
    />
    <v-select
      :items="items"
      append-icon="expand_more"
      placeholder="Choose currency"
      filled
    />
    <div class="form__dropdown-container">
      <v-text-field
        filled
        outlined
        placeholder="Withdraw amount"
        type="text"
        @focus="showDropdown = true"
        @blur="showDropdown = false"
      />
      <v-card
        class="form__dropdown"
        v-show="showDropdown"
      >
        <div class="form__dropdown-row">
          <v-chip
            color="rgba(42, 101, 145, 0.1)"
            text-color="rgba(42, 101, 145, 1)"
          >
            Balance:&nbsp;
            <strong>0.04763864</strong>
          </v-chip>
        </div>
        <v-chip
          v-for="(chip, id) in chipsPercent"
          :key="`percent-chip-${id}`"
          color="label"
          text-color="white"
          class="mr10"
        >
          <strong>{{ chip }}</strong>
        </v-chip>
      </v-card>
    </div>
    <v-btn
      color="primary"
      height="50"
      block
    >
      Apply
    </v-btn>
  </div>
</template>

<script>
export default {
  name: 'TabRebalance',
  data() {
    return {
      items: ['Kraken','Kraken1'],
      chipsPercent: ['10%', '25%', '50%', '100%', 'Split'],
      showDropdown: false
    }
  }
}
</script>

<style lang="scss" scoped>
.form {
  &__title {
    font-size: 12px;
    line-height: 16px;
    padding-left: 18px;
    margin-bottom: 10px;
  }

  &__dropdown-row {
    margin-bottom: 10px;
  }

  &__dropdown-container {
    position: relative;
  }

  &__dropdown {
    position: absolute;
    left: 0;
    bottom: -50%;
    width: 100%;
    padding: 20px;
    transform: translateY(50%);
    z-index: 1;
  }
}

.mr10 {
  margin-right: 10px;
}
</style>