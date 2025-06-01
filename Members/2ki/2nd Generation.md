Sakurazaka46's 2nd generation currently has  `$= dv.pages("#members/2").filter(x => x.status !== "Graduated").length` members:
```dataviewjs
let members = dv.pages('"Members/2ki"')
let active = members.filter(x => x.status === "Active");
let graduated = members.filter(x => x.status === "Graduated");
let hiatus = members = members.filter(x => x.status === "Hiatus");
let printing = ""

if (active.length != 0) {
	dv.paragraph("**Active (" + active.length + ")**")
}
for (i = 0; i < active.length; i++) {
	printing += active[i].file.link + ", "
}
dv.paragraph(printing.slice(0, -2))
printing = ""

if (hiatus.length != 0) {
	dv.paragraph("**On hiatus (" + hiatus.length + ")**")
}
for (i = 0; i < hiatus.length; i++) {
	printing += hiatus[i].file.link + ", "
}
dv.paragraph(printing.slice(0, -2))
printing = ""

if (graduated.length != 0) {
	dv.paragraph("**Graduated (" + graduated.length + ")**")
}
for (i = 0; i < graduated.length; i++) {
	printing += graduated[i].file.link + ", "
}
dv.paragraph(printing.slice(0, -2))
```

## Joining Sakurazaka46

The members of 2nd generation were initially members of Keyakizaka46. When the group rebranded into Sakurazaka46 the members were all transferred over.

The auditions for 2nd generation were held in March 2018 as a part of the Sakamichi joint auditions. 9 members were announced as members of Keyakizaka46 in December of 2018, while 6 of them joined Sakamichi Keshuusei as trainees. In February of 2020 the final 6 members joined Keyakizaka46.

```dataviewjs
let members = dv.pages('"Members/2ki/Profiles"')
let later = members.filter(x => x.joined.year === 2020);
members = members.filter(x => x.joined.year === 2018);
let printing = ""

dv.paragraph("**December 2018 (" + members.length + ")**")
for (i = 0; i < members.length; i++) {
	printing += members[i].file.link + ", "
}
dv.paragraph(printing.slice(0, -2))
printing = ""

dv.paragraph("**February 2020 (" + later.length + ")**")
for (i = 0; i < later.length; i++) {
	printing += later[i].file.link + ", "
}
dv.paragraph(printing.slice(0, -2))

```
