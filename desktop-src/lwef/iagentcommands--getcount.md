---
title: Иаженткоммандс вычислить
description: Иаженткоммандс вычислить
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ece3e007b644b370ee721cef2d273fa50d43ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412785"
---
# <a name="iagentcommandsgetcount"></a>Иаженткоммандс:: NOCOUNT

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of count of commands
);                    
```

Возвращает количество объектов [**Command**](/windows/desktop/lwef/the-command-object) в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*пдвкаунт*
</dt> <dd>

Адрес переменной, которая получает количество [**команд**](/windows/desktop/lwef/the-command-object) в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

*пдвкаунт* включает только число [**команд**](/windows/desktop/lwef/the-command-object) , определяемых в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) . Сервер или другие записи клиента не включены.

 

 