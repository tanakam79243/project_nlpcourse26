---
title: "Natural Language Processing Course"
author: "Tanaka Manhede"
date: "January 2026"
output:
  html_document:
    toc: true
    toc_float: true
    toc_depth: 3
    css: !expr here::here("/Users/tanakamanhede/Library/CloudStorage/OneDrive-TempleUniversity/Manhede_RData/styles_templates/jr_19.css")
---



##                              RENOVATION UNDERWAY

More content to come...

## Note of the Day:

The joke is embedded in the name of the data frame; enjoy! 

## Coder's Note

Welcome to my hub! Here, I will be periodically documenting my coding journey. Some code you will see will make you squint your eyes in confusion. Don't fret! Look the other way and recognize that the code works, equivalent to that of duct tape. Over time, I will upgrade from duct tape to b7000. The metaphor may not make sense but all this just to say enjoy the process of my code writing! Throughout the journey, there will be fun tidbits sprinkled throughout the page to distract from the code, don't get side tracked!  

## Homework One

For my first homework I am going to produce is a string called "Mary had a little lamb" in one code block. Then I'm going to split the string to one word per row. Then I'm going to add a variable called Nletters that counts the letters in each word. The other part of your homework is to style your css to your personal needs.

 

So, step one is to produce the string "Mary had a Little Lamb"


``` r
my_string <- "Mary had a little lamb"

print(my_string)
```

```
## [1] "Mary had a little lamb"
```

That seemed easy...


Now, we are going to take the string "Mary had a little lamb" and put it into a data frame that counts the number of letters/characters in each word. The challenge is being able to create a table that I can simply change the string and it will automatically update; so a bit of elbow grease was used, but nevertheless here is the code:


``` r
# This splits the sentence by word, given that there is a space inserted
# between each word
words = str_split(my_string, " ")

# This is a data frame that serves to list out the words in the sentence and
# the number of letters or characters in each word. It has been formated this
# way so that a different sentence can be inserted and formatted as a data
# frame
df.lambchops <- data.frame(x = words, y = NA)

# I am renaming the column with more appropriate names. (haha lamb chops)
colnames(df.lambchops)[1] <- "Words"
colnames(df.lambchops)[2] <- "N_letters"

# For the N_letters column, here we are counting the number of characters or
# letters in each word that has its own row
df.lambchops$N_letters <- nchar(df.lambchops$Words)

print(df.lambchops)
```

```
##    Words N_letters
## 1   Mary         4
## 2    had         3
## 3      a         1
## 4 little         6
## 5   lamb         4
```

All in a good day's work! 


## Homework Two

"Patiently waiting for the next assignment"

-TK

