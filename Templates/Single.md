---
tags:
  - single
members: 
center: 
tracklist: 
banner: 
banner_x: 0.54313
cover: 
order: 
released:
---

# `$= dv.current().file.folder`
Start Over is the `$= dv.current().order`th single released by Sakurazaka46. 
Released on `$= dv.current().released`

-----
## Included members
```dataviewjs
let smth = `"${dv.current().file.folder}/Songs"`
let songs = dv.pages(smth)
songs = songs.sort(x => x.order)
let info = dv.page("info")
for (let i = 0; i< songs.length; i++) {
	dv.header(4, "**"+ songs[i].file.link + "**")
	let txt = "**" + songs[i].type + "** (" + songs[i].members.length + " members)"
	txt += " ([[" + songs[i].center + "]] center)"
	dv.paragraph(txt)
	txt = ""
	let members = dv.current().members
	members = members.map(x => dv.page(x))
	let gens = []
	for (let i = 1; i<=info.Generations; i++) {
		let smth = members.filter(x => x.generation == i)
		if (smth.length != 0) {
			gens.push(smth);
		}
	}
	for (let i = 0; i< gens.length; i++) {
		let text = ""
		if (gens[i][0].generation == 1) {
			text += "- **" + gens[i][0].generation + "st Generation** ("
		}
		if (gens[i][0].generation == 2) {
			text += "- **" + gens[i][0].generation + "nd Generation** ("
		}
		if (gens[i][0].generation == 3) {
			text += "- **" + gens[i][0].generation + "rd Generation** ("
		}
		text += gens[i].length + "): "
		for (let j = 0; j< gens[i].length; j++) {
			if (gens[i][j].name === songs[i].center.center) {
				text += gens[i][j].file.link + " (C), "
			}
			else {
				text += gens[i][j].file.link + ", "
			}
		}
		dv.paragraph(text.slice(0, -2))
	}
	dv.el("br", "")
}
```
## Participation Table
```dataviewjs
let smth = `"${dv.current().file.folder}/Songs"`
let songs = dv.pages(smth)
songs = songs.sort(x => x.order)
let info = dv.page("info")
for (let i = 0; i< songs.length; i++) {
	dv.header(4, "**"+ songs[i].file.link + "**")
	let txt = "**" + songs[i].type + "** (" + songs[i].members.length + " members)"
	txt += " ([[" + songs[i].center + "]] center)"
	dv.paragraph(txt)
	txt = ""
	let members = songs[i].members
	members = members.map(x => dv.page(x))
	let gens = []
	for (let j = 1; j<=info.Generations; j++) {
		let smth = members.filter(x => x.generation == j)
		if (smth.length != 0) {
			gens.push(smth);
		}
	}
	for (let j = 0; j< gens.length; j++) {
		let text = ""
		if (gens[j][0].generation == 1) {
			text += "- **" + gens[j][0].generation + "st Generation** ("
		}
		if (gens[j][0].generation == 2) {
			text += "- **" + gens[j][0].generation + "nd Generation** ("
		}
		if (gens[j][0].generation == 3) {
			text += "- **" + gens[j][0].generation + "rd Generation** ("
		}
		text += gens[j].length + "): "
		for (let k = 0; k < gens[j].length; k++) {
			if (gens[j][k].name == songs[i].center) {
				text += gens[j][k].file.link + " (C), "
			}
			else {
				text += gens[j][k].file.link + ", "
			}
		}
		dv.paragraph(text.slice(0, -2))
	}
	dv.el("br", "")
}
```

----
## Covers
