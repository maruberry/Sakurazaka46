---
tags:
  - single
  - udagawa
members:
  - Morita Hikaru
  - Fujiyoshi Karin
  - Yamasaki Ten
  - Matono Mio
  - Taniguchi Airi
  - Moriya Rena
  - Tamura Hono
  - Yamashita Shizuki
  - Murayama Miu
  - Mukai Itoha
  - Ozono Rei
  - Matsuda Rina
  - Murai Yu
  - Ishimori Rika
  - Koike Minami
  - Inoue Rina
  - Endo Hikari
  - Onuma Akiho
  - Kousaka Marino
  - Takemoto Yui
  - Endo Riko
  - Odakura Reina
  - Kojima Nagisa
  - Nakashima Yuzuki
  - Masumoto Kira
center:
  - Morita Hikaru
tracklist:
  - UDAGAWA GENERATION
  - Nightmare Shoukogun
  - Nothing Special
  - Ikanaide
  - ULTRAVIOLET
  - Monshirouchou ga Tashika ton Deta
banner: "![[Udagawa_Generation.png]]"
banner_x: 0.54313
cover: Type_A_Udagawa.png
order: "11"
released: 2025-02-19
---

# UDAGAWA GENERATION

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
## Participation Table
```dataviewjs

let members = dv.current().members
members = members.map(x => dv.page(x))
let songs = dv.pages('"Releases/Udagawa Generation/Songs"')
songs = songs.sort(x => x.order)
let rows = []
for (i = 0; i < members.length; i++) {
	let row = [];
	let cnt = 0
	for (j = 0; j < songs.length; j++) {
		if (songs[j].members.includes(members[i].file.name)){
			cnt += 1
			row.push("x")
		}
		else {
			row.push(" ")
		}
	}
	let smth = [members[i].file.link + " (" + cnt + ")"]
	rows.push(smth.concat(row))
}

let cols = ["Members"]
for (j = 0; j < songs.length; j++) {
	cols.push(songs[j].file.name);
}

dv.table(cols,rows);
```

----
## Covers
![[Type_A_Udagawa.png||200+grid]]![[Type_B_Udagawa.png||200+grid]]![[Type_C_Udagawa.png|200+grid]]
![[Type_D_Udagawa.png||200+grid]]![[Regular_Udagawa.png||200+grid]]![[Digital_Udagawa.png||200+grid]]![[Special_Udagawa.png||200+grid]]

