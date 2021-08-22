---
title: Иажентусеринпут Жетитемид
description: Иажентусеринпут Жетитемид
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde65fc10a4cb467bd69f200e3244f1a2a73c0424d64f6a4babbd2cefd18e0be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609264"
---
# <a name="iagentuserinputgetitemid"></a>Иажентусеринпут:: Жетитемид

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 




