# F036 vue+flask中医热性药知识图谱可视化系统vue+flask+echarts+mysql


> 完整项目收费，可联系QQ: 81040295 微信: mmdsj186011 注明从github来的，谢谢！
也可以关注我的B站： 麦麦大数据 https://space.bilibili.com/1583208775
> 

关注B站，有好处！
编号:  F036
## 视频

[video(video-dKV7dwOq-1761375371400)(type-bilibili)(url-https://player.bilibili.com/player.html?aid=659817171)(image-https://i-blog.csdnimg.cn/img_convert/095dae303488923dda4525b6d00f1372.jpeg)(title-vue+python 中药可视化系统前后端分离带数据库echarts可视化、Flask)]

## 1 系统简介
系统简介：本系统是一个基于Vue+Flask+ECharts+MySQL构建的中医热性药知识图谱可视化系统，旨在为用户提供中医药材和方剂的知识查询与可视化分析服务。系统的核心功能包括：首页，展示系统概览及热性药材的知识点图谱；药材搜索与介绍模块，支持用户查询中医热性药材的详细信息；方剂搜索与构成查看模块，提供热性方剂的组成成分及其药理作用；功效关键词提取与分析模块，通过自然语言处理技术提取关键词并生成可视化分析图表；以及用户管理模块，包含登录、注册、修改个人信息、头像及密码等功能，确保用户体验的安全性和个性化需求。
## 2 功能设计
系统采用B/S（浏览器/服务器）架构模式，前端基于Vue.js框架，结合Vuex进行状态管理，Vue Router实现路由导航，ECharts负责数据可视化图表的渲染。前端通过RESTful API与Flask后端交互，后端负责业务逻辑处理，同时利用MySQL数据库进行数据存储，包括中医热性药材、方剂、功效关键词等相关信息的持久化管理。此外，系统还集成了数据爬虫模块，用于抓取并处理中医药相关数据，清洗后导入数据库，为系统提供数据支持。
### 2.1系统架构图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c059c460fea440d681dea9af4b91247c.jpeg)
### 2.2 功能模块图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/eefff9ae53c44d60bf38e42a970ee1e4.png)
## 3 功能展示
### 3.1 登录 & 注册
登录注册做的是一个可以切换的登录注册界面，点击去登录后者去注册可以切换，背景是一个视频，循环播放。
登录需要验证用户名和密码是否正确，如果**不正确会有错误提示**。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6d148c6cf6bb4071b0c2ab6cc621d3f2.png)
注册需要**验证用户名是否存在**，如果错误会有提示。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0040b6b5008545f4b022c03dfc104c5d.png)
### 3.2 主页
主页的布局采用了左侧是菜单，右侧是操作面板的布局方法，右侧的上方还有用户的头像和退出按钮，如果是新注册用户，没有头像，这边则不显示，需要在个人设置中上传了头像之后就会显示。
### 3.3 药材搜索 & 药材详情
药材搜索：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ae3f992112b94957b28319fcd9c004e0.png)
药材详情
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/23dcc444f7d64ca99aac088421df736c.png)
### 3.4  方剂搜索 & 构成查看
方剂搜索：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/2da3b7a2e9ec4ac7b20524a9fe162747.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/204a829ca4bf4f3d90825f8b9d67867f.png)
方剂的构成，组成成分：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/84c24d573b7f4140a040de8d97a79186.png)
### 3.5  数据大屏可视化
数据大屏可视化包含了
药材的类型和药味的分析：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d05281151e0d41fd8fb1eb9f26385395.png)
类型和药味的排名：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/552bdfb3d72840bf85656f8f5430c6ed.png)
### 3.6  关键词分析 & 关键词提取
关键词提取：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/2b8e655bd5f8451494134b07cbcf52bf.png)
关键词分析：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/273e8a5a50e343edb9ba625ae36a9e89.png)
### 3.7 个人设置
个人设置方面包含了用户信息修改、密码修改功能。
用户信息修改中可以上传头像，完成用户的头像个性化设置，也可以修改用户其他信息。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/cb822c8e534b4b43ba1d3e5e5833ead7.png)
修改密码需要输入用户旧密码和新密码，验证旧密码成功后，就可以完成密码修改。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d87b0003606d4d67b93b14555924852b.png)
## 4程序代码
### 4.1 代码说明
代码介绍：该功能旨在构建一个中医热性药物的可视化界面，基于Vue框架和ECharts图表库。界面将展示中医药物的热性分布，用户可以通过地图、柱状图等方式查看药物的热性分布情况。界面支持药物信息的筛选、查看详情以及交互式的数据探索。
### 4.2 流程图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ed22a84997ad4998959be82ec8148d64.png)

### 4.3 代码实例
```python
<template>
  <div class="app-container">
    <div class="filter-container">
      <el-select v-model="selectValue" placeholder="请选择">
        <el-option label="全部" value="all"></el-option>
        <el-option label="高热" value="high"></el-option>
        <el-option label="中热" value="medium"></el-option>
        <el-option label="微热" value="low"></el-option>
      </el-select>
    </div>
    <div id="chart" style="width: 100%; height: 600px;"></div>
    <div class="table-container">
      <el-table :data="medicineList" stripe>
        <el-table-column prop="name" label="药物名称"></el-table-column>
        <el-table-column prop="properties" label="性味"></el-table-column>
        <el-table-column prop="effects" label="功效"></el-table-column>
      </el-table>
    </div>
  </div>
</template>

<script>
import echarts from 'echarts'
import 'echarts/map/js/china.js'

export default {
  data() {
    return {
      chart: null,
      selectValue: 'all',
      medicineList: [
        {
          name: '药物A',
          properties: '辛、温',
          effects: '温中散寒'
        },
        // ... more data
      ]
    }
  },
  mounted() {
    this.initChart()
  },
  methods: {
    initChart() {
      this.chart = echarts.init(document.getElementById('chart'))
      const option = {
        title: {
          text: '中医药热性分布图'
        },
        toolbox: {
          feature: {
            saveAsImage: {}
          }
        },
        series: [
          {
            type: 'map',
            mapType: 'china',
            data: []
          }
        ]
      }
      this.chart.setOption(option)
    }
  }
}
</script>

<style>
.app-container {
  padding: 20px;
}

.filter-container {
  margin-bottom: 20px;
}

.table-container {
  margin-top: 20px;
}
</style>

```
```
