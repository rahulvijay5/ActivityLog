# 📅 Daily Activity Log - Day [2]  
### Date: 2 January'25  

## ✅ What was done today:  
- Learned about adding gestures in Expo with `react-native-reanimated` and `react-native-gesture-handler`.  
- Explored how to scale and move elements on the screen using gestures.  
- Set up screenshot functionality using `react-native-view-shot` and `expo-media-library`.  
- Configured the status bar and updated the app icon.  

## 📚 What I learned today:  
- Implementing double-tap gestures to scale images:  
  ```jsx
  const doubleTap = Gesture.Tap()
    .numberOfTaps(2)
    .onStart(() => {
      if (scaleImage.value !== imageSize * 2) {
        scaleImage.value = scaleImage.value * 2;
      } else {
        scaleImage.value = Math.round(scaleImage.value / 2);
      }
    });
    ```
- Using Pan gestures to drag elements:
```jsx
const drag = Gesture.Pan().onChange(event => {
  translateX.value += event.changeX;
  translateY.value += event.changeY;
});
```
- Asking for gallery permissions with expo-media-library.
- Benefits of FlatList and SectionList for efficient list rendering.

## 🎯 What I will do tomorrow:

Either:
- Build more complex UIs for practice or,
- Learn how to integrate backends into React Native apps.
- Follow the roadmap at React Native Roadmap.

## Github Repo:
- [Expo Docs App](https://github.com/rahulvijay5/expo-docs-app)

---
### Reflection:
React Native's gestures and animations offer incredible flexibility, but integrating them requires a good grasp of its unique APIs.