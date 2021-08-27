---
title: Иажентчарактер
description: Иажентчарактер
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297f187b7045b1da5773643f2765160c71fbca0d4eb7c6ec12c4032e2f1d5806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114784"
---
# <a name="iagentcharacterstop"></a>Иажентчарактер:: останавливаться

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иажентчарактер::P готовка**](iagentcharacter--prepare.md), [ **иажентчарактер:: стопалл**](iagentcharacter--stopall.md)


 

 




