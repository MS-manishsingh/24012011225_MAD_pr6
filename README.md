Practical-6: Frame by Frame Animation & Twin Animation



👤 Author
Name: Rutul Patel Enrollment No.: 24012011123


🎯 Aim
Create an Android Application to demonstrate Frame by Frame Animation and a Splash Screen to demonstrate Twin Animation.

📖 About the Practical
This practical covers two core Android animation concepts:

Frame by Frame Animation (AnimationDrawable) — a sequence of static images is displayed one after another at a fixed interval to simulate motion, similar to a flipbook. Used here in three places: the Ganpat University logo on the splash screen, the alarm clock on the main screen, and the filling heart icon inside the info card.

Twin Animation (Animation / AnimationUtils) — a <set> of animation tags (<translate>, <rotate>, <scale>) applied together on a single view (the Ganpat University logo) to create a combined transform effect on the splash screen.

The app has two screens:

SplashActivity — displays the Ganpat University / U.V. Patel College of Engineering logo on a radial gradient background (dark olive green #30500E → dark navy #1E2545), created using a <gradient> tag inside a <shape> drawable. Two animations run on the logo at the same time: a frame by frame animation (uvpce_animation_list.xml, 8 logo frames, oneshot="true") and a twin animation (twinanimation.xml — translate + rotate 0°→360° + scale up to 2.0x then back down to 0.5x). Once the twin animation finishes (onAnimationEnd), it navigates to MainActivity.

MainActivity — displays a frame by frame animation of an alarm clock (10 frames, looping continuously via oneshot="false") inside a MaterialCardView-based UI, along with a title, description, Create Alarm / Cancel Alarm buttons, and a heart icon that is itself a 5-frame frame by frame animation (empty → full heart).

🛠️ Concepts & Components Used
ImageView
AnimationDrawable (Frame by Frame Animation)
Animation / AnimationUtils (Twin Animation)
Animation.AnimationListener (onAnimationStart, onAnimationEnd, onAnimationRepeat)
onWindowFocusChanged() method — used to correctly start AnimationDrawable after the view is attached to the window
<animation-list> — frame sequence with android:oneshot attribute (true for the splash logo, false for the looping alarm and heart)
<set> tag with <translate>, <rotate>, <scale> tags for twin animation
enableEdgeToEdge() — Immersive Mode / Edge to Edge display
WindowInsetsCompat — handling system bar insets manually
<gradient> tag inside <shape> — radial gradient background for splash screen
ConstraintLayout — used for all screen layouts
MaterialCardView — used for the info card on the main screen
Intent — navigation from SplashActivity to MainActivity

##   🎬 Demo Video

https://github.com/user-attachments/assets/448eaa80-ec4c-458c-80e1-07c6624a9ef6

## 📸 Screenshots

<img width="300" height="400" alt="unnamed (1)" src="https://github.com/user-attachments/assets/b1791a93-f5d9-4b01-89d2-fb3cbcb2fe31" />

<img width="300" height="400" alt="unnamed" src="https://github.com/user-attachments/assets/5abfbe80-0cda-4d1a-aadc-5725ad2f27ff" />

