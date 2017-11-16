<template>
  <div class="hello">
    <tree-grid :columns="columns" :tree-structure="true" :data-source="dataSource"></tree-grid>
  </div>
</template>

<script>
import {TreeGrid} from './treeTable'
export default {
  name: 'hello',
  data () {
    return {
      columns: [
          {
            text: '姓名',
            dataIndex: 'name'
          },
          {
            text: '年龄',
            dataIndex: 'age'
          },
          {
            text: '性别',
            dataIndex: 'sex'
          }
        ],
      dataSource: [
        {
          id: 1,
          parent_department: 0,
          name: '测试1',
          age: 18,
          sex: '男',
          children: [
            {
              id: 2,
              parent_department: 1,
              name: '测试2',
              age: 22,
              sex: '男'
            }
          ]
        },
        {
          id: 3,
          parent_department: 0,
          name: '测试3',
          age: 23,
          sex: '女',
          children: [
            {
              id: 4,
              parent_department: 3,
              name: '测试4',
              age: 22,
              sex: '男'
            },
            {
              id: 5,
              parent_department: 3,
              name: '测试5',
              age: 25,
              sex: '男'
            },
            {
              id: 6,
              parent_department: 3,
              name: '测试6',
              age: 26,
              sex: '女',
              children: [
                {
                  id: 7,
                  parent_department: 6,
                  name: '测试7',
                  age: 27,
                  sex: '男'
                }
              ]
            }
          ]
        },
        {
          id: 18,
          parent_department: 0,
          name: '测试8',
          age: 18,
          sex: '男'
        }
      ],
      // dataSource: [
      //   {
      //       id: 1,
      //       name: "A部门",
      //       parent_department: 0,
      //       tag: "111",
      //       level: 0
      //   },
      //   {
      //       id: 15,
      //       name: "A-1部门111123qweqw",
      //       parent_department: 1,
      //       tag: "111111",
      //       level: 1
      //   },
      //   {
      //       id: 4,
      //       name: "B部门123123",
      //       parent_department: 0,
      //       tag: "11",
      //       level: 0
      //   },
      //   {
      //       id: 12,
      //       name: "C部门",
      //       parent_department: 0,
      //       tag: "11111",
      //       level: 0
      //   },
      //   {
      //       id: 14,
      //       name: "D部门",
      //       parent_department: 0,
      //       tag: "11222",
      //       level: 0
      //   }
      // ]
    }
  },
  components: {
    TreeGrid
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
