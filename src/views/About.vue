<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div :class="{ active: isActive }">
      Hello Vue JS
    </div>
    <div style="margin-top: 10px;" :class=" isActive ? 'active' : ''">
      Hello World
    </div>
    <button style="margin-top:10px" @click="toogleBtn()">{{btnLabel}}</button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isActive: false,
      btnLabel: "Active"
    };
  },
  methods:{
    toogleBtn(){
      this.isActive = !this.isActive;
      this.btnLabel = !this.isActive ? "Active" : "Deactive";
    }
  }
};
</script>
<style scoped>
.active {
  background-color: blue;
  color: white;
}
</style>
