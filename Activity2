package com.example.exercise4;

import android.app.Activity;
import android.os.Bundle;
import android.util.Log;
import android.widget.TextView;

public class Activity_2 extends Activity {

	@Override
	protected void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		setContentView(R.layout.activity_2);
		
		
		Bundle extras = this.getIntent().getExtras();
		String gender = extras.getString("gender");
		String weight = extras.getString("weight");
		String heightFeet = extras.getString("heightFeet");
		String heightInches = extras.getString("heightInches");
		if (extras != null){
			Log.v("myApp","gender="+ gender);
			Log.v("myApp", heightFeet);
			Log.v("myApp", heightInches);
			Log.v("myApp", weight);
		
		TextView response1 = (TextView) findViewById(R.id.response1);
		response1.setText("You are a " + gender);
		TextView response2 = (TextView) findViewById(R.id.response2);
		response2.setText("Your Height is " + heightFeet +"'"  + heightInches + "''");
		TextView response3 = (TextView) findViewById(R.id.response3);
		response3.setText("Your Standard Weight is " + weight + " Kg");
		}
				
	}
}
