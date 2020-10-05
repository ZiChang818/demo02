# demo02
实验内容：根据图片要求，完成Android布局

实验步骤：

1、线性布局实验

代码：

```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
 android:orientation="vertical" android:layout_width="match_parent"
 android:layout_height="match_parent"
 >
 <!--父标签设置为垂直布局-->
 <LinearLayout
     android:layout_width="match_parent"
     android:layout_height="wrap_content"
     android:orientation="horizontal">
     <!--子标签设置为水平布局-->
     <Button
         android:id="@+id/button1"
         android:layout_width="wrap_content"
         android:layout_height="wrap_content"
         android:text="@string/button1" />
...
```

设置两个 LinearLayout ，第一个 LinearLayout 作为父标签，第二个 LinearLayout 作为子标签，子标签在父标签内。父标签设置为垂直布局，子标签设置为水平布局。结构如下：

```
<LinearLayout ...>
	<LinearLayout ...>
		...
	</LinearLayout>
</LinearLayout>
```

Strings配置

```
    <string name="button11_name">one_one</string>
    <string name="button12_name">one_two</string>
    <string name="button13_name">one_three</string>
    <string name="button14_name">one_four</string>
    <string name="button21_name">two_one</string>
    <string name="button22_name">two_two</string>
    <string name="button23_name">two_three</string>
    <string name="button24_name">two_four</string>
    <string name="button31_name">three_one</string>
    <string name="button32_name">three_two</string>
    <string name="button33_name">three_three</string>
    <string name="button34_name">three_four</string>
    <string name="button41_name">four_one</string>
    <string name="button42_name">four_two</string>
    <string name="button43_name">four_three</string>
    <string name="button44_name">four_four</string>
```

运行结果：

1、线性布局浏览

![imag]()

2、线性布局运行

![imag]()



2、约束布局实验

代码：

```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <TextView
        android:id="@+id/textView4"
        android:layout_width="60dp"
        android:layout_height="40dp"
        android:background="#F80707"
        android:gravity="center"
        android:text="red"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView5"

        android:layout_width="60dp"
        android:layout_height="40dp"

        android:background="#FF9800"
        android:gravity="center"
        android:text="orange"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.0" />

    <TextView
        android:id="@+id/textView6"
        android:layout_width="60dp"
        android:layout_height="40dp"
        android:background="#FFEB3B"
        android:gravity="center"
        android:text="yellow"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView7"
        android:layout_width="60dp"
        android:layout_height="40dp"
        android:layout_marginTop="280dp"
        android:background="#2196F3"
        android:gravity="center"
        android:text="blue"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView8"
        android:layout_width="60dp"
        android:layout_height="40dp"
        android:layout_marginStart="60dp"
        android:layout_marginTop="280dp"
        android:background="#85F107"
        android:gravity="center"
        android:text="green"
        app:layout_constraintEnd_toStartOf="@+id/textView7"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView9"
        android:layout_width="60dp"
        android:layout_height="40dp"
        android:layout_marginTop="280dp"
        android:layout_marginEnd="60dp"
        android:background="#673AB7"
        android:gravity="center"
        android:text="indgio"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toEndOf="@+id/textView7"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView10"
        android:layout_width="0dp"
        android:layout_height="40dp"
        android:background="#D806FB"
        android:gravity="center"
        android:text="violet"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView7"
        app:layout_constraintVertical_bias="0.544" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

1、约束布局浏览

![imag]()

2、约束布局运行

![imag]()



3、表格布局实验

代码：

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent">
    <TableLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:shrinkColumns="0">
        <Button
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:text="open...                                                                   ctrl+o"
            android:gravity="left"

            >

        </Button>
        <Button
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:text="save...                                                                    ctrl+s"
            android:gravity="left"
            android:layout_marginTop="-11dp"
            >

        </Button>
        <Button
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:text="save As...                                                           ctrl+shift+s"
            android:gravity="left"
            android:layout_marginTop="-11dp"
            >

        </Button>
        <View  android:layout_height="2px"
            android:layout_width="match_parent"
            android:background="#000000"
            android:layout_marginTop="-3dp"
            ></View>
        <Button
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:text="Import..."
            android:gravity="left"
            android:layout_marginTop="-4dp"
            >
        </Button>
        <Button
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:text="Export...                                                                  ctrl+e"
            android:gravity="left"
            android:layout_marginTop="-11dp"
            >
        </Button>
        <View  android:layout_height="2px"
            android:layout_width="match_parent"
            android:background="#000000"
            android:layout_marginTop="-3dp"
            ></View>
        <Button
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:text="quilt..."
            android:gravity="left"
            android:layout_marginTop="-4dp"
            >
        </Button>
    </TableLayout>
</LinearLayout>
```

1、表格布局浏览

![image]()

2、表格布局运行

![image]()
