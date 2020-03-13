## [TIP] SafeAreaView: *top/bottom only*

```javascript
import SafeAreaView from *react-navigation*
```

instead of 

```javascript
import SafeAreaView from *react-native*
```

Then, manage the props `forceInset={{ top: 'never', bottom: 'always' }}`, for example, if you dont want the SafeView on *top* (and vice versa).

[Link 1](https://github.com/facebook/react-native/issues/18825#issuecomment-396179883)