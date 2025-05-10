---
layout: post
title: "My First Foray into Vibe Coding"
date: 2025-05-10 13:31:51 -0600
categories: [Programming]
tags: [vibe-coding]
---

<div style="text-align: center; margin-bottom: 2em;">
<img src="/assets/images/bear-vibe-code.jpeg" alt="A bear coding with good vibes" style="width: 35%;">
<p style="font-style: italic; color: #666; margin-top: 0.5em; font-size: 0.9em;">Created with Gemini using the prompt: Create an image of a bear acting like a human and vibe coding. The screen should contain go source code that is accessing dynamodb. Make it clear that the bear is not working too hard, but is instructing the LLM on how to program.</p>
</div>

Based on all the chatter I've been hearing about vibe coding, I'm late to the party. I don't use AI much in my day-to-day life - my primary use case is generating images like the one at the top of this post to troll my coworkers. However, I do recognize that in the near future (now?) most jobs are going to require some fluency with AI and there will be an expectation that AI tools are used to boost productivity. To get my feet wet with a coding assistant, I decided to use vibe coding to assist me in evaluating a change that we made to some retention logic. The steps I needed to perform are as follows:

1. Retrieve a binary blob from DynamoDB using an id as the key. The key could have one of two prefixes, depending on the environment. Also, the table that the blob is stored in could have one of two names, depending on the environment.
2. Deserialize the binary blob into one of two structures, again depending on the environment.
3. Iterate through the structure, looking for arrays of a particular structure.
4. For any non-nil elements in the array, check whether the timestamp contained in the structure was less than a year old.

<div style="text-align: center; margin: 1em 0;">
<img src="/assets/images/blob.png" alt="Binary blob visualization" style="width: 25%;">
<p style="font-style: italic; color: #666; margin-top: 0.5em; font-size: 0.9em;">Created with Gemini using the prompt: Create a cartoony image of a binary blob running away from DynamoDB</p>
</div>

Up until now, when I had to do something similar, I would just use the AWS command line utility to dump the data from DynamoDB and then copy the data into a Go test case to do the deserializing and pretty printing as JSON (basically, steps 1 and 2). I figured I could replicate this process with some vibe coding, and then manually do steps 3 and 4 by piping the output into a chain of command line tools.

I had a pretty good idea of what this program should look like, and I described the task using phrasing similar to the steps above with some additional detail related to the tables and structures. I was pleasantly surprised that the generated code was almost completely correct on the first try. One bug was due to me providing an incorrect table name, and another one was due to the code attempting to use the `S` (string) value in the returned DynamoDB item instead of the `B` (binary) value. More impressive is that I didn't have to explain which prefix to use for each environment; the system was able to infer it from other code in the repository. Things were going so swimmingly that I vibe coded steps 3 and 4 as well. The only major hiccup was that the program did not initially check for nil array elements for step 4, so the first iteration blew up. That was easy enough to fix, and I soon had a program that completely solved my task. I even added green check mark emoji next to every timestamp that was checked and passed the age test.

I ended up cleaning up the base version of this program that handled steps 1 and 2, added pretty printed JSON output, and added it to the repository as a tool for other folks to use. I should note that the generated code had nice input checking and meaningful error messages which made it easy to determine what the issue was when the program failed.

I've since used AI a bit more to assist me in some development tasks, and it's definitely been hit or miss. One task that is somewhat meta was to develop a container for Jekyll server so that I could preview my blog without polluting my local machine with various Ruby packages. The AI I was using got into a loop where it kept switching between adding and removing ARM-specific directives to the Dockerfile. I eventually just used [this project](https://github.com/BretFisher/jekyll-serve) as a basis for the Dockerfile.

Also, I'm actually writing this blog post with some AI assistance. I used it to create the skeleton of the blog post and to provide some syntax guidance as I get used to Jekyll (it turns out that a lot of it is just the Markdown syntax that we're all familiar with). I also had it do a spellcheck pass before I published the post.

My main takeaway from my experiences this week is that LLMs can definitely be useful in speeding up some coding tasks - especially when the vibe programmer has a well-conceived idea of what the program should look like, the dependencies involved, and the gotchas that might crop up. For example, if someone had never worked with DynamoDB before, and they ran into the `S` vs `B` issue, they might be stuck (though maybe they could have talked it through with the LLM).
