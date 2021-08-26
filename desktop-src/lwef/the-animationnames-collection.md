---
title: Коллекция Аниматионнамес
description: Коллекция Аниматионнамес
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c9ee781b836599ccf9689bfae974fd4cf3af32d75df2070e984ae9b6596f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960664"
---
# <a name="the-animationnames-collection"></a>Коллекция Аниматионнамес

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

Коллекция [**аниматионнамес**](https://www.bing.com/search?q=**AnimationNames**) — это специальная коллекция, содержащая список имен анимаций, скомпилированных для символа. С помощью коллекции можно перечислить имена анимаций для символа. например, в Visual Basic или VBScript (2,0 или более поздней версии) доступ к этим именам можно получить с помощью команды **For Each... Следующие** операторы:


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



Элементы в коллекции не имеют свойств, поэтому доступ к отдельным элементам напрямую невозможен.

Предмет. ACF символов коллекция возвращает все анимации, определенные для символа, а не только те, которые были получены с помощью метода [**Get**](get-method.md) .

 

 




