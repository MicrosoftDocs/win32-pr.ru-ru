---
description: 'Поиск: протокол приложения — это расширяемое соглашение для вызова приложения для поиска настольных систем в Windows Vista с пакетом обновления 1 (SP1) и более поздними версиями.'
title: Использование протокола поиска
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 91a1ec25-f6ab-4377-8478-20bc51a1d5df
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a9223a2a30cab85f8e1b0dac0d0df2dc4fe8f80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997882"
---
# <a name="using-the-search-protocol"></a><span data-ttu-id="92e4f-103">Использование протокола поиска</span><span class="sxs-lookup"><span data-stu-id="92e4f-103">Using the search Protocol</span></span>

<span data-ttu-id="92e4f-104">**Поиск:** [протокол приложения](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) — это расширяемое соглашение для вызова приложения для поиска настольных систем в Windows Vista с пакетом обновления 1 (SP1) и более поздними версиями.</span><span class="sxs-lookup"><span data-stu-id="92e4f-104">The **search:** [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is an extensible convention for calling the desktop search application on Windows Vista with Service Pack 1 (SP1) and later versions.</span></span> <span data-ttu-id="92e4f-105">Протокол был создан в Windows Vista с пакетом обновления 1 (SP1) (Дополнительные сведения см. в статье базы знаний [Обзор изменений Windows Vista Desktop Search в Windows Vista с пакетом обновления](https://support.microsoft.com/kb/941946)SP1), чтобы Windows смогла определить и вызвать приложение для поиска настольных систем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92e4f-105">The protocol was created in Windows Vista with SP1 (for information see the Knowledge Base article [Overview of Windows Vista desktop search Changes in Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) to give Windows a way to determine and call the default desktop search application.</span></span>

<span data-ttu-id="92e4f-106">Синтаксис протокола предоставляет ряд параметров, полезных для выполнения стандартных операций поиска рабочего стола, таких как пользовательские условия поиска или расположение, в котором был начат поиск.</span><span class="sxs-lookup"><span data-stu-id="92e4f-106">The protocol syntax provides a number of parameters useful for performing common desktop searches, such as user-entered search terms or the location on which the search was begun.</span></span> <span data-ttu-id="92e4f-107">Когда пользователи выполняют поиск из одной из двух доступных точек входа (в меню " **Пуск** " или в проводнике Windows), операционная система использует протокол поиска для запуска приложения для поиска настольных систем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92e4f-107">When users search from one of the two available search entry points (either the **Start** menu or Windows Explorer), the operating system uses the search protocol to launch the default desktop search application.</span></span> <span data-ttu-id="92e4f-108">Это достигается путем добавления вводимых пользователем условий поиска в стандартный синтаксис протокола поиска и передачи этих сведений приложению, зарегистрированному в качестве приложения поиска по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92e4f-108">It does this by adding the user-entered search terms to the standard search protocol syntax and passing that information to the application registered as the default search application.</span></span>

<span data-ttu-id="92e4f-109">Если другие приложения для поиска настольных систем не установлены, поиск, введенный в эти точки входа, запускает проводник Windows Search.</span><span class="sxs-lookup"><span data-stu-id="92e4f-109">If no other desktop search applications are installed, a search entered into these entry points launches the Windows Search Explorer.</span></span> <span data-ttu-id="92e4f-110">Однако сторонние разработчики могут создавать, устанавливать и регистрировать свои приложения для работы с протоколом поиска, а также как приложение поиска по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92e4f-110">However, third-party developers can create, install, and register their applications to handle the search protocol and to be the default search application.</span></span> <span data-ttu-id="92e4f-111">Такие приложения должны поддерживать синтаксис протокола поиска и регистрироваться в компоненте « [программы по умолчанию](default-programs.md) », чтобы обеспечить удобство работы с Windows.</span><span class="sxs-lookup"><span data-stu-id="92e4f-111">Such applications need to support the search protocol syntax and register with the [Default Programs](default-programs.md) feature to ensure a seamless experience with Windows.</span></span>

<span data-ttu-id="92e4f-112">При разработке приложения, предназначенного для использования или построения на определенном приложении для поиска на рабочем столе, не следует зависеть от протокола **поиска:** протокол.</span><span class="sxs-lookup"><span data-stu-id="92e4f-112">If you develop an application that is intended to use or build upon a specific desktop search application, you should not depend exclusively on the **search:** protocol.</span></span> <span data-ttu-id="92e4f-113">Так как многие приложения могут владеть **поиском:** протоколом, нет никакой гарантии, что целевое приложение для поиска настольных систем будет иметь его в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="92e4f-113">Because many applications could own the **search:** protocol, there is no guarantee that your targeted desktop search application will own it at any given time.</span></span> <span data-ttu-id="92e4f-114">Вместо этого следует использовать частный протокол поиска, определенный в целевом приложении поиска на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="92e4f-114">Instead, you should use a private search protocol defined by that targeted desktop search application.</span></span> <span data-ttu-id="92e4f-115">Это означает, что приложения для поиска на рабочем столе, предназначенные для платформы приложений сторонних разработчиков, должны поддерживать протокол **поиска:** Protocol и собственный собственный протокол поиска.</span><span class="sxs-lookup"><span data-stu-id="92e4f-115">This means that desktop search applications intended to be a platform for third-party applications should support both the **search:** protocol and their own proprietary search protocol.</span></span>

> [!Note]  
> <span data-ttu-id="92e4f-116">В поле **Поиск:** протокол не заменяет собственный поиск по протоколу [MS:](../search/-search-3x-wds-qryidx-searchms.md) .</span><span class="sxs-lookup"><span data-stu-id="92e4f-116">The **search:** protocol does not replace the proprietary [search-ms:](../search/-search-3x-wds-qryidx-searchms.md) protocol.</span></span> <span data-ttu-id="92e4f-117">Приложения по-прежнему могут использовать протокол **Search-MS:** для запуска обозревателя поиска окна или для автоматического запроса индексатора поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="92e4f-117">Applications can still use the **search-ms:** protocol to launch Window Search Explorer or to silently query the Windows Search indexer.</span></span>

 

<span data-ttu-id="92e4f-118">В этой статье рассматриваются следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="92e4f-118">This topic covers the following:</span></span>

-   [<span data-ttu-id="92e4f-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92e4f-119">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="92e4f-120">Windows Vista с пакетом обновления 1 (SP1) использование поиска: протокол</span><span class="sxs-lookup"><span data-stu-id="92e4f-120">Windows Vista with SP1 use of the search: protocol</span></span>](#windows-vista-with-sp1-use-of-the-search-protocol)
-   [<span data-ttu-id="92e4f-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="92e4f-121">Examples</span></span>](#examples)
-   [<span data-ttu-id="92e4f-122">Регистрация приложения, обрабатывающего протокол</span><span class="sxs-lookup"><span data-stu-id="92e4f-122">Registering the Application that Handles the Protocol</span></span>](#registering-the-application-that-handles-the-protocol)
    -   [<span data-ttu-id="92e4f-123">Записи реестра</span><span class="sxs-lookup"><span data-stu-id="92e4f-123">Registry Entries</span></span>](#registry-entries)
-   [<span data-ttu-id="92e4f-124">См. также</span><span class="sxs-lookup"><span data-stu-id="92e4f-124">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="92e4f-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92e4f-125">Syntax</span></span>

<span data-ttu-id="92e4f-126">Протокол поиска использует следующий стандартный синтаксис в кодировке URL:</span><span class="sxs-lookup"><span data-stu-id="92e4f-126">The search protocol uses the following standard URL-encoded syntax:</span></span>


```C++
search:parameter=value[&parameter=value]&
```



<span data-ttu-id="92e4f-127">Синтаксис начинается с определения самого протокола (**Поиск:**).</span><span class="sxs-lookup"><span data-stu-id="92e4f-127">The syntax begins by identifying the protocol itself (**search:**).</span></span> <span data-ttu-id="92e4f-128">Пары "параметр-значение" — это аргументы, передаваемые в поисковую систему, как описано в следующей таблице, в которой показаны все возможные параметры синтаксиса протокола поиска.</span><span class="sxs-lookup"><span data-stu-id="92e4f-128">The parameter/value pairs are arguments passed to the Search engine, as described in the following table, which shows all of the possible parameters for the search protocol syntax.</span></span>



| <span data-ttu-id="92e4f-129">Параметр</span><span class="sxs-lookup"><span data-stu-id="92e4f-129">Parameter</span></span>                                              | <span data-ttu-id="92e4f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="92e4f-130">Value</span></span>                                                         | <span data-ttu-id="92e4f-131">Описание</span><span class="sxs-lookup"><span data-stu-id="92e4f-131">Description</span></span>                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92e4f-132">query</span><span class="sxs-lookup"><span data-stu-id="92e4f-132">query</span></span>                                                  | <span data-ttu-id="92e4f-133">Текст в кодировке URL</span><span class="sxs-lookup"><span data-stu-id="92e4f-133">URL-encoded text</span></span>                                              | <span data-ttu-id="92e4f-134">Текст запроса, указанный пользователем.</span><span class="sxs-lookup"><span data-stu-id="92e4f-134">The query text entered by the user.</span></span>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="92e4f-135">инпутлокале</span><span class="sxs-lookup"><span data-stu-id="92e4f-135">inputlocale</span></span>](search-protocol-localeidentifiers.md)   | <span data-ttu-id="92e4f-136">Любой допустимый идентификатор кода языка (LCID)</span><span class="sxs-lookup"><span data-stu-id="92e4f-136">Any valid language code identifier (LCID)</span></span>                     | <span data-ttu-id="92e4f-137">КОД языка, определяющий язык ввода для запроса.</span><span class="sxs-lookup"><span data-stu-id="92e4f-137">The LCID that identifies the input language for the query.</span></span>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="92e4f-138">кэйвордлокале</span><span class="sxs-lookup"><span data-stu-id="92e4f-138">keywordlocale</span></span>](search-protocol-localeidentifiers.md) | <span data-ttu-id="92e4f-139">Любой допустимый код языка</span><span class="sxs-lookup"><span data-stu-id="92e4f-139">Any valid LCID</span></span>                                                | <span data-ttu-id="92e4f-140">КОД языка, определяющий язык международной версии индексатора.</span><span class="sxs-lookup"><span data-stu-id="92e4f-140">The LCID that identifies the language of the international version of the Indexer.</span></span> <span data-ttu-id="92e4f-141">Значение по умолчанию — 1033 (EN-US).</span><span class="sxs-lookup"><span data-stu-id="92e4f-141">The default is 1033 (en-us).</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="92e4f-142">иерархической</span><span class="sxs-lookup"><span data-stu-id="92e4f-142">crumb</span></span>](search-protocol-crumb.md)                     | <span data-ttu-id="92e4f-143">АКС, инструкция</span><span class="sxs-lookup"><span data-stu-id="92e4f-143">AQS statement</span></span>                                                 | <span data-ttu-id="92e4f-144">Этот аргумент ограничивает область поиска.</span><span class="sxs-lookup"><span data-stu-id="92e4f-144">This argument restricts the scope being searched.</span></span> <span data-ttu-id="92e4f-145">В Windows Vista протокол поиска поддерживает полную АКС, а также специальную реализацию для `location` аргумента.</span><span class="sxs-lookup"><span data-stu-id="92e4f-145">In Windows Vista, the search protocol supports full AQS as well as a special implementation for a `location` argument.</span></span> <span data-ttu-id="92e4f-146">В Windows XP протокол Search также поддерживает полную АКС, за исключением специальной реализации `kind` и `store` .</span><span class="sxs-lookup"><span data-stu-id="92e4f-146">In Windows XP, the search protocol also supports full AQS, except for a special implementation of `kind` and `store`.</span></span> |
| [<span data-ttu-id="92e4f-147">Syntax</span><span class="sxs-lookup"><span data-stu-id="92e4f-147">syntax</span></span>](search-protocol-syntaxargument.md)           | <span data-ttu-id="92e4f-148">НКС, АКС (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="92e4f-148">NQS, AQS (not case sensitive)</span></span>                                 | <span data-ttu-id="92e4f-149">Синтаксис запроса, используемый для поиска в индексе: естественный синтаксис запроса или синтаксис расширенных запросов (АКС).</span><span class="sxs-lookup"><span data-stu-id="92e4f-149">The query syntax to use to search the index: either Natural Query Syntax or Advanced Query Syntax (AQS).</span></span> <span data-ttu-id="92e4f-150">АКС является значением по умолчанию и всегда считается проанализированным и поддерживаемым.</span><span class="sxs-lookup"><span data-stu-id="92e4f-150">AQS is the default and is always assumed parsed and supported.</span></span>                                                                                                                        |
| [<span data-ttu-id="92e4f-151">стаккедби</span><span class="sxs-lookup"><span data-stu-id="92e4f-151">stackedby</span></span>](search-protocol-stackedby.md)             | <span data-ttu-id="92e4f-152">Любое допустимое свойство из системы свойств</span><span class="sxs-lookup"><span data-stu-id="92e4f-152">Any valid property from the property system</span></span>                   | <span data-ttu-id="92e4f-153">Свойство, указывающее столбец, по которому должны быть упорядочены результаты.</span><span class="sxs-lookup"><span data-stu-id="92e4f-153">A property that specifies the column to stack results by.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="92e4f-154">subquery</span><span class="sxs-lookup"><span data-stu-id="92e4f-154">subquery</span></span>](search-protocol-subquery.md)               | <span data-ttu-id="92e4f-155">Полностью указанный путь к сохраненному файлу поиска ( \* . Search-MS)</span><span class="sxs-lookup"><span data-stu-id="92e4f-155">A fully specified path for a Saved Search file (\*.search-ms)</span></span> | <span data-ttu-id="92e4f-156">Результаты вложенного запроса используются в качестве источника запроса.</span><span class="sxs-lookup"><span data-stu-id="92e4f-156">The results of the subquery are used as the source for the query.</span></span> <span data-ttu-id="92e4f-157">То есть термины запроса ищутся по результатам вложенного запроса.</span><span class="sxs-lookup"><span data-stu-id="92e4f-157">That is, the query terms are searched for against the results of the subquery.</span></span>                                                                                                                                               |
| <span data-ttu-id="92e4f-158">displayname</span><span class="sxs-lookup"><span data-stu-id="92e4f-158">displayname</span></span>                                            | <span data-ttu-id="92e4f-159">Строка в кодировке URL</span><span class="sxs-lookup"><span data-stu-id="92e4f-159">URL-encoded string</span></span>                                            | <span data-ttu-id="92e4f-160">Имя текущего поиска.</span><span class="sxs-lookup"><span data-stu-id="92e4f-160">The name of the current search.</span></span>                                                                                                                                                                                                                                                                |



 

## <a name="windows-vista-with-sp1-use-of-the-search-protocol"></a><span data-ttu-id="92e4f-161">Windows Vista с пакетом обновления 1 (SP1) использование поиска: протокол</span><span class="sxs-lookup"><span data-stu-id="92e4f-161">Windows Vista with SP1 use of the search: protocol</span></span>

<span data-ttu-id="92e4f-162">В Windows Vista с пакетом обновления 1 (SP1) есть несколько точек входа, из которых вызывается протокол **Search:** .</span><span class="sxs-lookup"><span data-stu-id="92e4f-162">Windows Vista with SP1 has several entry points from which it calls the **search:** protocol.</span></span> <span data-ttu-id="92e4f-163">Эти точки входа описаны ниже, а также общий синтаксис, связанный с каждой из них.</span><span class="sxs-lookup"><span data-stu-id="92e4f-163">These entry points are outlined below as well as the common syntax associated with each.</span></span>



| <span data-ttu-id="92e4f-164">Точка входа протокола поиска</span><span class="sxs-lookup"><span data-stu-id="92e4f-164">Search protocol entry point</span></span> | <span data-ttu-id="92e4f-165">Расположение</span><span class="sxs-lookup"><span data-stu-id="92e4f-165">Location</span></span>         | <span data-ttu-id="92e4f-166">Запрос вызван</span><span class="sxs-lookup"><span data-stu-id="92e4f-166">Query called</span></span>                                                         |
|-----------------------------|------------------|----------------------------------------------------------------------|
| <span data-ttu-id="92e4f-167">**Поиск везде**</span><span class="sxs-lookup"><span data-stu-id="92e4f-167">**Search Everywhere**</span></span>       | <span data-ttu-id="92e4f-168">Меню " **Пуск** "</span><span class="sxs-lookup"><span data-stu-id="92e4f-168">**Start** menu</span></span>   | <span data-ttu-id="92e4f-169">Поиск: Query =<*условие поиска*></span><span class="sxs-lookup"><span data-stu-id="92e4f-169">search:query=<*Search Term*></span></span>                                   |
| <span data-ttu-id="92e4f-170">**Поиск везде**</span><span class="sxs-lookup"><span data-stu-id="92e4f-170">**Search Everywhere**</span></span>       | <span data-ttu-id="92e4f-171">Проводник</span><span class="sxs-lookup"><span data-stu-id="92e4f-171">Windows Explorer</span></span> | <span data-ttu-id="92e4f-172">Поиск: запрос =<*термин поиска*>&путь = расположение: <*Расположение*></span><span class="sxs-lookup"><span data-stu-id="92e4f-172">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |
| <span data-ttu-id="92e4f-173">Клавиша Windows+F</span><span class="sxs-lookup"><span data-stu-id="92e4f-173">Windows logo key+F</span></span>          | <span data-ttu-id="92e4f-174">В любом месте</span><span class="sxs-lookup"><span data-stu-id="92e4f-174">Anywhere</span></span>         | <span data-ttu-id="92e4f-175">осуществлять</span><span class="sxs-lookup"><span data-stu-id="92e4f-175">search:</span></span>                                                              |
| <span data-ttu-id="92e4f-176">CTRL+F</span><span class="sxs-lookup"><span data-stu-id="92e4f-176">CTRL+F</span></span>                      | <span data-ttu-id="92e4f-177">Проводник</span><span class="sxs-lookup"><span data-stu-id="92e4f-177">Windows Explorer</span></span> | <span data-ttu-id="92e4f-178">Поиск: запрос =<*термин поиска*>&путь = расположение: <*Расположение*></span><span class="sxs-lookup"><span data-stu-id="92e4f-178">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |
| <span data-ttu-id="92e4f-179">F3</span><span class="sxs-lookup"><span data-stu-id="92e4f-179">F3</span></span>                          | <span data-ttu-id="92e4f-180">Меню " **Пуск** "</span><span class="sxs-lookup"><span data-stu-id="92e4f-180">**Start** menu</span></span>   | <span data-ttu-id="92e4f-181">осуществлять</span><span class="sxs-lookup"><span data-stu-id="92e4f-181">search:</span></span>                                                              |
| <span data-ttu-id="92e4f-182">F3</span><span class="sxs-lookup"><span data-stu-id="92e4f-182">F3</span></span>                          | <span data-ttu-id="92e4f-183">Проводник</span><span class="sxs-lookup"><span data-stu-id="92e4f-183">Windows Explorer</span></span> | <span data-ttu-id="92e4f-184">Поиск: запрос =<*термин поиска*>&путь = расположение: <*Расположение*></span><span class="sxs-lookup"><span data-stu-id="92e4f-184">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |



 

<span data-ttu-id="92e4f-185">Точки входа протокола поиска с пакетом обновления 1 (SP1) для Windows Vista не используют все возможные параметры в протоколе поиска.</span><span class="sxs-lookup"><span data-stu-id="92e4f-185">The Windows Vista with SP1 search protocol entry points do not take advantage of all the possible parameters in the search protocol.</span></span> <span data-ttu-id="92e4f-186">Приложения, которые связаны только с обработкой вызовов протокола поиска из Windows Vista с пакетом обновления 1 (SP1), могут использовать приведенную ниже таблицу в качестве рекомендации по минимальным требованиям, которые необходимо реализовать.</span><span class="sxs-lookup"><span data-stu-id="92e4f-186">Applications that are only concerned with handling search protocol calls from Windows Vista with SP1 can use the following table as a guide to the minimum they need to implement.</span></span>



| <span data-ttu-id="92e4f-187">Параметр</span><span class="sxs-lookup"><span data-stu-id="92e4f-187">Parameter</span></span>                                              | <span data-ttu-id="92e4f-188">Используется Windows?</span><span class="sxs-lookup"><span data-stu-id="92e4f-188">Used by Windows?</span></span> | <span data-ttu-id="92e4f-189">Как Windows Vista с пакетом обновления 1 (SP1) использует ее при вызове поиска:</span><span class="sxs-lookup"><span data-stu-id="92e4f-189">How Windows Vista with SP1 uses it when calling search:</span></span>                                                                                                                                                                                                                     |
|--------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92e4f-190">query</span><span class="sxs-lookup"><span data-stu-id="92e4f-190">query</span></span>                                                  | <span data-ttu-id="92e4f-191">Да</span><span class="sxs-lookup"><span data-stu-id="92e4f-191">Yes</span></span>              | <span data-ttu-id="92e4f-192">Текст запроса, указанный пользователем.</span><span class="sxs-lookup"><span data-stu-id="92e4f-192">The query text entered by the user.</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="92e4f-193">иерархической</span><span class="sxs-lookup"><span data-stu-id="92e4f-193">crumb</span></span>](search-protocol-crumb.md)                     | <span data-ttu-id="92e4f-194">Да</span><span class="sxs-lookup"><span data-stu-id="92e4f-194">Yes</span></span>              | <span data-ttu-id="92e4f-195">[](search-protocol-crumb.md) в этом `location` случае аргумент используется для указания места, откуда поступил запрос.</span><span class="sxs-lookup"><span data-stu-id="92e4f-195">[crumb](search-protocol-crumb.md) uses the `location` argument to specify where the query came from.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="92e4f-196">subquery</span><span class="sxs-lookup"><span data-stu-id="92e4f-196">subquery</span></span>](search-protocol-subquery.md)               | <span data-ttu-id="92e4f-197">Да</span><span class="sxs-lookup"><span data-stu-id="92e4f-197">Yes</span></span>              | <span data-ttu-id="92e4f-198">Результаты аргумента [вложенного запроса](search-protocol-subquery.md) используются в качестве области элементов для поиска.</span><span class="sxs-lookup"><span data-stu-id="92e4f-198">The results of the [Subquery](search-protocol-subquery.md) argument are used as the scope of items to search.</span></span> <span data-ttu-id="92e4f-199">Обычно это можно использовать, если пользователь использовал для поиска файл. Search-MS, а затем назвать приложение поиска рабочего стола по умолчанию в этом поиске.</span><span class="sxs-lookup"><span data-stu-id="92e4f-199">This would typically be used if a user was using a .search-ms file to search and then called the default desktop search application from within that search.</span></span> |
| [<span data-ttu-id="92e4f-200">инпутлокале</span><span class="sxs-lookup"><span data-stu-id="92e4f-200">inputlocale</span></span>](search-protocol-localeidentifiers.md)   | <span data-ttu-id="92e4f-201">Нет</span><span class="sxs-lookup"><span data-stu-id="92e4f-201">No</span></span>               | <span data-ttu-id="92e4f-202">В настоящий момент не используется.</span><span class="sxs-lookup"><span data-stu-id="92e4f-202">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="92e4f-203">кэйвордлокале</span><span class="sxs-lookup"><span data-stu-id="92e4f-203">keywordlocale</span></span>](search-protocol-localeidentifiers.md) | <span data-ttu-id="92e4f-204">Нет</span><span class="sxs-lookup"><span data-stu-id="92e4f-204">No</span></span>               | <span data-ttu-id="92e4f-205">В настоящий момент не используется.</span><span class="sxs-lookup"><span data-stu-id="92e4f-205">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="92e4f-206">Syntax</span><span class="sxs-lookup"><span data-stu-id="92e4f-206">syntax</span></span>](search-protocol-syntaxargument.md)           | <span data-ttu-id="92e4f-207">Нет</span><span class="sxs-lookup"><span data-stu-id="92e4f-207">No</span></span>               | <span data-ttu-id="92e4f-208">В настоящий момент не используется.</span><span class="sxs-lookup"><span data-stu-id="92e4f-208">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="92e4f-209">стаккедби</span><span class="sxs-lookup"><span data-stu-id="92e4f-209">stackedby</span></span>](search-protocol-stackedby.md)             | <span data-ttu-id="92e4f-210">Нет</span><span class="sxs-lookup"><span data-stu-id="92e4f-210">No</span></span>               | <span data-ttu-id="92e4f-211">В настоящий момент не используется.</span><span class="sxs-lookup"><span data-stu-id="92e4f-211">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="92e4f-212">displayname</span><span class="sxs-lookup"><span data-stu-id="92e4f-212">displayname</span></span>                                            | <span data-ttu-id="92e4f-213">Нет</span><span class="sxs-lookup"><span data-stu-id="92e4f-213">No</span></span>               | <span data-ttu-id="92e4f-214">В настоящий момент не используется.</span><span class="sxs-lookup"><span data-stu-id="92e4f-214">Not currently used.</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="examples"></a><span data-ttu-id="92e4f-215">Примеры</span><span class="sxs-lookup"><span data-stu-id="92e4f-215">Examples</span></span>

<span data-ttu-id="92e4f-216">Если пользователь вводит "Microsoft" в меню " **Пуск** " и нажимает кнопку " **Поиск везде**", полученный запрос протокола поиска будет выполнен:</span><span class="sxs-lookup"><span data-stu-id="92e4f-216">If a user enters "Microsoft" in the **Start** menu and clicks **Search Everywhere**, the resulting search protocol call is made:</span></span>


```C++
search:query=microsoft&
```



<span data-ttu-id="92e4f-217">Если пользователь вводит "Сиэтл" в проводнике Windows в C: \\ MyFolder, а затем нажимает кнопку " **Поиск везде**", выполняется следующий вызов с использованием escape-символов для ":" и " \\ ":</span><span class="sxs-lookup"><span data-stu-id="92e4f-217">If a user enters "Seattle" in Windows Explorer within C:\\MyFolder and then clicks **Search Everywhere**, the following call is made, using escape characters for ':' and '\\':</span></span>


```C++
search:query=seattle&crumb=location:C%3A%5CMyFolder
```



## <a name="registering-the-application-that-handles-the-protocol"></a><span data-ttu-id="92e4f-218">Регистрация приложения, обрабатывающего протокол</span><span class="sxs-lookup"><span data-stu-id="92e4f-218">Registering the Application that Handles the Protocol</span></span>

<span data-ttu-id="92e4f-219">Так как несколько приложений могут конкурировать за протокол поиска, необходимо зарегистрировать приложение в программе [по умолчанию](default-programs.md) во время установки, чтобы пользователь мог легко настроить по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92e4f-219">Because multiple applications can contend for the search protocol, you should register your application with the [Default Programs](default-programs.md) feature during installation to enable the user to configure the default more easily.</span></span> <span data-ttu-id="92e4f-220">В дополнение к обычным процедурам установки в Windows XP, приложение на основе Windows Vista должно быть зарегистрировано в компоненте "программы по умолчанию", чтобы приложение и пользователи могли легко настраивать значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92e4f-220">In addition to the installation procedures normally practiced under Windows XP, a Windows Vista-based application must register with the Default Programs feature so that the application and users can seamlessly configure defaults.</span></span>

<span data-ttu-id="92e4f-221">После установки необходимых двоичных файлов на компьютере пользователя подпрограммы установки должны выполнить следующие общие задачи:</span><span class="sxs-lookup"><span data-stu-id="92e4f-221">After installing the necessary binary files on the user's computer, your installation routine should complete these general tasks:</span></span>

1.  <span data-ttu-id="92e4f-222">Запишите идентификаторы ProgID на **\_ локальный \_ компьютер hKey**, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="92e4f-222">Write ProgIDs to **HKEY\_LOCAL\_MACHINE**, as described below.</span></span> <span data-ttu-id="92e4f-223">Обратите внимание, что приложения должны создавать идентификаторы ProgID для конкретного приложения для протокола поиска.</span><span class="sxs-lookup"><span data-stu-id="92e4f-223">Note that applications must create application-specific ProgIDs for the search protocol.</span></span>
2.  <span data-ttu-id="92e4f-224">Утверждение сопоставления протокола поиска на уровне компьютера.</span><span class="sxs-lookup"><span data-stu-id="92e4f-224">Claim machine-level search protocol association.</span></span>
3.  <span data-ttu-id="92e4f-225">Зарегистрируйте приложение в [программах по умолчанию](default-programs.md), как описано в разделах [Регистрация приложения для использования с программами по умолчанию](default-programs.md)в качестве средства для протокола поиска.</span><span class="sxs-lookup"><span data-stu-id="92e4f-225">Register the application with [Default Programs](default-programs.md), as explained in [Registering an Application for Use with Default Programs](default-programs.md), as a contender for the search protocol.</span></span>

### <a name="registry-entries"></a><span data-ttu-id="92e4f-226">Записи реестра</span><span class="sxs-lookup"><span data-stu-id="92e4f-226">Registry Entries</span></span>

<span data-ttu-id="92e4f-227">Ниже приведены примеры необходимых записей реестра для вымышленного приложения поиска на рабочем столе, Поиск contoso.</span><span class="sxs-lookup"><span data-stu-id="92e4f-227">The following are examples of the required registry entries for a fictional desktop search application, Contoso Search.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            URL Protocol = ""
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            DefaultIcon
               (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe,-7
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe %1
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Contoso Search = "Software\\Contoso\\Search\\Capabilities"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               ApplicationName = "Contoso Search Test App"
               ApplicationDescription = "Contoso search is a great new desktop search application"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               UrlAssociations
                  search = "contoso-search"
```

## <a name="related-topics"></a><span data-ttu-id="92e4f-228">См. также</span><span class="sxs-lookup"><span data-stu-id="92e4f-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92e4f-229">Синтаксис расширенных запросов</span><span class="sxs-lookup"><span data-stu-id="92e4f-229">Advanced Query Syntax</span></span>](../search/-search-3x-advancedquerysyntax.md)
</dt> <dt>

[<span data-ttu-id="92e4f-230">Программы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="92e4f-230">Default Programs</span></span>](default-programs.md)
</dt> </dl>

 

 
