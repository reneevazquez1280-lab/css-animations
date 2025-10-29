# css-transition

## Learning Target
- I am reviewing box model properties, flex containers, and hover selectors 
- I am learning how to use the CSS transition and transform properties to automatically animate between two states

## Success Criteria
- I can set initial and :hover or :active properties for an element in CSS (colors, border, position, etc.)
- I can use the transition property to animate the transition to the hovered state
- I can use the transform property to scale, rotate, or translate an element



## Get started
1. Install Live Server and Go Live to view how the webpage looks with no styling
2. Follow directions below

## 1. Define animations with ```@keyframes```
### Option A: Use from and to
```from``` should contain the properties/values at the beginning of the animation.  
```to``` should contain the properties/values at the end of the animation.
```css
@keyframes animation-name {
    from {
        /* starting properties */
    }

    to {
        /* ending properties */
    }
}
```
### Option B: Use percentages
Define values at specific percentages of the animation. You can specify any percentage values for steps in the animation.
```css
@keyframes animation-name {
    0% {
        /* starting properties */
    }
    25% {
        /* properties after 25% of time as elapsed */
    }
    50% {
        /* properties at 50% */
    }
    75% {
        /* properties at 75% */
    }
    100% {
        /* properties at 100% (the end) */
    }
}
```
### Common properties to animate
```css
background-color:
color:
transform: scale() | rotate() | translate() | skew();
opacity: /* 0 is fully transparent, 1 (or 100%) is fully opaque */
```

## 2. Apply animation to a selector
```css
selector {
    animation: name duration timing-function;
}
```
For example:
```css
img {
    animation: spin 1s linear;
}
```
You can *optionally* set other properties to control how the animation behaves
```css
selector {
    animation: name duration timing-function;
    animation-iteration-count: infinite; /* repeat infinitely or a specific number of times */
    animation-delay: 1s; /* start animation after 1s */
    animation-fill-mode: forwards; /* The element will keep its ending animation properties */
}

```

## Transform property
```css
selector {
    transform: translate(x, y) | scale(%) | rotate(deg) | skew(deg, deg);
}
```