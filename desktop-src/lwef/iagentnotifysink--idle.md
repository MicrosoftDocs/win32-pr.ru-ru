---
title: Иажентнотифисинк бездействие
description: Иажентнотифисинк бездействие
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8263bd9bc62d4fccfad74b18b189c6e4bae426245dd3d4d6a46c826ebacf498d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105184"
---
# <a name="iagentnotifysinkidle"></a>Иажентнотифисинк:: Idle

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

Уведомляет клиентское приложение, когда изменилось состояние **состояние простояа** символа.

-   Нет возвращаемого значения.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*
</dt> <dd>

Идентификатор запущенного запроса.

</dd> <dt>

<span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*Откройте*
</dt> <dd>

Начальный флаг. Это логическое значение имеет **значение true** , если символ начинается состояние простоя и **false** при остановке состояние простоя.

</dd> </dl>

Это событие позволяет контролировать, когда сервер Microsoft Agent запускает или останавливает обработку символа в состоянии простоя.

## <a name="see-also"></a>См. также

[**Иажентчарактер:: жетидлеон**](iagentcharacter--getidleon.md), [ **иажентчарактер:: сетидлеон**](iagentcharacter--setidleon.md)


 

 




