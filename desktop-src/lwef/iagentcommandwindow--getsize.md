---
title: Иаженткоммандвиндов
description: Иаженткоммандвиндов
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 200853d88f4f4ea70fce0f80d73f343a2a4d46935a2dfca0ebf78021b0b884ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961584"
---
# <a name="iagentcommandwindowgetsize"></a>Иаженткоммандвиндов:: DataSize

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for Voice Commands Window width
   long * plHeight  // address of variable for Voice Commands Window height
);
```

Получает текущий размер окна "Voice Commands".

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*плвидс*
</dt> <dd>

Адрес переменной, получающей ширину окна "Voice Commands" (в пикселях) относительно начала экрана (сверху слева).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*плхеигхт*
</dt> <dd>

Адрес переменной, получающей высоту окна "Voice Commands" (в пикселях) относительно начала экрана (сверху слева).

</dd> </dl>

## <a name="see-also"></a>См. также

[**Иаженткоммандвиндов:: Disposition**](iagentcommandwindow--getposition.md)


 

 




