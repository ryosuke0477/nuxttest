<template>
  <div class="students">
    <div>
      <h2>生徒一覧</h2>
      <ul>
        <li v-for="student in students" :key="student.index">
          <NuxtLink :to = "student.link" class="nuxt">{{student.name}}</NuxtLink>
        </li>
      </ul>
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
          link: "/students/qnfungqxllc3m1ak"
        },
        {
          id: "7j9cumkgsq6l264c",
          name: "生徒B",
          link: "/students/7j9cumkgsq6l264c"
        },
        {
          id: "eo34bhey9m0d92ou",
          name: "生徒C",
          link: "/students/eo34bhey9m0d92ou"
        },
      ],
    };
  },

};
</script>


<style>
.students {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>