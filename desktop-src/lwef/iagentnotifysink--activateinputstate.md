---
title: Иажентнотифисинк Активатеинпутстате
description: Иажентнотифисинк Активатеинпутстате
ms.assetid: 2476e475-d80c-47e9-bb60-e0fca41becc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437a2d86ae3d79a51bc2adc3b3d32ee719502087c4c723e2c1778103596b97d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749586"
---
# <a name="iagentnotifysinkactivateinputstate"></a>Иажентнотифисинк:: Активатеинпутстате

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT ActivateInputState(
   long dwCharID,   // character ID
   long bActivated  // input activation flag
);                          
```

Уведомляет клиентское приложение о том, что введенное значение активного состояния ввода символа изменилось.

-   Нет возвращаемого значения.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*
</dt> <dd>

Идентификатор символа, состояние активации которого изменилось.

</dd> <dt>

<span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*бактиватед*
</dt> <dd>

Входной флаг активности. Это логическое значение равно **true** , если символ, на который ссылается *двчарид* , стал активным входным. и **false** , если символ потерял активное состояние входа.

</dd> </dl>

 

 




