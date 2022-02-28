---
template: blog-post
title: Please Save Their Eyes with Light & Dark Mode
slug: light-and-dark-mode
date: 2022-02-27 23:25
description: light and dark mode post
featuredImage: /assets/walling-jv_r_dnziwu-unsplash.jpg
---
When a website, one goal is to make sure your site is viewable on all devices, but since that is nearly impossible to do, you may want to start with something a little more reasonable¬—creating a light and dark mode version of your website. By making both a light and a dark mode version of your website you are able to have a website that most people will find appealing. This is because those who like viewing darker webpages or don’t like using light mode at night (and vice-versa) can view your website peacefully at any point in time. This can be achieved very easily using the media query prefers-color-scheme. With the prefers-color-scheme media query, you can create a color scheme for light consisting of a light background (usually white) and dark text color (usually black) or for dark a dark background (usually black) and light text color (usually white). You can ever create other color schemes for example a red color scheme if you really wanted to (but I would not recommend making this for light or dark mode. Instead as an option on the page to switch to which is a whole other topic to cover in how to do this). Here is an example of how you could create a light & dark mode using the media query:

```css
@media (prefers-color-scheme: light) {
	background-color: white; /* white background */
	color: black; /* black text color */
}

@media (prefers-color-scheme: dark) {
	background-color: black; /* black background */
	color: white; /* white text color */
}
```

One way you can take this a step further is to use CSS custom properties in your light and dark mode media queries. The first thing to do when using CSS custom properties for light and dark mode is to use the :root variable to create a basic light mode and then creating a basic dark mode like before. By doing this you are saying immediately default to root unless the browser is set to dark mode. This just makes things easier if you end up setting up even more modes in your website. For example, to create a basic root/light mode you can do:

```css
:root {
	--background-color: white;
	--text-color: black;
}
```

You can also add in other CSS custom properties like creating & using a --headerBG for custom colored header background and --headerTC  for custom colored text in your header for BOTH light and dark mode.

Although you now have creative freedom to put whatever colors you want for your color schemes in both Light and Dark Mode. I would like to remind you to always write your CSS with accessibility in mind. You should always make sure you text is not just legible, but it is actually readable. Make sure that when you are making your light and dark mode that the colors don’t make your text become harder to read. You may need to adjust the colors or even your font size and weight. You should also make sure that when you create these color schemes that any border colors are adjusted/changed so that they are visible in either mode that it is necessary in. Ideally you will use CSS custom properties to easily apply these changes based on which mode the user is using. 

If you would like more information on any of these topics, you can check out [Medium – Light vs Dark Mode](https://medium.com/gumgum-tech/light-vs-dark-mode-debate-prefers-color-scheme-will-answer-d079a5f106aa), [Medium – CSS Accessibility](https://medium.com/@matuzo/writing-css-with-accessibility-in-mind-8514a0007939) and [CSS-Irl](https://css-irl.info/quick-and-easy-dark-mode-with-css-custom-properties/)