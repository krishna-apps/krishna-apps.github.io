<template>
    <div class="ft">
        <form @submit.prevent="onSubmit()">
            <custom-input v-model:value="name" placeholder="Name" :validator="(v) => v.length<3 ? '* Name must be at least 3 characters long' : ''"></custom-input>
            <custom-input v-model:value="phone" placeholder="Phone"></custom-input>
            <custom-input v-model:value="email" placeholder="Email" :validator="validateEmail"></custom-input>
            <p class="form-el">
                <textarea cols="30" rows="10" v-model="message"></textarea>
            </p>
            <p class="form-el">
                <input type="submit" value="Submit" />
            </p>
        </form>
    </div>
</template>

<script>
import CustomInput from './CustomInput'
export default {
    data() {
        return {
            name: '',
            phone: '',
            email: '',
            message: ''
        }
    },
    methods: {
        validateEmail(email) {
            if(/^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/.test(email)) {
                return '';
            } else {
                return '* Please enter a valid email'
            }
        },
        onSubmit() {
            if(this.name && this.email && ~this.validateEmail(this.email) && this.message)
                console.log(`${this.name}\n${this.phone}\n${this.email}\n${this.message}`);
            else {
                window.alert('Please fill the form!')
            }
        }
    },
    components: {
        CustomInput
    }
}
</script>