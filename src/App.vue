<template>
  <div>
    <div class="menu-box">
      <div v-for="tree in trees" class="menu-item">
        <tree-menu
          :nodes="tree.tree.nodes"
          :label="tree.tree.label"
          :depth="0"
        ></tree-menu>
      </div>
    </div>
  </div>
</template>

<script>
import TreeMenu from "./component/TreeMenu.vue";
export default {
  components: {
    "tree-menu": TreeMenu,
  },
  data() {
    return {
      trees: [
        {
          tree: {
            label: "Senat",
            nodes: [
              {
                label: "item1",
                nodes: [
                  {
                    label: "item1.1",
                    nodes: [
                      {
                        label: "item1.2.1",
                      },
                    ],
                  },
                  {
                    label: "item1.2",
                    nodes: [
                      {
                        label: "item1.2.1",
                      },
                    ],
                  },
                ],
              },
              {
                label: "item2",
                nodes: [
                  {
                    label: "item1.2.1",
                    nodes: [
                      {
                        label: "item1.2.1",
                        nodes: [
                          {
                            label: "item1.2.1",
                            nodes: [
                              {
                                label: "item1.2.1",
                              },
                            ],
                          },
                        ],
                      },
                    ],
                  },
                ],
              },
            ],
          },
        },
        {
          tree: {
            label: "hujjatlar",
            nodes: [
              {
                label: "item1",
                nodes: [
                  {
                    label: "item1.1",
                    nodes: [
                      {
                        label: "item1.2.1",
                      },
                    ],
                  },
                  {
                    label: "item1.2",
                    nodes: [
                      {
                        label: "item1.2.1",
                      },
                    ],
                  },
                ],
              },
              {
                label: "item2",
                nodes: [
                  {
                    label: "item1.2.1",
                    nodes: [
                      {
                        label: "item1.2.1",
                        nodes: [
                          {
                            label: "item1.2.1",
                            nodes: [
                              {
                                label: "item1.2.1",
                              },
                            ],
                          },
                        ],
                      },
                    ],
                  },
                ],
              },
            ],
          },
        },
        {
          tree: {
            label: "Media",
          },
        },
        {
          tree: {
            label: "Kontakt",
          },
        },
      ],
    };
  },
  methods: {
    greeting: function () {
      // return <h1>jhhj</h1>;
    },
  },
};
</script>

<style>
.menu-box {
  display: flex;
  margin: 10px;
}
.menu-item {
  margin-right: 60px;
}
</style>
