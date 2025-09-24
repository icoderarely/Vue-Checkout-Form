<script>
import AccountPreferences from './components/AccountPreferences.vue';
import Profile from './components/Profile.vue';

export default {
  components: {
    Profile,
    AccountPreferences,
  }
}
</script>

<template>
  <h1>You did it!</h1>
  <Profile />
  <AccountPreferences />
</template>

<style scoped></style>
