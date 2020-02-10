<template>
    <div>
        <h1>User Component</h1>
        <p>I'm a user</p>
        <button @click="changeName"> Change my name </button>
        <p>Name is {{ name }}</p>
        <div class="components-container">
            <UserDetails :myName="name"
                         @nameWasReset="name = $event"></UserDetails>
            <UserEdit></UserEdit>
        </div>
    </div>
</template>

<script>
    import UserDetails from './UserDetails';
    import UserEdit from './UserEdit';

    export default {
      data: function() {
        return {
          name: 'Max'
        }
      },
      methods: {
        changeName() {
          this.name = 'Alena'
        }
      },
      name: "User",
      components: {
        UserDetails,
        UserEdit
      },
    }
</script>
<style scoped>
    .components-container {
        background-color: lightblue;
        display: flex;
        padding: 80px;
        margin: 40px;
    }
</style>
