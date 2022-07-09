## ⚡ Hashnode Blog Cards 🚀 Reference Link 🔗 of Blogs are not enough, Give your blogs what it deserves with Blog Cards

⚡ The **Hashnode Blog Cards** is a set of `GET` requests which will fetch the Blogs from your Hashnode ids with few parameters and will create SVG cards to bring 😎 awesomeness to your blog links. 🎉


Website link [https://hashnode-blog-cards.vercel.app](https://hashnode-blog-cards.vercel.app/) 
 
Github link [https://github.com/Souravdey777/HashnodeBlogCards](https://github.com/Souravdey777/HashnodeBlogCards) 

It can be added anywhere in Github, Hashnode, Devpost, Postman Documentation, or any markdown editor. It can also be added to any website with HTML syntax with just the `img` tag

Now you can add your hashnode blogs to your GitHub profile in .md file to show your latest blogs or to your Repositories or even to any website.

It is simple to use and the APIs can be explored with the `Hashnode Blog Cards` API Playground.


[![screencapture-hashnode-blog-cards-vercel-app-2021-02-06-22_05_56.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1612636233705/j7sKuVsJE.png)](https://hashnode-blog-cards.vercel.app/)


## How to use it?


%[https://www.canva.com/design/DAEVebtGYdg/view]


---

#### getHashnodeBlog

This API endpoint will fetch a specific blog by its URL

```
https://hashnode-blog-cards.vercel.app/api/getHashnodeBlog?url=https://souravdey777.hashnode.dev/flexbox-guide-flexbox-layout-made-simple-with-an-interactive-tool&large=true&theme=light
```

Response 

![](https://hashnode-blog-cards.vercel.app/api/getHashnodeBlog?url=https://souravdey777.hashnode.dev/flexbox-guide-flexbox-layout-made-simple-with-an-interactive-tool&large=true&theme=light)

#### List of parameters

- `url`= The URL of the specific blog

This is a mandatory parameter

eg. `https://souravdey777.hashnode.dev/flexbox-guide-flexbox-layout-made-simple-with-an-interactive-tool`

- `theme`= The theme of the Card.

This is not a mandatory parameter and the default value is `light`.
Other values are possible values are `dark` or `blue`

- `large`= The size of the Card.

This is not a mandatory parameter and the default value is `false`. And when set to true gives a larger Card.

---

#### getHashnodeBlogBySequence

This API endpoint will fetch a specific blog by the Hashnode username of the author and the serial no of the blog starting from 1 being the latest.

```
https://hashnode-blog-cards.vercel.app/api/getHashnodeBlogBySequence?username=Souravdey777&sequence=1&large=true&theme=light
```

Response 

![](https://hashnode-blog-cards.vercel.app/api/getHashnodeBlogBySequence?username=Souravdey777&sequence=1&large=true&theme=light)

#### List of parameters

- `username`= The hashnode username of the blogger.

This is a mandatory parameter.

eg. `souravdey777` this is my hashnode username.

- `sequence`= The serial no of the blog starting from 1 being the latest. Because of this parameter, the blogs will be changing when you add them to your website or Github profile whenever you add a new blog.

This is a mandatory parameter.

eg. `souravdey777` this is my hashnode username.

- `theme`= The theme of the Card.

This is not a mandatory parameter and the default value is `light`.
Other values are possible values are `dark` or `blue`

- `large`= The size of the Card.

This is not a mandatory parameter and the default value is `false`. And when set to true gives a larger Card.

---

#### getLatestHashnodeBlog

This API endpoint will fetch a set of the latest blogs by the Hashnode username of the author and the limit up to which the blogs are needed

```
https://hashnode-blog-cards.vercel.app/api/getLatestHashnodeBlog?username=Souravdey777&limit=3&large=true&theme=light
``` 
Response 

![](https://hashnode-blog-cards.vercel.app/api/getLatestHashnodeBlog?username=Souravdey777&limit=3&large=true&theme=light)

#### List of parameters

- `username`= The hashnode username of the blogger.

This is a mandatory parameter.

eg. `souravdey777` this is my hashnode username.

- `limit`= The no of the blog starting from latest to the limit defined or all blog you have if the no of blog you have is less than the limit defined.

It is not a mandatory param and the default value is `3`. The maximum possible value is 6.

eg. `souravdey777` this is my hashnode username.

- `theme`= The theme of the Card.

This is not a mandatory parameter and the default value is `light`.
Other values are possible values are `dark` or `blue`

- `large`= The size of the Card.

This is not a mandatory parameter and the default value is `false`. And when set to true gives a larger Card.

---

Now let's see what are the themes we have,

#### For `theme=light`

![](https://hashnode-blog-cards.vercel.app/api/getHashnodeBlog?url=https://souravdey777.hashnode.dev/flexbox-guide-flexbox-layout-made-simple-with-an-interactive-tool&large=true&theme=light)

#### For `theme=dark`

![](https://hashnode-blog-cards.vercel.app/api/getHashnodeBlog?url=https://souravdey777.hashnode.dev/flexbox-guide-flexbox-layout-made-simple-with-an-interactive-tool&large=true&theme=dark)

#### For `theme=blue`

![](https://hashnode-blog-cards.vercel.app/api/getHashnodeBlog?url=https://souravdey777.hashnode.dev/flexbox-guide-flexbox-layout-made-simple-with-an-interactive-tool&large=true&theme=blue)

---

Now let's see the different size we have

#### For `large=true`

![](https://hashnode-blog-cards.vercel.app/api/getHashnodeBlog?url=https://souravdey777.hashnode.dev/flexbox-guide-flexbox-layout-made-simple-with-an-interactive-tool&large=true&theme=light)

#### For `large=false`

![](https://hashnode-blog-cards.vercel.app/api/getHashnodeBlog?url=https://souravdey777.hashnode.dev/flexbox-guide-flexbox-layout-made-simple-with-an-interactive-tool&large=false&theme=light)

#### For 'img' tag custom size defined with `width` and `height` attributes.

---

#### Markdown Syntax
```
[![Hashnode Blog Card](https://hashnode-blog-cards.vercel.app/api/API_ENDPOINT?PARAMS)](BLOG_URL)
```
#### HTML

```
<a href="BLOG_URL">
<img src="https://hashnode-blog-cards.vercel.app/api/getHashnodeBlog?url="https://hashnode-blog-cards.vercel.app/api/API_ENDPOINT?PARAMS" alt="Sourav Dey's Hashnode Blog Cards" />
</a>
```

## My Journey with the Hashnode Blog Cards 

I designed and created mockups for the cards first. 

![Capture.JPG](https://cdn.hashnode.com/res/hashnode/image/upload/v1612643221885/h86DX1NuR.jpeg)

Exported the final SVG from `figma`.

Gone through the documentations of `Nextjs`. 

Checked out the hashnode APIs with [https://api.hashnode.com/](https://api.hashnode.com/) and @[Sandeep Panda](@sandeep)'s blog

Created APIs to fetch the data from hashnode APIs and made the SVG content dynamic.

This is how the APIs were created after that I deployed them in vercel by importing the git repo.

Next, It was the API Playground website.

Edited Lottie Animation as per the color codes.
![Capture.JPG](https://cdn.hashnode.com/res/hashnode/image/upload/v1612643387119/ekrj7o_Oo.jpeg)

Then, it was all `Reactjs`. 

And Yes It also has an error page for wrong links. 😉

![screencapture-hashnode-blog-cards-vercel-app-jhvdyu-2021-02-07-02_12_12.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1612644163863/WWmaAoX1X.png)

## Learnings

- I have been using react for the last 2 years. And honestly, I was only using `CRA` but this is the first time I used `Nextjs` and because of that the deployment in `Vercel` was super smooth. 

- `Lottiefiles`. I used it for the first time and I loved it. I edited the animations with the [Lottie design Editor](https://lottiefiles.com/editor) and the assets in the website are from  [pixeltrue](https://www.pixeltrue.com/free-illustrations).

- We often don't do proper `code linting` on our side projects. But This time I can proudly say I did it properly. Referred to this blog [ESlint and Prettier for React apps](https://dev.to/onygami/eslint-and-prettier-for-react-apps-bonus-next-js-and-typescript-3e46)


## Dependencies


```
  "dependencies": {
    "axios": "^0.21.1",
    "next": "10.0.5",
    "prop-types": "^15.7.2",
    "react": "17.0.1",
    "react-dom": "17.0.1",
    "react-lottie": "^1.2.3"
  },
  "devDependencies": {
    "eslint": "^7.19.0",
    "eslint-config-prettier": "^7.2.0",
    "eslint-plugin-jsx-a11y": "^6.4.1",
    "eslint-plugin-prettier": "^3.3.1",
    "eslint-plugin-react": "^7.22.0",
    "eslint-plugin-react-hooks": "^4.2.0",
    "eslint-plugin-simple-import-sort": "^7.0.0",
    "prettier": "^2.2.1"
  }

``` 


## What is next for the `Hashnode blog Cards`

I have to enhance a few things that I already have in mind.

- PWA of the website
- Markdown and HTML syntax generator or API
- Horizontal Cards.
- more themes

This API is for the Hashnode community so Please tell me what you all will prefer next in this.


>Special thanks to @[Sandeep Panda](@sandeep) for the explanatory blog on Hashnode APIs. 
Click the card below and check out the blog.
[![Blog](https://hashnode-blog-cards.souravdey777.vercel.app/api/getHashnodeBlog?url=https://sandeep.dev/how-to-show-blog-posts-from-your-hashnode-blog-on-your-personal-site&large=true&theme=dark)](https://sandeep.dev/how-to-show-blog-posts-from-your-hashnode-blog-on-your-personal-site)

## License

📝 Distributed under the `MIT` License. See  [LICENSE](https://github.com/Souravdey777/HashnodeBlogCards/blob/main/LICENSE)  for more information.


## Contribution and Support

- [Ask for a new feature or theme](https://github.com/Souravdey777/HashnodeBlogCards/discussions/)

-  [Open a Pull Request](https://github.com/Souravdey777/HashnodeBlogCards/pulls) 
 
- [Raise an Issue](https://github.com/Souravdey777/HashnodeBlogCards/issues/new) 


👨‍🚀 Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

Hope you Loved it! Do let me know in the comments.

## Contact me 

- [Github](https://github.com/Souravdey777/)
- [LinkedIn](https://www.linkedin.com/in/souravdey777)
- [Twitter](https://twitter.com/Souravdey777)


 



