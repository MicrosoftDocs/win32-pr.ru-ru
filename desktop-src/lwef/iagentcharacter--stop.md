---
title: Иажентчарактер
description: Иажентчарактер
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356c81996a9410eccb2007dc5261913e30a1b414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411204"
---
# <a name="iagentcharacterstop"></a>Иажентчарактер:: останавливаться

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

Останавливает указанную анимацию (запрос) и удаляет ее из очереди анимации символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*дврекид*
</dt> <dd>

Идентификатор останавливаемого запроса.

</dd> </dl>

**Остановить** также можно использовать для остановки [**всех вызовов,**](iagentcharacter--prepare.md) помещенных в очередь.

## <a name="see-also"></a>См. также:

[**Иажентчарактер::P готовка**](iagentcharacter--prepare.md), [ **иажентчарактер:: стопалл**](iagentcharacter--stopall.md)


 

 




