---
title: Иажентнотифисинк Рекуесткомплете
description: Иажентнотифисинк Рекуесткомплете
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265a7111369dec687fd74b9c66c27275a40e164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332000"
---
# <a name="iagentnotifysinkrequestcomplete"></a>Иажентнотифисинк:: Рекуесткомплете

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

Уведомляет клиентское приложение о завершении запроса.

-   Нет возвращаемого значения.

<dl> <dt>

<span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*дврекуестид*
</dt> <dd>

Идентификатор запущенного запроса.

</dd> <dt>

<span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*хрстатус*
</dt> <dd>

Код состояния. Этот параметр возвращает код состояния для запроса.

</dd> </dl>

Это событие позволяет отслеживанию завершения метода, поставленного в очередь, с помощью идентификатора запроса.

## <a name="see-also"></a>См. также:

[**Иажентнотифисинк:: рекуестстарт**](iagentnotifysink--requeststart.md), [**Иажент:: Load**](iagent--load.md), [**иажентчарактер:: Жестуреат**](iagentcharacter--gestureat.md), [**иажентчарактер:: Hide**](iagentcharacter--hide.md), [**иажентчарактер:: Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter:: MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::P готовка**](iagentcharacter--prepare.md), [**IAgentCharacter::Pный макет**](iagentcharacter--play.md), [**IAgentCharacter:: Показать**](iagentcharacter--show.md), [**IAgentCharacter:: говорите**](iagentcharacter--speak.md), [**IAgentCharacter:: wait**](iagentcharacter--wait.md)


 

 




