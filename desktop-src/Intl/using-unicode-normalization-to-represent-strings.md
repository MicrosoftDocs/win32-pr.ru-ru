---
description: Приложения могут использовать Юникод для представления строк в нескольких формах.
ms.assetid: 027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35
title: Использование нормализации Юникода для представления строк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad452db3bc20518320afcf77e5f6483e010cd144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913691"
---
# <a name="using-unicode-normalization-to-represent-strings"></a><span data-ttu-id="8736d-103">Использование нормализации Юникода для представления строк</span><span class="sxs-lookup"><span data-stu-id="8736d-103">Using Unicode Normalization to Represent Strings</span></span>

<span data-ttu-id="8736d-104">Приложения могут использовать Юникод для представления строк в нескольких формах.</span><span class="sxs-lookup"><span data-stu-id="8736d-104">Applications can use Unicode to represent strings in multiple forms.</span></span> <span data-ttu-id="8736d-105">По мере того, как принятие Юникода увеличилось, особенно через Интернет, потребность в возникли сомнения устраняет ненужные различия в строках Юникода.</span><span class="sxs-lookup"><span data-stu-id="8736d-105">As Unicode acceptance has grown, especially via the Internet, the need has arisen to eliminate non-essential differences in Unicode strings.</span></span> <span data-ttu-id="8736d-106">Несколько представлений для сочетания символов усложняют программное обеспечение, например, когда веб-сервер отвечает на запрос страницы или компоновщик ищет определенный идентификатор в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="8736d-106">Multiple representations for a combination of characters complicate software, for example, when a Web server responds to a page request or a linker seeks a particular identifier in a library.</span></span>

> [!Caution]  
> <span data-ttu-id="8736d-107">Различные строки в Юникоде могут показаться визуально идентичными, что вызывает проблемы безопасности.</span><span class="sxs-lookup"><span data-stu-id="8736d-107">Different Unicode strings can appear to be visually identical, raising security concerns.</span></span> <span data-ttu-id="8736d-108">Дополнительные сведения см. в разделе [вопросы безопасности: международные функции](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="8736d-108">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

<span data-ttu-id="8736d-109">В ответ на это требование Консорциум Unicode определил процесс, называемый «нормализацией», который создает одно двоичное представление для любого из эквивалентных двоичных представлений символа.</span><span class="sxs-lookup"><span data-stu-id="8736d-109">In response to this requirement, the Unicode Consortium has defined a process called "normalization," which produces one binary representation for any of the equivalent binary representations of a character.</span></span> <span data-ttu-id="8736d-110">После нормализации две строки эквивалентны только в том случае, если они имеют идентичные двоичные представления.</span><span class="sxs-lookup"><span data-stu-id="8736d-110">Once normalized, two strings are equivalent if and only if they have identical binary representations.</span></span> <span data-ttu-id="8736d-111">Нормализация устраняет некоторые различия, но сохраняет регистр.</span><span class="sxs-lookup"><span data-stu-id="8736d-111">The normalization eliminates some differences but preserves case.</span></span>

<span data-ttu-id="8736d-112">Чтобы использовать нормализацию Юникода, приложение может вызывать функции [**нормализестринг**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) и [**иснормализедстринг**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) для изменения порядка строк АКККОРДИНГ в Unicode 4,0 TR \# 15.</span><span class="sxs-lookup"><span data-stu-id="8736d-112">To use Unicode normalization, an application can call the [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) and [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) functions for rearrangement of strings acccording to Unicode 4.0 TR\#15.</span></span> <span data-ttu-id="8736d-113">Нормализация может помочь повысить безопасность за счет сокращения числа альтернативных строковых представлений, имеющих одинаковые лингвистические значения.</span><span class="sxs-lookup"><span data-stu-id="8736d-113">Normalization can help improve security by reducing alternate string representations that have the same linguistic meaning.</span></span> <span data-ttu-id="8736d-114">Однако помните, что нормализация не может полностью исключить альтернативные представления.</span><span class="sxs-lookup"><span data-stu-id="8736d-114">Remember, however, that normalization cannot eliminate alternate representations entirely.</span></span>

<span data-ttu-id="8736d-115">Подробное описание стандартов Юникода для нормализации см. в [стандартном приложении Юникода \# 15: формы нормализации Юникода](https://www.unicode.org/reports/tr15) (уакс \# 15).</span><span class="sxs-lookup"><span data-stu-id="8736d-115">For a detailed description of the Unicode standards for normalization, refer to [Unicode Standard Annex \#15: Unicode Normalization Forms](https://www.unicode.org/reports/tr15) (UAX \#15).</span></span>

> [!Caution]  
> <span data-ttu-id="8736d-116">Поскольку нормализация может изменить форму строки, механизмы безопасности или алгоритмы проверки символов, как правило, должны быть реализованы после нормализации.</span><span class="sxs-lookup"><span data-stu-id="8736d-116">Because normalization can change the form of a string, security mechanisms or character validation algorithms should usually be implemented after normalization.</span></span> <span data-ttu-id="8736d-117">Дополнительные сведения см. в разделе [вопросы безопасности: международные функции](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="8736d-117">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="provide-multiple-representations-of-the-same-string"></a><span data-ttu-id="8736d-118">Предоставление нескольких представлений одной и той же строки</span><span class="sxs-lookup"><span data-stu-id="8736d-118">Provide Multiple Representations of the Same String</span></span>

<span data-ttu-id="8736d-119">Во многих случаях в Юникоде разрешено несколько представлений, то есть одной и той же строки, лингвистических.</span><span class="sxs-lookup"><span data-stu-id="8736d-119">In many cases, Unicode allows multiple representations of what is, linguistically, the same string.</span></span> <span data-ttu-id="8736d-120">Пример:</span><span class="sxs-lookup"><span data-stu-id="8736d-120">For example:</span></span>

-   <span data-ttu-id="8736d-121">Заглавная буква A с диересис (умляут) может быть представлена одной кодовой точкой Юникода "Ä" (U + 00C4) или сочетанием прописной буквы A и сочетанием Диересис ("A" + "ё", то есть U + 0041 U + 0308).</span><span class="sxs-lookup"><span data-stu-id="8736d-121">Capital A with dieresis (umlaut) can be represented either as a single Unicode code point "Ä" (U+00C4) or the combination of Capital A and the combining Dieresis character ("A" + "¨", that is, U+0041 U+0308).</span></span> <span data-ttu-id="8736d-122">Аналогичные рекомендации применяются ко многим другим символам с диакритическими знаками.</span><span class="sxs-lookup"><span data-stu-id="8736d-122">Similar considerations apply for many other characters with diacritic marks.</span></span>
-   <span data-ttu-id="8736d-123">Заглавная буква A может быть представлена обычным способом (прописная буква A, U + 0041) или по ширине прописной буквы A (U + FF21).</span><span class="sxs-lookup"><span data-stu-id="8736d-123">Capital A itself can be represented either in the usual manner (Latin Capital Letter A, U+0041) or by Fullwidth Latin Capital Letter A (U+FF21).</span></span> <span data-ttu-id="8736d-124">Аналогичные рекомендации применяются для других простых латинских букв (как в верхнем, так и в нижнем регистре) и для символов катакана, используемых для написания японского языка.</span><span class="sxs-lookup"><span data-stu-id="8736d-124">Similar considerations apply for the other simple Latin letters (both uppercase and lowercase) and for the katakana characters used in writing Japanese.</span></span>
-   <span data-ttu-id="8736d-125">Строка «Fi» может быть представлена либо символами «f», «i» (U + 0066 U + 0069), либо лигатурой «Fi» (U + FB01).</span><span class="sxs-lookup"><span data-stu-id="8736d-125">The string "fi" can be represented either by the characters "f" and "i" (U+0066 U+0069) or by the ligature "ﬁ" (U+FB01).</span></span> <span data-ttu-id="8736d-126">Аналогичные соображения относятся ко многим другим сочетаниям символов, для которых Юникод определяет лигатуры.</span><span class="sxs-lookup"><span data-stu-id="8736d-126">Similar considerations apply for many other combinations of characters for which Unicode defines ligatures.</span></span>

## <a name="use-the-four-defined-normalization-forms"></a><span data-ttu-id="8736d-127">Использовать четыре определенные формы нормализации</span><span class="sxs-lookup"><span data-stu-id="8736d-127">Use the Four Defined Normalization Forms</span></span>

<span data-ttu-id="8736d-128">Приложения могут выполнять нормализацию Юникода с помощью нескольких алгоритмов, называемых «формами нормализации», которые подчиняются различным правилам.</span><span class="sxs-lookup"><span data-stu-id="8736d-128">Your applications can perform Unicode normalization using several algorithms, called "normalization forms," that obey different rules.</span></span> <span data-ttu-id="8736d-129">Консорциум Unicode определил четыре формы нормализации: NFC (форма C), NFD (форма D), НФКК (форма KC) и НФКД (форма KD).</span><span class="sxs-lookup"><span data-stu-id="8736d-129">The Unicode Consortium has defined four normalization forms: NFC (form C), NFD (form D), NFKC (form KC), and NFKD (form KD).</span></span> <span data-ttu-id="8736d-130">Каждая форма устраняет некоторые различия, но сохраняет регистр.</span><span class="sxs-lookup"><span data-stu-id="8736d-130">Each form eliminates some differences but preserves case.</span></span> <span data-ttu-id="8736d-131">Win32 и платформа .NET Framework поддерживают все четыре формы нормализации.</span><span class="sxs-lookup"><span data-stu-id="8736d-131">Win32 and the .NET Framework support all four normalization forms.</span></span>

<span data-ttu-id="8736d-132">[**\_ Форма нормы**](/windows/desktop/api/Winnls/ne-winnls-norm_form) типа перечисления NLS поддерживает четыре стандартные формы нормализации Юникода.</span><span class="sxs-lookup"><span data-stu-id="8736d-132">The NLS enumeration type [**NORM\_FORM**](/windows/desktop/api/Winnls/ne-winnls-norm_form) supports the four standard Unicode normalization forms.</span></span> <span data-ttu-id="8736d-133">Формы C и D предоставляют канонические формы для строк.</span><span class="sxs-lookup"><span data-stu-id="8736d-133">Forms C and D provide canonical forms for strings.</span></span> <span data-ttu-id="8736d-134">Неканонические формы KC и KD обеспечивают дальнейшую совместимость и могут раскрывать определенные семантические эквивалентные, не очевидные в формах C и D. Однако они делают это за счет определенной потери информации, и обычно не следует использовать в качестве канонического способа хранения строк.</span><span class="sxs-lookup"><span data-stu-id="8736d-134">Non-canonical forms KC and KD provide further compatibility, and can reveal certain semantic equivalences that are not apparent in forms C and D. However, they do so at the expense of a certain loss of information, and generally should not be used as a canonical way to store strings.</span></span>

<span data-ttu-id="8736d-135">Из двух канонических форм форма C представляет собой «составную» форму, а форма «D» — это «разложенная» форма.</span><span class="sxs-lookup"><span data-stu-id="8736d-135">Of the two canonical forms, form C is a "composed" form and form D is a "decomposed" form.</span></span> <span data-ttu-id="8736d-136">Например, форма C использует одну кодовую точку Юникода «Ä» (U + 00C4), а форма D использует («A» + «ё»), то есть U + 0041 U + 0308).</span><span class="sxs-lookup"><span data-stu-id="8736d-136">For example, form C uses the single Unicode code point "Ä" (U+00C4), while form D uses ("A" + "¨", that is U+0041 U+0308).</span></span> <span data-ttu-id="8736d-137">Эти данные отображаются одинаково, так как "ё" (U + 0308) — это несамостоятельный символ.</span><span class="sxs-lookup"><span data-stu-id="8736d-137">These render identically, because "¨" (U+0308) is a combining character.</span></span> <span data-ttu-id="8736d-138">Форма D может использовать любое количество кодовых точек для представления одной кодовой точки, используемой формой C.</span><span class="sxs-lookup"><span data-stu-id="8736d-138">Form D can use any number of code points to represent a single code point used by form C.</span></span>

<span data-ttu-id="8736d-139">Если две строки идентичны в форме C или форме D, они идентичны в другой форме.</span><span class="sxs-lookup"><span data-stu-id="8736d-139">If two strings are identical in either form C or form D, they are identical in the other form.</span></span> <span data-ttu-id="8736d-140">Более того, при правильном отображении они отображают неразличимы друг от друга и от исходной ненормализованной строки.</span><span class="sxs-lookup"><span data-stu-id="8736d-140">Furthermore, when correctly rendered, they display indistinguishably from one another and from the original non-normalized string.</span></span>

<span data-ttu-id="8736d-141">После нормализации строки не могут быть постоянно возвращены в исходное представление.</span><span class="sxs-lookup"><span data-stu-id="8736d-141">Once normalized, strings cannot be consistently returned to their original representation.</span></span> <span data-ttu-id="8736d-142">Например, если строка с сочетанием составных и разделенных символьных представлений преобразуется в нормализованную форму, невозможно отменить нормализацию для исходной смешанной строки.</span><span class="sxs-lookup"><span data-stu-id="8736d-142">For example, if a string with a mixture of composed and decomposed character representations is converted to a normalized form, there is no way to un-normalize it to the original mixed string.</span></span> <span data-ttu-id="8736d-143">Таким образом, если приложению требуется исходное представление строки, оно должно хранить это представление явным образом.</span><span class="sxs-lookup"><span data-stu-id="8736d-143">Therefore, if an application requires the original representation of the string, it must store that representation explicitly.</span></span> <span data-ttu-id="8736d-144">Однако преобразование между двумя каноническими формами осуществляется с помощью обратимого преобразования.</span><span class="sxs-lookup"><span data-stu-id="8736d-144">However, converting between the two canonical forms is reversible.</span></span> <span data-ttu-id="8736d-145">Строка в формате C может быть преобразована в форму D, а затем обратно в форму C, а результат идентичен исходной строке в формате C.</span><span class="sxs-lookup"><span data-stu-id="8736d-145">A string in form C can be converted to form D and then back to form C, and the result is identical to the original form C string.</span></span>

<span data-ttu-id="8736d-146">Формы KC и KD похожи на формы C и D соответственно, но эти формы совместимости имеют дополнительные сопоставления совместимых символов с базовой формой каждого символа.</span><span class="sxs-lookup"><span data-stu-id="8736d-146">Forms KC and KD are similar to forms C and D, respectively, but these "compatibility forms" have additional mappings of compatible characters to the basic form of each character.</span></span> <span data-ttu-id="8736d-147">Такие сопоставления могут привести к потере незначительных символов.</span><span class="sxs-lookup"><span data-stu-id="8736d-147">Such mappings can cause minor character variations to be lost.</span></span> <span data-ttu-id="8736d-148">Они объединяют определенные символы, которые являются визуально отличающимися.</span><span class="sxs-lookup"><span data-stu-id="8736d-148">They combine certain characters that are visually distinct.</span></span> <span data-ttu-id="8736d-149">Например, они объединяют символы полной и половинной ширины с одним и тем же семантическим значением или разными формами того же арабского письма или лигатурой "Fi" (U + FB01) и парой символов "Fi" (U + 0066 U + 0069).</span><span class="sxs-lookup"><span data-stu-id="8736d-149">For example, they combine full-width and half-width characters with the same semantic meaning, or different forms of the same Arabic letter, or the ligature "ﬁ" (U+FB01) and the character pair "fi" (U+0066 U+0069).</span></span> <span data-ttu-id="8736d-150">Они также объединяют некоторые символы, которые иногда могут иметь другое семантическое значение, например цифру, записанную в виде надстрочного знака, в виде подстрочного или заключенного в круг.</span><span class="sxs-lookup"><span data-stu-id="8736d-150">They also combine some characters that might sometimes have a different semantic meaning, such as a digit written as a superscript, as a subscript, or enclosed in a circle.</span></span> <span data-ttu-id="8736d-151">Из-за этой потери информации Forms KC и KD обычно не следует использовать в качестве канонических форм строк, но они полезны для определенных приложений.</span><span class="sxs-lookup"><span data-stu-id="8736d-151">Because of this information loss, forms KC and KD generally should not be used as canonical forms of strings, but they are useful for certain applications.</span></span>

<span data-ttu-id="8736d-152">Форма KC является составной формой, а форма KD — разделенной формой.</span><span class="sxs-lookup"><span data-stu-id="8736d-152">Form KC is a composed form and form KD is a decomposed form.</span></span> <span data-ttu-id="8736d-153">Приложение может возвращаться между Forms KC и KD, но не существует согласованного способа перехода от формы KC или KD к исходной строке, даже если исходная строка находится в формате C или D.</span><span class="sxs-lookup"><span data-stu-id="8736d-153">The application can go back and forth between forms KC and KD, but there is no consistent way to go from form KC or KD back to the original string, even if the original string is in form C or D.</span></span>

<span data-ttu-id="8736d-154">Windows, приложения Майкрософт и платформа .NET Framework обычно создают символы в форме C, используя обычные методы ввода.</span><span class="sxs-lookup"><span data-stu-id="8736d-154">Windows, Microsoft applications, and the .NET Framework generally generate characters in form C using normal input methods.</span></span> <span data-ttu-id="8736d-155">Для большинства целей в Windows форма «C» является предпочтительной формой.</span><span class="sxs-lookup"><span data-stu-id="8736d-155">For most purposes on Windows, form C is the preferred form.</span></span> <span data-ttu-id="8736d-156">Например, символы в форме C создаются вводом с клавиатуры Windows.</span><span class="sxs-lookup"><span data-stu-id="8736d-156">For example, characters in form C are produced by Windows keyboard input.</span></span> <span data-ttu-id="8736d-157">Однако символы, импортированные из Интернета и других платформ, могут ввести другие формы нормализации в поток данных.</span><span class="sxs-lookup"><span data-stu-id="8736d-157">However, characters imported from the Web and other platforms can introduce other normalization forms into the data stream.</span></span>

<span data-ttu-id="8736d-158">Следующие примеры взяты из УАКС \# 15 и иллюстрируют различия между четырьмя формами нормализации.</span><span class="sxs-lookup"><span data-stu-id="8736d-158">The following examples are drawn from UAX \#15, and illustrate the differences among the four normalization forms.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8736d-159">До преобразования</span><span class="sxs-lookup"><span data-stu-id="8736d-159">Original</span></span></th>
<th><span data-ttu-id="8736d-160">Форма D</span><span class="sxs-lookup"><span data-stu-id="8736d-160">Form D</span></span></th>
<th><span data-ttu-id="8736d-161">Форма C</span><span class="sxs-lookup"><span data-stu-id="8736d-161">Form C</span></span></th>
<th><span data-ttu-id="8736d-162">Примечания</span><span class="sxs-lookup"><span data-stu-id="8736d-162">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8736d-163">&quot;äффин&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-163">&quot;Äffin&quot;</span></span></td>
<td><span data-ttu-id="8736d-164">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-164">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="8736d-165">&quot;äффин&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-165">&quot;Äffin&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="8736d-166">Ffi_ligature (U + FB03) не разлагаются, так как имеет сопоставление совместимости, а не каноническое сопоставление. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8736d-166">The ffi_ligature (U+FB03) is not decomposed, because it has a compatibility mapping, not a canonical mapping.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8736d-167">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-167">&quot;Ä\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="8736d-168">&quot;A\u0308\uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-168">&quot;A\u0308\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="8736d-169">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-169">&quot;Ä\uFB03n&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8736d-170">&quot;Генри IV&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-170">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="8736d-171">&quot;Генри IV&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-171">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="8736d-172">&quot;Генри IV&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-172">&quot;Henry IV&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="8736d-173">РИМСКИЕ цифры IV (U + 2163) не разлагаются. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8736d-173">The ROMAN NUMERAL IV (U+2163) is not decomposed.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8736d-174">&quot;Генри \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-174">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="8736d-175">&quot;Генри \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-175">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="8736d-176">&quot;Генри \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-176">&quot;Henry \u2163&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8736d-177">ga</span><span class="sxs-lookup"><span data-stu-id="8736d-177">ga</span></span></td>
<td><span data-ttu-id="8736d-178">Ка + 10</span><span class="sxs-lookup"><span data-stu-id="8736d-178">ka +ten</span></span></td>
<td><span data-ttu-id="8736d-179">ga</span><span class="sxs-lookup"><span data-stu-id="8736d-179">ga</span></span></td>
<td rowspan="5"><span data-ttu-id="8736d-180">Разные эквиваленты совместимости одного японского символа не являются одной и той же строкой в форме C. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8736d-180">Different compatibility equivalents of a single Japanese character do not result in the same string in form C.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8736d-181">Ка + 10</span><span class="sxs-lookup"><span data-stu-id="8736d-181">ka +ten</span></span></td>
<td><span data-ttu-id="8736d-182">Ка + 10</span><span class="sxs-lookup"><span data-stu-id="8736d-182">ka +ten</span></span></td>
<td><span data-ttu-id="8736d-183">ga</span><span class="sxs-lookup"><span data-stu-id="8736d-183">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8736d-184">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="8736d-184">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="8736d-185">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="8736d-185">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="8736d-186">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="8736d-186">hw_ka +hw_ten</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8736d-187">ка + hw_ten</span><span class="sxs-lookup"><span data-stu-id="8736d-187">ka +hw_ten</span></span></td>
<td><span data-ttu-id="8736d-188">ка + hw_ten</span><span class="sxs-lookup"><span data-stu-id="8736d-188">ka +hw_ten</span></span></td>
<td><span data-ttu-id="8736d-189">ка + hw_ten</span><span class="sxs-lookup"><span data-stu-id="8736d-189">ka +hw_ten</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8736d-190">hw_ka + 10</span><span class="sxs-lookup"><span data-stu-id="8736d-190">hw_ka +ten</span></span></td>
<td><span data-ttu-id="8736d-191">hw_ka + 10</span><span class="sxs-lookup"><span data-stu-id="8736d-191">hw_ka +ten</span></span></td>
<td><span data-ttu-id="8736d-192">hw_ka + 10</span><span class="sxs-lookup"><span data-stu-id="8736d-192">hw_ka +ten</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8736d-193">какс</span><span class="sxs-lookup"><span data-stu-id="8736d-193">kaks</span></span></td>
<td><span data-ttu-id="8736d-194">б <sub>i</sub> + + KS <sub>f</sub></span><span class="sxs-lookup"><span data-stu-id="8736d-194">k <sub>i</sub> + a ₘ + ks <sub>f</sub></span></span></td>
<td><span data-ttu-id="8736d-195">какс</span><span class="sxs-lookup"><span data-stu-id="8736d-195">kaks</span></span></td>
<td><span data-ttu-id="8736d-196">Слоги хангыль поддерживаются в нормализации.</span><span class="sxs-lookup"><span data-stu-id="8736d-196">Hangul syllables are maintained under normalization.</span></span><br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8736d-197">До преобразования</span><span class="sxs-lookup"><span data-stu-id="8736d-197">Original</span></span></th>
<th><span data-ttu-id="8736d-198">Форма KD</span><span class="sxs-lookup"><span data-stu-id="8736d-198">Form KD</span></span></th>
<th><span data-ttu-id="8736d-199">Форма KC</span><span class="sxs-lookup"><span data-stu-id="8736d-199">Form KC</span></span></th>
<th><span data-ttu-id="8736d-200">Примечания</span><span class="sxs-lookup"><span data-stu-id="8736d-200">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8736d-201">&quot;äффин&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-201">&quot;Äffin&quot;</span></span></td>
<td><span data-ttu-id="8736d-202">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-202">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="8736d-203">&quot;äффин&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-203">&quot;Äffin&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="8736d-204">Ffi_ligature (U + FB03) разлагаются в форме KC, но не в форме C. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8736d-204">The ffi_ligature (U+FB03) is decomposed in form KC, but not in form C.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8736d-205">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-205">&quot;Ä\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="8736d-206">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-206">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="8736d-207">&quot;äффин&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-207">&quot;Äffin&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8736d-208">&quot;Генри IV&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-208">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="8736d-209">&quot;Генри IV&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-209">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="8736d-210">&quot;Генри IV&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-210">&quot;Henry IV&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="8736d-211">Результирующие строки здесь идентичны в форме KC. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8736d-211">The resulting strings here are identical in form KC.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8736d-212">&quot;Генри \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-212">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="8736d-213">&quot;Генри IV&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-213">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="8736d-214">&quot;Генри IV&quot;</span><span class="sxs-lookup"><span data-stu-id="8736d-214">&quot;Henry IV&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8736d-215">ga</span><span class="sxs-lookup"><span data-stu-id="8736d-215">ga</span></span></td>
<td><span data-ttu-id="8736d-216">Ка + 10</span><span class="sxs-lookup"><span data-stu-id="8736d-216">ka +ten</span></span></td>
<td><span data-ttu-id="8736d-217">ga</span><span class="sxs-lookup"><span data-stu-id="8736d-217">ga</span></span></td>
<td rowspan="5"><span data-ttu-id="8736d-218">Разные эквиваленты совместимости одного японского символа в одной строке в формате KC. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8736d-218">Different compatibility equivalents of a single Japanese character result in the same string in form KC.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8736d-219">Ка + 10</span><span class="sxs-lookup"><span data-stu-id="8736d-219">ka +ten</span></span></td>
<td><span data-ttu-id="8736d-220">Ка + 10</span><span class="sxs-lookup"><span data-stu-id="8736d-220">ka +ten</span></span></td>
<td><span data-ttu-id="8736d-221">ga</span><span class="sxs-lookup"><span data-stu-id="8736d-221">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8736d-222">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="8736d-222">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="8736d-223">Ка + 10</span><span class="sxs-lookup"><span data-stu-id="8736d-223">ka +ten</span></span></td>
<td><span data-ttu-id="8736d-224">ga</span><span class="sxs-lookup"><span data-stu-id="8736d-224">ga</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8736d-225">ка + hw_ten</span><span class="sxs-lookup"><span data-stu-id="8736d-225">ka +hw_ten</span></span></td>
<td><span data-ttu-id="8736d-226">Ка + 10</span><span class="sxs-lookup"><span data-stu-id="8736d-226">ka +ten</span></span></td>
<td><span data-ttu-id="8736d-227">ga</span><span class="sxs-lookup"><span data-stu-id="8736d-227">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8736d-228">hw_ka + 10</span><span class="sxs-lookup"><span data-stu-id="8736d-228">hw_ka +ten</span></span></td>
<td><span data-ttu-id="8736d-229">Ка + 10</span><span class="sxs-lookup"><span data-stu-id="8736d-229">ka +ten</span></span></td>
<td><span data-ttu-id="8736d-230">ga</span><span class="sxs-lookup"><span data-stu-id="8736d-230">ga</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8736d-231">какс</span><span class="sxs-lookup"><span data-stu-id="8736d-231">kaks</span></span></td>
<td><span data-ttu-id="8736d-232">б <sub>i</sub> + + KS <sub>f</sub></span><span class="sxs-lookup"><span data-stu-id="8736d-232">k <sub>i</sub> + a ₘ + ks <sub>f</sub></span></span></td>
<td><span data-ttu-id="8736d-233">какс</span><span class="sxs-lookup"><span data-stu-id="8736d-233">kaks</span></span></td>
<td><span data-ttu-id="8736d-234">Слоги хангыль поддерживаются в нормализации.</span><span class="sxs-lookup"><span data-stu-id="8736d-234">Hangul syllables are maintained under normalization.</span></span> <span data-ttu-id="8736d-235">В более ранних версиях Юникода такие символы, как KS <sub>f</sub> , имеют сопоставление совместимости с k <sub>f</sub> + s <sub>f</sub>.</span><span class="sxs-lookup"><span data-stu-id="8736d-235">In earlier Unicode versions, jamo characters like ks <sub>f</sub> had compatibility mappings to k <sub>f</sub> + s <sub>f</sub>.</span></span> <span data-ttu-id="8736d-236">Эти сопоставления были удалены в Юникоде 2.1.9, чтобы обеспечить поддержку слогов хангыль.</span><span class="sxs-lookup"><span data-stu-id="8736d-236">These mappings were removed in Unicode 2.1.9 to ensure that Hangul syllables are maintained.</span></span><br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="8736d-237">Две приведенные выше таблицы имеют авторские права на © 1998-2006 Unicode, Inc. Все права защищены.</span><span class="sxs-lookup"><span data-stu-id="8736d-237">The two tables above have a copyright of © 1998-2006 Unicode, Inc. All Rights Reserved.</span></span>

 

## <a name="use-composed-forms-for-single-glyphs"></a><span data-ttu-id="8736d-238">Использование составных форм для одиночных глифов</span><span class="sxs-lookup"><span data-stu-id="8736d-238">Use Composed Forms for Single Glyphs</span></span>

<span data-ttu-id="8736d-239">Многие последовательности символов, соответствующие одному глифу, не состоят из составных форм.</span><span class="sxs-lookup"><span data-stu-id="8736d-239">Many character sequences that correspond to a single glyph do not have composed forms.</span></span> <span data-ttu-id="8736d-240">Даже при нормализации формы C один визуальный глиф или логический текстовый элемент может состоять из нескольких кодовых позиций Юникода.</span><span class="sxs-lookup"><span data-stu-id="8736d-240">Even when normalized by form C, a single visual glyph or logical text element can be composed of multiple Unicode code points.</span></span> <span data-ttu-id="8736d-241">Например, несколько символов, используемых в записи литовский, имеют двойные диакритические знаки, так как они содержат только разразделенные формы.</span><span class="sxs-lookup"><span data-stu-id="8736d-241">For example, several characters used in writing Lithuanian have double diacritics, as they have only decomposed forms.</span></span> <span data-ttu-id="8736d-242">Например, строчные буквы U с Макрон и тильда ("ū̃", U + 016b U + 0303, где первая кодовая точка — строчная буква U с Макрон, а вторая — сочетание острых знаков).</span><span class="sxs-lookup"><span data-stu-id="8736d-242">An example is lowercase U with macron and tilde ("ū̃", U+016b U+0303, where the first code point is a lowercase U with macron and the second is a combining acute accent).</span></span>

## <a name="example"></a><span data-ttu-id="8736d-243">Пример</span><span class="sxs-lookup"><span data-stu-id="8736d-243">Example</span></span>

<span data-ttu-id="8736d-244">Соответствующий пример можно найти в [примере NLS: нормализация Юникода](nls--unicode-normalization-sample.md).</span><span class="sxs-lookup"><span data-stu-id="8736d-244">A relevant example can be found in [NLS: Unicode Normalization Sample](nls--unicode-normalization-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8736d-245">См. также</span><span class="sxs-lookup"><span data-stu-id="8736d-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8736d-246">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="8736d-246">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="8736d-247">Вопросы безопасности: международные функции</span><span class="sxs-lookup"><span data-stu-id="8736d-247">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> <dt>

[<span data-ttu-id="8736d-248">**иснормализедстринг**</span><span class="sxs-lookup"><span data-stu-id="8736d-248">**IsNormalizedString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[<span data-ttu-id="8736d-249">**нормализестринг**</span><span class="sxs-lookup"><span data-stu-id="8736d-249">**NormalizeString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 




