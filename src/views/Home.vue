<template>
  <div class="home">
    <Form />
    <Location />
    <Geolocation />

  </div>
</template>

<script>
import Form from "../components/Form.vue"
import Location from "../components/Location.vue"
import Geolocation from "../components/Geolocation.vue"


export default {
  name: 'Home',
  components: { Form, Location, Geolocation }
}
</script>
