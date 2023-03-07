<template>
  <div>
    <h1>Books Management System</h1>
    <div>
      <button class="btn" @click="$router.push('/booksManage')">Start For Free</button>
    </div>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>
.btn{
  background-color: dodgerblue;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    font-size: 14px;
    cursor: pointer;
}
</style>