---
name: Koike Minami
birthday: 
height: 
birthplace: 
status: Graduated
joined: 2025-04-21
graduated: 
generation: "1"
japanese_name: 
tags:
  - "#members"
---

# `$= dv.current().file.name` `$= dv.current().japanese_name`
---
**Birthday:** 
	`$= dv.current().birthday` (`$= dv.date("today").year - dv.current().birthday.year` yrs)

**Height:** ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎**Birthplace:**               
`$= dv.current().height` cm ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎‎‎Osaka     

**Nicknames**:

//Introduction goes here//

----
##### **History**
```dataviewjs

dv.paragraph(dv.current().joined.toFormat('DDD') +" - Joined Sakurazaka46")
if (dv.current().status === "Graduated") {
	let txt = dv.current().graduated.toFormat('DDD') 
	let smth = `${txt} - Graduated from Sakurazaka46`
	dv.paragraph(smth)
}
```
----

##### **Meaning of Kanji in her name:**
`$= dv.current().japanese_name[0]`
`$= dv.current().japanese_name[1]`  
`$= dv.current().japanese_name[2]`  
`$= dv.current().japanese_name[3]`  

##### **Relationships with other members:**


----
## A-sides
```dataviewjs
let smth = dv.current().file.link + "haha"

let songs = dv.pages("#song")
let asides = songs.filter(x => x.a_side)
asides = asides.filter(x => x.members.includes(dv.current().file.name))
asides = asides.sort(x => x.released)

for (i = 0; i < asides.length; i++) {
	let text = asides[i].file.link;
	if (asides[i].center === dv.current().file.name) {
		text += " (Center)";
	}
	dv.paragraph(text);
}
if (asides.length === 0) {
	dv.paragraph(":(");
}

```
---
## B-sides
```dataviewjs
let songs = dv.pages("#song")
let bsides = songs.filter(x => !x.a_side);
bsides = bsides.filter(x => x.members.includes(dv.current().file.name));
bsides = bsides.sort(x => x.released)

for (i = 0; i < bsides.length; i++) {
	let text = bsides[i].file.link;
	if (bsides[i].center === dv.current().file.name) {
		text += " (Center)";
	}
	dv.paragraph(text);
}
```
