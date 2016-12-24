<template>
  <div>
    <doc :name="name"
      :desc="desc"
      :parm_desc="parm_desc"
      :parms="parms"
      :code="code"
      >
      <clipboard :content="message"></clipboard>
    </doc>
  </div>
</template>

<script>
  import Clipboard from './Bz'
  import Doc from 'bz-doc'

  export default {
    components: {
      Doc,
      Clipboard
    },
    data: function () {
      return {
        title: 'Clipboard',
        desc: '点击复制',
        parm_desc: `注意，要把ZeroClipboard.swf 放到 /static/ZeroClipboard.swf 才能使用`,
        message: '复制到clipborad的内容',
        code: `<Clipboard><input type="text"></Clipboard>`,
        parms: [
          {parm: 'content', desc: '要copy的文本内容'}
        ]
      }
    }
  }
</script>
