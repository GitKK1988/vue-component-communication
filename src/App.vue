<script>
import ActiveUser from './components/ActiveUser.vue';
import UserData from './components/UserData.vue';

export default {
  components: {
    ActiveUser,
    UserData
  },
  data(){
    return {
      users: [
      ],
    }
  },
  methods: {
    addnewUser(newname, newage){
      console.log(newname, newage);
      const newUser = {
        id: new Date().toISOString(),
        name: newname,
        age: newage
      }
      this.users.push(newUser);
      
    }
  }
  
}
</script>

<template>

  <div>
    <UserData @add-user="addnewUser"></UserData>

    <div v-for="user in users" :key="user.id">
      <ActiveUser :user="user"></ActiveUser>
    </div>
    
    
  </div>

</template>

<style scoped>

</style>
