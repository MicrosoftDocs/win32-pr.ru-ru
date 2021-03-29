---
title: Иажентбаллун Жетбордерколор
description: Иажентбаллун Жетбордерколор
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f78bf9425cbb12c6a87f3ad64b6c5523dc7bbd8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777582"
---
# <a name="iagentballoongetbordercolor"></a>Иажентбаллун:: Жетбордерколор

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также:

[**Иажентбаллун:: жетбаккколор**](iagentballoon--getbackcolor.md), [ **иажентбаллун:: "ForeColor"**](iagentballoon--getforecolor.md)


 

 




