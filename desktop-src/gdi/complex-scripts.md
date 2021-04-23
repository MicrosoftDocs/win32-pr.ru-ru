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
# <a name="complex-scripts"></a><span data-ttu-id="3d2ad-103">Сложные наборы символов</span><span class="sxs-lookup"><span data-stu-id="3d2ad-103">Complex Scripts</span></span>

<span data-ttu-id="3d2ad-104">Хотя функции, обсуждаемые в предыдущей работе, хорошо работают на многих языках, они могут не работать с потребностями сложных наборов символов.</span><span class="sxs-lookup"><span data-stu-id="3d2ad-104">While the functions discussed in the preceding work well for many languages, they may not deal with the needs of complex scripts.</span></span> <span data-ttu-id="3d2ad-105">*Сложные наборы символов* — это языки, печатные формы которых не отображаются простым образом.</span><span class="sxs-lookup"><span data-stu-id="3d2ad-105">*Complex scripts* are languages whose printed form is not rendered in a simple way.</span></span> <span data-ttu-id="3d2ad-106">Например, сложный скрипт может допускать двунаправленную отрисовку, контекстуальное формирование глифов или присоединяемых символов.</span><span class="sxs-lookup"><span data-stu-id="3d2ad-106">For example, a complex script may allow bidirectional rendering, contextual shaping of glyphs, or combining characters.</span></span> <span data-ttu-id="3d2ad-107">Из-за этих особых требований Управление выводом текста должно быть очень гибким.</span><span class="sxs-lookup"><span data-stu-id="3d2ad-107">Due to these special requirements, the control of text output must be very flexible.</span></span>

<span data-ttu-id="3d2ad-108">Функции, отображающие текстовые [**тексты**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**таббедтекстаут**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)и [**жеттекстекстентекспоинт**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) , были расширены для поддержки сложных наборов символов.</span><span class="sxs-lookup"><span data-stu-id="3d2ad-108">Functions that display text [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext), and [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) have been extended to support complex scripts.</span></span> <span data-ttu-id="3d2ad-109">Как правило, эта поддержка прозрачна для приложения.</span><span class="sxs-lookup"><span data-stu-id="3d2ad-109">In general, this support is transparent to the application.</span></span> <span data-ttu-id="3d2ad-110">Однако приложения должны сохранять символы в буфере и отображать целую строку текста за один раз, чтобы модули, использующие сложные скрипты, могли использовать контекст для правильного упорядочения и создания глифов.</span><span class="sxs-lookup"><span data-stu-id="3d2ad-110">However, applications should save characters in a buffer and display a whole line of text at one time, so that the complex script shaping modules can use context to reorder and generate glyphs correctly.</span></span> <span data-ttu-id="3d2ad-111">Кроме того, поскольку Ширина глифа может зависеть от контекста, приложения должны использовать [**жеттекстекстентекспоинт**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) , чтобы определить длину строки, а не использовать кэшированную ширину символов.</span><span class="sxs-lookup"><span data-stu-id="3d2ad-111">In addition, because the width of a glyph can vary by context, applications should use [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) to determine line length rather than using cached character widths.</span></span>

<span data-ttu-id="3d2ad-112">Кроме того, в сложных приложениях, поддерживающих сценарии, следует рассмотреть возможность добавления поддержки для чтения справа налево и выравнивания по правому краю для своих приложений.</span><span class="sxs-lookup"><span data-stu-id="3d2ad-112">In addition, complex script-aware applications should consider adding support for right-to-left reading order and right alignment to their applications.</span></span> <span data-ttu-id="3d2ad-113">Можно переключать порядок чтения или выравнивание между левым и правым кодом, используя следующий код:</span><span class="sxs-lookup"><span data-stu-id="3d2ad-113">You can toggle the reading order or alignment between left and right with the following code:</span></span>


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



<span data-ttu-id="3d2ad-114">Чтобы одновременно включить оба атрибута, выполните следующую инструкцию, а затем вызовите [**сеттексталигн**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) и [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), как показано выше:</span><span class="sxs-lookup"><span data-stu-id="3d2ad-114">To toggle both attributes at once, execute the following statement and then call [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) and [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), as shown previously:</span></span>


```C++
lAlign = TA_RIGHT^TA_RTLREADING;  //pre-inline !
```



<span data-ttu-id="3d2ad-115">Также можно обрабатывать сложные сценарии с помощью Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="3d2ad-115">You can also process complex scripts with Uniscribe.</span></span> <span data-ttu-id="3d2ad-116">Uniscribe — это набор функций, которые обеспечивают хорошее управление сложными скриптами.</span><span class="sxs-lookup"><span data-stu-id="3d2ad-116">Uniscribe is a set of functions that allow a fine degree of control for complex scripts.</span></span> <span data-ttu-id="3d2ad-117">Дополнительные сведения см. в разделе [Uniscribe](../intl/uniscribe.md) и [обработка сложных наборов символов](../intl/processing-complex-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="3d2ad-117">For more information, see [Uniscribe](../intl/uniscribe.md) and [Processing Complex Scripts](../intl/processing-complex-scripts.md).</span></span>

 

 
