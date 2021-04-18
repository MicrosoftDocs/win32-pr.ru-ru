---
title: Иажентпропертишит
description: Иажентпропертишит
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5e185a6e8d55d87e561f727c8dc9df8a8cfd63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700574"
---
# <a name="iagentpropertysheetgetsize"></a>Иажентпропертишит:: DataSize

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

Возвращает размер окна страницы свойств агента Microsoft Agent.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*плвидс*
</dt> <dd>

Адрес переменной, получающей ширину страницы свойств в пикселях относительно начала координат экрана (в левом верхнем углу).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*плхеигхт*
</dt> <dd>

Адрес переменной, которая получает высоту страницы свойств в пикселях относительно начала координат экрана (в левом верхнем углу).

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иажентпропертишит:: Disposition**](iagentpropertysheet--getposition.md)


 

 




