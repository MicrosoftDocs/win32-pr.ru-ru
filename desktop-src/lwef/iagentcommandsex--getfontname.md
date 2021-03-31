---
title: Иаженткоммандсекс Жетфонтнаме
description: Иаженткоммандсекс Жетфонтнаме
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215f08cbe1e5e97b218f9279baff5e3affd74956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411056"
---
# <a name="iagentcommandsexgetfontname"></a>Иаженткоммандсекс:: Жетфонтнаме

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

Извлекает значение шрифта, отображаемого во всплывающем меню символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*пбсзфонтнаме*
</dt> <dd>

Адрес BSTR, который получает имя шрифта, отображаемое во всплывающем меню символа.

</dd> </dl>

Возвращаемое имя шрифта соответствует шрифту, используемому для отображения текста во всплывающем меню символа, если клиентское приложение является входным. Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра идентификатор языка символа, или если параметр не задан, используется идентификатор языка пользователя по умолчанию.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

## <a name="see-also"></a>См. также:

[**Иаженткоммандсекс:: сетфонтнаме**](iagentcommandsex--setfontname.md), [ **иаженткоммандсекс:: сетфонтсизе**](iagentcommandsex--setfontsize.md)


 

 




