<template>
  <div class="hello">
    <h1>Ice Cream Challenge {{ nowNum }}</h1>
    <div class="col">
      <form id="code" class="form-group">
        <div class="form-group">
          {{ msg }}
          <input
            type="code"
            v-model="submitCode"
            class="form-control"
            id="exampleInputEmail1"
            placeholder="Mã bí mật"
          />
        </div>
        <button type="" @click="submit" class="btn btn-danger">Submit</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "Decode",
  data: () => ({
    nowNum: 1,
    msg: "",
    dataCode: [
      { challengeNum: 1, code: "ABC" },
      { challengeNum: 2, code: "AAA" },
      { challengeNum: 3, code: "BBB" },
      { challengeNum: 4, code: "DDD" },
      { challengeNum: 5, code: "ALAL" },
    ],
  }),
  methods: {
    submit() {
      this.nowNum = this.nowNum + 1;
      if (
        this.dataCode.find(this.checkCode(code)) &&
        this.dataCode.isFinite((item) => item.challengeNum === this.nowNum)
      ) {
        this.msg = "Thành công";
      } else {
        this.msg = "Sai rồi :)";
      }
    },
    checkCode(code) {
      return this.submitCode === code;
    },
    checkChalNum() {},
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
