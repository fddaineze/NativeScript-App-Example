<template>
  <Page actionBarHidden="true">
    <ActionBar title="Login" class="action-bar" />
    <FlexboxLayout flexDirection="column" justifyContent="center" class="full-height">
      <Image src="~/assets/images/nsvue_logo.png" class="logo-container" />

      <StackLayout class="container">
        <FlexboxLayout alignItems="center" class="border-bottom">
          <Image src="~/assets/images/icon_user.png" width="16" height="16" class="icon-margin" />
          <TextField v-model="usernameInput" hint="Username" class="form-input" />
        </FlexboxLayout>

        <FlexboxLayout alignItems="center" class="border-bottom">
          <Image src="~/assets/images/icon_lock.png" width="16" height="16" class="icon-margin" />
          <TextField v-model="passwordInput" hint="Password" secure="true" class="form-input" />
        </FlexboxLayout>

        <Button text="Login" @tap="onButtonTap" class="my-button" />

        <FlexboxLayout alignItems="center" justifyContent="space-between" class="auth-buttons">
          <Label horizontalAlignment="left" text="Create Account" />
          <Label horizontalAlignment="right" text="Forgot Password" />
        </FlexboxLayout>
      </StackLayout>
    </FlexboxLayout>
  </Page>
</template>

<script >
export default {
  data() {
    return {
      usernameInput: "",
      passwordInput: ""
    };
  },
  methods: {
    onButtonTap() {
      console.log("--onButtonTap--");
      console.log("user: ", this.usernameInput);
      console.log("pass: ", this.passwordInput);
    }
  }
};
</script>

<style lang="scss">
.action-bar {
  display: none;
}
.border-bottom {
  border-bottom-width: 1;
  border-bottom-color: white;
  margin-bottom: 40;
  padding-bottom: 8;
}
.form-input {
  color: white;
  placeholder-color: white;
}
.icon-margin {
  margin-right: 10;
}
.my-button {
  background-color: #4bd5dc;
  color: white;
  font-weight: bold;
  border-radius: 25;
  padding-top: 14;
  padding-bottom: 14;
  text-transform: uppercase;
  letter-spacing: 0.1;
  margin-bottom: 20;
  margin-top: 10;
}
.auth-buttons {
  color: white;
  font-size: 14;
}
.full-height {
  height: 100%;
  background-color: #39b994;
  background-image: linear-gradient(#337fc7, #39b994);
  background: #337fc7;
  background: linear-gradient(#337fc7, #39b994);
}
.logo-container {
  width: 150;
  margin-bottom: 60;
}
.container {
  margin-left: 34;
  margin-right: 34;
}
</style>