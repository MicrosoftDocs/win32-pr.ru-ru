---
title: Иажентнотифисинк Баллунвисиблестате
description: Иажентнотифисинк Баллунвисиблестате
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f61f1213c6d947f2ca23e0b67ff8eef393892f4732e4a419ec93c277a62af99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976184"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a>Иажентнотифисинк:: Баллунвисиблестате

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT BalloonVisibleState(
   long dwCharID,  // character ID
   long bVisible   // visibility flag
);                          
```

Уведомляет клиентское приложение, когда изменяется состояние видимости всплывающего слова символа.

-   Нет возвращаемого значения.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*
</dt> <dd>

Идентификатор символа, чье состояние видимости всплывающей подсказки слова изменилось.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*бвисибле*
</dt> <dd>

Флаг видимости. Это логическое значение имеет **значение true** , когда отображается всплывающее сообщение слова "символ". и **false** , если он скрыт.

</dd> </dl>

Это событие отправляется всем клиентам символа.

 

 




