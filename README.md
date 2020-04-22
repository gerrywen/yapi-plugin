# yapi-plugin

## 使用说明：
[使用教程]<https://github.com/diwand/YapiIdeaUploadPlugin/wiki/快速使用>
>  打开idea preferneces->plugins-> install plugin from disk,导入disk目录下jar 包后(install)，重启 

>  项目.idea目录下的misc.xml配置  

```xml
  <component name="yapi">
    <option name="moduleList">xinyartech-erp-web-api</option>
  </component>
  <component name="xinyartech-erp-web-api">
    <option name="xinyartech-erp-web-api.projectToken">08c09a8e7297077803f3beaf108ae4a19eabd8c3074dd022bd19c20750956217</option>
    <option name="xinyartech-erp-web-api.projectId">7</option>
    <option name="xinyartech-erp-web-api.yapiUrl">http://121.40.103.53:33066</option>
    <option name="xinyartech-erp-web-api.projectType">api</option>
    <option name="xinyartech-erp-web-api.attachUploadUrl">http://localhost/fileupload</option>
    <option name="xinyartech-erp-web-api.returnClass">com.xinyartech.erp.base.wrapper.ResponseWrapper</option>
  </component>
```

> 各个参数获得 

token 获取方式： 打开yapi ->具体项目->设置->token 配置<br/>
项目id 获取方式：点击项目，查看url 中project 后面的数字为项目id http://127.0.0.1:3000/project/72/interface/api<br/>
yapiUrl 获取方式：部署的yapi 地址<br/>
projectType 填写方式： 根据你要上传的接口类型决定，接口就填api<br/>
attachUploadUrl 填写方式:上传java 类zip 的url,如果要用请实现http://localhost/fileupload 接口 接口请求参数为 file 文件类型。(可不填)<br/>
returnClass 填写方式:统一返回对象的全路径（1.7.4及之后支持,之前版本可不配)<br/>
moduleList 获取方式：模块名称，用 "," 分割 ，不支持父节点和子模块名称一样的情况<br/>

> 上传

选中controller 类中的方法名称或类名（要选中方法名称，或类名，选中类名为当前类所有接口都上传），右击XinYaApiUpload(alt+u快捷键)

> cross-request 插件下载安装教程
<https://cloud.tencent.com/developer/article/1517980>
