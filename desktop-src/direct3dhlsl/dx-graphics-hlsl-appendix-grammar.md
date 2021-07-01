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
ms.openlocfilehash: b77f1050beaee2b269d12e69704018e3c5abee6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129852"
---
# <a name="grammar"></a><span data-ttu-id="639e2-103">Грамматика</span><span class="sxs-lookup"><span data-stu-id="639e2-103">Grammar</span></span>

<span data-ttu-id="639e2-104">Инструкции HLSL создаются с использованием следующих правил для грамматики.</span><span class="sxs-lookup"><span data-stu-id="639e2-104">HLSL statements are constructed using the following rules for grammar.</span></span>

-   [<span data-ttu-id="639e2-105">Пробелы</span><span class="sxs-lookup"><span data-stu-id="639e2-105">Whitespace</span></span>](#whitespace)
-   [<span data-ttu-id="639e2-106">Числа с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="639e2-106">Floating point numbers</span></span>](#floating-point-numbers)
-   [<span data-ttu-id="639e2-107">Целые числа</span><span class="sxs-lookup"><span data-stu-id="639e2-107">Integer numbers</span></span>](#integer-numbers)
-   [<span data-ttu-id="639e2-108">Символы</span><span class="sxs-lookup"><span data-stu-id="639e2-108">Characters</span></span>](#characters)
-   [<span data-ttu-id="639e2-109">Строки</span><span class="sxs-lookup"><span data-stu-id="639e2-109">Strings</span></span>](#strings)
-   [<span data-ttu-id="639e2-110">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="639e2-110">Identifiers</span></span>](#identifiers)
-   [<span data-ttu-id="639e2-111">Операторы</span><span class="sxs-lookup"><span data-stu-id="639e2-111">Operators</span></span>](#operators)
-   [<span data-ttu-id="639e2-112">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="639e2-112">Related topics</span></span>](#related-topics)

## <a name="whitespace"></a><span data-ttu-id="639e2-113">Пробелы</span><span class="sxs-lookup"><span data-stu-id="639e2-113">Whitespace</span></span>

<span data-ttu-id="639e2-114">Следующие символы распознаются как пробелы.</span><span class="sxs-lookup"><span data-stu-id="639e2-114">The following characters are recognized as white space.</span></span>

- <span data-ttu-id="639e2-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="639e2-115">SPACE</span></span>
- <span data-ttu-id="639e2-116">TAB</span><span class="sxs-lookup"><span data-stu-id="639e2-116">TAB</span></span>
- <span data-ttu-id="639e2-117">КОНЦА строки</span><span class="sxs-lookup"><span data-stu-id="639e2-117">EOL</span></span>
- <span data-ttu-id="639e2-118">Комментарии в стиле C (/ \* \* /)</span><span class="sxs-lookup"><span data-stu-id="639e2-118">C style comments (/\* \*/)</span></span>
- <span data-ttu-id="639e2-119">Комментарии в стиле C++ (//)</span><span class="sxs-lookup"><span data-stu-id="639e2-119">C++ style comments (//)</span></span>

## <a name="floating-point-numbers"></a><span data-ttu-id="639e2-120">Числа с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="639e2-120">Floating point numbers</span></span>

<span data-ttu-id="639e2-121">Числа с плавающей запятой представлены в HLSL следующим образом:</span><span class="sxs-lookup"><span data-stu-id="639e2-121">Floating point numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="639e2-122">экспонента с плавающей запятой-часть (неявное) (неявное) (OPT)</span><span class="sxs-lookup"><span data-stu-id="639e2-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span></span>

    <span data-ttu-id="639e2-123">экспонента числа с плавающей запятой-часть (OPT)</span><span class="sxs-lookup"><span data-stu-id="639e2-123">digit-sequence exponent-part floating-suffix(opt)</span></span>

-   <span data-ttu-id="639e2-124">Дробная константа:</span><span class="sxs-lookup"><span data-stu-id="639e2-124">fractional-constant :</span></span>

    <span data-ttu-id="639e2-125">последовательность цифр (OPT).</span><span class="sxs-lookup"><span data-stu-id="639e2-125">digit-sequence(opt) .</span></span> <span data-ttu-id="639e2-126">последовательность цифр</span><span class="sxs-lookup"><span data-stu-id="639e2-126">digit-sequence</span></span>

    <span data-ttu-id="639e2-127">последовательность цифр.</span><span class="sxs-lookup"><span data-stu-id="639e2-127">digit-sequence .</span></span>

-   <span data-ttu-id="639e2-128">степень — часть:</span><span class="sxs-lookup"><span data-stu-id="639e2-128">exponent-part :</span></span>

    <span data-ttu-id="639e2-129">знак "e" (нежелательна) — последовательность цифр</span><span class="sxs-lookup"><span data-stu-id="639e2-129">e sign(opt) digit-sequence</span></span>

    <span data-ttu-id="639e2-130">Знак "E" (нежелательна) — последовательность цифр</span><span class="sxs-lookup"><span data-stu-id="639e2-130">E sign(opt) digit-sequence</span></span>

-   <span data-ttu-id="639e2-131">sign : один из указанных ниже знаков</span><span class="sxs-lookup"><span data-stu-id="639e2-131">sign : one of</span></span>

    \+ -

-   <span data-ttu-id="639e2-132">последовательность цифр:</span><span class="sxs-lookup"><span data-stu-id="639e2-132">digit-sequence :</span></span>

    <span data-ttu-id="639e2-133">цифровой-знак</span><span class="sxs-lookup"><span data-stu-id="639e2-133">digit</span></span>

    <span data-ttu-id="639e2-134">последовательность-цифр цифра</span><span class="sxs-lookup"><span data-stu-id="639e2-134">digit-sequence digit</span></span>

-   <span data-ttu-id="639e2-135">floating-suffix : одно из указанных ниже значений</span><span class="sxs-lookup"><span data-stu-id="639e2-135">floating-suffix : one of</span></span>

    <span data-ttu-id="639e2-136">h з f l L</span><span class="sxs-lookup"><span data-stu-id="639e2-136">h H f F l L</span></span>

    <span data-ttu-id="639e2-137">Используйте суффикс "L" для указания полного литерала с плавающей запятой 64-разрядной точности.</span><span class="sxs-lookup"><span data-stu-id="639e2-137">Use the “L” suffix to specify a full 64-bit precision floating-point literal.</span></span> <span data-ttu-id="639e2-138">Значение по умолчанию — 32-разрядный литерал с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="639e2-138">A 32-bit float literal is the default.</span></span>

    <span data-ttu-id="639e2-139">Например, компилятор распознает следующее литеральное значение в виде литерала с плавающей запятой 32-разрядной точности и игнорирует младшие биты:</span><span class="sxs-lookup"><span data-stu-id="639e2-139">For example, the compiler recognizes the following literal value as a 32-bit precision floating-point literal and ignores the lower bits:</span></span>

    ```
    double x = -0.6473313946860445;
    ```

    

    <span data-ttu-id="639e2-140">Компилятор распознает следующее литеральное значение как литерал с плавающей запятой 64-разрядной точности:</span><span class="sxs-lookup"><span data-stu-id="639e2-140">The compiler recognizes the following literal value as a 64-bit precision floating-point literal:</span></span>

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a><span data-ttu-id="639e2-141">Целые числа</span><span class="sxs-lookup"><span data-stu-id="639e2-141">Integer numbers</span></span>

<span data-ttu-id="639e2-142">Целочисленные числа представлены в HLSL следующим образом:</span><span class="sxs-lookup"><span data-stu-id="639e2-142">Integer numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="639e2-143">Integer-Константное целое число-суффикс (OPT)</span><span class="sxs-lookup"><span data-stu-id="639e2-143">integer-constant integer-suffix(opt)</span></span>
-   <span data-ttu-id="639e2-144">Integer — константа: один из</span><span class="sxs-lookup"><span data-stu-id="639e2-144">integer-constant: one of</span></span>

    <span data-ttu-id="639e2-145">\# (десятичное число)</span><span class="sxs-lookup"><span data-stu-id="639e2-145">\# (decimal number)</span></span>

    <span data-ttu-id="639e2-146">0 \# (восьмеричное число)</span><span class="sxs-lookup"><span data-stu-id="639e2-146">0\# (octal number)</span></span>

    <span data-ttu-id="639e2-147">0x \# (шестнадцатеричное число)</span><span class="sxs-lookup"><span data-stu-id="639e2-147">0x\# (hex number)</span></span>

-   <span data-ttu-id="639e2-148">суффикс Integer-может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="639e2-148">integer-suffix can be any one of these:</span></span>

    <span data-ttu-id="639e2-149">u U l L</span><span class="sxs-lookup"><span data-stu-id="639e2-149">u U l L</span></span>

## <a name="characters"></a><span data-ttu-id="639e2-150">Characters</span><span class="sxs-lookup"><span data-stu-id="639e2-150">Characters</span></span>

<span data-ttu-id="639e2-151">Символы представлены в HLSL следующим образом:</span><span class="sxs-lookup"><span data-stu-id="639e2-151">Characters are represented in HLSL as follows:</span></span>



| <span data-ttu-id="639e2-152">Знак</span><span class="sxs-lookup"><span data-stu-id="639e2-152">Character</span></span>                                          | <span data-ttu-id="639e2-153">Описание</span><span class="sxs-lookup"><span data-stu-id="639e2-153">Description</span></span>                                                                |
|-------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="639e2-154">ц</span><span class="sxs-lookup"><span data-stu-id="639e2-154">'c'</span></span>                                       | <span data-ttu-id="639e2-155">символов</span><span class="sxs-lookup"><span data-stu-id="639e2-155">(character)</span></span>                                                     |
| <span data-ttu-id="639e2-156">' \\ a ' ' \\ b ' ' \\ f ' ' \\ b ' ' \\ r \\ \\ ' ' ' ' v ' '</span><span class="sxs-lookup"><span data-stu-id="639e2-156">'\\a' '\\b' '\\f' '\\b' '\\r' '\\t' '\\v'</span></span> | <span data-ttu-id="639e2-157">экранирует</span><span class="sxs-lookup"><span data-stu-id="639e2-157">(escapes)</span></span>                                                       |
| <span data-ttu-id="639e2-158">'\\\#\#\#'</span><span class="sxs-lookup"><span data-stu-id="639e2-158">'\\\#\#\#'</span></span>                                | <span data-ttu-id="639e2-159">(восьмеричный escape-символ — \# это восьмеричная цифра)</span><span class="sxs-lookup"><span data-stu-id="639e2-159">(octal escape, each \# is an octal digit)</span></span>                       |
| <span data-ttu-id="639e2-160">" \\ x \# "</span><span class="sxs-lookup"><span data-stu-id="639e2-160">'\\x\#'</span></span>                                   | <span data-ttu-id="639e2-161">(шестнадцатеричный escape \# -символ, шестнадцатеричное число, любое количество цифр)</span><span class="sxs-lookup"><span data-stu-id="639e2-161">(hex escape, \# is hex number, any number of digits)</span></span>            |
| <span data-ttu-id="639e2-162">" \\ c"</span><span class="sxs-lookup"><span data-stu-id="639e2-162">'\\c'</span></span>                                     | <span data-ttu-id="639e2-163">(c — это другой символ, включая обратную косую черту и кавычки)</span><span class="sxs-lookup"><span data-stu-id="639e2-163">(c is other character, including backslash and quotation marks)</span></span> |



 

<span data-ttu-id="639e2-164">В выражениях препроцессора не поддерживаются escape-последовательности.</span><span class="sxs-lookup"><span data-stu-id="639e2-164">Escapes are not supported in preprocessor expressions.</span></span>

## <a name="strings"></a><span data-ttu-id="639e2-165">Строки</span><span class="sxs-lookup"><span data-stu-id="639e2-165">Strings</span></span>

<span data-ttu-id="639e2-166">Строки представлены в HLSL следующим образом:</span><span class="sxs-lookup"><span data-stu-id="639e2-166">Strings are represented in HLSL as follows:</span></span>

<span data-ttu-id="639e2-167">"s" (s — любая строка с escape-символами).</span><span class="sxs-lookup"><span data-stu-id="639e2-167">"s" (s is any string with escapes).</span></span>

## <a name="identifiers"></a><span data-ttu-id="639e2-168">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="639e2-168">Identifiers</span></span>

<span data-ttu-id="639e2-169">Идентификаторы представлены в HLSL следующим образом:</span><span class="sxs-lookup"><span data-stu-id="639e2-169">Identifiers are represented in HLSL as follows:</span></span>


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a><span data-ttu-id="639e2-170">Операторы</span><span class="sxs-lookup"><span data-stu-id="639e2-170">Operators</span></span>


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



<span data-ttu-id="639e2-171">Кроме того, любой другой отдельный символ, не совпадающий с другим правилом.</span><span class="sxs-lookup"><span data-stu-id="639e2-171">Also any other single character that did not match another rule.</span></span>

## <a name="related-topics"></a><span data-ttu-id="639e2-172">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="639e2-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="639e2-173">Приложение (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="639e2-173">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




