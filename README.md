# react-native-animatable
Standard set of easy to use animations for React Native

## Installation

`$ npm install react-native-animatable --save`

## Usage

To animate things you must use the `createAnimatableComponent` composer similar to the `Animated.createAnimatedComponent`. The common components `View`, `Text` and `Image` are precomposed and exposed under the `Animatable` namespace. If you have your own component that you wish to animate, simply wrap it with a `Animatable.View` or compose it with:

```js
var Animatable = require('react-native-animatable');
MyCustomComponent = Animatable.createAnimatableComponent(MyCustomComponent);
```

### Declarative Usage

```html
<Animatable.Text animation="zoomInUp">Zoom me up, Scotty</Animatable.Text>;
```

#### Properties
*Note: Other properties will be passed down to underlying component.*

| Prop | Description | Default |
|---|---|---|
|**`animation`**|Name of the animation, see below for available animations. |*None*|
|**`duration`**|For how long the animation will run (milliseconds). |`1000`|
|**`delay`**|Optionally delay animation (milliseconds). |`0`|

### Imperative Usage

All animations are exposed as functions on Animatable elements, they take an optional `duration` argument.

```js
var Animatable = require('react-native-animatable');

React.createClass({
  render: function() {
    return (
      <TouchableWithoutFeedback onPress={() => this.refs.view.bounce(800);>
        <Animatable.View ref="view">
          <Text>Bounce me!</Text>
        </Animatable.View>
      </TouchableWithoutFeedback>
    );
  }
};
```

## Demo / Example

See `Example` folder. 

![animatable-demo](https://cloud.githubusercontent.com/assets/378279/10567141/079de586-75c9-11e5-8ea4-e63c0176f519.gif)

## Animations

Animations are heavily inspired by [Animated.css](https://daneden.github.io/animate.css/).

### Attention Seekers

* `bounce`
* `flash`
* `jello`
* `pulse`
* `rubberBand`
* `shake`
* `swing`
* `tada`
* `wobble`

### Bouncing Entrances

* `bounceIn`
* `bounceInDown`
* `bounceInUp`
* `bounceInLeft`
* `bounceInRight`

### Bouncing Exits

* `bounceOut`
* `bounceOutDown`
* `bounceOutUp`
* `bounceOutLeft`
* `bounceOutRight`

### Fading Entrances

* `fadeIn`
* `fadeInDown`
* `fadeInDownBig`
* `fadeInUp`
* `fadeInUpBig`
* `fadeInLeft`
* `fadeInLeftBig`
* `fadeInRight`
* `fadeInRightBig`

### Fading Exits

* `fadeOut`
* `fadeOutDown`
* `fadeOutDownBig`
* `fadeOutUp`
* `fadeOutUpBig`
* `fadeOutLeft`
* `fadeOutLeftBig`
* `fadeOutRight`
* `fadeOutRightBig`

### Flippers

* `flipInX`
* `flipInY`
* `flipOutX`
* `flipOutY`

### Lightspeed

* `lightSpeedIn`
* `lightSpeedOut`

### Sliding Entrances

* `slideInDown`
* `slideInUp`
* `slideInLeft`
* `slideInRight`

### Sliding Exits

* `slideOutDown`
* `slideOutUp`
* `slideOutLeft`
* `slideOutRight`

### Zooming Entrances

* `zoomIn`
* `zoomInDown`
* `zoomInUp`
* `zoomInLeft`
* `zoomInRight`

### Zooming Exits

* `zoomOut`
* `zoomOutDown`
* `zoomOutUp`
* `zoomOutLeft`
* `zoomOutRight`


## License

[MIT License](http://opensource.org/licenses/mit-license.html). © Joel Arvidsson 2015
