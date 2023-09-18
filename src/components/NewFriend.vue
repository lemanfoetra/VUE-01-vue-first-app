<template>
    <form @submit.prevent="submitData">
        <div class="mb-10">
            <label>Name</label>
            <input type="text" v-model="enteredName">
        </div>

        <div class="mb-10">
            <label>Phone</label>
            <input type="text" v-model="enteredPhone">
        </div>

        <div class="mb-10">
            <label>Email</label>
            <input type="text" v-model="enteredEmail">
        </div>
        <div class="mb-10">
            <button>Simpan Friend</button>
        </div>
    </form>
</template>

<script>
export default {
    emits: [
        'add-contact'
    ],
    data() {
        return {
            enteredName: '',
            enteredPhone: '',
            enteredEmail: '',
        }
    },
    methods: {
        submitData() {
            this.$emit('add-contact', this.enteredName, this.enteredPhone, this.enteredEmail)
        }
    }
}
</script>