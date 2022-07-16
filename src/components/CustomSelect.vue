<template>
  <div class="custom-select" :tabindex="tabindex" @blur="open = false">
    <div class="selected" :class="{ open: open }" @click="open = !open">
      {{ selected }}
    </div>
    <div class="items" :class="{ selectHide: !open }">
      <div
        v-for="(option, i) of options"
        :key="i"
        @click="
          selected = option;
          open = false;
          $emit('input', option);
        "
      >
        {{ option }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    options: {
      type: Array,
      required: true,
    },
    default: {
      type: String,
      required: false,
      default: null,
    },
    tabindex: {
      type: Number,
      required: false,
      default: 0,
    },
  },
  data() {
    return {
      selected: this.default
        ? this.default
        : this.options.length > 0
        ? this.options[0]
        : null,
      open: false,
    };
  },
  mounted() {
    this.$emit("input", this.selected);
  },
};
</script>

<style scoped>
.custom-select {
  position: relative;
  width: 100%;
  text-align: left;
  outline: none;
  height: 47px;
  line-height: 47px;
}

.custom-select .selected {
  background-color: #fff;
  border-radius: 3px 3px 0px 0px;
  color: #272733;
  padding-left: 10px;
  cursor: pointer;
  user-select: none;
}

.custom-select .selected.open {
    background: rgba(61, 64, 80, 0.85);
    border-radius: 3px 3px 0px 0px;
    color: #fff;

}

.custom-select .selected:after {
  position: absolute;
  content: "";
  top: 22px;
  right: 1em;
  width: 0;
  height: 0;
  border: 5px solid transparent;
  border-color: #272733 transparent transparent transparent;
}
.custom-select .selected.open:after {
    border-color: #fff transparent transparent transparent;
    transform: rotate(180deg);
    top: 18px;
}

.custom-select .items {
  color: #fff;
  border-radius: 0px 0px 6px 6px;
  overflow: hidden;
  border-right: 1px solid #3D4050;;
  border-left: 1px solid #3D4050;
  border-bottom: 1px solid #3D4050;;
  position: absolute;
  background-color: #272733;
  left: 0;
  right: 0;
  z-index: 1;
  overflow-y: scroll;
  max-height: 226px;
}

.custom-select .items div {
  color: #fff;
  padding-left: 1em;
  cursor: pointer;
  user-select: none;
}

.custom-select .items div:hover {
  color: #3E9CDC;
}

.selectHide {
  display: none;
}

</style>
