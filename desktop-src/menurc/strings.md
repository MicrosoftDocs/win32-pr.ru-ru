---
title: Строки
description: В этом разделе обсуждаются строковые функции.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- ресурсы, строки
- строки;
- строковые функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3231006de2dfe6ed611b58e5b511819a40c21e8b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103795223"
---
# <a name="strings"></a><span data-ttu-id="8b7a2-106">Строки</span><span class="sxs-lookup"><span data-stu-id="8b7a2-106">Strings</span></span>

<span data-ttu-id="8b7a2-107">В этом разделе описываются строковые функции и объясняется, как использовать их в приложениях.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-107">This section describes the string functions and explains how to use them in your applications.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="8b7a2-108">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="8b7a2-108">In This Section</span></span>



| <span data-ttu-id="8b7a2-109">Имя</span><span class="sxs-lookup"><span data-stu-id="8b7a2-109">Name</span></span>                                     | <span data-ttu-id="8b7a2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8b7a2-110">Description</span></span>                                             |
|------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="8b7a2-111">Сведения о строках</span><span class="sxs-lookup"><span data-stu-id="8b7a2-111">About Strings</span></span>](about-strings.md)       | <span data-ttu-id="8b7a2-112">Описывает строковые функции.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-112">Discusses the string functions.</span></span><br/>              |
| [<span data-ttu-id="8b7a2-113">О Стрсафе. h</span><span class="sxs-lookup"><span data-stu-id="8b7a2-113">About Strsafe.h</span></span>](strsafe-ovw.md)       | <span data-ttu-id="8b7a2-114">Описывает строковые функции в Стрсафе. h.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-114">Discusses the string functions in Strsafe.h.</span></span><br/> |
| [<span data-ttu-id="8b7a2-115">Ссылка на строку</span><span class="sxs-lookup"><span data-stu-id="8b7a2-115">String Reference</span></span>](string-reference.md) | <span data-ttu-id="8b7a2-116">Содержит справочник по API.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-116">Contains the API reference.</span></span><br/>                  |



 

### <a name="string-functions"></a><span data-ttu-id="8b7a2-117">Строковые функции</span><span class="sxs-lookup"><span data-stu-id="8b7a2-117">String Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b7a2-118">Имя</span><span class="sxs-lookup"><span data-stu-id="8b7a2-118">Name</span></span></th>
<th><span data-ttu-id="8b7a2-119">Описание</span><span class="sxs-lookup"><span data-stu-id="8b7a2-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8b7a2-120"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>чарловер</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-120"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-121">Преобразует строку символов или один символ в нижний регистр.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-121">Converts a character string or a single character to lowercase.</span></span> <span data-ttu-id="8b7a2-122">Если операнд является символьной строкой, функция преобразует символы на месте.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-122">If the operand is a character string, the function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-123"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>чарловербуфф</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-123"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-124">Преобразует символы верхнего регистра в буфере в символы нижнего регистра.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-124">Converts uppercase characters in a buffer to lowercase characters.</span></span> <span data-ttu-id="8b7a2-125">Функция преобразует символы на месте.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-125">The function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-126"><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>чарнекст</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-126"><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-127">Извлекает указатель на следующий символ в строке.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-127">Retrieves a pointer to the next character in a string.</span></span> <span data-ttu-id="8b7a2-128">Эта функция может выполнять обработку строк, состоящих из однобайтовых символов или из одного или нескольких байтов.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-128">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-129"><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>чарнекстекса</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-129"><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-130">Получает указатель на следующий символ в строке.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-130">Retrieves the pointer to the next character in a string.</span></span> <span data-ttu-id="8b7a2-131">Эта функция может выполнять обработку строк, состоящих из однобайтовых символов или из одного или нескольких байтов.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-131">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-132"><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>чарпрев</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-132"><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-133">Извлекает указатель на предшествующий символ в строке.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-133">Retrieves a pointer to the preceding character in a string.</span></span> <span data-ttu-id="8b7a2-134">Эта функция может выполнять обработку строк, состоящих из однобайтовых символов или из одного или нескольких байтов.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-134">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-135"><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>чарпревекса</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-135"><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-136">Получает указатель на предшествующий символ в строке.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-136">Retrieves the pointer to the preceding character in a string.</span></span> <span data-ttu-id="8b7a2-137">Эта функция может выполнять обработку строк, состоящих из однобайтовых символов или из одного или нескольких байтов.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-137">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-138"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>чартуем</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-138"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-139">Преобразует строку в набор символов, определяемый изготовителем оборудования.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-139">Translates a string into the OEM-defined character set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-140"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>чартуембуфф</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-140"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-141">Преобразует указанное число символов в строке в набор символов, определенный изготовителем оборудования.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-141">Translates a specified number of characters in a string into the OEM-defined character set.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-142"><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>чаруппер</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-142"><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-143">Преобразует строку символов или один символ в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-143">Converts a character string or a single character to uppercase.</span></span> <span data-ttu-id="8b7a2-144">Если операнд является символьной строкой, функция преобразует символы на месте.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-144">If the operand is a character string, the function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-145"><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>чаруппербуфф</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-145"><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-146">Преобразует символы нижнего регистра в буфере в символы верхнего регистра.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-146">Converts lowercase characters in a buffer to uppercase characters.</span></span> <span data-ttu-id="8b7a2-147">Функция преобразует символы на месте.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-147">The function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-148"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-148"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-149">Сравнивает две символьные строки, используя заданный языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-149">Compares two character strings, using the specified locale.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8b7a2-150">Для совместимости с Юникодом используйте <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>компарестринжекс</strong></a> или версию <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>API CompareString</strong></a>с поддержкой Юникода.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-150">For compatibility with Unicode, use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> or the Unicode version of <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-151"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>компарестринжекс</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-151"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-152">Сравнивает два строки Юникода (расширенных символов) с использованием указанного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-152">Compares two Unicode (wide character) strings, using the specified locale.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-153"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-153"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-154">Сопоставляет одну строку с другой, выполняя указанный параметр преобразования.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-154">Maps one string to another, performing a specified transformation option.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-155"><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>жетстрингтипеа</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-155"><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-156">Извлекает сведения о символьном типе для символов в указанной исходной строке.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-156">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="8b7a2-157">Для каждого символа в строке функция задает один или несколько битов в соответствующем 16-разрядном элементе выходного массива.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-157">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="8b7a2-158">Каждый бит определяет заданный символьный тип, например, является ли символ буквой, цифрой или ни одной.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-158">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-159"><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>жетстрингтипикс</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-159"><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-160">Извлекает сведения о символьном типе для символов в указанной исходной строке.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-160">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="8b7a2-161">Для каждого символа в строке функция задает один или несколько битов в соответствующем 16-разрядном элементе выходного массива.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-161">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="8b7a2-162">Каждый бит определяет заданный символьный тип, например, является ли символ буквой, цифрой или ни одной.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-162">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span> <br/> <span data-ttu-id="8b7a2-163">В отличие от его близких родственников <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>жетстрингтипеа</strong></a> и <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>жетстрингтипев</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>жетстрингтипикс</strong></a> по-разному покрывает стандартное поведение с помощью параметра <strong> # define Юникода</strong> .</span><span class="sxs-lookup"><span data-stu-id="8b7a2-163">Unlike its close relatives <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> exhibits standard behavior through the use of the <strong>#define UNICODE</strong> switch.</span></span> <span data-ttu-id="8b7a2-164">Это рекомендуемая функция.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-164">It is the recommended function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-165"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>жетстрингтипев</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-165"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-166">Извлекает сведения о символьном типе для символов в указанной исходной строке.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-166">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="8b7a2-167">Для каждого символа в строке функция задает один или несколько битов в соответствующем 16-разрядном элементе выходного массива.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-167">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="8b7a2-168">Каждый бит определяет заданный символьный тип, например, является ли символ буквой, цифрой или ни одной.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-168">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-169"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>исчаралфа</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-169"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-170">Определяет, является ли символ буквенно-знакомым.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-170">Determines whether a character is an alphabetical character.</span></span> <span data-ttu-id="8b7a2-171">Это определение основано на семантике языка, выбранного пользователем во время установки или с помощью панели управления.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-171">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-172"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>исчаралфанумерик</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-172"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-173">Определяет, является ли символ алфавитным или цифровым символом.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-173">Determines whether a character is either an alphabetical or a numeric character.</span></span> <span data-ttu-id="8b7a2-174">Это определение основано на семантике языка, выбранного пользователем во время установки или с помощью панели управления.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-174">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-175"><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>исчарловер</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-175"><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-176">Определяет, является ли символ строчным.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-176">Determines whether a character is lowercase.</span></span> <span data-ttu-id="8b7a2-177">Это определение основано на семантике языка, выбранного пользователем во время установки или с помощью панели управления.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-177">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-178"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>исчаруппер</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-178"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-179">Определяет, является ли символ прописным.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-179">Determines whether a character is uppercase.</span></span> <span data-ttu-id="8b7a2-180">Это определение основано на семантике языка, выбранного пользователем во время установки или с помощью панели управления.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-180">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-181"><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>лоадстринг</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-181"><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-182">Загружает строковый ресурс из исполняемого файла, связанного с указанным модулем, копирует строку в буфер и добавляет завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-182">Loads a string resource from the executable file associated with a specified module, copies the string into a buffer, and appends a terminating NULL character.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-183"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>лстркат</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-183"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-184">Добавляет одну строку в другую.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-184">Appends one string to another.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-185"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>лстркмп</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-185"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-186">Сравнивает две символьные строки.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-186">Compares two character strings.</span></span> <span data-ttu-id="8b7a2-187">При сравнении учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-187">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-188"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>лстркмпи</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-188"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-189">Сравнивает две символьные строки.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-189">Compares two character strings.</span></span> <span data-ttu-id="8b7a2-190">Сравнение выполняется без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-190">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-191"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>лстркпи</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-191"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-192">Копирует строку в буфер.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-192">Copies a string to a buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-193"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>лстркпин</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-193"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-194">Копирует указанное число символов из исходной строки в буфер.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-194">Copies a specified number of characters from a source string into a buffer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-195"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-195"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-196">Определяет длину указанной строки (не включая завершающий нуль-символ).</span><span class="sxs-lookup"><span data-stu-id="8b7a2-196">Determines the length of the specified string (not including the terminating null character).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-197"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>оемточар</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-197"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-198">Преобразует строку из кодировки, определенной изготовителем оборудования, в строку в кодировке ANSI или в расширенных символах.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-198">Translates a string from the OEM-defined character set into either an ANSI or a wide-character string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-199"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>оемточарбуфф</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-199"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-200">Преобразует указанное число символов в строке из набора, заданного изготовителем оборудования, в строку в кодировке ANSI или в расширенных символах.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-200">Translates a specified number of characters in a string from the OEM-defined character set into either an ANSI or a wide-character string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b7a2-201"><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>вспринтф</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-201"><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-202">Записывает форматированные данные в указанный буфер.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-202">Writes formatted data to the specified buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b7a2-203"><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>ввспринтф</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b7a2-203"><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></span></span></td>
<td><span data-ttu-id="8b7a2-204">Записывает форматированные данные в указанный буфер с помощью указателя на список аргументов.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-204">Writes formatted data to the specified buffer using a pointer to a list of arguments.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="strsafe-functions"></a><span data-ttu-id="8b7a2-205">Функции стрсафе</span><span class="sxs-lookup"><span data-stu-id="8b7a2-205">Strsafe Functions</span></span>



| <span data-ttu-id="8b7a2-206">Имя</span><span class="sxs-lookup"><span data-stu-id="8b7a2-206">Name</span></span>                                             | <span data-ttu-id="8b7a2-207">Описание</span><span class="sxs-lookup"><span data-stu-id="8b7a2-207">Description</span></span>                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b7a2-208">**стрингкбкат**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-208">**StringCbCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | <span data-ttu-id="8b7a2-209">Сцепляет одну строку с другой строкой.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-209">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="8b7a2-210">**стрингкбкатекс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-210">**StringCbCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | <span data-ttu-id="8b7a2-211">Сцепляет одну строку с другой строкой.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-211">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="8b7a2-212">**стрингкбкатн**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-212">**StringCbCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | <span data-ttu-id="8b7a2-213">Сцепляет указанное число байтов из одной строки в другую.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-213">Concatenates the specified number of bytes from one string to another string.</span></span><br/>         |
| [<span data-ttu-id="8b7a2-214">**стрингкбкатнекс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-214">**StringCbCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | <span data-ttu-id="8b7a2-215">Сцепляет указанное число байтов из одной строки в другую.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-215">Concatenates the specified number of bytes from one string to another string.</span></span><br/>         |
| [<span data-ttu-id="8b7a2-216">**стрингкбкопи**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-216">**StringCbCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | <span data-ttu-id="8b7a2-217">Копирует одну строку в другую.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-217">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="8b7a2-218">**стрингкбкопекс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-218">**StringCbCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | <span data-ttu-id="8b7a2-219">Копирует одну строку в другую.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-219">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="8b7a2-220">**стрингкбкопин**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-220">**StringCbCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | <span data-ttu-id="8b7a2-221">Копирует указанное число байтов из одной строки в другую.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-221">Copies the specified number of bytes from one string to another.</span></span><br/>                      |
| [<span data-ttu-id="8b7a2-222">**стрингкбкопинекс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-222">**StringCbCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | <span data-ttu-id="8b7a2-223">Копирует указанное число байтов из одной строки в другую.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-223">Copies the specified number of bytes from one string to another.</span></span><br/>                      |
| [<span data-ttu-id="8b7a2-224">**стрингкбжетс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-224">**StringCbGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | <span data-ttu-id="8b7a2-225">Получает одну строку текста из stdin, вплоть до символа новой строки (" \\ n").</span><span class="sxs-lookup"><span data-stu-id="8b7a2-225">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="8b7a2-226">**стрингкбжетсекс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-226">**StringCbGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | <span data-ttu-id="8b7a2-227">Получает одну строку текста из stdin, вплоть до символа новой строки (" \\ n").</span><span class="sxs-lookup"><span data-stu-id="8b7a2-227">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="8b7a2-228">**стрингкбленгс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-228">**StringCbLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | <span data-ttu-id="8b7a2-229">Определяет, превышает ли строка указанную длину в байтах.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-229">Determines whether a string exceeds the specified length, in bytes.</span></span><br/>                   |
| [<span data-ttu-id="8b7a2-230">**стрингкбпринтф**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-230">**StringCbPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | <span data-ttu-id="8b7a2-231">Записывает форматированные данные в указанную строку.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-231">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="8b7a2-232">**стрингкбпринтфекс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-232">**StringCbPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | <span data-ttu-id="8b7a2-233">Записывает форматированные данные в указанную строку.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-233">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="8b7a2-234">**стрингкбвпринтф**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-234">**StringCbVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | <span data-ttu-id="8b7a2-235">Записывает форматированные данные в указанную строку, используя указатель на список аргументов.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-235">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="8b7a2-236">**стрингкбвпринтфекс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-236">**StringCbVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | <span data-ttu-id="8b7a2-237">Записывает форматированные данные в указанную строку, используя указатель на список аргументов.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-237">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="8b7a2-238">**стрингкчкат**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-238">**StringCchCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | <span data-ttu-id="8b7a2-239">Сцепляет одну строку с другой строкой.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-239">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="8b7a2-240">**стрингкчкатекс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-240">**StringCchCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | <span data-ttu-id="8b7a2-241">Сцепляет одну строку с другой строкой.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-241">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="8b7a2-242">**стрингкчкатн**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-242">**StringCchCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | <span data-ttu-id="8b7a2-243">Сцепляет указанное количество символов из одной строки в другую.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-243">Concatenates the specified number of characters from one string to another string.</span></span><br/>    |
| [<span data-ttu-id="8b7a2-244">**стрингкчкатнекс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-244">**StringCchCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | <span data-ttu-id="8b7a2-245">Сцепляет указанное количество символов из одной строки в другую.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-245">Concatenates the specified number of characters from one string to another string.</span></span><br/>    |
| [<span data-ttu-id="8b7a2-246">**стрингкчкопи**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-246">**StringCchCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | <span data-ttu-id="8b7a2-247">Копирует одну строку в другую.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-247">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="8b7a2-248">**стрингкчкопекс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-248">**StringCchCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | <span data-ttu-id="8b7a2-249">Копирует одну строку в другую.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-249">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="8b7a2-250">**стрингкчкопин**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-250">**StringCchCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | <span data-ttu-id="8b7a2-251">Копирует указанное число символов из одной строки в другую.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-251">Copies the specified number of characters from one string to another.</span></span><br/>                 |
| [<span data-ttu-id="8b7a2-252">**стрингкчкопинекс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-252">**StringCchCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | <span data-ttu-id="8b7a2-253">Копирует указанное число символов из одной строки в другую.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-253">Copies the specified number of characters from one string to another.</span></span><br/>                 |
| [<span data-ttu-id="8b7a2-254">**стрингкчжетс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-254">**StringCchGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | <span data-ttu-id="8b7a2-255">Получает одну строку текста из stdin, вплоть до символа новой строки (" \\ n").</span><span class="sxs-lookup"><span data-stu-id="8b7a2-255">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="8b7a2-256">**стрингкчжетсекс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-256">**StringCchGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | <span data-ttu-id="8b7a2-257">Получает одну строку текста из stdin, вплоть до символа новой строки (" \\ n").</span><span class="sxs-lookup"><span data-stu-id="8b7a2-257">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="8b7a2-258">**стрингкчленгс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-258">**StringCchLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | <span data-ttu-id="8b7a2-259">Определяет, превышает ли строка указанную длину в символах.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-259">Determines whether a string exceeds the specified length, in characters.</span></span><br/>              |
| [<span data-ttu-id="8b7a2-260">**стрингкчпринтф**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-260">**StringCchPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | <span data-ttu-id="8b7a2-261">Записывает форматированные данные в указанную строку.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-261">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="8b7a2-262">**стрингкчпринтфекс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-262">**StringCchPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | <span data-ttu-id="8b7a2-263">Записывает форматированные данные в указанную строку.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-263">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="8b7a2-264">**стрингкчвпринтф**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-264">**StringCchVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | <span data-ttu-id="8b7a2-265">Записывает форматированные данные в указанную строку, используя указатель на список аргументов.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-265">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="8b7a2-266">**стрингкчвпринтфекс**</span><span class="sxs-lookup"><span data-stu-id="8b7a2-266">**StringCchVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | <span data-ttu-id="8b7a2-267">Записывает форматированные данные в указанную строку, используя указатель на список аргументов.</span><span class="sxs-lookup"><span data-stu-id="8b7a2-267">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |



 

 

