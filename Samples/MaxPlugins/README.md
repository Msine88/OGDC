
编译工具：
1.   VS 2012
2.   安装3dsMax 2014
	
联调环境配置：
1.使用x64平台的解决方案。
2.打开Max2014Plugin属性页，配置属性->链接器->常规->输出文件改为3dsmax安装目录中的stdplugs/SuMax2014Plugin.gup。
    （例如：C:\Program Files\Autodesk\3ds Max 2014\stdplugs\SuMax2014Plugin.gup）
3.打开Max2014Plugin属性页，配置属性->调试->命令改为3dsmax安装目录的可执行文件路径。
    （例如：C:\Program Files\Autodesk\3ds Max 2014\3dsmax.exe） 
4.将Samples\MaxPlugins\Bin_Unicode_x64下的文件拷到Builds\Win_Solution_vc11\Bin_Unicode_x64下，后者为环境变量，运行3dsmax2014的release版；
   将Samples\MaxPlugins\BinD_Unicode_x64下的文件拷到Builds\Win_Solution_vc11\BinD_Unicode_x64下，后者为环境变量，调试3dsmax2014的debug版。
5.修改Builds\Win_Solution_vc11\Bin_Unicode_x64（release版）或 Builds\Win_Solution_vc11\BinD_Unicode_x64（debug版）中的supermap.xml文件中的<CurrentCulture>标签可替换菜单显示语言（中文/英文）。

插件功能：
1.将3dsmax场景中未隐藏的Node分别导出为一个S3MB文件；
2.将3dsmax场景中未隐藏的Node导出到UDB中。