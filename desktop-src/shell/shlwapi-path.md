---
description: В этом разделе описываются функции обработки пути оболочки Windows. Программные элементы, описанные в этой документации, экспортируются с помощью Shlwapi.dll и определяются в Shlwapi. h и Shlwapi. lib.
title: Функции обработки пути оболочки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8ed0a5e0f2e91a2e647af461ee6679a5542d28b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997903"
---
# <a name="shell-path-handling-functions"></a><span data-ttu-id="5f8a7-104">Функции обработки пути оболочки</span><span class="sxs-lookup"><span data-stu-id="5f8a7-104">Shell Path Handling Functions</span></span>

<span data-ttu-id="5f8a7-105">В этом разделе описываются функции обработки пути оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-105">This section describes the Windows Shell path handling functions.</span></span> <span data-ttu-id="5f8a7-106">Программные элементы, описанные в этой документации, экспортируются с помощью Shlwapi.dll и определяются в Shlwapi. h и Shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5f8a7-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="5f8a7-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5f8a7-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="5f8a7-108">Topic</span></span></th>
<th><span data-ttu-id="5f8a7-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5f8a7-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5f8a7-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>пасаддбаккслаш</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-111">Добавляет обратную косую черту в конец строки, чтобы создать правильный синтаксис для пути.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-111">Adds a backslash to the end of a string to create the correct syntax for a path.</span></span> <span data-ttu-id="5f8a7-112">Если в исходном пути уже есть обратная косая черта, обратная косая черта не добавляется.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-112">If the source path already has a trailing backslash, no backslash will be added.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5f8a7-113">Неправильное использование этой функции может привести к переполнению буфера.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-113">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="5f8a7-114">На своем месте рекомендуется использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>паскчаддбаккслаш</strong></a> или <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>паскчаддбаккслашекс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5f8a7-114">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>пасаддекстенсион</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-116">Добавляет расширение имени файла в строку пути.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-116">Adds a file name extension to a path string.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5f8a7-117">Неправильное использование этой функции может привести к переполнению буфера.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-117">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="5f8a7-118">Мы рекомендуем использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>паскчаддекстенсион</strong></a> на своем месте.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-118">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>пасаппенд</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-120">Добавляет один путь к концу другого.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-120">Appends one path to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5f8a7-121">Неправильное использование этой функции может привести к переполнению буфера.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-121">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="5f8a7-122">На своем месте рекомендуется использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>паскчаппенд</strong></a> или <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>паскчаппендекс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5f8a7-122">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>пасбуилдрут</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-124">Создает корневой путь из заданного номера диска.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-124">Creates a root path from a given drive number.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>пасканоникализе</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-126">Упрощает путь путем удаления элементов навигации, таких как &quot; . &quot; и &quot; .. &quot; , для создания прямого, правильно сформированного пути.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-126">Simplifies a path by removing navigation elements such as &quot;.&quot; and &quot;..&quot; to produce a direct, well-formed path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>паскомбине</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-128">Объединяет две строки, представляющие правильно сформированные пути, в один путь. также сцепляет все элементы относительного пути.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-128">Concatenates two strings that represent properly formed paths into one path; also concatenates any relative path elements.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5f8a7-129">Неправильное использование этой функции может привести к переполнению буфера.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-129">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="5f8a7-130">На своем месте рекомендуется использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>паскчкомбине</strong></a> или <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>паскчкомбиникс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5f8a7-130">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>паскоммонпрефикс</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-132">Сравнивает два пути, чтобы определить, имеют ли они общий префикс.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-132">Compares two paths to determine if they share a common prefix.</span></span> <span data-ttu-id="5f8a7-133">Префикс имеет один из следующих типов: &quot; C: \\ &quot; , &quot; ., &quot; . &quot; . &quot; , &quot; .. \\ &quot; .</span><span class="sxs-lookup"><span data-stu-id="5f8a7-133">A prefix is one of these types: &quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-134"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>паскомпактпас</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-134"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-135">Усекает путь к файлу в соответствии с заданной шириной в пикселях, заменяя компоненты пути многоточием.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-135">Truncates a file path to fit within a given pixel width by replacing path components with ellipses.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-136"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>паскомпактпасекс</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-136"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-137">Усекает путь, чтобы он поместился в определенное число символов, заменяя компоненты пути многоточием.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-137">Truncates a path to fit within a certain number of characters by replacing path components with ellipses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>паскреатефромурл</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-139">Преобразует URL-адрес файла в путь Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-139">Converts a file URL to a Microsoft MS-DOS path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-140"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>паскреатефромурлаллок</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-140"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-141">Создает путь из URL-адреса файла.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-141">Creates a path from a file URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-142"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>пасфиликсистс</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-142"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-143">Определяет, является ли допустимым путь к объекту файловой системы, например файлу или папке.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-143">Determines whether a path to a file system object such as a file or folder is valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>пасфиндекстенсион</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-145">Поиск расширения в пути.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-145">Searches a path for an extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-146"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>пасфиндфиленаме</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-146"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-147">Поиск имени файла в пути.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-147">Searches a path for a file name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-148"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>пасфинднексткомпонент</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-148"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-149">Анализирует путь и возвращает часть этого пути, следующую за первой обратной косой чертой.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-149">Parses a path and returns the portion of that path that follows the first backslash.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>пасфиндонпас</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-151">Выполняет поиск файла.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-151">Searches for a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-152"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>пасфиндсуффиксаррай</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-152"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-153">Определяет, имеет ли заданное имя файла один из списков суффиксов.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-153">Determines whether a given file name has one of a list of suffixes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-154"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>пасжетаргс</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-154"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-155">Находит аргументы командной строки в заданном пути.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-155">Finds the command line arguments within a given path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>пасжетчартипе</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-157">Определяет тип символа относительно пути.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-157">Determines the type of character in relation to a path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-158"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>пасжетдривенумбер</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-158"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-159">Ищет в пути букву диска в диапазоне от "A" до "Z" и возвращает соответствующий номер диска.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-159">Searches a path for a drive letter within the range of 'A' to 'Z' and returns the corresponding drive number.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-160"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>пасисконтенттипе</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-160"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-161">Определяет, соответствует ли зарегистрированный тип содержимого файла указанному типу содержимого.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-161">Determines if a file's registered content type matches the specified content type.</span></span> <span data-ttu-id="5f8a7-162">Эта функция получает тип содержимого для указанного типа файла и сравнивает эту строку с <em>псзконтенттипе</em>.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-162">This function obtains the content type for the specified file type and compares that string with the <em>pszContentType</em>.</span></span> <span data-ttu-id="5f8a7-163">Сравнение выполняется без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-163">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-164"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>пасисдиректори</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-164"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-165">Проверяет, является ли путь допустимым каталогом.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-165">Verifies that a path is a valid directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>пасисдиректоремпти</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-167">Определяет, является ли указанный путь пустым каталогом.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-167">Determines whether a specified path is an empty directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-168"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>пасисфилеспек</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-168"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-169">Выполняет поиск в пути любых символов, разделяющих путь (например, ":" или " \' ).</span><span class="sxs-lookup"><span data-stu-id="5f8a7-169">Searches a path for any path-delimiting characters (for example, ':' or '\' ).</span></span> <span data-ttu-id="5f8a7-170">Если нет символов, разделяющих пути, путь считается путем к файлу спецификации файла.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-170">If there are no path-delimiting characters present, the path is considered to be a File Spec path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-171"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>пасиштмлфиле</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-171"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-172">Определяет, является ли файл HTML-файлом.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-172">Determines if a file is an HTML file.</span></span> <span data-ttu-id="5f8a7-173">Определение устанавливается на основе типа содержимого, зарегистрированного для расширения файла.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-173">The determination is made based on the content type that is registered for the file's extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-174"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>пасислфнфилеспек</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-174"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-175">Определяет, имеет ли имя файла полный формат.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-175">Determines whether a file name is in long format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-176"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>пасиснетворкпас</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-176"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-177">Определяет, представляет ли строка пути сетевой ресурс.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-177">Determines whether a path string represents a network resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-178"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>пасиспрефикс</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-178"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-179">Выполняет поиск по пути, чтобы определить, содержит ли он допустимый префикс типа, переданного <em>псзпрефикс</em>.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-179">Searches a path to determine if it contains a valid prefix of the type passed by <em>pszPrefix</em>.</span></span> <span data-ttu-id="5f8a7-180">Префикс имеет один из следующих типов: &quot; C: \\ &quot; , &quot; ., &quot; . &quot; . &quot; , &quot; .. \\ &quot; .</span><span class="sxs-lookup"><span data-stu-id="5f8a7-180">A prefix is one of these types: &quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-181"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>пасисрелативе</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-181"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-182">Выполняет поиск по пути и определяет, является ли он относительным.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-182">Searches a path and determines if it is relative.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-183"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>пасисрут</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-183"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-184">Определяет, относится ли строка пути к корню тома.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-184">Determines whether a path string refers to the root of a volume.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-185"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>пасиссамерут</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-185"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-186">Сравнивает два пути, чтобы определить, имеют ли они общий корневой компонент.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-186">Compares two paths to determine if they have a common root component.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-187"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>пасиссистемфолдер</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-187"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-188">Определяет, содержит ли существующая папка атрибуты, которые делают ее системной папкой.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-188">Determines if an existing folder contains the attributes that make it a system folder.</span></span> <span data-ttu-id="5f8a7-189">Кроме того, эта функция указывает, должны ли определенные атрибуты определить папку как системную папку.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-189">Alternately, this function indicates if certain attributes qualify a folder to be a system folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-190"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>пасисунк</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-190"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-191">Определяет, является ли строка пути допустимым UNC-путем (в отличие от пути, основанного на букве диска).</span><span class="sxs-lookup"><span data-stu-id="5f8a7-191">Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-192"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>пасисунксервер</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-192"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-193">Определяет, является ли строка допустимым UNC-именем только для пути сервера.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-193">Determines if a string is a valid UNC for a server path only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>пасисунксервершаре</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-195">Определяет, является ли строка допустимым UNC-путем к общему ресурсу на \\ <em>сервере</em> \ <em></em>.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-195">Determines if a string is a valid UNC share path, \\<em>server</em>\<em>share</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>пасисурл</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-197">Проверяет заданную строку, чтобы определить, соответствует ли она допустимому формату URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-197">Tests a given string to determine if it conforms to a valid URL format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>пасмакепретти</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-199">Преобразует путь все прописные буквы в символы нижнего регистра, чтобы обеспечить единообразный внешний вид.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-199">Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-200"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>пасмакесистемфолдер</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-200"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-201">Предоставляет существующей папке правильные атрибуты для того, чтобы стать системной папкой.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-201">Gives an existing folder the proper attributes to become a system folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-202"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>пасматчспек</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-202"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-203">Выполняет поиск строки, используя тип совпадения с подстановочным знаком MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-203">Searches a string using a MS-DOS wildcard match type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>пасматчспецекс</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-205">Сопоставляет имя файла из пути с одним или несколькими шаблонами имен файлов.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-205">Matches a file name from a path against one or more file name patterns.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-206"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>паспарсеиконлокатион</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-206"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-207">Анализирует строку расположения файла, содержащую расположение файла и индекс значка, и возвращает отдельные значения.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-207">Parses a file location string that contains a file location and icon index, and returns separate values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-208"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>паскуотеспацес</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-208"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-209">Поиск пробелов в пути.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-209">Searches a path for spaces.</span></span> <span data-ttu-id="5f8a7-210">Если найдены пробелы, весь путь заключается в кавычки.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-210">If spaces are found, the entire path is enclosed in quotation marks.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>пасрелативепасто</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-212">Создает относительный путь от одного файла или папки к другому.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-212">Creates a relative path from one file or folder to another.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>пасремовеаргс</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-214">Удаляет все аргументы из заданного пути.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-214">Removes any arguments from a given path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-215"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>пасремовебаккслаш</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-215"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-216">Удаляет замыкающую обратную косую черту из заданного пути.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-216">Removes the trailing backslash from a given path.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5f8a7-217">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-217">This function is deprecated.</span></span> <span data-ttu-id="5f8a7-218">Мы рекомендуем использовать функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>паскчремовебаккслаш</strong></a> или <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>паскчремовебаккслашекс</strong></a> на своем месте.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-218">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-219"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>пасремовебланкс</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-219"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-220">Удаляет все начальные и конечные пробелы из строки.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-220">Removes all leading and trailing spaces from a string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-221"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>пасремовикстенсион</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-221"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-222">Удаляет расширение имени файла из пути, если он имеется.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-222">Removes the file name extension from a path, if one is present.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5f8a7-223">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-223">This function is deprecated.</span></span> <span data-ttu-id="5f8a7-224">Мы рекомендуем использовать <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>паскчремовикстенсион</strong></a> на своем месте.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-224">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-225"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>пасремовефилеспек</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-225"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-226">Удаляет завершающее имя файла и обратную косую черту из пути, если они есть.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-226">Removes the trailing file name and backslash from a path, if they are present.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5f8a7-227">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-227">This function is deprecated.</span></span> <span data-ttu-id="5f8a7-228">Мы рекомендуем использовать функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>паскчремовефилеспек</strong></a> на своем месте.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-228">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-229"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>пасренамикстенсион</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-229"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-230">Заменяет расширение имени файла новым расширением.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-230">Replaces the extension of a file name with a new extension.</span></span> <span data-ttu-id="5f8a7-231">Если имя файла не содержит расширение, расширение будет присоединено к концу строки.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-231">If the file name does not contain an extension, the extension will be attached to the end of the string.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5f8a7-232">Неправильное использование этой функции может привести к переполнению буфера.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-232">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="5f8a7-233">Мы рекомендуем использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>паскчренамикстенсион</strong></a> на своем месте.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-233">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>пассеарчандкуалифи</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-235">Определяет, является ли данный путь правильно отформатированным и полным.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-235">Determines if a given path is correctly formatted and fully qualified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-236"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>пассетдлгитемпас</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-236"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-237">Задает текст дочернего элемента управления в окне или диалоговом окне с помощью <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>паскомпактпас</strong></a> , чтобы гарантировать, что путь умещается в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-237">Sets the text of a child control in a window or dialog box, using <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> to ensure the path fits in the control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-238"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>пасскипрут</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-238"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-239">Извлекает указатель на первый символ в пути после буквы диска или UNC-сервера или пути к общей папке.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-239">Retrieves a pointer to the first character in a path following the drive letter or UNC server/share path elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-240"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>пасстриппас</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-240"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-241">Удаляет часть пути к полному пути и файлу.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-241">Removes the path portion of a fully qualified path and file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>пасстрипторут</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-243">Удаляет все элементы File и Directory в пути, за исключением корневой информации.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-243">Removes all file and directory elements in a path except for the root information.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5f8a7-244">Неправильное использование этой функции может привести к переполнению буфера.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-244">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="5f8a7-245">Мы рекомендуем использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>паскчстрипторут</strong></a> на своем месте.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-245">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-246"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>пасундекорате</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-246"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-247">Удаляет Оформление из строки пути.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-247">Removes the decoration from a path string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>пасунекспанденвстрингс</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-249">Заменяет определенные имена папок в полном пути на соответствующую строку среды.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-249">Replaces certain folder names in a fully qualified path with their associated environment string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>пасунмакесистемфолдер</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-251">Удаляет атрибуты из папки, сделав ее системной папкой.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-251">Removes the attributes from a folder that make it a system folder.</span></span> <span data-ttu-id="5f8a7-252">На самом деле эта папка должна существовать в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-252">This folder must actually exist in the file system.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-253"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>пасункуотеспацес</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-253"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-254">Удаляет кавычки с начала и с конца пути.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-254">Removes quotes from the beginning and end of a path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-255"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>шскипжунктион</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-255"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-256">Проверяет контекст привязки, чтобы проверить, является ли он ненадежным для привязки к конкретному объекту компонента.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-256">Checks a bind context to see if it is safe to bind to a particular component object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-257"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>урлапплисчеме</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-257"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-258">Определяет схему для указанной строки URL-адреса и возвращает строку с соответствующим префиксом.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-258">Determines a scheme for a specified URL string, and returns a string with an appropriate prefix.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-259"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>урлканоникализе</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-259"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-260">Преобразует строку URL-адреса в каноническую форму.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-260">Converts a URL string into canonical form.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-261"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>урлкомбине</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-261"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-262">При указании с относительным URL-адресом и его базой, возвращает URL-адрес в канонической форме.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-262">When provided with a relative URL and its base, returns a URL in canonical form.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-263"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>урлкомпаре</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-263"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-264">Выполняет сравнение с учетом регистра двух строк URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-264">Makes a case-sensitive comparison of two URL strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-265"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>урлкреатефромпас</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-265"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-266">Преобразует путь MS-DOS в канонический URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-266">Converts a MS-DOS path to a canonicalized URL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-267"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>урлескапе</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-267"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-268">Преобразует символы или суррогатные пары в URL-адресе, который может быть изменен во время передачи через Интернет ( &quot; ненадежные &quot; символы) в соответствующие управляющие последовательности.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-268">Converts characters or surrogate pairs in a URL that might be altered during transport across the Internet (&quot;unsafe&quot; characters) into their corresponding escape sequences.</span></span> <span data-ttu-id="5f8a7-269">Суррогатные пары — это символы между U + 10000 и U + 10FFFF (в UTF-32) или между DC00 и DFFF (в UTF-16).</span><span class="sxs-lookup"><span data-stu-id="5f8a7-269">Surrogate pairs are characters between U+10000 to U+10FFFF (in UTF-32) or between DC00 to DFFF (in UTF-16).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-270"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>урлескапеспацес</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-270"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-271">Макрос, который преобразует символы пробела в соответствующую escape-последовательность.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-271">A macro that converts space characters into their corresponding escape sequence.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-272"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>урлжетлокатион</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-272"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-273">Извлекает расположение из URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-273">Retrieves the location from a URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-274"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>урлжетпарт</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-274"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-275">Принимает строку URL-адреса и возвращает указанную часть этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-275">Accepts a URL string and returns a specified part of that URL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-276"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>урлхаш</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-276"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-277">Хэширует строку URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-277">Hashes a URL string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-278"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>урлис</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-278"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-279">Проверяет, имеет ли URL-адрес указанный тип.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-279">Tests whether a URL is a specified type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-280"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>урлисфилеурл</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-280"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-281">Проверяет URL-адрес, чтобы определить, является ли он URL-адресом файла.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-281">Tests a URL to determine if it is a file URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-282"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>урлиснохистори</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-282"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-283">Возвращает значение, указывающее, является ли URL-адрес URL, который обычно не включается в журнал навигации.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-283">Returns whether a URL is a URL that browsers typically do not include in navigation history.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-284"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>урлисопакуе</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-284"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-285">Возвращает значение, указывающее, является ли URL-адрес непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-285">Returns whether a URL is opaque.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f8a7-286"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>урлунескапе</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-286"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-287">Преобразует escape-последовательности обратно в обычные символы.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-287">Converts escape sequences back into ordinary characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f8a7-288"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>урлунескапеинплаце</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f8a7-288"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f8a7-289">Преобразует escape-последовательности обратно в обычные символы и перезаписывает исходную строку.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-289">Converts escape sequences back into ordinary characters and overwrites the original string.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




