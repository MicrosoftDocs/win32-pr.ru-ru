---
title: Иажентусеринпут вычислить
description: Иажентусеринпут вычислить
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f52c296dd152fd1e31a87e21d80f8b25d52ae880b300487cdcba746e81dfa0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749521"
---
# <a name="iagentuserinputgetcount"></a>Иажентусеринпут:: NOCOUNT

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

Возвращает число вариантов [**команд**](command-event.md) , передаваемых обратному вызову [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*пдвкаунт*
</dt> <dd>

Адрес переменной, которая получает количество вариантов [**команд**](command-event.md) , идентифицируемых сервером.

</dd> </dl>

Если речевой ввод не является источником команды, например, если пользователь выбрал команду во всплывающем меню символа, функция **NOCOUNT** возвращает значение 1. Если функция **NOCOUNT** возвращает ноль (0), подсистема распознавания речи обнаружила речевой ввод, но определила, что соответствующей команды не было.

 

 




