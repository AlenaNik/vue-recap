<template>
    <div class="wrapper">
       <p>User component</p>
        {{ name }}
        <button @click="changeName">Change name</button>
        <app-user-detail
                :user="name"
                @nameWasReset="name = $event"
                :resetFn="resetName"
                :userage="age"
        ></app-user-detail>
        <app-user-edit :userage="age"
                       @AgeUpdate="age = $event"
        ></app-user-edit>
    </div>
</template>

<script>
import UserDetails from './UserDetails'
import UserEdit from './UserEdit'
export default {
  data: function() {
    return {
      name: 'Alena',
      age: 28
    }
  },
  methods: {
    changeName() {
      this.name = 'Jaime'
    },
    resetName() {
      this.name = 'Baton'
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
