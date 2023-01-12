<script>

    export default {
        name: 'UserData',
        emits: ['add-user'],
        data(){
            return {

                    name: '',
                    age: ''

            }
        },
        methods: {
            addaUser(){
                this.$emit('add-user', this.name, this.age);
                this.name = '';
                this.age = '';
            }
        }
    }

</script>

<template>

    <div>
        <form @submit.prevent="submitData">
            <input type="text" placeholder="name" v-model="name"><br>
            <input type="text" placeholder="age" v-model="age">
            <button @click="addaUser">add user</button>
        </form>
    </div>
</template>

<style>

</style>
