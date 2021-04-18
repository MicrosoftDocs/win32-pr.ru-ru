---
title: Обработчики событий
description: Обработчики событий
ms.assetid: abb5f123-b838-46fb-ab11-cee70cc76a38
keywords:
- Обложки проигрывателя Windows Media, обработчики событий в JScript
- обложки, обработчики событий в JScript
- события, JScript
- Файлы JScript для обложек, обработчики событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec4413ae3a2358b01685cd0edfe66de92810a64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691134"
---
# <a name="event-handlers"></a>Обработчики событий

Microsoft JScript используется для обработки событий в файле определения обложки. Дополнительные сведения о обработчиках событий см. в разделе [Обработка событий](handling-events.md) .

В обработчике событий может быть несколько строк кода, но необходимо соблюдать осторожность, чтобы не превысить длину строки, которую разрешает JScript. Разделяйте строки точками с запятой.


```C++
onclick = "JScript: player.URL = 'https://proseware.com/cool.wma' ; myText.value = 'Playing'; "

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование JScript**](using-jscript.md)
</dt> </dl>

 

 




