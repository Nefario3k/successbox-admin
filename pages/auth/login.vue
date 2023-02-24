<template>
  <div>
    <v-row class="login__row">
      <div class="col-12 col-md-6 col-lg-6 col-xl-6 login__row-left">
        <div>
          <v-tabs-items style="background: transparent" v-model="tabs">
            <v-tab-item v-for="n in 3" :key="n">
              <img src="/images/png/login.png" alt="" />
              <p>Read on the go!</p>
              <span>Prepare and read topics in all subjects on the go.</span>
            </v-tab-item>
          </v-tabs-items>

          <div class="tab__controller">
            <svg
              :class="{ active: tabs == 0 }"
              @click="tabs = 0"
              width="10"
              height="10"
              viewBox="0 0 10 10"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <circle cx="5" cy="5" r="5" fill="#383B4C" />
            </svg>
            <svg
              :class="{ active: tabs == 1 }"
              @click="tabs = 1"
              width="10"
              height="10"
              viewBox="0 0 10 10"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <circle cx="5" cy="5" r="5" fill="#383B4C" />
            </svg>
            <svg
              :class="{ active: tabs == 2 }"
              @click="tabs = 2"
              width="10"
              height="10"
              viewBox="0 0 10 10"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <circle cx="5" cy="5" r="5" fill="#383B4C" />
            </svg>
          </div>
        </div>
      </div>
      <div class="col-12 col-md-6 col-lg-6 col-xl-6 login__row-right">
        <form autocomplete="on" class="login__form">
          <img src="/images/png/logo.png" alt="" />
          <div class="relative inputSection">
            <input
              autofocus
              autocomplete="off"
              :class="{ containsElement: login.phone_number }"
              id="loginPhone"
              type="number"
              required
              v-model="login.phone_number"
            />
            <label
              for="loginPhone"
              :class="{ containsElement: login.phone_number }"
              class="placeholder"
              >Phone Number</label
            >
          </div>
          <div class="mt-3 relative inputSection">
            <input
              autocomplete="off"
              required
              :class="{ containsElement: login.password }"
              id="loginPassword"
              type="password"
              v-model="login.password"
            />
            <label
              for="loginPassword"
              :class="{ containsElement: login.password }"
              class="placeholder"
              >Password</label
            >
          </div>
          <v-btn type="submit" color="#383B4C" class="Btn"> LOG IN </v-btn>
        </form>
      </div>
    </v-row>
  </div>
</template>

<script>
export default {
  layout: "empty",
  data() {
    return {
      tabs: 0,
      login: {
        phone_number: "",
        password: "",
      },
    };
  },
};
</script>

<style lang="scss" scoped>
</style>