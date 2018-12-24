<template>
  <div id="timer">
    <Calendar></Calendar>
  </div>
</template>
<script>
import Calendar from "vue-calendar-component";
export default {
  name: "Timer",
  data() {
    return {};
  },
   components: {
    Calendar
  }
};
</script>
<style lang="less" scoped>
#timer{
  margin-top: 10px
}
</style>
