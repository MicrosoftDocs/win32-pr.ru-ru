---
title: Иажентнотифисинк закладка
description: Иажентнотифисинк закладка
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1febedfc962904544a49b8621812d0518026b459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774846"
---
# <a name="iagentnotifysinkbookmark"></a>Иажентнотифисинк:: Bookmark

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

Уведомляет клиентское приложение о завершении заданной закладки.

-   Нет возвращаемого значения.

<dl> <dt>

<span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*двбукмаркид*
</dt> <dd>

Идентификатор закладки, которая привела к срабатыванию события.

</dd> </dl>

При включении тегов закладок в метод [**говорите**](speak-method.md) можно отнестись к возникновению этого события.

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: говорите**](iagentcharacter--speak.md), [теги выходных данных агента Microsoft Agent](microsoft-agent-speech-output-tags.md)


 

 




