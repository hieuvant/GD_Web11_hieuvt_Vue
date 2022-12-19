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
            style="background-position: -628px -972px"
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
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">NV1234</td>
              <td class="number-left-name">Test1</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv5591122333</td>
              <td class="number-left-name">Mai Sơn Trà</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng sản xuất</td>
              <td class="number-left">Phòng sản xuất</td>
              <td class="number-left">Phòng sản xuất</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv559901674421</td>
              <td class="number-left-name">Hồ Văn ANh</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv55990167442</td>
              <td class="number-left-name">tryng</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv5599057441</td>
              <td class="number-left-name">Hồ Văn ANh</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv559</td>
              <td class="number-left-name">Mạnh Nguyễn A</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng đào tạo</td>
              <td class="number-left">Phòng đào tạo</td>
              <td class="number-left">Phòng đào tạo</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv559905744544</td>
              <td class="number-left-name">Nam đế</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv55990167447</td>
              <td class="number-left-name">Nam dương</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv5599057447</td>
              <td class="number-left-name">Quách Tĩnh</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv559905744</td>
              <td class="number-left-name">Dương Khang</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng đào tạo</td>
              <td class="number-left">Phòng đào tạo</td>
              <td class="number-left">Phòng đào tạo</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv4811</td>
              <td class="number-left-name">Mạnh Nguyễn</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv38947388</td>
              <td class="number-left-name">Mai Sơn Trà</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv88374984</td>
              <td class="number-left-name">Đào Dương</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng sản xuất</td>
              <td class="number-left">Phòng sản xuất</td>
              <td class="number-left">Phòng sản xuất</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv6600</td>
              <td class="number-left-name">to van tai</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv076393</td>
              <td class="number-left-name">Nguyen ngoc</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv55990265444762</td>
              <td class="number-left-name">nam abc</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv5599016744277</td>
              <td class="number-left-name">Nguyen quang manh</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">NV22012000</td>
              <td class="number-left-name">Mai Sơn Trà 2345</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng đào tạo</td>
              <td class="number-left">Phòng đào tạo</td>
              <td class="number-left">Phòng đào tạo</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nvaung1</td>
              <td class="number-left-name">nvaung</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv0393113</td>
              <td class="number-left-name">nvaung</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv267</td>
              <td class="number-left-name">to van tai</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv9956</td>
              <td class="number-left-name">ádasasdas</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-left">Phòng tuyển sinh</td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin"><div class="table-checklist"></div></td>
              <td class="number-marin">
                <button class="btn-edit"></button
                ><button class="btn-remove"></button>
              </td>
            </tr>
            <tr>
              <td class="number-marin">
                <input type="checkbox" class="checkbox-table" />
              </td>
              <td class="number-marin">nv55990265444761</td>
              <td class="number-left-name">Loằng tà loằng ngoằng</td>
              <td class="number-marin"></td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
              <td class="number-left">Phòng nhân sự</td>
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
export default {
    name:"TheMain",
    methods: {
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
  },
};
</script>
<style scoped>
@import url(../css/layout/page.css);
</style>