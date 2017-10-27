# CustomTitleBar
一款项目中常用的标题样式
# CustomTitileBar
通用Android标题栏控件


## 主要功能：
- 支持左、右按钮
- 支持按钮点击背景
- 支持自定义左右按钮图片、文字样式及标题文字样式


## 效果图

![1](https://github.com/xiaohaibin/CustomTitileBar/blob/master/screenshot/gif.gif)

## 基本使用

 [ ![Download](https://api.bintray.com/packages/jxnk25/maven/CommonTitleBar/images/download.svg) ](https://bintray.com/jxnk25/maven/CommonTitleBar/_latestVersion)

#### 1.添加Gradle依赖

```
dependencies {
    compile 'compile 'com.xhb:commontitlebar:latestVersion'//将latestVersion替换成上面最新的版本号
}
```

#### 2.在布局文件中添加

```
    <com.stx.xhb.commontitlebar.CustomTitlebar
        android:id="@+id/title3"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:title_text="标题"
        app:left_button_image="@mipmap/icon_back"
        app:title_textSize="14sp"
        app:right_button_image="@mipmap/img_currency_selected"/>
```


#### 3.在Activity或者Fragment中配置

```
        CustomTitlebar customTitlebar2 = (CustomTitlebar) findViewById(R.id.title2);
        customTitlebar2.setAction(new CustomTitlebar.TitleBarOnClickListener() {
            @Override
            public void performAction(View view) {
                switch (view.getId()){
                    case R.id.iv_left:
                        Toast.makeText(MainActivity.this, "左边图片按钮", Toast.LENGTH_SHORT).show();
                        break;
                    case R.id.tv_right:
                        Toast.makeText(MainActivity.this, "右边文字按钮", Toast.LENGTH_SHORT).show();
                        break;
                }
            }
        });

```


## 自定义属性说明

| 属性名 | 属性说明 | 属性值 | 
| ------------ | ------------- | ------------ |
| title_background| 标题栏背景色 | color，默认为white |
| left_button_image| 左边图片按钮背景 | reference ，不设置则不显示|
| left_button_text| 左边文字按钮内容 |string |
| left_button_textColor| 左边文字按钮文字颜色 | color，默认为Color.GRAY |
| left_button_textSize| 左边文字按钮文字大小 | dimension，默认为14sp |
| title_text| 标题文字内容 | string |
| title_textColor| 标题文字颜色 |color，默认为Color.GRAY |
| title_textSize| 标题文字大小| dimension，默认为14sp |
| right_button_image| 右边图片按钮背景 |reference  ，不设置则不显示|
| right_button_text| 右边文字按钮内容 | string |
| right_button_textColor| 右边文字颜色 | color，默认为Color.GRAY |
| right_button_textSize| 右边文字大小 | dimension，默认为14sp |
| show_line| 是否显示顶部分割线 | booleanT类型，默认显示 |

## 关于我
个人邮箱：yanjiabin159357@163.com
[GitHub主页](https://github.com/yanjiabin)
[个人博客](http://blog.csdn.net/yanjiabin159357)



    
#如果喜欢，还请statr&Fork&follow进行支持，谢谢O(∩_∩)O~。#
