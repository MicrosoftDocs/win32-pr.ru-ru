---
title: Иажентбаллун
description: Иажентбаллун
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7a251471b0281661b087dbfb9b141c54ff9dc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710149"
---
# <a name="iagentballoongetforecolor"></a>Иажентбаллун::/ForeColor

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetForeColor(
   long * plFGColor // address of variable for foreground color displayed
);                  // in word balloon
```

Извлекает значение цвета переднего плана, отображаемого в окне всплывающей подсказки.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*плфгколор*
</dt> <dd>

Адрес переменной, получающей параметр цвета для переднего плана.

</dd> </dl>

Цвет переднего плана, используемый в подсказке для символьного слова, определен в редакторе символов Microsoft Agent. Оно не может быть изменено приложением. Однако пользователь может переопределить цвет переднего плана для всех символов на странице свойств Microsoft Agent.

## <a name="see-also"></a>См. также:

[**Иажентбаллун:: Жетбаккколор**](iagentballoon--getbackcolor.md)


 

 




