## [ERROR] Invariant Violation: Text strings must be rendered within a <Text> component

I've shot myself in the foot too many times over this, so I'm leaving this here for the next person not to...

Whenever you see this error, 99% of cases will be caused by using conditional rendering with only `&&` instead of ternary `? :` statements. 
Why? Because when your condition resolves to `undefined`, there are no components there, as opposed to null or an empty array which would have safely showed an empty space and save your life from the red screen of hell.

Change ALL OF YOUR LOGICAL CONDITIONAL RENDERS into ternary renditions.

ie:
```javascript
// DON'T DO
widgetNumber === 10 && <MyComponent />

// DO DO
widgetNumber === 10 ? <MyComponent /> : null
```
Every. Single. Time. Please. For the love of React Native.
  
[Link](https://stackoverflow.com/a/59108109)

## [TIP] React Native Paper: Accordion.Item with inherited margin left from Accordion.List with left icon

Wrap `Accordion.List` children with Fragments! **Fragments don't inherit the styling props from their parent components.**

[Link](https://stackoverflow.com/a/71400227)
