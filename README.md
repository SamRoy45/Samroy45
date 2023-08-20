### Hi there 👋

<!--
**SamRoy45/Samroy45** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <string name="game_services_project_id"
            translatable="false">add your Project ID here</string>
</resources>  android {
    ...
    buildFeatures {
      prefab true
    }
    ...
  }
  dependencies {
    ...
    implementation "com.google.android.gms:play-services-games-v2-native-c:17.0.0-beta1"
  }<manifest>
  <application>
    <meta-data android:name="com.google.android.gms.games.APP_ID"
               android:value="@string/game_services_project_id"/>
  </application>
    </manifest>  find_package(com.google.android.gms.games.v2.c REQUIRED CONFIG)

  // link games_static for -DANDROID_STL=c++_static or default
  // link games_shared for -DANDROID_STL=c++_shared
  target_link_libraries(
    app PUBLIC com.google.android.gms.games.v2.c::games_static)
