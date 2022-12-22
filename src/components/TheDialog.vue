<template>
    <div v-show="showDialog" id="dialog-teacher-detail" class="dialog" style="display: block;">
                                <div class="dialog-weapper">
                                    <div class="dialog-sidebar">
                                        <div class="dialog-avt">
                                            <div class="img-avt">
                                            </div>
                                            <button class="btn-upload-avt">
                                                Chọn ảnh
                                            </button>
                                        </div>
                                        <div class="dialog-text-name">
                                            <div class="dialog-name">
                                                Họ và Tên
                                            </div>
                                            <div class="dialog-stt">
                                                Số hiệu cán bộ
                                            </div>
                                        </div>
                                    </div>
                                    <div class="space-left"></div>
                                    <div class="dialog-form-right">
                                        <div class="dialog_header">
                                            <div class="dialog-text-header">Thêm
                                                hồ sơ Cán
                                                bộ, giáo viên</div>
                                            <button @click="closeDialog" class="btn-dialog-close" id="btnDialogClose">
                                            </button>
                                        </div>
                                        <div class="dialog_container">
                                            <div class="dialog_container-left">
                                                <div class="stt-dialog">
                                                    <div class="text-stt-dialog">Mã
                                                        số hiệu
                                                        cán bộ </div>
                                                    <div class="color-text-dialog">*</div>
                                                    <div class="dialog-el-2">
                                                        <input id="txtEmployeeCode" type="text" class="input-stt-dialog-left">
                                                    </div>
                                                </div>
                                                <div class="phone-dialog">
                                                    <div class="text-phone-dialog">Số
                                                        điện
                                                        thoại</div>
                                                    <input id="txtEmployeeMobie" type="text" class="input-phone-dialog-left">
                                                </div>
                                                <div class="dropdownlist-dialog-left">
                                                    <div class="text-tbm-dialog">Tổ
                                                        bộ môn
                                                    </div>
                                                    <div class="combobox-dialog-left">
                                                        <input type="text" class="combobox-input-dialog-left">
                                                        <button id="combobox__btn-left" class="combobox__button-left"></button>
                                                        <div id="cbx-dialog-left__data" class="combobox-dialog-left__data">
                                                            <div class="data-item">Tổ
                                                                Toán-Tin</div>
                                                            <div class="data-item">Tổ
                                                                Lý-Hóa</div>
                                                            <div class="data-item">Tổ
                                                                Sinh-Sử-Địa</div>
                                                            <div class="data-item">Tổ
                                                                Anh
                                                                văn</div>
                                                            <div class="data-item">Tổ
                                                                Ngữ
                                                                Văn</div>
                                                            <div class="data-item">Tổ
                                                                Văn
                                                                Phòng</div>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                            <div class="dialog_container-right">
                                                <div class="name-dialog">
                                                    <div class="text-name-dialog">Họ
                                                        và tên
                                                    </div>
                                                    <div class="color-text-dialog">*</div>
                                                    <div class="dialog-el-0">
                                                        <input type="text" id="txtEmployeeName" class="input-name-dialog-right">
                                                    </div>
                                                </div>
                                                <div class="email-dialog">
                                                    <div class="text-email-dialog">Email</div>
                                                    <input type="text" id="txtEmployeeEmail" class="input-email-dialog-right">
                                                </div>
                                                <div class="dropdownlist-dialog-right">
                                                    <div class="text-qlm-dialog">QL
                                                        theo môn
                                                    </div>
                                                    <div class="combobox-dialog-right">
                                                        <input type="text" class="combobox-input-dialog-right">
                                                        <button id="combobox__btn-right" class="combobox__button-right"></button>
                                                        <div id="cbx-dialog-right__data" class="combobox-dialog-right__data">
                                                            <div class="data-item">Tổ
                                                                Toán-Tin</div>
                                                            <div class="data-item">Tổ
                                                                Lý-Hóa</div>
                                                            <div class="data-item">Tổ
                                                                Sinh-Sử-Địa</div>
                                                            <div class="data-item">Tổ
                                                                Anh
                                                                văn</div>
                                                            <div class="data-item">Tổ
                                                                Ngữ
                                                                Văn</div>
                                                            <div class="data-item">Tổ
                                                                Văn
                                                                Phòng</div>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="dialog_container-bottom">
                                            <div class="dropdownlist-dialog-bottom">
                                                <div class="text-qlk-dialog">QL
                                                    kho,
                                                    phòng
                                                </div>
                                                <div class="combobox-dialog-bottom">
                                                    <input type="text" class="combobox-input-dialog-bottom">
                                                    <button id="combobox__btn-bottom" class="combobox__button-bottom"></button>
                                                    <div id="cbx-dialog-bottom" class="combobox-dialog-bottom__data">
                                                        <div class="data-item">Tổ
                                                            Toán-Tin</div>
                                                        <div class="data-item">Tổ
                                                            Lý-Hóa</div>
                                                        <div class="data-item">Tổ
                                                            Sinh-Sử-Địa</div>
                                                        <div class="data-item">Tổ
                                                            Anh
                                                            văn</div>
                                                        <div class="data-item">Tổ
                                                            Ngữ
                                                            Văn</div>
                                                        <div class="data-item">Tổ
                                                            Văn
                                                            Phòng</div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="checkbox-dialog">
                                            <div class="ckb-item">
                                                <input type="checkbox" class="ckb-dialog">
                                                <div class="text-ckb">Trình độ
                                                    nghiệp vụ QLTB</div>
                                            </div>
                                            <div class="ckb-item">
                                                <input type="checkbox" class="ckb-dialog">
                                                <div class="text-ckb">Đang làm
                                                    việc</div>
                                            </div>
                                        </div>
                                        <div class="dialog_footer">
                                            <button @click="closeDialog" class="btn-close">Đóng
                                            </button>
                                            <button id="btnSave" class="btn
                                                btn-dialog-add">Lưu</button>
                                        </div>
                                    </div>
                                </div>
                                <!-- <div id="toastMsg" class="toast-message-container">
                                    <div class="toast-message">
                                      <div class="toast-message-left">
                                        <div class="toast-message-img"></div>
                                        <div class="toast-message-text">
                                          <div class="toast-message-title">Lỗi</div>
                                          <div class="toast-message-content"></div>
                                        </div>
                                      </div>
                                      <div id="toastMsgClose" class="toast-message-close"></div>
                                    </div>
                                  </div> -->
                                  <!-- <div id="toastMsgSucces" class="toast-message-container">
                                    <div class="toast-message">
                                      <div class="toast-message-left">
                                        <div class="toast-message-img-succes"></div>
                                        <div class="toast-message-text">
                                          <div class="toast-message-title">Thành Công</div>
                                        </div>
                                      </div>
                                      <div id="toastMsgSuccesClose" class="toast-message-close"></div>
                                    </div>
                                  </div> -->
                            </div>
</template>
<script>
export default {
    name:"TheDialog",
    methods: {
    /** 
  * Hàm đóng Dialog
  * Author: TVHieu - MF1485 (15/12/2022)
  */
    closeDialog() {
      try {
        document.querySelector(".dialog").style.display = "none";
      } catch (error) {
        console.log("error");
      }
    },
  },
};
</script>
<style scoped>
@import url(../css/base/dialog.css);
</style>