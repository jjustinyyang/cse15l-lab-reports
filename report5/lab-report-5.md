Intro
---

This lab report is an extension to lab report 3, which I researched on the `grep` command line options. 

In this lab report, I am researching on the `find` command line options. I chose this this lab report topic because it is interesting to see how useful the terminal commands are and learning this would help me access my files easier and faster.

Examples of them would be provided using the files and directories from `skill-demo1-data/written_2` provided in class.

size option
---

This command line option find files that is less than or greater than a specific file size.

- example 1: 

`Justins-MacBook-Air:written_2 justinyang$ find . -size -2k`

```
.
./non-fiction
./non-fiction/OUP
./non-fiction/OUP/Berk
./non-fiction/OUP/Abernathy
./non-fiction/OUP/Rybczynski
./non-fiction/OUP/Kauffman
./non-fiction/OUP/Fletcher
./non-fiction/OUP/Castro
./travel_guides
./travel_guides/berlitz1/HandRLasVegas.txt
./travel_guides/berlitz1/HandRIstanbul.txt
./travel_guides/berlitz1/HandRHongKong.txt
./travel_guides/berlitz1/HandRLisbon.txt
./travel_guides/berlitz1/HandRMallorca.txt
./travel_guides/berlitz1/HandRLosAngeles.txt
./travel_guides/berlitz1/HandRMadeira.txt
./travel_guides/berlitz1/HandRIbiza.txt
./travel_guides/berlitz1/HandRLakeDistrict.txt
./travel_guides/berlitz1/HandRJerusalem.txt
```

- example 2: 

`Justins-MacBook-Air:written_2 justinyang$ find -size +120k`

```
./travel_guides/berlitz1/WhereToIndia.txt
./travel_guides/berlitz1/WhereToItaly.txt
./travel_guides/berlitz1/WhereToMalaysia.txt
./travel_guides/berlitz1/WhereToJapan.txt
./travel_guides/berlitz1/WhereToFrance.txt
./travel_guides/berlitz2/Canada-WhereToGo.txt
./travel_guides/berlitz2/China-WhereToGo.txt
```

type option
---

This command line option find files that is a specific type.

- example 1: 

`Justins-MacBook-Air:written_2 justinyang$ find -type d`

```
.
./non-fiction
./non-fiction/OUP
./non-fiction/OUP/Berk
./non-fiction/OUP/Abernathy
./non-fiction/OUP/Rybczynski
./non-fiction/OUP/Kauffman
./non-fiction/OUP/Fletcher
./non-fiction/OUP/Castro
./travel_guides
./travel_guides/berlitz1
./travel_guides/berlitz2
```

- example 2: 

`Justins-MacBook-Air:Castro justinyang$ find . -type f`

```
./chR.txt
./chP.txt
./chQ.txt
./chB.txt
./chC.txt
./chA.txt
./chV.txt
./chW.txt
./chM.txt
./chZ.txt
./chL.txt
./chN.txt
./chY.txt
./chO.txt
```

time option
---

This command line option find files that is modified within specific time in days, if use `-mtime`; minutes if use `-mmin`.

While `m` stands for `modified`, we can use `a` for `accessed` or `c` for `created`.

- example 1: `find -mtime -1`

```
.
./non-fiction
./non-fiction/OUP
./non-fiction/OUP/Berk
./non-fiction/OUP/Berk/ch2.txt
./non-fiction/OUP/Berk/ch1.txt
./non-fiction/OUP/Berk/CH4.txt
./non-fiction/OUP/Berk/ch7.txt
./non-fiction/OUP/Abernathy
./non-fiction/OUP/Abernathy/ch2.txt
./non-fiction/OUP/Abernathy/ch3.txt
./non-fiction/OUP/Abernathy/ch1.txt
./non-fiction/OUP/Abernathy/ch7.txt
./non-fiction/OUP/Abernathy/ch6.txt
./non-fiction/OUP/Abernathy/ch8.txt
./non-fiction/OUP/Abernathy/ch9.txt
./non-fiction/OUP/Abernathy/ch15.txt
./non-fiction/OUP/Abernathy/ch14.txt
./non-fiction/OUP/Rybczynski
./non-fiction/OUP/Rybczynski/ch2.txt
./non-fiction/OUP/Rybczynski/ch3.txt
./non-fiction/OUP/Rybczynski/ch1.txt
./non-fiction/OUP/Kauffman
./non-fiction/OUP/Kauffman/ch3.txt
./non-fiction/OUP/Kauffman/ch1.txt
./non-fiction/OUP/Kauffman/ch4.txt
./non-fiction/OUP/Kauffman/ch5.txt
./non-fiction/OUP/Kauffman/ch7.txt
./non-fiction/OUP/Kauffman/ch6.txt
./non-fiction/OUP/Kauffman/ch8.txt
./non-fiction/OUP/Kauffman/ch9.txt
./non-fiction/OUP/Kauffman/ch10.txt
./non-fiction/OUP/Fletcher
./non-fiction/OUP/Fletcher/ch2.txt
./non-fiction/OUP/Fletcher/ch1.txt
./non-fiction/OUP/Fletcher/ch5.txt
./non-fiction/OUP/Fletcher/ch6.txt
./non-fiction/OUP/Fletcher/ch9.txt
./non-fiction/OUP/Fletcher/ch10.txt
./non-fiction/OUP/Castro
./non-fiction/OUP/Castro/chR.txt
./non-fiction/OUP/Castro/chP.txt
./non-fiction/OUP/Castro/chQ.txt
./non-fiction/OUP/Castro/chB.txt
./non-fiction/OUP/Castro/chC.txt
./non-fiction/OUP/Castro/chA.txt
./non-fiction/OUP/Castro/chV.txt
./non-fiction/OUP/Castro/chW.txt
./non-fiction/OUP/Castro/chM.txt
./non-fiction/OUP/Castro/chZ.txt
./non-fiction/OUP/Castro/chL.txt
./non-fiction/OUP/Castro/chN.txt
./non-fiction/OUP/Castro/chY.txt
./non-fiction/OUP/Castro/chO.txt
./travel_guides
./travel_guides/berlitz1
./travel_guides/berlitz1/HandRLasVegas.txt
./travel_guides/berlitz1/HistoryJapan.txt
./travel_guides/berlitz1/IntroMalaysia.txt
./travel_guides/berlitz1/HandRIstanbul.txt
./travel_guides/berlitz1/HistoryJamaica.txt
./travel_guides/berlitz1/HandRJamaica.txt
./travel_guides/berlitz1/HandRHongKong.txt
./travel_guides/berlitz1/HistoryEgypt.txt
./travel_guides/berlitz1/IntroEdinburgh.txt
./travel_guides/berlitz1/HistoryIsrael.txt
./travel_guides/berlitz1/IntroDublin.txt
./travel_guides/berlitz1/HistoryIndia.txt
./travel_guides/berlitz1/IntroFrance.txt
./travel_guides/berlitz1/IntroMadeira.txt
./travel_guides/berlitz1/WhatToLakeDistrict.txt
./travel_guides/berlitz1/IntroIbiza.txt
./travel_guides/berlitz1/HistoryItaly.txt
./travel_guides/berlitz1/WhereToGreek.txt
./travel_guides/berlitz1/WhereToLakeDistrict.txt
./travel_guides/berlitz1/HistoryDublin.txt
./travel_guides/berlitz1/IntroIsrael.txt
./travel_guides/berlitz1/WhatToIbiza.txt
./travel_guides/berlitz1/HistoryFrance.txt
./travel_guides/berlitz1/WhatToHawaii.txt
./travel_guides/berlitz1/HistoryMallorca.txt
./travel_guides/berlitz1/HistoryJerusalem.txt
./travel_guides/berlitz1/HandRLisbon.txt
./travel_guides/berlitz1/WhereToIndia.txt
./travel_guides/berlitz1/HistoryMadrid.txt
./travel_guides/berlitz1/HistoryHongKong.txt
./travel_guides/berlitz1/IntroMadrid.txt
./travel_guides/berlitz1/IntroLosAngeles.txt
./travel_guides/berlitz1/HistoryIstanbul.txt
./travel_guides/berlitz1/WhereToItaly.txt
./travel_guides/berlitz1/HistoryLasVegas.txt
./travel_guides/berlitz1/HistoryGreek.txt
./travel_guides/berlitz1/HandRMallorca.txt
./travel_guides/berlitz1/JungleMalaysia.txt
./travel_guides/berlitz1/WhatToMadeira.txt
./travel_guides/berlitz1/WhatToFWI.txt
./travel_guides/berlitz1/WhereToMalaysia.txt
./travel_guides/berlitz1/WhatToMalaysia.txt
./travel_guides/berlitz1/WhatToDublin.txt
./travel_guides/berlitz1/WhereToJapan.txt
./travel_guides/berlitz1/HistoryHawaii.txt
./travel_guides/berlitz1/WhatToFrance.txt
./travel_guides/berlitz1/WhereToEgypt.txt
./travel_guides/berlitz1/WhereToEdinburgh.txt
./travel_guides/berlitz1/WhatToIsrael.txt
./travel_guides/berlitz1/HandRLosAngeles.txt
./travel_guides/berlitz1/HistoryMadeira.txt
./travel_guides/berlitz1/IntroJerusalem.txt
./travel_guides/berlitz1/HandRMadeira.txt
./travel_guides/berlitz1/WhereToIsrael.txt
./travel_guides/berlitz1/HandRIbiza.txt
./travel_guides/berlitz1/WhereToFrance.txt
./travel_guides/berlitz1/WhereToDublin.txt
./travel_guides/berlitz1/IntroLasVegas.txt
./travel_guides/berlitz1/IntroIstanbul.txt
./travel_guides/berlitz1/WhereToMallorca.txt
./travel_guides/berlitz1/WhatToMallorca.txt
./travel_guides/berlitz1/IntroHongKong.txt
./travel_guides/berlitz1/IntroFWI.txt
./travel_guides/berlitz1/IntroJamaica.txt
./travel_guides/berlitz1/IntroGreek.txt
./travel_guides/berlitz1/HandRIsrael.txt
./travel_guides/berlitz1/WhatToEdinburgh.txt
./travel_guides/berlitz1/WhereToMadeira.txt
./travel_guides/berlitz1/WhatToGreek.txt
./travel_guides/berlitz1/HandRLakeDistrict.txt
./travel_guides/berlitz1/WhereToIbiza.txt
./travel_guides/berlitz1/WhereToHawaii.txt
./travel_guides/berlitz1/HandRMadrid.txt
./travel_guides/berlitz1/HistoryMalaysia.txt
./travel_guides/berlitz1/IntroItaly.txt
./travel_guides/berlitz1/WhatToIndia.txt
./travel_guides/berlitz1/WhereToLosAngeles.txt
./travel_guides/berlitz1/HandRJerusalem.txt
./travel_guides/berlitz1/HistoryIbiza.txt
./travel_guides/berlitz1/HistoryEdinburgh.txt
./travel_guides/berlitz1/HistoryFWI.txt
./travel_guides/berlitz1/IntroIndia.txt
./travel_guides/berlitz1/WhatToItaly.txt
./travel_guides/berlitz1/HistoryLakeDistrict.txt
./travel_guides/berlitz1/WhereToMadrid.txt
./travel_guides/berlitz1/WhereToJerusalem.txt
./travel_guides/berlitz1/IntroEgypt.txt
./travel_guides/berlitz1/HandRHawaii.txt
./travel_guides/berlitz1/WhatToJapan.txt
./travel_guides/berlitz1/WhatToJamaica.txt
./travel_guides/berlitz1/IntroLakeDistrict.txt
./travel_guides/berlitz1/IntroMallorca.txt
./travel_guides/berlitz1/WhatToHongKong.txt
./travel_guides/berlitz1/WhatToEgypt.txt
./travel_guides/berlitz1/WhereToHongKong.txt
./travel_guides/berlitz1/WhereToFWI.txt
./travel_guides/berlitz1/WhatToIstanbul.txt
./travel_guides/berlitz1/WhereToIstanbul.txt
./travel_guides/berlitz1/IntroJapan.txt
./travel_guides/berlitz1/WhatToLasVegas.txt
./travel_guides/berlitz1/WhatToLosAngeles.txt
./travel_guides/berlitz2
./travel_guides/berlitz2/Portugal-History.txt
./travel_guides/berlitz2/Berlin-WhereToGo.txt
./travel_guides/berlitz2/Costa-History.txt
./travel_guides/berlitz2/Amsterdam-WhereToGo.txt
./travel_guides/berlitz2/Costa-WhereToGo.txt
./travel_guides/berlitz2/Amsterdam-WhatToDo.txt
./travel_guides/berlitz2/CostaBlanca-WhatToDo.txt
./travel_guides/berlitz2/Barcelona-History.txt
./travel_guides/berlitz2/Portugal-WhereToGo.txt
./travel_guides/berlitz2/Boston-WhereToGo.txt
./travel_guides/berlitz2/Poland-WhatToDo.txt
./travel_guides/berlitz2/California-WhereToGo.txt
./travel_guides/berlitz2/Cuba-WhatToDo.txt
./travel_guides/berlitz2/Berlin-History.txt
./travel_guides/berlitz2/Bahamas-WhereToGo.txt
./travel_guides/berlitz2/Cancun-WhatToDo.txt
./travel_guides/berlitz2/Bali-History.txt
./travel_guides/berlitz2/Crete-WhereToGo.txt
./travel_guides/berlitz2/Athens-History.txt
./travel_guides/berlitz2/Berlin-WhatToDo.txt
./travel_guides/berlitz2/Canada-WhereToGo.txt
./travel_guides/berlitz2/Bali-WhereToGo.txt
./travel_guides/berlitz2/Budapest-WhereoGo.txt
./travel_guides/berlitz2/Barcelona-WhereToGo.txt
./travel_guides/berlitz2/Athens-WhereToGo.txt
./travel_guides/berlitz2/Paris-WhereToGo.txt
./travel_guides/berlitz2/China-WhereToGo.txt
./travel_guides/berlitz2/Bermuda-WhatToDo.txt
./travel_guides/berlitz2/California-History.txt
./travel_guides/berlitz2/Vallarta-History.txt
./travel_guides/berlitz2/Budapest-WhatToDo.txt
./travel_guides/berlitz2/Cancun-History.txt
./travel_guides/berlitz2/PuertoRico-WhatToDo.txt
./travel_guides/berlitz2/Vallarta-WhatToDo.txt
./travel_guides/berlitz2/Bali-WhatToDo.txt
./travel_guides/berlitz2/CostaBlanca-History.txt
./travel_guides/berlitz2/CstaBlanca-WhereToGo.txt
./travel_guides/berlitz2/NewOrleans-History.txt
./travel_guides/berlitz2/PuertoRico-History.txt
./travel_guides/berlitz2/Algarve-Intro.txt
./travel_guides/berlitz2/Nepal-History.txt
./travel_guides/berlitz2/China-History.txt
./travel_guides/berlitz2/Canada-History.txt
./travel_guides/berlitz2/Crete-History.txt
./travel_guides/berlitz2/Portugal-WhatToDo.txt
./travel_guides/berlitz2/Bahamas-Intro.txt
./travel_guides/berlitz2/Amsterdam-History.txt
./travel_guides/berlitz2/Bahamas-WhatToDo.txt
./travel_guides/berlitz2/Barcelona-WhatToDo.txt
./travel_guides/berlitz2/Algarve-WhatToDo.txt
./travel_guides/berlitz2/PuertoRico-WhereToGo.txt
./travel_guides/berlitz2/Cuba-WhereToGo.txt
./travel_guides/berlitz2/Costa-WhatToDo.txt
./travel_guides/berlitz2/Beijing-History.txt
./travel_guides/berlitz2/Nepal-WhereToGo.txt
./travel_guides/berlitz2/CanaryIslands-WhereToGo.txt
./travel_guides/berlitz2/Bermuda-history.txt
./travel_guides/berlitz2/CanaryIslands-History.txt
./travel_guides/berlitz2/Amsterdam-Intro.txt
./travel_guides/berlitz2/Crete-WhatToDo.txt
./travel_guides/berlitz2/Algarve-WhereToGo.txt
./travel_guides/berlitz2/Athens-Intro.txt
./travel_guides/berlitz2/Algarve-History.txt
./travel_guides/berlitz2/Poland-History.txt
./travel_guides/berlitz2/Beijing-WhereToGo.txt
./travel_guides/berlitz2/CanaryIslands-WhatToDo.txt
./travel_guides/berlitz2/California-WhatToDo.txt
./travel_guides/berlitz2/Budapest-History.txt
./travel_guides/berlitz2/China-WhatToDo.txt
./travel_guides/berlitz2/Athens-WhatToDo.txt
./travel_guides/berlitz2/Nepal-WhatToDo.txt
./travel_guides/berlitz2/Bermuda-WhereToGo.txt
./travel_guides/berlitz2/Paris-WhatToDo.txt
./travel_guides/berlitz2/Cuba-History.txt
./travel_guides/berlitz2/Vallarta-WhereToGo.txt
./travel_guides/berlitz2/Bahamas-History.txt
./travel_guides/berlitz2/Beijing-WhatToDo.txt
./travel_guides/berlitz2/Cancun-WhereToGo.txt
```

- example 2: `Justins-MacBook-Air:written_2 justinyang$ find . -mmin -20`

```
./non-fiction/OUP/Castro/chR.txt
```

exec option
---

This command line option find files and perform specific actions on them.

- example 1: `find -exec`

```

```

- example 2: `find -exec`



Conclusion
---

Four command line options I researched:

- `-size`: find files that is less than or greater than a specific file size.
- `-type`: find files that is a specific type.
- `-mtime`: find files that is modified within specific time in days.
- `-exec`: find files and perform specific actions on them.

Source
---
  
ChatGPT
