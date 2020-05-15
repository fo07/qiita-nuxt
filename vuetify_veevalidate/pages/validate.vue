<template>
 <validation-observer ref="obs" v-slot="{ invalid }">
    <v-form>
      <validation-provider
        v-slot="{ errors }"
        rules="required|email|max:12"
      >
        <v-text-field
          v-model="email"
          :error-messages="errors"
          label="メールアドレス"
          required
          filled
        />
      </validation-provider>
    </v-form>
    <v-btn type="submit" :disabled="invalid">
        Submit
      </v-btn>
 </validation-observer>
</template>
<script>

export default {
  data() {
      return {
          email: ""
      }
  }
}
</script>
