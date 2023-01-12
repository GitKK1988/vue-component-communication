<script>

    export default {
        name: 'ActiveUser',
        props: ['user'],
        data(){
            return {
                activeuser: {
                    id: this.user.id,
                    name: this.user.name,
                    age: this.user.age
                }
            }
        }
    }

</script>

<template>

    <div>
        <p>Id: {{ user.id }}</p>
        <p>Name: {{ user.name }}</p>
        <p>Age: {{ user.age }}</p>
    </div>
</template>

<style>

</style>
