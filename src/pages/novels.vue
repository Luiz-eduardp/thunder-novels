<template>
<q-page padding>
  {{novelList}}

</q-page>
</template>

<script>

export default {
    // name: 'PageName',
    data() {
        return {
            novelList: []
        }
    },
  created() {
  // Simple GET request using fetch
  fetch("./jsons/novels.json")
    .then(response => response.json())
    .then(data => (this.novelList = data));
}
}
</script>
