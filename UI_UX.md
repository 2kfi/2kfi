# THE GOLDEN RATIO
## For Gaps

the golden gap ratio is 1.618
Start from 8 then times 1.618
go 13,21,34 and so on

## For Pages and layout
the main idea 38.2% on side for ACTIONS
61.8% for context and content

This is **over-applied**.

- Works well for **marketing pages**
- Not great for:
    - dashboards
    - dense tools
    - data-heavy UIs

> Use ratio _when it improves clarity_, not by default.

## Type Scale

- body at 16px
- Sub-headers at 28 px
- Headers at 42px
- The Display or Hero at 68px

## Notifications
- for mobile it goes : top
- for Desktop it goes bottom right
- timing
	 - 4 sec for info
	 - 7 sec for warnnings
	 - errors stay untill Acknowledged
- stacking notifactions
	 - maxium 3
	 - pushs the old notifcaitons up 
	 - damping 20
	 - stiffness : 180
- always dismissible
	- a buttom for example
	- swipe for mobile
	- and hover to pause
- color coded
	- each one needs a special color (e.g red for warrnings)
## LOADING AND PATERNS
- LOADING IS A SYSTEM!
	you can have a single right choice per conetxt
- Types of loadings
	- Skeleton: 
		When you know the shape (e.g contant like cards, lists and Articals)
		and wait time is over 300ms
		Ensure the skeleton is the _exact_ size of the content to prevent the page from jumping when it loads.
	- Spinner:
		for waits under 3 sec, when you don't know the duration and just want to say "something is happening right now in the backend"
		NEVER for fullpages load
	- progress bar:
		when you know the percentage (e.g file uploads, installs)
		anything over three secends
		IT builds trust
	- Optimistic UI
		A pro move
		Used for Like, Saves, Bookmarks, Mutaions That Succeed 99% of the time
		You show the resault instantly and roll back only if it fails
	- Show NOTHING (no load screen)
		for anything less than 300ms
		a Flash of a load screen is worst than a bit of delay
		Human Brain reads it as a bug
  
## Grids
- grids are a ratio systems
- REMMEMBER THO! breakpoints doesn't go by pages but but elements
- number 12 is loved by swiss typography and scaled by modern freamworks too
- default value is 12, because it's the smallest number that can be divided on 2,3,4 and 6
	 - use 12 columns on desktop
	 - use 8 columns on tablet
	 - use 4 columns on mobile
	 - it's parsed not guessed 
	- 4:8 gives conatnt, so it's a narrow sidebar, and a wide content area
	- 6:6 makes everything equal
	- 3:9 makes a minimal sidebar and a dominant content
- but when the screen shrinks, the Grid Reconfigures, for examble
	- 1280px wide screen takes 12 coloums for a grid
	- 768px wide screen takes 6 coloums
	- 480px wide screens takes 4 colums
	- 320px wide screens take a single colum
	- EVERY break point is a grid descition
- spacing
	- 8px feels tight and tecnical
	- 24 px feels balanced and clean
	- 40px feels editorial and premium



## **Contrast & Accessibility.**
- Never rely on color alone to convey meaning (e.g., if a field is "Red" for error, it also needs an "Icon" or "Text" for colorblind users).



## Dropdown

- Make it clickable.
	- a correct arrow
	- a hover state
	- a minimum 44 pixel click target
	- users should never wander if it's clickable or not
- flip on edge
	 - when the drop-down hits  the viewport bottom, it should open upward
	 - NEVER CLIP THE LAST ITEM of the screen because of a ciewport
- Keyboard always.
	 - Keyboard navigation is not optional
	 - arrow keys to move
	 - enter to select
	 - escabe to close the menu
	 - ever user deserves access
- 10+ items = search
	 - anything past 10 items, means add search
	 - filtering keep scrolling every single time
	 - above 100 items then virtualize the list
- hit 150 ms
	 - animate in under 150ms
	 - this time is fast enought to feel instent and slow enough to feel  smooth.
	 - anything longer feels janky

## tooltips
- don't make annoying tooltips
- rule 1 : wait 300ms before you show the tooltip
- rule 2 : point with an arrow, don't just make a box with info, use a tail to guide the eye to the tool or icon 
- rule 3 : flip near view port edges, a cutten toltip is work than a no tooltip at all
- rule 4: dismiss everywhere, mouse leave, escape key, focus out or tap out the shape
- rule 5 : maximum 300px wide, one scentence maximum, a tool tip is a hint not a part of docs
- Rule 6: Never put info required for a task inside a tooltip (since mobile users can't always "hover").
## filing feilds
1)  At rest
	 - lable outside, helper below (never inside)
2) at focus
	 - ring contrast at least 3:1 (fevrable to be 4.5:1)
	 - avoid colors like soft blue because it fails accsisablity
3) Valudation failed
	 - color + icon + message 
	 - an only red bordar (ring) is not notciable by 12% of users (color blind)
4)  it worked!
	 - confirm inside field + icon (optinal)
	 - avoid toasts because they disaper too soon
5) locked (AKA Disablied)
	 - locked mouse cursior
	 - gray grayscale background
	 - avoid opasity 0.5 because it looks like loading
6) Async in flight 
	 - disable input, show progress,  prevent double submit
	 - spinner inside the feild
	 - avoid not having a loading state = it shows as an error and pushs double submit
- 6 states, one forgoten = one bug
- To be clear: 1. Default, 2. Hover, 3. Focus, 4. Disabled, 5. Error, 6. Success.

## For this use CSS, not JS
- Smooth scroll  
- Dark mode  
- Text truncation  
- Sticky headers  
- Scroll snap  
- System accent colors








# 📱 MOBILE AGENT RULES: THE GOLDEN SYSTEM

## 1. THE GOLDEN GAPS (SPACING)
*Formula: Base 8 * 1.618 (Fibonacci Sequence)*
- **Small:** 13px (Tight groupings)
- **Medium:** 21px (Standard component spacing)
- **Large:** 34px (Section breathing room)
- **Note:** Avoid >34px on mobile to preserve screen real estate.

## 2. LAYOUT: THE VERTICAL RATIO
*Applying the 38.2% / 61.8% split to height*
- **Content Zone (Top 61.8%):** Context, images, and primary reading data.
- **Action Zone (Bottom 38.2%):** The "Thumb Zone." Place all critical buttons, inputs, and navigation here.

## 3. MOBILE TYPE SCALE
- **Hero / Display:** 42px (Scaled down from desktop to prevent clipping)
- **Headers:** 28px
- **Sub-headers:** 20px
- **Body Text:** 16px (Minimum for accessibility)

## 4. NOTIFICATION LOGIC (MOBILE)
- **Position:** Top (System standard)
- **Stacking:** Maximum 3; newest pushes oldest **UP**.
- **Interaction:** Always dismissible; Swipe to dismiss.
- **Physics:** Stiffness: 180 | Damping: 20.
- **Timing:**
  - **Info:** 4s
  - **Warning:** 7s
  - **Error:** Persistent (User must acknowledge)

## 5. LOADING SYSTEM (PERCEIVED PERFORMANCE)
- **< 300ms:** Show Nothing (Prevents visual "flicker").
- **> 300ms:** Skeleton Screens (For known content structures like cards/lists).
- **< 3s:** Spinner (Generic "backend is working" signal).
- **> 3s:** Progress Bar (Builds trust for long tasks/uploads).
- **Optimistic UI:** Update UI immediately for "Likes," "Saves," and "Bookmarks." Revert only on 1% failure cases.
