# Android Frame-by-Frame Animation and Splash Screen

![Android](https://img.shields.io/badge/Platform-Android-green)
![Language](https://img.shields.io/badge/Language-Kotlin-blue)
![UI](https://img.shields.io/badge/UI-XML-orange)
![IDE](https://img.shields.io/badge/IDE-Android%20Studio-lightgrey)
![License](https://img.shields.io/badge/License-Educational-lightgrey)

An Android application developed using **Kotlin and XML** to demonstrate **Frame-by-Frame Animation** and **Twin Animation** through a Splash Screen.

The application demonstrates how images can be animated frame by frame using `AnimationDrawable` and how multiple animation effects such as **Scale, Translate, Rotate, and Alpha** can be combined using the `<set>` tag.

---

## 📌 Practical Information

| Field                      | Details                                    |
| -------------------------- | ------------------------------------------ |
| **Subject**                | Mobile Application Development             |
| **Practical No.**          | 6                                          |
| **Practical Title**        | Frame-by-Frame Animation and Splash Screen |
| **Student Enrollment No.** | 25172022051                                |
| **Programming Language**   | Kotlin                                     |
| **UI Technology**          | XML                                        |
| **Development Tool**       | Android Studio                             |
| **Repository**             | `25172022051_MAD_PRACTICAL_6`              |

---

## 🎯 Aim

To create an Android application to demonstrate **Frame-by-Frame Animation** and **Splash Screen to demonstrate Twin Animation**.

---

## 📖 Introduction

Animation is used in Android applications to make the user interface more attractive and interactive.

This practical demonstrates two important types of animation:

1. **Frame-by-Frame Animation**
2. **Twin Animation**

The application also demonstrates the use of a **Splash Screen** with a gradient background and multiple animation effects.

---

## ✨ Features

* Displays a Splash Screen when the application starts.
* Uses a **radial gradient rectangle** for the Splash Screen background.
* Uses **pink and blue** gradient colors.
* Demonstrates **Frame-by-Frame Animation**.
* Uses `AnimationDrawable`.
* Uses the `<animation-list>` XML tag.
* Uses the `oneShot` attribute.
* Demonstrates **Twin Animation**.
* Uses the `<set>` XML tag.
* Uses `<scale>` animation.
* Uses `<translate>` animation.
* Uses `<rotate>` animation.
* Uses `<alpha>` animation.
* Uses `android:startOffset`.
* Uses `android:duration`.
* Uses `AnimationUtils` class.
* Uses `loadAnimation()` method.
* Uses `setAnimationListener()` method.
* Uses `overridePendingTransition()` method.
* Uses `finish()` method.
* Uses `onWindowFocusChanged()` method.
* Uses **Immersive Mode**.
* Uses **Display Edge-to-Edge**.
* Uses **ImageView**.
* Uses **anim folder** in `res`.
* Demonstrates converting an SVG file into an XML drawable.

---

## 🛠️ Technologies Used

* **Android Studio**
* **Kotlin**
* **XML**
* **Android SDK**
* **ImageView**
* **AnimationDrawable**
* **AnimationUtils**
* **Animation XML**
* **SplashScreen**
* **SplashActivity**
* **MainActivity**
* **Immersive Mode**
* **Edge-to-Edge Display**
* **SVG / Vector Drawable**
* **Gradient Drawable**

---

## 🎨 User Interface

The application contains two main screens:

### 1. Splash Screen

The Splash Screen is displayed when the application starts.

It contains:

* Gradient background.
* Animated application logo or image.
* Twin Animation effects.
* Full-screen immersive appearance.

### 2. Main Activity

The Main Activity demonstrates Frame-by-Frame Animation.

It contains:

* An ImageView.
* Animated images.
* Frame-by-frame animation.
* UI elements according to the practical design.

### Example UI

```text
┌──────────────────────────────┐
│                              │
│                              │
│          SPLASH              │
│          SCREEN              │
│                              │
│       Animated Logo          │
│                              │
│                              │
└──────────────────────────────┘
                ↓
┌──────────────────────────────┐
│                              │
│          MAIN ACTIVITY       │
│                              │
│       Frame Animation        │
│                              │
│       [ Animated Image ]     │
│                              │
└──────────────────────────────┘
```

> **Note:** The exact UI depends on the XML layout implemented in the project.

---

## 🎞️ What is Frame-by-Frame Animation?

**Frame-by-Frame Animation** is an animation technique in which a sequence of images is displayed one after another.

Each image is called a **frame**.

When the frames are displayed quickly, they create the appearance of movement.

### Example

```text
Frame 1 → Frame 2 → Frame 3 → Frame 4
```

### Real-Life Example

A moving cartoon character can be created by displaying multiple images of the character in different positions.

### Android Implementation

Frame-by-Frame Animation can be implemented using:

* `AnimationDrawable`
* `<animation-list>`
* `ImageView`

---

## 🎬 What is Twin Animation?

**Twin Animation** refers to the combination of two or more animation effects to create a single animation.

For example:

* Scale + Alpha
* Translate + Rotate
* Scale + Rotate
* Translate + Alpha

In this practical, multiple animation effects are combined using the `<set>` tag.

### Example

```text
Scale Animation
       +
Alpha Animation
       ↓
Combined Animation
```

### Android Implementation

Twin Animation can be implemented using:

* `<set>`
* `<scale>`
* `<translate>`
* `<rotate>`
* `<alpha>`
* `AnimationUtils`
* `loadAnimation()`

---

## 🔄 Application Workflow

```text
Application Starts
        ↓
SplashActivity
        ↓
Gradient Background
        ↓
Twin Animation
        ↓
Animation Completes
        ↓
MainActivity
        ↓
Frame-by-Frame Animation
        ↓
AnimationDrawable
```

---

## 🌈 Splash Screen Gradient Background

The Splash Screen uses a **radial gradient rectangle**.

### Required Properties

| Property          | Value     |
| ----------------- | --------- |
| **Shape**         | Rectangle |
| **Gradient Type** | Radial    |
| **Center X**      | `0.9`     |
| **Center Y**      | `0.9`     |
| **Radius**        | `1500`    |
| **Start Color**   | Pink      |
| **End Color**     | Blue      |

### Example XML

```xml
<shape xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">

    <gradient
        android:type="radial"
        android:centerX="0.9"
        android:centerY="0.9"
        android:gradientRadius="1500"
        android:startColor="#FF69B4"
        android:endColor="#0000FF" />

</shape>
```

### Explanation

* `<shape>` creates the drawable shape.
* `android:shape="rectangle"` creates a rectangle.
* `android:type="radial"` creates a radial gradient.
* `android:centerX="0.9"` sets the horizontal center.
* `android:centerY="0.9"` sets the vertical center.
* `android:gradientRadius="1500"` sets the gradient radius.
* `android:startColor` defines the starting color.
* `android:endColor` defines the ending color.

---

## 🖼️ ImageView

`ImageView` is an Android UI component used to display images.

### Example

```xml
<ImageView
    android:id="@+id/imageView"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:src="@drawable/logo" />
```

### Purpose

* Displays images.
* Displays animated images.
* Used with `AnimationDrawable`.

---

## 🎞️ Frame-by-Frame Animation using AnimationDrawable

`AnimationDrawable` is used to display a sequence of drawable images.

### Example XML

```xml
<animation-list
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:oneshot="false">

    <item
        android:drawable="@drawable/frame1"
        android:duration="100" />

    <item
        android:drawable="@drawable/frame2"
        android:duration="100" />

    <item
        android:drawable="@drawable/frame3"
        android:duration="100" />

</animation-list>
```

### Example Kotlin

```kotlin
val imageView = findViewById<ImageView>(R.id.imageView)

imageView.setBackgroundResource(R.drawable.frame_animation)

val animationDrawable =
    imageView.background as AnimationDrawable

animationDrawable.start()
```

### Explanation

* `<animation-list>` contains multiple frames.
* `<item>` defines each frame.
* `android:drawable` specifies the image.
* `android:duration` specifies how long each frame is displayed.
* `AnimationDrawable` controls the animation.
* `start()` starts the animation.

---

## 🔁 oneShot Attribute

The `oneShot` attribute controls whether the animation repeats.

### Example

```xml
android:oneshot="true"
```

### Meaning

* `true` → Animation plays only once.
* `false` → Animation repeats continuously.

---

## 🎭 Twin Animation using `<set>`

The `<set>` tag is used to combine multiple animations.

### Example

```xml
<set xmlns:android="http://schemas.android.com/apk/res/android">

    <scale
        android:fromXScale="0.5"
        android:toXScale="1.0"
        android:fromYScale="0.5"
        android:toYScale="1.0"
        android:duration="1000" />

    <alpha
        android:fromAlpha="0.0"
        android:toAlpha="1.0"
        android:duration="1000" />

</set>
```

### Explanation

* `<set>` combines multiple animations.
* `<scale>` changes the size.
* `<alpha>` changes transparency.
* Both animations run together.

---

## 📏 `<scale>` Tag

The `<scale>` tag is used to change the size of a view.

### Example

```xml
<scale
    android:fromXScale="0.5"
    android:toXScale="1.0"
    android:fromYScale="0.5"
    android:toYScale="1.0"
    android:duration="1000" />
```

### Purpose

* Zoom in.
* Zoom out.
* Change the size of a view.

---

## ↔️ `<translate>` Tag

The `<translate>` tag is used to move a view from one position to another.

### Example

```xml
<translate
    android:fromXDelta="-100"
    android:toXDelta="0"
    android:duration="1000" />
```

### Purpose

* Moves a view horizontally.
* Moves a view vertically.

---

## 🔄 `<rotate>` Tag

The `<rotate>` tag is used to rotate a view.

### Example

```xml
<rotate
    android:fromDegrees="0"
    android:toDegrees="360"
    android:duration="1000" />
```

### Purpose

* Rotates a view.
* Creates a spinning effect.

---

## 🌫️ `<alpha>` Tag

The `<alpha>` tag is used to change the transparency of a view.

### Example

```xml
<alpha
    android:fromAlpha="0.0"
    android:toAlpha="1.0"
    android:duration="1000" />
```

### Purpose

* Fade in.
* Fade out.
* Change transparency.

---

## ⏱️ android:startOffset

`android:startOffset` specifies the delay before an animation starts.

### Example

```xml
android:startOffset="100"
```

### Meaning

The animation starts after **100 milliseconds**.

---

## ⏳ android:duration

`android:duration` specifies how long an animation runs.

### Example

```xml
android:duration="1000"
```

### Meaning

The animation runs for **1000 milliseconds = 1 second**.

---

## 🧰 AnimationUtils Class

`AnimationUtils` is used to load animation resources.

### Example

```kotlin
val animation = AnimationUtils.loadAnimation(
    this,
    R.anim.twin_animation
)
```

### Purpose

* Loads animation XML.
* Creates an Animation object.

---

## 📥 loadAnimation() Method

`loadAnimation()` loads an animation resource from the `res/anim` folder.

### Example

```kotlin
val animation = AnimationUtils.loadAnimation(
    this,
    R.anim.twin_animation
)
```

### Purpose

* Loads XML animation.
* Applies animation to a View.

---

## 👂 setAnimationListener() Method

`setAnimationListener()` is used to listen for animation events.

### Example

```kotlin
animation.setAnimationListener(object :
    Animation.AnimationListener {

    override fun onAnimationStart(animation: Animation?) {
    }

    override fun onAnimationEnd(animation: Animation?) {
    }

    override fun onAnimationRepeat(animation: Animation?) {
    }
})
```

### Methods

| Method                | Purpose                       |
| --------------------- | ----------------------------- |
| `onAnimationStart()`  | Called when animation starts  |
| `onAnimationEnd()`    | Called when animation ends    |
| `onAnimationRepeat()` | Called when animation repeats |

---

## 🔀 overridePendingTransition()

`overridePendingTransition()` is used to apply animation while moving from one Activity to another.

### Example

```kotlin
overridePendingTransition(
    android.R.anim.fade_in,
    android.R.anim.fade_out
)
```

### Purpose

* Applies transition animation.
* Makes Activity navigation smoother.

---

## 🛑 finish() Method

`finish()` is used to close the current Activity.

### Example

```kotlin
finish()
```

### Purpose

* Closes the current Activity.
* Prevents returning to the Splash Screen using the Back button.

---

## 🖥️ onWindowFocusChanged() Method

`onWindowFocusChanged()` is called when the Activity gains or loses window focus.

It can be used to apply immersive mode.

### Example

```kotlin
override fun onWindowFocusChanged(hasFocus: Boolean) {
    super.onWindowFocusChanged(hasFocus)

    if (hasFocus) {
        // Apply immersive mode
    }
}
```

### Purpose

* Detects window focus changes.
* Applies full-screen UI behavior.

---

## 🖥️ Immersive Mode

**Immersive Mode** allows an application to display content in full screen by hiding system bars.

It is useful for:

* Splash Screens.
* Games.
* Media applications.
* Full-screen experiences.

### Example

```kotlin
window.decorView.systemUiVisibility =
    View.SYSTEM_UI_FLAG_IMMERSIVE_STICKY or
            View.SYSTEM_UI_FLAG_FULLSCREEN or
            View.SYSTEM_UI_FLAG_HIDE_NAVIGATION or
            View.SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN or
            View.SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION or
            View.SYSTEM_UI_FLAG_LAYOUT_STABLE
```

> **Note:** Modern Android applications may use `WindowInsetsControllerCompat` for immersive mode.

---

## 📱 Display Edge-to-Edge

**Edge-to-Edge** allows application content to extend behind the system bars.

### Example

```kotlin
enableEdgeToEdge()
```

### Purpose

* Uses the full screen.
* Allows content to extend behind system bars.
* Creates a modern UI experience.

---

## 📂 anim Folder in res

The `anim` folder is used to store animation XML files.

### Example Structure

```text
res/
└── anim/
    ├── twin_animation.xml
    ├── scale_animation.xml
    ├── translate_animation.xml
    ├── rotate_animation.xml
    └── alpha_animation.xml
```

### Purpose

* Stores animation resources.
* Allows animations to be loaded using `AnimationUtils`.

---

## 🖼️ Convert SVG File to XML File

Android supports vector drawable XML files.

An SVG file can be converted into an Android Vector Drawable XML file.

### Steps

1. Open Android Studio.
2. Right-click on the `res/drawable` folder.
3. Select **New → Vector Asset**.
4. Select **Local File (SVG, PSD)**.
5. Choose the SVG file.
6. Click **Next**.
7. Click **Finish**.

Android Studio creates an XML vector drawable.

### Example

```text
res/
└── drawable/
    └── logo.xml
```

### Usage

```xml
android:src="@drawable/logo"
```

---

## 📂 Project Structure

```text
25172022051_MAD_PRACTICAL_6/
│
├── .idea/
│
├── app/
│   └── src/
│       └── main/
│           │
│           ├── java/
│           │   └── com/
│           │       └── example/
│           │           └── a25172022051_MAD_PRACTICAL_6/
│           │               │
│           │               ├── MainActivity.kt
│           │               └── SplashActivity.kt
│           │
│           ├── res/
│           │   ├── anim/
│           │   │   ├── twin_animation.xml
│           │   │   ├── scale_animation.xml
│           │   │   ├── translate_animation.xml
│           │   │   ├── rotate_animation.xml
│           │   │   └── alpha_animation.xml
│           │   │
│           │   ├── drawable/
│           │   │   ├── splash_background.xml
│           │   │   ├── frame_animation.xml
│           │   │   └── logo.xml
│           │   │
│           │   ├── mipmap/
│           │   │
│           │   ├── layout/
│           │   │   ├── activity_main.xml
│           │   │   └── activity_splash.xml
│           │   │
│           │   └── values/
│           │       ├── colors.xml
│           │       ├── strings.xml
│           │       └── themes.xml
│           │
│           └── AndroidManifest.xml
│
├── gradle/
│
├── build.gradle.kts
├── settings.gradle.kts
├── gradle.properties
├── gradlew
├── gradlew.bat
└── README.md
```

> **Note:** The actual package name and file names may differ depending on the project implementation.

---

## 📄 MainActivity.kt Responsibilities

`MainActivity.kt` is responsible for:

* Initializing the Activity.
* Connecting the XML layout with the Activity.
* Displaying the main UI.
* Loading Frame-by-Frame Animation.
* Using `AnimationDrawable`.
* Starting the animation.
* Handling ImageView.

---

## 📄 SplashActivity.kt Responsibilities

`SplashActivity.kt` is responsible for:

* Displaying the Splash Screen.
* Applying the gradient background.
* Loading Twin Animation.
* Using `AnimationUtils`.
* Using `loadAnimation()`.
* Using `setAnimationListener()`.
* Starting MainActivity after animation completes.
* Applying `overridePendingTransition()`.
* Calling `finish()`.

---

## 📄 activity_main.xml Responsibilities

`activity_main.xml` is responsible for:

* Creating the main UI.
* Displaying ImageView.
* Providing the frame animation view.
* Arranging UI components.

---

## 📄 activity_splash.xml Responsibilities

`activity_splash.xml` is responsible for:

* Creating the Splash Screen UI.
* Displaying the animated logo.
* Applying the gradient background.
* Providing the view for Twin Animation.

---

## 📄 AndroidManifest.xml Responsibilities

`AndroidManifest.xml` is responsible for:

* Registering Activities.
* Declaring the SplashActivity.
* Declaring the MainActivity.
* Setting the launcher Activity.

### Example

```xml
<activity
    android:name=".SplashActivity"
    android:exported="true">

    <intent-filter>
        <action android:name="android.intent.action.MAIN" />
        <category android:name="android.intent.category.LAUNCHER" />
    </intent-filter>

</activity>

<activity
    android:name=".MainActivity"
    android:exported="false" />
```

---

## 🚀 How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/yashPatel228/25172022051_MAD_PRACTICAL_6.git
```

### Step 2: Open the Project

Open the cloned project in **Android Studio**.

### Step 3: Wait for Gradle Sync

Allow Android Studio to complete the Gradle synchronization.

### Step 4: Connect a Device

Connect an Android device using USB debugging or start an Android Emulator.

### Step 5: Run the Application

Click the **Run ▶️** button in Android Studio.

### Step 6: Observe the Splash Screen

The Splash Screen will appear with the gradient background and animation.

### Step 7: Observe Twin Animation

The Splash Screen will demonstrate combined animation effects.

### Step 8: Observe MainActivity

After the Splash Screen animation completes, MainActivity will open.

### Step 9: Observe Frame Animation

The MainActivity will demonstrate Frame-by-Frame Animation.

---

## 📊 Expected Output

### Splash Screen

```text
┌──────────────────────────────┐
│                              │
│                              │
│       Animated Logo          │
│                              │
│      Splash Screen           │
│                              │
│                              │
└──────────────────────────────┘
```

### MainActivity

```text
┌──────────────────────────────┐
│                              │
│       Main Activity          │
│                              │
│       Frame Animation        │
│                              │
│       [ Animated Image ]     │
│                              │
└──────────────────────────────┘
```

### Animation Output

* Splash Screen appears.
* Gradient background is displayed.
* Twin Animation plays.
* MainActivity opens.
* Frame-by-Frame Animation starts.

---

## 🧪 Testing

The application can be tested using the following operations:

| Test Case                      | Expected Result                                        |
| ------------------------------ | ------------------------------------------------------ |
| Open the application           | Splash Screen appears                                  |
| Check gradient background      | Pink and blue radial gradient is displayed             |
| Check Twin Animation           | Multiple animation effects play                        |
| Wait for animation completion  | MainActivity opens                                     |
| Check Frame Animation          | Images are displayed one after another                 |
| Check `oneShot`                | Animation repeats or plays once according to its value |
| Check `startOffset`            | Animation starts after the specified delay             |
| Check `duration`               | Animation runs for the specified time                  |
| Check `setAnimationListener()` | Animation events are detected                          |
| Check `finish()`               | SplashActivity closes after transition                 |
| Check Edge-to-Edge             | Content uses the full screen                           |
| Check SVG conversion           | SVG is converted into XML drawable                     |

---

## 🛠️ Troubleshooting

### 1. Animation Does Not Start

Check that:

* The animation XML file exists.
* The ImageView ID is correct.
* The drawable resource is correctly referenced.
* `animationDrawable.start()` is called.

---

### 2. Splash Screen Does Not Open

Check that:

* SplashActivity is registered in the Manifest.
* SplashActivity is the launcher Activity.
* The package name is correct.

---

### 3. Twin Animation Does Not Work

Check that:

* The animation XML is placed inside `res/anim`.
* The `<set>` tag is used correctly.
* `AnimationUtils.loadAnimation()` is called.
* The animation is applied to the correct View.

---

### 4. Gradient Background Does Not Appear

Check that:

* The gradient XML is placed inside `res/drawable`.
* The drawable is applied to the correct layout.
* The gradient attributes are correct.

---

### 5. SVG File Does Not Work

Check that:

* The SVG file is converted using Vector Asset.
* The XML drawable is placed inside `res/drawable`.
* The drawable is referenced correctly.

---

## 🎓 Study / Viva Questions

### 1. What is Frame-by-Frame Animation?

Frame-by-Frame Animation displays a sequence of images one after another to create movement.

### 2. What is Twin Animation?

Twin Animation combines two or more animation effects into a single animation.

### 3. What is AnimationDrawable?

AnimationDrawable is used to display a sequence of drawable images.

### 4. What is the use of `<animation-list>`?

`<animation-list>` defines a list of animation frames.

### 5. What is the use of `oneShot`?

`oneShot` controls whether the animation repeats.

### 6. What is the use of `<set>`?

`<set>` combines multiple animations.

### 7. What is the use of `<scale>`?

`<scale>` changes the size of a View.

### 8. What is the use of `<translate>`?

`<translate>` moves a View.

### 9. What is the use of `<rotate>`?

`<rotate>` rotates a View.

### 10. What is the use of `<alpha>`?

`<alpha>` changes the transparency of a View.

### 11. What is `android:startOffset`?

It specifies the delay before an animation starts.

### 12. What is `android:duration`?

It specifies the time taken by an animation.

### 13. What is AnimationUtils?

AnimationUtils is used to load animation resources.

### 14. What is `loadAnimation()`?

`loadAnimation()` loads an animation XML resource.

### 15. What is `setAnimationListener()`?

It is used to listen for animation events.

### 16. What is `overridePendingTransition()`?

It applies animation while moving between Activities.

### 17. What is `finish()`?

`finish()` closes the current Activity.

### 18. What is SplashScreen?

SplashScreen is the first screen displayed when an application starts.

### 19. What is Immersive Mode?

Immersive Mode hides system bars to provide a full-screen experience.

### 20. What is Edge-to-Edge?

Edge-to-Edge allows application content to extend behind system bars.

### 21. What is ImageView?

ImageView is an Android UI component used to display images.

### 22. What is the use of the `anim` folder?

The `anim` folder stores animation XML files.

### 23. How can SVG be converted into XML?

SVG can be converted into an Android Vector Drawable XML using Android Studio's Vector Asset tool.

---

## 📚 Learning Outcomes

After completing this practical, students will understand:

* How to create a Splash Screen.
* How to create Frame-by-Frame Animation.
* How to create Twin Animation.
* How to use AnimationDrawable.
* How to use `<animation-list>`.
* How to use `oneShot`.
* How to use `<set>`.
* How to use `<scale>`.
* How to use `<translate>`.
* How to use `<rotate>`.
* How to use `<alpha>`.
* How to use `android:startOffset`.
* How to use `android:duration`.
* How to use AnimationUtils.
* How to use `loadAnimation()`.
* How to use `setAnimationListener()`.
* How to use `overridePendingTransition()`.
* How to use `finish()`.
* How to use `onWindowFocusChanged()`.
* How to use Immersive Mode.
* How to use Edge-to-Edge display.
* How to use ImageView.
* How to use the `anim` folder.
* How to convert SVG into XML drawable.
* How to apply gradient backgrounds.

---

## ✅ Conclusion

This practical demonstrates the development of an **Android application using Kotlin and XML**.

The application uses **Frame-by-Frame Animation** to display a sequence of images and **Twin Animation** to combine multiple animation effects.

It also demonstrates the use of **SplashScreen, AnimationDrawable, AnimationUtils, ImageView, Gradient Drawable, Immersive Mode, and Edge-to-Edge Display**.

Through this practical, students learn how to create attractive and interactive Android applications using animation techniques.

---

## 👨‍💻 Author

**Yash Patel**

**Enrollment No.:** 25172022051

**Subject:** Mobile Application Development

---

## 📌 Repository

This project is available on GitHub:

**25172022051_MAD_PRACTICAL_6**

---

## 📄 License

This project is created for **educational and practical purposes**.
