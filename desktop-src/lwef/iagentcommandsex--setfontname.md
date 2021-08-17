---
title: Иаженткоммандсекс Сетфонтнаме
description: Иаженткоммандсекс Сетфонтнаме
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511425df848749791d2803a484e00da8e838cfa191eade05c578fdad4b3ca6cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105207"
---
# <a name="iagentcommandsexsetfontname"></a>Иаженткоммандсекс:: Сетфонтнаме

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font to be displayed in character's pop-up menu
);
```

Задает шрифт, отображаемый во всплывающем меню символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*бсзфонтнаме*
</dt> <dd>

Значение типа BSTR, которое задает шрифт, отображаемый во всплывающем меню символа.

</dd> </dl>

Это свойство определяет шрифт, используемый для отображения текста во всплывающем меню символа. Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра идентификатор языка символа — или, если это не задано — параметр идентификатор языка пользователя по умолчанию.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

## <a name="see-also"></a>См. также

[**Иаженткоммандсекс:: жетфонтнаме**](iagentcommandsex--getfontname.md), [**Иаженткоммандсекс:: FontSize**](iagentcommandsex--getfontsize.md), [**иаженткоммандсекс:: сетфонтсизе**](iagentcommandsex--setfontsize.md)


 

 




