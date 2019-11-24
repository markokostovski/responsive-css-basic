# Responsive css basic

Goal of this course would be to explain how to properly use responsive and regular css in mid-to-big sized projects.
Examples are simplified, and the principles and "way of thinking" is more important than the code. In smaller projects there is no real need for abstractions like this, since it can be considered "overcomplicated". But on bigger project, it's impossible to do it otherwise

## Selectors

For selectors, you should use element and class. When you name your class, it would be good to define at a bit more, and have some sort of pattern for pages/components
`.page-homescreen-background` or
`homescreen-bacground` for pages
`compenent-header-logo` or
`header-logo` for components
Naming classes like that are pretty useful if you don't use module imports or css-in-js. In that way you would know class origin only from reading i it's name.
You could take a look at `BEM` online (although I don't prefer it, maybe someone reading this would suit it's taste more)

Important! Use different attributes for js selectors if possible,
`<a data-onclick="open-modal" href="#">Click me</a>` is `$('[data-onclick]')..` in jQuery, and would make your life easier over time since you would separate css in js selectors.
What is also really good in this is that you can add values to your selectors, making your code much more declarative. [https://codeburst.io/declarative-vs-imperative-programming-a8a7c93d9ad2](https://codeburst.io/declarative-vs-imperative-programming-a8a7c93d9ad2)
Other solution would be to use prefixes for js selectors `js-onclick-open-modal`.

## File abstraction

Learn to think in "components", and whichever component would be re-used, it makes sense to add it in different css file. If it's something unique only on 1 page, but not on every component, put it on "page" level.
Use themes for variables and css rules on that theme, and general for something that is needed on EVERY page, component and whole project
