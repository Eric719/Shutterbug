##斯坦福大学iOS公开课 Shutterbug
遇到一个小问题，在这里记一下。

当前使用xcode7，在创建Universal项目时，不会自动生成 Main_iPhone.storyboard 和 Main_iPad.storyboard，手动增加方法：

1.首先设置Devices为Universal。

2.选中项目中的Main.storyboard，打开右侧工具栏，选中最左边的文本图标（show the file inspector），取消选中 Use Size Classes 选项。

3.在弹出框中,Keep size class data for:选择iPhone，然后点击Disable Size Classes 按钮。

4.将Main.storyboard重命名为Main_iPhone.storyboard。

5.文件－新建－iOS-User Interface－选择Storyboard，点击Next，命名为Main_iPad.storyboard，然后创建，保存在当前项目下。

6.在Main_iPad.storyboard中，设置根视图，然后同样打开右侧工具栏，选file inspector，取消选中Use Size Classes。

7.在弹出框中，Keep size class data for:选择iPad，点击Disable Size Classes 按钮。

8.打开Info.plist文件，将 Main storyboard file base name 的值，修改为 Main_iPhone，然后在下面再添加一条 Main storyboard file base name (iPad)，其值为：Main_iPad。

9.OK

