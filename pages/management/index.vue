<template>
  <div class="group">
    <div>
      <h2>生徒管理ページ</h2>
      <table>
        <tr>
          <th>名前</th>
          <th>ID</th>
        </tr>
        <tr v-for="student in students" :key="student.index">
          <td>{{student.name}}</td>
          <td>{{student.id}}</td>
        </tr>
      </table>
      <p><NuxtLink to = "/" class="nuxt">戻る</NuxtLink></p>
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
  h2,p{
    text-align: center;
  }

  tr,th,td{

    padding: 30px;
  }
</style>
