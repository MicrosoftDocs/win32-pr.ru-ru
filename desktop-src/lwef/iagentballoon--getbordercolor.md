---
title: Иажентбаллун Жетбордерколор
description: Иажентбаллун Жетбордерколор
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ed636d5209402959adbb2a777577a87c8cc23f8eed4faeb8ac003981e5e2d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478638"
---
# <a name="iagentballoongetbordercolor"></a>Иажентбаллун:: Жетбордерколор

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetBorderColor (
  long * plBorderColor// address of variable for border color displayed
);                    // for word balloon
```

Извлекает значение цвета границы, отображаемого для всплывающей подсказки.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*плбордерколор*
</dt> <dd>

Адрес переменной, получающей параметр цвета для границы всплывающей подсказки.

</dd> </dl>

Цвет границы для всплывающего слова символа определяется в редакторе символов Microsoft Agent. Оно не может быть изменено приложением. Однако пользователь может изменить цвет границы для всех символов на странице свойств Microsoft Agent.

## <a name="see-also"></a>См. также

[**Иажентбаллун:: жетбаккколор**](iagentballoon--getbackcolor.md), [ **иажентбаллун:: "ForeColor"**](iagentballoon--getforecolor.md)


 

 




