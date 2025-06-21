<template>
  <div class="addEdit-block">
    <el-form
      class="detail-form-content"
      ref="ruleForm"
      :model="ruleForm"
      :rules="rules"
      label-width="80px"
	  :style="{backgroundColor:addEditForm.addEditBoxColor}"
    >
      <el-row>
                        <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="理论" prop="lilun">
          <el-input v-model="ruleForm.lilun" 
              placeholder="理论" clearable  :readonly="ro.lilun"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="理论" prop="lilun">
              <el-input v-model="ruleForm.lilun" 
                placeholder="理论" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
                                    <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="实验" prop="shiyan">
          <el-input v-model="ruleForm.shiyan" 
              placeholder="实验" clearable  :readonly="ro.shiyan"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="实验" prop="shiyan">
              <el-input v-model="ruleForm.shiyan" 
                placeholder="实验" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
                                                                  <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="课程系数" prop="kechengxishu">
          <el-input v-model="ruleForm.kechengxishu" 
              placeholder="课程系数" clearable  :readonly="ro.kechengxishu"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="课程系数" prop="kechengxishu">
              <el-input v-model="ruleForm.kechengxishu" 
                placeholder="课程系数" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
                                    <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="合班数量" prop="hebanshuliang">
          <el-input v-model="ruleForm.hebanshuliang" 
              placeholder="合班数量" clearable  :readonly="ro.hebanshuliang"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="合班数量" prop="hebanshuliang">
              <el-input v-model="ruleForm.hebanshuliang" 
                placeholder="合班数量" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
                                    <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="合班系数" prop="hebanxishu">
          <el-input v-model="ruleForm.hebanxishu" 
              placeholder="合班系数" clearable  :readonly="ro.hebanxishu"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="合班系数" prop="hebanxishu">
              <el-input v-model="ruleForm.hebanxishu" 
                placeholder="合班系数" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
                                    <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="作业增量系数" prop="zuoyezengliangxishu">
          <el-input v-model="ruleForm.zuoyezengliangxishu" 
              placeholder="作业增量系数" clearable  :readonly="ro.zuoyezengliangxishu"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="作业增量系数" prop="zuoyezengliangxishu">
              <el-input v-model="ruleForm.zuoyezengliangxishu" 
                placeholder="作业增量系数" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
                                    <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="作业增量" prop="zuoyezengliang">
          <el-input v-model="ruleForm.zuoyezengliang" 
              placeholder="作业增量" clearable  :readonly="ro.zuoyezengliang"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="作业增量" prop="zuoyezengliang">
              <el-input v-model="ruleForm.zuoyezengliang" 
                placeholder="作业增量" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
                                    <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="实验类型系数" prop="shiyanleixingxishu">
          <el-input v-model="ruleForm.shiyanleixingxishu" 
              placeholder="实验类型系数" clearable  :readonly="ro.shiyanleixingxishu"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="实验类型系数" prop="shiyanleixingxishu">
              <el-input v-model="ruleForm.shiyanleixingxishu" 
                placeholder="实验类型系数" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
                                    <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="实习调整系数" prop="shixidiaozhengxishu">
          <el-input v-model="ruleForm.shixidiaozhengxishu" 
              placeholder="实习调整系数" clearable  :readonly="ro.shixidiaozhengxishu"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="实习调整系数" prop="shixidiaozhengxishu">
              <el-input v-model="ruleForm.shixidiaozhengxishu" 
                placeholder="实习调整系数" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
                                    <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="当量学时" prop="dangliangxueshi">
          <el-input v-model="ruleForm.dangliangxueshi" 
              placeholder="当量学时" clearable  :readonly="ro.dangliangxueshi"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="当量学时" prop="dangliangxueshi">
              <el-input v-model="ruleForm.dangliangxueshi" 
                placeholder="当量学时" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
                                                                  <el-col :span="12">
        <el-form-item class="select" v-if="type!='info'" label="教师工号" prop="jiaoshigonghao">
          <el-select  @change="jiaoshigonghaoChange" v-model="ruleForm.jiaoshigonghao" placeholder="请选择教师工号">
            <el-option
                v-for="(item,index) in jiaoshigonghaoOptions"
                v-bind:key="index"
                :label="item"
                :value="item">
            </el-option>
          </el-select>
        </el-form-item>
        <div v-else>
          <el-form-item class="input"v-if="ruleForm.jiaoshigonghao" label="教师工号" prop="jiaoshigonghao">
              <el-input v-model="ruleForm.jiaoshigonghao" 
                placeholder="教师工号" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
                                    <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="教师姓名" prop="jiaoshixingming">
          <el-input v-model="ruleForm.jiaoshixingming" 
              placeholder="教师姓名" clearable  :readonly="ro.jiaoshixingming"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="教师姓名" prop="jiaoshixingming">
              <el-input v-model="ruleForm.jiaoshixingming" 
                placeholder="教师姓名" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
                                    <el-col :span="12">
        <el-form-item class="date" v-if="type!='info'" label="提交时间" prop="tijiaoshijian">
            <el-date-picker
                format="yyyy 年 MM 月 dd 日"
                value-format="yyyy-MM-dd"
                v-model="ruleForm.tijiaoshijian" 
                type="date"
                placeholder="提交时间">
            </el-date-picker> 
        </el-form-item>
        <div v-else>
          <el-form-item class="input" v-if="ruleForm.tijiaoshijian" label="提交时间" prop="tijiaoshijian">
              <el-input v-model="ruleForm.tijiaoshijian" 
                placeholder="提交时间" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
                              </el-row>
                                                    <el-row>
            <el-col :span="24">
              <el-form-item class="textarea" v-if="type!='info'" label="实习" prop="shixi">
                <el-input
                  style="min-width: 200px; max-width: 600px;"
                  type="textarea"
                  :rows="8"
                  placeholder="实习"
                  v-model="ruleForm.shixi" >
                </el-input>
              </el-form-item>
              <div v-else>
                <el-form-item v-if="ruleForm.shixi" label="实习" prop="shixi">
                    <span>{{ruleForm.shixi}}</span>
                </el-form-item>
              </div>
            </el-col>
          </el-row>
                                                                                                                                                <el-row>
            <el-col :span="24">
              <el-form-item class="textarea" v-if="type!='info'" label="备注" prop="beizhu">
                <el-input
                  style="min-width: 200px; max-width: 600px;"
                  type="textarea"
                  :rows="8"
                  placeholder="备注"
                  v-model="ruleForm.beizhu" >
                </el-input>
              </el-form-item>
              <div v-else>
                <el-form-item v-if="ruleForm.beizhu" label="备注" prop="beizhu">
                    <span>{{ruleForm.beizhu}}</span>
                </el-form-item>
              </div>
            </el-col>
          </el-row>
                                                                                                                                                                                                                                                                                      <el-form-item class="btn">
                <el-button v-if="type!='info'" type="primary" class="btn-success" @click="onSubmit">提交</el-button>
        <el-button v-if="type!='info'" class="btn-close" @click="back()">取消</el-button>
        <el-button v-if="type=='info'" class="btn-close" @click="back()">返回</el-button>
      </el-form-item>
    </el-form>
    
    
  </div>
</template>
<script>
// 数字，邮件，手机，url，身份证校验
import { isNumber,isIntNumer,isEmail,isPhone, isMobile,isURL,checkIdCard } from "@/utils/validate";
export default {
  data() {
    let self = this
    var validateIdCard = (rule, value, callback) => {
      if(!value){
        callback();
      } else if (!checkIdCard(value)) {
        callback(new Error("请输入正确的身份证号码"));
      } else {
        callback();
      }
    };
    var validateUrl = (rule, value, callback) => {
      if(!value){
        callback();
      } else if (!isURL(value)) {
        callback(new Error("请输入正确的URL地址"));
      } else {
        callback();
      }
    };
    var validateMobile = (rule, value, callback) => {
      if(!value){
        callback();
      } else if (!isMobile(value)) {
        callback(new Error("请输入正确的手机号码"));
      } else {
        callback();
      }
    };
    var validatePhone = (rule, value, callback) => {
      if(!value){
        callback();
      } else if (!isPhone(value)) {
        callback(new Error("请输入正确的电话号码"));
      } else {
        callback();
      }
    };
    var validateEmail = (rule, value, callback) => {
      if(!value){
        callback();
      } else if (!isEmail(value)) {
        callback(new Error("请输入正确的邮箱地址"));
      } else {
        callback();
      }
    };
    var validateNumber = (rule, value, callback) => {
      if(!value){
        callback();
      } else if (!isNumber(value)) {
        callback(new Error("请输入数字"));
      } else {
        callback();
      }
    };
    var validateIntNumber = (rule, value, callback) => {
      if(!value){
        callback();
      } else if (!isIntNumer(value)) {
        callback(new Error("请输入整数"));
      } else {
        callback();
      }
    };
    return {
	  addEditForm: {"btnSaveFontColor":"#fff","selectFontSize":"14px","btnCancelBorderColor":"#DCDFE6","inputBorderRadius":"4px","inputFontSize":"14px","textareaBgColor":"#fff","btnSaveFontSize":"14px","textareaBorderRadius":"4px","uploadBgColor":"#fff","textareaBorderStyle":"solid","btnCancelWidth":"88px","textareaHeight":"120px","dateBgColor":"#fff","btnSaveBorderRadius":"4px","uploadLableFontSize":"14px","textareaBorderWidth":"1px","inputLableColor":"#606266","addEditBoxColor":"rgba(251, 249, 249, 1)","dateIconFontSize":"14px","btnSaveBgColor":"#409EFF","uploadIconFontColor":"#8c939d","textareaBorderColor":"#DCDFE6","btnCancelBgColor":"#ecf5ff","selectLableColor":"#606266","btnSaveBorderStyle":"solid","dateBorderWidth":"1px","dateLableFontSize":"14px","dateBorderRadius":"4px","btnCancelBorderStyle":"solid","selectLableFontSize":"14px","selectBorderStyle":"solid","selectIconFontColor":"#C0C4CC","btnCancelHeight":"44px","inputHeight":"40px","btnCancelFontColor":"#606266","dateBorderColor":"#DCDFE6","dateIconFontColor":"#C0C4CC","uploadBorderStyle":"solid","dateBorderStyle":"solid","dateLableColor":"#606266","dateFontSize":"14px","inputBorderWidth":"1px","uploadIconFontSize":"28px","selectHeight":"40px","inputFontColor":"#606266","uploadHeight":"148px","textareaLableColor":"#606266","textareaLableFontSize":"14px","btnCancelFontSize":"14px","inputBorderStyle":"solid","btnCancelBorderRadius":"4px","inputBgColor":"#fff","inputLableFontSize":"14px","uploadLableColor":"#606266","uploadBorderRadius":"4px","btnSaveHeight":"44px","selectBgColor":"#fff","btnSaveWidth":"88px","selectIconFontSize":"14px","dateHeight":"40px","selectBorderColor":"#DCDFE6","inputBorderColor":"#DCDFE6","uploadBorderColor":"#DCDFE6","textareaFontColor":"#606266","selectBorderWidth":"1px","dateFontColor":"#606266","btnCancelBorderWidth":"1px","uploadBorderWidth":"1px","textareaFontSize":"14px","selectBorderRadius":"4px","selectFontColor":"#606266","btnSaveBorderColor":"#409EFF","btnSaveBorderWidth":"1px"},
      id: '',
      type: '',
      ro:{
	lilun : false,
	shiyan : false,
	shixi : false,
	kechengxishu : false,
	hebanshuliang : false,
	hebanxishu : false,
	zuoyezengliangxishu : false,
	zuoyezengliang : false,
	shiyanleixingxishu : false,
	shixidiaozhengxishu : false,
	dangliangxueshi : false,
	beizhu : false,
	jiaoshigonghao : false,
	jiaoshixingming : false,
	tijiaoshijian : false,
      },
            ruleForm: {
                	        lilun: '',
	                        	        shiyan: '',
	                        	        shixi: '',
	                        	        kechengxishu: '',
	                        	        hebanshuliang: '',
	                        	        hebanxishu: '',
	                        	        zuoyezengliangxishu: '',
	                        	        zuoyezengliang: '',
	                        	        shiyanleixingxishu: '',
	                        	        shixidiaozhengxishu: '',
	                        	        dangliangxueshi: '',
	                        	        beizhu: '',
	                        	        jiaoshigonghao: '',
	                        	        jiaoshixingming: '',
	                        	        tijiaoshijian: '',
	                      },
                                                                                                                                                                                                jiaoshigonghaoOptions: [],
                                                rules: {
                  lilun: [
                                    	                                                              ],
                  shiyan: [
                                    	                                                              ],
                  shixi: [
                                    	                                                              ],
                  kechengxishu: [
                                    	                                                              ],
                  hebanshuliang: [
                                    	                                                              ],
                  hebanxishu: [
                                    	                                                              ],
                  zuoyezengliangxishu: [
                                    	                                                              ],
                  zuoyezengliang: [
                                    	                                                              ],
                  shiyanleixingxishu: [
                                    	                                                              ],
                  shixidiaozhengxishu: [
                                    	                                                              ],
                  dangliangxueshi: [
                                    	                                                              ],
                  beizhu: [
                                    	                                                              ],
                  jiaoshigonghao: [
                                    	                                                              ],
                  jiaoshixingming: [
                                    	                                                              ],
                  tijiaoshijian: [
                                    	                                                              ],
              }
    };
  },
  props: ["parent"],
  computed: {
                                                                                                                                                                                          },
  created() {
	this.ruleForm.tijiaoshijian = this.getCurDate()
	this.addEditStyleChange()
	this.addEditUploadStyleChange()
  },
  methods: {
        // 下载
    download(file){
      window.open(`${file}`)
    },
    // 初始化
    init(id,type) {
      if (id) {
        this.id = id;
        this.type = type;
      }
      if(this.type=='info'||this.type=='else'){
        this.info(id);
      }else if(this.type=='cross'){
        var obj = this.$storage.getObj('crossObj');
        for (var o in obj){
          	            if(o=='lilun'){
            this.ruleForm.lilun = obj[o];
	    this.ro.lilun = true;
            continue;
          }
	            	            if(o=='shiyan'){
            this.ruleForm.shiyan = obj[o];
	    this.ro.shiyan = true;
            continue;
          }
	            	            if(o=='shixi'){
            this.ruleForm.shixi = obj[o];
	    this.ro.shixi = true;
            continue;
          }
	            	            if(o=='kechengxishu'){
            this.ruleForm.kechengxishu = obj[o];
	    this.ro.kechengxishu = true;
            continue;
          }
	            	            if(o=='hebanshuliang'){
            this.ruleForm.hebanshuliang = obj[o];
	    this.ro.hebanshuliang = true;
            continue;
          }
	            	            if(o=='hebanxishu'){
            this.ruleForm.hebanxishu = obj[o];
	    this.ro.hebanxishu = true;
            continue;
          }
	            	            if(o=='zuoyezengliangxishu'){
            this.ruleForm.zuoyezengliangxishu = obj[o];
	    this.ro.zuoyezengliangxishu = true;
            continue;
          }
	            	            if(o=='zuoyezengliang'){
            this.ruleForm.zuoyezengliang = obj[o];
	    this.ro.zuoyezengliang = true;
            continue;
          }
	            	            if(o=='shiyanleixingxishu'){
            this.ruleForm.shiyanleixingxishu = obj[o];
	    this.ro.shiyanleixingxishu = true;
            continue;
          }
	            	            if(o=='shixidiaozhengxishu'){
            this.ruleForm.shixidiaozhengxishu = obj[o];
	    this.ro.shixidiaozhengxishu = true;
            continue;
          }
	            	            if(o=='dangliangxueshi'){
            this.ruleForm.dangliangxueshi = obj[o];
	    this.ro.dangliangxueshi = true;
            continue;
          }
	            	            if(o=='beizhu'){
            this.ruleForm.beizhu = obj[o];
	    this.ro.beizhu = true;
            continue;
          }
	            	            if(o=='jiaoshigonghao'){
            this.ruleForm.jiaoshigonghao = obj[o];
	    this.ro.jiaoshigonghao = true;
            continue;
          }
	            	            if(o=='jiaoshixingming'){
            this.ruleForm.jiaoshixingming = obj[o];
	    this.ro.jiaoshixingming = true;
            continue;
          }
	            	            if(o=='tijiaoshijian'){
            this.ruleForm.tijiaoshijian = obj[o];
	    this.ro.tijiaoshijian = true;
            continue;
          }
	                    }
                                                                                                                                                                                                                                                              }
            // 获取用户信息
      this.$http({
        url: `${this.$storage.get('sessionTable')}/session`,
        method: "get"
      }).then(({ data }) => {
        if (data && data.code === 0) {
          var json = data.data;
                                                                                                                                                                                                                                                                                                                                                            } else {
          this.$message.error(data.msg);
        }
      });
                                                                                                                                                                                                                                                                  this.$http({
              url: `option/jiaoshi/jiaoshigonghao`,
              method: "get"
            }).then(({ data }) => {
              if (data && data.code === 0) {
                this.jiaoshigonghaoOptions = data.data;
              } else {
                this.$message.error(data.msg);
              }
            });
                                                                },
                                                                                                            // 下二随
    jiaoshigonghaoChange () {
      this.$http({
        url: `follow/jiaoshi/jiaoshigonghao?columnValue=`+ this.ruleForm.jiaoshigonghao,
        method: "get"
      }).then(({ data }) => {
        if (data && data.code === 0) {
                                                                                                                                                                                                                                                                                                                                  if(data.data.jiaoshixingming){
                this.ruleForm.jiaoshixingming = data.data.jiaoshixingming
              }
                                                    } else {
          this.$message.error(data.msg);
        }
      });
    },
                            // 多级联动参数
                                                                                                                                                                  info(id) {
      this.$http({
        url: `gongzuoliang/info/${id}`,
        method: "get"
      }).then(({ data }) => {
        if (data && data.code === 0) {
        this.ruleForm = data.data;
	//解决前台上传图片后台不显示的问题
	let reg=new RegExp('../../../upload','g')//g代表全部
        } else {
          this.$message.error(data.msg);
        }
      });
    },
        // 提交
    onSubmit() {
                  // ${column.compare}
                              // ${column.compare}
                              // ${column.compare}
                              // ${column.compare}
                              // ${column.compare}
                              // ${column.compare}
                              // ${column.compare}
                              // ${column.compare}
                              // ${column.compare}
                              // ${column.compare}
                              // ${column.compare}
                              // ${column.compare}
                              // ${column.compare}
                              // ${column.compare}
                              // ${column.compare}
                                                                                                                                                                                                                                                                                                                  this.$refs["ruleForm"].validate(valid => {
        if (valid) {
          this.$http({
            url: `gongzuoliang/${!this.ruleForm.id ? "save" : "update"}`,
            method: "post",
            data: this.ruleForm
          }).then(({ data }) => {
            if (data && data.code === 0) {
              this.$message({
                message: "操作成功",
                type: "success",
                duration: 1500,
                onClose: () => {
                  this.parent.showFlag = true;
                  this.parent.addOrUpdateFlag = false;
                  this.parent.gongzuoliangCrossAddOrUpdateFlag = false;
                  this.parent.search();
                  this.parent.contentStyleChange();
                }
              });
            } else {
              this.$message.error(data.msg);
            }
          });
        }
      });
    },
    // 获取uuid
    getUUID () {
      return new Date().getTime();
    },
    // 返回
    back() {
      this.parent.showFlag = true;
      this.parent.addOrUpdateFlag = false;
      this.parent.gongzuoliangCrossAddOrUpdateFlag = false;
      this.parent.contentStyleChange();
    },
                                                                                                                                                                                        	addEditStyleChange() {
	  this.$nextTick(()=>{
	    // input
	    document.querySelectorAll('.addEdit-block .input .el-input__inner').forEach(el=>{
	      el.style.height = this.addEditForm.inputHeight
	      el.style.color = this.addEditForm.inputFontColor
	      el.style.fontSize = this.addEditForm.inputFontSize
	      el.style.borderWidth = this.addEditForm.inputBorderWidth
	      el.style.borderStyle = this.addEditForm.inputBorderStyle
	      el.style.borderColor = this.addEditForm.inputBorderColor
	      el.style.borderRadius = this.addEditForm.inputBorderRadius
	      el.style.backgroundColor = this.addEditForm.inputBgColor
	    })
	    document.querySelectorAll('.addEdit-block .input .el-form-item__label').forEach(el=>{
	      el.style.lineHeight = this.addEditForm.inputHeight
	      el.style.color = this.addEditForm.inputLableColor
	      el.style.fontSize = this.addEditForm.inputLableFontSize
	    })
	    // select
	    document.querySelectorAll('.addEdit-block .select .el-input__inner').forEach(el=>{
	      el.style.height = this.addEditForm.selectHeight
	      el.style.color = this.addEditForm.selectFontColor
	      el.style.fontSize = this.addEditForm.selectFontSize
	      el.style.borderWidth = this.addEditForm.selectBorderWidth
	      el.style.borderStyle = this.addEditForm.selectBorderStyle
	      el.style.borderColor = this.addEditForm.selectBorderColor
	      el.style.borderRadius = this.addEditForm.selectBorderRadius
	      el.style.backgroundColor = this.addEditForm.selectBgColor
	    })
	    document.querySelectorAll('.addEdit-block .select .el-form-item__label').forEach(el=>{
	      el.style.lineHeight = this.addEditForm.selectHeight
	      el.style.color = this.addEditForm.selectLableColor
	      el.style.fontSize = this.addEditForm.selectLableFontSize
	    })
	    document.querySelectorAll('.addEdit-block .select .el-select__caret').forEach(el=>{
	      el.style.color = this.addEditForm.selectIconFontColor
	      el.style.fontSize = this.addEditForm.selectIconFontSize
	    })
	    // date
	    document.querySelectorAll('.addEdit-block .date .el-input__inner').forEach(el=>{
	      el.style.height = this.addEditForm.dateHeight
	      el.style.color = this.addEditForm.dateFontColor
	      el.style.fontSize = this.addEditForm.dateFontSize
	      el.style.borderWidth = this.addEditForm.dateBorderWidth
	      el.style.borderStyle = this.addEditForm.dateBorderStyle
	      el.style.borderColor = this.addEditForm.dateBorderColor
	      el.style.borderRadius = this.addEditForm.dateBorderRadius
	      el.style.backgroundColor = this.addEditForm.dateBgColor
	    })
	    document.querySelectorAll('.addEdit-block .date .el-form-item__label').forEach(el=>{
	      el.style.lineHeight = this.addEditForm.dateHeight
	      el.style.color = this.addEditForm.dateLableColor
	      el.style.fontSize = this.addEditForm.dateLableFontSize
	    })
	    document.querySelectorAll('.addEdit-block .date .el-input__icon').forEach(el=>{
	      el.style.color = this.addEditForm.dateIconFontColor
	      el.style.fontSize = this.addEditForm.dateIconFontSize
	      el.style.lineHeight = this.addEditForm.dateHeight
	    })
	    // upload
	    let iconLineHeight = parseInt(this.addEditForm.uploadHeight) - parseInt(this.addEditForm.uploadBorderWidth) * 2 + 'px'
	    document.querySelectorAll('.addEdit-block .upload .el-upload--picture-card').forEach(el=>{
	      el.style.width = this.addEditForm.uploadHeight
	      el.style.height = this.addEditForm.uploadHeight
	      el.style.borderWidth = this.addEditForm.uploadBorderWidth
	      el.style.borderStyle = this.addEditForm.uploadBorderStyle
	      el.style.borderColor = this.addEditForm.uploadBorderColor
	      el.style.borderRadius = this.addEditForm.uploadBorderRadius
	      el.style.backgroundColor = this.addEditForm.uploadBgColor
	    })
	    document.querySelectorAll('.addEdit-block .upload .el-form-item__label').forEach(el=>{
	      el.style.lineHeight = this.addEditForm.uploadHeight
	      el.style.color = this.addEditForm.uploadLableColor
	      el.style.fontSize = this.addEditForm.uploadLableFontSize
	    })
	    document.querySelectorAll('.addEdit-block .upload .el-icon-plus').forEach(el=>{
	      el.style.color = this.addEditForm.uploadIconFontColor
	      el.style.fontSize = this.addEditForm.uploadIconFontSize
	      el.style.lineHeight = iconLineHeight
	      el.style.display = 'block'
	    })
	    // 多文本输入框
	    document.querySelectorAll('.addEdit-block .textarea .el-textarea__inner').forEach(el=>{
	      el.style.height = this.addEditForm.textareaHeight
	      el.style.color = this.addEditForm.textareaFontColor
	      el.style.fontSize = this.addEditForm.textareaFontSize
	      el.style.borderWidth = this.addEditForm.textareaBorderWidth
	      el.style.borderStyle = this.addEditForm.textareaBorderStyle
	      el.style.borderColor = this.addEditForm.textareaBorderColor
	      el.style.borderRadius = this.addEditForm.textareaBorderRadius
	      el.style.backgroundColor = this.addEditForm.textareaBgColor
	    })
	    document.querySelectorAll('.addEdit-block .textarea .el-form-item__label').forEach(el=>{
	      // el.style.lineHeight = this.addEditForm.textareaHeight
	      el.style.color = this.addEditForm.textareaLableColor
	      el.style.fontSize = this.addEditForm.textareaLableFontSize
	    })
	    // 保存
	    document.querySelectorAll('.addEdit-block .btn .btn-success').forEach(el=>{
	      el.style.width = this.addEditForm.btnSaveWidth
	      el.style.height = this.addEditForm.btnSaveHeight
	      el.style.color = this.addEditForm.btnSaveFontColor
	      el.style.fontSize = this.addEditForm.btnSaveFontSize
	      el.style.borderWidth = this.addEditForm.btnSaveBorderWidth
	      el.style.borderStyle = this.addEditForm.btnSaveBorderStyle
	      el.style.borderColor = this.addEditForm.btnSaveBorderColor
	      el.style.borderRadius = this.addEditForm.btnSaveBorderRadius
	      el.style.backgroundColor = this.addEditForm.btnSaveBgColor
	    })
	    // 返回
	    document.querySelectorAll('.addEdit-block .btn .btn-close').forEach(el=>{
	      el.style.width = this.addEditForm.btnCancelWidth
	      el.style.height = this.addEditForm.btnCancelHeight
	      el.style.color = this.addEditForm.btnCancelFontColor
	      el.style.fontSize = this.addEditForm.btnCancelFontSize
	      el.style.borderWidth = this.addEditForm.btnCancelBorderWidth
	      el.style.borderStyle = this.addEditForm.btnCancelBorderStyle
	      el.style.borderColor = this.addEditForm.btnCancelBorderColor
	      el.style.borderRadius = this.addEditForm.btnCancelBorderRadius
	      el.style.backgroundColor = this.addEditForm.btnCancelBgColor
	    })
	  })
	},
	addEditUploadStyleChange() {
		this.$nextTick(()=>{
		  document.querySelectorAll('.addEdit-block .upload .el-upload-list--picture-card .el-upload-list__item').forEach(el=>{
			el.style.width = this.addEditForm.uploadHeight
			el.style.height = this.addEditForm.uploadHeight
			el.style.borderWidth = this.addEditForm.uploadBorderWidth
			el.style.borderStyle = this.addEditForm.uploadBorderStyle
			el.style.borderColor = this.addEditForm.uploadBorderColor
			el.style.borderRadius = this.addEditForm.uploadBorderRadius
			el.style.backgroundColor = this.addEditForm.uploadBgColor
		  })
	  })
	},
  }
};
</script>
<style lang="scss">
.editor{
  height: 500px;
  
  & /deep/ .ql-container {
	  height: 310px;
  }
}
.amap-wrapper {
  width: 100%;
  height: 500px;
}
.search-box {
  position: absolute;
}
.addEdit-block {
	margin: -10px;
}
.detail-form-content {
	padding: 12px;
}
.btn .el-button {
  padding: 0;
}
</style>
