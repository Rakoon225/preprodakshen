<script>
export default {
  name: "el-description",
  props: {
    param: {
      type: String,
      require: false,
      default: "none",
    },
  },
  computed: {
    // titleClass() {
    //   return ["title", `title-${this.param}`];
    // },
  },
};
</script>

<template>
  <p :class="`element`"><slot></slot></p>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/var' as v;

// $title-sizes: (
//   "main": (
//     "font-size": 37px,
//     "font-weight": 400,
//     "text-align": center,
//     "display": block,
//   ),
// );

// @each $name, $sizeMap in $title-sizes {
//   .title-#{$name} {
//     text-align: map-get($sizeMap, "text-align");
//     display: map-get($sizeMap, "display");

//     @media (min-width: 576px) {
//       font-size: map-get($sizeMap, "font-size");
//       font-weight: map-get($sizeMap, "font-weight");
//     }
//     @media (max-width: 576px) {
//       font-size: calc(#{map-get($sizeMap, "font-size")} - 4px);
//       font-weight: map-get($sizeMap, "font-weight");
//     }
//   }
// }

.element {
  font-family: "sfuid";
  font-weight: 300;
  color: v.$color1;
  @media(min-width: 576px){
    font-size: 18px;
  }
  @media(max-width: 576px){
    font-size: 16px;
  }
}
</style>
