---
tags:
  - single
  - I_want_tomorrow
members:
  - Uemura Rina
  - Koike Minami
  - Saito Fuyuka
  - Inoue Rina
  - Endo Hikari
  - Ozono Rei
  - Onuma Akiho
  - Kousaka Marino
  - Takemoto Yui
  - Tamura Hono
  - Fujiyoshi Karin
  - Masumoto Kira
  - Matsuda Rina
  - Morita Hikaru
  - Moriya Rena
  - Yamasaki Ten
  - Ishimori Rika
  - Endo Riko
  - Kojima Nagisa
  - Taniguchi Airi
  - Nakashima Yuzuki
  - Matono Mio
  - Mukai Itoha
  - Murai Yu
  - Murayama Miu
  - Yamashita Shizuki
center:
  - Yamashita Shizuki
tracklist:
  - 19sai no Galette
  - Arashi no Mae Sekai no Owari
  - Boku wa Boku wo Suki ni Naranai
  - Honshitsuteki na Koto
  - I want tomorrow to come
  - Imasara Suddenly
  - Tokyo Snow
banner: "![[Artist_Tomorrow.png]]"
banner_x: 1
cover: Type_A_Tomorrow.png
banner_y: 0.1
released: 2024-10-23
order: "10"
name: I want tomorrow to come
---

# I want tomorrow to come
I want tomorrow to come is the `$= dv.current().order`th single released by Sakurazaka46. 
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
	if (songs[i].center != "unknown") {
		txt += " ([[" + songs[i].center + "]] center)"
	}
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
let members = dv.current().members
members = members.map(x => dv.page(x))
let smth = `"${dv.current().file.folder}/Songs"`
let songs = dv.pages(smth)
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

![[Type_A_Tomorrow.png||+grid]]![[Type_B_Tomorrow.png|+grid]]![[Type_C_Tomorrow.png|+grid]]
![[Type_D_Tomorrow.png|+grid]]![[Regular_Tomorrow.png|+grid]]