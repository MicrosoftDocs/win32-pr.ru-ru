---
title: Иажентчарактер
description: Иажентчарактер
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40c219cd0a1dc1d11738149ca7cfd9869fe682e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332755"
---
# <a name="iagentcharactergetsize"></a>Иажентчарактер:: DataSize

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 




