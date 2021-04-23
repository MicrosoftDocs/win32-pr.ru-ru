---
title: Вызов WDS из командной строки
description: Вы можете запустить пользовательский интерфейс Microsoft Windows Desktop Search (WDS) с конкретным фильтром, хранилищем и запросом из другого приложения или веб-страницы, использующей объект модуля поддержки браузера (BHO), с помощью синтаксиса командной строки windowssearch.exe.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efae7aebc13f578e9c5c32542b451d3600a93a2b
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "103789162"
---
# <a name="calling-wds-from-the-command-line"></a><span data-ttu-id="e66d8-103">Вызов WDS из командной строки</span><span class="sxs-lookup"><span data-stu-id="e66d8-103">Calling WDS from the Command Line</span></span>

> [!NOTE]
> <span data-ttu-id="e66d8-104">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e66d8-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="e66d8-105">В более поздних выпусках используйте вместо этого [Поиск Windows](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="e66d8-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="e66d8-106">Вы можете запустить пользовательский интерфейс Microsoft Windows Desktop Search (WDS) с конкретным фильтром, хранилищем и запросом из другого приложения или веб-страницы, использующей объект модуля поддержки браузера (BHO), с помощью синтаксиса командной строки windowssearch.exe.</span><span class="sxs-lookup"><span data-stu-id="e66d8-106">You can launch the Microsoft Windows Desktop Search (WDS) user interface with a specific filter, store, and query from another application or a webpage that uses the Browser Helper Object (BHO) by using the windowssearch.exe command line syntax.</span></span> <span data-ttu-id="e66d8-107">При вызове WDS из командной строки сведения о действиях пользователя или выборе в окне WDS не возвращаются вызывающему приложению или веб-странице.</span><span class="sxs-lookup"><span data-stu-id="e66d8-107">When calling WDS from the command line, no information about the user's actions or selection in the WDS window is returned to the calling application or webpage.</span></span>

<span data-ttu-id="e66d8-108">Путь установки WDS указывается в параметре реестра InstallDir в разделе HKEY_LOCAL_MACHINE \\ Software \\ Microsoft \\ Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="e66d8-108">The WDS installation path is specified in the InstallDir registry setting under HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows Desktop Search.</span></span> <span data-ttu-id="e66d8-109">Путь по умолчанию, по которому устанавливается windowssearch.exe, — это Program Files \\ Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="e66d8-109">The default path that windowssearch.exe is installed to is Program Files\\Windows Desktop Search.</span></span>

## <a name="command-line-syntax"></a><span data-ttu-id="e66d8-110">Синтаксис командной строки</span><span class="sxs-lookup"><span data-stu-id="e66d8-110">Command Line Syntax</span></span>

<span data-ttu-id="e66d8-111">Следующий синтаксис применяется к интерфейсу командной строки Windows Desktop Search 2. x.</span><span class="sxs-lookup"><span data-stu-id="e66d8-111">The following syntax applies to the Windows Desktop Search 2.x command-line interface.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e66d8-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e66d8-112">Options</span></span></th>
<th><span data-ttu-id="e66d8-113">Параметр</span><span class="sxs-lookup"><span data-stu-id="e66d8-113">Parameter</span></span></th>
<th><span data-ttu-id="e66d8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e66d8-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e66d8-115">/стартуп</span><span class="sxs-lookup"><span data-stu-id="e66d8-115">/startup</span></span></td>

<td><span data-ttu-id="e66d8-116">Инициализирует панель поиска Windows</span><span class="sxs-lookup"><span data-stu-id="e66d8-116">Initializes Windows Desktop Search</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e66d8-117">/индекснов</span><span class="sxs-lookup"><span data-stu-id="e66d8-117">/indexnow</span></span></td>

<td><span data-ttu-id="e66d8-118">Отключает отключать индексацию и повторно сканирует все расположения индексов</span><span class="sxs-lookup"><span data-stu-id="e66d8-118">Turns off indexing back-off and rescans all index locations</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e66d8-119">/шовстатус</span><span class="sxs-lookup"><span data-stu-id="e66d8-119">/showstatus</span></span></td>

<td><span data-ttu-id="e66d8-120">Отображение окна состояния индексирования</span><span class="sxs-lookup"><span data-stu-id="e66d8-120">Shows the indexing status window</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e66d8-121">/лаунчсеарчвиндов или/УРЛ</span><span class="sxs-lookup"><span data-stu-id="e66d8-121">/launchsearchwindow or /url</span></span></td>

<td><span data-ttu-id="e66d8-122">Открывает окно WDS с пустым запросом</span><span class="sxs-lookup"><span data-stu-id="e66d8-122">Opens a WDS window with an empty query</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e66d8-123">/урл</span><span class="sxs-lookup"><span data-stu-id="e66d8-123">/url</span></span></td>
<td><span data-ttu-id="e66d8-124">Поиск: [магазин | отображение | запрос] строка запроса</span><span class="sxs-lookup"><span data-stu-id="e66d8-124">search:[store|show|query] query string</span></span></td>
<td><span data-ttu-id="e66d8-125">Открывает окно WDS с запросом и фильтром на основе следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="e66d8-125">Opens a WDS window with a query and filter based on the following parameters:</span></span>
<ul>
<li><p><span data-ttu-id="e66d8-126">хранилище — указывает источник данных для запроса: файлы, Outlook, аутлукекспресс.</span><span class="sxs-lookup"><span data-stu-id="e66d8-126">store - Specifies the data source to query: files, outlook, outlookexpress.</span></span> <span data-ttu-id="e66d8-127">Если не указано, будет выполнен поиск по всем хранилищам.</span><span class="sxs-lookup"><span data-stu-id="e66d8-127">If not specified all stores will be searched.</span></span> <br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="e66d8-128">Хотя расширенный синтаксис запросов поддерживает ссылку на Microsoft Outlook как OE, параметр Store в командной строке должен иметь значение "аутлукекспресс".</span><span class="sxs-lookup"><span data-stu-id="e66d8-128">While Advanced Query Syntax supports referencing Microsoft Outlook as 'oe', the store parameter on the command line must be 'outlookexpress'.</span></span>
</blockquote>
<p><br/></p></li>
<li><p><span data-ttu-id="e66d8-129">показывать — указывает наблюдаемый тип возвращаемых результатов.</span><span class="sxs-lookup"><span data-stu-id="e66d8-129">show - Specifies which perceived type of results to return.</span></span> <span data-ttu-id="e66d8-130">Полный список типов см. в разделе <a href="-search-2x-wds-perceivedtype.md">наблюдаемые типы</a> .</span><span class="sxs-lookup"><span data-stu-id="e66d8-130">See <a href="-search-2x-wds-perceivedtype.md">Perceived Types</a> for a complete list of types.</span></span> <span data-ttu-id="e66d8-131">Если не указано, будут возвращены все типы.</span><span class="sxs-lookup"><span data-stu-id="e66d8-131">If not specified, all types will be returned.</span></span> <br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="e66d8-132">Существует три различия между значениями воспринимаемого типа и значениями для представления.</span><span class="sxs-lookup"><span data-stu-id="e66d8-132">There are three differences between the perceived type values and the values for show.</span></span> <span data-ttu-id="e66d8-133">Для <code>show</code> Используйте "Documents" вместо "doc", "Pictures" вместо "pics" и "текстдокументс" вместо "Text".</span><span class="sxs-lookup"><span data-stu-id="e66d8-133">For <code>show</code>, use 'documents' instead of 'doc', 'pictures' instead of 'pics', and 'textdocuments' instead of 'text'.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="e66d8-134">запрос — задает условие поиска.</span><span class="sxs-lookup"><span data-stu-id="e66d8-134">query - Specifies the search criteria.</span></span> <span data-ttu-id="e66d8-135">Это значение поддерживает <a href="-search-2x-wds-aqsreference.md">Расширенные параметры синтаксиса запросов</a> для уточнения результатов.</span><span class="sxs-lookup"><span data-stu-id="e66d8-135">This value supports <a href="-search-2x-wds-aqsreference.md">Advanced Query Syntax</a> parameters to refine the results.</span></span> <span data-ttu-id="e66d8-136">Параметр запроса должен быть последним параметром в URL-адресе.</span><span class="sxs-lookup"><span data-stu-id="e66d8-136">The query parameter must be the last parameter in the URL.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a><span data-ttu-id="e66d8-137">Пример</span><span class="sxs-lookup"><span data-stu-id="e66d8-137">Example</span></span>

<span data-ttu-id="e66d8-138">Например, для поиска изображений по всем файлам, соответствующим критерию "фоновый рисунок", используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e66d8-138">For example, to search all files for pictures matching the criteria 'wallpaper' use the following command:</span></span>

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a><span data-ttu-id="e66d8-139">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e66d8-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e66d8-140">**Reference**</span><span class="sxs-lookup"><span data-stu-id="e66d8-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e66d8-141">Синтаксис расширенных запросов</span><span class="sxs-lookup"><span data-stu-id="e66d8-141">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="e66d8-142">Наблюдаемые типы</span><span class="sxs-lookup"><span data-stu-id="e66d8-142">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="e66d8-143">Вызов WDS из веб-страниц</span><span class="sxs-lookup"><span data-stu-id="e66d8-143">Calling WDS from Web Pages</span></span>](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





