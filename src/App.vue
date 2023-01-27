<script setup>
import { ref } from "vue";

const stuid = ref("");
const stuName = ref("");
const stulName = ref("");
const checkedName = ref([]);
const requid = ref("");



</script>

<template>
  <h1>แบบฟอร์มลาออก</h1>
  <br />
  <form >
    วันที่ <input type="date" name="" />
    คณะ
    <select name="" id="">
      <option>กรุณาเลือกคณะ</option>
      <option>บริหาร</option>
      <option>ท่องเที่ยว</option>
      <option>ศิลปศาสตร์</option>
      <option>วิทยาศาสตร์</option></select
    ><br />

    <table>
      <tr>
        <td><label for=""> คำนำหน้า </label></td>
        <td>
          <select name="" id="">
            <option value="">นาย</option>
            <option value="">นาง</option>
            <option value="">นางสาว</option>
          </select>
        </td>
      </tr>
      <tr>
        <td><label for=""> ชื่อ </label></td>
        <td>
          <input
            type="text"
            name="stuName"
            id=""
            v-model="stuName"
            maxlength="20"
            required
          /><br />
        </td>
      </tr>
      <tr>
        <td><label for=""> นามสกุล </label></td>
        <td>
          <input
            type="text"
            name="stufName"
            id=""
            v-model="stulName"
            maxlength="20"
            required
          />
        </td>
      </tr>
      <tr>
        <td><label for=""> รหัสนักศึกษา </label></td>
        <td><input type="text" name="stuid" id="" v-model="stuid" required /></td>
      </tr>
      <tr>
        <td><label for=""> หมายเลขโทรศัพท์ </label></td>
        <td><input type="" name="" id="" /></td>
      </tr>

      <tr>
        <td><label for=""> หลักสูตร : </label></td>
        <td>
          <div>
            <input type="checkbox" id="full" value="Full" v-model="checkedName" />
            <label for="full"> 4-5 ปี </label>
            <input type="checkbox" id="compare" value="Compare" v-model="checkedName" />
            <label for="compare"> 4 ปีเที่ยบเข้าเรียน (2ปี) </label> <br />
            <input type="checkbox" id="normal" value="Normal" v-model="checkedName" />
            <label for="normal"> ภาคปกติ </label>
            <input
              type="checkbox"
              id="contribution"
              value="Contribution"
              v-model="checkedName"
            />
            <label for="contribution"> ภาคสมทบ </label>
          </div>
        </td>
      </tr>
      <tr>
        <td><label for=""> สาขาวิชา </label></td>
        <td>
          <select name="" id="">
            <option>กรุณาเลือกสาขา</option>
            <option>วิทยาการคอมพิวเตอร์</option>
            <option>เคมี</option>
            <option>เทคโนโลยีดิจิทัล</option>
            <option>คณิตศาสตร์</option>
          </select>
        </td>
      </tr>
      <tr>
        <td><label for=""> คณะ </label></td>
        <td>
          <select name="" id="">
            <option>กรุณาเลือกคณะ</option>
            <option>บริหาร</option>
            <option>ท่องเที่ยว</option>
            <option>ศิลปศาสตร์</option>
            <option>วิทยาศาสตร์</option>
          </select>
        </td>
      </tr>
      <tr>
        <td><label for=""> เหตุผลการลาออก </label></td>
        <td>
          <textarea
            name="requid"
            id="requid"
            v-model="requid"
            cols="22"
            rows="7"
          ></textarea>
        </td>
      </tr>
    </table>

    <input type="checkbox" id="full" value="Full" required />
    <label for=""> ยืนยันการส่งคำร้องลาออก</label> <br />

    
    <input type="submit" v-on:click="getDate()"/>
    {{ stuName }}{{ stuid }}{{ requid }}
  </form>
</template>


 


