# Pre-Intro
Many people believe that as time goes on, GPT-4 becomes less effective. I, on the other hand, think it's becoming more laid-back. Here's what you can do about it.

# Introduction
In this section, I aim to share the prompts and strategies I use to maximize the potential of this model. There will be sources cited and examples illustrated through screenshots.

### Why this introduction? 
I encountered a scenario where a prominent YouTuber complained that Custom GPT wasn't integrating well with their Knowledge Base and wasn't performing as expected. They lamented that GPT-4's effectiveness deteriorates over time.

Contrary to this, I not only manage to consistently direct it to access the Knowledge Base - sometimes multiple times in a single action - but I also don't feel that it's getting worse. It may be a bit more laid-back, which means we need to interact with it differently and apply more pressure, but it's certainly not deteriorating in quality.

[screenshot comparison: theirs vs. mine]

### Conclusion: 
Knowing how to prompt effectively turns you into a real expert in this field because you can simply achieve more.

### Disclaimer: 
This is not to discredit those who haven't mastered this control. It's just that, as in many areas of life, there's always room for improvement, and here I want to show what can be done better.

## Getting Down to Business
Skip using the "Builder" function, and write prompts in your own style.

[screenshot]

## Repetition
A fundamental observation is the need for extensive repetition of key elements in the prompts. This is almost to the point of excess. Various experiments have shown that the model often focuses on the beginning and end of inputs while sometimes neglecting the middle. This is where it tends to be 'lazy'. [source link]
Therefore, repeating crucial elements increases the likelihood that the model will perform the desired actions and not overlook anything.

However, this approach has a drawback: if we emphasize and repeat, we're just using more characters to convey our intentions, and the character count is limited. In Custom Instructions within the GPT Chat interface, it's 1500 characters, and in Custom GPT, it's 8000 characters.

[screenshots]

## Using Variables
Since we'll be repeating to increase our chances of getting what we want but also need to save on character count, we can start using something akin to programming variables.
How do we do this? 

[screenshot]

### Example: 
I relentlessly remind the model to use a specific .txt file, mentioning it repeatedly in different parts of the prompt. Instead of rewriting the .txt file's name each time, I define a variable at the top of the prompt, such as SAINT FILE = {here goes the .txt filename}.
Then, throughout the prompt construction, I use this SAINT FILE variable. It not only saves characters but also eliminates the need to repeatedly write out the long filename, which is especially handy in Custom GPT scenarios involving frequent Knowledge Base modifications.
This approach simplifies the process; you only need to change the file name in the variable once, replace the file in the Knowledge Base, and everything works seamlessly.

[screenshots]

## Assertive Language
Another important aspect is the use of assertive language. Experiments have shown that LLMs (large language models) can be 'emotionally manipulated' or persuaded using assertive language. [source link]
For instance, expressing frustration can prompt the model to put in extra effort to alleviate that frustration, thus overcoming its 'laziness'.

[screenshot]

## Tipping
Another trick, as described in various sources and well-tested, involves motivating the model with a hypothetical reward. For example, writing something like, "don't be lazy, and if you do well, I'll tip you not 5 or 10 dollars, but 200 dollars. Do we have a deal?" This approach can improve the quality of the results. [source link]

## Custom Instruction Creator by @DaveShapiro
When crafting Custom Instructions for the interface or system prompt for Custom GPT or API calls, it's beneficial to use a prompt creator that turns a user's draft into a system prompt. I learned this trick from @DaveShapiro and often use it to create a framework.

[screenshot]

With this framework, you can:
1. Place variables at the top,
2. Add various reminders like "this is crucial," "that's absolutely important to notice that [...]," etc.

## Specifying Specific Tools
Once you have this skeleton and start creating the actual custom prompt, you can request specific functionalities. For example, "I want to see the Code Interpreter running".

## Confirmation Step
Then, you can specify that after each step performed by the custom GPT in a query, it should confirm the action in 5-10 words. This ensures it doesn't skip steps and completes each task as required.

[screenshot]

## Including Specific Functions
If the Code Interpreter successfully performs an action during testing in development mode, note the function it used. If it's successful, expand on it, see which function it used, and then include that specific function in your system prompt.

[screenshots]

This way, if you've figured out a successful approach through testing, you don't need to leave the model to guess. You can specifically direct it: "In this particular instance, use this function." Including this in your system prompt is another way to gain control.

## Structuring the Output
Similarly, you can specify exactly how the output should be structured, detailing its exact format.

[screenshot]

# To Wrap It Up
This is why I talked about using variables at the top and saving characters. These are the places where you need to insert functions, specify output structure, etc., and this is where the character count becomes crucial.
Always try to reduce instructions to a formula or variable and place it at the top to save characters.

[screenshot]

Finally, as mentioned earlier, we shouldn't leave decisions to the model like "okay, I might use this or that," leaving it unsure.

No. We clearly define: "In this place, use the Web Browsing Tool (Bing), here use the Code Interpreter, here unzip a packed file in your Knowledge Base," etc. We precisely define each step.

# Final Words
Crafting a good system prompt is akin to writing a program, with variables, functions, and tricks like 'confirm,' which serve as a form of console printing or debugging.

Overall, this comprehensive approach is why I don't feel that GPT-4 is getting worse. By tightening the screws and maintaining significant control over what the model does for me, the above methods are ways to tighten these screws and maintain control. That's all, thanks, bye.

# My Example System Prompts

[screenshot example 1]

[screenshot example 2]

[screenshot example 3]