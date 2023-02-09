<template>
  <div>
    <v-dialog
      :persistent="persistent"
      max-width="440"
      v-model="showBox"
      :width="width"
      class="modal"
    >
      <v-card class="cardBox relative">
        <div @click="showBox = false" class="absolute close">
          <svg
            width="17"
            height="16"
            viewBox="0 0 17 16"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M15.5312 12.9688C16.1406 13.5312 16.1406 14.5156 15.5312 15.0781C15.25 15.3594 14.875 15.5 14.5 15.5C14.0781 15.5 13.7031 15.3594 13.4219 15.0781L8.5 10.1562L3.53125 15.0781C3.25 15.3594 2.875 15.5 2.5 15.5C2.07812 15.5 1.70312 15.3594 1.42188 15.0781C0.8125 14.5156 0.8125 13.5312 1.42188 12.9688L6.34375 8L1.42188 3.07812C0.8125 2.51562 0.8125 1.53125 1.42188 0.96875C1.98438 0.359375 2.96875 0.359375 3.53125 0.96875L8.5 5.89062L13.4219 0.96875C13.9844 0.359375 14.9688 0.359375 15.5312 0.96875C16.1406 1.53125 16.1406 2.51562 15.5312 3.07812L10.6094 8.04688L15.5312 12.9688Z"
              fill="black"
            />
          </svg>
        </div>
        <div class="logo__img">
          <img src="/images/png/logo.png" alt="" />
        </div>
        <div class="row trans__row">
          <!-- header  -->
          <div class="col-12 edit_section_header">
            <header>Transaction Receipt</header>
          </div>

          <!-- content  -->
          <div class="col-6 trans__content">
            <span class="trans__content-title">Num of Subscriptions</span>
          </div>
          <div class="col-6 trans__content">
            <span>600</span>
          </div>

          <div class="col-6 trans__content">
            <span class="trans__content-title">Subscription Type</span>
          </div>
          <div class="col-6 trans__content">
            <span>Study Plan - 400 Practice Plan - 600</span>
          </div>

          <div class="col-6 trans__content">
            <span class="trans__content-title">Amount</span>
          </div>
          <div class="col-6 trans__content">
            <span>6,500,000</span>
          </div>

          <div class="col-6 trans__content">
            <span class="trans__content-title">Transaction Date</span>
          </div>
          <div class="col-6 trans__content">
            <span>2022-04-01 13:23:56</span>
          </div>

          <div class="col-6 trans__content">
            <span class="trans__content-title">Sender</span>
          </div>
          <div class="col-6 trans__content">
            <span>Patrick Elemide</span>
          </div>

          <div class="col-6 trans__content">
            <span class="trans__content-title">Status</span>
          </div>
          <div class="col-6 trans__content">
            <span class="status">Successful</span>
          </div>

          <div class="col-12 trans__content disclaimer">
            <span class="italic"
              >If you have any questions or need more information, please
              contact us on <a href="tel:+23490123456789">090123456789</a> or
              <a href="mailto:admin@successbox.net"
                >admin@successbox.net</a
              ></span
            >
          </div>
        </div>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showBox: false,
      persistent: false,
      width: "100%",
      user: {
        first_name: "",
        last_name: "",
        email: "",
        phone: "",
        role: "Admin",
        password: "",
      },
      cPassword: "",
    };
  },
  methods: {
    showDialogue() {
      this.showBox = true;
    },
  },
};
</script>

<style lang="scss" scoped>
.cardBox {
  background: #fff;
  padding: 22px 30px;
  border-radius: 8px;
  .logo__img {
    text-align: center;
    padding-top: 26px;
    padding-bottom: 15px;
  }
  .trans__row {
    .edit_section_header {
      padding-top: 0;
      header {
        font-weight: var(--font-bold);
        font-size: var(--header-font-size);
        color: var(--secondary-color);
        text-align: center;
      }
    }
    .trans__content {
      padding-top: 0;
      &.disclaimer {
        padding-top: 34px;
      }
      span {
        font-size: var(--normal-font-size);
        color: var(--nav-h3-color);
        font-weight: var(--font-light);
        &.trans__content-title {
          font-weight: var(--font-bold);
        }
        &.status {
          color: var(--success-color-second);
        }
        &.italic {
          font-size: var(--small-font-size);
          font-style: italic;
          line-height: 14px;
          display: inline-block;
          a {
            color: var(--primary-color);
          }
        }
      }
    }
  }
}
.close {
  right: 15px;
  top: 10px;
  cursor: pointer;
  svg {
    &:hover {
      path {
        fill: tomato;
      }
    }
  }
}
</style>