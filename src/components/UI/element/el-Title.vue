<script>
export default {
  name: "el-title",
  props: {
    param: {
      type: String,
      required: false,
      default: "just",
    },
  },
  computed: {
    returnClass() {
      return ["element", `element-${this.param}`];
    },
  },
};
</script>

<template>
  <span :class="returnClass"><slot></slot></span>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/var' as v;

$element-sizes: (
  "main": (
    "font-size": 37px,
    "font-weight": 400,
    "text-align": center,
    "display": block,
  ),
  "just": (
    "font-size": 27px,
    "font-weight": 400,
  ),
);

@each $name, $sizeMap in $element-sizes {
  .element-#{$name} {
    text-align: map-get($sizeMap, "text-align");
    display: map-get($sizeMap, "display");

    @media (min-width: 576px) {
      font-size: map-get($sizeMap, "font-size");
      font-weight: map-get($sizeMap, "font-weight");
    }
    @media (max-width: 576px) {
      font-size: calc(#{map-get($sizeMap, "font-size")} - 4px);
      font-weight: map-get($sizeMap, "font-weight");
    }
  }
}

.element {
  font-family: "sfuid";
  color: v.$color1;
}
</style>
