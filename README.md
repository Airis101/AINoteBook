# AIM∞AINoteBook

## 一、简介

AIM∞AINoteBook 一款精巧的AI笔记本，将传统的手写计划本“智能&动态化”，使用高强度算法对数据进行了加密处理，为大家提供安全、便捷的个人日常规划以及本地知识管理体验。

## 二、主要功能

- DashBoard一览任务计划等信息
- 日记、周计划、报告等多类型笔记管理
- AI阶段性分析
- AIMi酱同学智能问答
- 导出功能(支持分析报告、聊天记录为txt、pdf、word)
- 数据本地加密存储
- 支持多用户
- 支持多模型，DeepSeek、Qwen、OpenAI

## 三、部署运行

### 1. 环境准备
- Windows 10/11  

为了尽可能的照顾到所有人，包括非IT行业的人员也能够方便快速的部署，我们提供了最为便捷的方式，在windows环境中，AINoteBook依赖的所有环境均集成到了主程序AINoteBook.exe中，大家只需要一键运行即可启动整个AINoteBook服务。
> **注:** 当前仅提供windows平台支持，后续陆续提供linux、mac平台版本。  

### 2. 下载AINoteBook到本地
下载完后，对应下图四个文件：  

<img width="1027" height="166" alt="image" src="https://github.com/user-attachments/assets/207f80c4-3d57-4e0a-af4e-e6bb23790793" />  
可对主程序AINoteBook.exe进行hash校验，如下:

    md5: 5E199E42AA5650350CA133F9D79F36E3
    sha1: F792098E2B986E5555EA4944810412F7F82752BC

### 3. 运行AINoteBook主程序
点击运行主程序后，看到如下界面表示服务启动成功：  

<img width="1305" height="629" alt="image" src="https://github.com/user-attachments/assets/4758be88-f474-4d5f-8f69-44a2634f0b48" />


同时会自动打开浏览器看到AINoteBook登录界面：  

<img width="1444" height="973" alt="image" src="https://github.com/user-attachments/assets/db257841-1d43-4afc-88db-c35953a87b18" />

### 4. 激活AI,配置API_KEY

AINoteBook_v1.0.0支持三家模型提供商的模型，DeepSeek、Qwen以及OpenAI，经过安全、性能考虑，AIMi酱仅用Qwen做支持！  
> 为了安全起见，决定不把API_KEY写入程序保存，大家可以配置对应的环境变量，这样AINoteBook会自动识别。

下面进行API_KEY环境变量配置部分介绍：
#### 1）环境变量名称
    DeepSeek: API_KEY_QWQ
    Qwen: API_KEY_DEEPSEEK
    OpenAI: API_KEY_GPT
#### 2）获取API_KEY
访问模型所需的API_KEY可以在对应的厂商官网获取，获取到的API_KEY格式如下:  

    sk-000000000yourkey000000000000

#### 3)配置环境变量  
以阿里通义千问Qwen为例，进行介绍，右键此电脑，点击 **属性**  
<img width="547" height="506" alt="image" src="https://github.com/user-attachments/assets/19637c5b-8766-477d-b603-7e894359dfc5" />  

在弹出来的界面 系统->系统属性 中点击 **高级系统设置**  
<img width="1415" height="493" alt="image" src="https://github.com/user-attachments/assets/ab3bcef8-185c-443c-a092-7e1bb986a637" />  

在弹出来的界面中，点击 **环境变量**  
<img width="734" height="823" alt="image" src="https://github.com/user-attachments/assets/6e89092d-e4b0-4a90-9c30-414b3f31ed72" />   

在弹出来的环境变量界面，可以选择新建用户变量，也可以选择新建系统变量，以用户变量为例，点击 **新建**  
<img width="961" height="475" alt="image" src="https://github.com/user-attachments/assets/cf51a41a-95c5-4118-abc3-d5b237a0345f" />  

在弹出来的界面中，
- 变量名(N)：就是之前提到过的三家模型提供商对应的API_KEY名称，如上 1）中介绍的，这里我们用的是Qwen，即变量名这里填： "API_KEY_QWQ"
- 变量值(V): 就是你在对应模型厂商获取到的API_KEY的值，如上 2）中介绍的，获取到后填入即可  


<img width="1011" height="257" alt="image" src="https://github.com/user-attachments/assets/05ed41c4-6acb-4c7e-b93d-7487ff3eee72" />  

> **注意**：一定对应上，比如你使用的是Qwen，那么API_KEY_QWQ的值应该是你在阿里千问里获取到的API_KEY值！  


### 5. 注册账号，开始使用
在AINoteBook注册界面注册一个账号后，便可登陆系统开始使用，

<img width="1519" height="1002" alt="image" src="https://github.com/user-attachments/assets/16b2e9da-d03e-4276-8583-31756ca4c0ed" />

可在分析中，和AIMi酱聊天测试上 3) API_KEY环境变量是否配置成功  

<img width="1654" height="1012" alt="image" src="https://github.com/user-attachments/assets/5f299429-efc5-4815-889f-83afb05cb748" />

## 6.功能介绍

### 1) 仪表盘
<img width="1616" height="1069" alt="image" src="https://github.com/user-attachments/assets/eeb1d56c-9301-445f-aece-baa2d5b87f8e" />
在仪表盘中，你可以一览任务一些关键信息，如临近截至日期的任务完成率、待办任务、记录日记数目等等信息，你还可以选择右上方的下拉栏里面进行时间筛选，可以将展示数据范围固定到一个时间段(本周/本月/本年/所有时间)。  
你还可以点击上方的**待办任务**和**日记卡片**，直接看相应的信息，如下图所示：
<img width="1382" height="461" alt="image" src="https://github.com/user-attachments/assets/3719deb6-efa2-4dd6-98e0-0a122477e516" />

### 2) 计划  
计划模块分为 **计划编辑** 以及 **历史计划查询** 这两部分。  
在 **计划编辑** 界面，你可以进行计划编写，每个计划栏包含一下选项： 
- 计划标题
- 描述
- 任务执行状态
- 任务重要性
- 任务截至日期  
 
如下图所示：  

<img width="1616" height="980" alt="image" src="https://github.com/user-attachments/assets/eaa2a38f-8a5d-4fa3-990b-7f3ff75913ad" />


在 **历史计划查询**  界面，你可以对历史编写的计划进行查询，默认该栏会显示历史所有计划项目，可以按照一下方式进行筛选和排序：  
- 按照时间范围进行筛选
- 按照任务状态筛选
- 按照任务重要性进行排序  
 
例如，下面查询日期范围在 **2025/07/01 - 2025/07/31**、任务状态为 **未开始**、按照 **未完成任务临近截止日期** 进行筛选排序：  
<img width="565" height="466" alt="image" src="https://github.com/user-attachments/assets/9e1079be-1e0a-4001-af43-6e3252f05f90" />


另外在计划编辑界面有上方提供了三个不同颜色功能按钮  

<img width="781" height="53" alt="image" src="https://github.com/user-attachments/assets/480015d3-4fe7-4d30-92dc-5749ff5e037d" />

分别是:  

- 蓝色: 保存当前计划栏中编写的计划
- 黄色: 返回本周计划(查看本周编写的计划项目)  
- 灰色: 将右侧中筛选后的计划项目同步到计划编辑栏  


可以配合筛选功能来快速对计划进行编辑。  

### 3) 日记
日记模块同样分为 **写日记** 和 **计划列表** 两个部分，如下图：  
<img width="1607" height="1055" alt="image" src="https://github.com/user-attachments/assets/2280d872-a6bc-404e-96da-58f2538f9ab3" />  

在**写日记**界面中，你可以进行日记编写(当然也不一定必须是日记，你可以自己定义去写什么，比如随手记这种)，每个日记包含一下部分:  
- 日期 
- 心情：分为五个级别
- 内容
- 标签：可以是 生活、学习、运动、娱乐等  

编写完后保存即可。  
在 **历史计划** 查询界面，可以查看历史日记条目，默认会显示所有日记。可以进行查询筛选，支持按 **关键字** 以及 **日期查询**。如下，按照关键字“骑行”进行筛选  
 <img width="578" height="266" alt="image" src="https://github.com/user-attachments/assets/9e2f4648-f4c1-42f4-9572-f26771da7de5" />

在筛选结果中点击指定日记条目，会自动同步到日记填写界面，方便进行修改等操作  
 <img width="1569" height="531" alt="image" src="https://github.com/user-attachments/assets/db826c2e-8f12-435f-b501-ae6650f123a9" />


### 4) 分析  
分析模块分为 **数据分析中心** 以及 **AIMi酱同学** 两部分。
<img width="1720" height="1139" alt="image" src="https://github.com/user-attachments/assets/3de28e9f-42b6-491e-b707-f96a9313c360" />

在**数据分析中心**界面，你可以选择对自己自定日期范围内的的日常学习生活等进行总结，可以选择不同的模型来进行分析:  
<img width="1114" height="1019" alt="image" src="https://github.com/user-attachments/assets/d948a4f2-e13e-4ed2-90f9-efeba28baa6f" />

指定筛选日期后，便会开是尽心分析，分析结果将按照如下五个维度进行:  
- 任务完成情况分析
- 心情趋势变化追踪
- 时间管理效率评估
- 个性化改进建议
- 亮点总结  

分析结果类似下图:  

<img width="1129" height="950" alt="image" src="https://github.com/user-attachments/assets/8987a674-bcde-442b-9ea6-af6c47d47669" />

你还可以在界面下方的**历史报告**中查看历史分析的报告  

<img width="1466" height="801" alt="image" src="https://github.com/user-attachments/assets/a7586bf3-1c88-4b68-b4e2-daef5e4a8f9d" />

你也可以将分析结果导出为 txt/word/pdf   

<img width="927" height="168" alt="image" src="https://github.com/user-attachments/assets/a12bc26f-ef3f-4339-aa67-33d3f2ee409c" />

在**AIMi酱同学**对话框中，你可以和AIMi酱进行包含计划任务、日记信息等在内的智能对话。你可以通过新建会话的方式来对对话内容进行分类，这样在基于上下文的回答过程中AIMi酱会回答的更加准确，如下图:   

<img width="525" height="319" alt="image" src="https://github.com/user-attachments/assets/38cba9dc-090d-4791-827f-1d866ec2ac59" />

随后你便可以在对应的会话中和AIMi酱进行聊天。
在聊天过程中，你可以通过右上方的**记忆功能**按钮来决定是否让AIMi酱记住之前的聊天对话信息，开启后，AIMi酱在长上下问对话过程中回答会更加准确，但是同时缺点是 “比较烧钱”！  

我们的建议是，对于单次不需要参考以前聊天内容的问答，可以关闭该功能。对于多次相关问答，则开启该功能。  

<img width="560" height="141" alt="image" src="https://github.com/user-attachments/assets/6929d2a7-2cab-4f4a-a042-64e2ea232f67" />

最后，你还可以将对话内容导出为 txt/word/pdf  

<img width="522" height="440" alt="image" src="https://github.com/user-attachments/assets/5d7d2284-3b8f-4c49-8176-f783ab540f19" />


### **AIMi酱功能探索**
AIM∞AINoteBook最智能的部分就是AIMi酱同学了，她可以为你提供强大的旅行安排、任务规划、计划规划、日程整理等帮助。  
这里以一个日常生活中常见的例子 “旅游规划” 来进行展示:  

>  **现在有这样一个场景：你想最近这一段时间去苏州旅游，但同时又不想因此拉下还没有完成的任务计划，此时你就可以让AIMi酱去帮你整理一份同时包含完成计划在内的旅游规划方案。**

有时候，当你懒得去仪表盘或计划栏看你当前剩余待办的任务或计划项时候，你就可以把问题抛给AIMi酱，她会帮你整理   

<img width="557" height="882" alt="image" src="https://github.com/user-attachments/assets/1f3fe72d-0f8f-40f3-95b2-84ba1a488ae2" />

随后，你可以直接让AIMi酱来给你整理一份带任务计划的旅游方案   

<img width="654" height="1107" alt="image" src="https://github.com/user-attachments/assets/1e93644e-b743-4bb0-806c-b9100edc5568" />
<img width="661" height="895" alt="image" src="https://github.com/user-attachments/assets/c67494f6-2be4-41bf-8629-80566b15f7be" />

有时候，AIMi酱还会自动帮你导出旅游方案文档(也可以手动导出)，在浏览器下载界面即可看到导出文档  

<img width="1143" height="929" alt="image" src="https://github.com/user-attachments/assets/03e2bf82-ccb9-4c54-9e79-05d7b465f9c4" />

AIMi酱还有很多强大功能，另外AINoteBook也不仅只可应用在记笔记这一件事上，你也可以把它应用到日常办公，例如以下行业：  
   
   - 教师<br>
      - 记录教学方案计划<br>
      - 学生学习成长记录跟踪<br>
      - 班级考试成绩统计记录<br>
      - ...<br>
   - 医生<br>
      - 药物信息&作用记录<br>
      - 病人治疗计划跟踪<br>
      - 病人治疗康复过程统计跟踪<br>
      - ...<br>
   - ...

这样，对于教师，例如你想要分析某一个学生的学习以及成长情况，你只需要询问AIMi酱即可，AIMi酱会给生成一份针对该学生的学习成长分析报告；对于医生，想要追踪分析一个病人的治疗过程以及康复状况，也只需询问AIMi酱即可。  

另外对于很多在职员工，可能经常需要填写周报、月报、半年绩效考核、年度绩效考核等等报告，如果你之前相关内容已经记录在了AINoteBook当中，你就可以让AIMi酱来帮你完成，你只需要告诉AIMi将报告编写格式等要求，AIMi酱便会自动根据你的历史记录来帮你写完整个报告。

剩下很多功能大家可以自行探索，如果你在使用的过程发现了有更好的应用方式，也欢迎进行共享！


## 四、安全说明

在AINoteBook中，即使我们已经采用了高强度的加密算法以及签名来保障数据安全，但事无绝对，如果你需要更安全的保护你的数据，一个好的建议是，可以把AINoteBook复制到一个加密磁盘或u盘中，然后在加密磁盘或u盘中启动AINotebook即可，这样攻击复杂度会在上升一个层次！  

AINoteBook无需安装，启动时候自动加载到内存中运行，因此放在U盘还有一个好处，当你换电脑或者想要在其他电脑上运行你的AINoteBook时候，只需要插入U盘即可运行，但同时需要注意该电脑也需要配置API_KEY环境变量！ 


## 五、后续版本规划
当下，虽然我们将AINoteBook的所有数据均存放在本地，但AINoteBook需要依赖模型提供商来提供AI支持，所以数据并不算完全本地化。

未来，我们将为AIM∞AINoteBook提供本地模型支持，让数据彻底与互联网分离，实现完全本地化！

同时，我们也将引入更多强大的功能，AINoteBook将支持图片&视频记录、视频/网页/文档总结、虚拟角色等等多元化功能，AIMi酱也将走出聊天框，成为你更为强大的个人助手！  


## 六、反馈与支持

如有问题或建议，欢迎联系AI Mission Infinity开发团队或提交 issue。 

**另外可以关注团队bilibili(搜索AIMInfinity即可)、Tiktok、X、Medium等官方账号，我们会进行更多的有趣分享，包括AINoteBook的详细"食用指南"!**


## 贡献者名单
- s3r2t
- 小不点要听话
- Freedom369369
- Lumira


---

>**AIM∞AINoteBook完全免费，任何人均可将其应用到自己的日常生活中。**

<img width="1197" height="1189" alt="image" src="https://github.com/user-attachments/assets/a31cb229-8d1a-42e2-9c22-60cc69bde1bb" />  
<img width="1197" height="550" alt="image" src="https://github.com/user-attachments/assets/8cdc8488-ca90-46f9-ad54-b17737470a45" />

