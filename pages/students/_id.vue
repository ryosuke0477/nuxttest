<template>
  <div class="student_id">
    <div>
      <h2>
        {{student}}
      </h2>
      <p><NuxtLink to = "/students" class="nuxt-first">生徒一覧へ戻る</NuxtLink></p>
      <p><NuxtLink to = "/" class="nuxt">トップページへ</NuxtLink></p>
    </div>
  </div>
</template>


<script>
export default {
    validate({ params }) {
      // const validate = 0;
      // this.students.forEach(element => {
      //    if(element.id==params.id){
      //     validate=1
      //   };
      // });
    //   if (validate == 0) {
    //   return false
    //     } else {
    //       return true
    // }
    //   if (params.id == this.students[0].id | params.id == this.students[1].id | params.id == this.students[2].id) {
    //   return true
    //     } else {
    //       return false
    // }
    if (params.id === undefined) {
      return false
    } else {
      return true
    }

  },
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
      student:"初期値",
      receiveId:this.$route.params.id
    };
  },
    created() {
        this.students.forEach(element => {
        if(element.id==this.receiveId){
          this.student=element.name
        }
      });
  },

};
</script>


<style>
.student_id {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

p{
  display: inline-block;
}

.nuxt-first{
    border-right: solid;
    padding-right: 10px;
}

</style>