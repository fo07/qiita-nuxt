<template>
  <ValidationProvider rules="required" v-slot="{ errors }">
    <v-text-field
        v-model="name"
        :error-messages="errors"
        label="お名前"
    />
    <v-text-field
        v-model="email"
        :error-messages="errors"
        label="メールアドレス"
    />
    <v-text-field
        v-model="password"
        :error-messages="errors"
        label="パスワード"
    />
  </ValidationProvider>
</template>

<script>
import { ValidationProvider } from "vee-validate";

export default {
  components: {
    ValidationProvider
  },
  data() {
    return {
      name: "",
      email: "",
      password: ""
    };
  }
};
</script>
