---
layout:     post
title:      "Man must explore, and this is exploration at its greatest"
subtitle:   "Problems look mighty small from 150 miles up"
date:       2014-09-24 12:00:00
author:     "Start Bootstrap"
header-img: "img/post-bg-06.jpg"
header-img-credits: "[NASA on The Commons](https://www.flickr.com/photos/nasacommons/){:rel='nofollow'}"
---

<p>Never in all their history have men been able truly to conceive of the world as one: a single sphere, a globe, having the qualities of a globe, a round earth in which all the directions eventually meet, in which there is no center because every point, or none, is center — an equal earth which all men occupy as equals. The airman's earth, if free men make it, will be truly round: a globe in practice, not in theory.</p>

<p>Science cuts two ways, of course; its products can be used for both good and evil. But there's no turning back from science. The early warnings about technological dangers also come from science.</p>

<p>What was most significant about the lunar voyage was not that man set foot on the Moon but that they set eye on the earth.</p>

<p>A Chinese tale tells of some men sent to harm a young girl who, upon seeing her beauty, become her protectors rather than her violators. That's how I felt seeing the Earth for the first time. I could not help but love and cherish her.</p>

<p>For those who have seen the Earth from space, and for the hundreds and perhaps thousands more who will, the experience most certainly changes your perspective. The things that we share in our world are far more valuable than those which divide us.</p>

<h2 class="section-heading">The Final Frontier</h2>

<p>There can be no thought of finishing for ‘aiming for the stars.’ Both figuratively and literally, it is a task to occupy the generations. And no matter how much progress one makes, there is always the thrill of just beginning.</p>

<p>There can be no thought of finishing for ‘aiming for the stars.’ Both figuratively and literally, it is a task to occupy the generations. And no matter how much progress one makes, there is always the thrill of just beginning.</p>

<blockquote>The dreams of yesterday are the hopes of today and the reality of tomorrow. Science has not yet mastered prophecy. We predict too much for the next year and yet far too little for the next ten.</blockquote>

<p>Spaceflights cannot be stopped. This is not the work of any one man or even a group of men. It is a historical process which mankind is carrying out in accordance with the natural laws of human development.</p>

<h2 class="section-heading">Reaching for the Stars</h2>

<p>As we got further and further away, it [the Earth] diminished in size. Finally it shrank to the size of a marble, the most beautiful you can imagine. That beautiful, warm, living object looked so fragile, so delicate, that if you touched it with a finger it would crumble and fall apart. Seeing this has to change a man.</p>

<a href="#">
    <img src="{{ site.baseurl }}/img/post-sample-image.jpg" alt="Post Sample Image">
</a>
<span class="caption text-muted">To go places and do things that have never been done before – that’s what living is all about.</span>

<p>Space, the final frontier. These are the voyages of the Starship Enterprise. Its five-year mission: to explore strange new worlds, to seek out new life and new civilizations, to boldly go where no man has gone before.</p>

<p>As I stand out here in the wonders of the unknown at Hadley, I sort of realize there’s a fundamental truth to our nature, Man must explore, and this is exploration at its greatest.</p>

{% highlight c %}
/*
  Keyboard logout

 This sketch demonstrates the Keyboard library.

 When you connect pin 2 to ground, it performs a logout.
 It uses keyboard combinations to do this, as follows:

 On Windows, CTRL-ALT-DEL followed by ALT-l
 On Ubuntu, CTRL-ALT-DEL, and ENTER
 On OSX, CMD-SHIFT-q

 To wake: Spacebar.

 Circuit:
 * Arduino Leonardo or Micro
 * wire to connect D2 to ground.

 created 6 Mar 2012
 modified 27 Mar 2012
 by Tom Igoe

 This example is in the public domain

 http://www.arduino.cc/en/Tutorial/KeyboardLogout
 */

#define OSX 0
#define WINDOWS 1
#define UBUNTU 2

#include "Keyboard.h"

// change this to match your platform:
int platform = OSX;

void setup() {
  // make pin 2 an input and turn on the
  // pullup resistor so it goes high unless
  // connected to ground:
  pinMode(2, INPUT_PULLUP);
  Keyboard.begin();
}

void loop() {
  while (digitalRead(2) == HIGH) {
    // do nothing until pin 2 goes low
    delay(500);
  }
  delay(1000);

  switch (platform) {
    case OSX:
      Keyboard.press(KEY_LEFT_GUI);
      // Shift-Q logs out:
      Keyboard.press(KEY_LEFT_SHIFT);
      Keyboard.press('Q');
      delay(100);
      Keyboard.releaseAll();
      // enter:
      Keyboard.write(KEY_RETURN);
      break;
    case WINDOWS:
      // CTRL-ALT-DEL:
      Keyboard.press(KEY_LEFT_CTRL);
      Keyboard.press(KEY_LEFT_ALT);
      Keyboard.press(KEY_DELETE);
      delay(100);
      Keyboard.releaseAll();
      //ALT-l:
      delay(2000);
      Keyboard.press(KEY_LEFT_ALT);
      Keyboard.press('l');
      Keyboard.releaseAll();
      break;
    case UBUNTU:
      // CTRL-ALT-DEL:
      Keyboard.press(KEY_LEFT_CTRL);
      Keyboard.press(KEY_LEFT_ALT);
      Keyboard.press(KEY_DELETE);
      delay(1000);
      Keyboard.releaseAll();
      // Enter to confirm logout:
      Keyboard.write(KEY_RETURN);
      break;
  }

  // do nothing:
  while (true);
}
{% endhighlight %}

<p>Placeholder text by <a href="http://spaceipsum.com/">Space Ipsum</a>. Photographs by <a href="https://www.flickr.com/photos/nasacommons/">NASA on The Commons</a>.</p>
