---
title: Иажентчарактер
description: Иажентчарактер
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af078eb9980399793e00f8bd3deaefef7f048a900423c1ee50ac8d4f4a310b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962234"
---
# <a name="iagentcharactergetsize"></a>Иажентчарактер:: DataSize

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

Возвращает размер кадра анимации символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*плвидс*
</dt> <dd>

Адрес переменной, получающей ширину кадра анимации символов в пикселях относительно начала координат экрана (в левом верхнем углу).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*плхеигхт*
</dt> <dd>

Адрес переменной, получающей высоту кадра анимации символов в пикселях относительно начала координат экрана (в левом верхнем углу).

</dd> </dl>

Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на его прямоугольной рамке анимации.

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: SetSize**](iagentcharacter--setsize.md)


 

 




