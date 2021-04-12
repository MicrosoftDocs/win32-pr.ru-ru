---
title: Иажентчарактер
description: Иажентчарактер
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cdff0d6876fc7257e05014f3d9ba695db5d168
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332760"
---
# <a name="iagentcharactergetposition"></a>Иажентчарактер:: Disposition

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

Возвращает расположение кадра анимации символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*пллефт*
</dt> <dd>

Адрес переменной, получающей экранную координату левого края кадра анимации символов в пикселях относительно начала координат экрана (в левом верхнем углу).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*плтоп*
</dt> <dd>

Адрес переменной, получающей экранную координату верхнего края кадра анимации символов в пикселях относительно начала координат экрана (в левом верхнем углу).

</dd> </dl>

Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на его прямоугольной рамке анимации.

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: SetPosition**](iagentcharacter--setposition.md), [ **иажентчарактер:: DataSize**](iagentcharacter--getsize.md)


 

 




