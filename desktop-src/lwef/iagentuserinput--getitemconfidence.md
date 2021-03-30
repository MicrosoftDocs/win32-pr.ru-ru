---
title: Иажентусеринпут Жетитемконфиденце
description: Иажентусеринпут Жетитемконфиденце
ms.assetid: 7d1ca2f0-416c-43c3-99a8-9f287cb88de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846e1fca9ea1245a62fc68330d68263b63fb7cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328200"
---
# <a name="iagentuserinputgetitemconfidence"></a>Иажентусеринпут:: Жетитемконфиденце

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetItemConfidence(
   long dwItemIndex,    // index of Command alternative
   long * plConfidence  // address of confidence value for Command 
);
```

Получает значение достоверности для [**команды**](command-event.md) , передаваемой в обратный вызов [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*двитеминдекс*
</dt> <dd>

Индекс альтернативы [**команды**](command-event.md) , передаваемой обратному вызову [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*плконфиденце*
</dt> <dd>

Адрес переменной, получающей оценку достоверности для альтернативы [**команды**](command-event.md) , передаваемой обратному вызову [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .

</dd> </dl>

Если речевой ввод не является источником команды, например, если пользователь выбрал команду во всплывающем меню символа, сервер Microsoft Agent возвращает значение достоверности наилучшего соответствия, равное 100, и значения достоверности для всех остальных альтернатив в виде нуля (0).

## <a name="see-also"></a>См. также:

[**Иажентусеринпут:: жетитемид**](iagentuserinput--getitemid.md), [**Иажентусеринпут:: жеталлитемдата**](iagentuserinput--getallitemdata.md), [**иажентусеринпут:: жетитемтекст**](iagentuserinput--getitemtext.md)


 

 




