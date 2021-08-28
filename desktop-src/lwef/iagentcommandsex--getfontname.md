---
title: Иаженткоммандсекс Жетфонтнаме
description: Иаженткоммандсекс Жетфонтнаме
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 757b2d7554f1efcee27a519b9df61b4601a237b557c3aa26b6575864144a2850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105240"
---
# <a name="iagentcommandsexgetfontname"></a>Иаженткоммандсекс:: Жетфонтнаме

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иаженткоммандсекс:: сетфонтнаме**](iagentcommandsex--setfontname.md), [ **иаженткоммандсекс:: сетфонтсизе**](iagentcommandsex--setfontsize.md)


 

 




