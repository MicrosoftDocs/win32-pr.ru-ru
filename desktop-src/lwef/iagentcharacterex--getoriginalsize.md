---
title: Иажентчарактерекс Жеторигиналсизе
description: Иажентчарактерекс Жеторигиналсизе
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55abb64a8466b13ee41119e2a8a359ceeb182c92f7b4d2b1071547df07110052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750522"
---
# <a name="iagentcharacterexgetoriginalsize"></a>Иажентчарактерекс:: Жеторигиналсизе

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetOriginalSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

Получает исходный размер кадра анимации символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*плвидс*
</dt> <dd>

Адрес переменной, получающей исходную ширину кадра анимации символов в пикселях.

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*плхеигхт*
</dt> <dd>

Адрес переменной, получающей исходную высоту кадра анимации символов в пикселях.

</dd> </dl>

Этот вызов возвращает исходный размер рамки символов, созданной в редакторе символов Microsoft Agent.

## <a name="see-also"></a>См. также

[**Иажентчарактер:: DataSize**](iagentcharacter--getsize.md)


 

 




