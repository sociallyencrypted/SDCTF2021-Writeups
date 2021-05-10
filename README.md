# SDCTF2021-Writeups
Hi! These are the official write-ups for the OSINT category by team Da Froggies for SDCTF 2021 organised by UC San Diego.

## hide-and-seek
### Category
OSINT
### Points
100
### Description
We don't know the flag, but we know some people who do! Here are their locations:
#### Location
`?v=hqXOIZtRYZU`
#### Location2
`qFHIm0c.jpeg`

### Solution
We looked at the two locations and immediately realised that the first location is one part of a [youtube URL](https://www.youtube.com/watch?v=hqXOIZtRYZU) while the second one is one part of some image sharing website (which we guessed out to be [Imgur](https://i.imgur.com/qFHIm0c.jpeg)) . With this information we were able to obtain the flags in two pieces (with the added fun of watching Aaron reveal his GPA in the youtube video).

### Flag
`sdctf{W0w_1_h4D_n0_ID3a!}`

## hide-and-seek-2
### Category
OSINT
### Points
200
### Description
I've gotten some more good intel. Apparently, the following information is the location of another flag!
#### First piece of info
`gg/4KcDWnUYMs`
#### Second piece of info
`810237829564727312-810359639975526490`

### Solution
The two pieces of info clearly pointed that the first is one part of a [discord server URL](https://www.discord.gg/4KcDWnUYMs) and Luciolle pointed out the second one includes message IDs. On joining the discord, we found a number of messages with different flags. Now, copying one of those IDs, we saw a URL like `discord.com/channels/810237829564727308/810237829564727312/810382741837185046`. We recognised that the `810237829564727312` part of the hint was indicative of the user posting the message, so we had to modify the last part of the URL. Changing that to `discord.com/channels/810237829564727308/810237829564727312/810382741837185046` we got the flag!

### Flag
`sdctf{m@st3R_h@Ck3R_4807}`

## speed-studying
### Category
OSINT
### Points
75
### Description
Help, I'm studying for a test, and I need you to find an example problem for me... I'm sure you can find it out there somewhere! I'm trying to remember this professor's name but I'm having trouble...who is the only professor at UC San Diego that is both an Assistant Professor for the Computer Science department, and an Associate Professor for the Mathematics department?
#### Note
The flag is not in the usual `sdctf{}` format. Submit that professor's First and Last name (but not the middle name, if any) separated by a single space. For example, if the professor has first name John and last name Appleseed, then...
#### Please Submit
John Appleseed

### Solution
With a quick google search about UC San Diego, we figured out that the domain for UCSD is `ucsd.edu`. Now, we did some Google Dorking (the exact query we used was `site:ucsd.edu Assistant Professor Computer Science Mathematics`) and after scrolling without results on a few pages, we finally found the [Faculty Profile](http://cseweb.ucsd.edu/~dakane/) of Daniel Kane, the professor we had been looking for.

### Flag
`Daniel Kane`

## speed-studying-2
### Category
OSINT
### Points
282
### Description
Nice, now that you've found Daniel Kane, I need an example from one of his classes. I don't remember anything about it other than its called "The Skyline Problem". Can you find it?

### Solution
Google Dorking was our friend again! This time, our search query was `site:ucsd.edu Skyline Problem` which led us to a specific PDF called [Homework3](https://cseweb.ucsd.edu/~dakane/CSE101%20Problem%20Archive/F18/Homework3.pdf) which had the flag in the footer :)

### Flag
`sdctf{N1ce_d0rKiNG_C@pt41N}`
