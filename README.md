```java
private void onScaleAnimationBySpringWayOne(){
//        ScaleAnimation animation =new ScaleAnimation(1.0f,1.8f,1.0f,1.8f);
//        animation.setDuration(1000);
//        animation.setInterpolator(new SpringScaleInterpolator(0.4f));
//        imageView.startAnimation(animation);
        ObjectAnimator animatorX = ObjectAnimator.ofFloat(imageView,"scaleX",1.0f,1.8f);
        ObjectAnimator animatorY = ObjectAnimator.ofFloat(imageView,"scaleY",1.0f,1.8f);
        AnimatorSet set =new AnimatorSet();
        set.setDuration(1000);
        set.setInterpolator(new SpringScaleInterpolator(0.4f));
        set.playTogether(animatorX,animatorY);
        set.start();

    }
```
