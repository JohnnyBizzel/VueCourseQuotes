<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
      <div class="panel quote">      
      <slot name="content"></slot>
      </div>

    </div>
</template>

<script>
export default {
  props: ["quotes"]
};
</script>

<style scoped>
.panel {
  border: 1px solid red;
  box-shadow: 1px 1px 2px black;
  padding: 30px;
  margin: 30px auto;
  text-align: center;
}
.quote {
  /* cursor: pointer;*/
  
    /* cursor: url(../assets/iconmonstr-trash-can-27.svg), auto; */
  
}
.quote:hover {
  background-color: #ffefef;
  cursor: url('https://uploads.codesandbox.io/uploads/user/7a85e947-b83d-42b1-97ff-756aa2b4517b/H_nu-iconmonstr-trash-can-27.svg'), auto;
}
</style>
