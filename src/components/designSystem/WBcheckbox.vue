<template>
  <div class="mdc-form-field" :id="id" :data-wbid="'checkbox' + _uid">
    <div class="mdc-checkbox">
      <input type="checkbox" class="mdc-checkbox__native-control" :id="'checkbox-' + _uid" />
      <div class="mdc-checkbox__background">
        <svg class="mdc-checkbox__checkmark" viewBox="0 0 24 24">
          <path
            class="mdc-checkbox__checkmark-path"
            fill="none"
            d="M1.73,12.91 8.1,19.28 22.79,4.59"
          />
        </svg>
        <div class="mdc-checkbox__mixedmark"></div>
      </div>
    </div>
    <label :for="'checkbox-' + _uid">{{label}}</label>
  </div>
</template>

<script>
import { Builder } from "_PagesSrc/ts/designSystem/Builder";

export default {
  props: {
    id: null,
    label: { default: "Checkbox Label" }
  },
  data: function() {
    return {
      element: null
    };
  },
  mounted() {
    this.element = Builder.getInstance().init("WBcheckbox", "checkbox" + this._uid);
  }
};
</script>