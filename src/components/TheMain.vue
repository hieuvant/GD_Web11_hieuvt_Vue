<template>
  <div class="main">
    <div class="page-header">
      <div class="page-header-left">
        <div class="input-header">
          <input type="text" class="input-search" />
        </div>
      </div>
      <div class="page-header-right">
        <div class="page-button">
          <button  @click="btnAddOnClick" class="btn btn-add" id="btn-add">
            Thêm</button
          ><button class="btn-output">Xuất Khẩu</button
          ><button
            class="btn-more-op"
          ></button>
        </div>
      </div>
    </div>
    <div class="page-body">
      <div class="tb-paging">
        <table id="tb-employee-list">
          <thead>
            <tr>
              <th class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </th>
              <th>Số hiệu cán bộ</th>
              <th>Họ và tên</th>
              <th>Số điện thoại</th>
              <th>Tổ chuyên môn</th>
              <th>QL theo môn</th>
              <th>QL kho, phòng</th>
              <th>Đào tạo QLTB</th>
              <th>Đang làm việc</th>
              <th></th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(item,index) in employees" :key="index">
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">{{item.EmployeeCode}}</td>
              <td class="number-left-name">{{item.FullName}}</td>
              <td class="number-marin">{{item.PhoneNumber}}</td>
              <td class="number-left">Tổ Toán - Tin</td>
              <td class="number-left">Toán</td>
              <td class="number-left">Phòng tin học</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit" alt="" tabindex="0" @click="editData(item.EmployeeId)"></button
                ><button class="btn-remove" alt="" tabindex="0" @click="deleteData(item.EmployeeId)"></button>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
      <div class="paging">
        <button class="btn-paging-movetofirt"></button
        ><button class="btn-paging-pre"></button>
        <div class="paging-number">
          <input type="text" placeholder="1" class="input-number" />
        </div>
        <button class="btn-paging-next"></button
        ><button class="btn-paging-movetolast"></button>
        <div class="paging-text">1/2 trang</div>
        <div class="paging-text-total">(56 giáo viên)</div>
      </div>
    </div>
  </div>
  <TheDialog v-if="showDetail" :teacherId="teacherIdSelected" @onClose="onCloseDetail"></TheDialog>
</template>
<script>
import TheDialog from "@/components/TheDialog.vue";
import axios from "axios";
export default {
    name:"TheMain",
    components:{
            TheDialog
        },
        created(){
            //thực hiện load dữ liệu
            this.loadData();
        },
    methods: {

    /** 
  * Hàm load dữ liệu
  * Author: TVHieu - MF1485 (22/12/2022)
  */
             loadData(){
                //Gọi API:
                axios.get("https://cukcuk.manhnv.net/api/v1/employees")
                    .then(res=>{
                        this.employees = res.data;
                    })
                    .catch(error=>{
                        console.log(error);
                    })
            },
            /**
            * Hiển form thêm mới dữ liệu
            * Author : TVHieu - MF1485
            */
            btnAddOnClick(){
                try{
                    this.showDetail = true;
                }
                catch(e){
                    console.log(e);
                }
            }, 
            /**
            * Đóng form thêm mới dữ liệu
            * Author : TVHieu - MF1485
            */
            onCloseDetail(){
                try{
                    this.showDetail = false;
                    //Load lại dữ liệu
                    this.loadData()
                }
                catch(e){
                    console.log(e);
                }
            },
            /**
             * Edit data
             * 
             */
             editData(id){
                try{
                    this.teacherIdSelected = id;
                    console.log("Edit item : ",this.teacherIdSelected);
                    this.showDetail = true;
                }
                catch(e){
                    console.log(e);
                }
            },
            /**
             * Delete Data 
             * author : TVHieu - MF1485 (24/12/2022)
             */
            deleteData(id){
                try{
                    axios.delete('https://cukcuk.manhnv.net/api/v1/employees/'+id)
                        .then(() => this.loadData())
                }
                catch(e){
                    console.log(e);
                }
            },
  },
        data(){
            return{
                employees:[],
                showDetail:false,
                teacherIdSelected: {},
            }
        }
};
</script>
<style scoped>
@import url(../css/layout/page.css);
</style>