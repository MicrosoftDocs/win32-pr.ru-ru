---
title: Иаженткоммандсекс
description: Иаженткоммандсекс
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a2450d94e89dd9dddc00a11af7f37bf4837558
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411055"
---
# <a name="iagentcommandsexgetfontsize"></a>Иаженткоммандсекс:: FontSize

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 




