---
description: Можно определить и назначить пользовательские области ввода, используя синтаксис регулярных выражений для рукописного ввода, понятный некоторым распознавателям рукописного ввода Майкрософт.
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: Справочник по синтаксису регулярных выражений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c0de50ff37795032719d9bc90ee81891324ba9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104273197"
---
# <a name="regular-expression-syntax-reference"></a><span data-ttu-id="18c2b-103">Справочник по синтаксису регулярных выражений</span><span class="sxs-lookup"><span data-stu-id="18c2b-103">Regular Expression Syntax Reference</span></span>

<span data-ttu-id="18c2b-104">Можно определить и назначить пользовательские области ввода, используя синтаксис регулярных выражений для рукописного ввода, понятный некоторым распознавателям рукописного ввода Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="18c2b-104">You can define and assign custom input scopes using the handwriting regular expression syntax that is understood by some of the Microsoft handwriting recognizers.</span></span> <span data-ttu-id="18c2b-105">Синтаксис представляет собой подмножество [реализации языка регулярных выражений](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) в платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="18c2b-105">The syntax is a subset of the [Regular Expression Language Implementation](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) in the .NET Framework.</span></span>

<span data-ttu-id="18c2b-106">Существуют некоторые различия в способах использования регулярных выражений рукописного ввода и способах использования других типов регулярных выражений.</span><span class="sxs-lookup"><span data-stu-id="18c2b-106">There are some differences in the way that handwriting regular expressions are used and the way the other types of regular expressions are used.</span></span> <span data-ttu-id="18c2b-107">Синтаксис рукописного ввода используется для указания точной строки, которая будет соответствовать механизму распознавания, а не подстроке.</span><span class="sxs-lookup"><span data-stu-id="18c2b-107">The handwriting syntax is used to specify an exact string that will be matched by the recognition engine and not a sub-string.</span></span> <span data-ttu-id="18c2b-108">Например, регулярное выражение s ( \[ a-z \] +) p возвратит совпадение для "полный курс", "останавливаться", "Step" и "есофагус".</span><span class="sxs-lookup"><span data-stu-id="18c2b-108">For example, the regular expression s(\[a-z\]+)p would return matches for "soup", "stop", "instep", and "esophagus".</span></span> <span data-ttu-id="18c2b-109">В то же время, эквивалентное регулярное выражение для рукописного ввода, например s (! — \_ онечар) + p, будет соответствовать "полный курс" и "останавливаться", но не "пошаговый" и "есофагус".</span><span class="sxs-lookup"><span data-stu-id="18c2b-109">Whereas, an equivalent handwriting regular expression such as s(!IS\_ONECHAR)+p would match "soup" and "stop", but not "instep" and "esophagus".</span></span>

<span data-ttu-id="18c2b-110">Регулярные выражения для рукописного ввода не поддерживают неразрывные пробелы в регулярных выражениях.</span><span class="sxs-lookup"><span data-stu-id="18c2b-110">Handwriting regular expressions do not support non-breaking spaces within regular expressions.</span></span> <span data-ttu-id="18c2b-111">Это значит, что нельзя использовать сущность "nbsp" в регулярном выражении рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="18c2b-111">That is, you cannot use the "nbsp" entity within a handwriting regular expression.</span></span>

<span data-ttu-id="18c2b-112">В следующих разделах более подробно описан синтаксис.</span><span class="sxs-lookup"><span data-stu-id="18c2b-112">The following sections describe the syntax in more detail.</span></span>

## <a name="valid-operators"></a><span data-ttu-id="18c2b-113">Допустимые операторы</span><span class="sxs-lookup"><span data-stu-id="18c2b-113">Valid Operators</span></span>

<span data-ttu-id="18c2b-114">Следующие операторы допустимы для создания регулярных выражений для определения областей ввода для распознавателей рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="18c2b-114">The following operators are valid for creating regular expressions to define input scopes for handwriting recognizers.</span></span>



| <span data-ttu-id="18c2b-115">Оператор</span><span class="sxs-lookup"><span data-stu-id="18c2b-115">Operator</span></span>      | <span data-ttu-id="18c2b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="18c2b-116">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | <span data-ttu-id="18c2b-117">Постфиксный унарный оператор, обозначающий ноль или более вхождений операнда.</span><span class="sxs-lookup"><span data-stu-id="18c2b-117">Postfix unary operator signifying zero or more occurrences of the operand.</span></span><br/> |
| +<br/>  | <span data-ttu-id="18c2b-118">Постфиксный унарный оператор, обозначающий одно или несколько вхождений операнда.</span><span class="sxs-lookup"><span data-stu-id="18c2b-118">Postfix unary operator signifying one or more occurrences of the operand.</span></span><br/>  |
| <span data-ttu-id="18c2b-119">?</span><span class="sxs-lookup"><span data-stu-id="18c2b-119">?</span></span><br/>  | <span data-ttu-id="18c2b-120">Постфиксный унарный оператор, обозначающий ноль или одно вхождение операнда.</span><span class="sxs-lookup"><span data-stu-id="18c2b-120">Postfix unary operator signifying zero or one occurrence of the operand.</span></span><br/>   |
| \|<br/> | <span data-ttu-id="18c2b-121">Бинарный оператор инфиксные значение "или".</span><span class="sxs-lookup"><span data-stu-id="18c2b-121">Binary infix operator meaning "or".</span></span><br/>                                        |
| <span data-ttu-id="18c2b-122">()</span><span class="sxs-lookup"><span data-stu-id="18c2b-122">()</span></span><br/> | <span data-ttu-id="18c2b-123">Используется для группирования элементов.</span><span class="sxs-lookup"><span data-stu-id="18c2b-123">Used to group items.</span></span><br/>                                                       |



 

<span data-ttu-id="18c2b-124">Реализация регулярных выражений в Майкрософт для распознавателей рукописного ввода позволяет выполнять повторяющиеся приложения постфиксных унарных операторов.</span><span class="sxs-lookup"><span data-stu-id="18c2b-124">The Microsoft implementation of regular expressions for handwriting recognizers allows repeated applications of postfix unary operators.</span></span> <span data-ttu-id="18c2b-125">Например, a \* \* = (а \* ) \* = a \* , b??</span><span class="sxs-lookup"><span data-stu-id="18c2b-125">For example, a\*\* = (a\*)\* = a\*, b??</span></span> <span data-ttu-id="18c2b-126">= (b?)?</span><span class="sxs-lookup"><span data-stu-id="18c2b-126">= (b?)?</span></span> <span data-ttu-id="18c2b-127">= b?.</span><span class="sxs-lookup"><span data-stu-id="18c2b-127">= b?.</span></span> <span data-ttu-id="18c2b-128">Они также разрешают непоследовательные повторы, например: a \* ? \* = ((а \* )?) \* = \* \* a \* .</span><span class="sxs-lookup"><span data-stu-id="18c2b-128">They also allow non-consecutive repetitions, for example: a\*?\* = ((a\*)?)\* = (a\*)\* = a\*.</span></span> <span data-ttu-id="18c2b-129">Это отличается от платформа .NET Framework регулярных выражений, которые разрешают только?</span><span class="sxs-lookup"><span data-stu-id="18c2b-129">This is different from .NET Framework regular expressions, which only allow the ?</span></span> <span data-ttu-id="18c2b-130">оператор, который должен повторяться.</span><span class="sxs-lookup"><span data-stu-id="18c2b-130">operator to be repeated.</span></span>

<span data-ttu-id="18c2b-131">Другое отличие от платформа .NET Framework регулярных выражений заключается в том, что регулярные выражения для рукописного ввода не поддерживают пустое выражение, обозначенное пустой парой скобок ().</span><span class="sxs-lookup"><span data-stu-id="18c2b-131">Another difference from .NET Framework regular expressions is that handwriting regular expressions do not support an empty expression designated with an empty pair of parentheses, ().</span></span>

> [!Note]  
> <span data-ttu-id="18c2b-132">Для регулярных выражений рукописного ввода поддерживаются только символы кодовой страницы 1252.</span><span class="sxs-lookup"><span data-stu-id="18c2b-132">Only characters in the 1252 codepage are supported for handwriting regular expressions.</span></span>

 

## <a name="using-input-scopes"></a><span data-ttu-id="18c2b-133">Использование областей ввода</span><span class="sxs-lookup"><span data-stu-id="18c2b-133">Using Input Scopes</span></span>

<span data-ttu-id="18c2b-134">Также можно использовать набор стандартных областей ввода, которые определены как часть функции [**сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) в регулярных выражениях.</span><span class="sxs-lookup"><span data-stu-id="18c2b-134">You can also use the set of regular input scopes that are defined as part of the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) function in your regular expressions.</span></span> <span data-ttu-id="18c2b-135">Например, значение Month (числовое) — это \_ \_ месяц даты.</span><span class="sxs-lookup"><span data-stu-id="18c2b-135">For example, the value for Month (numerical) is IS\_DATE\_MONTH.</span></span> <span data-ttu-id="18c2b-136">Синтаксис для указания области ввода как части регулярного выражения заключается в начале перечислимого значения области ввода с открывающей круглой скобкой и восклицательным знаком, (! и поставьте закрывающую круглую скобку,) в конце.</span><span class="sxs-lookup"><span data-stu-id="18c2b-136">The syntax for specifying an input scope as part of a regular expression is to prepend the input scope enumerated value with an open parenthesis and an exclamation point, (!, and place a closing parenthesis, ), on the end.</span></span> <span data-ttu-id="18c2b-137">Пример:</span><span class="sxs-lookup"><span data-stu-id="18c2b-137">For example:</span></span>

<span data-ttu-id="18c2b-138">(! Является \_ \_месяц даты)</span><span class="sxs-lookup"><span data-stu-id="18c2b-138">(!IS\_DATE\_MONTH)</span></span>

<span data-ttu-id="18c2b-139">Если объединить \_ область ввода по умолчанию, индексами ее с любой другой областью ввода, то этот распознаватель может вернуть любое одно выражение, которое поддерживает модель языка по умолчанию (например, одно слово из системного словаря или даты) с знаками препинания или без них, или любое значение, которое соответствует остальной части регулярного выражения, переданного распознавателю.</span><span class="sxs-lookup"><span data-stu-id="18c2b-139">If you combine the IS\_DEFAULT input scope by ORing it with any other input scope, the effect is that the recognizer can return either any single expression that the default language model supports (for example, one word from the system dictionary or a date) with or without punctuation, or any value that meets the rest of the regular expression passed in to the recognizer.</span></span>

> [!Note]  
> <span data-ttu-id="18c2b-140">Следующие члены [**сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) не поддерживаются в регулярных выражениях: \_ фраселист, является \_ REGULAREXPRESSION, является \_ SRGS, является \_ XML.</span><span class="sxs-lookup"><span data-stu-id="18c2b-140">The following members of [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) are not supported in regular expressions: IS\_PHRASELIST, IS\_REGULAREXPRESSION, IS\_SRGS, IS\_XML.</span></span>

 

## <a name="unsupported-operators"></a><span data-ttu-id="18c2b-141">Неподдерживаемые операторы</span><span class="sxs-lookup"><span data-stu-id="18c2b-141">Unsupported Operators</span></span>

<span data-ttu-id="18c2b-142">Следующие операторы регулярных выражений не поддерживаются при создании регулярных выражений рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="18c2b-142">The following regular expression operators are not supported when creating handwriting regular expressions.</span></span>



| <span data-ttu-id="18c2b-143">Оператор</span><span class="sxs-lookup"><span data-stu-id="18c2b-143">Operator</span></span>                                     | <span data-ttu-id="18c2b-144">Описание</span><span class="sxs-lookup"><span data-stu-id="18c2b-144">Description</span></span>                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="18c2b-145">.</span><span class="sxs-lookup"><span data-stu-id="18c2b-145">.</span></span><br/>                                 | <span data-ttu-id="18c2b-146">Символ точки.</span><span class="sxs-lookup"><span data-stu-id="18c2b-146">Period character.</span></span><br/>                                        |
| \[\]<br/>                              | <span data-ttu-id="18c2b-147">Квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="18c2b-147">Square brackets.</span></span> <span data-ttu-id="18c2b-148">Используйте круглые скобки для группирования элементов.</span><span class="sxs-lookup"><span data-stu-id="18c2b-148">Use parenthesis for grouping items.</span></span><br/>     |
| {}<br/>                                | <span data-ttu-id="18c2b-149">Фигурные скобки.</span><span class="sxs-lookup"><span data-stu-id="18c2b-149">Curly brackets.</span></span><br/>                                          |
| <span data-ttu-id="18c2b-150">(?\# Комментарий) и \# \[ комментарий\]</span><span class="sxs-lookup"><span data-stu-id="18c2b-150">(?\# comment) and \#\[ comment \]</span></span><br/> | <span data-ttu-id="18c2b-151">Примечания.</span><span class="sxs-lookup"><span data-stu-id="18c2b-151">Comments.</span></span><br/>                                                |
| $<br/>                                 | <span data-ttu-id="18c2b-152">Знак доллара.</span><span class="sxs-lookup"><span data-stu-id="18c2b-152">Dollar sign character.</span></span><br/>                                   |
| ^<br/>                                 | <span data-ttu-id="18c2b-153">Знак крышки.</span><span class="sxs-lookup"><span data-stu-id="18c2b-153">Caret character.</span></span><br/>                                         |
| -<br/>                                 | <span data-ttu-id="18c2b-154">Дефисный символ.</span><span class="sxs-lookup"><span data-stu-id="18c2b-154">Dash character.</span></span> <span data-ttu-id="18c2b-155">Необходимо или ( \| ) вместе со всеми наборами элементов.</span><span class="sxs-lookup"><span data-stu-id="18c2b-155">Must OR (\|) together all sets of items.</span></span><br/> |



 

## <a name="escaping-characters"></a><span data-ttu-id="18c2b-156">Экранирование символов</span><span class="sxs-lookup"><span data-stu-id="18c2b-156">Escaping Characters</span></span>

<span data-ttu-id="18c2b-157">Обычные символы, отличные от тех, которые перечислены в следующей таблице, совпадают.</span><span class="sxs-lookup"><span data-stu-id="18c2b-157">Ordinary characters, other than the ones in the following table, match themselves.</span></span> <span data-ttu-id="18c2b-158">То есть "a" в регулярном выражении указывает, что входные данные должны соответствовать "a".</span><span class="sxs-lookup"><span data-stu-id="18c2b-158">That is, an "a" in a regular expression specifies that input should match an "a".</span></span>

<span data-ttu-id="18c2b-159">Еще одно существенное различие в написании регулярных выражений рукописного ввода заключается в том, что в регулярном выражении можно только экранирование ограниченного набора символов.</span><span class="sxs-lookup"><span data-stu-id="18c2b-159">Another significant difference in writing handwriting regular expressions is that you can only escape a limited set of characters within a regular expression.</span></span> <span data-ttu-id="18c2b-160">В следующей таблице приведен допустимый набор символов, которые можно экранировановать.</span><span class="sxs-lookup"><span data-stu-id="18c2b-160">The following table outlines the allowed set of characters that can be escaped.</span></span> <span data-ttu-id="18c2b-161">Любая другая попытка экранирования символа приведет к ошибке, вызываемой распознавателем.</span><span class="sxs-lookup"><span data-stu-id="18c2b-161">Any other attempt to escape a character will result in an error being thrown by the recognizer.</span></span>



| <span data-ttu-id="18c2b-162">Знак</span><span class="sxs-lookup"><span data-stu-id="18c2b-162">Character</span></span>       |
|-----------------|
| \\\*<br/> |
| \\+<br/>  |
| <span data-ttu-id="18c2b-163">\\?</span><span class="sxs-lookup"><span data-stu-id="18c2b-163">\\?</span></span><br/>  |
| <span data-ttu-id="18c2b-164">\\(</span><span class="sxs-lookup"><span data-stu-id="18c2b-164">\\(</span></span><br/>  |
| <span data-ttu-id="18c2b-165">\\)</span><span class="sxs-lookup"><span data-stu-id="18c2b-165">\\)</span></span><br/>  |
| \\\|<br/> |
| \\\\<br/> |
| <span data-ttu-id="18c2b-166">\\!</span><span class="sxs-lookup"><span data-stu-id="18c2b-166">\\!</span></span><br/>  |
| <span data-ttu-id="18c2b-167">\\.</span><span class="sxs-lookup"><span data-stu-id="18c2b-167">\\.</span></span><br/>  |
| \\\[<br/> |
| \\\]<br/> |
| \\^<br/>  |
| <span data-ttu-id="18c2b-168">\\{</span><span class="sxs-lookup"><span data-stu-id="18c2b-168">\\{</span></span><br/>  |
| <span data-ttu-id="18c2b-169">\\}</span><span class="sxs-lookup"><span data-stu-id="18c2b-169">\\}</span></span><br/>  |
| \\$<br/>  |
| \\\#<br/> |



 

 

 