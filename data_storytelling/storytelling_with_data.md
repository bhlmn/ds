Notes on data storytelling while reading [Storytelling with Data](http://www.storytellingwithdata.com/) by Cole Nussbaumer Knaflic.

## 1 | The importance of context

### Exploratory analysis

Exploratory analysis differs completely from explanatory analysis. The latter is _not_ about telling everything you've learned. Rather, it is about effectively communicating **only** the information your audience needs to know. To make this easier, answer a few simple questions *before* crafting your story:

* Who is your audience (be specific)? What is their relationship to you? How can you best resonate with them?
* What do you want your audience to know or do? If recommending an action, make the call to action clear!
  * Once you identify this, make sure that **every** part of your story supports this goal and this goal only.
* How will you communicate?
  * If a live presentation, practice it to many friends and/or colleagues.
  * If a written document, have these same folks read, edit, and make comments. The more iterations the better.

Only *after* these questions have been answered should you start to think: **what data are available that will help make my point?**

### The 3-minute story & Big Idea

You should be able to strip the "so-what" down to a paragraph or even *a single sentence*. The 3-minute story is self explanatory, and the author provides a great [example of one](http://www.storytellingwithdata.com/blog/2014/02/the-3-minute-story). A 3-minute story contains the Big Idea, which is an even more concise version of your message.

The Big Idea must:
* articulate your unique point of view
* convey what's at stake
* be a complete sentence.

An example can be found [here](http://www.storytellingwithdata.com/blog/2014/02/whats-big-idea). Identifying (and practicing) your 3-minute story and Big Idea ahead of item not only keeps your story focussed, it provides the ability to tell your story even if your allotted time gets cut in half on the spot!

### Storyboarding

[Storyboarding](http://www.storytellingwithdata.com/blog/2015/8/24/how-i-storyboard) is the process of establishing a structure/visual outline of what you want to communicate. Grab a white-board or table, post-it notes, and/or a plain peice of paper. Write each point of your story on a separate post-it note ... than start organizing! Make sure to have your Big Idea on one of the post-its. It might belong at the end **and** the beginning!

## 2 | Choosing an effective visual

There are many types of visuals, but the author typically uses one of a select list ...

### Simple text

When you only have one or two numbers that you want to communicate, it can be very effective to just put up the number(s)! For example:

![simple text example](https://static1.squarespace.com/static/55b6a6dce4b089e11621d3ed/55b6d08fe4b0d8b921b02f83/55b6d0a5e4b0d8b921b03644/1438044325129/1000w/)

### Tables

While not the go to for communicating information (especially for presentations), tables can be the tool of choice in written reports when the audience is mixed (and therefore looking for different things).

* Make sure to minimize borders ... make them really light or get rid of them: highlight just the data!
* Sort the data in a way that is [meaningful to your audience](http://www.storytellingwithdata.com/blog/2012/01/tables-that-make-sense).

### Heatmaps

### Scatterplots

### Line graphs

* Very useful for plotting continuous data, such as time series!
* Make sure to highlight what is really important!
* Put categorical labels on the right in matching color.
* Include final values with the label!
* Annotate them! Check out [this page](http://www.storytellingwithdata.com/blog/2018/1/22/88-annotated-line-graphs) for 88 examples of annotated line graphs!

![Austin DWIs](https://static1.squarespace.com/static/55b6a6dce4b089e11621d3ed/t/58d55b28e4fcb5243dcd92b2/1490377517580/?format=750w)

### Slopegraphs

* Typically not useful if many of the lines overlap.
* Make sure to draw attention to what you are trying to communicate.

![slopegraph example](https://static1.squarespace.com/static/55b6a6dce4b089e11621d3ed/55b6d08fe4b0d8b921b02f83/55b6d094e4b0d8b921b0315f/1438044308816/1000w/)

### Bar charts

These are great when dealing with categorical data. Some best practices:
* Go horizontal if you can! This causes the data to be viewed by the audience naturally (zigzagging from left to right, top to bottom).
* Place the most important category at the top!
* **Always** have a zero baseline.

![horizontal bar example](https://static1.squarespace.com/static/55b6a6dce4b089e11621d3ed/55b6d08fe4b0d8b921b02f83/55b6d0a0e4b0d8b921b034cd/1438044320231/1000w/)
![horizontal bar example 2](https://static1.squarespace.com/static/55b6a6dce4b089e11621d3ed/55b6d08fe4b0d8b921b02f83/55b6d0b5e4b0d8b921b039a6/1438044341384/1000w/)

Bar charts can also be stacked:

![stacked horizontal bar chart](https://static1.squarespace.com/static/55b6a6dce4b089e11621d3ed/t/5a0b4d0f71c10b438dd70604/1510690072500/Stacked+bar+-+example+from+book.png?format=750w)

Or can be turned into [waterfall charts](http://www.storytellingwithdata.com/blog/2011/11/waterfall-chart):

![waterfall chart](https://static1.squarespace.com/static/55b6a6dce4b089e11621d3ed/55b6d08fe4b0d8b921b02f83/55b6d0b5e4b0d8b921b03993/1438044341235/1000w/)

### Area charts

Area charts are to be avoided *unless* comparing numbers that differ greatly in magnitude. When this is the case, a square area chart works much better than a typical bar chart:

![square area chart](https://static1.squarespace.com/static/55b6a6dce4b089e11621d3ed/55b6d08fe4b0d8b921b02f83/55b6d09ee4b0d8b921b03421/1438044318757/1000w/)

Other than that, **don't show area charts** (pie charts, donut charts, etc.). Also, don't use 3D. It might look fancy, but it hurts interpretability.

Also, in case where you are tempred to use a secondary y-axis, *don't do it*! Instead either label the points of the second axis directly or split the graphs vertically, in either case letting them share the same x-axis:

![two y axes](https://static1.squarespace.com/static/55b6a6dce4b089e11621d3ed/55b6d08fe4b0d8b921b02f83/55b6d0b8e4b0d8b921b03a9c/1438044344273/1000w/)

## 3 | Clutter is your enemy

The cognitive supply of your audience is *finite*, and each element you put in front of them drains some of that supply. Thus, you should remove any elemnt whose informational value is outweighted by the cognitive load it demands. The more we remove unnecessary elemtns, the more the data stand out (which is what we want!).

### Maintain visual order

> "When design is thoughtful, it fades into the background so that your audience doesn't even notice it. When it's not, your audience feels the burden."

Some guidelines for maintaining visual order:
* Upper-left justify text (and put information at the upper left so people see it first!) ... don't center align.
* Avoid diagonally or vertically oriented text. It takes longer to process.
* Lighten most text. It isn't the star -- the data are.
* Pair grouped data and text with colors (try not to draw lines).
* The more whitespace the better! Whitespace helps draw attention to what *isn't* whitespace.

> "The more things we make different, the less ... [they] stand out."

Thus, if we want to emphasize just *one thing*, then make that *one thing* different from the rest. Don't give all of the groups different colors if you really only want to highlight one of the groups.

### Decluttering step by step

[Here](http://www.storytellingwithdata.com/blog/2017/3/29/declutter-this-graph) is a good example. Also check out [this video](https://www.youtube.com/watch?v=X79o46W5plI).

![declutter example](https://static1.squarespace.com/static/55b6a6dce4b089e11621d3ed/t/58dbf3cc59cc68c3b0a33458/1490809812854/?format=1000w)

* In short, take a look at an image and ask, "what can I live without". Choose one thing at a time until you can't lose any more elements.
* Then think about how the remaining elements can be changed to more effectively tell your story.

## 4 | Focus your audience's attention

Leverage preattentive attributes so that your audience can pick up the point you are trying to make without having to dedicate any concious thought to it. One preattentive attribute is color, which is helpful in this exercise: how many 3s are in the pictures below?

![3s](https://kathep.com/site/assets/files/3417/screen_shot_2017-10-16_at_1_03_03_pm.png)  ![3s with color](https://kathep.com/site/assets/files/3417/screen_shot_2017-10-16_at_1_03_12_pm.png).

The second image made it *much* easier. Since the 3s stand out, your brain counts them without even trying. Thus, preattentive attributes, when used strategically, *"... enable our audience to see what we want them to see before they even know they're seeing it!"* Here are the many preattentive attributes:

![preattentive attributes](https://kathep.com/site/assets/files/3417/screen_shot_2017-10-16_at_1_03_22_pm.png)

In each one of these examples, we instinctively notice the one element that stands out from the rest. Thus, these attributes should be used sparingly (if everything is made to stand out, nothing will).

### Preattentive attributes with text

With text, color, bold, and italics (in decreasing order) are useful for creating a visual hierarchy. This allows us to display a lot of information, of which its summary can quickly be absorbed. For example:

![visual hierarchy](https://kathep.com/site/assets/files/3417/screen_shot_2017-10-16_at_1_03_50_pm.png)

In this image we can understand key points in only a few seconds (because they stand out), and then we can get more detailed information after our interest is peaked and we already understand the key points.

### Preattentive attributes in figures

Some figures, even after decluttering, can contain overwhelming amounts of information. Devoid of preattentive attributes, the audience is then left to their own devices to process all of this information and discern what we *really* want them to understand. It's up to us to focus the story. Notice the difference in the two images below:

![design concerns](https://kathep.com/site/assets/files/3417/screen_shot_2017-10-16_at_1_04_00_pm.png)  ![design concerns improved](https://kathep.com/site/assets/files/3417/screen_shot_2017-10-16_at_1_04_14_pm.png)

In the figure at right it's *much* easier to understand the point of the figure. The presenter wants us to know that noise is a common design concern. This story is all but lost in the original figure, and it only took a small bit of color to focus the story. In live presentation settings, one effective strategy is displaying the same visual again and again with different pieces emphasized to tell different stories or different aspects of a story.

**Note! When one point of a figure is highlighted it becomes more difficult to see the rest of the information. Thus, avoid preattentive attributes during exploratory analysis, as you can miss out on some key insights!"**

Here is a checklist for deciding how to use preattentive attributes to focus your audience's attention on what matters:

1. Declutter
2. Push everything to the background (so nothing stands out)
3. Make the data stand out
4. If you don't want the focus to be the upper left of the figure (that's where eyes go by default!), use preattentive attributes to your advantage

Note how selectively adding data markers and simple color changes focusses the attention to the right side of the graph:

![received-processed-original](https://kathep.com/site/assets/files/3417/screen_shot_2017-10-16_at_1_04_40_pm.png) ![received-processed-final](https://kathep.com/site/assets/files/3417/screen_shot_2017-10-16_at_1_05_22_pm.png)

#### Size

The size of figure elements intuitively communicates important: big elements grab attention! Thus, if elements have equal importance, make them the same size! Failing to do this can have big consequences!

#### Color

This is one of the best tools in your toolkit. The author recommends designing visuals in shades of grey (allowing for greater contrast), and picking one "attention-grabbing" color (such as blue) to highlight important elements.

When using color:
* **use it sparingly**.
