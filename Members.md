Sakurazaka46 currently has `$= dv.pages("#members").filter(x => x.status !== "Graduated").length - 1` members. The group has in its history had `$= dv.pages("#members").length - 1` members

## By Generation

#### *1st generation* [[1st Generation|(link)]]
```dataviewjs
let members = dv.pages('"Members/1ki"')
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

#### *2nd generation* [[2nd Generation|(link)]]
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

#### *3rd generation* [[3rd Generation|(link)]]
```dataviewjs
let members = dv.pages('"Members/3ki"')
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

#### *4th generation* [[4th Generation|(link)]]
```dataviewjs
let members = dv.pages('"Members/4ki"')
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
----
## Current by Birth Year
```dataviewjs
let members = dv.pages('"Members"')
members = members.filter(x => x.status !== "Graduated")
members = members.filter(x => x.birthday)
members = members.sort(x => x.birthday.year)
let bd = members[0].birthday.year
let printing = ""
let count = 0;
for (i = 0; i < members.length; i++) {
	if (members[i].birthday.year != bd) {
		dv.paragraph("*" + bd + "* ("+count + ")")
		dv.paragraph(printing.slice(0, -2))
		bd = members[i].birthday.year
		printing = ""
		count = 0;
	}
	count += 1;
	printing += members[i].file.link + ", "
}
dv.paragraph("*" + bd + "* ("+count + ")")
dv.paragraph(printing.slice(0, -2))
```
-----
## All by Birth Year
```dataviewjs
let members = dv.pages('"Members"')
members = members.filter(x => x.birthday)
members = members.sort(x => x.birthday.year)
let bd = members[0].birthday.year
let printing = ""
let count = 0;
for (i = 0; i < members.length; i++) {
	if (members[i].birthday.year != bd) {
		dv.paragraph("*" + bd + "* ("+count + ")")
		dv.paragraph(printing.slice(0, -2))
		bd = members[i].birthday.year
		printing = ""
		count = 0;
	}
	count += 1;
	printing += members[i].file.link + ", "
}
dv.paragraph("*" + bd + "* ("+count + ")")
dv.paragraph(printing.slice(0, -2))
```

----
