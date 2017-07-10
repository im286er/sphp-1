<h1>SPHP（A Simple PHP Framework） 一个简洁的PHP框架 ....</h1>

<h2>1.目录结构</h2>
<br>sphp/
<br>├── config
<br>├── default
<br>│   ├── controller
<br>│   │   ├── base.class.php
<br>│   │   └── index.class.php
<br>│   ├── module
<br>│   │   └── base.class.php
<br>│   └── templates
<br>│       └── index.html
<br>├── framework
<br>│   ├── controller
<br>│   ├── include
<br>│   ├── lib
<br>│   ├── module
<br>│   └── third
<br>│       └── smarty-2.6.30
<br>├── index.php
<br>├── README.md
<br>├── _templates_c
<br>└── _templates_cache

结构说明：config（配置目录）、default（默认项目可自由定义名称）、framework（框架核心程序）
_templates_c（smarty编译目录）、_templates_cache（smarty缓存目录）、index.php（单入口访问程序）

<h2>2.访问路径</h2>
<br>eg：http://example.com/index.php?site=default&ctl=index&act=index
<br>site：项目名称
<br>ctl：控制器名称
<br>act：方法名称


<h2>3.控制器命名规则</h2>
<br>eg：
<br>product.class.php（文件命名）
<br>/项目名称/controller/ （存放路径）

class controller_product extends controller_base
<br>{
<br>   public function __construct() {
<br>      parent::__construct()
<br>   }
}

<h2>4.模型命名规则</h2>
<br>eg：
<br>product.class.php（文件名称）
<br>/项目名称/module/ （存放路径）

class module_product extends module_base
<br>{
<br>   public function __construct() {
<br>      parent::__construct()
<br>   }
}

<h2>5.模板命名规则</h2>
<br>模板文件存放路径为：/项目名称/templates/，文件后缀可遵循Smarty或自己设置