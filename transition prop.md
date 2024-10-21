In **Framer Motion**, the `transition` property is used to define how animations should behave over time, allowing you to control the duration, easing, delay, and other aspects of your animations. You can apply the `transition` property on elements that are being animated using the `motion` component.

### Common `transition` properties:

1. **duration**: Sets how long the animation should last (in seconds).
   ```js
   transition: { duration: 0.5 }
   ```

2. **ease**: Defines the easing function for the animation. You can use predefined ease types like `easeIn`, `easeOut`, `easeInOut`, or even a custom cubic-bezier curve.
   ```js
   transition: { ease: "easeInOut" }
   ```

3. **delay**: Adds a delay (in seconds) before the animation starts.
   ```js
   transition: { delay: 0.2 }
   ```

4. **stiffness** (for spring animations): Controls how stiff the spring is, affecting the "bounciness" of the animation.
   ```js
   transition: { type: "spring", stiffness: 100 }
   ```

5. **damping** (for spring animations): Reduces the oscillation in spring animations.
   ```js
   transition: { type: "spring", damping: 20 }
   ```

6. **mass**: The mass of the spring system, impacting the animation speed.
   ```js
   transition: { type: "spring", mass: 0.5 }
   ```

7. **repeat**: Specifies how many times the animation should repeat. It can also take `Infinity` for endless repetition.
   ```js
   transition: { repeat: 2 }
   ```

8. **repeatType**: Determines the type of repeat: `loop`, `reverse`, or `mirror`.
   ```js
   transition: { repeat: Infinity, repeatType: "reverse" }
   ```

9. **type**: Specifies the type of animation, either `"tween"` (default) or `"spring"`.
   ```js
   transition: { type: "tween", ease: "linear" }
   ```

### Example Usage:
```jsx
<motion.div
  animate={{ x: 100 }}
  transition={{ duration: 0.5, ease: "easeInOut" }}
  
>
  Move me!
</motion.div>
```

In this example, the div will move 100 pixels on the x-axis over 0.5 seconds with an ease-in-out effect.