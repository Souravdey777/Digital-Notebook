## 🎨 Moving Gradient animation with CSS

Simple animations can bring a huge difference to your websites.
Let's build something simple and unique.


### Complete page background animation with CSS moving gradient

%[https://codepen.io/souravdey777/pen/poROYza]
> The above Codepen example shows a moving gradient animation on the whole body of the website.

Code snippet for the animation effect.

HTML 👇
```
<body>
  <h1>
     Animation effect on "body"
  </h1>
</body>
``` 

CSS 👇
```
body {
  background: -webkit-linear-gradient(
    -70deg,
    #a2facf,
    #64acff
  );
  background-size: 400% 400%;
  animation: gradient 5s ease infinite;
}

@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}
```
#### what is actually happening ??

The ** background size here is 400% 400%** and the background is moving. Thus, the animation is happening. 

![Frame 2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1618910655541/iHGAtnmJX.png)


![Frame 3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1618910678556/58MXeNJ4m.png)


A lot of cool stuff can be code with this type of animation.

### 1. 🌈 Rainbow Effect


%[https://codepen.io/souravdey777/pen/JjEmYRQ]
> The above Codepen example shows a 🌈 rainbow effect.

This is similar to the animation that we saw in the previous example but with 7 colors.


### 2. Loader for cards and simple components.

%[https://codepen.io/souravdey777/pen/dyNgYZY]
> The above Codepen example shows a loader 🐌 with the same gradient animation.

### 3. Implementing the same effect on a button or cards

%[https://codepen.io/souravdey777/pen/WNRaGMB]
> The above Codepen example shows 🌈 the rainbow effect on a button.

### 4. On Hover the same animation effect

%[https://codepen.io/souravdey777/pen/ExZdNav]
> Animation on hovering on the card

### Configurable parameters

#### → Changing the `background-size`

#### → Changing the `time-duration`

#### → Changing the `degree` of the linear gradient.


Now, put on your creative 🤠 hats and make an interesting animation effect with moving gradients.

Drop the website link in the comments for which you would be doing it or have done it.

Show your love by Sharing the blog. 🤗 

### You can find in me on the web 🌍

- [Github](https://github.com/Souravdey777)
- [LinkedIn](https://www.linkedin.com/in/souravdey777)
- [Twitter](https://twitter.com/Souravdey777)

