---
layout: post
title: Themes and Navigation
date: 2023-06-22 17:09
author: Ted Bjurlin
tags: [disco-tray]
summary: Three weeks in, and I have finally gotten to the user interface.
---

The Lake Nixon Scheduling app is coming along quite well. I have almost entirely finished the backend of the app, with the exception of a few minor bugs. It is possible to add, edit, and remove appointments, as well as sort them by both group and activity.

I have also done some major refactoring. All of the excess code and unused functions have finally been removed, and the app is much lighter weight. There is only one more major step between the current app and a full beta version: the user interface.

The original UI was quite rough. It had been designed around the colors present in the lake nixon logo: brown, green, and pastel blue and yellow. Although these colors meshed well in the logo, with the green and brown taking center stage, they did not work well in the app UI. This was mostly due the the fact that the yellow did not mesh well with the ther colors, and the blue did not provide the contrast needed in a light mode app.

The first step I took in updataing the UI was to cut the colors used in the app down to white, green, and brown. Due to the simplicity of the app, I decided that it was better to have a simpler palette. (I also don't have the graphic design chops to do much with a more sophisticated palette). With this in mind, the app theme has been rebuilt with the new colors.

While we have been researching the flutter theme system, Simon stumbled upon a very strange behavior of dart's class system. Using the keyword `extension` it is possible to extend the attributes of an existing class. So far, the only abilities we have found is the ability to add getters and static variables said class. What I find so strange about this is that it does not create a new extended class, but rather extends the existing class in any context that has access to the extension. For example:

{% highlight dart linenos %}

class Foo {
    Foo({required this.bar}) {
        String bar;
    }
}

extension on Foo {
    String get baz => 'baz';
}

{% endhighlight %}

Here I create a class called `Foo`, with a single field. Anywhere this class instantiated, it is possible to access that field. If the extension, which does not need to be name, is imported, `Foo` now has a gettercalled baz, which returns `baz`. The new field is not, however, included in `Foo`'s original constructor. This means that the value of `baz` is essentially static. It can be changed with a setter, but it will always have the same inital value.

The application that we found for this strange behavior was the ability to extend the Flutter `ColorScheme` and `TextTheme` classes used in the theme with custom fields. The existing names for the fields offered by these classes were not nearly descriptive enough, and became confusing, so I added my own, such as the `Color` `nixonBrown` in the `ColorScheme` class and the `TextStyle` `appBarTitle` in the `TextTheme` class. While this has worked great for me, as I only need a single field, the static nature of dart extensions became a stumbling block for Simon. In his app, Hendrix Today, he had to implement a light and a dark theme, and being unable to change the values of the new fields with constructor meant that he couldn't switch between the themes on the fly. In the end he had to switch back to using the basic fields included in the classes.

More recently, I have been playing around with the layouts and designs of some of the apps pages, in the hopes of discovering a consistent style to build the UI around. So far, I have been somewhat successful, and I hope to finish in the next week.

We have also decided on a new title font for our app. The students in the original class had picked a handwriting-style font called Fruit Days, to match the summer camp vibes of the app. However, this font has proved to be difficult to read, and more importantly, is only licensed for personal use. Now, after trying a couple of others, we have settled on Itim, another handwriting-style font that is provided through Google Fonts. This time, it has an open license and is significantly more legible.

With these large changes, we are very close to a final prototype, and soon I expect to be moving on to another app from our pile.