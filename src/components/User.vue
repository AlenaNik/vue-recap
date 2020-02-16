<template>
    <div class="wrapper">
        <app-user-detail></app-user-detail>
        <app-user-edit></app-user-edit>
    </div>
</template>

<script>
import UserDetails from './UserDetails'
import UserEdit from './UserEdit'
export default {
  components: {
    appUserDetail: UserDetails,
    appUserEdit: UserEdit
  }
}

</script>

<style scoped>
    .wrapper {
        height: 400px;
        background-color: lightblue;
        display: grid;
        grid-template-columns: 1fr 1fr;
        place-items: center;
    }

</style>
