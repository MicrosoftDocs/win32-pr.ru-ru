---
title: Иаженткоммандсекс
description: Иаженткоммандсекс
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92f2ce1908ea5f37d24fb8a085204917440f61ae30feb1e596639d0240c353d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976274"
---
# <a name="iagentcommandsexgetfontsize"></a>Иаженткоммандсекс:: FontSize

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

Извлекает значение размера шрифта, отображаемого во всплывающем меню символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*плфонтсизе*
</dt> <dd>

Адрес значения, получающего размер шрифта.

</dd> </dl>

Размер кегля возвращаемого шрифта соответствует размеру, определенному для отображения текста во всплывающем меню символа, если клиент является входным. Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра идентификатор языка символа, или если параметр не задан, используется пользовательский язык по умолчанию.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

## <a name="see-also"></a>См. также:

[**Иаженткоммандсекс:: сетфонтсизе**](iagentcommandsex--setfontsize.md), [ **иаженткоммандсекс:: сетфонтнаме**](iagentcommandsex--setfontname.md)


 

 




