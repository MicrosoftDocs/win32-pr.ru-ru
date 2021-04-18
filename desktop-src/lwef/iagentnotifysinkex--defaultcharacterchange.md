---
title: Иажентнотифисинкекс Дефаултчарактерчанже
description: Иажентнотифисинкекс Дефаултчарактерчанже
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ec212887d17d1aa59d942ece79b3e6928900ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700611"
---
# <a name="iagentnotifysinkexdefaultcharacterchange"></a>Иажентнотифисинкекс::D Ефаултчарактерчанже

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

Уведомляет клиентское приложение об изменении символа по умолчанию.

-   Нет возвращаемого значения.

<dl> <dt>

<span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*бсзгуид*
</dt> <dd>

Уникальный идентификатор для символа.

</dd> </dl>

Когда пользователь изменяет символ, назначенный в качестве символа по умолчанию для пользователя, сервер отправляет это событие клиентам, которые загрузили символ по умолчанию. Событие возвращает уникальный идентификатор (GUID) символа, отформатированный с помощью фигурных скобок и дефисов, который определяется при построении символа с помощью редактора символов Microsoft Agent.

Когда появляется новый символ, он предполагает тот же размер, что и любой уже загруженный экземпляр символа или предыдущий символ по умолчанию (в указанном порядке).

## <a name="see-also"></a>См. также:

[**Иажент:: Load**](iagent--load.md)


 

 




