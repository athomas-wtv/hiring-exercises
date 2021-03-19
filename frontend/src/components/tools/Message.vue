<template>
  <div>
    <p>{{messageText}}</p>
  </div>
</template>
<script>

export default {
  name: "Message",
  components: {
  },
  props: ['messageText'],
  data() {
    return {
      message: ''
    }
  },
  methods: {
    
  },
}
</script>
