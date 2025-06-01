---
name: Odakura Reina
birthday: 2004-07-25
height: "163"
birthplace: Tokyo
status: Active
joined: 2023-01-09
graduated: 
generation: "3"
japanese_name: 小田倉麗奈
tags:
  - members/3
---
![[Reina_Udagawa.png||300]]
# `$= dv.current().file.name` `$= dv.current().japanese_name`
---
**Birthday:** 
	`$= dv.current().birthday` (`$= dv.date("today").year - dv.current().birthday.year` yrs)

**Height:** ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎**Birthplace:**               
`$= dv.current().height` cm ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎‎‎Osaka     

**Nicknames**:
Reina

//Introduction goes here//

##### **Meaning of Kanji in her name:**
`$= dv.current().japanese_name[0]`
`$= dv.current().japanese_name[1]`  
`$= dv.current().japanese_name[2]`  
`$= dv.current().japanese_name[3]`  
`$= dv.current().japanese_name[4]`

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
