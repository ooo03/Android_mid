NotePad 笔记应用

项目概述

NotePad是一个基于Android平台的简易笔记应用，提供了创建、编辑、删除和分类管理笔记的功能。本项目是在Android官方早期数据库操作教程的基础上进行扩展和优化，增加了笔记分类功能和现代化的UI设计。

功能特点

基本功能
1. 创建新笔记
2. 编辑现有笔记
3. 删除笔记
4. 查看笔记列表
5. 搜索笔记

扩展功能
1. 笔记分类管理
   1.1 支持多种分类：未分类、个人、工作、学习、其他
   1.2 分类选择UI
   1.3 分类显示功能
2. 现代化UI设计
   2.1 浅色主题
   2.2 卡片式布局
   2.3 阴影和深度效果
   2.4 优化的颜色方案

技术实现

数据存储
1. SQLite数据库：使用SQLite作为本地数据库存储笔记数据
2. ContentProvider：通过NotePadProvider管理数据访问，提供统一的接口
3. SQLiteOpenHelper：实现DatabaseHelper类管理数据库的创建和版本控制

数据库结构

CREATE TABLE notes (
_id INTEGER PRIMARY KEY AUTOINCREMENT,
title TEXT,
note TEXT,
created INTEGER,
modified INTEGER,
category TEXT DEFAULT '未分类'
);

主要组件

1. NotesList：笔记列表页面，显示所有笔记
2. NoteEditor：笔记编辑页面，用于创建和编辑笔记内容
3. TitleEditor：标题编辑页面，用于设置笔记标题
4. NotePadProvider：内容提供程序，管理数据访问
5. DatabaseHelper：数据库助手类，管理数据库创建和版本控制

界面设计

1. 使用自定义主题和样式
2. 卡片式布局设计
3. 现代化的颜色方案
4. 响应式布局

项目结构

NotePad/
└── app/
└── src/
└── main/
├── java/com/example/android/notepad/
│   ├── NoteEditor.java       笔记编辑界面
│   ├── NotePad.java          主应用
│   ├── NotePadProvider.java  内容提供程序
│   ├── NotesList.java        笔记列表界面
│   └── TitleEditor.java      标题编辑界面
├── res/
│   ├── drawable/             图像资源
│   ├── layout/               布局文件
│   │   ├── note_editor.xml   笔记编辑布局
│   │   ├── noteslist_item.xml笔记列表项布局
│   │   └── title_editor.xml  标题编辑布局
│   ├── menu/                 菜单资源
│   ├── values/               值资源
│   │   ├── strings.xml       字符串资源
│   │   └── styles.xml        样式资源
│   └── xml/                  XML资源
└── AndroidManifest.xml       应用清单

界面展示

笔记列表界面
1. 显示所有笔记的标题、修改日期和分类
2. 支持长按操作（删除、分享等）
3. 支持搜索功能
<img width="520" height="942" alt="{47232ACB-07AE-4A31-BE68-2D7BC32E2CC4}" src="https://github.com/user-attachments/assets/6f29a134-0825-419e-a67d-ba2d1c4e6d1f" />
<img width="504" height="953" alt="{1D107773-7C85-4A60-8A1B-3D65CA220488}" src="https://github.com/user-attachments/assets/dbb41987-e490-4d58-896e-b7a2bf845e84" />

笔记编辑界面
1. 支持多行文本编辑
2. 自动换行
3. 支持分类选择

分类选择界面
1. 提供预设的分类选项
2. 支持快速选择和更改分类

使用方法

1. 创建笔记：
   1.1 在笔记列表界面点击菜单按钮，选择"新建"或"添加笔记"
   1.2 输入笔记内容
   1.3 点击菜单按钮，选择"保存"
   1.4 输入笔记标题
   1.5 选择分类（可选）

2. 编辑笔记：
   2.1 在笔记列表界面点击要编辑的笔记
   2.2 修改笔记内容
   2.3 点击菜单按钮，选择"保存"

3. 删除笔记：
   3.1 在笔记列表界面长按要删除的笔记
   3.2 选择"删除"

4. 更改笔记分类：
   4.1 在笔记编辑界面点击菜单按钮
   4.2 选择"更改分类"
   4.3 选择新的分类

安装和运行

1. 克隆项目到本地：
   ```
   git clone https://github.com/yourusername/NotePad.git
   ```

2. 使用Android Studio打开项目

3. 连接Android设备或启动模拟器

4. 运行项目

许可证

本项目采用Apache License 2.0许可证，详见LICENSE文件。

致谢

1. Android官方文档和示例
2. 参考了CSDN上的Android Sample--NotePad解析（https://blog.csdn.net/llfjfz/article/details/67638499）
