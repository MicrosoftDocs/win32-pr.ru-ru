---
description: Общие сведения о платформе текстовых служб для планшетных ПК.
ms.assetid: f77fe77a-8625-47c5-bfc7-b473c8e8a8c6
title: Платформа текстовых служб (планшетный ПК)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25eb3e635ae7394502ed203cb9ea31e115dc09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684510"
---
# <a name="text-services-framework-tablet-pc"></a>Платформа текстовых служб (планшетный ПК)

Если [Платформа текстовых служб (TSF)](../tsf/text-services-framework.md) включена для элемента управления с присоединенным объектом [Пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) , объект пенинпутпанел может вставлять текст напрямую. Если элемент управления не поддерживает платформу текстовых служб (TSF), то объект Пенинпутпанел должен использовать [функцию SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) для вставки текста.

Возможность вставки текста напрямую очень важна для тех, кто помещает знаки восточно-азиатских языков, где использование [функции SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) может привести к неправильным символам.

TSF предоставляет интерфейс для исправления ошибок распознавания, позволяющий конечному пользователю исправлять, переписывать или даже диктовать нужный текст.

TSF включается путем вызова метода [енаблетсф](/previous-versions/ms569656(v=vs.100)) с параметром *Enable* , установленным в **значение true**.

\[C\#\]


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



Объект [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) , присоединенный к элементу управления [InkEdit](/previous-versions/ms552265(v=vs.100)) , обеспечивает надежный пользовательский интерфейс, так как InkEdit поддерживает TSF. Однако обязательно задайте для свойства [инкмоде](/previous-versions/ms835850(v=msdn.10)) значение [Microsoft. Ink. инкмоде. Ink](/previous-versions/ms827399(v=msdn.10)) в элементе управления InkEdit, как указано в разделе [рекомендации](best-practices.md) .

В примере [пенинпутпанел](peninputpanel-sample.md) приведен пример включения TSF.

## <a name="related-topics"></a>См. также

<dl> <dt>

[инфраструктуры текстовых служб (TSF)](../tsf/text-services-framework.md)
</dt> </dl>

 

 
