<template>
  <div style="width: 100%">
    <WBtopAppBar title="Title" variant="standard" ref="topAppBar"></WBtopAppBar>
    <WBdrawer topappbar="standard" ref="drawer"></WBdrawer>
    <WBdrawerMainContent topappbar="standard" ref="drawerMainContent">
      
      <WBbutton></WBbutton>
      <WBbuttonFAB></WBbuttonFAB>
      <WBbuttonIcon></WBbuttonIcon>
      <WBcard img="https://material-components.github.io/material-components-web-catalog/static/media/photos/3x2/2.jpg" :action="false"></WBcard>
      <WBcheckbox></WBcheckbox>
      <WBchipContainer>
        <WBchip text="chipsa osak ksakd"></WBchip>
        <WBchip text="chipsa hahaha ksakd"></WBchip>
      </WBchipContainer>

      <WBdataTable>
        <WBdataTableHead>
          <WBdataTableColumn text="coluna 1"></WBdataTableColumn>
          <WBdataTableColumn text="coluna 2"></WBdataTableColumn>
          <WBdataTableColumn text="coluna 3"></WBdataTableColumn>
        </WBdataTableHead>

        <WBdataTableBody>
          <WBdataTableRow>
            <WBdataTableColumn variant="body" text="coluna 1"></WBdataTableColumn>
            <WBdataTableColumn variant="body" text="coluna 2"></WBdataTableColumn>
            <WBdataTableColumn variant="body" text="coluna 3"></WBdataTableColumn>
          </WBdataTableRow>
        </WBdataTableBody>
      </WBdataTable>

      <WBlist>
        <WBlistItem></WBlistItem>
        <WBlistItem></WBlistItem>
      </WBlist>

      <WBmodal ref="modal">

      </WBmodal>

      <WBradioButton></WBradioButton>
      <WBradioButton></WBradioButton>

      <WBtextfield></WBtextfield>

      <WBselect :items="['op1', 'op2']">

      </WBselect>

    </WBdrawerMainContent>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator';
import { Builder } from '_PagesSrc/ts/designSystem/Builder';
import WBtopAppBar from '_Components/designSystem/WBtopAppBar.vue';
import WBdrawer from '_Components/designSystem/WBdrawer.vue';
import WBdrawerMainContent from '_Components/designSystem/WBdrawerMainContent.vue';
import WBbutton from '_Components/designSystem/WBbutton.vue';
import WBbuttonFAB from '_Components/designSystem/WBbuttonFAB.vue';
import WBbuttonIcon from '_Components/designSystem/WBbuttonIcon.vue';
import WBcard from '_Components/designSystem/WBcard.vue';
import WBcheckbox from '_Components/designSystem/WBcheckbox.vue';
import WBchip from '_Components/designSystem/WBchip.vue';
import WBchipContainer from '_Components/designSystem/WBchipContainer.vue';
import WBdataTable from '_Components/designSystem/WBdataTable.vue';
import WBdataTableHead from '_Components/designSystem/WBdataTableHead.vue';
import WBdataTableBody from '_Components/designSystem/WBdataTableBody.vue';
import WBdataTableRow from '_Components/designSystem/WBdataTableRow.vue';
import WBdataTableColumn from '_Components/designSystem/WBdataTableColumn.vue';
import WBlist from '_Components/designSystem/WBlist.vue';
import WBlistItem from '_Components/designSystem/WBlistItem.vue';
import WBmodal from '_Components/designSystem/WBmodal.vue';
import WBradioButton from '_Components/designSystem/WBradioButton.vue';
import WBtextfield from '_Components/designSystem/WBtextfield.vue';
import WBselect from '_Components/designSystem/WBselect.vue';

@Component({
  components: {
    WBtopAppBar,
    WBdrawer,
    WBdrawerMainContent,
    WBbutton,
    WBbuttonFAB,
    WBbuttonIcon,
    WBcard,
    WBcheckbox,
    WBchip,
    WBchipContainer,
    WBdataTable,
    WBdataTableHead,
    WBdataTableBody,
    WBdataTableRow,
    WBdataTableColumn,
    WBlist,
    WBlistItem,
    WBmodal,
    WBradioButton,
    WBtextfield,
    WBselect
  }
})
export default class MyClass extends Vue {
  mounted() {
    // window.setTimeout(() => {
    //   console.log((<any>this.$refs.modal).element.mdc.open());
    // }, 5000);

    this.$nextTick(() => {
      const builder = Builder.getInstance();
      builder.afterMounted();
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
</style>