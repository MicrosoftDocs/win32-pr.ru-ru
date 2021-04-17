---
title: Иажентусеринпут Жетитемид
description: Иажентусеринпут Жетитемид
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ae1386d87fa6051111801c5603837519eeb4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700467"
---
# <a name="iagentuserinputgetitemid"></a>Иажентусеринпут:: Жетитемид

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetItemID(
   long dwItemIndex,    // index of Command alternative
   long * pdwCommandID  // address of a variable for number of alternatives 
);
```

Получает идентификатор альтернативной [**команды**](command-event.md) , передаваемой обратному вызову [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*двитеминдекс*
</dt> <dd>

Индекс альтернативы [**команды**](command-event.md) , переданной в обратный вызов [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*пдвкоммандид*
</dt> <dd>

Адрес переменной, которая получает идентификатор [**команды**](command-event.md).

</dd> </dl>

Если голосовое входное значение активирует обратный вызов [**иажентнотифисинк:: Command**](iagentnotifysink--command.md) , сервер возвращает идентификаторы для всех совпадающих [**команд**](command-event.md) , определенных приложением.

## <a name="see-also"></a>См. также:

[**Иажентусеринпут:: жетитемконфиденце**](iagentuserinput--getitemconfidence.md), [**Иажентусеринпут:: жетитемтекст**](iagentuserinput--getitemtext.md), [**иажентусеринпут:: жеталлитемдата**](iagentuserinput--getallitemdata.md)


 

 




