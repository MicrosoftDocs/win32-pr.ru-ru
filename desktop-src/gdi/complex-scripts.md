---
description: Хотя функции, обсуждаемые в предыдущей работе, хорошо работают на многих языках, они могут не работать с потребностями сложных наборов символов.
ms.assetid: a60b50c8-13e8-4c61-989f-187bb67cf929
title: Сложные наборы символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149aa1d9a6f5caf78fec5227f25aa30146fc273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898450"
---
# <a name="complex-scripts"></a>Сложные наборы символов

Хотя функции, обсуждаемые в предыдущей работе, хорошо работают на многих языках, они могут не работать с потребностями сложных наборов символов. *Сложные наборы символов* — это языки, печатные формы которых не отображаются простым образом. Например, сложный скрипт может допускать двунаправленную отрисовку, контекстуальное формирование глифов или присоединяемых символов. Из-за этих особых требований Управление выводом текста должно быть очень гибким.

Функции, отображающие текстовые [**тексты**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**таббедтекстаут**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)и [**жеттекстекстентекспоинт**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) , были расширены для поддержки сложных наборов символов. Как правило, эта поддержка прозрачна для приложения. Однако приложения должны сохранять символы в буфере и отображать целую строку текста за один раз, чтобы модули, использующие сложные скрипты, могли использовать контекст для правильного упорядочения и создания глифов. Кроме того, поскольку Ширина глифа может зависеть от контекста, приложения должны использовать [**жеттекстекстентекспоинт**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) , чтобы определить длину строки, а не использовать кэшированную ширину символов.

Кроме того, в сложных приложениях, поддерживающих сценарии, следует рассмотреть возможность добавления поддержки для чтения справа налево и выравнивания по правому краю для своих приложений. Можно переключать порядок чтения или выравнивание между левым и правым кодом, используя следующий код:


```C++
// Save lAlign (this example uses static variables) 
static LONG lAlign = TA_LEFT;

// When user toggles alignment (assuming TA_CENTER is not supported). 

lAlign = TA_RIGHT;

// When the user toggles reading order. 

lAlign = TA_RTLREADING;

// Before calling ExtTextOut, for example, when processing WM_PAINT  

SetTextAlign (hDc, lAlign);
```



Чтобы одновременно включить оба атрибута, выполните следующую инструкцию, а затем вызовите [**сеттексталигн**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) и [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), как показано выше:


```C++
lAlign = TA_RIGHT^TA_RTLREADING;  //pre-inline !
```



Также можно обрабатывать сложные сценарии с помощью Uniscribe. Uniscribe — это набор функций, которые обеспечивают хорошее управление сложными скриптами. Дополнительные сведения см. в разделе [Uniscribe](../intl/uniscribe.md) и [обработка сложных наборов символов](../intl/processing-complex-scripts.md).

 

 
