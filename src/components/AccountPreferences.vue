<script>
import { Checkbox, RadioButton, RadioButtonGroup, Select } from 'primevue';
export default {
  components: {
    Checkbox,
    RadioButton,
    RadioButtonGroup,
    Select,
  },
  data() {
    return {
      isSub: false,
      selectedContact: null,
      contactOption: [
        { op: "Email", key: "email" },
        { op: "Phone", key: "phone" },
        { op: "None", key: "none" },
      ],
      selectedCity: null,
      cities: [
        { name: 'New York', code: 'NY' },
        { name: 'Rome', code: 'RM' },
        { name: 'London', code: 'LDN' },
        { name: 'Istanbul', code: 'IST' },
        { name: 'Paris', code: 'PRS' }
      ]
    }
  },
}
</script>

<template>
  <Checkbox inputId="newsletter" v-model="isSub" binary />
  <label for="newsletter"> Subscribe to newsletter</label>
  <br />
  <label for="contact">Preferred Contact Method: </label>

  <!-- <RadioButtonGroup v-model="ingredient" name="pizza"> -->
  <!--   <RadioButton inputId="email" value="email" /> -->
  <!--   <label for="email"> Email &nbsp;</label> -->
  <!--   <RadioButton inputId="phone" value="phone" /> -->
  <!--   <label for="phone"> Phone &nbsp;</label> -->
  <!--   <RadioButton inputId="none" value="none" /> -->
  <!--   <label for="none"> None</label> -->
  <!-- </RadioButtonGroup> -->
  <template v-for="contact in contactOption" :key="contact.key">
    <RadioButton v-model="selectedContact" :input-id="contact.key" name="dynamic" :value="contact.key" />
    <label :for="contact.key">{{ contact.op }}</label>
  </template>
  <br>

  <Select v-model="selectedCity" :options="cities" optionValue="name" optionLabel="name" placeholder="Select a City"
    class="w-full md:w-56" />

</template>
