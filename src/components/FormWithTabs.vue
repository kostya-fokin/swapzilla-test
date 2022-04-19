<template>
  <v-container>
    <v-dialog
      v-model="dialog"
      width="780"
    >
      <v-card>
        <v-card-title>
          <v-tabs
            v-model="tab"
          >
            <v-tab
              v-for="tab in tabs"
              :key="`tab-${tab}`"
            >
              {{ tab }}
            </v-tab>
          </v-tabs>
        </v-card-title>

        <div class="form__container">
          <div class="form">
            <v-tabs-items
              v-model="tab"
            >
              <v-tab-item
                v-for="tab in tabs"
                :key="tab"
                transition="fade"
              >
                <component :is="tab "/>
              </v-tab-item>
            </v-tabs-items>
          </div>
        </div>
        <v-icon
          class="form__close-button"
          large
          @click="handleCloseClick"
        >
          close
        </v-icon>
      </v-card>
    </v-dialog>
  </v-container>
</template>

<script>
  import Deposit from '@/components/tabs/Deposit.vue'
  import Withdraw from '@/components/tabs/Withdraw.vue'
  import Rebalance from '@/components/tabs/Rebalance.vue'
  export default {
    name: 'FormWithTabs',

    components: {
      Deposit,
      Withdraw,
      Rebalance,
    },

    data: () => ({
      dialog: true,
      tab: 'Deposit',
      tabs: ['Deposit', 'Withdraw', 'Rebalance'],
    }),
    methods: {
      handleCloseClick() {
        this.dialog = false;
      }
    }
  }
</script>

<style lang="scss">
.form {
  width: 380px;

  &__container {
    display: flex;
    justify-content: center;
    padding-top: 30px;
    padding-bottom: 70px;
  }

  &__close-button {
    position: absolute !important;
    top: 22px;
    right: 22px;
    cursor: pointer;
    font-size: 39px !important;
  }
}
</style>