---
title: Коллекция Аниматионнамес
description: Коллекция Аниматионнамес
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9e0c2c1d42f51f9d50bafaee61b6ab51d5b85f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888404"
---
# <a name="the-animationnames-collection"></a>Коллекция Аниматионнамес

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

Коллекция [**аниматионнамес**](https://www.bing.com/search?q=**AnimationNames**) — это специальная коллекция, содержащая список имен анимаций, скомпилированных для символа. С помощью коллекции можно перечислить имена анимаций для символа. Например, в Visual Basic или VBScript (2,0 или более поздней версии) доступ к этим именам можно получить с помощью команды **For Each... Следующие** операторы:


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



Элементы в коллекции не имеют свойств, поэтому доступ к отдельным элементам напрямую невозможен.

Предмет. ACF символов коллекция возвращает все анимации, определенные для символа, а не только те, которые были получены с помощью метода [**Get**](get-method.md) .

 

 




