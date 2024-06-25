+++
title = 'SOLVED Error Says to Remove Site From Gitmodules but Its Not There Hugo Submodule With PaperMod'
date = 2024-06-25T21:54:51+07:00
description = "i will to explain why hugo PaperMod can't deploy to github because error says to remove site from .gitmodules but it's not ..."
tags = [
    "tips&tricks",
    "programming",
    "static-website",
    "hugo-static",
]
categories = [
    "programming",
    "hugo-static",
    "bloging",
    "solved",
]
series = ["Themes Guide"]
aliases = ["static-website"]
image = "gitsubmodule.jpg"
+++


### mian topics
i will to explain why hugo PaperMod can't deploy to github because error says to remove site from .gitmodules but it's not ......**_

in this case, i install Hugo PaperMod theme use as submodule.

why error can't deploy to github because from .gimodules it appears? this happens because no file .gitmodules inside my hugo project, for that i need to create a file .gitmodules, Inside the .gitmodules file contains.

```
[submodule "themes/PaperMod"]
	path = themes/PaperMod
	url = https://github.com/adityatelange/hugo-PaperMod.git
```

 the location of **.gitmodules** file is more or less like this


``````````flow
-->your hugo project
     |
      -->.gitmodules file
``````````

and should this matter be resolved 😃
