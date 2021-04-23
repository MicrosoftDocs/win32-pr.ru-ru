---
title: Функции расширенного редактирования
description: Функции расширенного редактирования
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99f776b9a08095fa66645713e107a3d66920e80f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105651478"
---
# <a name="rich-edit-functions"></a><span data-ttu-id="abe6c-103">Функции расширенного редактирования</span><span class="sxs-lookup"><span data-stu-id="abe6c-103">Rich Edit Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="abe6c-104">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="abe6c-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="abe6c-105">Раздел</span><span class="sxs-lookup"><span data-stu-id="abe6c-105">Topic</span></span></th>
<th><span data-ttu-id="abe6c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="abe6c-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abe6c-107"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>аутокорректпрок</em></a></span><span class="sxs-lookup"><span data-stu-id="abe6c-107"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a></span></span><br/></td>
<td><span data-ttu-id="abe6c-108">Функция <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>аутокорректпрок</em></a> является определяемой приложением функцией обратного вызова, которая используется с сообщением <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="abe6c-108">The <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> function is an application-defined callback function that is used with the <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> message.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abe6c-109"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>едитстреамкаллбакк</em></a></span><span class="sxs-lookup"><span data-stu-id="abe6c-109"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a></span></span><br/></td>
<td><span data-ttu-id="abe6c-110">Функция <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>едитстреамкаллбакк</em></a> — это определяемая приложением функция обратного вызова, используемая с сообщениями <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> и <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="abe6c-110">The <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> function is an application defined callback function used with the <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> and <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> messages.</span></span> <span data-ttu-id="abe6c-111">Он используется для передачи потока данных в элемент управления Rich Edit или из него.</span><span class="sxs-lookup"><span data-stu-id="abe6c-111">It is used to transfer a stream of data into or out of a rich edit control.</span></span> <span data-ttu-id="abe6c-112">Тип <strong>едитстреамкаллбакк</strong> определяет указатель на эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="abe6c-112">The <strong>EDITSTREAMCALLBACK</strong> type defines a pointer to this callback function.</span></span> <span data-ttu-id="abe6c-113"><em>Едитстреамкаллбакк</em> — это заполнитель для имени определяемой приложением функции.</span><span class="sxs-lookup"><span data-stu-id="abe6c-113"><em>EditStreamCallback</em> is a placeholder for the application-defined function name.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abe6c-114"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>едитвордбреакпроцекс</em></a></span><span class="sxs-lookup"><span data-stu-id="abe6c-114"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a></span></span><br/></td>
<td><span data-ttu-id="abe6c-115">Функция <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>едитвордбреакпроцекс</em></a> — это определяемая приложением функция обратного вызова, используемая с сообщением <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="abe6c-115">The <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> function is an application defined callback function used with the <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> message.</span></span> <span data-ttu-id="abe6c-116">Он определяет индекс символа разрыва слова или класс символов и флаги разрыва слова для символов в указанном тексте.</span><span class="sxs-lookup"><span data-stu-id="abe6c-116">It determines the character index of the word break or the character class and word-break flags of the characters in the specified text.</span></span> <span data-ttu-id="abe6c-117">Тип <strong>едитвордбреакпроцекс</strong> определяет указатель на эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="abe6c-117">The <strong>EDITWORDBREAKPROCEX</strong> type defines a pointer to this callback function.</span></span> <span data-ttu-id="abe6c-118"><em>Едитвордбреакпроцекс</em> — это заполнитель для имени определяемой приложением функции.</span><span class="sxs-lookup"><span data-stu-id="abe6c-118"><em>EditWordBreakProcEx</em> is a placeholder for the application-defined function name.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abe6c-119"><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>жетмасалфанумерик</strong></a></span><span class="sxs-lookup"><span data-stu-id="abe6c-119"><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a></span></span><br/></td>
<td><span data-ttu-id="abe6c-120">Извлекает формат преобразования Юникода (UTF) — 32 математический алфавитный символ, соответствующий заданному базовому символу многоязыковой плоскости (BMP) и стилю математических символов.</span><span class="sxs-lookup"><span data-stu-id="abe6c-120">Retrieves the Unicode Transformation Format (UTF)-32 math alphanumeric character that corresponds to the specified Basic Multilingual Plane (BMP) character and math style.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abe6c-121"><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>жетмасалфанумериккоде</strong></a></span><span class="sxs-lookup"><span data-stu-id="abe6c-121"><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a></span></span><br/></td>
<td><span data-ttu-id="abe6c-122">Извлекает стиль математических символов и базовый код, соответствующий заданному замыкающему байту пары математических знаков.</span><span class="sxs-lookup"><span data-stu-id="abe6c-122">Retrieves the math style and the upright Basic Multilingual Plane (BMP) character code that corresponds to the specified trailing byte of a math surrogate pair.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abe6c-123"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>хифенатепрок</em></a></span><span class="sxs-lookup"><span data-stu-id="abe6c-123"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a></span></span><br/></td>
<td><span data-ttu-id="abe6c-124">Функция <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>хифенатепрок</em></a> — это определяемая приложением функция обратного вызова, используемая с сообщением <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="abe6c-124">The <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> function is an application defined callback function used with the <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> message.</span></span> <span data-ttu-id="abe6c-125">Он определяет, как расстановка переносов выполняется в элементе управления Microsoft Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="abe6c-125">It determines how hyphenation is done in a Microsoft Rich Edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abe6c-126"><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>масбуилддовн</strong></a></span><span class="sxs-lookup"><span data-stu-id="abe6c-126"><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a></span></span><br/></td>
<td><span data-ttu-id="abe6c-127">Преобразует встроенный математический, Ruby и другие встроенные объекты в указанном диапазоне в линейную форму.</span><span class="sxs-lookup"><span data-stu-id="abe6c-127">Translates the built-up math, ruby, and other inline objects in the specified range to linear form.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abe6c-128"><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>масбуилдуп</strong></a></span><span class="sxs-lookup"><span data-stu-id="abe6c-128"><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a></span></span><br/></td>
<td><span data-ttu-id="abe6c-129">Преобразует математические значения линейного формата в диапазоне в встроенную форму или изменяет текущую встроенную форму.</span><span class="sxs-lookup"><span data-stu-id="abe6c-129">Converts the linear-format math in a range to a built-up form, or modifies the current built-up form.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abe6c-130"><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>мастранслате</strong></a></span><span class="sxs-lookup"><span data-stu-id="abe6c-130"><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a></span></span><br/></td>
<td><span data-ttu-id="abe6c-131">Преобразует математические символы в указанном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="abe6c-131">Translates the math characters in the specified range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abe6c-132"><a href="reextendedregisterclass.md"><strong>рикстендедрегистеркласс</strong></a></span><span class="sxs-lookup"><span data-stu-id="abe6c-132"><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a></span></span><br/></td>
<td><span data-ttu-id="abe6c-133">Регистрирует два имени класса, REListBox20W и RECombobox20W, которые можно использовать для создания окон с широкими возможностями редактирования или ComboBox.</span><span class="sxs-lookup"><span data-stu-id="abe6c-133">Registers two class names, REListBox20W and RECombobox20W, that could be used to create Rich Edit listbox or combobox windows.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="abe6c-134">Предназначен для внутреннего использования; не рекомендуется для использования в приложениях.</span><span class="sxs-lookup"><span data-stu-id="abe6c-134">Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="abe6c-135">Эта функция может не поддерживаться в будущих версиях.</span><span class="sxs-lookup"><span data-stu-id="abe6c-135">This function may not be supported in future versions.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

