---
title: Иажентчарактер
description: Иажентчарактер
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a63e75111b7694fcb993e141b8534e8f174efd1a1a252f250167ecb597149f7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609994"
---
# <a name="iagentcharactergetposition"></a>Иажентчарактер:: Disposition

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 




