### PathObjects - Revealing Object Interactions to Assist Developers in Program Comprehension

#### Abstract

Program comprehension is a tedious necessity during software development with complex cognitive demands.
Reportedly, it amounts to up to 60% of the software engineering time and labor.
One reason that makes program comprehension such a time-consuming activity is that it requires developers to bridge a gap of abstraction levels.
Namely, the low-level abstractions of the inner workings of computers and the high-level abstractions of object-oriented programming languages and design documents diverge. 
Unfortunately, widespread development tools contribute little to bridge this gap, and present information about program behavior with technical views instead of adapting to the abstractions of object-orientation.
However, to close this gap, an information presentation at the abstraction level of objects and their interactions would be desirable, which in turn could contribute to reduce the time required for program comprehension.

Therefore, this thesis presents PathObjects, an interactive way of diagraming program behavior at the abstraction level of object interactions. 
It allows developers to navigate and explore execution traces through an immediate information presentation while maintaining a low memory footprint.
We put this concept into practice with an implementation for the Squeak/Smalltalk environment. 
With the aid of a user study, we show that PathObjects can help developers to comprehend an unknown software system faster and to a higher degree compared to the standard development tools.
We conclude that our concept can assist developers in object-oriented program comprehension by closing the gap of abstraction levels, and thus represents a step towards the reduction of the required time of this laborious activity.

#### Download Thesis

The LaTeX sources and a precompiled PDF version are available [here](https://github.com/leoschweizer/PathObjects-Thesis/releases/tag/v1.0).

***

### Building

**Requirements**
  * [MiKTeX](http://miktex.org)
  * Install latest `caption` package ([trunk](http://sourceforge.net/p/latex-caption/code/HEAD/tree/trunk/tex/))
  * [R](http://www.r-project.org) 3.0 or newer
  * [Graphviz](http://graphviz.org) 2.34 or newer
  * [ImageMagick](http://www.imagemagick.org) in case you want to use the `thumbs` task
  
**Build**

    $ git clone git@github.com:leoschweizer/PathObjects-Thesis.git
    $ cd PathObjects-Thesis
    $ rake
    
***

### Sneak Peek

![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page1.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page2.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page3.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page4.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page5.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page6.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page7.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page8.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page9.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page10.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page11.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page12.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page13.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page14.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page15.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page16.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page17.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page18.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page19.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page20.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page21.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page22.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page23.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page24.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page25.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page26.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page27.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page28.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page29.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page30.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page31.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page32.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page33.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page34.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page35.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page36.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page37.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page38.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page39.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page40.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page41.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page42.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page43.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page44.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page45.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page46.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page47.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page48.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page49.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page50.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page51.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page52.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page53.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page54.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page55.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page56.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page57.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page58.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page59.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page60.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page61.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page62.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page63.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page64.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page65.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page66.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page67.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page68.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page69.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page70.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page71.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page72.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page73.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page74.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page75.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page76.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page77.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page78.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page79.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page80.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page81.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page82.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page83.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page84.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page85.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page86.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page87.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page88.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page89.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page90.png)
![](http://leoschweizer.github.io/PathObjects-Thesis/thumbs/page91.png)

***

### License

<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="Creative Commons License" style="border-width:0" src="http://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a><br />This <span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/Text" rel="dct:type">work</span> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a>.
