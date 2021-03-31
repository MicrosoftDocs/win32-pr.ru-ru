---
title: Иажентчарактер SetPosition
description: Иажентчарактер SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee48ea26c714c570f7ae11b9b2dbc0fe92ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067754"
---
# <a name="iagentcharactersetposition"></a>Иажентчарактер:: SetPosition

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 




