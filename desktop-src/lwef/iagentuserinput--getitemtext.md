---
title: Иажентусеринпут Жетитемтекст
description: Иажентусеринпут Жетитемтекст
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7010172147f86282903641c46aa5137ce69c80be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067236"
---
# <a name="iagentuserinputgetitemtext"></a>Иажентусеринпут:: Жетитемтекст

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

Получает текст голоса для альтернативной [**команды**](command-event.md) , передаваемой обратному вызову [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*двитеминдекс*
</dt> <dd>

Индекс альтернативы [**команды**](command-event.md) , передаваемой обратному вызову [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*пбсзтекст*
</dt> <dd>

Адрес строки BSTR, которая получает значение текста голоса для [**команды**](command-event.md).

</dd> </dl>

Если речевой ввод не является источником команды, например, если пользователь выбрал команду во всплывающем меню символа, сервер возвращает **значение NULL** для текста голоса [**команды**](command-event.md).

## <a name="see-also"></a>См. также:

[**Иажентусеринпут:: жетитемконфиденце**](iagentuserinput--getitemconfidence.md), [**Иажентусеринпут:: жетитемид**](iagentuserinput--getitemid.md), [**иажентусеринпут:: жеталлитемдата**](iagentuserinput--getallitemdata.md)


 

 




