# Frontend Mentor Challenge - Huddle Landing Page Solution π­

Hello, δ½ ε₯½, μλνμΈμ, Hola, Hallo, Bonjour!  

Welcome to my **mobile-first**, **responsive**, solution the **[Huddle Landing Page Challenge](https://www.frontendmentor.io/challenges/huddle-landing-page-with-a-single-introductory-section-B_2Wvxgi0/hub)** from Frontend Mentor!

## Table of Contents π§΅
<hr>

- [Overview π](https://github.com/JoleneKearse/fem-huddle-landing-page#overview-)
  - [The Challenge π](https://github.com/JoleneKearse/fem-huddle-landing-page#the-challenge-)
  - [Screenshot πΈ](https://github.com/JoleneKearse/fem-huddle-landing-page#screenshot-)
  - [Links π](https://github.com/JoleneKearse/fem-huddle-landing-page#links-)

- [My Process π€](https://github.com/JoleneKearse/fem-huddle-landing-page#my-process-)
  - [Built with π ](https://github.com/JoleneKearse/fem-huddle-landing-page#built-with-)
  - [What I learned π](https://github.com/JoleneKearse/fem-huddle-landing-page#what-i-learned-)
  - [Continued development π](https://github.com/JoleneKearse/fem-huddle-landing-page#continued-development-)
  - [Useful resources π](https://github.com/JoleneKearse/fem-huddle-landing-page#useful-resources-)
- [Author π€ͺ](https://github.com/JoleneKearse/fem-huddle-landing-page#author-)
 - [My journey π](https://github.com/JoleneKearse/fem-huddle-landing-page#my-journey-)
 - [Let's connect π―](https://github.com/JoleneKearse/fem-huddle-landing-page#lets-connect-)

## Overview π
<hr>

### The Challenge π

Users should be able to:
- [x] View the optimal layout for the page depending on their device's screen size
- [x] See hover states for all interactive elements on the page

### Screenshot πΈ

Here's the provided design files:
![The Figma file's screenshots including desktop, active states & mobile](screenshots/figma-designs.png)

And, tada πͺ, my solution - also in desktop, active states and mobile views:
![My solution screenshots of desktop, active states, and mobile views](screenshots/screenshot.gif)

### Links π

- [Github](https://github.com/JoleneKearse/fem-huddle-landing-page#overview-) - I certainly hope you're checking out this awesome-sauce README that I spent a fun evening composing!
- [Live link](https://fem-huddle-landing-page-jade.vercel.app/) - And also hope you, spectacular π you, have the time to impart your so-appreciated code reviews to me.  

## My Process π€

I generally always start out **mobile-first**, but I had recently caught an article on whether mobile-first should be your choice.  So, I considered the use case of this particular website...
- I could see a product manager going into a company boardroom and doing an awesome lead-through of the product...
- ... but then thought, hmm... most users would come from emails or calls to action from elsewhere, so...
- The majority would probably still see it from their mobiles! 

So mobile-first won out! π

Next I decided, semi-with-crossed-fingers π€, that the 'cross the diamond' images in the back would be do-able with psuedo-elements and decided to leave that until the end.  _I'm hoping that doesn't come back to bite me in the butt!_ β‘

### Built with π 
- Semantic HTML5 markup - _I'd forgotten this on my last challenge, which I blame React for!_ π€£
- CSS custom properties
- Mobile-first workflow
- `position: absolute`
- Flexbox

### What I learned π

#### 1) Adding Hover & Focus Effects on SVGs

1) I do not know as much about applying `:hover` and `:focus` effects to **svg** images as I thought!

Full disclosure: I originally exported the assets from **Figma** as **PNG** files.  _This dates back to my teaching career, where I needed the transparency of the PNG image file format - ingrained habits break hard_. But then I hated the _blurriness_ of the images and switched back to **SVG**.

I was π― sure that you could modify SVG file colours (_Yes, I'm Canadian, and use Canadian spellings_) with CSS.  But **I don't have as much experience exporting assets from Figma**, so may be completely missing something here.  

No matter what I did, I wasn't able to change the colour on a state change!

I applied a class of `.icon` to each, but 
```CSS
.icon:hover,
.icon:focus {
  color: var(--clr-accent-300);
}
```
didn't work!

Huh?

So, I will admit I went to [ChatGPT](https://chat.openai.com/chat) for help... and probably a bit too early.  I blindly followed it's solution of
```CSS
.icon path[stroke="white"]:hover {
  stroke: var(--clr-accent-300);
}
```
and the multitude of other complicated selectors I had to add on after hunting down the `white` in the `.svg` files.  Like, it was so much work and didn't even work!

Next I asked our friendly neighbourhood AI if I could do it with JavaScript.  Again I blindly followed along...  After some clarifying questions, I identified it wouldn't have worked anyway.

So...

I went back to a good old-fashioned Google search and was reminded of the `filter` property.  I read a few articles, then, duh π€¦, remembered that there are so, so, so many intelligent software engineers already out there!

Well, one of them must have created a [handly-dandy generator](https://codepen.io/sosuke/pen/Pjoqqp).  Lo and behold, someone had!  

#### 2) A Reminder of Fixed Position

The background image did come back to bite me!  Like a fool,  I stubbornly persisited in media query after media query to keep my `header` in the proper position.  I had to prove it could be done!  Then I came back to reality...

That made no sense whatsoever!

I found I could readjust my margins by controlling the container itself:
```CSS
.container {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    width: clamp(296px, 80vw, var(--width-max));
    margin-inline: auto;
}
``` 

---

### Continued development π

Although I've been itching to get back to building my own projects, this one showed me I've been neglecting my love for CSS!  

### Useful resources π

[Is Mobile First Always The Best Approach?](https://cleancommit.io/blog/is-mobile-first-always-the-best-approach/)

[ChatGPT](https://chat.openai.com/chat)

[CSS filter generator to convert from black to target hex color](https://codepen.io/sosuke/pen/Pjoqqp)

[Font-size Clamp Generator](https://clamp.font-size.app/)

[Viewport Resizer Chrome Extension](https://chrome.google.com/webstore/detail/viewport-resizer-%E2%80%93-respon/kapnjjcfcncngkadhpmijlkblpibdcgm/related?hl=en)


## Author π€ͺ
<hr>

Hiya! π My name is **Jolene Kearse**, (no pronouns, as Jolene, or pretty much whatever you want to call me - within limits π€£ - is fine with me).  

I may be a _tad_ older than you at 41 π, simply because I was an **English as a Foreign Language Teacher** οΈππ§βπ« for over 15 years - so, yeah, _for a little bit_ π€...  I lived all over the world, including China, England & South Korea.

But that was then! 

...

Now I'm an awesome **Software Engineer**! :dancer:  I'm a **proud, self-taught individual**. 

### My journey π

I'm also proud of how far I came in 2022.  I finally learned **JavaScript**! π» _I had struggled for about a year before I finally could add that to my skillset.  If you're interested in an awesome π₯ course check out **[Class Central's Bootcamp YouTube Playlist going through freeCodeCamp's Algorithms and Data Structures Certification](https://www.youtube.com/playlist?list=PLU3RKvMpgrSEoqVIV14K_zuinrIBcnCgT).**

Then I met an awesome group of fellow-learning devs, **The Explorers**.  This exposed me to the myriad and oft-confusing ways of using **Git** in a team - loving it now!  But also projects using so many kinds of tech that would've just blown my mind a year before π€― including:
- React
- TypeScript
- Tailwind

I even participated in **[#Hacktoberfest](https://hacktoberfest.com/)** and earned the coveted T-shirt! ππ

But who cares about 2022? This is 2023!

...

I've been boning up on **React**, and just taking so many courses to learn **Backend Development** and **navigate the process of earning my first tech job**!

One of those courses has seen me going back to **Python** - which I had treated as my _crutch language_ to understand JavaScript.  π€£  But I've been loving navigating in multiple languages.

Another challenge I am undertaking this year is [Exercism's](https://exercism.org/) **#12in23**.  This is a cool π opportunity to _try out_ 12 different languages this year.  Each month has a theme, like **Functional February** and **Mechanical March** to encourage you to check out different language paradims.  I'm loving this chance to dip my toe in other types of programming.  I find I'm gaining the ability to evaluate various languages' strengths and project needs.

### Let's connect π―

I'd love β€οΈ to connect with y'all (_sorry, I love using that ironicallly and do so with great frequency_ π):
- [LinkedIn](https://www.linkedin.com/in/jolene-kearse-2562ba218/)
- [Github](https://github.com/JoleneKearse)
- [Twitter](https://twitter.com/FromJolene)


