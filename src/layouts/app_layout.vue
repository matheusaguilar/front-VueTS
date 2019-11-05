<template>
  <div style="width: 100%">
    <WBtopAppBar title="Title" variant="standard"></WBtopAppBar>
    <WBdrawer topappbar="standard"></WBdrawer>
    <WBdrawerMainContent topappbar="standard">
     
    </WBdrawerMainContent>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator';
import WBtopAppBar from '_Components/designSystem/WBtopAppBar.vue';
import WBdrawer from '_Components/designSystem/WBdrawer.vue';
import WBdrawerMainContent from '_Components/designSystem/WBdrawerMainContent.vue';

import { Teste } from '_PagesSrc/ts/array';

@Component({
  components: {
    WBtopAppBar,
    WBdrawer,
    WBdrawerMainContent
  }
})
export default class MyClass extends Vue {

  mounted() {
    console.log(Teste);
    const x = new Teste();
    x.teste();
    console.log('kasdkas ksakdksa ksa ');
  }

  teste() {
    const x = '5';
    console.log(x);
  }
}
</script>

<style lang="scss">
body {
  margin: 0px;
  display: flex;
  height: 100vh;
  background: #f1f1f1;
}
</style>