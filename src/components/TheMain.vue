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
          <button  @click="showDialog" class="btn btn-add" id="btnAdd">
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
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">NV00001</td>
              <td class="number-left-name">NGUYỄN MINH HẢI</td>
              <td class="number-marin">0354534566</td>
              <td class="number-left">Tổ Toán - Tin</td>
              <td class="number-left">Toán</td>
              <td class="number-left">Phòng tin học</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
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
</template>
<script>
import axios from "axios"
export default {
    name:"TheMain",
    methods: {

    created(){
          //thực hiện load dữ liệu
            this.loadData();
        },
    /** 
  * Hàm mở Dialog
  * Author: TVHieu - MF1485 (15/12/2022)
  */
    showDialog() {
      try {
        document.querySelector(".dialog").style.display = "flex";
      } catch (error) {
        console.log("error");
      }
    },

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
                //Gán dữ liệu
                //Hiển thị lỗi nếu có
            },
  },
};
</script>
<style scoped>
@import url(../css/layout/page.css);
</style>