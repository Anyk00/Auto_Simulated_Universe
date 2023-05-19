# Auto_Simulated_Universe
星穹铁道-模拟宇宙全自动化

有一定的断点回复功能，你可以切出去做其他事，切回来会继续自动化。

目前只支持模拟宇宙6，地图数据基本录完了

----------------------------------------------------------------------------------------------

### 用法

**第一次运行**
双击install_requirements.bat安装依赖库

进入游戏，将人物传送到黑塔的办公室，然后双击 **校准.bat** 等待视角转换结束

**运行脚本**

人物靠近模拟宇宙（出现f键交互条）

双击run.bat 或者 管理员权限运行 <pre><code>python states.py --find=1
</code></pre>

只支持1920\*1080(窗口化或全屏幕)，关闭“沿用自动战斗设置”，关闭HDR。

info.txt中保存了模拟宇宙开局选的角色，1表示第一个角色。最好在一号位选远程角色（艾丝妲、三月七）方便开怪。

----------------------------------------------------------------------------------------------

### 部分逻辑

选祝福的逻辑是硬选巡猎，事件基本都会跳过，最后一层不会强化祝福，奇物随机选。

寻路模块基于小地图，所以跑图的时候会低头保持小地图不受高亮的天空干扰

小地图中只会识别白色边缘线和黄色交互点。

----------------------------------------------------------------------------------------------

支持增加地图，具体方法为

进入新图，然后运行 python states.py --find=0

注意，一开始的状态必须是刚进图、视角也没有改变的状态

几秒后角色会后退，然后前进。在角色前进时，你可以移动鼠标改变视角。

在地图中绕一圈，感觉差不多就ctrl+c结束进程能得到地图数据了。保存在imgs/maps/xxxxx目录下（可以按修改时间排序）

最好保持低头状态，减少高亮天空的干扰。

有怪的图最好用希儿战技，被锁定会影响小地图识别。

小地图上表示人物视角的淡蓝色扇形（探照灯）也会影响小地图白色边缘线的识别。因此尽量让探照灯少照射到白色边缘。

imgs/maps/xxxxx目录下会存在target.jpg，你可以用windows自带的画图打开它，然后在上面标记点（可以参考其它地图文件中的target.jpg）

靛蓝色：路径点 黄色：终点 绿色：交互点（问号点） 红色：怪点

----------------------------------------------------------------------------------------------

欢迎加入，欢迎反馈bug，QQ群：831830526
