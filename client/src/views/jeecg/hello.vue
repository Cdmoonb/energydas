



<template>
  <div>
    {{msg}}
  </div>
</template>
<script>
  import {getAction} from '../../api/manage'
  export default {
    data() {
      return {
        msg: ''
      }
    },

    methods: {
      hello() {
        var url = "/test/jeecgDemo1/hello"
        getAction(url).then((res) => {
          if (res.success) {
            this.msg = res.result;
          }
        })

      }
    },
    created() {
      this.hello();
    }
  }

</script>