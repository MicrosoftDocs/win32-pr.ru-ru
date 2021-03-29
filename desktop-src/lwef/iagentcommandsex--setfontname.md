---
title: Иаженткоммандсекс Сетфонтнаме
description: Иаженткоммандсекс Сетфонтнаме
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9a4b76a58fc3651c02bedc43f8d372f607c2df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773694"
---
# <a name="iagentcommandsexsetfontname"></a>Иаженткоммандсекс:: Сетфонтнаме

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также:

[**Иаженткоммандсекс:: жетфонтнаме**](iagentcommandsex--getfontname.md), [**Иаженткоммандсекс:: FontSize**](iagentcommandsex--getfontsize.md), [**иаженткоммандсекс:: сетфонтсизе**](iagentcommandsex--setfontsize.md)


 

 




