---
title: Иаженткоммандвиндов
description: Иаженткоммандвиндов
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cf42d98f811905590209b6fed70b28a5728903
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710099"
---
# <a name="iagentcommandwindowgetsize"></a>Иаженткоммандвиндов:: DataSize

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также:

[**Иаженткоммандвиндов:: Disposition**](iagentcommandwindow--getposition.md)


 

 




