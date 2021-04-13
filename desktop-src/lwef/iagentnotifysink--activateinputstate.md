---
title: Иажентнотифисинк Активатеинпутстате
description: Иажентнотифисинк Активатеинпутстате
ms.assetid: 2476e475-d80c-47e9-bb60-e0fca41becc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821f5943bb87f9c19a66125028604fa5d116a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258759"
---
# <a name="iagentnotifysinkactivateinputstate"></a>Иажентнотифисинк:: Активатеинпутстате

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




