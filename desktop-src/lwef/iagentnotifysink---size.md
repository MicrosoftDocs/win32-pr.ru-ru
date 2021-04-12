---
title: Размер Иажентнотифисинк
description: Размер Иажентнотифисинк
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252ad15f6bb5201e8ec000292d1e89efe9368934
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532291"
---
# <a name="iagentnotifysinksize"></a>Иажентнотифисинк:: size

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Size(
   long dwCharID,  // character ID
   long lWidth,    // new width
   long lHeight,   // new height
);                          
```

Уведомляет клиентское приложение об изменении размера символа.

-   Нет возвращаемого значения.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*
</dt> <dd>

Идентификатор символа, размер которого был изменен.

</dd> <dt>

<span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*лвидс*
</dt> <dd>

Ширина кадра анимации символа в пикселях.

</dd> <dt>

<span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*лхеигхт*
</dt> <dd>

Высота кадра анимации символа (в пикселях).

</dd> </dl>

Это событие отправляется всем клиентам символа.

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: DataSize**](iagentcharacter--getsize.md), [ **иажентчарактер:: SetSize**](iagentcharacter--setsize.md)


 

 




