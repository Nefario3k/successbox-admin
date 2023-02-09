<template>
  <div>
    <v-dialog
      :persistent="persistent"
      max-width="853"
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
        <form autocomplete="off" class="row row_form">
          <!-- header  -->
          <div class="col-12 edit_section_header">
            <header>Add New School</header>
          </div>

          <!-- input area  -->
          <div class="col-12 label__area"><header>School Details</header></div>

          <!-- password  -->
          <div class="col-6 inputArea">
            <input
              autocomplete="false"
              required
              type="text"
              placeholder="Name of School*"
              id="description"
            />
          </div>

          <!-- class  -->
          <div class="col-6 inputArea">
            <select id="class_select" class="form_input">
              <option class="first_option">
                <span>Number of Request*</span>
              </option>

              <option v-for="item in 6" :value="item" :key="item">
                Item {{ item }}
              </option>
            </select>
          </div>

          <!-- text area  -->
          <div class="col-6 inputArea">
            <textarea
              autocomplete="false"
              required
              placeholder="Address of School*"
              id="address"
            ></textarea>
          </div>

          <!-- drag  -->
          <div class="col-6 inputArea">
            <div class="drag__content">
              <div>
                <svg
                  width="20"
                  height="14"
                  viewBox="0 0 20 14"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M16.7812 6.09375C16.9062 5.75 17 5.40625 17 5C17 3.34375 15.6562 2 14 2C13.375 2 12.7812 2.1875 12.3125 2.53125C11.4688 1.03125 9.84375 0 8 0C5.21875 0 3 2.25 3 5C3 5.09375 3 5.1875 3 5.28125C1.25 5.875 0 7.5625 0 9.5C0 12 2 14 4.5 14H16C18.1875 14 20 12.2188 20 10C20 8.09375 18.625 6.46875 16.7812 6.09375ZM6.71875 6.96875L9.46875 4.21875C9.53125 4.15625 9.71875 4 10 4C10.25 4 10.4375 4.15625 10.5 4.25L13.25 7C13.5625 7.28125 13.5625 7.75 13.25 8.03125C12.9688 8.34375 12.5 8.34375 12.2188 8.03125L10.75 6.5625V11.25C10.75 11.6875 10.4062 12 10 12C9.5625 12 9.25 11.6875 9.25 11.25V6.5625L7.75 8.03125C7.4375 8.3125 6.96875 8.3125 6.6875 8.03125C6.375 7.71875 6.40625 7.28125 6.71875 6.96875Z"
                    fill="#383B4C"
                  />
                </svg>
                <p>Upload Image</p>
                <span
                  >Drag and drop a file or
                  <span class="browse">browse</span></span
                >
              </div>
            </div>
          </div>

          <div class="col-12 label__area"><header>Contact Details</header></div>

          <div class="col-6 inputArea">
            <input
              autocomplete="false"
              required
              type="text"
              placeholder="Name of Primary Contact Person*"
              id="ctone"
            />
          </div>

          <div class="col-6 inputArea">
            <input
              autocomplete="false"
              required
              type="text"
              placeholder="Name of Secondary Contact Person*"
              id="cttwo"
            />
          </div>

          <div class="col-6 inputArea">
            <input
              autocomplete="false"
              required
              type="text"
              placeholder="Phone Number*"
              id="phoneone"
            />
          </div>

          <div class="col-6 inputArea">
            <input
              autocomplete="false"
              required
              type="text"
              placeholder="Phone Number*"
              id="phonetwo"
            />
          </div>

          <div class="col-6 inputArea">
            <input
              autocomplete="false"
              required
              type="email"
              placeholder="Email"
              id="mail1"
            />
          </div>

          <div class="col-6 inputArea">
            <input
              autocomplete="false"
              required
              type="email"
              placeholder="Email"
              id="mail2"
            />
          </div>

          <!-- drag  -->
          <div class="col-6 inputArea">
            <div class="drag__content">
              <div>
                <svg
                  width="20"
                  height="14"
                  viewBox="0 0 20 14"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M16.7812 6.09375C16.9062 5.75 17 5.40625 17 5C17 3.34375 15.6562 2 14 2C13.375 2 12.7812 2.1875 12.3125 2.53125C11.4688 1.03125 9.84375 0 8 0C5.21875 0 3 2.25 3 5C3 5.09375 3 5.1875 3 5.28125C1.25 5.875 0 7.5625 0 9.5C0 12 2 14 4.5 14H16C18.1875 14 20 12.2188 20 10C20 8.09375 18.625 6.46875 16.7812 6.09375ZM6.71875 6.96875L9.46875 4.21875C9.53125 4.15625 9.71875 4 10 4C10.25 4 10.4375 4.15625 10.5 4.25L13.25 7C13.5625 7.28125 13.5625 7.75 13.25 8.03125C12.9688 8.34375 12.5 8.34375 12.2188 8.03125L10.75 6.5625V11.25C10.75 11.6875 10.4062 12 10 12C9.5625 12 9.25 11.6875 9.25 11.25V6.5625L7.75 8.03125C7.4375 8.3125 6.96875 8.3125 6.6875 8.03125C6.375 7.71875 6.40625 7.28125 6.71875 6.96875Z"
                    fill="#383B4C"
                  />
                </svg>
                <p>Upload Image</p>
                <span
                  >Drag and drop a file or
                  <span class="browse">browse</span></span
                >
              </div>
            </div>
          </div>

          <!-- drag  -->
          <div class="col-6 inputArea">
            <div class="drag__content">
              <div>
                <svg
                  width="20"
                  height="14"
                  viewBox="0 0 20 14"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M16.7812 6.09375C16.9062 5.75 17 5.40625 17 5C17 3.34375 15.6562 2 14 2C13.375 2 12.7812 2.1875 12.3125 2.53125C11.4688 1.03125 9.84375 0 8 0C5.21875 0 3 2.25 3 5C3 5.09375 3 5.1875 3 5.28125C1.25 5.875 0 7.5625 0 9.5C0 12 2 14 4.5 14H16C18.1875 14 20 12.2188 20 10C20 8.09375 18.625 6.46875 16.7812 6.09375ZM6.71875 6.96875L9.46875 4.21875C9.53125 4.15625 9.71875 4 10 4C10.25 4 10.4375 4.15625 10.5 4.25L13.25 7C13.5625 7.28125 13.5625 7.75 13.25 8.03125C12.9688 8.34375 12.5 8.34375 12.2188 8.03125L10.75 6.5625V11.25C10.75 11.6875 10.4062 12 10 12C9.5625 12 9.25 11.6875 9.25 11.25V6.5625L7.75 8.03125C7.4375 8.3125 6.96875 8.3125 6.6875 8.03125C6.375 7.71875 6.40625 7.28125 6.71875 6.96875Z"
                    fill="#383B4C"
                  />
                </svg>
                <p>Upload Image</p>
                <span
                  >Drag and drop a file or
                  <span class="browse">browse</span></span
                >
              </div>
            </div>
          </div>

          <!-- cumpolsory  -->
          <div class="col-12 inputArea d-flex align-center">
            <v-checkbox
              label="Send Invoice to email"
              color="var(--primary-color)"
              value="red"
              hide-details
            ></v-checkbox>
          </div>

          <div class="col-12 inputArea listing_action">
            <v-btn class="Btn upload"
              ><svg
                width="15"
                height="15"
                viewBox="0 0 15 15"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M7.5 0.96875C3.75391 0.96875 0.71875 4.00391 0.71875 7.75C0.71875 11.4961 3.75391 14.5312 7.5 14.5312C11.2461 14.5312 14.2812 11.4961 14.2812 7.75C14.2812 4.00391 11.2461 0.96875 7.5 0.96875ZM11.4375 8.51562C11.4375 8.70703 11.2734 8.84375 11.1094 8.84375H8.59375V11.3594C8.59375 11.5508 8.42969 11.6875 8.26562 11.6875H6.73438C6.54297 11.6875 6.40625 11.5508 6.40625 11.3594V8.84375H3.89062C3.69922 8.84375 3.5625 8.70703 3.5625 8.51562V6.98438C3.5625 6.82031 3.69922 6.65625 3.89062 6.65625H6.40625V4.14062C6.40625 3.97656 6.54297 3.8125 6.73438 3.8125H8.26562C8.42969 3.8125 8.59375 3.97656 8.59375 4.14062V6.65625H11.1094C11.2734 6.65625 11.4375 6.82031 11.4375 6.98438V8.51562Z"
                  fill="#EFF1F9"
                />
              </svg>
              <span>ADD School</span></v-btn
            >
          </div>
        </form>
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
  .row_form {
    .edit_section_header {
      margin-bottom: 11px;
      header {
        font-weight: var(--font-bold);
        font-size: var(--header-font-size);
        color: var(--secondary-color);
        text-align: center;
      }
      &.underSide {
        padding-top: 20px;
      }
    }
    .inputArea {
      padding-top: 0;
      &.listing_action {
        text-align: right;
        .Btn {
          min-height: 4.2rem;
          max-width: 18rem;
          width: 100%;
          border-radius: 10px;
          font-weight: var(--font-medium);
          font-size: var(--normal-font-size);
          border: 1px solid #b3acb6;
          color: var(--border02-color);
          background: transparent;
          box-shadow: none !important;
          svg {
            margin-right: 10px;
          }
          &.upload {
            background: #b3acb6 !important;
            color: #fff;
          }
        }
      }
      .ebook {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 8px;
        padding-top: 8px;
        .ebook__input {
          //   width: 100%;
          height: 20.2rem;
          background-color: var(--body-color);
          display: flex;
          align-items: center;
          justify-content: center;
          padding: 12px;
          text-align: center;
          border-radius: 10px;
          cursor: pointer;
          p {
            font-weight: var(--font-light);
            color: var(--nav-h3-color);
            font-size: var(--normal-font-size);
            margin-bottom: 8px;
          }
          span {
            font-weight: var(--font-light);
            color: #b3acb6;
            font-size: var(--normal-font-size);
            line-height: 16px;
            display: inline-block;
          }
        }
      }
      label {
        font-weight: 500;
        font-size: 1.4rem;
        color: var(--secondary-color);
        margin-bottom: 4px;
        display: inline-flex;
        align-items: center;
        gap: 8px;
        svg {
          cursor: pointer;
        }
      }
      input {
        border: 1px solid var(--nav-h3-color) !important;
        border-radius: 10px;
        height: 4.4rem;
        text-transform: initial;
        color: #b3acb6;
        &::placeholder {
          font-size: var(--small-font-size);
          color: #b3acb6;
          font-weight: 400;
        }
        &.active {
          border-color: var(--primary-color);
        }
        &:focus {
          border-color: var(--primary-color);
        }
        &.content {
          border-color: var(--primary-color);
        }
      }
      select {
        color: #b3acb6;
        font-size: var(--small-font-size);
        font-weight: var(font-medium);
        letter-spacing: -0.011em;
        text-align: left;
        -moz-appearance: none; /* Firefox */
        -webkit-appearance: none; /* Safari and Chrome */
        appearance: none;
        background-image: url("/images/svg/arrow_down.svg") !important;
        background-position: bottom 17px right 15px !important;
        background-repeat: no-repeat !important;
        height: 4.4rem !important;
        border-radius: 10px !important;
        width: 100%;
        padding: 10px;
        outline: none;
        border: 1px solid var(--nav-h3-color);
        cursor: pointer;
        option {
          color: var(--nav-h3-color);
          font-weight: var(--font-medium);
          font-size: var(--normal-font-size);
          &[selected] {
            background: var(--primary-color);
            color: #fff;
          }
          &:hover {
            background: var(--primary-color) !important;
            color: #fff !important;
          }
        }
      }
      textarea {
        height: 100%;
        border: 1px solid var(--nav-h3-color) !important;
        border-radius: 10px;
        resize: none;
        &::placeholder {
          font-size: var(--small-font-size);
          color: #b3acb6;
          font-weight: 400;
        }
      }
      .drag__content {
        height: 13.6rem;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 10px;
        border: 1px dashed var(--nav-h3-color);
        text-align: center;
        // transform: matrix(1, 0, 0, -1, 0, 0);
        p {
          margin-top: 10px;
          margin-bottom: 10px;
          color: #b3acb6;
          font-weight: var(--font-light);
          font-size: var(--normal-font-size);
        }
        span {
          font-weight: var(--font-light);
          font-size: var(--normal-font-size);
          color: var(--nav-h3-color);
          .browse {
            color: var(--primary-color);
            cursor: pointer;
          }
        }
      }
      &.fileInputArea {
        & svg {
          cursor: pointer;
          &:hover {
            rect {
              stroke: var(--primary-color);
            }
            path {
              fill: var(--primary-color);
            }
          }
        }
      }
    }
    .label__area {
      header {
        font-weight: var(--font-light);
        font-size: 1.8rem;
        color: var(--secondary-color);
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

@media (max-width: 611px) {
  .listing_action {
    display: flex;
    align-items: center;
    flex-direction: column-reverse;
    gap: 23px;
    .Btn {
      max-width: 100% !important;
      &.upload {
        margin: 0 !important;
      }
    }
  }
}
</style>