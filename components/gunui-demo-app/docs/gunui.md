GunUi
===
> A collection of widgets to visualize your Gun data. 

So you've played with Gun ? You've build your 'todo-app' with javascript, the Gun-API, HTML and CSS? <br>
And now you're ready to start that really big application with a lot of data and complexity...

You're going to create a lot of `gun.get().on(callback)` stuff in there, and in all those callbacks you will have to keep that browser in sync... updating lists, changing content... across pages...<br>
I guess we're back in 'callback hell'.

<i>Well maybe not</i><br>
GunUi is a collection of Polymer webcomponents created especially for Gun. It tries to prevent that 'callback hell', because every element handles its own peace of data.

> The 'todo-app' is actually a tutorial in this documentation 😉.<br>
> Take a look at [Todo]()

Gun awareness
===
Every element is - what i like to call - 'Gun aware'...meaning that every element will be 'linked' to a certain data-point in your graph-data by just setting two attributes; 'soul' and 'prop'.

It will look like 
```
	<gun-ui-ledbutton soul="livingroom" prop="lights"></gun-ui-ledbutton>
```

`<gun-ui-ledbutton>` translates this as `gun.get("livingroom").get("lights")`.

To let the element be truly 'Gun-aware' it needs to change it's 'state' when his data-point changes...for this we add another attribute; "subscribe".

So now it looks like 
```
	<gun-ui-ledbutton soul="livingroom" prop="lights" subscribe></gun-ui-ledbutton>
```

When the data-point `gun.get("livingroom").get("lights")` changes...so does the  `<gun-ui-ledbutton>`.

> There is a reason that i don't let the elements 'subscribe' by default...because whe have an alternative.<br>
> more on that in [Subscribe...or not]()

These docs
===
This page is the main documentation for all GunUi related stuff. It provides you with element specific documentation and demo's and to a few tutorials.

I hope you will enjoy Gun and Polymer 😀
