---
name: Fujiyoshi Karin
birthday: 2001-08-29
height: "163"
birthplace: Osaka
status: Active
joined: 2018-12-04
graduated: 
generation: "2"
japanese_name: 藤吉夏鈴
tags:
  - members/2
---
![[Karin_Udagawa.png||300]]
# `$= dv.current().name` `$= dv.current().japanese_name`
---
**Birthday:** 
	`$= dv.current().birthday` (`$= dv.date("today").year - dv.current().birthday.year` yrs)

**Height:** ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎**Birthplace:**               
`$= dv.current().height` cm ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎‎‎Osaka     

**Nicknames**:
	Rin
	Karin
	Rorochan

Karin is one of the original 3 centers and is popular among female Buddies. Among all sakurazaka46 members she has been the most active in acting. She's got a nonchalant attitude and tends to have a poker face unless performing. She is best at emotional performances that tug on your heartstrings with her facial expressions. 

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
`$= dv.current().japanese_name[0]` (fuji) Wisteria
`$= dv.current().japanese_name[1]`  (yoshi) Good luck, joy
`$= dv.current().japanese_name[2]`  (ka) Summer, on'yomi pronounciation because Karin is not a japanese name
`$= dv.current().japanese_name[3]`  (rin) Small bell, on'yomi pronounciation because Karin is not a japanese name

When using auto translate her name will usually be translated as Fujiyoshi Natsurin

##### **Relationships with other members:**
[[Yamasaki Ten]] 
- Have done many photoshoots together
- w-center for [[Addiction]]

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

## Media Appearances outside of Sakurazaka46


## More pictures of her
