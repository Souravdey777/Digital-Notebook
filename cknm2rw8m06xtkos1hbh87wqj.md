## 🎨 Page fade-in animation with CSS

### Simple animations can bring a huge difference to your websites.


Let us create a page fade-in animation with CSS.

%[https://codepen.io/souravdey777/pen/KKaByRY]

> The above codepen shows animation with `opacity:` from `0` to `1`. Because of `infinite`, it is animating continuously 

check the whole code in [Codepen](https://codepen.io/souravdey777/pen/KKaByRY) or,
check the code below for the animation

HTML snippet.

```
<body>
  <h1>
    This is the fade-in animation moving in y axis 
  </h1>
  <!-- Your code -->
</body>
``` 

Now, add the below code to your 🎨 CSS.

```
body{
  animation: fadeIn 2s infinite;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
``` 

If you remove the `infinite` from the CSS you will get the animation effect on the first render only. With `infinite` it is animating continuously.

There can be many more possibilities.

Check this out,

%[https://codepen.io/souravdey777/pen/PoWBEGV]
>The above codepen shows animation with `transform:` from `translateY(50px)` to `translateY(0)` and `opacity:` from `0` to `1`. Because of `infinite` it is animating continuously.

Link for [Codepen](https://codepen.io/souravdey777/pen/PoWBEGV)

The HTML code snippet will be the same and for the 🎨 CSS. check the code below 👇


```
body{
  animation: fadeIn 2s infinite;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(50px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
``` 
Just remove the `infinite` from the CSS code for getting the animation once on the load of the page only.

Now, put on your creative hats and make an animation effect for your whole website on the initial load.

You can check something similar I did for my portfolio website.
 [Souravdey.Space](https://souravdey.space) ✌

Drop the website link in the comments for which you would be doing it or have done it.

Show your love by Sharing the blog. 🤗 

### Contact me 🌍

- [Github](https://github.com/Souravdey777/)
- [LinkedIn](https://www.linkedin.com/in/souravdey777)
- [Twitter](https://twitter.com/Souravdey777)

