##note：

### 一、简要说明
android:windowSoftInputMode用于设置当前activity主窗口与软键盘的交互模式，可以用来避免输入法面板遮挡问题。 
这个属性能影响两件事情： 

* 【一】当有焦点产生时，软键盘是隐藏还是显示 
* 【二】是否减少活动主窗口大小以便腾出空间放软键盘 

它的设置必须是下面列表中的一个值，或一个”state…”值加一个”adjust…”值的组合。各个值之间用|分开，例如：

	android:windowSoftInputMode="stateHidden|adjustResize"

### 二、常见用法，进activity时默认不弹起
进入新 Activity界面，想阻止软键盘自动弹出，只要在 AndroidManifest.xml 中对应的Activity下设置
    
    android:windowSoftInputMode="adjustUnspecified|stateHidden"

### 三、常见用法，键盘顶起布局显示

    android:windowSoftInputMode="adjustPan|stateHidden"

### 键盘跟布局的关系
键盘

### windowSoftInputMode各值得含义
1. stateUnspecified：软键盘的状态并没有指定，系统将选择一个合适的状态或依赖于主题的设置 
* stateUnchanged：当这个activity出现时，软键盘将一直保持在上一个activity里的状态，无论是隐藏还是显示 
* stateHidden：用户选择activity时，软键盘总是被隐藏 
* stateAlwaysHidden：当该Activity主窗口获取焦点时，软键盘也总是被隐藏的 
* stateVisible：软键盘通常是可见的 
* stateAlwaysVisible：用户选择activity时，软键盘总是显示的状态 
* adjustUnspecified：默认设置，通常由系统自行决定是隐藏还是显示 
* adjustResize：该Activity总是调整屏幕的大小以便留出软键盘的空间 
* adjustPan：当前窗口的内容将自动移动以便当前焦点从不被键盘覆盖和用户能总是看到输入内容的部分

##question：

##extention：


##reference: