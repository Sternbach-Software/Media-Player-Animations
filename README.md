# MediaPlayerAnimations
A repository of XML animations relevant to media players (e.g. rewind, fast-forward, play/pause, etc.). I struggled to find these online until I decided to make my own.

##Play/Pause


![LibVLC stack](https://images.videolan.org/images/libvlc_stack.png)


Credits: https://github.com/videolan/vlc-android

###/drawable/anim_play_pause.xml

```
<animated-vector xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:aapt="http://schemas.android.com/aapt">
    <aapt:attr name="android:drawable">
        <vector
                android:name="vector"
                android:width="48dp"
                android:height="48dp"
                android:viewportWidth="48"
                android:viewportHeight="48">
            <path
                    android:pathData="m24,4c-11.04,0 -20,8.96 -20,20 0,11.04 8.96,20 20,20 11.04,0 20,-8.96 20,-20 0,-11.04 -8.96,-20 -20,-20zM24,41.5c-9.647,0 -17.5,-7.853 -17.5,-17.5 0,-9.647 7.853,-17.5 17.5,-17.5 9.647,0 17.5,7.853 17.5,17.5 0,9.647 -7.853,17.5 -17.5,17.5z"
                    android:fillColor="?attr/colorOnSurface"/>

            <group
                    android:name="group"
                    android:pivotX="24"
                    android:pivotY="24">
                <path
                        android:name="path"
                        android:pathData="m25.7287,30.6573 l-0.1473,-13.3232 3.3728,-0.0373 0.0843,13.3239 -3.3098,0.0366m-6.8299,-13.2493 l3.3718,-0.0373 0.1483,13.3232 -3.3108,0.0356 -0.2093,-13.3215m5.1896,14.5915"
                        android:fillColor="?attr/colorOnSurface"/>
            </group>
        </vector>
    </aapt:attr>
    <target android:name="group">
        <aapt:attr name="android:animation">
            <objectAnimator
                    android:duration="300"
                    android:interpolator="@android:interpolator/fast_out_slow_in"
                    android:propertyName="rotation"
                    android:valueFrom="0"
                    android:valueTo="90"
                    android:valueType="floatType" />
        </aapt:attr>
    </target>
    <target android:name="path">
        <aapt:attr name="android:animation">
            <objectAnimator
                    android:duration="300"
                    android:interpolator="@android:interpolator/fast_out_slow_in"
                    android:propertyName="pathData"
                    android:valueFrom="M 32 24 L 20 24.074 L 20 15 L 32 24 L 32 24 M 20 33 L 20 24.074 L 32 24 L 31.783 24.162 L 20 33 M 32 24 L 32 24 L 32 24"
                    android:valueTo="M 30.667 22.333 L 17.333 22.333 L 17.333 19 L 30.667 19 L 30.667 22.333 M 17.333 29 L 17.333 25.667 L 30.667 25.667 L 30.667 29 L 17.333 29 M 32 24 L 32 24 L 32 24"
                    android:valueType="pathType" />
        </aapt:attr>
    </target>
</animated-vector>
```


###/drawable/anim_pause_play.xml

```
<animated-vector xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:aapt="http://schemas.android.com/aapt">
    <aapt:attr name="android:drawable">
        <vector
                android:name="vector"
                android:width="48dp"
                android:height="48dp"
                android:viewportWidth="48"
                android:viewportHeight="48">
            <path
                    android:name="path_2"
                    android:fillColor="?attr/colorOnSurface"
                    android:pathData="M 24 4 C 12.96 4 4 12.96 4 24 C 4 35.04 12.96 44 24 44 C 35.04 44 44 35.04 44 24 C 44 12.96 35.04 4 24 4 Z M 24 41.5 C 14.353 41.5 6.5 33.647 6.5 24 C 6.5 14.353 14.353 6.5 24 6.5 C 33.647 6.5 41.5 14.353 41.5 24 C 41.5 33.647 33.647 41.5 24 41.5 Z"
                    android:strokeWidth="1" />
            <group
                    android:name="group"
                    android:pivotX="24"
                    android:pivotY="24">
                <path
                        android:name="path"
                        android:pathData="M 32 24 L 20 24.074 L 20 15 L 32 24 L 32 24 M 20 33 L 20 24.074 L 32 24 L 31.783 24.162 L 20 33 M 32 24 L 32 24 L 32 24"
                        android:fillColor="?attr/colorOnSurface"
                        android:strokeWidth="1" />
            </group>
        </vector>
    </aapt:attr>
    <target android:name="group">
        <aapt:attr name="android:animation">
            <objectAnimator
                    android:duration="300"
                    android:interpolator="@android:interpolator/fast_out_slow_in"
                    android:propertyName="rotation"
                    android:valueFrom="90"
                    android:valueTo="0"
                    android:valueType="floatType" />
        </aapt:attr>
    </target>
    <target android:name="path">
        <aapt:attr name="android:animation">
            <objectAnimator
                    android:duration="300"
                    android:interpolator="@android:interpolator/fast_out_slow_in"
                    android:propertyName="pathData"
                    android:valueFrom="M 30.667 22.333 L 17.333 22.333 L 17.333 19 L 30.667 19 L 30.667 22.333 M 17.333 29 L 17.333 25.667 L 30.667 25.667 L 30.667 29 L 17.333 29 M 32 24 L 32 24 L 32 24"
                    android:valueTo="M 32 24 L 20 24.074 L 20 15 L 32 24 L 32 24 M 20 33 L 20 24.074 L 32 24 L 31.783 24.162 L 20 33 M 32 24 L 32 24 L 32 24"
                    android:valueType="pathType" />
        </aapt:attr>
    </target>
</animated-vector>
```

###Kotlin

```
        val playToPause = AnimatedVectorDrawableCompat.create(this, R.drawable.anim_play_pause)!!
        val pauseToPlay = AnimatedVectorDrawableCompat.create(this, R.drawable.anim_pause_play)!!
        var playing = false
        findViewById<ImageView>(R.id.play_icon).setOnClickListener {
            val drawable = if (playing) playToPause else pauseToPlay
            (it as ImageView).setImageDrawable(drawable)
            it.post { drawable.start() }
            playing = !playing
        }
```

##Rewind

![LibVLC stack](https://images.videolan.org/images/libvlc_stack.png)

##Fast-forward

![LibVLC stack](https://images.videolan.org/images/libvlc_stack.png)
