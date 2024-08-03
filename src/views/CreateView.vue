<template>
    <div align="center" class="q-pa-md">
        <div class="q-gutter-md" style="max-width: 300px;">
            <q-form @submit="onSubmit">
                <q-input v-model="fname" label="First Name" />
                <q-input v-model="lname" label="Last Name" />
                <q-input v-model="username" label="Username" />
                <q-input v-model="password" label="Password" />
                <q-input v-model="email" label="Email" />
                <q-input v-model="avatar" label="Avatar" />
                <q-btn class="q-mt-sm" label="Submit" type="submit" color="secondary" />
            </q-form>
        </div>
    </div>
</template>
<script setup>
import { ref } from 'vue';

const fname = ref('')
const lname = ref('')
const username = ref('')
const password = ref('')
const email = ref('')
const avatar = ref('')

const onSubmit = () =>{
    alert('submit')
}
</script>
<style >
    
</style>