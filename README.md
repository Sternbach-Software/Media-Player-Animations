# Media-Player-Animations
A repository of XML animations relevant to media players (e.g. rewind, fast-forward, play/pause, etc.). I struggled to find these online until I decided to make my own.


- [Play/Pause](#play-pause)
- [Rewind](#rewind)
- [Fast-forward](#fast-forward)

## Play/Pause


![GIF](https://github.com/shmueldabomb441/MediaPlayerAnimations/blob/01660fb905f98a10f699ab8a40aa73c360d3616e/play_pause.gif)


Credits: https://github.com/videolan/vlc-android

### /drawable/anim_play_pause.xml

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


### /drawable/anim_pause_play.xml

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

### Kotlin

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

## Rewind

![GIF](https://github.com/shmueldabomb441/MediaPlayerAnimations/blob/4301ea88b7718a28e6482bf8ad61d7cc8b81a7cd/rewind_gif.gif)


You can change how far it rotates by editing the `toValue`. You can change the icon that rotates to a different icon (with a different interval) without changing the animation by just swapping out the `android:drawable="@drawable/ic_rewind"` value in `anim_rewind.xml` and adding the `group` tag to the new icon in the same place as it is in `ic_rewind.xml`.

### /drawable/ic_rewind.xml

```
<vector android:height="48dp" android:tint="#000000"
    android:viewportHeight="24" android:viewportWidth="24"
    android:width="48dp" xmlns:android="http://schemas.android.com/apk/res/android">

	<group
		android:name="rotationGroup"
		android:pivotX="12"
		android:pivotY="13">
	<path android:fillColor="@android:color/white" android:pathData="M11.99,5V1l-5,5l5,5V7c3.31,0 6,2.69 6,6s-2.69,6 -6,6s-6,-2.69 -6,-6h-2c0,4.42 3.58,8 8,8s8,-3.58 8,-8S16.41,5 11.99,5z"/>
	</group>
	<path android:fillColor="@android:color/white" android:pathData="M10.89,16h-0.85v-3.26l-1.01,0.31v-0.69l1.77,-0.63h0.09V16z"/>
    <path android:fillColor="@android:color/white" android:pathData="M15.17,14.24c0,0.32 -0.03,0.6 -0.1,0.82s-0.17,0.42 -0.29,0.57s-0.28,0.26 -0.45,0.33s-0.37,0.1 -0.59,0.1s-0.41,-0.03 -0.59,-0.1s-0.33,-0.18 -0.46,-0.33s-0.23,-0.34 -0.3,-0.57s-0.11,-0.5 -0.11,-0.82V13.5c0,-0.32 0.03,-0.6 0.1,-0.82s0.17,-0.42 0.29,-0.57s0.28,-0.26 0.45,-0.33s0.37,-0.1 0.59,-0.1s0.41,0.03 0.59,0.1c0.18,0.07 0.33,0.18 0.46,0.33s0.23,0.34 0.3,0.57s0.11,0.5 0.11,0.82V14.24zM14.32,13.38c0,-0.19 -0.01,-0.35 -0.04,-0.48s-0.07,-0.23 -0.12,-0.31s-0.11,-0.14 -0.19,-0.17s-0.16,-0.05 -0.25,-0.05s-0.18,0.02 -0.25,0.05s-0.14,0.09 -0.19,0.17s-0.09,0.18 -0.12,0.31s-0.04,0.29 -0.04,0.48v0.97c0,0.19 0.01,0.35 0.04,0.48s0.07,0.24 0.12,0.32s0.11,0.14 0.19,0.17s0.16,0.05 0.25,0.05s0.18,-0.02 0.25,-0.05s0.14,-0.09 0.19,-0.17s0.09,-0.19 0.11,-0.32s0.04,-0.29 0.04,-0.48V13.38z"/>
</vector>
```

### /animator/animator_rewind.xml

```
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="http://schemas.android.com/apk/res/android">
	<objectAnimator
		android:duration="200"
		android:propertyName="rotation"
		android:valueFrom="360"
		android:valueTo="315"
		android:repeatMode="reverse"
		android:repeatCount="1"
		/>
</set>
```

### /drawable/anim_rewind.xml

```
<?xml version="1.0" encoding="utf-8"?>
<animated-vector xmlns:android="http://schemas.android.com/apk/res/android"
	android:drawable="@drawable/ic_rewind" >
	<target
		android:name="rotationGroup"
		android:animation="@animator/animator_rewind" />
</animated-vector>
```

### Kotlin

```
        val rewindAnim = AnimatedVectorDrawableCompat.create(this, R.drawable.anim_rewind)!!
        rewindButtonImageView.setImageDrawable(rewindAnim)
        rewindButtonImageView.setOnClickListener {
            it.post { rewindAnim.start() }
        }
```

## Fast-forward

See note to [Rewind](#rewind) for how to change the seconds interval text inside

![GIF](https://github.com/shmueldabomb441/MediaPlayerAnimations/blob/4301ea88b7718a28e6482bf8ad61d7cc8b81a7cd/fast_forward_gif.gif)

### /drawable/ic_forward.xml

```
<vector android:height="48dp" android:tint="#000000"
    android:viewportHeight="24" android:viewportWidth="24"
    android:width="48dp" xmlns:android="http://schemas.android.com/apk/res/android">

	<group
		android:name="rotationGroup"
		android:pivotX="12"
		android:pivotY="13">
	<path android:fillColor="@android:color/white" android:pathData="M18,13c0,3.31 -2.69,6 -6,6s-6,-2.69 -6,-6s2.69,-6 6,-6v4l5,-5l-5,-5v4c-4.42,0 -8,3.58 -8,8c0,4.42 3.58,8 8,8s8,-3.58 8,-8H18z"/>
	</group>
	<path android:fillColor="@android:color/white" android:pathData="M10.86,15.94l0,-4.27l-0.09,0l-1.77,0.63l0,0.69l1.01,-0.31l0,3.26z"/>
    <path android:fillColor="@android:color/white" android:pathData="M12.25,13.44v0.74c0,1.9 1.31,1.82 1.44,1.82c0.14,0 1.44,0.09 1.44,-1.82v-0.74c0,-1.9 -1.31,-1.82 -1.44,-1.82C13.55,11.62 12.25,11.53 12.25,13.44zM14.29,13.32v0.97c0,0.77 -0.21,1.03 -0.59,1.03c-0.38,0 -0.6,-0.26 -0.6,-1.03v-0.97c0,-0.75 0.22,-1.01 0.59,-1.01C14.07,12.3 14.29,12.57 14.29,13.32z"/>
</vector>
```

### /animator/animator_fast_forward.xml

```
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="http://schemas.android.com/apk/res/android">
	<objectAnimator
		android:duration="200"
		android:propertyName="rotation"
		android:valueFrom="0"
		android:valueTo="45"
		android:repeatMode="reverse"
		android:repeatCount="1"
		/>
</set>
```

### /drawable/anim_forward.xml

```
<?xml version="1.0" encoding="utf-8"?>
<animated-vector xmlns:android="http://schemas.android.com/apk/res/android"
	android:drawable="@drawable/ic_forward" >
	<target
		android:name="rotationGroup"
		android:animation="@animator/animator_fast_forward" />
</animated-vector>
```
