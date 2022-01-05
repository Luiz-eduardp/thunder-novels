<template>
  <q-page padding>
    <q-banner dense inline-actions class="text-white bg-red" style="height:100%">
      You have lost connection to the internet. This app is offline.
      <template v-slot:action>
        <q-btn flat color="white" label="Turn ON Wifi" />
      </template>
    </q-banner>
  </q-page>
</template>

<script>
export default {
  // name: 'PageName',
}
</script>
