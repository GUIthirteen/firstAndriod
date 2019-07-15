# firstAndriod
first Android just for test
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity implements View.OnClickListener{
    private TextView mTextView;
    //快捷键倒包 alt+enter
    private Button mButton;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        mTextView=findViewById(R.id.TextView);
        mButton=findViewById(R.id.Button);
        //R文件 所有项目资源文件，完全不需要手动更改
        //存储数据的方式都是以int类型保存
        //实现监听第一步，先实现view.onclicklistener接口并
        //第二部：给控制设置监听 this代表当前activity
        mButton.setOnClickListener(this);
    }

    @Override
    public void onClick(View view) {
        mTextView.setText("LSF");
    }
}
