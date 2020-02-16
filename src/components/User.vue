<template>
    <div class="wrapper">
       <p>User component</p>
        {{ name }}
        <button @click="changeName">Change name</button>
        <app-user-detail :user="name" @nameWasReset="name = $event"></app-user-detail>
        <app-user-edit></app-user-edit>
    </div>
</template>

<script>
import UserDetails from './UserDetails'
import UserEdit from './UserEdit'
export default {
  data: function() {
    return {
      name: 'Alena',
    }
  },
  methods: {
    changeName() {
      this.name = 'Jaime'
    }
  },
  components: {
    appUserDetail: UserDetails,
    appUserEdit: UserEdit
  }
}

</script>

<style scoped>
    .wrapper {
        background-color: lightblue;
        display: grid;
        grid-template-columns: 1fr 1fr;
        place-items: center;
    }

</style>
