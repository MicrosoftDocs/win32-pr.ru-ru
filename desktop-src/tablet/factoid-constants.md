---
description: Определяет константные строковые значения, которые используются для повышения точности распознавания путем предоставления распознаватель контекстной информации.
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: Константы фактоид (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1353a4989ddfb5af3865788c0fa7fdc2d377f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542151"
---
# <a name="factoid-constants"></a><span data-ttu-id="e7184-103">Константы фактоид</span><span class="sxs-lookup"><span data-stu-id="e7184-103">Factoid Constants</span></span>

<span data-ttu-id="e7184-104">Определяет константные строковые значения, которые используются для повышения точности распознавания путем предоставления распознаватель контекстной информации.</span><span class="sxs-lookup"><span data-stu-id="e7184-104">Defines constant string values that are used to increase recognition accuracy by providing contextual information to the recognizer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e7184-105">Имя</span><span class="sxs-lookup"><span data-stu-id="e7184-105">Name</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e7184-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e7184-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl> <span data-ttu-id="e7184-107"><dt><strong>FACTOID_NONE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-107"><dt><strong>FACTOID_NONE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-108">Отключает все остальные фактоидс и словари.</span><span class="sxs-lookup"><span data-stu-id="e7184-108">Disables all other factoids and dictionaries.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl> <span data-ttu-id="e7184-109"><dt><strong>FACTOID_DEFAULT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-109"><dt> <strong>FACTOID_DEFAULT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-110">Значение по умолчанию для фактоидс для западных языков включает системный словарь, Пользовательский словарь, различные знаки препинания, а также веб-фактоид и Number.</span><span class="sxs-lookup"><span data-stu-id="e7184-110">The Default setting for factoids for western languages includes the system dictionary, user dictionary, various punctuations, and the Web and Number factoid.</span></span> <span data-ttu-id="e7184-111">Значение по умолчанию для фактоидс для восточно-азиатских языков включает все символы, поддерживаемые распознавателем.</span><span class="sxs-lookup"><span data-stu-id="e7184-111">The Default setting for factoids for East Asian languages includes all characters supported by the recognizer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl> <span data-ttu-id="e7184-112"><dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-112"><dt> <strong>FACTOID_SYSTEMDICTIONARY</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-113">Указывает распознавателю использовать только системный словарь.</span><span class="sxs-lookup"><span data-stu-id="e7184-113">Indicates to a recognizer to use the system dictionary only.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl> <span data-ttu-id="e7184-114"><dt><strong>FACTOID_WORDLIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-114"><dt> <strong>FACTOID_WORDLIST</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-115">Указывает распознавателю использовать программный список слов.</span><span class="sxs-lookup"><span data-stu-id="e7184-115">Indicates to a recognizer to use a programmatically-defined list of words.</span></span> <span data-ttu-id="e7184-116">Список слов определяется свойством <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>"список слов"</strong></a> объекта <a href="inkrecognizercontext-class.md"><strong>инкрекогнизерконтекст</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e7184-116">The list of words is defined by the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>WordList</strong></a> property of a <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e7184-117">Если строка добавляется в список слов, ее заглавные версии также неявно добавляются.</span><span class="sxs-lookup"><span data-stu-id="e7184-117">If a string is added to a word list, its capitalized versions are also implicitly added.</span></span> <span data-ttu-id="e7184-118">Например, добавление &quot; Hello &quot; неявно добавляет &quot; Hello &quot; и &quot; Hello &quot; .</span><span class="sxs-lookup"><span data-stu-id="e7184-118">For instance, adding &quot;hello&quot; implicitly adds &quot;Hello&quot; and &quot;HELLO&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl> <span data-ttu-id="e7184-119"><dt><strong>FACTOID_EMAIL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-119"><dt> <strong>FACTOID_EMAIL</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-120">Указывает распознавателю искать адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e7184-120">Indicates to a recognizer to look for an email address.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e7184-121">&quot; someone@example.com &quot; Для этого фактоид необходимо использовать полный адрес электронной почты, например.</span><span class="sxs-lookup"><span data-stu-id="e7184-121">A fully qualified email address, such as &quot;someone@example.com&quot;, must be used for this factoid.</span></span> <span data-ttu-id="e7184-122">Неизвестный псевдоним, такой как &quot; пользователь &quot; , не распознается.</span><span class="sxs-lookup"><span data-stu-id="e7184-122">A lone alias, such as &quot;someone&quot;, is not recognized.</span></span>
</blockquote>
<br/>
<pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl> <span data-ttu-id="e7184-123"><dt><strong>FACTOID_WEB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-123"><dt><strong>FACTOID_WEB</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-124">Указывает распознавателю искать веб-адрес.</span><span class="sxs-lookup"><span data-stu-id="e7184-124">Indicates to a recognizer to look for a Web address.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl> <span data-ttu-id="e7184-125"><dt><strong>FACTOID_ONECHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-125"><dt> <strong>FACTOID_ONECHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-126">Указывает распознавателю искать одиночный символ.</span><span class="sxs-lookup"><span data-stu-id="e7184-126">Indicates to a recognizer to look for a single character.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e7184-127">Этот фактоид ищет любой изолированный символ ANSI.</span><span class="sxs-lookup"><span data-stu-id="e7184-127">This factoid looks for any isolated ANSI character.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl> <span data-ttu-id="e7184-128"><dt><strong>FACTOID_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-128"><dt> <strong>FACTOID_NUMBER</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-129">Указывает распознавателю искать число.</span><span class="sxs-lookup"><span data-stu-id="e7184-129">Indicates to a recognizer to look for a number.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e7184-130">К числовым значениям относятся разделители, десятичные числа, порядковые номера и другие часто используемые числовые символы.</span><span class="sxs-lookup"><span data-stu-id="e7184-130">Numeric values include separators, decimals, ordinals and other commonly used numeric symbols.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl> <span data-ttu-id="e7184-131"><dt><strong>FACTOID_DIGIT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-131"><dt> <strong>FACTOID_DIGIT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-132">Указывает распознавателю искать одну цифру от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="e7184-132">Indicates to a recognizer to look for a single digit, 0 through 9.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl> <span data-ttu-id="e7184-133"><dt><strong>FACTOID_NUMBERSIMPLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-133"><dt> <strong>FACTOID_NUMBERSIMPLE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-134">Предоставляет распознаватель с простым числовым контекстом.</span><span class="sxs-lookup"><span data-stu-id="e7184-134">Provides a simple numeric context to a recognizer.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e7184-135">Эта фактоид не поддерживается в этой версии пакета SDK для планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="e7184-135">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl> <span data-ttu-id="e7184-136"><dt><strong>FACTOID_CURRENCY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-136"><dt> <strong>FACTOID_CURRENCY</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-137">Указывает распознавателю искать символы, обозначающие денежные значения.</span><span class="sxs-lookup"><span data-stu-id="e7184-137">Indicates to a recognizer to look for characters that denote a currency value.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl> <span data-ttu-id="e7184-138"><dt><strong>FACTOID_POSTALCODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-138"><dt> <strong>FACTOID_POSTALCODE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-139">Указывает распознавателю искать почтовые коды.</span><span class="sxs-lookup"><span data-stu-id="e7184-139">Indicates to a recognizer to look for postal codes.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>98112</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl> <span data-ttu-id="e7184-140"><dt><strong>FACTOID_PERCENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-140"><dt> <strong>FACTOID_PERCENT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-141">Указывает распознавателю искать проценты.</span><span class="sxs-lookup"><span data-stu-id="e7184-141">Indicates to a recognizer to look for percentages.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>87%</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl> <span data-ttu-id="e7184-142"><dt><strong>FACTOID_DATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-142"><dt> <strong>FACTOID_DATE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-143">Указывает распознавателю искать символы, которые обозначают дату.</span><span class="sxs-lookup"><span data-stu-id="e7184-143">Indicates to a recognizer to look for characters that denote a date.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>10/30/2001, &#39;01, 31/12, 12/99, 1999-2000</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl> <span data-ttu-id="e7184-144"><dt><strong>FACTOID_TIME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-144"><dt> <strong>FACTOID_TIME</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-145">Указывает распознавателю искать символы, которые обозначают время.</span><span class="sxs-lookup"><span data-stu-id="e7184-145">Indicates to a recognizer to look for characters that denote a time.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl> <span data-ttu-id="e7184-146"><dt><strong>FACTOID_TELEPHONE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-146"><dt> <strong>FACTOID_TELEPHONE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-147">Указывает распознавателю искать символы, которые обозначают номер телефона.</span><span class="sxs-lookup"><span data-stu-id="e7184-147">Indicates to a recognizer to look for characters that denote a telephone number.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl> <span data-ttu-id="e7184-148"><dt><strong>FACTOID_FILENAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-148"><dt> <strong>FACTOID_FILENAME</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-149">Указывает распознавателю искать символы, которые обозначают имя файла.</span><span class="sxs-lookup"><span data-stu-id="e7184-149">Indicates to a recognizer to look for characters that denote a file name.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl> <span data-ttu-id="e7184-150"><dt><strong>FACTOID_UPPERCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-150"><dt> <strong>FACTOID_UPPERCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-151">Указывает распознавателю искать один символ в верхнем регистре: от A до Z.</span><span class="sxs-lookup"><span data-stu-id="e7184-151">Indicates to a recognizer to look for a single uppercase character: A through Z.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl> <span data-ttu-id="e7184-152"><dt><strong>FACTOID_LOWERCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-152"><dt> <strong>FACTOID_LOWERCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-153">Указывает распознавателю искать один символ в нижнем регистре: от A до Z.</span><span class="sxs-lookup"><span data-stu-id="e7184-153">Indicates to a recognizer to look for a single lowercase character: A through Z.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e7184-154">Эта фактоид не поддерживается в этой версии пакета SDK для планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="e7184-154">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl> <span data-ttu-id="e7184-155"><dt><strong>FACTOID_PUNCCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-155"><dt> <strong>FACTOID_PUNCCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-156">Указывает распознавателю искать символы пунктуации.</span><span class="sxs-lookup"><span data-stu-id="e7184-156">Indicates to a recognizer to look for punctuation characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e7184-157">Эта фактоид не поддерживается в этой версии пакета SDK для планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="e7184-157">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl> <span data-ttu-id="e7184-158"><dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-158"><dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-159">Указывает распознавателю искать часто используемые символы кандзи, катакана и хирагана.</span><span class="sxs-lookup"><span data-stu-id="e7184-159">Indicates to a recognizer to look for commonly used Kanji, Katakana, and Hiragana characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl> <span data-ttu-id="e7184-160"><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-160"><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-161">Указывает распознавателю искать часто используемые символы упрощенного китайского письма.</span><span class="sxs-lookup"><span data-stu-id="e7184-161">Indicates to a recognizer to look for commonly used Simplified Chinese characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl> <span data-ttu-id="e7184-162"><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-162"><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-163">Указывает распознавателю искать часто используемые символы традиционного китайского языка.</span><span class="sxs-lookup"><span data-stu-id="e7184-163">Indicates to a recognizer to look for commonly used Traditional Chinese characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl> <span data-ttu-id="e7184-164"><dt><strong>FACTOID_KOREANCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-164"><dt><strong>FACTOID_KOREANCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-165">Указывает распознавателю искать часто используемые корейские символы.</span><span class="sxs-lookup"><span data-stu-id="e7184-165">Indicates to a recognizer to look for commonly used Korean characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl> <span data-ttu-id="e7184-166"><dt><strong>FACTOID_HIRAGANA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-166"><dt><strong>FACTOID_HIRAGANA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-167">Указывает распознавателю искать только символы хирагана.</span><span class="sxs-lookup"><span data-stu-id="e7184-167">Indicates to a recognizer to look for Hiragana characters only.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl> <span data-ttu-id="e7184-168"><dt><strong>FACTOID_KATAKANA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-168"><dt><strong>FACTOID_KATAKANA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-169">Указывает распознавателю искать только символы катакана.</span><span class="sxs-lookup"><span data-stu-id="e7184-169">Indicates to a recognizer to look for Katakana characters only.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl> <span data-ttu-id="e7184-170"><dt><strong>FACTOID_KANJICOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-170"><dt><strong>FACTOID_KANJICOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-171">Указывает распознавателю искать часто используемые символы кандзи.</span><span class="sxs-lookup"><span data-stu-id="e7184-171">Indicates to a recognizer to look for commonly used kanji characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl> <span data-ttu-id="e7184-172"><dt><strong>FACTOID_KANJIRARE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-172"><dt><strong>FACTOID_KANJIRARE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-173">Указывает распознавателю искать редко используемые символы кандзи.</span><span class="sxs-lookup"><span data-stu-id="e7184-173">Indicates to a recognizer to look for rarely used kanji characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e7184-174">Эта фактоид не поддерживается в этой версии пакета SDK для планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="e7184-174">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl> <span data-ttu-id="e7184-175"><dt><strong>FACTOID_BOPOMOFO</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-175"><dt><strong>FACTOID_BOPOMOFO</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-176">Указывает распознавателю искать бопомофо-символы.</span><span class="sxs-lookup"><span data-stu-id="e7184-176">Indicates to a recognizer to look for Bopomofo characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl> <span data-ttu-id="e7184-177"><dt><strong>FACTOID_JAMO</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-177"><dt><strong>FACTOID_JAMO</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-178">Указывает распознавателю искать символы азбуки хангыль-совместимости.</span><span class="sxs-lookup"><span data-stu-id="e7184-178">Indicates to a recognizer to look for Hangul compatibility Jamo characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl> <span data-ttu-id="e7184-179"><dt><strong>FACTOID_HANGULCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-179"><dt><strong>FACTOID_HANGULCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-180">Указывает распознавателю искать часто используемые символы хангыль.</span><span class="sxs-lookup"><span data-stu-id="e7184-180">Indicates to a recognizer to look for commonly used Hangul characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl> <span data-ttu-id="e7184-181"><dt><strong>FACTOID_HANGULRARE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e7184-181"><dt><strong>FACTOID_HANGULRARE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e7184-182">Указывает распознавателю искать редко используемые символы хангыль.</span><span class="sxs-lookup"><span data-stu-id="e7184-182">Indicates to a recognizer to look for rarely used Hangul characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e7184-183">Эта фактоид не поддерживается в этой версии пакета SDK для планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="e7184-183">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="e7184-184">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7184-184">Remarks</span></span>

<span data-ttu-id="e7184-185">В C++ вы можете получить доступ к этим константам в файле заголовка Мсинкаут. h, который находится в папке <systemdrive> : \\ Program Files \\ Microsoft Tablet PC Platform SDK \\ include, если пакет SDK установлен в расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e7184-185">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include directory if you installed the SDK in the default location.</span></span>

> [!Note]  
> <span data-ttu-id="e7184-186">Эти константы являются Вчарс, а не BSTRs.</span><span class="sxs-lookup"><span data-stu-id="e7184-186">These constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="e7184-187">Перед использованием в качестве параметров методов объекта их необходимо преобразовать в BSTRs.</span><span class="sxs-lookup"><span data-stu-id="e7184-187">They must be converted into BSTRs before use as parameters to object methods.</span></span> <span data-ttu-id="e7184-188">Дополнительные сведения о типе данных BSTR см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="e7184-188">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="e7184-189">Для распознавания символов латинского алфавита фактоидс, определенный в этом классе, предоставляется только для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="e7184-189">For recognizers of Latin script, the factoids defined in this class are provided for backward compatibility only.</span></span> <span data-ttu-id="e7184-190">Для новой разработки рекомендуется использовать значения, определенные в функции [сетинпутскопе](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) .</span><span class="sxs-lookup"><span data-stu-id="e7184-190">For new development, you are encouraged to use the values defined in the [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) function.</span></span> <span data-ttu-id="e7184-191">Дополнительные сведения см. [в разделе Использование контекста для повышения точности](using-context-to-improve-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="e7184-191">For details, see [Using Context to Improve Accuracy](using-context-to-improve-accuracy.md).</span></span>

 

<span data-ttu-id="e7184-192">Используйте эти идентификаторы, чтобы указать, какие фактоид должны использоваться во время распознавания.</span><span class="sxs-lookup"><span data-stu-id="e7184-192">Use these identifiers to specify which factoid should be used during recognition.</span></span>

<span data-ttu-id="e7184-193">Следующие сочетания фактоидс поддерживаются только для западных языков.</span><span class="sxs-lookup"><span data-stu-id="e7184-193">The following combinations of factoids are supported for western languages only.</span></span> <span data-ttu-id="e7184-194">Они не имеют отдельных определений, но являются допустимыми входными строковыми литералами для свойства [**фактоид**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) объектов, использующих фактоидс.</span><span class="sxs-lookup"><span data-stu-id="e7184-194">These do not have separate definitions, but are acceptable string literal inputs to the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of objects that use factoids.</span></span> <span data-ttu-id="e7184-195">Эти константы фактоид строк позволяют входным данным соответствовать любому из фактоидс в выражении.</span><span class="sxs-lookup"><span data-stu-id="e7184-195">These factoid string constants allow the input to match any of the factoids in the expression.</span></span>



| <span data-ttu-id="e7184-196">Сочетание</span><span class="sxs-lookup"><span data-stu-id="e7184-196">Combination</span></span>               | <span data-ttu-id="e7184-197">Определение</span><span class="sxs-lookup"><span data-stu-id="e7184-197">Definition</span></span>                                                |
|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e7184-198">"веб- \| список слов"</span><span class="sxs-lookup"><span data-stu-id="e7184-198">"WEB\|WORDLIST"</span></span>           | <span data-ttu-id="e7184-199">Веб-фактоид или список слов.</span><span class="sxs-lookup"><span data-stu-id="e7184-199">The Web factoid or the word list.</span></span>                         |
| <span data-ttu-id="e7184-200">" \| список слов электронной почты"</span><span class="sxs-lookup"><span data-stu-id="e7184-200">"EMAIL\|WORDLIST"</span></span>         | <span data-ttu-id="e7184-201">Фактоид электронной почты или список слов.</span><span class="sxs-lookup"><span data-stu-id="e7184-201">The Email factoid or the word list.</span></span>                       |
| <span data-ttu-id="e7184-202">"имя_файла \| Web \| список слов"</span><span class="sxs-lookup"><span data-stu-id="e7184-202">"FILENAME\|WEB\|WORDLIST"</span></span> | <span data-ttu-id="e7184-203">Имя файла фактоид или веб-фактоид или список слов.</span><span class="sxs-lookup"><span data-stu-id="e7184-203">The Filename factoid or the Web factoid or the word list.</span></span> |



 

<span data-ttu-id="e7184-204">Если используется элемент управления [InkEdit](inkedit-control-reference.md) , фактоид может быть задан как свойство элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e7184-204">If you are using the [InkEdit](inkedit-control-reference.md) control, the factoid can be set as a property of the control.</span></span>

<span data-ttu-id="e7184-205">При использовании API платформы Tablet PC можно задать свойство [**фактоид**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) для объекта [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e7184-205">If you are using the Tablet PC Platform APIs, you can set the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property on an [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

<span data-ttu-id="e7184-206">Кроме того, можно задать для этого свойства фактическую строковую константу фактоид.</span><span class="sxs-lookup"><span data-stu-id="e7184-206">Alternatively, you can set this property with the actual factoid string constant.</span></span>

> [!Note]  
> <span data-ttu-id="e7184-207">Константы строк фактоид чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="e7184-207">Factoid string constants are case sensitive.</span></span> <span data-ttu-id="e7184-208">Дополнительные сведения о фактоидс и способах их использования см. в разделе Использование контекста для [повышения точности](using-context-to-improve-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="e7184-208">For more information about factoids and how to use them, see Using Context to [Improve Accuracy](using-context-to-improve-accuracy.md).</span></span> <span data-ttu-id="e7184-209">Чтобы определить, доступен ли фактоид на определенном языке, см. раздел [Supported фактоидс from версии 1](supported-factoids-from-version-1.md).</span><span class="sxs-lookup"><span data-stu-id="e7184-209">To determine whether a factoid is available in a specific language, see [Supported Factoids from Version 1](supported-factoids-from-version-1.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e7184-210">Требования</span><span class="sxs-lookup"><span data-stu-id="e7184-210">Requirements</span></span>



| <span data-ttu-id="e7184-211">Требование</span><span class="sxs-lookup"><span data-stu-id="e7184-211">Requirement</span></span> | <span data-ttu-id="e7184-212">Значение</span><span class="sxs-lookup"><span data-stu-id="e7184-212">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7184-213">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7184-213">Minimum supported client</span></span><br/> | <span data-ttu-id="e7184-214">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e7184-214">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e7184-215">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7184-215">Minimum supported server</span></span><br/> | <span data-ttu-id="e7184-216">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e7184-216">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e7184-217">Header</span><span class="sxs-lookup"><span data-stu-id="e7184-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7184-218"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e7184-218"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7184-219">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7184-219">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7184-220">[**Класс фактоид свойства \[ инкрекогнизеконтекст\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="e7184-220">[**Factoid Property \[InkRecognizeContext Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)</span></span>
</dt> <dt>

<span data-ttu-id="e7184-221">[**Класс фактоид свойства \[ пенинпутпанел\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="e7184-221">[**Factoid Property \[PenInputPanel Class\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)</span></span>
</dt> <dt>

<span data-ttu-id="e7184-222">[**\[Элемент управления InkEdit свойства фактоид\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="e7184-222">[**Factoid Property \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)</span></span>
</dt> <dt>

[<span data-ttu-id="e7184-223">Использование контекста для повышения точности</span><span class="sxs-lookup"><span data-stu-id="e7184-223">Using Context to Improve Accuracy</span></span>](using-context-to-improve-accuracy.md)
</dt> <dt>

[<span data-ttu-id="e7184-224">Поддерживаемые Фактоидс из версии 1</span><span class="sxs-lookup"><span data-stu-id="e7184-224">Supported Factoids from Version 1</span></span>](supported-factoids-from-version-1.md)
</dt> </dl>

 

