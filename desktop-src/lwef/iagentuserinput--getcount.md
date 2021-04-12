---
title: Иажентусеринпут вычислить
description: Иажентусеринпут вычислить
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac4b597f7367eff10154bde256698ef371c3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252700"
---
# <a name="iagentuserinputgetcount"></a>Иажентусеринпут:: NOCOUNT

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




