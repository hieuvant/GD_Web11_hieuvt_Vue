<template>
    <!--Thông tin chi tiết giảng viên-->
    <div id="popup-teacher-detail" class="dialog">
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
                                            <button @click="onCloseDetail" class="btn-dialog-close" id="btn-close">
                                            </button>
                                        </div>
                                        <div class="dialog_container">
                                            <div class="dialog_container-left">
                                                <div class="stt-dialog">
                                                    <div for="txtTeacherCode" class="text-stt-dialog">Mã
                                                        số hiệu
                                                        cán bộ </div>
                                                    <div class="color-text-dialog">*</div>
                                                    <div class="dialog-el">
                                                        <input 
                                                         v-model="newTeacher.EmployeeCode"
                                                         v-bind:class="{'input--error':errors.EmployeeCode}"
                                                         @blur="validate()" 
                                                         field-label="Số hiệu cán bộ"
                                                         ref="txtTeacherCode"
                                                         type="text" 
                                                         class="input-stt-dialog-left">
                                                         <!-- Thêm class input--error nếu errors.EmployeeCode có dữ liệu -->
                                                         <div class="error-text" v-if="errors.EmployeeCode">
                                                         {{ errors.EmployeeCode }}
                                                         </div>
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
                                                    <div for="txtTeacherName" class="text-name-dialog">Họ
                                                        và tên
                                                    </div>
                                                    <div class="color-text-dialog">*</div>
                                                    <div class="dialog-el">
                                                        <input
                                                        id="txtTeacherName" 
                                                        v-model="newTeacher.FullName" 
                                                        v-bind:class="{'input--error':errors.FullName}" 
                                                        @blur="validate()" 
                                                        field-label="Họ và tên" 
                                                        type="text" 
                                                        class="input-name-dialog-right">
                                                        <!-- Thêm class input--error nếu errors.FullName có dữ liệu -->
                                                        <div class="error-text" v-if="errors.FullName">
                                                        {{ errors.FullName }}
                                                        </div>
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
                                            <button  
                                            id="btn-close-form-detail"
                                            @click="onCloseDetail" 
                                            class="btn-close">Đóng
                                            </button>
                                            <button 
                                            id="btn-Save" 
                                            @click="btnSaveOnClick"
                                            class="btn btn-dialog-add">Lưu</button>
                                        </div>
                                    </div>
                                </div>
                            </div>
</template>
<script>
import axios from 'axios';
export default {
    name:"TheDialog",
    props:["teacherId"],
    data(){
            return{
                errors:{
                   EmployeeCode:'',
                   FullName:'',
                },
                newTeacher:{
                   EmployeeCode:'',
                   FullName:'',
                }
            }
        },
        created(){
            let teacherId = this.teacherId;
            if(teacherId){
                this.getTeacherId(teacherId);
            }
        },
    methods: {
        /**
             * Validate dữ liệu
             * author : TVHieu - MF1485
             */
             validate(){
                let isValid = true;
                //Set lại giá trị khi đã validate hoặc đã fill data
                this.errors = {
                    EmployeeCode:'',
                    FullName:'',
                }
                if(!this.newTeacher.EmployeeCode){
                    this.errors.EmployeeCode = "Số hiệu cán bộ không được để trống";
                    isValid = false
                }
                if(!this.newTeacher.FullName){
                    this.errors.FullName = "Họ tên cán bộ không được để trống";
                    isValid = false
                }
                return isValid;
            },

             /**
             * Lưu dữ liệu và Thêm mới
             * author : TVHieu - MF1485
             */
            btnSaveOnClick(){
                try{
                    //Validate data
                    if(this.validate()){
                        if(this.newTeacher.EmployeeId){
                            axios.put(`https://cukcuk.manhnv.net/api/v1/Employees/${this.newTeacher.EmployeeId}`,this.newTeacher)
                                .then((res) => {
                                    console.log(res.data);
                                    alert("Thành công");
                                })
                                .catch((error)=>{
                                    console.log(error);
                                })
                        }
                        else{
                            axios.post("https://cukcuk.manhnv.net/api/v1/Employees",this.newTeacher)
                                .then((res) => {
                                    console.log(res.data);
                                    alert("Thành công");
                                })
                                .catch((error)=>{
                                    console.log(error);
                                })
                            return;
                        }
                    }
                }
                catch(e){
                    console.log(e);
                }
            },

            /**
             * Đóng form Thêm mới
             */

            onCloseDetail(){
                try{
                    this.$emit("onClose");
                }
                catch(e){
                    console.log(e);
                }
            },

            /**
             * Lấy id của giáo viên cần sửa
             * 
             */
            getTeacherId(teacherId){
                axios.get(`https://cukcuk.manhnv.net/api/v1/Employees/${teacherId}`)
                    .then((res) => {
                        this.newTeacher = res.data
                    })
                    .catch((error) => {
                        console.log(error);
                    })
            },
  },
};
</script>
<style scoped>
@import url(../css/base/dialog.css);
</style>