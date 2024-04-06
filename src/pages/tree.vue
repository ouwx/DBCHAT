<template>
  <div>
    <el-radio v-model="radio" label="1">备选项</el-radio>
    <el-radio v-model="radio" label="2">备选项</el-radio>
    <div class="buttons">
      <el-button @click="getCheckedNodes">切换数据库</el-button>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      radio: '1'
    };
  },
  methods: {
    async postData() {
      try {
        const response = await axios.post('http://example.com/api/post', {
          data: 'your data'
        });
        console.log(response.data);
      } catch (error) {
        console.error(error);
      }
    },    
    }
  }
};
</script>