---
title: Иаженткоммандвиндов
description: Иаженткоммандвиндов
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8c036d02c210ecb26da5dfde207bfe56afe8a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986562"
---
# <a name="iagentcommandwindowgetposition"></a>Иаженткоммандвиндов:: Disposition

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 




