---
title: Иажентчарактерекс Жеторигиналсизе
description: Иажентчарактерекс Жеторигиналсизе
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e1712587e70d9756e3d37ca9e0f3cbfdb82c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067790"
---
# <a name="iagentcharacterexgetoriginalsize"></a>Иажентчарактерекс:: Жеторигиналсизе

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: DataSize**](iagentcharacter--getsize.md)


 

 




