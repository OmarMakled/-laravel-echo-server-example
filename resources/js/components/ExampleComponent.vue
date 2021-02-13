<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-md-8">
        <div class="card">
          <div class="card-header">Socket.io Component</div>

          <div class="card-body">Open the console.</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    window.Echo.channel("messages").listen(".UserEvent", function (data) {
      console.log(data);
    });
  },
};
</script>
