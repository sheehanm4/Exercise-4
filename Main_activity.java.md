# Exercise-4
package com.example.exercise4;


import android.app.Activity;
import android.content.Intent;
import android.os.Bundle;
import android.util.Log;
import android.view.Menu;
import android.view.MenuItem;
import android.view.View;
import android.view.View.OnClickListener;
import android.widget.Button;
import android.widget.CheckBox;
import android.widget.CompoundButton;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends Activity {

	@Override
	public void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		setContentView(R.layout.activity_main); 
		CheckBox checkbox1 = (CheckBox)findViewById(R.id.checkBox1);		
		CheckBox checkbox2 = (CheckBox)findViewById(R.id.checkBox2);
		Button button1 = (Button)findViewById(R.id.button1);
		button1.setOnClickListener(new View.OnClickListener(){	
		double factor = 45.5;
			
			public void onClick(View v) {
					EditText feet = (EditText) findViewById(R.id.editText02);
					String value1 = feet.getText().toString();
					EditText inches = (EditText) findViewById(R.id.editText01);
					String value2 = inches.getText().toString();
					double feet1 = Integer.parseInt(value1);
					double inches1 = Integer.parseInt(value2);
					double totalHeight = (feet1*12)+ inches1; 
					double idealWeight = (factor + (2.3 * (totalHeight-60)));
					String answer = Double.toString(idealWeight);
					Log.v("myApp", answer);
					Intent intent1 = new Intent();
					intent1.setClass(MainActivity.this,Activity_2.class);
					Bundle bundle1 = new Bundle();
					bundle1.putString("gender", "Male");
					bundle1.putString("heightFeet",value1);
					bundle1.putString("heightInches",value2);
					bundle1.putString("weight",answer);
					intent1.putExtras(bundle1);
					startActivity(intent1);	
					Log.v("myApp","my intent started");
			}	
		
	});
}}
