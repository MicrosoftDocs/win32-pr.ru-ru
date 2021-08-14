---
title: Обработчики событий
description: Обработчики событий
ms.assetid: abb5f123-b838-46fb-ab11-cee70cc76a38
keywords:
- обложки проигрыватель Windows Media, обработчики событий в JScript
- обложки, обработчики событий в JScript
- события, JScript
- JScript файлы для обложек, обработчики событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94c936e36cd9b7404260473068ccc3d6c3f5d0ab75553ba878dff88587e535ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339275"
---
# <a name="event-handlers"></a>Обработчики событий

Microsoft JScript используется для обработки событий в файле определения обложки. Дополнительные сведения о обработчиках событий см. в разделе [Обработка событий](handling-events.md) .

в обработчике событий может быть несколько строк кода, но необходимо соблюдать осторожность, чтобы не превысить длину строки, которая JScript разрешена. Разделяйте строки точками с запятой.


```C++
onclick = "JScript: player.URL = 'https://proseware.com/cool.wma' ; myText.value = 'Playing'; "

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Использование JScript**](using-jscript.md)
</dt> </dl>

 

 




