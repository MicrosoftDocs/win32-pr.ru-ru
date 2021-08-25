---
title: Иажентчарактер
description: Иажентчарактер
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089226f98969594a1d19afc7f3bb529c30943e06ec4083364dc5ae2f9850c9c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848524"
---
# <a name="iagentcharactersetsize"></a>Иажентчарактер:: SetSize

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetSize(
   long * lWidth,  // width of the character frame
   long * lHeight  // height of the character frame
);
```

Задает размер кадра анимации символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*лвидс*
</dt> <dd>

Ширина кадра анимации символа в пикселях.

</dd> <dt>

<span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*лхеигхт*
</dt> <dd>

Высота кадра анимации символа (в пикселях).

</dd> </dl>

Изменение размера кадра символа масштабирует символ до размера, заданного этим методом. Параметр этого свойства применяется ко всем клиентам символа.

Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на его прямоугольной рамке анимации.

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: DataSize**](iagentcharacter--getsize.md)


 

 




