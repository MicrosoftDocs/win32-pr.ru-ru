---
title: Грамматика
description: Инструкции HLSL создаются с использованием следующих правил для грамматики.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2346e1ca2302f80c796558b4aa2bbdce016d494
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532903"
---
# <a name="grammar"></a><span data-ttu-id="4c615-103">Грамматика</span><span class="sxs-lookup"><span data-stu-id="4c615-103">Grammar</span></span>

<span data-ttu-id="4c615-104">Инструкции HLSL создаются с использованием следующих правил для грамматики.</span><span class="sxs-lookup"><span data-stu-id="4c615-104">HLSL statements are constructed using the following rules for grammar.</span></span>

-   [<span data-ttu-id="4c615-105">Бель</span><span class="sxs-lookup"><span data-stu-id="4c615-105">Whitespace</span></span>](#whitespace)
-   [<span data-ttu-id="4c615-106">Числа с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="4c615-106">Floating point numbers</span></span>](#floating-point-numbers)
-   [<span data-ttu-id="4c615-107">Целые числа</span><span class="sxs-lookup"><span data-stu-id="4c615-107">Integer numbers</span></span>](#integer-numbers)
-   [<span data-ttu-id="4c615-108">Символы</span><span class="sxs-lookup"><span data-stu-id="4c615-108">Characters</span></span>](#characters)
-   [<span data-ttu-id="4c615-109">Строки</span><span class="sxs-lookup"><span data-stu-id="4c615-109">Strings</span></span>](#strings)
-   [<span data-ttu-id="4c615-110">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="4c615-110">Identifiers</span></span>](#identifiers)
-   [<span data-ttu-id="4c615-111">Операторы</span><span class="sxs-lookup"><span data-stu-id="4c615-111">Operators</span></span>](#operators)
-   [<span data-ttu-id="4c615-112">См. также</span><span class="sxs-lookup"><span data-stu-id="4c615-112">Related topics</span></span>](#related-topics)

## <a name="whitespace"></a><span data-ttu-id="4c615-113">Пробелы</span><span class="sxs-lookup"><span data-stu-id="4c615-113">Whitespace</span></span>

<span data-ttu-id="4c615-114">Следующие символы распознаются как пробелы.</span><span class="sxs-lookup"><span data-stu-id="4c615-114">The following characters are recognized as white space.</span></span>



|                            |
|----------------------------|
| <span data-ttu-id="4c615-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="4c615-115">SPACE</span></span>                      |
| <span data-ttu-id="4c615-116">TAB</span><span class="sxs-lookup"><span data-stu-id="4c615-116">TAB</span></span>                        |
| <span data-ttu-id="4c615-117">КОНЦА строки</span><span class="sxs-lookup"><span data-stu-id="4c615-117">EOL</span></span>                        |
| <span data-ttu-id="4c615-118">Комментарии в стиле C (/ \* \* /)</span><span class="sxs-lookup"><span data-stu-id="4c615-118">C style comments (/\* \*/)</span></span> |
| <span data-ttu-id="4c615-119">Комментарии в стиле C++ (//)</span><span class="sxs-lookup"><span data-stu-id="4c615-119">C++ style comments (//)</span></span>    |



 

## <a name="floating-point-numbers"></a><span data-ttu-id="4c615-120">Числа с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="4c615-120">Floating point numbers</span></span>

<span data-ttu-id="4c615-121">Числа с плавающей запятой представлены в HLSL следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4c615-121">Floating point numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="4c615-122">экспонента с плавающей запятой-часть (неявное) (неявное) (OPT)</span><span class="sxs-lookup"><span data-stu-id="4c615-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span></span>

    <span data-ttu-id="4c615-123">экспонента числа с плавающей запятой-часть (OPT)</span><span class="sxs-lookup"><span data-stu-id="4c615-123">digit-sequence exponent-part floating-suffix(opt)</span></span>

-   <span data-ttu-id="4c615-124">Дробная константа:</span><span class="sxs-lookup"><span data-stu-id="4c615-124">fractional-constant :</span></span>

    <span data-ttu-id="4c615-125">последовательность цифр (OPT).</span><span class="sxs-lookup"><span data-stu-id="4c615-125">digit-sequence(opt) .</span></span> <span data-ttu-id="4c615-126">последовательность цифр</span><span class="sxs-lookup"><span data-stu-id="4c615-126">digit-sequence</span></span>

    <span data-ttu-id="4c615-127">последовательность цифр.</span><span class="sxs-lookup"><span data-stu-id="4c615-127">digit-sequence .</span></span>

-   <span data-ttu-id="4c615-128">степень — часть:</span><span class="sxs-lookup"><span data-stu-id="4c615-128">exponent-part :</span></span>

    <span data-ttu-id="4c615-129">знак "e" (нежелательна) — последовательность цифр</span><span class="sxs-lookup"><span data-stu-id="4c615-129">e sign(opt) digit-sequence</span></span>

    <span data-ttu-id="4c615-130">Знак "E" (нежелательна) — последовательность цифр</span><span class="sxs-lookup"><span data-stu-id="4c615-130">E sign(opt) digit-sequence</span></span>

-   <span data-ttu-id="4c615-131">sign : один из указанных ниже знаков</span><span class="sxs-lookup"><span data-stu-id="4c615-131">sign : one of</span></span>

    \+ -

-   <span data-ttu-id="4c615-132">последовательность цифр:</span><span class="sxs-lookup"><span data-stu-id="4c615-132">digit-sequence :</span></span>

    <span data-ttu-id="4c615-133">цифровой-знак</span><span class="sxs-lookup"><span data-stu-id="4c615-133">digit</span></span>

    <span data-ttu-id="4c615-134">последовательность-цифр цифра</span><span class="sxs-lookup"><span data-stu-id="4c615-134">digit-sequence digit</span></span>

-   <span data-ttu-id="4c615-135">floating-suffix : одно из указанных ниже значений</span><span class="sxs-lookup"><span data-stu-id="4c615-135">floating-suffix : one of</span></span>

    <span data-ttu-id="4c615-136">h з f l L</span><span class="sxs-lookup"><span data-stu-id="4c615-136">h H f F l L</span></span>

    <span data-ttu-id="4c615-137">Используйте суффикс "L" для указания полного литерала с плавающей запятой 64-разрядной точности.</span><span class="sxs-lookup"><span data-stu-id="4c615-137">Use the “L” suffix to specify a full 64-bit precision floating-point literal.</span></span> <span data-ttu-id="4c615-138">Значение по умолчанию — 32-разрядный литерал с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4c615-138">A 32-bit float literal is the default.</span></span>

    <span data-ttu-id="4c615-139">Например, компилятор распознает следующее литеральное значение в виде литерала с плавающей запятой 32-разрядной точности и игнорирует младшие биты:</span><span class="sxs-lookup"><span data-stu-id="4c615-139">For example, the compiler recognizes the following literal value as a 32-bit precision floating-point literal and ignores the lower bits:</span></span>

    ```
    double x = -0.6473313946860445;
    ```

    

    <span data-ttu-id="4c615-140">Компилятор распознает следующее литеральное значение как литерал с плавающей запятой 64-разрядной точности:</span><span class="sxs-lookup"><span data-stu-id="4c615-140">The compiler recognizes the following literal value as a 64-bit precision floating-point literal:</span></span>

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a><span data-ttu-id="4c615-141">Целые числа</span><span class="sxs-lookup"><span data-stu-id="4c615-141">Integer numbers</span></span>

<span data-ttu-id="4c615-142">Целочисленные числа представлены в HLSL следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4c615-142">Integer numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="4c615-143">Integer-Константное целое число-суффикс (OPT)</span><span class="sxs-lookup"><span data-stu-id="4c615-143">integer-constant integer-suffix(opt)</span></span>
-   <span data-ttu-id="4c615-144">Integer — константа: один из</span><span class="sxs-lookup"><span data-stu-id="4c615-144">integer-constant: one of</span></span>

    <span data-ttu-id="4c615-145">\# (десятичное число)</span><span class="sxs-lookup"><span data-stu-id="4c615-145">\# (decimal number)</span></span>

    <span data-ttu-id="4c615-146">0 \# (восьмеричное число)</span><span class="sxs-lookup"><span data-stu-id="4c615-146">0\# (octal number)</span></span>

    <span data-ttu-id="4c615-147">0x \# (шестнадцатеричное число)</span><span class="sxs-lookup"><span data-stu-id="4c615-147">0x\# (hex number)</span></span>

-   <span data-ttu-id="4c615-148">суффикс Integer-может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="4c615-148">integer-suffix can be any one of these:</span></span>

    <span data-ttu-id="4c615-149">u U l L</span><span class="sxs-lookup"><span data-stu-id="4c615-149">u U l L</span></span>

## <a name="characters"></a><span data-ttu-id="4c615-150">Characters</span><span class="sxs-lookup"><span data-stu-id="4c615-150">Characters</span></span>

<span data-ttu-id="4c615-151">Символы представлены в HLSL следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4c615-151">Characters are represented in HLSL as follows:</span></span>



|                                           |                                                                 |
|-------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4c615-152">ц</span><span class="sxs-lookup"><span data-stu-id="4c615-152">'c'</span></span>                                       | <span data-ttu-id="4c615-153">символов</span><span class="sxs-lookup"><span data-stu-id="4c615-153">(character)</span></span>                                                     |
| <span data-ttu-id="4c615-154">' \\ a ' ' \\ b ' ' \\ f ' ' \\ b ' ' \\ r \\ \\ ' ' ' ' v ' '</span><span class="sxs-lookup"><span data-stu-id="4c615-154">'\\a' '\\b' '\\f' '\\b' '\\r' '\\t' '\\v'</span></span> | <span data-ttu-id="4c615-155">экранирует</span><span class="sxs-lookup"><span data-stu-id="4c615-155">(escapes)</span></span>                                                       |
| <span data-ttu-id="4c615-156">'\\\#\#\#'</span><span class="sxs-lookup"><span data-stu-id="4c615-156">'\\\#\#\#'</span></span>                                | <span data-ttu-id="4c615-157">(восьмеричный escape-символ — \# это восьмеричная цифра)</span><span class="sxs-lookup"><span data-stu-id="4c615-157">(octal escape, each \# is an octal digit)</span></span>                       |
| <span data-ttu-id="4c615-158">" \\ x \# "</span><span class="sxs-lookup"><span data-stu-id="4c615-158">'\\x\#'</span></span>                                   | <span data-ttu-id="4c615-159">(шестнадцатеричный escape \# -символ, шестнадцатеричное число, любое количество цифр)</span><span class="sxs-lookup"><span data-stu-id="4c615-159">(hex escape, \# is hex number, any number of digits)</span></span>            |
| <span data-ttu-id="4c615-160">" \\ c"</span><span class="sxs-lookup"><span data-stu-id="4c615-160">'\\c'</span></span>                                     | <span data-ttu-id="4c615-161">(c — это другой символ, включая обратную косую черту и кавычки)</span><span class="sxs-lookup"><span data-stu-id="4c615-161">(c is other character, including backslash and quotation marks)</span></span> |



 

<span data-ttu-id="4c615-162">В выражениях препроцессора не поддерживаются escape-последовательности.</span><span class="sxs-lookup"><span data-stu-id="4c615-162">Escapes are not supported in preprocessor expressions.</span></span>

## <a name="strings"></a><span data-ttu-id="4c615-163">Строки</span><span class="sxs-lookup"><span data-stu-id="4c615-163">Strings</span></span>

<span data-ttu-id="4c615-164">Строки представлены в HLSL следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4c615-164">Strings are represented in HLSL as follows:</span></span>

<span data-ttu-id="4c615-165">"s" (s — любая строка с escape-символами).</span><span class="sxs-lookup"><span data-stu-id="4c615-165">"s" (s is any string with escapes).</span></span>

## <a name="identifiers"></a><span data-ttu-id="4c615-166">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="4c615-166">Identifiers</span></span>

<span data-ttu-id="4c615-167">Идентификаторы представлены в HLSL следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4c615-167">Identifiers are represented in HLSL as follows:</span></span>


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a><span data-ttu-id="4c615-168">Операторы</span><span class="sxs-lookup"><span data-stu-id="4c615-168">Operators</span></span>


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



<span data-ttu-id="4c615-169">Кроме того, любой другой отдельный символ, не совпадающий с другим правилом.</span><span class="sxs-lookup"><span data-stu-id="4c615-169">Also any other single character that did not match another rule.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c615-170">См. также</span><span class="sxs-lookup"><span data-stu-id="4c615-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c615-171">Приложение (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c615-171">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




