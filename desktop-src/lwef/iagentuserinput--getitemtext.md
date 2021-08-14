---
title: Иажентусеринпут Жетитемтекст
description: Иажентусеринпут Жетитемтекст
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd9c1392bd56e3bb59212edeb79d862260786edb87583c0e8fdf049e8345b40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359044"
---
# <a name="iagentuserinputgetitemtext"></a>Иажентусеринпут:: Жетитемтекст

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иажентусеринпут:: жетитемконфиденце**](iagentuserinput--getitemconfidence.md), [**Иажентусеринпут:: жетитемид**](iagentuserinput--getitemid.md), [**иажентусеринпут:: жеталлитемдата**](iagentuserinput--getallitemdata.md)


 

 




