title: Picker
---
多列选择器。

## 引入

```js
import { Picker } from 'we-vue'
Vue.component(Picker.name, Picker)
```

## 例子

### 基本示例

```html
<template>
  <div class="page page-with-padding">
    <wv-button @click="ticketPickerShow = true">单列选择器</wv-button>
    <wv-button @click="dayPickerShow = true">多列选择器</wv-button>

    <wv-picker v-model="ticketPickerShow" :slots="ticketSlots" @change="onChange"></wv-picker>
    <wv-picker v-model="dayPickerShow" :slots="daySlots" @change="onChange"></wv-picker>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        ticketValue: [],
        dayValue: [],
        ticketPickerShow: false,
        dayPickerShow: false,
        ticketSlots: [
          {
            values: [
              '汽车票',
              '飞机票',
              '火车票',
              '轮船票',
              '其它'
            ],
            defaultIndex: 2
          }
        ],
        daySlots: [
          {
            values: [
              '星期一',
              '星期二',
              '星期三',
              '星期四',
              '星期五'
            ],
            defaultIndex: 0
          },
          {
            values: [
              '上午',
              '下午'
            ],
            defaultIndex: 0
          }
        ]
      }
    },

    methods: {
      onChange (picker, value) {
        this.$nextTick(() => {
          console.log(picker.getValues())
        })
      }
    }
  }
</script>
```

### 省市区三级联动

**省市区三级联运示例代码较多，不便于在文档中显示和查看，建议查看[相应示例的源码](https://github.com/tianyong90/we-vue/blob/master/example/pages/picker.vue)**


## API

- picker

|   参数   |   类型    |   说明   | 可选值  |  默认值  |
| :----: | :-----: | :----: | :--: | :---: |
| confirm-text  | String  |  默认按钮文字   |      |   '确定'    |
| cancel-text  | String  |  取消按钮文字   |      |   '取消'    |
| slots  | Array  |  待选数据   |      |       |
| value-kay  | String  |  当前选中项 key   |      |       |

- picker-slot

|   参数   |   类型    |   说明   | 可选值  |  默认值  |
| :----: | :-----: | :----: | :--: | :---: |
| values  | Array  |  默认按钮文字   |      |   '确定'    |
| value  | Object  |  当前选中数据   |      |       |
| value-kay  | String  |  当前选中项 key   |      |       |

## Events

|   事件名   |   说明    |   参数   |
| :----: | :-----: | :----: |
| change  | 所选值改变  |  当前组件示例   |
| confirm  | confirm 按钮点击事件  |     |
| cancel  | cancel 按钮点击事件  |     |
