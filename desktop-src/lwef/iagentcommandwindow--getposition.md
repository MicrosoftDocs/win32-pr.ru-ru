---
title: Иаженткоммандвиндов
description: Иаженткоммандвиндов
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52571311a87ee0846dcaf515912762069fe3025a25c5a2589770ee9738bb2de7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716104"
---
# <a name="iagentcommandwindowgetposition"></a>Иаженткоммандвиндов:: Disposition

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

Возвращает расположение окна "Voice Commands".

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*пллефт*
</dt> <dd>

Адрес переменной, которая получает координату экрана левого края окна "Voice Commands" в пикселях относительно начала координат экрана (вверху слева).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*плтоп*
</dt> <dd>

Адрес переменной, которая получает координату экрана верхнего края окна "Voice Commands" в пикселях относительно начала координат экрана (вверху слева).

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иаженткоммандвиндов:: DataSize**](iagentcommandwindow--getsize.md)


 

 




