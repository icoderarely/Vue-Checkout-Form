<script>
// import InputText from 'primevue/inputtext';
import { Textarea, InputText, Button } from 'primevue'

export default {
  components: {
    InputText,
    Textarea,
    Button
  },
  data() {
    return {
      name: null,
      bio: null,
    }
  }
}
</script>

<template>
  <div>
    <label for="name">Enter Name: </label><br>
    <!-- <input type="text" v-model="name"> -->
    <InputText id="name" type="text" v-model="name" />

    <br>
    <label for="bio">Bio:</label><br>
    <!-- <textarea name="bio" id="bio" v-model="bio"></textarea> -->
    <Textarea v-model="bio" rows="2" cols="30" />
    <br>
    <Button>Click Me</Button>
  </div>
</template>
