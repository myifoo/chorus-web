<template>
  <div class='container-fix'>
    <div class='row'>
      <div class='col-md-4'>
          <span>
            <h1>name : {{name}}</h1>
            <h1>age : {{age}}</h1>
            <h1>{{details()}}</h1>
          </span>
      </div>
      <div class='col-md-4' v-html='message'></div>
      <div class='col-md-4'>
          <span>
            <label for="r1">修改颜色</label>
            <input type="checkbox" v-model="use" id="r1">
            <br><br>
            <div v-bind:class="{'class1': use}"> v-bind:class 指令  </div>
          </span>
      </div>
    </div>
    <div class='row'>
      <div class='col-md-4'>
          <span>.col-md-4</span>
      </div>
      <div class='col-md-4'>.col-md-4</div>
      <div class='col-md-4'>.col-md-4</div>
    </div>
    <div class='row'>
      <div class='col-md-4'>.col-md-4</div>
      <div class='col-md-4'>.col-md-4</div>
      <div class='col-md-4'>.col-md-4</div>
    </div>
    <div class='row'>
      <div class='col-md-4'>.col-md-4</div>
      <div class='col-md-4'>.col-md-4</div>
      <div class='col-md-4'>.col-md-4</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Example',
  data () {
    return {
      name: 'chorus',
      age: 22,
      message: '<h1>v-html message</h1>',
      use: false
    }
  },
  methods: {
    details: function () {
      return 'hello vue'
    }
  }
}
</script>

<style scoped>

.col-md-4 {
    height: 200px;
    border: 1px;
    border-style: dashed;
    border-color: #8080cc30;
    display: table;
}

.class1 {
    background-color: black
}

 span{ 
    display: table-cell;
    vertical-align: middle;
    text-align: center;
 }
</style>
