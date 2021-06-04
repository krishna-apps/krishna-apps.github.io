<template>
  <p class="form-el">
    <input
      :id="placeholder"
      type="text"
      v-model="val"
      @input="oninput()"
      @change="onchange()"
    />
    <label :htmlFor="placeholder" :class="{ active: val }">{{
      placeholder
    }}</label>
    <span className="form-validation">{{ error }}</span>
  </p>
</template>
<script>
export default {
    props: ['value', 'placeholder', 'validator'],
    data() {
        return {
            val: this.value,
            error: ''
        }
    },
    methods: {
        oninput() {
            this.$emit('update:value', this.val)
        },
        onchange() {
            if (this.validator)
                this.error = this.validator(this.val);
        }
    }
}
</script>