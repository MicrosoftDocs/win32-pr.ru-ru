---
title: Иажентпропертишит
description: Иажентпропертишит
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff4dcac994901824d7dc37868d7fcfc3f39cefd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700575"
---
# <a name="iagentpropertysheetgetposition"></a>Иажентпропертишит:: Disposition

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

Получает расположение окна страницы свойств агента Майкрософт.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*пллефт*
</dt> <dd>

Адрес переменной, которая получает координату экрана левого края страницы свойств в пикселях относительно начала координат экрана (в левом верхнем углу).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*плтоп*
</dt> <dd>

Адрес переменной, которая получает координату экрана верхнего края страницы свойств в пикселях относительно начала координат экрана (в левом верхнем углу).

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иажентпропертишит:: DataSize**](iagentpropertysheet--getsize.md)


 

 




