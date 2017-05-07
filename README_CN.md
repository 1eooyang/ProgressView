# ProgressView

ProgressView��һ���̳�Progressbar�Ľ�����ͼ��Ŀǰʵ���˴����ֽ��ȵ�ˮƽ�������Լ�Բ�ν�������Բ�ν������������ַ����ͨ���ν��ȣ��ڲ���ֱ�������Լ��ڲ����������ȡ�

## Demo
![demo](https://github.com/WhiteDG/ProgressView/blob/master/screenshot/demo.gif)


## ����

��build.gradle�������������
```
dependencies {
    compile 'com.white:progressview:1.0.0'
}
```

## ʹ��

1. �����ļ�

�ڲ����ļ������ProgressView����������Զ�������
```
// ˮƽ������
<com.white.progressview.HorizontalProgressView
    android:id="@+id/progress100"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:padding="10dp"
    android:progress="100"
    app:progressReachColor="@color/colorPrimary"
    app:progressTextColor="@color/colorPrimary"
    app:progressTextVisible="true"
    />
    
// Բ�ν�����
<com.white.progressview.CircleProgressView
      android:id="@+id/circle_progress_normal"
      android:layout_width="0dp"
      android:layout_height="wrap_content"
      android:layout_weight="1"
      android:padding="10dp"
      android:progress="68"
      app:progressNormalSize="4dp"
      app:progressReachSize="4dp"
      app:progressStyle="Normal"
      app:radius="28dp"
      />
```
2. Java����

����ͨ����������������ص��Զ�������
```
horizontalProgressView.setXXXX();
// ����:
horizontalProgressView.setTextVisible(false);
horizontalProgressView.setReachBarSize(4);
horizontalProgressView.setProgressPosition(HorizontalProgressView.TOP);
...
```
Ҳ�������ý��ȶ�����ָ������ʱ��
```
HorizontalProgressView horizontalProgressView = (HorizontalProgressView) findViewById(R.id.progress100);
// ��0��100ִ��2500ms�Ķ��� 
horizontalProgressView.setProgressInTime(100,2500);
// ��20��100ִ��2500ms�Ķ��� 
horizontalProgressView.setProgressInTime(0,100,2500);
// ��0����ǰ����ִ��2500ms�Ķ��� 
horizontalProgressView.runProgressAnim(2500);

CircleProgressView circleProgressView = (CircleProgressView) findViewById(R.id.circle_progress_normal);
...
// ��HorizontalProgressViewһ���ķ���
circleProgressView.setProgressInTime(100,2500);
    
```

## ����������

#### HorizontalProgressView

������ | ����˵��
---|---
progressNormalColor | ��������״̬�½�������ɫ
progressReachColor | �����ѵ���Ľ�������ɫ
progressTextColor | ���ý����ı���ɫ
progressTextSize | ���ý����ı���С
progressTextOffset | ���ý����ı���������ı߾�
progressNormalSize | ��������״̬�½�������С
progressReachSize | �����ѵ���Ľ�������С
progressTextPosition | ���ý����ı�λ��(CENTER/BOTTOM/TOP)(����/�ײ�/����)
progressTextVisible | �����Ƿ���ʾ�����ı�
progressTextSkewX | ���ý����ı���б�Ƕ�(б��)
progressTextPrefix | ���ý����ı�ǰ׺
progressTextSuffix | ���ý����ı���׺(Ĭ����%)
#### CircleProgressView

������ | ����˵��
---|---
progressNormalColor | ��������״̬�½�������ɫ
progressReachColor | �����ѵ���Ľ�������ɫ
progressTextColor | ���ý����ı���ɫ
progressTextSize | ���ý����ı���С
progressTextOffset | ���ý����ı���������ı߾�
progressNormalSize | ��������״̬�½�������С
progressReachSize | �����ѵ���Ľ�������С
radius | ����Բ�ΰ뾶
progressTextVisible | �����Ƿ���ʾ�����ı�
progressTextSkewX | ���ý����ı���б�Ƕ�(б��)
progressTextPrefix | ���ý����ı�ǰ׺
progressTextSuffix | ���ý����ı���׺(Ĭ����%)
progressStartArc | ���ý���ֵ��ʼ�Ƕ�
progressStyle | ����Բ�ν�����ʽ(Normal/FillInner/FillInnerArc)(��ͨ����/�ڲ���ֱ���/�ڲ��������)
reachCapRound | ���ý��ȱ߽��Ƿ�ʹ��Բ��(ʹ��Normal��ʽʱ����)
innerBackgroundColor | �����ڲ�������ɫ(ʹ��Normal��ʽʱ����)
innerProgressColor | �����ڲ�������ɫ(ʹ��FillInner��ʽʱ����)
innerPadding | �����ڲ�Բ���ⲿԲ�ļ��(ʹ��FillInnerArc��ʽʱ����)
outerColor | �����ⲿԲ����ɫ(ʹ��FillInnerArc��ʽʱ����)
outerSize | �����ⲿԲ����С(ʹ��FillInnerArc��ʽʱ����)

