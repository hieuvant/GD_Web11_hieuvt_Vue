<template>
  <div id="mySidebar" class="sidebar">
    <div class="sidebar-item-home">
      <div class="sidebar-item-home-left">
        <div
          class="icon-sidebar-home"
        ></div>
        <div class="sidebar-item-text-home">Thiết bị</div>
      </div>
      <div
        class="icofont-justify-all"
        href="javascript:void(0)"
        onclick="closeNav()"
      ></div>
    </div>
    <div class="sidebar-item-body">
      <div class="sidebar-item">
        <div
          class="icon-sidebar icon1"
        ></div>
        <div class="sidebar-item-text">Tổng quan</div>
      </div>
      <div class="sidebar-item">
        <div
          class="icon-sidebar icon2"
        ></div>
        <div class="sidebar-item-text">Thiết bị</div>
      </div>
      <div class="sidebar-item">
        <div
          class="icon-sidebar icon3"
        ></div>
        <div class="sidebar-item-text">Mượn trả</div>
      </div>
      <div class="sidebar-item">
        <div
          class="icon-sidebar icon4"
        ></div>
        <div class="sidebar-item-text">Báo cáo</div>
      </div>
      <div class="sidebar-item">
        <div
          class="icon-sidebar icon5"
        ></div>
        <div class="sidebar-item-text">Hệ thống</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
    name:"TheSidebar"
};
</script>
<style scoped>
@import url(../css/layout/sidebar.css);
</style>