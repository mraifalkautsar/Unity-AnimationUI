![Logo](Images/AnimationUI.png)
<h1 align="center">AnimationUI</h1>

AnimationUI is a unity tool to create UI animation easily with no code. You can simply drag and drop to create smooth UI animation. There are some option that you can set such as the easing, duration, etc. It basically consist of a component that has an array of sequence that has an array of task. You can also make a custom sequence with UnityEvent including the dynamic one.


## ✨ Demo Preview
<p align="center">
      <img src="./Images/PreviewAnimationUI.gif" align="left">
      <img src="./Images/PreviewSettings.gif" align="right">
</p>
</br>
<p align="center">
      <img src="./Images/PreviewUpgrade.gif" align="left">
      <img src="./Images/PreviewStart.gif" align="right">
</p>

<!-- <p align="center">
  <img alt="Preview AnimationUI" src="./Images/PreviewAnimationUI.gif" width="45%">
&nbsp; &nbsp; &nbsp; &nbsp;
  <img alt="Preview Settings" src="./Images/PreviewSettings.gif" width="45%">
</p>
<p align="center">
  <img alt="Preview Upgrade" src="./PreviewUpgrade.gif" width="45%">
&nbsp; &nbsp; &nbsp; &nbsp;
  <img alt="Preview Start" src="./PreviewStart.gif" width="45%">
</p> -->

<!-- ![Preview AnimationUI](Images/PreviewAnimationUI.gif)
![Preview Settings](Images/PreviewSettings.gif)
![Preview Upgrade](Images/PreviewUpgrade.gif)
![Preview Start](Images/PreviewStart.gif) -->




## ✨ Features

- Animate values of RectTransform, Image, Camera, CanvasGroup, Transform, and Dynamic UnityEvent.
- Preview animation in edit mode with Progress bar both globally and in each sequence.
- Set Active All Input 
- Play SFX
- Wait before executing next sequence
- Set Active GameObject
- UnityEvent
- Others


## 📖 Instruction
- Right click -> UI -> Create AnimationUI
- Or you can just add the AnimationUI Component to a gameObject

![Instruction 1](Images/1.gif)
![Instruction 2](Images/2.gif)
![Instruction 3](Images/3.gif)
![Instruction 4](Images/4.gif)
![Instruction 5](Images/5.gif)
![Instruction 6](Images/6.gif)



## 🔍 API Reference

Get the reference by

```csharp
AnimationUI _animationUI;
_animationUI.MyMethodName();
```

### 🔗 Syntax

| Method                            | Description                        |
|:--------                          | :------------------------------    |
|`Play()`                           | Play the animation |
|`PlayReversed()`                   | Play the animation but reversed. Usefull to go back from a certain menu quickly.|
|`AddFunctionAt(float time, delegate func)`| Add a function to be called at a certain time after the AnimationUI.Play() is called|
|`AddFunctionAtEnd(delegate func)`  |Add a function to be called at a certain time after the animation is finished |

Most of the variable in the Sequence class is modifiedable, so it's possible to change the values of `_animationUI.AnimationSequence[MyIndex].MyVariableName` on runtime.

#### 📖 Examples

Play the animation, call `LoadSceneWithLoadingBar()` after animation finished.
```csharp
_animationUI.Play();
_animationUI.AddFunctionAtEnd(LoadSceneWithLoadingBar);
```


## 📝 License
[MIT](https://choosealicense.com/licenses/mit/)


- readme to explain others category for custom button demos, etc.
- There's also reverse button usefull to go back from other menu
- if you're not sure about which variable to animate, you can always capture all variable with the set start or the set end button. One example is when you want to animate Rect Transform with Anchor Presets of strectch. just try enabling all variable and set everything, you might be able to produce some good results
- you may not need to code anything even if you want to create animation that for example has an object with position relative to the left side of the screen, maybe hidden outside screen, then it change into the middle
- show example even if the screen is so long, it will still work
- make sure to press the preview start because you may accidentally do something like disabling all input
- Theres progress indicator individually
- PlayOnStart usefull for transition to a new scene
- Put singleton in resource folder
- There's no proper way to block all input so please modify button block