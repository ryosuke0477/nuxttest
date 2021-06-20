<template>
  <div class="group">
    <div class="student">
      <h2 class="student-list">生徒一覧</h2>
      <p class="student-watch"><NuxtLink to = "/students" class="nuxt">生徒の情報を見る</NuxtLink></p>
    </div>
    <div class="admin">
      <h2 class="admin-list">管理者</h2>
      <p class="admin-watch"><NuxtLink to = "/management" class="nuxt">管理画面を見る</NuxtLink></p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      students: [
        {
          id: "qnfungqxllc3m1ak",
          name: "生徒A",
        },
        {
          id: "7j9cumkgsq6l264c",
          name: "生徒B",
        },
        {
          id: "eo34bhey9m0d92ou",
          name: "生徒C",
        },
      ],
    };
  },
};

</script>
  
<style>

  .group{
    display: flex;
    justify-content: center;
    align-items: center;
    height: 90vh;
  }
  .student{
    width: 200px;
    margin-right: 20px;
    text-align: center;
  }
  .admin{
    width: 200px;
    margin-left: 20px;
      text-align: center;
  }
</style>
