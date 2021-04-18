---
title: Иажентнотифисинк Баллунвисиблестате
description: Иажентнотифисинк Баллунвисиблестате
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2dd63d8eef3a7f1a70af81e13506a7e92ad84f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700612"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a>Иажентнотифисинк:: Баллунвисиблестате

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




