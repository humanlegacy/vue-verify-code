### 纯前端实现验证码功能

```html
  <vueVerifyCode @getCode="getCode" ref="verify"/>
```
```js
import vueVerifyCode from 'vue-verify-code'

components: { vueVerifyCode },,
methods: {
  getCode(code) {
    // 接收正确的验证码
    this.code = code
  }
}
```
### 属性
```js

  props: {
    // 验证码宽度
    width: {
      type: Number,
      default: 90
    },

    // 验证码高度
    height: {
      type: Number,
      default: 35
    },

    // 验证码字体
    codeFont: {
      type: String,
      default: '22px arial'
    },

    // 验证码类型   
    // calc：验证码为计算公式
    // code：验证码为数字大小写字母组合
    codeType: {
      type: String,
      default: 'code' //calc | code
    },

    // 验证码长度
    codeLength: {
      type: Number,
      default: 5
    },

    // 验证码大小写是否敏感
    strict: {
      type: Boolean,
      default: true
    },

    // 验证码计算范围
    calcRange: {
      type: Array,
      default: [10, 20]
    },
    // 验证码计算符号
    calcSymbol: {
      type: Array,
      default: ['+', '-', '*']
    },

    // 背景干扰线数量
    lineCount: {
      type: Number,
      default: 5
    }
  }
```