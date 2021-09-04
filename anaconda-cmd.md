<div id="cnblogs_post_body" class="blogpost-body blogpost-body-html">
<p>首先说一点：Windows下 Anaconda Prompt 这个东西就是用来管理Anaconda的，使用的是conda这样的一种命令<br>在Linux中，可以直接在终端中输入conda 命令</p>
<p>可以使用conda命令创建新的python环境（python版本，包），新的环境与原来的环境不相关。这样，方便不同的应用中使用不同的python版本。<br>创建新环境的步骤如下：<br>1、首先在所在系统中安装Anaconda。可以打开命令行输入conda -V检验是否安装以及当前conda的版本。</p>
<p>2、conda常用的命令。</p>
<p>&nbsp; &nbsp; 1）&nbsp;<span class="cnblogs_code">conda list</span>&nbsp; 查看安装了哪些包。</p>
<p>&nbsp; &nbsp; 2）&nbsp;<span class="cnblogs_code">conda <span style="color: rgb(0, 0, 255); background-color: rgb(246, 248, 250);">env</span> list</span>&nbsp; 或 &nbsp;<span class="cnblogs_code">conda <span style="color: rgb(0, 0, 255); background-color: rgb(246, 248, 250);">info</span> -e </span>&nbsp;查看当前存在哪些虚拟环境</p>
<p>&nbsp; &nbsp; 3）&nbsp;<span class="cnblogs_code">conda update conda</span>&nbsp; 检查更新当前conda</p>
<p>&nbsp; &nbsp; 4）&nbsp;<span class="cnblogs_code">conda --version </span>&nbsp;查询conda版本</p>
<p>&nbsp; &nbsp; 5）&nbsp;<span class="cnblogs_code">conda -h</span>&nbsp; 查询conda的命令使用</p>
<p>3、创建python虚拟环境。</p>
<p>&nbsp; &nbsp; &nbsp;使用 &nbsp;<span class="cnblogs_code">conda create -n your_env_name python=X.X</span>&nbsp;（2.7、3.6等)命令创建python版本为X.X、名字为your_env_name的虚拟环境。your_env_name文件可以在Anaconda安装目录envs文件下找到。</p>
<p>&nbsp; &nbsp; &nbsp;注意：默认的情况下只安装了一些必须的包，并不会像我们安装anaconda时自动安装很多常用的包。要实现上面的功能，则须在末尾加上‘anaconda’，完整命令是：</p>
<div class="cnblogs_code">
<code-box id="EHK77mJm" style="position: relative;display: block;"><button code-id="EHK77mJm" type="button" class="clipboard" data-clipboard-action="copy" data-clipboard-target="pre[code-id=EHK77mJm]" aria-label="复制代码" style="position: absolute; top: 8px; right: 23px; display: flex; justify-content: center; align-items: center; width: 30px; height: 25px; cursor: pointer; font-size: 14px; padding: 0px 0px 0px 2px; border: none; border-radius: 6px; color: rgb(153, 153, 153); opacity: 0; visibility: hidden; background-color: rgba(230, 230, 230, 0.2); user-select: none; transition: opacity 0.2s ease-in-out 0s, visibility 0.2s ease-in-out 0s; z-index: 1;"><i class="iconfont icon-fuzhi1"></i></button><pre style="background-color: rgb(246, 248, 250); overflow: visible; position: relative;" code-id="EHK77mJm" class="mCustomScrollbar _mCS_1 mCS-autoHide mCS_no_scrollbar"><div id="mCSB_1" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_1_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y mCS_x_hidden mCS_no_scrollbar_x" style="position: relative; top: 0px; left: 0px; width: 100%;" dir="ltr">conda create -n your_env_name python=X.X anaconda</div></div><div id="mCSB_1_scrollbar_vertical" class="mCSB_scrollTools mCSB_1_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_1_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px;"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_1_scrollbar_horizontal" class="mCSB_scrollTools mCSB_1_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_1_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; width: 0px; left: 0px;"><div class="mCSB_dragger_bar"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
</div>
<p>4、使用激活(或切换不同python版本)的虚拟环境。</p>
<p>&nbsp; &nbsp; 打开命令行输入python --version可以检查当前python的版本。</p>
<p>&nbsp; &nbsp; 使用如下命令即可&nbsp;激活你的虚拟环境(即将python的版本改变)。</p>
<p>&nbsp; &nbsp; Linux:&nbsp; &nbsp;<span class="cnblogs_code">source activate your_env_name</span>&nbsp;(虚拟环境名称)</p>
<p>&nbsp; &nbsp; Windows: &nbsp;<span class="cnblogs_code">activate your_env_name</span>&nbsp;(虚拟环境名称)</p>
<p>&nbsp; &nbsp;这是再使用&nbsp;&nbsp;<span class="cnblogs_code">python --version</span>&nbsp;可以检查当前python版本是否为想要的。</p>
<p>5、对虚拟环境中安装额外的包。</p>
<p>&nbsp; &nbsp; 使用命令&nbsp;<span class="cnblogs_code">conda <span style="color: rgb(0, 0, 255); background-color: rgb(246, 248, 250);">install</span> -n your_env_name [package]</span>&nbsp;即可安装package到your_env_name中</p>
<p>6、关闭虚拟环境(即从当前环境退出返回使用PATH环境中的默认python版本)。</p>
<p>&nbsp; &nbsp;使用如下命令即可。</p>
<div class="cnblogs_code">
<code-box id="MxsBrtcS" style="position: relative;display: block;"><button code-id="MxsBrtcS" type="button" class="clipboard" data-clipboard-action="copy" data-clipboard-target="pre[code-id=MxsBrtcS]" aria-label="复制代码" style="position: absolute; top: 8px; right: 23px; display: flex; justify-content: center; align-items: center; width: 30px; height: 25px; cursor: pointer; font-size: 14px; padding: 0px 0px 0px 2px; border: none; border-radius: 6px; color: rgb(153, 153, 153); opacity: 0; visibility: hidden; background-color: rgba(230, 230, 230, 0.2); user-select: none; transition: opacity 0.2s ease-in-out 0s, visibility 0.2s ease-in-out 0s; z-index: 1;"><i class="iconfont icon-fuzhi1"></i></button><pre style="background-color: rgb(246, 248, 250); overflow: visible; position: relative;" code-id="MxsBrtcS" class="mCustomScrollbar _mCS_2 mCS-autoHide mCS_no_scrollbar"><div id="mCSB_2" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_2_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y mCS_x_hidden mCS_no_scrollbar_x" style="position: relative; top: 0px; left: 0px; width: 100%;" dir="ltr"><span style="color: rgb(0, 0, 0); background-color: rgb(246, 248, 250);">   Linux: source deactivate


<p>7、删除虚拟环境。</p>
<p>&nbsp; &nbsp;使用命令&nbsp;<span class="cnblogs_code">conda remove -n your_env_name(虚拟环境名称) --all</span>&nbsp;， 即可删除。</p>
<p>8、删除环境中的某个包。</p>
<p>&nbsp; &nbsp;使用命令&nbsp;<span class="cnblogs_code">conda remove --name your_env_name package_name</span>&nbsp; 即可。</p>
