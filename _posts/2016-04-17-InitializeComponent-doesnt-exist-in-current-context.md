---
layout: post
title: "InitializeComponent doesn't exist in current context"
gh-repo: leif-larsen/leif-larsen.github.io
gh-badge: [star, fork, follow]
comments: true
image: /img/2016/04/screenshot.png
---
    
At Build 2016 it was announced that Xamarin would be included with Visual Studio, at no extra cost. It would also be included with Visual Studio Community Edition, rendering it completely free, which is great news. Anyway, when the update for Visual Studio became available I installed it and went to test my Xamarin apps with Visual Studio. 

Unfortunately, though, I ran into an issue with compilation. The compiler was complaining that <code>InitializeComponent()</code> did not exist in current context. This specific method is called in the constructor in the code-behind of a XAML file, and it is a method coming from the Xamarin package included. 

##Solution

Normally an error like this could be fixed by rebuilding the project, but in this case it didn't work. What I had to do to solve this was to open all XAML files and save the files. When this was done, the project built as expected, and I were able to test it. I am not sure what caused this problem, but luckily the fix wasn't to hard too find or execute (at least if you don't have tons of XAML files).

