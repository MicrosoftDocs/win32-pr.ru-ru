---
title: Иаженткоммандсекс Сетфонтсизе
description: Иаженткоммандсекс Сетфонтсизе
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19bb9a638141dc3cebe683748500510ea848a664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487592"
---
# <a name="iagentcommandsexsetfontsize"></a>Иаженткоммандсекс:: Сетфонтсизе

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

Задает размер шрифта, отображаемого во всплывающем меню символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*лфонтсизе*
</dt> <dd>

Размер шрифта.

</dd> </dl>

Это свойство определяет размер шрифта, используемого для отображения текста во всплывающем меню символа, если клиентское приложение является входным. Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра идентификатор языка символа — или, если это не задано — пользовательский параметр языка по умолчанию. Если вход не активен, текст [**заголовка**](caption-property.md) [**команды**](/windows/desktop/lwef/the-command-object) клиентского приложения отображается в кегле, указанном для клиента input-Active.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

## <a name="see-also"></a>См. также:

[**Иаженткоммандсекс:: FontSize**](iagentcommandsex--getfontsize.md), [**Иаженткоммандсекс:: жетфонтнаме**](iagentcommandsex--getfontname.md), [**иаженткоммандсекс:: сетфонтнаме**](iagentcommandsex--setfontname.md)


 

 