---
description: Узнайте, как использовать аргумент в поиске Windows в качестве средства управления областью поиска.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Аргумент с обопараметром (Поиск Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f56287c7182c0cf370250d53075a1c951ddf28b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403737"
---
# <a name="crumb-argument-windows-search"></a><span data-ttu-id="e55d8-103">Аргумент с обопараметром (Поиск Windows)</span><span class="sxs-lookup"><span data-stu-id="e55d8-103">CRUMB Argument (Windows Search)</span></span>

<span data-ttu-id="e55d8-104">`crumb`Аргумент поддерживает полные инструкции расширенного синтаксиса запросов (АКС) и особенно полезен в качестве средства управления областью поиска.</span><span class="sxs-lookup"><span data-stu-id="e55d8-104">The `crumb` argument supports full Advanced Query Syntax (AQS) statements and is especially useful as a means of controlling the scope of a search.</span></span> <span data-ttu-id="e55d8-105">Помимо АКС ементс, `crumb` аргумент может принимать Специальный `location` параметр в Windows Vista и `kind` `store` Параметры в XP, как описано далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="e55d8-105">In addition to AQS ements, the `crumb` argument can take a special `location` parameter on Windows Vista and `kind` and `store` parameters on XP, as described later in this topic.</span></span>

<span data-ttu-id="e55d8-106">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e55d8-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="e55d8-107">Синтаксис с повышей</span><span class="sxs-lookup"><span data-stu-id="e55d8-107">Crumb Syntax</span></span>](#crumb-syntax)
    -   [<span data-ttu-id="e55d8-108">Общие примеры</span><span class="sxs-lookup"><span data-stu-id="e55d8-108">General Examples</span></span>](#general-examples)
-   [<span data-ttu-id="e55d8-109">Использование инструкции with Vista (расположение)</span><span class="sxs-lookup"><span data-stu-id="e55d8-109">Using crumb with Vista (location)</span></span>](#using-crumb-with-vista-location)
    -   [<span data-ttu-id="e55d8-110">Примеры для Vista</span><span class="sxs-lookup"><span data-stu-id="e55d8-110">Vista Examples</span></span>](#vista-examples)
    -   [<span data-ttu-id="e55d8-111">Константы для общих папок</span><span class="sxs-lookup"><span data-stu-id="e55d8-111">Constants for Common Folders</span></span>](#constants-for-common-folders)
-   [<span data-ttu-id="e55d8-112">Использование инструкции with Windows XP (тип и магазин)</span><span class="sxs-lookup"><span data-stu-id="e55d8-112">Using crumb with Windows XP (kind and store)</span></span>](#using-crumb-with-windows-xp-kind-and-store)
    -   [<span data-ttu-id="e55d8-113">Примеры для XP</span><span class="sxs-lookup"><span data-stu-id="e55d8-113">XP Examples</span></span>](#xp-examples)
-   [<span data-ttu-id="e55d8-114">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e55d8-114">Related topics</span></span>](#related-topics)

 

## <a name="crumb-syntax"></a><span data-ttu-id="e55d8-115">Синтаксис с повышей</span><span class="sxs-lookup"><span data-stu-id="e55d8-115">Crumb Syntax</span></span>

<span data-ttu-id="e55d8-116">Синтаксис с обозначением выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e55d8-116">The crumb syntax is as follows:</span></span>


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



<span data-ttu-id="e55d8-117"><column>Часть является любым свойством в системе свойств, а свойство</span><span class="sxs-lookup"><span data-stu-id="e55d8-117">The <column> portion is any property in the property system, and the</span></span> <value> <span data-ttu-id="e55d8-118">часть является допустимым значением для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="e55d8-118">portion is a valid value for that property.</span></span> <span data-ttu-id="e55d8-119"><label>Часть является необязательным псевдонимом для свойства, которое отображается как указание пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e55d8-119">The <label> portion is an optional alias for the property that displays as a user interface hint.</span></span>

### <a name="general-examples"></a><span data-ttu-id="e55d8-120">Общие примеры</span><span class="sxs-lookup"><span data-stu-id="e55d8-120">General Examples</span></span>


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a><span data-ttu-id="e55d8-121">Использование инструкции with Vista (расположение)</span><span class="sxs-lookup"><span data-stu-id="e55d8-121">Using crumb with Vista (location)</span></span>

<span data-ttu-id="e55d8-122">В параметре WHERE Windows Vista поддерживает полную АКС, а также `location` свойство, которое имеет специальную реализацию, доступную только в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e55d8-122">In the crumb parameter, Windows Vista supports full AQS and also the `location` property, which has a special implementation available only on Windows Vista.</span></span> <span data-ttu-id="e55d8-123">Можно использовать либо строку АКС `location` , либо свойство в одном параметре, но не оба.</span><span class="sxs-lookup"><span data-stu-id="e55d8-123">You can use either an AQS string or the `location` property within a single crumb parameter, but not both.</span></span> <span data-ttu-id="e55d8-124">Если параметр ссылки содержит АКС, все остальное в этом параметре не учитывается.</span><span class="sxs-lookup"><span data-stu-id="e55d8-124">If the crumb parameter includes AQS, everything else in that crumb parameter is ignored.</span></span>

<span data-ttu-id="e55d8-125">`location`Свойство позволяет указать путь для поиска.</span><span class="sxs-lookup"><span data-stu-id="e55d8-125">The `location` property enables you to specify a path to search.</span></span> <span data-ttu-id="e55d8-126">Windows Vista может обходить индексатор и просматривать каталог напрямую, если расположение находится за пределами области обхода индексатора.</span><span class="sxs-lookup"><span data-stu-id="e55d8-126">Windows Vista can bypass the Indexer and traverse the directory directly if the location is outside the Indexer's crawl scope.</span></span> <span data-ttu-id="e55d8-127">Следовательно, эти операции поиска могут выполняться медленнее, чем поиск, использующий индексатор.</span><span class="sxs-lookup"><span data-stu-id="e55d8-127">Consequently, these searches may be slower than searches that use the Indexer.</span></span>

<span data-ttu-id="e55d8-128">При указании `location` свойства поддерживаются два дополнительных параметра и необязательно:</span><span class="sxs-lookup"><span data-stu-id="e55d8-128">When you specify a `location` property, two additional parameters are supported and optional:</span></span>



| <span data-ttu-id="e55d8-129">Параметр</span><span class="sxs-lookup"><span data-stu-id="e55d8-129">Parameter</span></span> | <span data-ttu-id="e55d8-130">Значения</span><span class="sxs-lookup"><span data-stu-id="e55d8-130">Values</span></span>                  | <span data-ttu-id="e55d8-131">Описание</span><span class="sxs-lookup"><span data-stu-id="e55d8-131">Description</span></span>                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e55d8-132">включения</span><span class="sxs-lookup"><span data-stu-id="e55d8-132">inclusion</span></span> | <span data-ttu-id="e55d8-133">включить, исключить</span><span class="sxs-lookup"><span data-stu-id="e55d8-133">include, exclude</span></span>        | <span data-ttu-id="e55d8-134">Указывает, должен ли запрос включать или исключать элементы из этого пути.</span><span class="sxs-lookup"><span data-stu-id="e55d8-134">Specifies whether the query should include or exclude items from that path.</span></span> <span data-ttu-id="e55d8-135">По умолчанию используется "include".</span><span class="sxs-lookup"><span data-stu-id="e55d8-135">"Include" is the default.</span></span> <span data-ttu-id="e55d8-136">Windows Vista не поддерживает исключения без включения.</span><span class="sxs-lookup"><span data-stu-id="e55d8-136">Windows Vista does not support exclusions without inclusions.</span></span> <span data-ttu-id="e55d8-137">(См. пример)</span><span class="sxs-lookup"><span data-stu-id="e55d8-137">(See example)</span></span> |
| <span data-ttu-id="e55d8-138">рекурсию;</span><span class="sxs-lookup"><span data-stu-id="e55d8-138">recursion</span></span> | <span data-ttu-id="e55d8-139">рекурсивный, нерекурсивный</span><span class="sxs-lookup"><span data-stu-id="e55d8-139">recursive, nonrecursive</span></span> | <span data-ttu-id="e55d8-140">Указывает, должен ли поиск выполнять рекурсию всех вложенных папок, начиная со значения, определенного в расположении:</span><span class="sxs-lookup"><span data-stu-id="e55d8-140">Specifies whether the search should recurse all subfolders starting from the value defined in the location:</span></span><value><span data-ttu-id="e55d8-141">.</span><span class="sxs-lookup"><span data-stu-id="e55d8-141">.</span></span> <span data-ttu-id="e55d8-142">"Recursive" — значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e55d8-142">"Recursive" is the default.</span></span>                             |



 

<span data-ttu-id="e55d8-143">Чтобы ограничить область поиска с помощью протокола Search-MS:, у вас есть различные параметры в зависимости от целевого объекта области.</span><span class="sxs-lookup"><span data-stu-id="e55d8-143">To scope a search using the search-ms: protocol, you have different options depending on the target of the scope.</span></span>

<span data-ttu-id="e55d8-144">Папка на локальном компьютере:</span><span class="sxs-lookup"><span data-stu-id="e55d8-144">Folder on a local machine:</span></span>

-   <span data-ttu-id="e55d8-145">Используйте АКС (путь = папка: <URL-адрес в кодировке>)</span><span class="sxs-lookup"><span data-stu-id="e55d8-145">Use AQS (crumb=folder:<URL-encoded path>)</span></span>
-   <span data-ttu-id="e55d8-146">Используйте аргумент Location (путь = расположение: <URL-адрес в кодировке>)</span><span class="sxs-lookup"><span data-stu-id="e55d8-146">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="e55d8-147">Папка на удаленном компьютере или в сети:</span><span class="sxs-lookup"><span data-stu-id="e55d8-147">Folder on a remote machine/network:</span></span>

-   <span data-ttu-id="e55d8-148">Используйте аргумент Location (путь = расположение: <URL-адрес в кодировке>)</span><span class="sxs-lookup"><span data-stu-id="e55d8-148">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="e55d8-149">Доступ к папке через известный обработчик протокола UNC:</span><span class="sxs-lookup"><span data-stu-id="e55d8-149">Folder accessed via a known UNC protocol handler:</span></span>

-   <span data-ttu-id="e55d8-150">Используйте АКС (повышено = Store <UNC protocol handler name> ).</span><span class="sxs-lookup"><span data-stu-id="e55d8-150">Use AQS (crumb=store:<UNC protocol handler name>)</span></span>
-   <span data-ttu-id="e55d8-151">Используйте аргумент Location (путь = расположение: <URL-адрес в кодировке>)</span><span class="sxs-lookup"><span data-stu-id="e55d8-151">Use location argument (crumb=location:<URL-encoded path>)</span></span>

### <a name="vista-examples"></a><span data-ttu-id="e55d8-152">Примеры для Vista</span><span class="sxs-lookup"><span data-stu-id="e55d8-152">Vista Examples</span></span>


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



<span data-ttu-id="e55d8-153">В первом примере выполняется поиск «отпуска», начиная с расположения shell://Personal (специального ярлыка для папки «Мои документы» пользователя), включая эту папку и все вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="e55d8-153">The first example executes a search for "vacation" starting at the shell://Personal location (a special shortcut to the user's My Documents folder), including that folder and all subfolders.</span></span> <span data-ttu-id="e55d8-154">См. таблицу ниже.</span><span class="sxs-lookup"><span data-stu-id="e55d8-154">See table below.</span></span>

<span data-ttu-id="e55d8-155">Во втором примере выполняется поиск в C: \\ Pictures, но не в c: \\ рисунки \\ дублируются.</span><span class="sxs-lookup"><span data-stu-id="e55d8-155">The second example executes a search within C:\\Pictures, but not in C:\\Pictures\\Duplicates.</span></span>

<span data-ttu-id="e55d8-156">В третьем примере выполняется поиск в документах C: \\ , ограниченных файлами, свойство Kind которых имеет значение pics.</span><span class="sxs-lookup"><span data-stu-id="e55d8-156">The third example executes a search within C:\\Documents, limited to files with the kind property set to pics.</span></span>

### <a name="constants-for-common-folders"></a><span data-ttu-id="e55d8-157">Константы для общих папок</span><span class="sxs-lookup"><span data-stu-id="e55d8-157">Constants for Common Folders</span></span>

<span data-ttu-id="e55d8-158">Windows Vista позволяет использовать значения [кновнфолдерид](/previous-versions//bb762584(v=vs.85)) , которые обеспечивают уникальный независимый от системы способ определения специальных папок, часто используемых приложениями, но которые могут не иметь одинакового имени или расположения в любой конкретной системе.</span><span class="sxs-lookup"><span data-stu-id="e55d8-158">Windows Vista enables the use of [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) values that provide a unique system-independent way to identify special folders used frequently by applications, but which may not have the same name or location on any given system.</span></span> <span data-ttu-id="e55d8-159">Например, системная папка может иметь значение «C: \\ Windows» на одной системе, а «c: \\ WinNT» — на другой.</span><span class="sxs-lookup"><span data-stu-id="e55d8-159">For example, the system folder may be "C:\\Windows" on one system and "C:\\Winnt" on another.</span></span> <span data-ttu-id="e55d8-160">До Windows Vista использовались [ксидлс](/windows/desktop/shell/csidl) .</span><span class="sxs-lookup"><span data-stu-id="e55d8-160">Prior to Windows Vista, [CSIDLs](/windows/desktop/shell/csidl) were used.</span></span>

<span data-ttu-id="e55d8-161">Используйте эти расположения в следующем синтаксисе:</span><span class="sxs-lookup"><span data-stu-id="e55d8-161">Use these locations with this syntax:</span></span>


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a><span data-ttu-id="e55d8-162">Использование инструкции with Windows XP (тип и магазин)</span><span class="sxs-lookup"><span data-stu-id="e55d8-162">Using crumb with Windows XP (kind and store)</span></span>

<span data-ttu-id="e55d8-163">Для поиска Windows в Windows XP (WDS 3. x) АКС термины "род" и "Store" имеют специальную реализацию.</span><span class="sxs-lookup"><span data-stu-id="e55d8-163">For Windows Search on Windows XP (WDS 3.x), the AQS terms "kind" and "store" have a special implementation.</span></span> <span data-ttu-id="e55d8-164">Значения "Kind" — это те же [значения, которые используются в WDS 2. x](../lwef/-search-2x-wds-perceivedtype.md).</span><span class="sxs-lookup"><span data-stu-id="e55d8-164">The "kind" values are the same [values used in WDS 2.x](../lwef/-search-2x-wds-perceivedtype.md).</span></span> <span data-ttu-id="e55d8-165">Значения "Store" включают следующее:</span><span class="sxs-lookup"><span data-stu-id="e55d8-165">The "store" values include the following:</span></span>

-   <span data-ttu-id="e55d8-166">действует</span><span class="sxs-lookup"><span data-stu-id="e55d8-166">mapi</span></span>
-   <span data-ttu-id="e55d8-167">файл</span><span class="sxs-lookup"><span data-stu-id="e55d8-167">file</span></span>
-   <span data-ttu-id="e55d8-168">аутлукекспресс</span><span class="sxs-lookup"><span data-stu-id="e55d8-168">outlookexpress</span></span>
-   <span data-ttu-id="e55d8-169">any</span><span class="sxs-lookup"><span data-stu-id="e55d8-169">any</span></span>

### <a name="xp-examples"></a><span data-ttu-id="e55d8-170">Примеры для XP</span><span class="sxs-lookup"><span data-stu-id="e55d8-170">XP Examples</span></span>


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



<span data-ttu-id="e55d8-171">Первый пример возвращает сообщения электронной почты Microsoft Outlook Express от Джон с пользовательской меткой "OE Mail".</span><span class="sxs-lookup"><span data-stu-id="e55d8-171">The first example returns Microsoft Outlook Express emails from John with the custom label, "OE Mail".</span></span> <span data-ttu-id="e55d8-172">Во втором примере выполняется поиск любого обмена данными из Джон.</span><span class="sxs-lookup"><span data-stu-id="e55d8-172">The second example executes a search for any communication from John.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e55d8-173">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e55d8-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e55d8-174">Начало работы с Parameter-Valueными аргументами</span><span class="sxs-lookup"><span data-stu-id="e55d8-174">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="e55d8-175">Аргументы идентификатора языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="e55d8-175">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="e55d8-176">Аргумент СИНТАКСИСа</span><span class="sxs-lookup"><span data-stu-id="e55d8-176">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="e55d8-177">СТАККЕДБИ, аргумент</span><span class="sxs-lookup"><span data-stu-id="e55d8-177">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="e55d8-178">Аргумент вложенного запроса</span><span class="sxs-lookup"><span data-stu-id="e55d8-178">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
