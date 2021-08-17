---
title: Иажентпропертишит
description: Иажентпропертишит
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74609f2e5f3201be07c425db17456f17e5202e6497b8b137815ae6124335650
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976144"
---
# <a name="iagentpropertysheetgetposition"></a>Иажентпропертишит:: Disposition

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иажентпропертишит:: DataSize**](iagentpropertysheet--getsize.md)


 

 




