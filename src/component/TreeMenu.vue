<template>
  <div class="tree-menu">
    <div :class="`menu-label menu-label${depth}`" @click="toggleChildren">
      <span>{{ label }}</span
      ><span class="arrow-bottom" v-if="nodes">></span>
    
    <div :class="`sub-menu${depth} sub-menu`">
      <tree-menu
        v-for="node in nodes"
        :nodes="node.nodes"
        :label="node.label"
        :depth="depth + 1"
      ></tree-menu>
    </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["label", "nodes", "depth"],
  name: "tree-menu",
  data() {
    return { showChildren: false };
  },
  computed: {
    indent() {
      return {  };
    },
  },
  methods: {
    toggleChildren() {
      this.showChildren = !this.showChildren;
    },
  },
};
</script>

<style>
.tree-menu {
  position: relative;
}
.menu-label {
  display: flex;
  font-size: 22px;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  cursor: pointer;
  align-items: center;
  padding: 5px 0;
  border-bottom: 1px solid rgba(97, 97, 97,0.4); 
}
.menu-label0{
  border: none;
}
.arrow-bottom {
  margin: 0 0 -7px 10px !important;
  padding: 0 !important;
  transform: scaleX(1.5) scale(0.75) rotateZ(90deg);
  display: block;
}
.sub-menu0 {
  top: 40px !important;
  left: 0 !important;
}
.sub-menu {
  margin-right: 10px !important;
  position: absolute;
  top: 0px;
  left: 153px;
  color: white;
  background-color: #1b325e;
  padding: 0 20px !important;
  border-radius: 5px;
  min-width: 130px;
  visibility: hidden;
  opacity: 0;
  transition: all 0.3s ease-in-out;
  /* transform: translateX(-50px) scale(0.8); */
  /* display: block !important; */
}

.menu-label0:hover .sub-menu0 {
  opacity: 1 !important;
  visibility: visible !important;
}

.menu-label1:hover .sub-menu1 {
  opacity: 1 !important;
  visibility: visible !important;
}

.menu-label2:hover .sub-menu2 {
  opacity: 1 !important;
  visibility: visible !important;
}

.menu-label3:hover .sub-menu3 {
  opacity: 1 !important;
  visibility: visible !important;
}

.menu-label4:hover .sub-menu4 {
  opacity: 1 !important;
  visibility: visible !important;
}

.menu-label5:hover .sub-menu5 {
  opacity: 1 !important;
  visibility: visible !important;
}

</style>
