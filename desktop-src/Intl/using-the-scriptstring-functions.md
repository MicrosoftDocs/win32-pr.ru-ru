---
description: Для приложения, которое работает с неформатированным текстом, Uniscribe предоставляет \* функции скриптстринг.
ms.assetid: bfbba5df-ce06-4012-a7b1-55d8ea580942
title: Использование функций Скриптстринг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a2df5e7515bd605ad48cc7a246941e9b6f08f2
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104070814"
---
# <a name="using-the-scriptstring-functions"></a><span data-ttu-id="7e365-103">Использование функций Скриптстринг</span><span class="sxs-lookup"><span data-stu-id="7e365-103">Using the ScriptString Functions</span></span>

<span data-ttu-id="7e365-104">Для приложения, которое работает с неформатированным текстом, Uniscribe предоставляет функции **скриптстринг \*** .</span><span class="sxs-lookup"><span data-stu-id="7e365-104">For an application dealing with unformatted text, Uniscribe provides the **ScriptString\*** functions.</span></span> <span data-ttu-id="7e365-105">Эти функции похожи на [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)и [**жеттекстекстент**](/cpp/mfc/reference/cdc-class#gettextextent), но они обеспечивают полную поддержку сложных скриптов, включая размещение курсора.</span><span class="sxs-lookup"><span data-stu-id="7e365-105">These functions are similar to [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext), and [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent), but they provide full complex script support, including caret placement.</span></span> <span data-ttu-id="7e365-106">Эти функции похожи на другие функции Uniscribe, но адаптированы к более простым требованиям обработки обычного текста.</span><span class="sxs-lookup"><span data-stu-id="7e365-106">These functions are similar to the other Uniscribe functions, but are tailored to the simpler requirements of plain text processing.</span></span>

<span data-ttu-id="7e365-107">В следующей таблице описаны функции **скриптстринг \*** и любые аналоги в других функциях Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="7e365-107">The following table details the **ScriptString\*** functions and any counterparts in the other Uniscribe functions.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7e365-108">Функция</span><span class="sxs-lookup"><span data-stu-id="7e365-108">Function</span></span></th>
<th><span data-ttu-id="7e365-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7e365-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e365-110"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>скриптстринганалисе</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-110"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></span></span></td>
<td><span data-ttu-id="7e365-111">Анализирует обычный текст.</span><span class="sxs-lookup"><span data-stu-id="7e365-111">Analyzes plain text.</span></span> <span data-ttu-id="7e365-112">Эта функция соответствует следующим функциям:</span><span class="sxs-lookup"><span data-stu-id="7e365-112">This function corresponds to the following functions:</span></span><br/> <dl><span data-ttu-id="7e365-113"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>скриптитемизе</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-113"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a></span></span><br /><span data-ttu-id="7e365-114">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>скриптшапе</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-114">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a></span></span><br /><span data-ttu-id="7e365-115">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>скриптплаце</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-115">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a></span></span><br /><span data-ttu-id="7e365-116">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>скриптбреак</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-116">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a></span></span><br /><span data-ttu-id="7e365-117">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>скриптжеткмап</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-117">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a></span></span><br /><span data-ttu-id="7e365-118">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>скриптжустифи</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-118">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a></span></span><br /><span data-ttu-id="7e365-119">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>скриптлайаут</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-119">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e365-120"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>скриптстрингкптокс</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-120"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></span></span></td>
<td><span data-ttu-id="7e365-121">Получает координату x для позиции символа.</span><span class="sxs-lookup"><span data-stu-id="7e365-121">Retrieves the x coordinate for a character position.</span></span> <span data-ttu-id="7e365-122">Эта функция соответствует <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>скрипткптокс</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7e365-122">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e365-123"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>скриптстрингфри</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-123"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></span></span></td>
<td><span data-ttu-id="7e365-124">Освобождает структуру <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7e365-124">Frees a <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e365-125"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>скриптстрингжетлогикалвидсс</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-125"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></span></span></td>
<td><span data-ttu-id="7e365-126">Преобразует визуальные значения ширины в логические.</span><span class="sxs-lookup"><span data-stu-id="7e365-126">Converts visual widths to logical widths.</span></span> <span data-ttu-id="7e365-127">Эта функция соответствует <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>скриптжетлогикалвидсс</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7e365-127">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e365-128"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>скриптстрингжетордер</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-128"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></span></span></td>
<td><span data-ttu-id="7e365-129">Сопоставляет позиции глифов символов аналогичным образом для <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">жетчарактерплацемент</a>, только для устаревшего использования.</span><span class="sxs-lookup"><span data-stu-id="7e365-129">Maps character glyph positions in a similar way to <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, for legacy use only.</span></span> <span data-ttu-id="7e365-130">Эта функция плохо работает с скриптами, которые создают более одного глифа для каждой кодовой точки.</span><span class="sxs-lookup"><span data-stu-id="7e365-130">This function does not work well with scripts that generate more than one glyph per code point.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e365-131"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>скриптстрингаут</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-131"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></span></span></td>
<td><span data-ttu-id="7e365-132">Отображает обычный текст.</span><span class="sxs-lookup"><span data-stu-id="7e365-132">Displays plain text.</span></span> <span data-ttu-id="7e365-133">Эта функция соответствует <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>скрипттекстаут</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7e365-133">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e365-134"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-134"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></span></span></td>
<td><span data-ttu-id="7e365-135">Возвращает указатель на длину обрезанной простой текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="7e365-135">Returns a pointer to the length of a clipped plain text string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e365-136"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-136"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></span></span></td>
<td><span data-ttu-id="7e365-137">Возвращает указатель на буфер логических атрибутов для проанализированной простой текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="7e365-137">Returns a pointer to the logical attributes buffer for an analyzed plain text string.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e365-138"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-138"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></span></span></td>
<td><span data-ttu-id="7e365-139">Возвращает указатель на размер (ширину и высоту) для проанализированной простой текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="7e365-139">Returns a pointer to the size (width and height) for an analyzed plain text string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e365-140"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>скриптстрингвалидате</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-140"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></span></span></td>
<td><span data-ttu-id="7e365-141">Определяет последовательности кодовых точек, недопустимые в данном скрипте.</span><span class="sxs-lookup"><span data-stu-id="7e365-141">Identifies code point sequences not valid in the given script.</span></span> <span data-ttu-id="7e365-142">Эта функция отличается от <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>скриптжеткмап</strong></a>, которая идентифицирует кодовые точки, отсутствующие в шрифте.</span><span class="sxs-lookup"><span data-stu-id="7e365-142">This function is different from <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>, which identifies code points not present in a font.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e365-143"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>скриптстрингкстокп</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e365-143"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></span></span></td>
<td><span data-ttu-id="7e365-144">Преобразует координату x в символьную точку.</span><span class="sxs-lookup"><span data-stu-id="7e365-144">Converts an x coordinate to a character position.</span></span> <span data-ttu-id="7e365-145">Эта функция соответствует <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>скрипткстокп</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7e365-145">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7e365-146">Чтобы отобразить только обычный текст без каких бы то ни было изменений, приложение должно вызвать [**скриптстринганалисе**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**скриптстрингаут**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout), а затем [**скриптстрингфри**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree).</span><span class="sxs-lookup"><span data-stu-id="7e365-146">To only display plain text without any modifications, an application should call [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout), and then [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree).</span></span> <span data-ttu-id="7e365-147">Другие функции используются для изменения обычного текста перед отображением.</span><span class="sxs-lookup"><span data-stu-id="7e365-147">The other functions are used to modify the plain text before display.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e365-148">См. также</span><span class="sxs-lookup"><span data-stu-id="7e365-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e365-149">Использование Uniscribe</span><span class="sxs-lookup"><span data-stu-id="7e365-149">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 
