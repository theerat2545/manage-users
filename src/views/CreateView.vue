<template>
    <div class="q-pa-md">
        <div class="q-gutter-md" style="max-width: 300px;">
            <q-form @submit="onSubmit">
                <q-input label="First Name" />
                <q-input label="Last Name" />
                <q-input label="Username" />
                <q-input label="Password" />
                <q-input label="Email" />
                <q-input label="Avatar" />
                <q-btn class="q-mt-sm" label="Submit" type="submit" color="secondary" />
            </q-form>
        </div>
    </div>
</template>
<script setup>
const onSubmit = () =>{

}
</script>
<style >
    
</style>