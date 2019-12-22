<template>
  <div style="width: 100%">
    <WBtopAppBar title="Sistema" variant="standard">
      <WBlist id="WBlist-1">
        <WBlistItem primaryText="Categorias" secondaryText leftIcon></WBlistItem>
        <WBlistItem primaryText="Sobre Nós" secondaryText leftIcon></WBlistItem>
        <WBlistItem primaryText="Contate-nos" secondaryText leftIcon></WBlistItem>
        <WBlistItem primaryText="Entrar" secondaryText leftIcon="input"></WBlistItem>
      </WBlist>
    </WBtopAppBar>
    <WBdrawer topappbar="standard">
      <WBlist>
        <WBlistItem primaryText="Categorias" secondaryText leftIcon></WBlistItem>
        <WBlistItem primaryText="Sobre Nós" secondaryText leftIcon></WBlistItem>
        <WBlistItem primaryText="Contate-nos" secondaryText leftIcon></WBlistItem>
      </WBlist>
    </WBdrawer>
    <WBdrawerMainContent topappbar="standard">
      <router-view />
    </WBdrawerMainContent>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator';
import WBtopAppBar from '_Components/designSystem/WBtopAppBar.vue';
import WBdrawer from '_Components/designSystem/WBdrawer.vue';
import WBdrawerMainContent from '_Components/designSystem/WBdrawerMainContent.vue';
import WBlist from '_Components/designSystem/WBlist.vue';
import WBlistItem from '_Components/designSystem/WBlistItem.vue';
import { Builder } from '_PagesSrc/ts/designSystem/Builder';

@Component({
  components: {
    WBtopAppBar,
    WBdrawer,
    WBdrawerMainContent,
    WBlist,
    WBlistItem
  }
})
export default class MyClass extends Vue {
  mounted() {
    this.$nextTick(() => {
      Builder.getInstance().afterMounted();
    });
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

.mdc-top-app-bar__section,
.mdc-top-app-bar__section--align-end {
  padding: 0px 12px;
}

#WBlist-1 {
  display: flex;
  color: white;
  padding: 0px 8px;
  height: 100%;

  li {
    user-select: none;
    height: 100%;

    .material-icons {
      margin-right: 16px;
      color: white;
    }
  }

  @media screen and (max-width: $mobile-bp) {
    display: none;
  }
}
</style>