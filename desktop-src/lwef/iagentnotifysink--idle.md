---
title: Иажентнотифисинк бездействие
description: Иажентнотифисинк бездействие
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43e060f361499b02bc0a83db697938975c76291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700681"
---
# <a name="iagentnotifysinkidle"></a>Иажентнотифисинк:: Idle

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: жетидлеон**](iagentcharacter--getidleon.md), [ **иажентчарактер:: сетидлеон**](iagentcharacter--setidleon.md)


 

 




