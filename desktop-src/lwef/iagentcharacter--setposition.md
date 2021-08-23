---
title: Иажентчарактер SetPosition
description: Иажентчарактер SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e973ec08cdab89c2d8c2501bd9ea1778866f5f7fa1757fe746e44495e41c275a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665644"
---
# <a name="iagentcharactersetposition"></a>Иажентчарактер:: SetPosition

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

Задает расположение кадра анимации символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*ллефт*
</dt> <dd>

Координата экрана левого края кадра анимации символов в пикселях относительно начала координат экрана (вверху слева).

</dd> <dt>

<span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*лтоп*
</dt> <dd>

Координата экрана верхнего края кадра анимации символов в пикселях относительно начала координат экрана (в левом верхнем углу).

</dd> </dl>

Параметр этого свойства применяется ко всем клиентам символа. Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на его прямоугольной рамке анимации.

> [!Note]  
> В отличие от метода [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) , эта функция не находится в очереди.

 

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: Disposition**](iagentcharacter--getposition.md)


 

 




