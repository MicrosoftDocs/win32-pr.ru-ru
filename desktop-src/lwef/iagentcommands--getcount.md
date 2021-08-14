---
title: Иаженткоммандс вычислить
description: Иаженткоммандс вычислить
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 810f9fc268bc13558e4e51a3b64dd6f5b1d54caa5a055d9c90b6a8d11c48b3c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749828"
---
# <a name="iagentcommandsgetcount"></a>Иаженткоммандс:: NOCOUNT

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 