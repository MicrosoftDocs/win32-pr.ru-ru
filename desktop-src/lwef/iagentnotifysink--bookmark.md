---
title: Иажентнотифисинк закладка
description: Иажентнотифисинк закладка
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02562b7cbf42c3445a25edc5071476da1b2d8dc53d80923ad875fddf09e5d31b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477100"
---
# <a name="iagentnotifysinkbookmark"></a>Иажентнотифисинк:: Bookmark

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иажентчарактер:: говорите**](iagentcharacter--speak.md), [теги выходных данных агента Microsoft Agent](microsoft-agent-speech-output-tags.md)


 

 




