---
layout: page
title: Animations in Flutter
permalink: /animations/
---

* TOC Placeholder
{:toc}

Well-designed animations makes a UI feel more intuitive,
contribute to the slick look and feel of a polished app,
and improve the user experience. Flutter's animation support
makes it easy to implement a variety of animation types.
Many widgets, especially
[Material Design widgets](https://flutter.io/widgets/material/),
come with the standard motion effects defined in their design spec,
but it's also possible to customize these effects.

The following resources are a good place to start learning the Flutter
animation framework. Each of these docs shows, step by step, how
to write animation code.
Note that more docs are in the works on how to implement common design patterns,
such as shared element transitions, and physics-based animations.
If you have a specific request, please
[file an issue](https://github.com/flutter/flutter/issues).

* [Tutorial: Animations in Flutter](/animations/animation-tutorial.html) <img src="/images/ic_new_releases_black_24px.svg"> NEW<br>
Explains the fundamental classes in the Flutter animation package
(controllers, Animatable, curves, listeners, builders),
as it guides you through a progression of tween animations using
different aspects of the animation APIs.

* [Zero to One with Flutter, part
1](https://medium.com/dartlang/zero-to-one-with-flutter-43b13fd7b354) and [part
2](https://medium.com/dartlang/zero-to-one-with-flutter-part-two-5aa2f06655cb)<br>
Medium articles showing how to create an animated chart using tweening.

* [Building Beautiful UIs with
Flutter](https://codelabs.developers.google.com/codelabs/flutter/index.html#0)<br>
Codelab demonstrating how to build a simple chat app. [Step 7 (Animate
your app)](https://codelabs.developers.google.com/codelabs/flutter/index.html#6)
shows how to animate the new message&mdash;sliding it from the input area up
to the message list.

## Animation types

Animations fall into one of two categories: tween- or physics-based.
The following sections explain what these terms mean, and points you to
resources where you can learn more. Note that, in some cases,
the best documentation we currently have is example code in the
Flutter gallery. More docs and examples will be forthcoming.

### Tween animation

Short for _in-betweening_. In a tween animation, the beginning
and ending points are defined, as well as a timeline, and a curve
that defines the timing and speed of the transition.
The framework calculates how to transition from the beginning point
to the end point.

The docs listed above, such as the [animations
tutorial](/animations/animation-tutorial.html) aren't about tweening,
specifically, but they use tweens in their examples.

### Physics-based animation

In physics-based animation, motion is modeled to resemble real-world
behavior. When you toss a ball, for example, where and when
it lands depends on how fast it was tossed, how heavy it is, and how
far off the ground. Similarly, dropping a ball attached to a spring falls
(and bounces) differently than dropping a ball attached to a string.

Note that more docs and examples on physics-based animations will be
forthcoming.

* [Flutter Gallery](https://github.com/flutter/flutter/tree/master/examples/flutter_gallery)<br>
Under **Material Components**, the
[Grid](https://github.com/flutter/flutter/blob/master/examples/flutter_gallery/lib/demo/material/grid_list_demo.dart) example
demonstrates a fling animation. Select one of the images from
the grid and zoom in. You can pan the image with flinging or dragging
gestures.

* Also see the API docs for
[AnimationController.animateWith](https://docs.flutter.io/flutter/animation/AnimationController/animateWith.html) and
[SpringSimulation](https://docs.flutter.io/flutter/physics/SpringSimulation-class.html).

## Common animation patterns

Most UX or motion designers find that certain animation patterns are
used repeatedly when designing a UI. This section lists some of the commonly
used animation patterns, and tells you where you can learn more.

### Animated list or grid
This pattern involves animating the addition or removal of elements from a
list or grid.

* [AnimatedList example](/catalog/samples/animated-list/)<br>
This demo, from the [Sample App Catalog](/catalog/samples), shows how to
animate adding an element to a list, or removing a selected element.
The internal Dart list is synced as the user modifies the list using
the plus (+) and minus (-) buttons.

### Shared element transition

In this pattern, the user selects an element&mdash;often an
image&mdash;from the page, and the UI animates the selected element
to a new page with more detail. In Flutter, you can easily implement
shared element transitions between routes (pages) using the Hero widget.
Hero animations can also occur in a dialog,
rather than being routed to a new page.

* [Flutter Gallery](https://github.com/flutter/flutter/tree/master/examples/flutter_gallery)<br>
You can build the Gallery app yourself, or download it from the Play Store.
The [Shrine](https://github.com/flutter/flutter/blob/master/examples/flutter_gallery/lib/demo/shrine_demo.dart)
demo includes an example of a hero animation.
{% comment %}
According to Hans, the demo in the Flutter Gallery that is called
"Animation" isn't really an animation demo. It's more of a
"scroll driven layout demo".
{% endcomment %}

* Also see the API docs for the
[Hero,](https://docs.flutter.io/flutter/widgets/Hero-class.html)
[Navigator,](https://docs.flutter.io/flutter/widgets/Navigator-class.html) and
[PageRoute](https://docs.flutter.io/flutter/widgets/PageRoute-class.html)
classes.

{% comment %}
### Staggered animation
We have nothing to show yet.
{% endcomment %}

## Other resources

Learn more about Flutter animations at the following links:

* [Animations: Technical Overview](/animations/overview.html)<br>
A look at some of the major classes in the animations library,
and Flutter's animation architecture.

* [Animation and Motion Widgets](/widgets/animation/)<br>
A catalog of some of the animation widgets provided in the Flutter APIs.

{% comment %}
Until the landing page for the animation library is reworked, leave this
link out.
* The [animation
library](https://docs.flutter.io/flutter/animation/animation-library.html)
in the [Flutter API docs](https://docs.flutter.io/)<br>
The animation API for the Flutter framework.
{% endcomment %}

<hr>

We are currently working on creating more animation docs and examples.
If there is something specific you'd like to see, please
[file an issue](https://github.com/flutter/flutter/issues).
