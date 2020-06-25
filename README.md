아무리 commit, pull,push해도 페이지가 업로드가 안되, 이렇게라도 올려요..ㅠㅠ
리뷰와 별점주는 코드입니다

게임추천앱
package com.jiyun.mm;

import android.app.Activity;
import android.os.Bundle;
import android.widget.RatingBar;
import android.widget.RatingBar.OnRatingBarChangeListener;
import android.widget.TextView;

public class MainActivity extends Activity {

    RatingBar rating;
    TextView tv01;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        rating = (RatingBar) findViewById(R.id.ratingBar1);
        tv01 = (TextView) findViewById(R.id.tv01);

        rating.setStepSize((float) 0.5);
        rating.setRating((float) 2.5);
        rating.setIsIndicator(false);

        rating.setOnRatingBarChangeListener(new OnRatingBarChangeListener() {

            @Override
            public void onRatingChanged(RatingBar ratingBar, float rating,
                                        boolean fromUser) {
                tv01.setText("평점 : " + rating);

            }
        });

    }

}

