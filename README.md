# 1.	课程设计目的
本课程设计的目的是实现南昌市旅游网站的静态页面设计，理论与实践相结合，让我们更深刻的理解上课时所讲的东西，加强我的动手能力，专业素质和专业技术，同时也要锻炼我的自主学习能力，是我能通过自己探索独立完成一些老师没有讲过的知识与内容。具体的课程设计应达到以下目的：
1．提高学生在实际操作中收集信息，对信息进行价值判断，进行信息整理、加工的能力。
2．在实际的项目任务中培养网页设计方面的素养。
3．在实际的项目任务中使学生网页编程和制作的能力得到提高。
4．培养学生团队协作和人际交往方面的能力。
5. 培养相关知识和技能的综合应用能力。

2.	实现功能
任务要求：
《Web程序设计》的课程设计课题选择应从专业网站建设的实际出发。具体要求如下：
1.	站点设计合理、管理有序、无多余文件和文件夹、大小合适。首页命名要规范，存放位置要正确，不可以是zhuye.htm、main.htm、我的主页.htm等。主页文件名应该使用index或default等。其他文件或文件名命名也要规范，不使用汉字或带有空格的名称。最好是符合各种系统命名规则。
2.	站点至少要有三层结构，如下图所示，页面数不得少于10页；如首页，登录页，注册页，其中一页必须是留言板；所有页均为静态页面，使用HTML、CSS制作，部分页面加入Javascript交互效果。
3.	自选主题，主题内容要合法、健康、实用。
4.	网页要有版权说明；
5.	要仔细考虑网站定位。分析面向的潜在访客群体的需求特点，选择内容和版式。
6.	网站主题突出、内容丰富；
7.	网站与网页风格应该协调一致，网站结构应层次分明，内容重点突出，页面设计要符合追求色彩的搭配、布局和合理性，以及要有一定的创意。
8.	各页面设计合理、美观，有创意。不要太花哨或太孩子气。要有网页平面设计过程，不要只是各种元素的随意拼凑。图片动画选用要适合主题，不要在网页中插入不相干的图片。适用于各种显示器的分辨率和颜色。不要太宽，否则显示器分辨率小时会出现水平滚动条。
9.	各个页面之间的链接要合理有效，路径要正确（相对路径）；
10.	注意网站的大小，图片保存格式和图片大小要合适；
11.	代码结构清晰，无垃圾代码。

我实现的功能：
我的课程设计的题目是网上书店。我的网站设计主要是我以前做过的一个网上商城的项目-品优购，结合当当网的页面布局，然后经过自己的增删改查就成了我的web课设。我总共写了6个页面，实现了网上书店的主页面，注册，登录，商品列表页，商品详情页，用户留言板等功能，其中运用了定位，浮动，动画，过渡，盒子模型等知识点，还有H5里的语义化标签和新增的表单属性等，更多网站图标，SEO，字体图标等亮点。
3.	网站分析设计
index.html
首先我创建了一个base.css，实现了css的初始化。然后创建了一个common.css，将公共部分的css代码放在其中，包括shortcut快捷导航栏，header头部模块（含有logo模块，search模块，热词模块，购物车模块），footer底部模块。其次再创建index.html，将网站的首页写好，其中包括了上述的shortcut快捷导航栏，header头部模块，footer底部模块，还有main模块，固定定位模块，今日推荐模块，猜你喜欢模块，楼层区域模块（主要包含商品的图片展示）。再创建index.css，将首页的css代码放入其中。最后引入base.css，common.css，index.css和字体图标的样式，网站图标。
而网站布局方面主要还是使用盒子模型，然后利用浮动，定位等方法，每个模块都是一个大盒子，都包含了版心（1200px），位于屏幕的中心。亮点有main模块focous盒子里运用了CSS3的动画，lifeservice盒子里则使用了表格布局，里面含有精灵图的切图使用。购物车模块则使用子绝父相，将购物车的商品数量放在上方。其他方面的布局大同小异。
list.html
这个是列表页面，位于全部商品中的电子书超链接中。主体分为了四个区域：头部导航区域，列表主体区域，列表分页区域，和尾部区域。头部和尾部区域与首页的设计一致；只不过多了个秒杀模块，还有nav导航栏多了秒杀的内容。列表主体则是设计了一个没有高的大盒子，通过16个li盒子撑开大盒子，大盒子加了伪类元素清除浮动法防止底部模块挤上来。列表主体里的每个小盒子，包括了商品图片，商品内容介绍，还有商品数量进度区域，使用了calc函数。列表分页模块则是利用了行内块元素的特点使盒子可以居中并排。
detail.html
商品详情页面则是list.html的子页面。位于第一个子盒子的图片链接中，同样包含了快捷导航头部区域，尾部区域，还多了产品详情模块，产品详情模块分为产品介绍模块和产品详情模块。这个模块的亮点在于产品介绍的布局使用了自定义列表进行布局，为了使每行左边子盒子（dt）的大小一致，而且没有给盒子高，使内容自动撑开盒子，每个dl盒子都需要清除浮动。产品介绍左边则还使用了伪元素，结合浮动将左拉右拉符号位于list_item盒子的左右两边。
lyb.html
留言板页面是位于快捷导航栏的客户服务超链接中，包含了快捷导航头部区域，尾部区域，还有就是留言板主体模块，模块分为留言板头部，用表格布局了一个网络商场的新闻列表，留言板身体部分则是用盒子模型布局，设计了姓名，内容，主题，邮箱等功能。
register.html
register.html页面是简约布局，注册主体部分使用了表格布局，表格布局的好处是左边的盒子可以自己设置宽高（dd是块级元素），包含文字的盒子可以不挤压input。还使用了前端表格验证，加了之前实验的代码，加以改动，可以实现手机号的位数在6-11位之间，然后两次密码输入密码不能相同，每个input不能为空等功能

log_in.html
登录页面的布局大致和注册页面差不多。不一样是登录页面的主体使用了背景图片，使页面更加艺术。登录主体使用了定位布局，功能有登录名，和登录密码。用了列表布局使log_bd盒子错落有致。
页面风格
每个页面的js，css，代码都有公共的，也有属于这个页面的。
1.HTML要规范，让页面HTML代码更具语义性。
2.了解各种图片格式特性，根据特性制定图片规范。
 3.CSS规范统一规项目 CSS 代码书写风格
4.命名规范从 目录、图片、HTML/CSS文件的命名等层面约定规范项目的命名习惯，增强项目代码的可读性。

