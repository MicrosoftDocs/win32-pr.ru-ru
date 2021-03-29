---
title: Форматирование текста в элементах управления Rich Edit
description: Приложение может отправить сообщения в элемент управления Rich Edit, чтобы форматировать символы и абзацы и получать сведения о форматировании.
ms.assetid: 19A4F0D1-88C5-407D-A70F-CB486DAD352E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246c6309dec94538f47ed9ca7e464f1d6d17f240
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "103789361"
---
# <a name="how-to-format-text-in-rich-edit-controls"></a><span data-ttu-id="57f18-103">Форматирование текста в элементах управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="57f18-103">How to Format Text in Rich Edit Controls</span></span>

<span data-ttu-id="57f18-104">Приложение может отправить сообщения в элемент управления Rich Edit, чтобы форматировать символы и абзацы и получать сведения о форматировании.</span><span class="sxs-lookup"><span data-stu-id="57f18-104">An application can send messages to a rich edit control in order to format characters and paragraphs and retrieve formatting information.</span></span> <span data-ttu-id="57f18-105">Атрибуты форматирования абзаца включают выравнивание, табуляцию, отступы, нумерацию и простые таблицы.</span><span class="sxs-lookup"><span data-stu-id="57f18-105">Paragraph formatting attributes include alignment, tabs, indents, numbering, and simple tables.</span></span> <span data-ttu-id="57f18-106">Для символов можно указать имя шрифта, размер, цвет и эффекты, такие как полужирный, курсив и защищенный.</span><span class="sxs-lookup"><span data-stu-id="57f18-106">For characters, you can specify font name, size, color, and effects such as bold, italic, and protected.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="57f18-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="57f18-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="57f18-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="57f18-108">Technologies</span></span>

-   [<span data-ttu-id="57f18-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="57f18-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="57f18-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="57f18-110">Prerequisites</span></span>

-   <span data-ttu-id="57f18-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="57f18-111">C/C++</span></span>
-   <span data-ttu-id="57f18-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="57f18-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="57f18-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="57f18-113">Instructions</span></span>

### <a name="format-text-in-a-rich-edit-control"></a><span data-ttu-id="57f18-114">Форматирование текста в элементе управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="57f18-114">Format Text in a Rich Edit Control</span></span>

<span data-ttu-id="57f18-115">Форматирование абзаца можно применить с помощью сообщения [**EM \_ сетпараформат**](em-setparaformat.md) .</span><span class="sxs-lookup"><span data-stu-id="57f18-115">You can apply paragraph formatting by using the [**EM\_SETPARAFORMAT**](em-setparaformat.md) message.</span></span> <span data-ttu-id="57f18-116">Чтобы определить текущее форматирование абзаца для выделенного текста, используйте сообщение [**EM \_ жетпараформат**](em-getparaformat.md) .</span><span class="sxs-lookup"><span data-stu-id="57f18-116">To determine the current paragraph formatting for the selected text, use the [**EM\_GETPARAFORMAT**](em-getparaformat.md) message.</span></span> <span data-ttu-id="57f18-117">Для указания атрибутов форматирования абзаца в обоих сообщениях используется [**Формат**](/windows/desktop/api/Richedit/ns-richedit-paraformat) значения или структура [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) .</span><span class="sxs-lookup"><span data-stu-id="57f18-117">The [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) or [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure is used with both messages to specify paragraph formatting attributes.</span></span>

<span data-ttu-id="57f18-118">Форматирование символов можно применить с помощью сообщения [**EM \_ сетчарформат**](em-setcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="57f18-118">You can apply character formatting by using the [**EM\_SETCHARFORMAT**](em-setcharformat.md) message.</span></span> <span data-ttu-id="57f18-119">Чтобы определить текущее форматирование символов для выделенного текста, можно использовать сообщение [**EM \_ жетчарформат**](em-getcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="57f18-119">To determine the current character formatting for the selected text, you can use the [**EM\_GETCHARFORMAT**](em-getcharformat.md) message.</span></span> <span data-ttu-id="57f18-120">Структура [**чарформат**](/windows/win32/api/richedit/ns-richedit-charformata) или [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) используется вместе с обоими сообщениями для указания атрибутов символов.</span><span class="sxs-lookup"><span data-stu-id="57f18-120">The [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) or [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure is used with both messages to specify character attributes.</span></span>

<span data-ttu-id="57f18-121">Кроме того, можно использовать сообщения [**EM \_ Сетчарформат**](em-setcharformat.md) и [**EM \_ жетчарформат**](em-getcharformat.md) для установки и извлечения форматирования символов точки вставки, то есть форматирования, применяемого к вставленным символам.</span><span class="sxs-lookup"><span data-stu-id="57f18-121">You can also use [**EM\_SETCHARFORMAT**](em-setcharformat.md) and [**EM\_GETCHARFORMAT**](em-getcharformat.md) messages to set and retrieve the character formatting of the insertion point, which is the formatting that is applied to any subsequently inserted characters.</span></span> <span data-ttu-id="57f18-122">Например, если приложение устанавливает форматирование символов по умолчанию полужирным, а пользователь вводит символ, этот символ выделяется полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="57f18-122">For example, if an application sets the default character formatting to bold and the user then types a character, that character is bold.</span></span>

<span data-ttu-id="57f18-123">Форматирование символов точки вставки применяется ко вновь вставленному тексту только в том случае, если текущий выделенный фрагмент пуст (если текущий выделенный фрагмент является точкой вставки).</span><span class="sxs-lookup"><span data-stu-id="57f18-123">The character formatting of the insertion point is applied to newly inserted text only if the current selection is empty (if the current selection is an insertion point).</span></span> <span data-ttu-id="57f18-124">В противном случае новый текст предполагает форматирование символов текста, который он заменяет.</span><span class="sxs-lookup"><span data-stu-id="57f18-124">Otherwise, the new text assumes the character formatting of the text it replaces.</span></span> <span data-ttu-id="57f18-125">При изменении выбора форматирование символов по умолчанию изменяется в соответствии с первым символом в новом выделенном фрагменте.</span><span class="sxs-lookup"><span data-stu-id="57f18-125">If the selection changes, the default character formatting changes to match the first character in the new selection.</span></span>

<span data-ttu-id="57f18-126">Защищенный символ уникален в том, что он не изменяет внешний вид текста.</span><span class="sxs-lookup"><span data-stu-id="57f18-126">The protected character effect is unique in that it does not change the appearance of text.</span></span> <span data-ttu-id="57f18-127">Если пользователь пытается изменить защищенный текст, элемент управления Rich Edit (Правка) отправляет родительскому окну код уведомления, [ \_ защищенный коротким](en-protected.md) кодом, позволяя родительскому окну разрешать или запрещать изменение.</span><span class="sxs-lookup"><span data-stu-id="57f18-127">If the user attempts to modify protected text, a rich edit control sends its parent window an [EN\_PROTECTED](en-protected.md) notification code, allowing the parent window to allow or prevent the change.</span></span> <span data-ttu-id="57f18-128">Чтобы получить этот код уведомления, необходимо включить его с помощью сообщения [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="57f18-128">To receive this notification code, you must enable it by using the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="57f18-129">Цвет переднего плана всегда является символьным атрибутом.</span><span class="sxs-lookup"><span data-stu-id="57f18-129">Foreground color is always a character attribute.</span></span> <span data-ttu-id="57f18-130">В Microsoft Rich Edit 1,0 цвет фона — это только свойство элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="57f18-130">In Microsoft Rich Edit 1.0, background color is only a property of the rich edit control.</span></span> <span data-ttu-id="57f18-131">Чтобы задать цвет фона по умолчанию, используйте сообщение [**EM \_ сетбкгндколор**](em-setbkgndcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="57f18-131">To set the default background color, use the [**EM\_SETBKGNDCOLOR**](em-setbkgndcolor.md) message.</span></span> <span data-ttu-id="57f18-132">Обратите внимание, что Расширенное редактирование не поддерживает сообщение [**WM \_ ктлколоредит**](wm-ctlcoloredit.md) .</span><span class="sxs-lookup"><span data-stu-id="57f18-132">Note that Rich Edit does not support the [**WM\_CTLCOLOREDIT**](wm-ctlcoloredit.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57f18-133">См. также</span><span class="sxs-lookup"><span data-stu-id="57f18-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57f18-134">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="57f18-134">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="57f18-135">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="57f18-135">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




