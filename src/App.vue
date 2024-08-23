<template>
    <div>
      <my-header/>
      <my-body/>
    </div>
</template>

<script>
import MyHeader from "@/components/MyHeader.vue";
import MyBody from "@/components/MyBody.vue";

export default {
  name: 'App',
  components: {
    MyHeader,
    MyBody
  }
}
</script>

<style>
* {
  font-family: 'Rawline-600',sans-serif;
  text-align: center;
  background-color: #FFFFFF;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
@font-face {
  font-family: 'Rawline-600', sans-serif;
  src: url('./assets/fonts/rawline-600.ttf');
  font-weight: 600;
}
@font-face {
  font-family: 'Rawline-400', sans-serif;
  src: url('./assets/fonts/rawline-cufonfonts/rawline-400i.ttf');
  font-weight: 400;
}
</style>
