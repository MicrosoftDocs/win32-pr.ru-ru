---
title: Протокол служб индексирования содержимого
description: Этот документ является спецификацией протокола службы индексирования содержимого.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c22bbda912333368e50d3e4a8ace2cd98856ea
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "103789318"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="5fa9d-103">Протокол служб индексирования содержимого</span><span class="sxs-lookup"><span data-stu-id="5fa9d-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="5fa9d-104">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="5fa9d-105">В более поздних выпусках используйте вместо этого [Поиск Windows](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="5fa9d-106">Спецификация протокола, версия 0,12</span><span class="sxs-lookup"><span data-stu-id="5fa9d-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="5fa9d-107">1 Введение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="5fa9d-108">1.1. Глоссарий</span><span class="sxs-lookup"><span data-stu-id="5fa9d-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="5fa9d-109">1.2. Ссылки</span><span class="sxs-lookup"><span data-stu-id="5fa9d-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="5fa9d-110">Общие сведения о протоколе 1,3 (краткий обзор)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="5fa9d-111">1.4. Связь с другими протоколами</span><span class="sxs-lookup"><span data-stu-id="5fa9d-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="5fa9d-112">1,5. Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="5fa9d-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="5fa9d-113">1.6. Постановление о пределах применения</span><span class="sxs-lookup"><span data-stu-id="5fa9d-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="5fa9d-114">1.7. Управление версиями и согласованность функций</span><span class="sxs-lookup"><span data-stu-id="5fa9d-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="5fa9d-115">1.8. Расширяемые поля поставщика</span><span class="sxs-lookup"><span data-stu-id="5fa9d-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="5fa9d-116">1.9. Назначения стандартов</span><span class="sxs-lookup"><span data-stu-id="5fa9d-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="5fa9d-117">2. Сообщения</span><span class="sxs-lookup"><span data-stu-id="5fa9d-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="5fa9d-118">2.1. Транспортировка</span><span class="sxs-lookup"><span data-stu-id="5fa9d-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="5fa9d-119">2.2. Синтаксис сообщений</span><span class="sxs-lookup"><span data-stu-id="5fa9d-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="5fa9d-120">3. Сведения о протоколе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="5fa9d-121">Сведения о сервере 3,1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="5fa9d-122">3,2. сведения о клиенте</span><span class="sxs-lookup"><span data-stu-id="5fa9d-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="5fa9d-123">4. Примеры протокола</span><span class="sxs-lookup"><span data-stu-id="5fa9d-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="5fa9d-124">4,1 Пример 1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="5fa9d-125">4,2. Пример 2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="5fa9d-126">5. Безопасность</span><span class="sxs-lookup"><span data-stu-id="5fa9d-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="5fa9d-127">5.1. Вопросы безопасности для разработчиков</span><span class="sxs-lookup"><span data-stu-id="5fa9d-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="5fa9d-128">5.2. Индекс параметров безопасности</span><span class="sxs-lookup"><span data-stu-id="5fa9d-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="5fa9d-129">6 индекс поведения, зависящего от версии</span><span class="sxs-lookup"><span data-stu-id="5fa9d-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="5fa9d-130">Этот документ является спецификацией протокола службы индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="5fa9d-131">Документация по протоколу сервера Workgroup Server (WSPP) предназначена для использования в сочетании с документацией по общедоступным стандартам, графикой программирования сети и концепциями распределенных систем Windows Workgroup, и предполагает, что читатель знаком с упомянутым материалом или имеет немедленный доступ к нему.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="5fa9d-132">Спецификация протокола WSPP не требует использования средств программирования Майкрософт или сред программирования, чтобы лицензироваться на разработку реализации.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="5fa9d-133">Лицензии, имеющие доступ к средствам и средам программирования Майкрософт, могут воспользоваться преимуществами этих средств.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="5fa9d-134">1. Введение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-134">1 Introduction</span></span>

-   [<span data-ttu-id="5fa9d-135">1.1. Глоссарий</span><span class="sxs-lookup"><span data-stu-id="5fa9d-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="5fa9d-136">1.2. Ссылки</span><span class="sxs-lookup"><span data-stu-id="5fa9d-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="5fa9d-137">Общие сведения о протоколе 1,3 (краткий обзор)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="5fa9d-138">1.4. Связь с другими протоколами</span><span class="sxs-lookup"><span data-stu-id="5fa9d-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="5fa9d-139">1,5. Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="5fa9d-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="5fa9d-140">1.6. Постановление о пределах применения</span><span class="sxs-lookup"><span data-stu-id="5fa9d-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="5fa9d-141">1.7. Управление версиями и согласованность функций</span><span class="sxs-lookup"><span data-stu-id="5fa9d-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="5fa9d-142">1.8. Расширяемые поля поставщика</span><span class="sxs-lookup"><span data-stu-id="5fa9d-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="5fa9d-143">1.9. Назначения стандартов</span><span class="sxs-lookup"><span data-stu-id="5fa9d-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="5fa9d-144">1.1. Глоссарий</span><span class="sxs-lookup"><span data-stu-id="5fa9d-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="5fa9d-145">Следующие термины определены в разделе глоссария в \[ MS-sys \] :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="5fa9d-146">Код GUID</span><span class="sxs-lookup"><span data-stu-id="5fa9d-146">GUID</span></span>
> -   <span data-ttu-id="5fa9d-147">Прямой порядок байтов</span><span class="sxs-lookup"><span data-stu-id="5fa9d-147">Little Endian</span></span>
> -   <span data-ttu-id="5fa9d-148">Именованный канал</span><span class="sxs-lookup"><span data-stu-id="5fa9d-148">Named Pipe</span></span>
> -   <span data-ttu-id="5fa9d-149">Путь</span><span class="sxs-lookup"><span data-stu-id="5fa9d-149">Path</span></span>

 

<span data-ttu-id="5fa9d-150">**Binding**: запрос на включение определенного **столбца** в возвращенный **набор строк** .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="5fa9d-151">**Привязка** указывает свойство, включаемое в результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="5fa9d-152">**Bookmark**: маркер, однозначно определяющий строку в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="5fa9d-153">**Catalog**— единица организации высшего уровня в службе индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="5fa9d-154">Он представляет собой набор индексированных документов, по которым можно выполнять запросы с помощью протокола службы индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="5fa9d-155">**Категория**: Иерархическое группирование строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="5fa9d-156">Например, результат запроса, содержащий столбцы Author и Title, можно классифицировать на основе автора.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="5fa9d-157">Каждая группа строк, содержащая одно и то же значение для автора, будет составлять категорию.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="5fa9d-158">**Глава** : диапазон **строк** в наборе **строк** .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="5fa9d-159">**Column**: контейнер для одного типа данных в **строке** .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="5fa9d-160">Столбцы сопоставляются с именами свойств и указывают, какие свойства используются для элементов **дерева** **команд** в поисковом запросе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="5fa9d-161">**Дерево команд**: сочетание **ограничений** , **категорий** и **порядков сортировки** , заданных для поискового запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="5fa9d-162">**Cursor**: сущность, используемая в качестве механизма для работы с одной **строкой** или небольшим блоком **строк** за раз в наборе данных, возвращаемых в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="5fa9d-163">**Курсор** располагается на одной **строке** в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="5fa9d-164">После того как **курсор** находится в строке, операции могут выполняться над этой **строкой** или в блоке **строк** , начиная с этой позиции.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="5fa9d-165">**Handle**— маркер, который можно использовать для распознавания и доступа к **курсорам** , **главам** и **закладкам** .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="5fa9d-166">**Index**: Постоянная структура, содержащая текстовое содержимое, извлеченное из файлов **службой индексирования** .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="5fa9d-167">Сюда входит список слов, которые хранятся вместе с содержащимся именем файла, расположением Word и **языковым стандартом** .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="5fa9d-168">**Индексирование**. процесс извлечения текста и свойств из файлов и сохранения извлеченных значений в **индексах** (для текста) и в **кэше свойств** (для свойств).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="5fa9d-169">**Служба индексирования**: служба, которая создает индексированные **каталоги** для содержимого и свойств файловых систем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="5fa9d-170">Приложения могут искать в каталогах сведения из файлов в индексированной файловой системе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="5fa9d-171">**Языковой стандарт**: идентификатор, как указано в \[ приложении MS-GPSI, \] который указывает предпочтения, связанные с языком.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="5fa9d-172">Эти настройки указывают, как форматируются даты и время, элементы сортируются в алфавитном порядке, сравниваются по строкам и т. д.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="5fa9d-173">**Запрос на естественном языке**. запрос, построенный на языке человека вместо синтаксиса запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="5fa9d-174">**Пропускаемое слово**: слово, которое игнорируется службой индексирования, если оно существует в **ограничениях** , указанных для поискового запроса, так как у него малое значение для дискриминатора.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="5fa9d-175">Примеры на английском языке: "a", "and" и "The".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="5fa9d-176">**Кэш свойств**: кэш свойств файла, извлеченных **службой индексирования** .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="5fa9d-177">**Индексирование свойств**. процесс создания **индекса** **свойств типа «значение** » документа, включая автора, тему, тип, число слов, число печатных страниц и другие свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="5fa9d-178">**Ограничение**: набор условий, которым должен соответствовать файл, включаемый в результаты поиска, возвращенные **службой индексирования** в ответ на поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="5fa9d-179">**Ограничение** ограничивает фокус поискового запроса, ограничивая файлы, которые **Служба индексирования** будет включать в результаты поиска, только те, которые соответствуют условиям.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="5fa9d-180">**Row**: коллекция **столбцов** , содержащая значения свойств, которые описывают отдельный файл из набора файлов, соответствующих **ограничениям** , указанным в поисковом запросе, отправленном в **службу индексирования** .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="5fa9d-181">**Набор строк: набор** **строк** , возвращаемых в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="5fa9d-182">**Порядок сортировки**. набор правил в поисковом запросе, который определяет порядок строк в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="5fa9d-183">Каждое правило состоит из свойства (имя, размер и т. д.) и направления упорядочения (по возрастанию или по убыванию).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="5fa9d-184">Несколько правил применяются последовательно.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="5fa9d-185">**Свойство текстового типа**: свойство, которое описывает содержимое документа и имеет только неформатированный текст, связанный с его именем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="5fa9d-186">**Свойство типа значения**— свойство, которое описывает один атрибут всего документа.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="5fa9d-187">Свойство типа значения имеет идентификатор типа данных и значение этого типа данных, связанное с его именем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="5fa9d-188">**Виртуальный корневой каталог**: альтернативный путь к папке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="5fa9d-189">У физической папки может быть не более одного виртуального корня.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="5fa9d-190">Пути, начинающиеся с виртуального корня, называются виртуальными путями.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="5fa9d-191">Например,/сервер/ванитирут может быть виртуальным корнем C: \\ IIS \\ Web \\ папка1.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="5fa9d-192">Затем файл C: \\ IIS \\ web \\ папка1 \\default.htm будет иметь виртуальный путь/сервер/ванитирут/default.htm.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="5fa9d-193">**Может**, не должен, не обязательно: эти термины (во всех прописных) используются, как описано в \[ RFC2119 \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="5fa9d-194">Во всех необязательных инструкциях используются термины MAY (ВОЗМОЖНО), SHOULD (СЛЕДУЕТ) или SHOULD NOT (НЕ СЛЕДУЕТ).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="5fa9d-195">1.2. Ссылки</span><span class="sxs-lookup"><span data-stu-id="5fa9d-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="5fa9d-196">1.2.1. Нормативные ссылки</span><span class="sxs-lookup"><span data-stu-id="5fa9d-196">1.2.1 Normative References</span></span>

<span data-ttu-id="5fa9d-197">\[IEEE754 \] институт инженеров по стандартизации и электронике, "Standard для Floating-Point арифметических операций", IEEE 754-1985, 1985 октября, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="5fa9d-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="5fa9d-198">\[MS-DCOM \] корпорации Майкрософт, «распределенные протоколы модели объектов Distributed Component», 2006 июня.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="5fa9d-199">\[MS-GPSI \] Microsoft Corporation, "Групповая политика установки программное расширение", июнь 2006 г.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="5fa9d-200">\[MS-SMB \] Корпорация Майкрософт, Microsoft (протокол SMB) и расширения, май 2006.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="5fa9d-201">\[MS-SYS Корпорация \] Майкрософт, "системный обзор v4", июль 2006.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="5fa9d-202">\[САЛТОН \] Салтон, G., "Автоматическая обработка текста: анализ преобразования и извлечение информации по компьютерам", 1988, ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="5fa9d-203">\[Unicode \] Consortium (Unicode Standard, версия 2,0, 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="5fa9d-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="5fa9d-204">1.2.2. Справочные ссылки</span><span class="sxs-lookup"><span data-stu-id="5fa9d-204">1.2.2 Informative References</span></span>

<span data-ttu-id="5fa9d-205">\[MSDN-OLEDB \] корпорации Майкрософт, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="5fa9d-206">\[MSDN — КУЕРЕРР \] корпорации Майкрософт, Query-Execution значения https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="5fa9d-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="5fa9d-207">Общие сведения о протоколе 1,3 (краткий обзор)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="5fa9d-208">**Служба индексирования** содержимого помогает эффективно организовывать извлеченные функции коллекции документов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="5fa9d-209">Протокол службы индексирования содержимого (CISP) позволяет клиенту взаимодействовать с сервером, на котором размещена служба индексирования, выдавать запросы и предоставлять администратору возможность управлять сервером индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="5fa9d-210">При обработке файлов служба индексирования анализирует набор документов и реорганизует их содержимое таким образом, что **Свойства** этих документов могут быть эффективно возвращены в ответ на запросы.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="5fa9d-211">Коллекция документов, которые можно запросить, состоит из **каталога** .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="5fa9d-212">Каталог может содержать **индекс** (для быстрого получения ссылки на текст) и **кэш свойств** (для быстрого извлечения значений свойств).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="5fa9d-213">По сути, каталог состоит из логической "таблицы" свойств с текстом или значением и соответствующим языковым стандартом, хранящимся в **столбцах** таблицы.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="5fa9d-214">Каждая строка таблицы соответствует отдельному документу в области каталога, а каждый столбец таблицы соответствует свойству.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="5fa9d-215">Конкретные задачи, выполняемые CISP, группируются в две функциональные области:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="5fa9d-216">Удаленное администрирование каталогов служб индексирования,</span><span class="sxs-lookup"><span data-stu-id="5fa9d-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="5fa9d-217">Удаленное выполнение запросов к каталогам службы индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="5fa9d-218">Задачи удаленного администрирования 1.3.1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="5fa9d-219">CISP включает следующие задачи управления каталогом служб индексирования из клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="5fa9d-220">Запрашивает текущее состояние каталога служб индексирования на сервере.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="5fa9d-221">Обновление состояния каталога служб индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="5fa9d-222">Запуск процесса индексирования для определенного набора файлов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="5fa9d-223">Инициация оптимизации индекса для повышения производительности запросов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="5fa9d-224">Все задачи удаленного администрирования следуют простой модели "запрос-ответ".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="5fa9d-225">На клиенте не ведется никаких состояний для вызова администрирования, и административные вызовы могут выполняться в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="5fa9d-226">1.3.2 удаленный запрос</span><span class="sxs-lookup"><span data-stu-id="5fa9d-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="5fa9d-227">CISP позволяет клиентам выполнять поисковые запросы к удаленному серверу, на котором размещена служба индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="5fa9d-228">Отправка поискового запроса — это многоэтапный процесс, инициированный клиентом.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="5fa9d-229">Для этого необходимо выполнить следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="5fa9d-230">Клиент запрашивает соединение с сервером, на котором размещена служба индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="5fa9d-231">Клиент отправляет параметры поискового запроса, в том числе следующие:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="5fa9d-232">**Ограничения** , указывающие, какие документы должны включаться и (или) исключены из результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="5fa9d-233">Порядок, в котором должны возвращаться результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="5fa9d-234">Столбцы, возвращаемые в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="5fa9d-235">Максимальное число **строк** , которое должно быть возвращено для запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="5fa9d-236">Максимальное время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="5fa9d-237">После того как сервер подтвердил запрос клиента на инициацию запроса, клиент может запросить сведения о состоянии запроса, но это не обязательное действие.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="5fa9d-238">Затем клиент указывает, какие свойства сервер должен включать в результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="5fa9d-239">Клиент запрашивает результирующий набор от сервера, а сервер отвечает, отправляя клиенту значения свойств для файлов, включенных в результаты поискового запроса клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="5fa9d-240">Если значение свойства слишком велико для одного буфера ответа, сервер не будет передавать свойство, а вместо этого установит для свойства значение отложено.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="5fa9d-241">Затем клиент запрашивает значение свойства отдельно, используя последовательность запросов для последовательных блоков значения, а затем возобновляет запрос других значений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="5fa9d-242">Когда клиент завершает работу с поисковым запросом и больше не требует дополнительных результатов, клиент обращается к серверу для освобождения запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="5fa9d-243">После того, как сервер выпустил запрос, клиент может отправить запрос на отключение от сервера.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="5fa9d-244">После этого соединение закрывается.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-244">The connection is then closed.</span></span> <span data-ttu-id="5fa9d-245">Кроме того, клиент может отправить еще один запрос и повторить последовательность из шага 2.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="5fa9d-246">Поведение Windows. Этот Протокол реализован в Windows 2000, Windows XP, Windows Server 2003 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="5fa9d-247">1.4. Связь с другими протоколами</span><span class="sxs-lookup"><span data-stu-id="5fa9d-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="5fa9d-248">CISP использует \[ протокол SMB MS-SMB \] для передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="5fa9d-249">Никакой другой протокол не зависит непосредственно от протокола службы индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="5fa9d-250">*Поведение Windows. Обычно приложения взаимодействуют с оболочкой интерфейса OLE DB \[ MSDN-OLEDB \] (например, клиент протокола), а не напрямую с протоколом.*</span><span class="sxs-lookup"><span data-stu-id="5fa9d-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="5fa9d-251">1,5. Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="5fa9d-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="5fa9d-252">Предполагается, что клиент получил имя сервера и имя каталога перед вызовом этого протокола.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="5fa9d-253">То, как клиент делает это, лежит вне области данной спецификации.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="5fa9d-254">Также предполагается, что клиент и сервер имеют сопоставление безопасности, которое можно использовать с именованными каналами \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="5fa9d-255">1.6. Постановление о пределах применения</span><span class="sxs-lookup"><span data-stu-id="5fa9d-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="5fa9d-256">CISP предназначен для запросов и управления каталогами на удаленном сервере от клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="5fa9d-257">CISP является устаревшим в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="5fa9d-258">1.7. Управление версиями и согласованность функций</span><span class="sxs-lookup"><span data-stu-id="5fa9d-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="5fa9d-259">Этот протокол не имеет механизмов управления версиями или согласования возможностей.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="5fa9d-260">1.8. Расширяемые поля поставщика</span><span class="sxs-lookup"><span data-stu-id="5fa9d-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="5fa9d-261">Этот протокол использует значения HRESULT, которые являются расширяемыми поставщиками.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="5fa9d-262">Поставщики могут выбирать собственные значения для этого поля, если бит C (0x20000000) задан в соответствии с разделом 4.1.1 в MS-SYS, что означает, что это \[ \] код клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="5fa9d-263">Этот протокол также использует значения NTSTATUS, взятые из числового пространства NTSTATUS, определенного в \[ MS-sys \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="5fa9d-264">Поставщики должны повторно использовать эти значения с указанным значением.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="5fa9d-265">Выбор любого другого значения вызывает риск конфликта в будущем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="5fa9d-266">*Поведение Windows. в Windows используются только значения, указанные в разделе 4.1.3 из \[ MS-sys \] .*</span><span class="sxs-lookup"><span data-stu-id="5fa9d-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="5fa9d-267">Идентификаторы свойств 1.8.1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="5fa9d-268">Свойства представлены идентификаторами, известными как идентификаторы свойств.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="5fa9d-269">Каждое свойство должно иметь глобальный уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="5fa9d-270">Этот идентификатор состоит из **идентификатора GUID** , представляющего коллекцию свойств, которые называются набором свойств, а также строки или 32-разрядного целого числа для идентификации свойства в наборе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="5fa9d-271">Если используется целочисленная форма идентификатора, значения 0x00000000, 0xFFFFFFFF и 0xFFFFFFFE считаются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="5fa9d-272">Поставщики могут гарантировать, что их свойства определяются уникальным образом, помещая их в набор свойств, определенный их собственным идентификатором GUID.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="5fa9d-273">1.9. Назначения стандартов</span><span class="sxs-lookup"><span data-stu-id="5fa9d-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="5fa9d-274">Этот протокол не имеет стандартных назначений, а только частные назначения, выполняемые корпорацией Майкрософт с использованием процедур распределения, заданных в других протоколах.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="5fa9d-275">Корпорация Майкрософт выделила этот протокол именованным каналом, как указано в \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="5fa9d-276">Назначение:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-276">The assignment is:</span></span>



| <span data-ttu-id="5fa9d-277">Параметр</span><span class="sxs-lookup"><span data-stu-id="5fa9d-277">Parameter</span></span> | <span data-ttu-id="5fa9d-278">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-278">Value</span></span>             | <span data-ttu-id="5fa9d-279">Справочник</span><span class="sxs-lookup"><span data-stu-id="5fa9d-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="5fa9d-280">Имя канала</span><span class="sxs-lookup"><span data-stu-id="5fa9d-280">Pipe name</span></span> | <span data-ttu-id="5fa9d-281">\\\\скадс элемента конфигурации канала \_</span><span class="sxs-lookup"><span data-stu-id="5fa9d-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="5fa9d-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="5fa9d-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="5fa9d-283">2. Сообщения</span><span class="sxs-lookup"><span data-stu-id="5fa9d-283">2 Messages</span></span>

-   [<span data-ttu-id="5fa9d-284">2.1. Транспортировка</span><span class="sxs-lookup"><span data-stu-id="5fa9d-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="5fa9d-285">2.2. Синтаксис сообщений</span><span class="sxs-lookup"><span data-stu-id="5fa9d-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="5fa9d-286">2.1. Транспортировка</span><span class="sxs-lookup"><span data-stu-id="5fa9d-286">2.1 Transport</span></span>

<span data-ttu-id="5fa9d-287">Все сообщения должны быть перенесены с помощью именованного канала, как указано в \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="5fa9d-288">Используется следующее имя канала:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="5fa9d-289">\\\\скадс элемента конфигурации канала \_</span><span class="sxs-lookup"><span data-stu-id="5fa9d-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="5fa9d-290">Этот протокол использует базовый протокол именованных каналов SMB для получения удостоверения вызывающей стороны, который установил подключение, как указано в разделе 2.2.8 \[ MS-SMB \] ; клиент должен задать идентификатор безопасности в \_ качестве имперсонатионлевел в запросе, чтобы открыть именованный канал.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="5fa9d-291">2.2. Синтаксис сообщений</span><span class="sxs-lookup"><span data-stu-id="5fa9d-291">2.2 Message Syntax</span></span>

<span data-ttu-id="5fa9d-292">Несколько структур и сообщений в следующих разделах относятся к маркерам глав или закладок.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="5fa9d-293">Маркер представляет собой 32-разрядную непрозрачную структуру, которая однозначно определяет главу или закладку.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="5fa9d-294">Как правило, клиентские приложения получают значения обработчиков через вызовы методов; Однако существует несколько хорошо известных значений, которые не нужно получать с сервера, значение которого указано в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="5fa9d-295">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-295">Value</span></span>                         | <span data-ttu-id="5fa9d-296">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-297">База данных \_ null \_ параметру hChapter 0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="5fa9d-298">Маркер главы для набора строк с неразбитым набором, содержащий все результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="5fa9d-299">ДББМК, \_ первый 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="5fa9d-300">Маркер закладки, указывающий первую строку в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="5fa9d-301">ДББМК \_ последний 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="5fa9d-302">Маркер закладки для закладки, определяющей последнюю строку в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="5fa9d-303">2.2.1 структуры</span><span class="sxs-lookup"><span data-stu-id="5fa9d-303">2.2.1 Structures</span></span>

<span data-ttu-id="5fa9d-304">В этом разделе описываются структуры данных, которые определяются и используются CISP.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="5fa9d-305">Все 2-, 4-и 8-байтовые целые числа со знаком и без знака в следующих структурах должны передаваться с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="5fa9d-306">В следующей таблице перечислены структуры данных, определенные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="5fa9d-307">Структура</span><span class="sxs-lookup"><span data-stu-id="5fa9d-307">Structure</span></span>                    | <span data-ttu-id="5fa9d-308">Описание</span><span class="sxs-lookup"><span data-stu-id="5fa9d-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-309">кбасесторажевариант</span><span class="sxs-lookup"><span data-stu-id="5fa9d-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="5fa9d-310">Содержит значение, по которому выполняется операция сопоставления для свойства, указанного в структуре Кпропертирестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="5fa9d-311">SAFEARRAY, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="5fa9d-312">Содержит многомерный массив.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="5fa9d-313">сафеаррайбаунд</span><span class="sxs-lookup"><span data-stu-id="5fa9d-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="5fa9d-314">Представляет границы для измерения массива, указанного в структуре SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="5fa9d-315">кфуллпропспек</span><span class="sxs-lookup"><span data-stu-id="5fa9d-315">CFullPropSpec</span></span>                | <span data-ttu-id="5fa9d-316">Содержит спецификацию свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="5fa9d-317">кконтентрестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-317">CContentRestriction</span></span>          | <span data-ttu-id="5fa9d-318">Содержит строку, соответствующую значению свойства в кэше свойств.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="5fa9d-319">ккэй</span><span class="sxs-lookup"><span data-stu-id="5fa9d-319">CKey</span></span>                         | <span data-ttu-id="5fa9d-320">Содержит значение свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="5fa9d-321">Цинтерналпропертирестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="5fa9d-322">Содержит значение свойства для сопоставления с операцией.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="5fa9d-323">кнатлангуажерестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="5fa9d-324">Содержит запрос на естественном языке для свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="5fa9d-325">кнодерестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-325">CNodeRestriction</span></span>             | <span data-ttu-id="5fa9d-326">Содержит массив узлов дерева команд, задающий ограничения для запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="5fa9d-327">коккрестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-327">COccRestriction</span></span>              | <span data-ttu-id="5fa9d-328">Содержит расположение слова в фразе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="5fa9d-329">кпропертирестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-329">CPropertyRestriction</span></span>         | <span data-ttu-id="5fa9d-330">Содержит значение свойства для сопоставления с операцией.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="5fa9d-331">кранжерестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-331">CRangeRestriction</span></span>            | <span data-ttu-id="5fa9d-332">Содержит ограничение на диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="5fa9d-333">кскоперестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-333">CScopeRestriction</span></span>            | <span data-ttu-id="5fa9d-334">Содержит ограничение на файлы для поиска.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="5fa9d-335">ксорт</span><span class="sxs-lookup"><span data-stu-id="5fa9d-335">CSort</span></span>                        | <span data-ttu-id="5fa9d-336">Определяет столбец для сортировки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="5fa9d-337">ксинрестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-337">CSynRestriction</span></span>              | <span data-ttu-id="5fa9d-338">Содержит слово или его синонимы для фразы запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="5fa9d-339">квекторрестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-339">CVectorRestriction</span></span>           | <span data-ttu-id="5fa9d-340">Содержит взвешенное значение или операцию для узла дерева команд.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="5fa9d-341">квордрестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-341">CWordRestriction</span></span>             | <span data-ttu-id="5fa9d-342">Содержит слово для фразы запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="5fa9d-343">крестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-343">CRestriction</span></span>                 | <span data-ttu-id="5fa9d-344">Содержит узел дерева команд запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="5fa9d-345">кколумнсет</span><span class="sxs-lookup"><span data-stu-id="5fa9d-345">CColumnSet</span></span>                   | <span data-ttu-id="5fa9d-346">Указывает число возвращаемых столбцов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="5fa9d-347">ккатегоризатионсет</span><span class="sxs-lookup"><span data-stu-id="5fa9d-347">CCategorizationSet</span></span>           | <span data-ttu-id="5fa9d-348">Содержит сведения о группировании набора результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="5fa9d-349">ккатегоризатионспек</span><span class="sxs-lookup"><span data-stu-id="5fa9d-349">CCategorizationSpec</span></span>          | <span data-ttu-id="5fa9d-350">Содержит определение категорий, в которых будут классифицироваться результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="5fa9d-351">кдбколид</span><span class="sxs-lookup"><span data-stu-id="5fa9d-351">CDbColId</span></span>                     | <span data-ttu-id="5fa9d-352">Содержит столбец.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="5fa9d-353">кдбпроп</span><span class="sxs-lookup"><span data-stu-id="5fa9d-353">CDbProp</span></span>                      | <span data-ttu-id="5fa9d-354">Содержит свойство.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="5fa9d-355">кдбпропсет</span><span class="sxs-lookup"><span data-stu-id="5fa9d-355">CDbPropSet</span></span>                   | <span data-ttu-id="5fa9d-356">Содержит набор свойств.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="5fa9d-357">кпидмаппер</span><span class="sxs-lookup"><span data-stu-id="5fa9d-357">CPidMapper</span></span>                   | <span data-ttu-id="5fa9d-358">Содержит массив идентификаторов свойств, указывающих свойства, возвращаемые в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="5fa9d-359">кровсикат</span><span class="sxs-lookup"><span data-stu-id="5fa9d-359">CRowSeekAt</span></span>                   | <span data-ttu-id="5fa9d-360">Содержит смещение для получения строк в сообщении Кпмжетровсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="5fa9d-361">кровсикатратио</span><span class="sxs-lookup"><span data-stu-id="5fa9d-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="5fa9d-362">Определяет точку, с которой начинается извлечение сообщения Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="5fa9d-363">кровсикбибукмарк</span><span class="sxs-lookup"><span data-stu-id="5fa9d-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="5fa9d-364">Определяет закладки, из которых извлекаются строки для сообщения Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="5fa9d-365">кровсикнекст</span><span class="sxs-lookup"><span data-stu-id="5fa9d-365">CRowSeekNext</span></span>                 | <span data-ttu-id="5fa9d-366">Содержит число строк, которые необходимо пропустить в сообщении Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="5fa9d-367">кровсетпропертиес</span><span class="sxs-lookup"><span data-stu-id="5fa9d-367">CRowsetProperties</span></span>            | <span data-ttu-id="5fa9d-368">Содержит сведения о конфигурации для запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="5fa9d-369">ксортсет</span><span class="sxs-lookup"><span data-stu-id="5fa9d-369">CSortSet</span></span>                     | <span data-ttu-id="5fa9d-370">Содержит порядок сортировки для запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="5fa9d-371">ктаблеколумн</span><span class="sxs-lookup"><span data-stu-id="5fa9d-371">CTableColumn</span></span>                 | <span data-ttu-id="5fa9d-372">Содержит столбец для сообщения Кпмсетбиндингс.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="5fa9d-373">сериализедпропертивалуе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="5fa9d-374">Содержит сериализованное значение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="5fa9d-375">2.2.1.1 Кбасесторажевариант</span><span class="sxs-lookup"><span data-stu-id="5fa9d-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="5fa9d-376">Структура Кбасесторажевариант содержит значение, по которому выполняется операция сопоставления для свойства, указанного в структуре Кпропертирестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="5fa9d-377">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-377">0</span></span>

<span data-ttu-id="5fa9d-378">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-378">1</span></span>

<span data-ttu-id="5fa9d-379">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-379">2</span></span>

<span data-ttu-id="5fa9d-380">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-380">3</span></span>

<span data-ttu-id="5fa9d-381">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-381">4</span></span>

<span data-ttu-id="5fa9d-382">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-382">5</span></span>

<span data-ttu-id="5fa9d-383">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-383">6</span></span>

<span data-ttu-id="5fa9d-384">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-384">7</span></span>

<span data-ttu-id="5fa9d-385">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-385">8</span></span>

<span data-ttu-id="5fa9d-386">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-386">9</span></span>

<span data-ttu-id="5fa9d-387">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-387">1</span></span><br/> <span data-ttu-id="5fa9d-388">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-388">0</span></span><br/>

<span data-ttu-id="5fa9d-389">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-389">1</span></span>

<span data-ttu-id="5fa9d-390">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-390">2</span></span>

<span data-ttu-id="5fa9d-391">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-391">3</span></span>

<span data-ttu-id="5fa9d-392">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-392">4</span></span>

<span data-ttu-id="5fa9d-393">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-393">5</span></span>

<span data-ttu-id="5fa9d-394">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-394">6</span></span>

<span data-ttu-id="5fa9d-395">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-395">7</span></span>

<span data-ttu-id="5fa9d-396">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-396">8</span></span>

<span data-ttu-id="5fa9d-397">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-397">9</span></span>

<span data-ttu-id="5fa9d-398">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-398">2</span></span><br/> <span data-ttu-id="5fa9d-399">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-399">0</span></span><br/>

<span data-ttu-id="5fa9d-400">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-400">1</span></span>

<span data-ttu-id="5fa9d-401">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-401">2</span></span>

<span data-ttu-id="5fa9d-402">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-402">3</span></span>

<span data-ttu-id="5fa9d-403">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-403">4</span></span>

<span data-ttu-id="5fa9d-404">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-404">5</span></span>

<span data-ttu-id="5fa9d-405">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-405">6</span></span>

<span data-ttu-id="5fa9d-406">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-406">7</span></span>

<span data-ttu-id="5fa9d-407">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-407">8</span></span>

<span data-ttu-id="5fa9d-408">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-408">9</span></span>

<span data-ttu-id="5fa9d-409">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-409">3</span></span><br/> <span data-ttu-id="5fa9d-410">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-410">0</span></span><br/>

<span data-ttu-id="5fa9d-411">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-411">1</span></span>

<span data-ttu-id="5fa9d-412">втипе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-412">vType</span></span>

<span data-ttu-id="5fa9d-413">vData1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-413">vData1</span></span>

<span data-ttu-id="5fa9d-414">vData2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-414">vData2</span></span>

<span data-ttu-id="5fa9d-415">Управляемое vValue (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-415">vValue (variable)</span></span>



 

<span data-ttu-id="5fa9d-416">**втипе**: признак типа, указывающий тип управляемое vValue.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="5fa9d-417">Это должно быть одно из значений VARENUM, указанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="5fa9d-418">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-418">Value</span></span>                 | <span data-ttu-id="5fa9d-419">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-420">VT \_ Empty (символ 0x0000)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="5fa9d-421">Управляемое vValue отсутствует.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="5fa9d-422">VT \_ null (0x0001)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="5fa9d-423">Управляемое vValue отсутствует.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="5fa9d-424">VT \_ I1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="5fa9d-425">1-байтовое целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="5fa9d-426">VT \_ UI1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="5fa9d-427">1-байтовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="5fa9d-428">VT \_ I2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="5fa9d-429">2-байтовое целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="5fa9d-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="5fa9d-431">2-байтовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="5fa9d-432">Логическое значение VT \_ (0x000B)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="5fa9d-433">Логическое значение; 2-байтовое целое число, содержащее символ 0x0000 (FALSE) или 0xFFFF (TRUE).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="5fa9d-434">VT \_ I4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="5fa9d-435">4-байтовое целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="5fa9d-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="5fa9d-437">4-байтовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="5fa9d-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="5fa9d-439">32-разрядное число с плавающей запятой, определенное в \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="5fa9d-440">VT \_ int (0x0016)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="5fa9d-441">4-байтовое целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="5fa9d-442">VT \_ uint (0x0017)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="5fa9d-443">4-байтовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="5fa9d-444">\_Ошибка VT (0x000A)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="5fa9d-445">4-байтовое целое число без знака, содержащее значение HRESULT, как указано в \[ MS-sys \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="5fa9d-446">VT \_ I8 (0x0014)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="5fa9d-447">8 байт целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="5fa9d-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="5fa9d-449">8-байтовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="5fa9d-450">VT \_ R8 (0x0005)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="5fa9d-451">64-разрядное число с плавающей запятой, определенное в \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="5fa9d-452">VT \_ CY (0x0006)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="5fa9d-453">8-байтное дополнение к целому числу (с масштабированием на 10 000).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="5fa9d-454">\_Дата VT (0x0007)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="5fa9d-455">64-разрядное число с плавающей запятой, представляющее количество дней с момента 00:00:00 31 декабря 1899 (координированное время в формате UTC).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="5fa9d-456">VT \_ fileTime (0x0040)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="5fa9d-457">64-разрядное целое число, представляющее число интервалов 100-наносекундных с 00:00:00 по 1 января 1601 г. (координированное время в формате UTC).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="5fa9d-458">VT \_ Decimal (0x000E)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="5fa9d-459">ДЕСЯТИЧная структура, как указано в разделе 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="5fa9d-460">VT \_ CLSID (0x0048)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="5fa9d-461">16-байтовое двоичное значение, содержащее идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="5fa9d-462">\_Большой двоичный объект VT (0x0041)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="5fa9d-463">Целое число без знака размером 4 байта в большом двоичном объекте, за которым следует множество байтов данных.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="5fa9d-464">VT \_ BSTR (0x0008)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="5fa9d-465">Целое число без знака длиной 4 байта в строке, за которым следует строка, как указано ниже в разделе управляемое vValue.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="5fa9d-466">VT \_ LPSTR (0x001E)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="5fa9d-467">Строка ANSI, заканчивающаяся нулем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="5fa9d-468">VT \_ LPWSTR (0x001F)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="5fa9d-469">Строка Юникода в Юникоде, заканчивающаяся нулем \[ \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="5fa9d-470">\_Вариант VT (0x000C)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="5fa9d-471">Кбасесторажевариант.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-471">CBaseStorageVariant.</span></span> <span data-ttu-id="5fa9d-472">НЕОБХОДИМО сочетать с модификатором типа в \_ массиве VT или в \_ векторе VT.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="5fa9d-473">В следующей таблице указаны модификаторы типа для Втипе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="5fa9d-474">Модификаторы типа могут быть двоичными ORed с Втипе, чтобы изменить значение управляемое vValue, чтобы указать, что это один из двух возможных типов массивов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="5fa9d-475">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-475">Value</span></span>               | <span data-ttu-id="5fa9d-476">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-477">\_Вектор VT (0x1000)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="5fa9d-478">Если индикатор типа сочетается с \_ вектором VT с помощью оператора OR, управляемое vValue является подсчитанным массивом значений указанного типа.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="5fa9d-479">Дополнительные сведения см. в разделе 2.2.1.1.1.2.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="5fa9d-480">Этот модификатор типа не должен сочетаться со следующими типами: VT \_ int, VT \_ uint, Decimal, VT \_ , BLOB- \_ \_ объект VT \_ .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="5fa9d-481">\_Массив VT (0x2000)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="5fa9d-482">Если индикатор типа сочетается с \_ массивом VT с помощью оператора OR, это значение является массивом SAFEARRAY (как указано в разделе 2.2.1.1.1.3), содержащим значения указанного типа.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="5fa9d-483">Этот модификатор типа не должен сочетаться со следующими типами: VT \_ i8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, \_ BLOB VT, \_ \_ объект объекта VT, VT \_ LPSTR, VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="5fa9d-484">**vData1**: Если втипе имеет тип VT \_ Decimal, значение этого поля указывается в качестве поля масштабирования в разделе 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="5fa9d-485">Для всех остальных Втипес значение должно быть равно 0x00.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="5fa9d-486">**vData2**: Если втипе имеет тип VT \_ Decimal, значение этого поля указывается как поле подписи в разделе 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="5fa9d-487">Для всех остальных Втипес значение должно быть равно 0x00.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="5fa9d-488">**управляемое vValue**: значение для операции сопоставления.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="5fa9d-489">Синтаксис должен быть указан в поле Втипе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="5fa9d-490">В следующей таблице приведены размеры для поля управляемое vValue, зависящие от поля Втипе для типов данных фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="5fa9d-491">Размер указан в байтах.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-491">The size is in bytes.</span></span>



| <span data-ttu-id="5fa9d-492">втипе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-492">vType</span></span>                                                   | <span data-ttu-id="5fa9d-493">Размер</span><span class="sxs-lookup"><span data-stu-id="5fa9d-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="5fa9d-494">VT \_ I1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="5fa9d-495">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-495">1</span></span>    |
| <span data-ttu-id="5fa9d-496">VT \_ I2, VT \_ UI2, логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="5fa9d-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="5fa9d-497">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-497">2</span></span>    |
| <span data-ttu-id="5fa9d-498">VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ int, VT \_ uint, \_ Ошибка VT</span><span class="sxs-lookup"><span data-stu-id="5fa9d-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="5fa9d-499">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-499">4</span></span>    |
| <span data-ttu-id="5fa9d-500">VT \_ i8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ , VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="5fa9d-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="5fa9d-501">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-501">8</span></span>    |
| <span data-ttu-id="5fa9d-502">VT \_ Decimal, VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="5fa9d-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="5fa9d-503">16</span><span class="sxs-lookup"><span data-stu-id="5fa9d-503">16</span></span>   |



 

<span data-ttu-id="5fa9d-504">Если для Втипе задано значение VT \_ BLOB, VT \_ BSTR или VT LPSTR, то \_ Структура управляемое vValue указана на следующей схеме:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="5fa9d-505">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-505">0</span></span>

<span data-ttu-id="5fa9d-506">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-506">1</span></span>

<span data-ttu-id="5fa9d-507">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-507">2</span></span>

<span data-ttu-id="5fa9d-508">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-508">3</span></span>

<span data-ttu-id="5fa9d-509">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-509">4</span></span>

<span data-ttu-id="5fa9d-510">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-510">5</span></span>

<span data-ttu-id="5fa9d-511">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-511">6</span></span>

<span data-ttu-id="5fa9d-512">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-512">7</span></span>

<span data-ttu-id="5fa9d-513">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-513">8</span></span>

<span data-ttu-id="5fa9d-514">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-514">9</span></span>

<span data-ttu-id="5fa9d-515">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-515">1</span></span><br/> <span data-ttu-id="5fa9d-516">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-516">0</span></span><br/>

<span data-ttu-id="5fa9d-517">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-517">1</span></span>

<span data-ttu-id="5fa9d-518">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-518">2</span></span>

<span data-ttu-id="5fa9d-519">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-519">3</span></span>

<span data-ttu-id="5fa9d-520">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-520">4</span></span>

<span data-ttu-id="5fa9d-521">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-521">5</span></span>

<span data-ttu-id="5fa9d-522">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-522">6</span></span>

<span data-ttu-id="5fa9d-523">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-523">7</span></span>

<span data-ttu-id="5fa9d-524">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-524">8</span></span>

<span data-ttu-id="5fa9d-525">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-525">9</span></span>

<span data-ttu-id="5fa9d-526">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-526">2</span></span><br/> <span data-ttu-id="5fa9d-527">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-527">0</span></span><br/>

<span data-ttu-id="5fa9d-528">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-528">1</span></span>

<span data-ttu-id="5fa9d-529">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-529">2</span></span>

<span data-ttu-id="5fa9d-530">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-530">3</span></span>

<span data-ttu-id="5fa9d-531">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-531">4</span></span>

<span data-ttu-id="5fa9d-532">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-532">5</span></span>

<span data-ttu-id="5fa9d-533">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-533">6</span></span>

<span data-ttu-id="5fa9d-534">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-534">7</span></span>

<span data-ttu-id="5fa9d-535">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-535">8</span></span>

<span data-ttu-id="5fa9d-536">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-536">9</span></span>

<span data-ttu-id="5fa9d-537">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-537">3</span></span><br/> <span data-ttu-id="5fa9d-538">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-538">0</span></span><br/>

<span data-ttu-id="5fa9d-539">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-539">1</span></span>

<span data-ttu-id="5fa9d-540">кбсизе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-540">cbSize</span></span>

<span data-ttu-id="5fa9d-541">Блобдата (переменная, необязательный)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="5fa9d-542">**кбсизе**: 32-разрядное целое число без знака, указывающее размер поля блобдата в байтах.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="5fa9d-543">Если Втипе имеет значение VT \_ BSTR или VT \_ LPSTR, для кбсизе должно быть задано значение 0x00000000, если представленная строка является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="5fa9d-544">**блобдата**: длина должна быть кбсизе в байтах.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="5fa9d-545">Если для Втипе задано значение VT \_ BLOB, это поле будет иметь непрозрачные двоичные данные BLOB.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="5fa9d-546">Для Втипе, установленного в VT \_ BSTR, это поле представляет собой набор символов в выбранной кодировке OEM.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="5fa9d-547">Клиент и сервер должны быть настроены для использования набора символов с возможностью взаимодействия (по протоколу внешнего вида протокола).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="5fa9d-548">Нет необходимости завершать его нулем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="5fa9d-549">Для Втипе, установленного в VT \_ LPSTR, это поле является строкой символов, завершающейся нулем, в выбранной кодировке OEM.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="5fa9d-550">Клиент и сервер должны быть настроены для использования набора символов с возможностью взаимодействия (по протоколу внешнего вида протокола).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="5fa9d-551">Если Втипе имеет значение VT \_ LPWSTR, структура управляемое vValue указывается на следующей схеме:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="5fa9d-552">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-552">0</span></span>

<span data-ttu-id="5fa9d-553">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-553">1</span></span>

<span data-ttu-id="5fa9d-554">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-554">2</span></span>

<span data-ttu-id="5fa9d-555">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-555">3</span></span>

<span data-ttu-id="5fa9d-556">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-556">4</span></span>

<span data-ttu-id="5fa9d-557">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-557">5</span></span>

<span data-ttu-id="5fa9d-558">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-558">6</span></span>

<span data-ttu-id="5fa9d-559">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-559">7</span></span>

<span data-ttu-id="5fa9d-560">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-560">8</span></span>

<span data-ttu-id="5fa9d-561">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-561">9</span></span>

<span data-ttu-id="5fa9d-562">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-562">1</span></span><br/> <span data-ttu-id="5fa9d-563">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-563">0</span></span><br/>

<span data-ttu-id="5fa9d-564">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-564">1</span></span>

<span data-ttu-id="5fa9d-565">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-565">2</span></span>

<span data-ttu-id="5fa9d-566">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-566">3</span></span>

<span data-ttu-id="5fa9d-567">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-567">4</span></span>

<span data-ttu-id="5fa9d-568">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-568">5</span></span>

<span data-ttu-id="5fa9d-569">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-569">6</span></span>

<span data-ttu-id="5fa9d-570">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-570">7</span></span>

<span data-ttu-id="5fa9d-571">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-571">8</span></span>

<span data-ttu-id="5fa9d-572">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-572">9</span></span>

<span data-ttu-id="5fa9d-573">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-573">2</span></span><br/> <span data-ttu-id="5fa9d-574">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-574">0</span></span><br/>

<span data-ttu-id="5fa9d-575">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-575">1</span></span>

<span data-ttu-id="5fa9d-576">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-576">2</span></span>

<span data-ttu-id="5fa9d-577">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-577">3</span></span>

<span data-ttu-id="5fa9d-578">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-578">4</span></span>

<span data-ttu-id="5fa9d-579">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-579">5</span></span>

<span data-ttu-id="5fa9d-580">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-580">6</span></span>

<span data-ttu-id="5fa9d-581">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-581">7</span></span>

<span data-ttu-id="5fa9d-582">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-582">8</span></span>

<span data-ttu-id="5fa9d-583">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-583">9</span></span>

<span data-ttu-id="5fa9d-584">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-584">3</span></span><br/> <span data-ttu-id="5fa9d-585">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-585">0</span></span><br/>

<span data-ttu-id="5fa9d-586">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-586">1</span></span>

<span data-ttu-id="5fa9d-587">кклен</span><span class="sxs-lookup"><span data-stu-id="5fa9d-587">ccLen</span></span>

<span data-ttu-id="5fa9d-588">String (переменная, необязательная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-588">string (variable, optional)</span></span>



 

<span data-ttu-id="5fa9d-589">**кклен**: 32-разрядное целое число без знака, указывающее размер строкового поля в символах Юникода.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="5fa9d-590">Для пустой строки необходимо задать значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="5fa9d-591">**строка**: строка Юникода, заканчивающаяся нулем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="5fa9d-592">2.2.1.1.1 Кбасесторажевариант структуры</span><span class="sxs-lookup"><span data-stu-id="5fa9d-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="5fa9d-593">В структуре Кбасесторажевариант используются следующие структуры.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="5fa9d-594">2.2.1.1.1.1 DECIMAL</span><span class="sxs-lookup"><span data-stu-id="5fa9d-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="5fa9d-595">Значение DECIMAL используется для представления точного числового значения с фиксированной точностью и фиксированным масштабом.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="5fa9d-596">Если для Втипе задано значение VT \_ Decimal (0x0000E), то поля vData1 и vData2 в КБАСЕСТОРАЖЕВАРИАНТ должны интерпретироваться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="5fa9d-597">**vData1**: количество цифр справа от десятичной запятой.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="5fa9d-598">Значение должно находиться в диапазоне от 0 до 28.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="5fa9d-599">**vData2**: знак числового значения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="5fa9d-600">Задайте значение 0x00, если положительный, 0x80, если отрицательный.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="5fa9d-601">Формат поля управляемое vValue:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-601">The format of the vValue field is:</span></span>



<span data-ttu-id="5fa9d-602">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-602">0</span></span>

<span data-ttu-id="5fa9d-603">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-603">1</span></span>

<span data-ttu-id="5fa9d-604">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-604">2</span></span>

<span data-ttu-id="5fa9d-605">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-605">3</span></span>

<span data-ttu-id="5fa9d-606">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-606">4</span></span>

<span data-ttu-id="5fa9d-607">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-607">5</span></span>

<span data-ttu-id="5fa9d-608">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-608">6</span></span>

<span data-ttu-id="5fa9d-609">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-609">7</span></span>

<span data-ttu-id="5fa9d-610">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-610">8</span></span>

<span data-ttu-id="5fa9d-611">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-611">9</span></span>

<span data-ttu-id="5fa9d-612">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-612">1</span></span><br/> <span data-ttu-id="5fa9d-613">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-613">0</span></span><br/>

<span data-ttu-id="5fa9d-614">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-614">1</span></span>

<span data-ttu-id="5fa9d-615">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-615">2</span></span>

<span data-ttu-id="5fa9d-616">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-616">3</span></span>

<span data-ttu-id="5fa9d-617">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-617">4</span></span>

<span data-ttu-id="5fa9d-618">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-618">5</span></span>

<span data-ttu-id="5fa9d-619">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-619">6</span></span>

<span data-ttu-id="5fa9d-620">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-620">7</span></span>

<span data-ttu-id="5fa9d-621">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-621">8</span></span>

<span data-ttu-id="5fa9d-622">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-622">9</span></span>

<span data-ttu-id="5fa9d-623">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-623">2</span></span><br/> <span data-ttu-id="5fa9d-624">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-624">0</span></span><br/>

<span data-ttu-id="5fa9d-625">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-625">1</span></span>

<span data-ttu-id="5fa9d-626">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-626">2</span></span>

<span data-ttu-id="5fa9d-627">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-627">3</span></span>

<span data-ttu-id="5fa9d-628">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-628">4</span></span>

<span data-ttu-id="5fa9d-629">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-629">5</span></span>

<span data-ttu-id="5fa9d-630">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-630">6</span></span>

<span data-ttu-id="5fa9d-631">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-631">7</span></span>

<span data-ttu-id="5fa9d-632">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-632">8</span></span>

<span data-ttu-id="5fa9d-633">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-633">9</span></span>

<span data-ttu-id="5fa9d-634">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-634">3</span></span><br/> <span data-ttu-id="5fa9d-635">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-635">0</span></span><br/>

<span data-ttu-id="5fa9d-636">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-636">1</span></span>

<span data-ttu-id="5fa9d-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="5fa9d-637">Hi32</span></span>

<span data-ttu-id="5fa9d-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="5fa9d-638">Lo32</span></span>

<span data-ttu-id="5fa9d-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="5fa9d-639">Mid32</span></span>



 

<span data-ttu-id="5fa9d-640">**Hi32**: наибольшее число 32 бит 96 разрядов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="5fa9d-641">**Lo32**: младшие 32 бита 96 разрядного целого числа.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="5fa9d-642">**Mid32**: середина 32 бит 96 разрядного целого числа.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="5fa9d-643">вектор 2.2.1.1.1.2 VT \_</span><span class="sxs-lookup"><span data-stu-id="5fa9d-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="5fa9d-644">\_Вектор VT используется для передачи одномерных массивов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="5fa9d-645">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-645">0</span></span>

<span data-ttu-id="5fa9d-646">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-646">1</span></span>

<span data-ttu-id="5fa9d-647">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-647">2</span></span>

<span data-ttu-id="5fa9d-648">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-648">3</span></span>

<span data-ttu-id="5fa9d-649">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-649">4</span></span>

<span data-ttu-id="5fa9d-650">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-650">5</span></span>

<span data-ttu-id="5fa9d-651">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-651">6</span></span>

<span data-ttu-id="5fa9d-652">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-652">7</span></span>

<span data-ttu-id="5fa9d-653">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-653">8</span></span>

<span data-ttu-id="5fa9d-654">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-654">9</span></span>

<span data-ttu-id="5fa9d-655">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-655">1</span></span><br/> <span data-ttu-id="5fa9d-656">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-656">0</span></span><br/>

<span data-ttu-id="5fa9d-657">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-657">1</span></span>

<span data-ttu-id="5fa9d-658">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-658">2</span></span>

<span data-ttu-id="5fa9d-659">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-659">3</span></span>

<span data-ttu-id="5fa9d-660">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-660">4</span></span>

<span data-ttu-id="5fa9d-661">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-661">5</span></span>

<span data-ttu-id="5fa9d-662">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-662">6</span></span>

<span data-ttu-id="5fa9d-663">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-663">7</span></span>

<span data-ttu-id="5fa9d-664">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-664">8</span></span>

<span data-ttu-id="5fa9d-665">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-665">9</span></span>

<span data-ttu-id="5fa9d-666">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-666">2</span></span><br/> <span data-ttu-id="5fa9d-667">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-667">0</span></span><br/>

<span data-ttu-id="5fa9d-668">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-668">1</span></span>

<span data-ttu-id="5fa9d-669">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-669">2</span></span>

<span data-ttu-id="5fa9d-670">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-670">3</span></span>

<span data-ttu-id="5fa9d-671">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-671">4</span></span>

<span data-ttu-id="5fa9d-672">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-672">5</span></span>

<span data-ttu-id="5fa9d-673">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-673">6</span></span>

<span data-ttu-id="5fa9d-674">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-674">7</span></span>

<span data-ttu-id="5fa9d-675">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-675">8</span></span>

<span data-ttu-id="5fa9d-676">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-676">9</span></span>

<span data-ttu-id="5fa9d-677">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-677">3</span></span><br/> <span data-ttu-id="5fa9d-678">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-678">0</span></span><br/>

<span data-ttu-id="5fa9d-679">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-679">1</span></span>

<span data-ttu-id="5fa9d-680">ввекторелементс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-680">vVectorElements</span></span>

<span data-ttu-id="5fa9d-681">ввектордата</span><span class="sxs-lookup"><span data-stu-id="5fa9d-681">vVectorData</span></span>



 

<span data-ttu-id="5fa9d-682">**ввекторелементс**: 32-разрядное целое число без знака, указывающее количество элементов в поле ввектордата.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="5fa9d-683">**ввектордата**: массив элементов, имеющих тип, обозначенный параметром втипе с сброшенным битом 0x1000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="5fa9d-684">Размер отдельного элемента фиксированной длины можно получить из таблицы типов данных фиксированной длины, как указано в разделе 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="5fa9d-685">Длина этого поля в байтах может быть вычислена путем умножения Ввекторелементс на размер отдельного элемента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="5fa9d-686">Для типов данных переменной длины Ввектордата содержит последовательность последовательных упакованных простых типов, где тип обозначается параметром Втипе с сброшенным битом 0x1000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="5fa9d-687">Это включает особый случай, обозначенный Втипе VT \_ array \| VT \_ (т. е. 0x100C).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="5fa9d-688">Элементы в поле Ввектордата должны быть разделены от 0 до 3 байтов, чтобы каждый элемент начинался со смещения, кратного 4 байтам от начала сообщения, содержащего этот массив.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="5fa9d-689">Если заданы байты заполнения, то значение, которое они содержат, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="5fa9d-690">Содержимое байтов заполнения должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="5fa9d-691">Для Втипе, установленного в VT \_ array \| VT \_ , тип для элементов в этой последовательности — кбасесторажевариант.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="5fa9d-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="5fa9d-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="5fa9d-693">SAFEARRAY используется для передачи многомерных массивов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="5fa9d-694">Структура содержит сведения о размере массива, а также данные в массиве.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="5fa9d-695">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-695">0</span></span>

<span data-ttu-id="5fa9d-696">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-696">1</span></span>

<span data-ttu-id="5fa9d-697">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-697">2</span></span>

<span data-ttu-id="5fa9d-698">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-698">3</span></span>

<span data-ttu-id="5fa9d-699">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-699">4</span></span>

<span data-ttu-id="5fa9d-700">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-700">5</span></span>

<span data-ttu-id="5fa9d-701">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-701">6</span></span>

<span data-ttu-id="5fa9d-702">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-702">7</span></span>

<span data-ttu-id="5fa9d-703">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-703">8</span></span>

<span data-ttu-id="5fa9d-704">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-704">9</span></span>

<span data-ttu-id="5fa9d-705">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-705">1</span></span><br/> <span data-ttu-id="5fa9d-706">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-706">0</span></span><br/>

<span data-ttu-id="5fa9d-707">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-707">1</span></span>

<span data-ttu-id="5fa9d-708">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-708">2</span></span>

<span data-ttu-id="5fa9d-709">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-709">3</span></span>

<span data-ttu-id="5fa9d-710">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-710">4</span></span>

<span data-ttu-id="5fa9d-711">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-711">5</span></span>

<span data-ttu-id="5fa9d-712">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-712">6</span></span>

<span data-ttu-id="5fa9d-713">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-713">7</span></span>

<span data-ttu-id="5fa9d-714">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-714">8</span></span>

<span data-ttu-id="5fa9d-715">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-715">9</span></span>

<span data-ttu-id="5fa9d-716">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-716">2</span></span><br/> <span data-ttu-id="5fa9d-717">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-717">0</span></span><br/>

<span data-ttu-id="5fa9d-718">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-718">1</span></span>

<span data-ttu-id="5fa9d-719">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-719">2</span></span>

<span data-ttu-id="5fa9d-720">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-720">3</span></span>

<span data-ttu-id="5fa9d-721">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-721">4</span></span>

<span data-ttu-id="5fa9d-722">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-722">5</span></span>

<span data-ttu-id="5fa9d-723">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-723">6</span></span>

<span data-ttu-id="5fa9d-724">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-724">7</span></span>

<span data-ttu-id="5fa9d-725">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-725">8</span></span>

<span data-ttu-id="5fa9d-726">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-726">9</span></span>

<span data-ttu-id="5fa9d-727">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-727">3</span></span><br/> <span data-ttu-id="5fa9d-728">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-728">0</span></span><br/>

<span data-ttu-id="5fa9d-729">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-729">1</span></span>

<span data-ttu-id="5fa9d-730">кдимс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-730">cDims</span></span>

<span data-ttu-id="5fa9d-731">ффеатурес</span><span class="sxs-lookup"><span data-stu-id="5fa9d-731">fFeatures</span></span>

<span data-ttu-id="5fa9d-732">кбелементс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-732">cbElements</span></span>

<span data-ttu-id="5fa9d-733">Ргсабаунд (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-733">Rgsabound (variable)</span></span>

<span data-ttu-id="5fa9d-734">Вдата (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-734">vData (variable)</span></span>



 

<span data-ttu-id="5fa9d-735">**кдимс**: 16-разрядное целое число без знака, указывающее количество измерений многомерного массива.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="5fa9d-736">**ффеатурес**: 16-разрядное битовое значение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="5fa9d-737">Значения представляют функции, определенные приложениями верхнего уровня, и должны игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="5fa9d-738">**кбелементс**: 32-битовое целое число без знака, указывающее размер каждого элемента массива.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="5fa9d-739">**Ргсабаунд**: массив, содержащий одну структуру сафеаррайбаунд, как указано в разделе 2.2.1.1.1.4, для измерения в массиве SafeArray.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="5fa9d-740">В этом массиве сначала находится крайне левое измерение, а в последнем — крайнее правое измерение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="5fa9d-741">**вдата**: вектор упакованных элементов определенного типа, обозначенный втипеом содержащего кбасесторажевариант, с битом 0x2000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="5fa9d-742">Вдата маршалируется аналогично \_ вектору VT, как указано в разделе 2.2.1.1.1.2, с разницей, что число элементов не сохраняется перед вектором.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="5fa9d-743">Вместо этого число элементов вычисляется путем умножения значения Целементс на все защищенные границы массива, заданные в поле Ргсабаунд.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="5fa9d-744">Элементы хранятся в векторе в порядке измерений, начиная с крайнего правого измерения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="5fa9d-745">Следующая диаграмма наглядно представляет пример двумерного массива.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="5fa9d-746">Первое измерение имеет Целементс, равное 4 (представлен горизонтально) и Ллбаунд равно 0, а второе измерение имеет Целементс, равное 2 (представлен вертикально), а Ллбаунд равно 0.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>



|            |            |            |            |
|------------|------------|------------|------------|
| <span data-ttu-id="5fa9d-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-747">0x00000001</span></span> | <span data-ttu-id="5fa9d-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-748">0x00000002</span></span> | <span data-ttu-id="5fa9d-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-749">0x00000003</span></span> | <span data-ttu-id="5fa9d-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="5fa9d-750">0x00000005</span></span> |
| <span data-ttu-id="5fa9d-751">0x00000007</span><span class="sxs-lookup"><span data-stu-id="5fa9d-751">0x00000007</span></span> | <span data-ttu-id="5fa9d-752">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5fa9d-752">0x00000011</span></span> | <span data-ttu-id="5fa9d-753">0x00000013</span><span class="sxs-lookup"><span data-stu-id="5fa9d-753">0x00000013</span></span> | <span data-ttu-id="5fa9d-754">0x00000017</span><span class="sxs-lookup"><span data-stu-id="5fa9d-754">0x00000017</span></span> |



 

<span data-ttu-id="5fa9d-755">С помощью приведенной выше схемы Вдата будет содержать следующую последовательность: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (сначала просматривая крайнее правое измерение, а затем увеличив следующее измерение).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-755">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="5fa9d-756">Предыдущая Ргсабаунд (которая регистрирует Целементс и LBound) будет выглядеть следующим образом: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-756">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="5fa9d-757">2.2.1.1.1.4 САФЕАРРАЙБАУНД</span><span class="sxs-lookup"><span data-stu-id="5fa9d-757">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="5fa9d-758">Структура САФЕАРРАЙБАУНД представляет границы одного измерения SAFEARRAY или SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-758">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="5fa9d-759">Он имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-759">Its format is:</span></span>



<span data-ttu-id="5fa9d-760">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-760">0</span></span>

<span data-ttu-id="5fa9d-761">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-761">1</span></span>

<span data-ttu-id="5fa9d-762">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-762">2</span></span>

<span data-ttu-id="5fa9d-763">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-763">3</span></span>

<span data-ttu-id="5fa9d-764">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-764">4</span></span>

<span data-ttu-id="5fa9d-765">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-765">5</span></span>

<span data-ttu-id="5fa9d-766">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-766">6</span></span>

<span data-ttu-id="5fa9d-767">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-767">7</span></span>

<span data-ttu-id="5fa9d-768">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-768">8</span></span>

<span data-ttu-id="5fa9d-769">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-769">9</span></span>

<span data-ttu-id="5fa9d-770">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-770">1</span></span><br/> <span data-ttu-id="5fa9d-771">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-771">0</span></span><br/>

<span data-ttu-id="5fa9d-772">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-772">1</span></span>

<span data-ttu-id="5fa9d-773">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-773">2</span></span>

<span data-ttu-id="5fa9d-774">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-774">3</span></span>

<span data-ttu-id="5fa9d-775">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-775">4</span></span>

<span data-ttu-id="5fa9d-776">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-776">5</span></span>

<span data-ttu-id="5fa9d-777">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-777">6</span></span>

<span data-ttu-id="5fa9d-778">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-778">7</span></span>

<span data-ttu-id="5fa9d-779">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-779">8</span></span>

<span data-ttu-id="5fa9d-780">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-780">9</span></span>

<span data-ttu-id="5fa9d-781">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-781">2</span></span><br/> <span data-ttu-id="5fa9d-782">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-782">0</span></span><br/>

<span data-ttu-id="5fa9d-783">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-783">1</span></span>

<span data-ttu-id="5fa9d-784">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-784">2</span></span>

<span data-ttu-id="5fa9d-785">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-785">3</span></span>

<span data-ttu-id="5fa9d-786">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-786">4</span></span>

<span data-ttu-id="5fa9d-787">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-787">5</span></span>

<span data-ttu-id="5fa9d-788">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-788">6</span></span>

<span data-ttu-id="5fa9d-789">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-789">7</span></span>

<span data-ttu-id="5fa9d-790">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-790">8</span></span>

<span data-ttu-id="5fa9d-791">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-791">9</span></span>

<span data-ttu-id="5fa9d-792">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-792">3</span></span><br/> <span data-ttu-id="5fa9d-793">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-793">0</span></span><br/>

<span data-ttu-id="5fa9d-794">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-794">1</span></span>

<span data-ttu-id="5fa9d-795">целементс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-795">cElements</span></span>

<span data-ttu-id="5fa9d-796">ллбаунд</span><span class="sxs-lookup"><span data-stu-id="5fa9d-796">lLbound</span></span>



 

<span data-ttu-id="5fa9d-797">**целементс**: 32-битовое целое число без знака, указывающее количество элементов в измерении.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-797">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="5fa9d-798">**ллбаунд**: 32-битовое целое число без знака, задающее нижнюю границу измерения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-798">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="5fa9d-799">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-799">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="5fa9d-800">SAFEARRAY2 используется для передачи многомерных массивов в СЕРИАЛИЗЕДПРОПЕРТИВАЛУЕ.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-800">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="5fa9d-801">Структура содержит сведения о границах, а также данные.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-801">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="5fa9d-802">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-802">0</span></span>

<span data-ttu-id="5fa9d-803">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-803">1</span></span>

<span data-ttu-id="5fa9d-804">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-804">2</span></span>

<span data-ttu-id="5fa9d-805">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-805">3</span></span>

<span data-ttu-id="5fa9d-806">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-806">4</span></span>

<span data-ttu-id="5fa9d-807">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-807">5</span></span>

<span data-ttu-id="5fa9d-808">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-808">6</span></span>

<span data-ttu-id="5fa9d-809">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-809">7</span></span>

<span data-ttu-id="5fa9d-810">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-810">8</span></span>

<span data-ttu-id="5fa9d-811">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-811">9</span></span>

<span data-ttu-id="5fa9d-812">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-812">1</span></span><br/> <span data-ttu-id="5fa9d-813">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-813">0</span></span><br/>

<span data-ttu-id="5fa9d-814">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-814">1</span></span>

<span data-ttu-id="5fa9d-815">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-815">2</span></span>

<span data-ttu-id="5fa9d-816">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-816">3</span></span>

<span data-ttu-id="5fa9d-817">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-817">4</span></span>

<span data-ttu-id="5fa9d-818">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-818">5</span></span>

<span data-ttu-id="5fa9d-819">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-819">6</span></span>

<span data-ttu-id="5fa9d-820">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-820">7</span></span>

<span data-ttu-id="5fa9d-821">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-821">8</span></span>

<span data-ttu-id="5fa9d-822">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-822">9</span></span>

<span data-ttu-id="5fa9d-823">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-823">2</span></span><br/> <span data-ttu-id="5fa9d-824">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-824">0</span></span><br/>

<span data-ttu-id="5fa9d-825">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-825">1</span></span>

<span data-ttu-id="5fa9d-826">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-826">2</span></span>

<span data-ttu-id="5fa9d-827">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-827">3</span></span>

<span data-ttu-id="5fa9d-828">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-828">4</span></span>

<span data-ttu-id="5fa9d-829">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-829">5</span></span>

<span data-ttu-id="5fa9d-830">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-830">6</span></span>

<span data-ttu-id="5fa9d-831">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-831">7</span></span>

<span data-ttu-id="5fa9d-832">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-832">8</span></span>

<span data-ttu-id="5fa9d-833">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-833">9</span></span>

<span data-ttu-id="5fa9d-834">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-834">3</span></span><br/> <span data-ttu-id="5fa9d-835">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-835">0</span></span><br/>

<span data-ttu-id="5fa9d-836">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-836">1</span></span>

<span data-ttu-id="5fa9d-837">кдимс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-837">cDims</span></span>

<span data-ttu-id="5fa9d-838">Ргсабаунд (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-838">Rgsabound (variable)</span></span>

<span data-ttu-id="5fa9d-839">Вдата (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-839">vData (variable)</span></span>



 

<span data-ttu-id="5fa9d-840">**кдимс**: 32-разрядное целое число без знака, указывающее количество измерений SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-840">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="5fa9d-841">**Ргсабаунд**: массив, содержащий одну структуру сафеаррайбаунд, как указано в разделе 2.2.1.1.1.4 для измерения в SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-841">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="5fa9d-842">В этом массиве сначала находится крайне левое измерение, а в последнем — крайнее правое измерение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-842">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="5fa9d-843">**вдата**: вектор упакованных элементов определенного типа, обозначенный двтипеом содержащего сериализедпропертивалуе, с битом 0x2000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-843">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="5fa9d-844">Формат Вдата, аналогичный указанному для поля Вдата массива SAFEARRAY в разделе 2.2.1.1.1.3.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-844">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="5fa9d-845">2.2.1.2 Кфуллпропспек</span><span class="sxs-lookup"><span data-stu-id="5fa9d-845">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="5fa9d-846">Структура Кфуллпропспек содержит идентификатор GUID набора свойств и идентификатор свойства для уникальной идентификации свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-846">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="5fa9d-847">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-847">0</span></span>

<span data-ttu-id="5fa9d-848">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-848">1</span></span>

<span data-ttu-id="5fa9d-849">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-849">2</span></span>

<span data-ttu-id="5fa9d-850">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-850">3</span></span>

<span data-ttu-id="5fa9d-851">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-851">4</span></span>

<span data-ttu-id="5fa9d-852">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-852">5</span></span>

<span data-ttu-id="5fa9d-853">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-853">6</span></span>

<span data-ttu-id="5fa9d-854">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-854">7</span></span>

<span data-ttu-id="5fa9d-855">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-855">8</span></span>

<span data-ttu-id="5fa9d-856">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-856">9</span></span>

<span data-ttu-id="5fa9d-857">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-857">1</span></span><br/> <span data-ttu-id="5fa9d-858">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-858">0</span></span><br/>

<span data-ttu-id="5fa9d-859">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-859">1</span></span>

<span data-ttu-id="5fa9d-860">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-860">2</span></span>

<span data-ttu-id="5fa9d-861">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-861">3</span></span>

<span data-ttu-id="5fa9d-862">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-862">4</span></span>

<span data-ttu-id="5fa9d-863">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-863">5</span></span>

<span data-ttu-id="5fa9d-864">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-864">6</span></span>

<span data-ttu-id="5fa9d-865">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-865">7</span></span>

<span data-ttu-id="5fa9d-866">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-866">8</span></span>

<span data-ttu-id="5fa9d-867">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-867">9</span></span>

<span data-ttu-id="5fa9d-868">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-868">2</span></span><br/> <span data-ttu-id="5fa9d-869">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-869">0</span></span><br/>

<span data-ttu-id="5fa9d-870">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-870">1</span></span>

<span data-ttu-id="5fa9d-871">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-871">2</span></span>

<span data-ttu-id="5fa9d-872">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-872">3</span></span>

<span data-ttu-id="5fa9d-873">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-873">4</span></span>

<span data-ttu-id="5fa9d-874">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-874">5</span></span>

<span data-ttu-id="5fa9d-875">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-875">6</span></span>

<span data-ttu-id="5fa9d-876">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-876">7</span></span>

<span data-ttu-id="5fa9d-877">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-877">8</span></span>

<span data-ttu-id="5fa9d-878">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-878">9</span></span>

<span data-ttu-id="5fa9d-879">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-879">3</span></span><br/> <span data-ttu-id="5fa9d-880">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-880">0</span></span><br/>

<span data-ttu-id="5fa9d-881">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-881">1</span></span>

<span data-ttu-id="5fa9d-882">\_гуидпропсет</span><span class="sxs-lookup"><span data-stu-id="5fa9d-882">\_guidPropSet</span></span>

<span data-ttu-id="5fa9d-883">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-883">...</span></span>

<span data-ttu-id="5fa9d-884">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-884">...</span></span>

<span data-ttu-id="5fa9d-885">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-885">...</span></span>

<span data-ttu-id="5fa9d-886">улкинд</span><span class="sxs-lookup"><span data-stu-id="5fa9d-886">ulKind</span></span>

<span data-ttu-id="5fa9d-887">прспек</span><span class="sxs-lookup"><span data-stu-id="5fa9d-887">PrSpec</span></span>

<span data-ttu-id="5fa9d-888">Имя свойства (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-888">Property name (variable)</span></span>



 

<span data-ttu-id="5fa9d-889">**\_ гуидпропсет**: идентификатор GUID набора свойств, которому принадлежит свойство.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-889">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="5fa9d-890">**улкинд**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-890">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="5fa9d-891">Одно из приведенных ниже значений, которое указывает содержимое Прспек.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-891">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="5fa9d-892">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-892">Value</span></span>                                            | <span data-ttu-id="5fa9d-893">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-893">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-894">ПРСПЕК \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5fa9d-894">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="5fa9d-895">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-895">0x00000000</span></span><br/> | <span data-ttu-id="5fa9d-896">Поле Прспек указывает число символов, отличных от NULL, в поле Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-896">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="5fa9d-897">ПРСПЕК \_ PropID</span><span class="sxs-lookup"><span data-stu-id="5fa9d-897">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="5fa9d-898">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-898">0x00000001</span></span><br/>  | <span data-ttu-id="5fa9d-899">В поле Прспек указывается идентификатор свойства (PROPID).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-899">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="5fa9d-900">**Прспек**: 32-битовое целое число без знака, равное значению, указанному в поле улкинд.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-900">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="5fa9d-901">**Имя свойства**: Если улкинд имеет значение прспек \_ PropID, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-901">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="5fa9d-902">Если для Улкинд задано значение ПРСПЕК \_ LPWSTR, то в этом поле должен содержаться массив, не учитывающий регистр, из прспек символов Юникода, отличных от NULL, содержащий имя свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-902">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="5fa9d-903">2.2.1.3 Кконтентрестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-903">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="5fa9d-904">Структура Кконтентрестриктион содержит строку, соответствующую свойству в кэше свойств.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-904">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="5fa9d-905">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-905">0</span></span>

<span data-ttu-id="5fa9d-906">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-906">1</span></span>

<span data-ttu-id="5fa9d-907">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-907">2</span></span>

<span data-ttu-id="5fa9d-908">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-908">3</span></span>

<span data-ttu-id="5fa9d-909">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-909">4</span></span>

<span data-ttu-id="5fa9d-910">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-910">5</span></span>

<span data-ttu-id="5fa9d-911">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-911">6</span></span>

<span data-ttu-id="5fa9d-912">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-912">7</span></span>

<span data-ttu-id="5fa9d-913">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-913">8</span></span>

<span data-ttu-id="5fa9d-914">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-914">9</span></span>

<span data-ttu-id="5fa9d-915">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-915">1</span></span><br/> <span data-ttu-id="5fa9d-916">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-916">0</span></span><br/>

<span data-ttu-id="5fa9d-917">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-917">1</span></span>

<span data-ttu-id="5fa9d-918">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-918">2</span></span>

<span data-ttu-id="5fa9d-919">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-919">3</span></span>

<span data-ttu-id="5fa9d-920">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-920">4</span></span>

<span data-ttu-id="5fa9d-921">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-921">5</span></span>

<span data-ttu-id="5fa9d-922">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-922">6</span></span>

<span data-ttu-id="5fa9d-923">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-923">7</span></span>

<span data-ttu-id="5fa9d-924">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-924">8</span></span>

<span data-ttu-id="5fa9d-925">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-925">9</span></span>

<span data-ttu-id="5fa9d-926">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-926">2</span></span><br/> <span data-ttu-id="5fa9d-927">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-927">0</span></span><br/>

<span data-ttu-id="5fa9d-928">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-928">1</span></span>

<span data-ttu-id="5fa9d-929">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-929">2</span></span>

<span data-ttu-id="5fa9d-930">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-930">3</span></span>

<span data-ttu-id="5fa9d-931">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-931">4</span></span>

<span data-ttu-id="5fa9d-932">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-932">5</span></span>

<span data-ttu-id="5fa9d-933">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-933">6</span></span>

<span data-ttu-id="5fa9d-934">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-934">7</span></span>

<span data-ttu-id="5fa9d-935">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-935">8</span></span>

<span data-ttu-id="5fa9d-936">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-936">9</span></span>

<span data-ttu-id="5fa9d-937">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-937">3</span></span><br/> <span data-ttu-id="5fa9d-938">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-938">0</span></span><br/>

<span data-ttu-id="5fa9d-939">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-939">1</span></span>

<span data-ttu-id="5fa9d-940">\_Свойство (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-940">\_Property (variable)</span></span>

<span data-ttu-id="5fa9d-941">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-941">...</span></span>

<span data-ttu-id="5fa9d-942">Padding1 (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-942">Padding1 (variable)</span></span>

<span data-ttu-id="5fa9d-943">Копия</span><span class="sxs-lookup"><span data-stu-id="5fa9d-943">Cc</span></span>

<span data-ttu-id="5fa9d-944">\_Пвксфрасе (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-944">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="5fa9d-945">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-945">...</span></span>

<span data-ttu-id="5fa9d-946">Padding2 (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-946">Padding2 (variable)</span></span>

<span data-ttu-id="5fa9d-947">lcid</span><span class="sxs-lookup"><span data-stu-id="5fa9d-947">lcid</span></span>

<span data-ttu-id="5fa9d-948">\_улженератемесод</span><span class="sxs-lookup"><span data-stu-id="5fa9d-948">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="5fa9d-949">**\_ Свойство**: структура кфуллпропспек, как указано в разделе 2.2.1.2.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-949">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="5fa9d-950">Это поле обозначает свойство, для которого необходимо выполнить операцию сопоставления.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-950">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="5fa9d-951">**Padding1**: это поле должно иметь длину от 0 до 3 байт.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-951">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="5fa9d-952">Длина этого поля должна быть такой, что следующее поле начинается со смещения, кратного 4 байтам от начала сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-952">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="5fa9d-953">Если это поле (т. е. Длина ненулевой), то значение, которое он содержит, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-953">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="5fa9d-954">Содержимое этого поля должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-954">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="5fa9d-955">**CC**: 32-битовое целое число без знака, указывающее количество символов в \_ поле пвксфрасе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-955">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="5fa9d-956">**\_ пвксфрасе**: строка Юникода, не заканчивающаяся нулем, представляющая слово или фразу для сопоставления со свойством.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-956">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="5fa9d-957">Это поле не должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-957">This field MUST NOT be empty.</span></span> <span data-ttu-id="5fa9d-958">Поле "копия" содержит длину строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-958">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="5fa9d-959">**Padding2**: это поле должно иметь длину от 0 до 3 байт.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-959">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="5fa9d-960">Длина этого поля должна быть такой, что следующее поле начинается со смещения, кратного 4 байтам от начала сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-960">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="5fa9d-961">Если это поле (т. е. Длина ненулевой), то значение, которое он содержит, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-961">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="5fa9d-962">Содержимое этого поля должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-962">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="5fa9d-963">**LCID**: 32-разрядное целое число без знака, указывающее языковой стандарт \_ пвксфрасе, как указано в \[ приложении MS-GPSI \] A.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-963">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="5fa9d-964">**\_ улженератемесод**: 32-битовое целое число без знака, определяющее метод, используемый при создании альтернативных форм Word</span><span class="sxs-lookup"><span data-stu-id="5fa9d-964">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="5fa9d-965">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-965">Value</span></span>                                                       | <span data-ttu-id="5fa9d-966">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-966">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-967">СОЗДАТЬ \_ \_ точный метод</span><span class="sxs-lookup"><span data-stu-id="5fa9d-967">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="5fa9d-968">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-968">0x00000000</span></span><br/>    | <span data-ttu-id="5fa9d-969">Точное соответствие.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-969">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="5fa9d-970">СОЗДАТЬ \_ \_ префикс метода</span><span class="sxs-lookup"><span data-stu-id="5fa9d-970">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="5fa9d-971">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-971">0x00000001</span></span> <br/>  | <span data-ttu-id="5fa9d-972">Совпадение префикса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-972">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="5fa9d-973">СОЗДАТЬ \_ метод \_ инфлект</span><span class="sxs-lookup"><span data-stu-id="5fa9d-973">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="5fa9d-974">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-974">0x00000002</span></span><br/> | <span data-ttu-id="5fa9d-975">Соответствует Перегибам слова.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-975">Matches inflections of a word.</span></span> <span data-ttu-id="5fa9d-976">Перегиб слова — это вариант корневого слова в той же части речи, который был изменен в соответствии с лингвистическими правилами данного языка.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-976">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="5fa9d-977">Например, в английской версии глагола "дорожки" включает "дорожки", "купание", "Swimming" и "свам".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-977">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="5fa9d-978">2.2.1.4 Ккэй</span><span class="sxs-lookup"><span data-stu-id="5fa9d-978">2.2.1.4 CKey</span></span>

<span data-ttu-id="5fa9d-979">Структура Ккэй содержит значение свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-979">The CKey structure contains a property value.</span></span>



<span data-ttu-id="5fa9d-980">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-980">0</span></span>

<span data-ttu-id="5fa9d-981">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-981">1</span></span>

<span data-ttu-id="5fa9d-982">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-982">2</span></span>

<span data-ttu-id="5fa9d-983">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-983">3</span></span>

<span data-ttu-id="5fa9d-984">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-984">4</span></span>

<span data-ttu-id="5fa9d-985">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-985">5</span></span>

<span data-ttu-id="5fa9d-986">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-986">6</span></span>

<span data-ttu-id="5fa9d-987">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-987">7</span></span>

<span data-ttu-id="5fa9d-988">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-988">8</span></span>

<span data-ttu-id="5fa9d-989">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-989">9</span></span>

<span data-ttu-id="5fa9d-990">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-990">1</span></span><br/> <span data-ttu-id="5fa9d-991">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-991">0</span></span><br/>

<span data-ttu-id="5fa9d-992">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-992">1</span></span>

<span data-ttu-id="5fa9d-993">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-993">2</span></span>

<span data-ttu-id="5fa9d-994">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-994">3</span></span>

<span data-ttu-id="5fa9d-995">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-995">4</span></span>

<span data-ttu-id="5fa9d-996">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-996">5</span></span>

<span data-ttu-id="5fa9d-997">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-997">6</span></span>

<span data-ttu-id="5fa9d-998">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-998">7</span></span>

<span data-ttu-id="5fa9d-999">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-999">8</span></span>

<span data-ttu-id="5fa9d-1000">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1000">9</span></span>

<span data-ttu-id="5fa9d-1001">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1001">2</span></span><br/> <span data-ttu-id="5fa9d-1002">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1002">0</span></span><br/>

<span data-ttu-id="5fa9d-1003">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1003">1</span></span>

<span data-ttu-id="5fa9d-1004">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1004">2</span></span>

<span data-ttu-id="5fa9d-1005">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1005">3</span></span>

<span data-ttu-id="5fa9d-1006">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1006">4</span></span>

<span data-ttu-id="5fa9d-1007">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1007">5</span></span>

<span data-ttu-id="5fa9d-1008">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1008">6</span></span>

<span data-ttu-id="5fa9d-1009">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1009">7</span></span>

<span data-ttu-id="5fa9d-1010">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1010">8</span></span>

<span data-ttu-id="5fa9d-1011">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1011">9</span></span>

<span data-ttu-id="5fa9d-1012">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1012">3</span></span><br/> <span data-ttu-id="5fa9d-1013">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1013">0</span></span><br/>

<span data-ttu-id="5fa9d-1014">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1014">1</span></span>

<span data-ttu-id="5fa9d-1015">PROPID</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1015">PROPID</span></span>

<span data-ttu-id="5fa9d-1016">CB</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1016">Cb</span></span>

<span data-ttu-id="5fa9d-1017">buf (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1017">buf (variable)</span></span>



 

<span data-ttu-id="5fa9d-1018">**PropID**: 32-битовое целое число без знака, представляющее идентификатор свойства, как описано в разделе 1.8.1.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1018">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="5fa9d-1019">Хорошо известные значения:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1019">Well-known values are:</span></span>



| <span data-ttu-id="5fa9d-1020">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1020">Value</span></span>      | <span data-ttu-id="5fa9d-1021">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1021">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="5fa9d-1022">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1022">0xFFFFFFFF</span></span> | <span data-ttu-id="5fa9d-1023">Представляет недопустимый идентификатор свойства и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1023">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="5fa9d-1024">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1024">0xFFFFFFFE</span></span> | <span data-ttu-id="5fa9d-1025">Представляет недопустимый идентификатор свойства и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1025">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="5fa9d-1026">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1026">0x00000000</span></span> | <span data-ttu-id="5fa9d-1027">Представляет идентификатор любого свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1027">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="5fa9d-1028">**CB**: 32-разрядное целое число без знака, содержащее длину buf в байтах.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1028">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="5fa9d-1029">**buf**: последовательность байтов, представляющих значение свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1029">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="5fa9d-1030">2.2.1.5 Цинтерналпропертирестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1030">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="5fa9d-1031">Структура Цинтерналпропертирестриктион содержит значение свойства для сопоставления с операцией.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1031">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="5fa9d-1032">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1032">0</span></span>

<span data-ttu-id="5fa9d-1033">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1033">1</span></span>

<span data-ttu-id="5fa9d-1034">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1034">2</span></span>

<span data-ttu-id="5fa9d-1035">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1035">3</span></span>

<span data-ttu-id="5fa9d-1036">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1036">4</span></span>

<span data-ttu-id="5fa9d-1037">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1037">5</span></span>

<span data-ttu-id="5fa9d-1038">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1038">6</span></span>

<span data-ttu-id="5fa9d-1039">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1039">7</span></span>

<span data-ttu-id="5fa9d-1040">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1040">8</span></span>

<span data-ttu-id="5fa9d-1041">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1041">9</span></span>

<span data-ttu-id="5fa9d-1042">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1042">1</span></span><br/> <span data-ttu-id="5fa9d-1043">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1043">0</span></span><br/>

<span data-ttu-id="5fa9d-1044">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1044">1</span></span>

<span data-ttu-id="5fa9d-1045">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1045">2</span></span>

<span data-ttu-id="5fa9d-1046">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1046">3</span></span>

<span data-ttu-id="5fa9d-1047">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1047">4</span></span>

<span data-ttu-id="5fa9d-1048">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1048">5</span></span>

<span data-ttu-id="5fa9d-1049">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1049">6</span></span>

<span data-ttu-id="5fa9d-1050">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1050">7</span></span>

<span data-ttu-id="5fa9d-1051">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1051">8</span></span>

<span data-ttu-id="5fa9d-1052">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1052">9</span></span>

<span data-ttu-id="5fa9d-1053">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1053">2</span></span><br/> <span data-ttu-id="5fa9d-1054">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1054">0</span></span><br/>

<span data-ttu-id="5fa9d-1055">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1055">1</span></span>

<span data-ttu-id="5fa9d-1056">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1056">2</span></span>

<span data-ttu-id="5fa9d-1057">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1057">3</span></span>

<span data-ttu-id="5fa9d-1058">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1058">4</span></span>

<span data-ttu-id="5fa9d-1059">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1059">5</span></span>

<span data-ttu-id="5fa9d-1060">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1060">6</span></span>

<span data-ttu-id="5fa9d-1061">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1061">7</span></span>

<span data-ttu-id="5fa9d-1062">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1062">8</span></span>

<span data-ttu-id="5fa9d-1063">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1063">9</span></span>

<span data-ttu-id="5fa9d-1064">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1064">3</span></span><br/> <span data-ttu-id="5fa9d-1065">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1065">0</span></span><br/>

<span data-ttu-id="5fa9d-1066">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1066">1</span></span>

<span data-ttu-id="5fa9d-1067">\_RelOp</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1067">\_relop</span></span>

<span data-ttu-id="5fa9d-1068">\_PID</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1068">\_pid</span></span>

<span data-ttu-id="5fa9d-1069">\_првал (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1069">\_prval (variable)</span></span>

<span data-ttu-id="5fa9d-1070">рестриктионпресент</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1070">restrictionPresent</span></span>

<span data-ttu-id="5fa9d-1071">Некстрестриктион (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1071">nextRestriction (variable)</span></span>



 

<span data-ttu-id="5fa9d-1072">**\_ relop**: 32-разрядное целое число, указывающее отношение для выполнения со свойством.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1072">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="5fa9d-1073">ДОЛЖНО иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1073">MUST be one of the following values:</span></span>



| <span data-ttu-id="5fa9d-1074">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1074">Value</span></span>                 | <span data-ttu-id="5fa9d-1075">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1075">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-1076">ПРЛТ 0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1076">PRLT 0x00000000</span></span>       | <span data-ttu-id="5fa9d-1077">Сравнение "меньше чем".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1077">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="5fa9d-1078">ПРЛЕ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1078">PRLE 0x00000001</span></span>       | <span data-ttu-id="5fa9d-1079">Сравнение "меньше или равно".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1079">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="5fa9d-1080">ПРГТ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1080">PRGT 0x00000002</span></span>       | <span data-ttu-id="5fa9d-1081">Сравнение "больше чем".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1081">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="5fa9d-1082">ПРЖЕ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1082">PRGE 0x00000003</span></span>       | <span data-ttu-id="5fa9d-1083">Сравнение "больше или равно".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1083">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="5fa9d-1084">ПРЕК 0x00000004</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1084">PREQ 0x00000004</span></span>       | <span data-ttu-id="5fa9d-1085">Сравнение на равенство.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1085">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="5fa9d-1086">ПРНЕ 0x00000005</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1086">PRNE 0x00000005</span></span>       | <span data-ttu-id="5fa9d-1087">Сравнение «не равно».</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1087">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="5fa9d-1088">ПРРЕ 0x00000006</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1088">PRRE 0x00000006</span></span>       | <span data-ttu-id="5fa9d-1089">Сравнение регулярных выражений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1089">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="5fa9d-1090">Праллбитс 0x00000007</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1090">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="5fa9d-1091">Побитовое и, возвращающее правый операнд.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1091">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="5fa9d-1092">Прсомебитс 0x00000008</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1092">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="5fa9d-1093">Побитовое и, возвращающее ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1093">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="5fa9d-1094">Пралл 0x00000100</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1094">PRAll 0x00000100</span></span>      | <span data-ttu-id="5fa9d-1095">Операция должна быть выполнена над столбцом набора строк и имеет значение true, если операция выполняется для всех строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1095">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="5fa9d-1096">ПРАНИ 0x00000200</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1096">PRAny 0x00000200</span></span>      | <span data-ttu-id="5fa9d-1097">Операция должна быть выполнена над столбцом набора строк, и имеет значение true, если операция выполняется для любой строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1097">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="5fa9d-1098">**\_ pid**: 32-разрядное целое число без знака, представляющее идентификатор свойства (см. раздел PropID в разделе 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1098">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="5fa9d-1099">**\_ Првал**: кбасесторажевариант, содержащий значение, которое необходимо связать со свойством.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1099">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="5fa9d-1100">**рестриктионпресент**: значение байта, указывающее, имеется ли поле некстрестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1100">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="5fa9d-1101">НЕОБХОДИМО задать значение 0x00 или 0x01.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1101">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="5fa9d-1102">Если задано значение 0x01, Рестриктионпресент указывает на наличие поля Некстрестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1102">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="5fa9d-1103">Если задано значение 0x00, Рестриктионпресент указывает, что поле Некстрестриктион отсутствует.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1103">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="5fa9d-1104">**некстрестриктион**: структура крестриктион, как указано в разделе 2.2.1.16, с указанием дополнительного ограничения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1104">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="5fa9d-1105">2.2.1.6 Кнатлангуажерестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1105">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="5fa9d-1106">Структура Кнатлангуажерестриктион содержит запрос на **естественном языке** , соответствующий свойству.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1106">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="5fa9d-1107">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1107">0</span></span>

<span data-ttu-id="5fa9d-1108">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1108">1</span></span>

<span data-ttu-id="5fa9d-1109">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1109">2</span></span>

<span data-ttu-id="5fa9d-1110">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1110">3</span></span>

<span data-ttu-id="5fa9d-1111">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1111">4</span></span>

<span data-ttu-id="5fa9d-1112">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1112">5</span></span>

<span data-ttu-id="5fa9d-1113">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1113">6</span></span>

<span data-ttu-id="5fa9d-1114">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1114">7</span></span>

<span data-ttu-id="5fa9d-1115">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1115">8</span></span>

<span data-ttu-id="5fa9d-1116">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1116">9</span></span>

<span data-ttu-id="5fa9d-1117">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1117">1</span></span><br/> <span data-ttu-id="5fa9d-1118">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1118">0</span></span><br/>

<span data-ttu-id="5fa9d-1119">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1119">1</span></span>

<span data-ttu-id="5fa9d-1120">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1120">2</span></span>

<span data-ttu-id="5fa9d-1121">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1121">3</span></span>

<span data-ttu-id="5fa9d-1122">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1122">4</span></span>

<span data-ttu-id="5fa9d-1123">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1123">5</span></span>

<span data-ttu-id="5fa9d-1124">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1124">6</span></span>

<span data-ttu-id="5fa9d-1125">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1125">7</span></span>

<span data-ttu-id="5fa9d-1126">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1126">8</span></span>

<span data-ttu-id="5fa9d-1127">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1127">9</span></span>

<span data-ttu-id="5fa9d-1128">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1128">2</span></span><br/> <span data-ttu-id="5fa9d-1129">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1129">0</span></span><br/>

<span data-ttu-id="5fa9d-1130">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1130">1</span></span>

<span data-ttu-id="5fa9d-1131">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1131">2</span></span>

<span data-ttu-id="5fa9d-1132">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1132">3</span></span>

<span data-ttu-id="5fa9d-1133">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1133">4</span></span>

<span data-ttu-id="5fa9d-1134">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1134">5</span></span>

<span data-ttu-id="5fa9d-1135">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1135">6</span></span>

<span data-ttu-id="5fa9d-1136">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1136">7</span></span>

<span data-ttu-id="5fa9d-1137">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1137">8</span></span>

<span data-ttu-id="5fa9d-1138">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1138">9</span></span>

<span data-ttu-id="5fa9d-1139">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1139">3</span></span><br/> <span data-ttu-id="5fa9d-1140">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1140">0</span></span><br/>

<span data-ttu-id="5fa9d-1141">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1141">1</span></span>

<span data-ttu-id="5fa9d-1142">\_Свойство (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1142">\_Property (variable)</span></span>

<span data-ttu-id="5fa9d-1143">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1143">...</span></span>

<span data-ttu-id="5fa9d-1144">\_заполнение \_ CC (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1144">\_padding\_cc (variable)</span></span>

<span data-ttu-id="5fa9d-1145">Копия</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1145">Cc</span></span>

<span data-ttu-id="5fa9d-1146">\_Пвксфрасе (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1146">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="5fa9d-1147">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1147">...</span></span>

<span data-ttu-id="5fa9d-1148">\_LCID заполнения \_ (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1148">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="5fa9d-1149">Код языка</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1149">Lcid</span></span>



 

<span data-ttu-id="5fa9d-1150">**\_ Свойство**: структура кфуллпропспек, как указано в разделе 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1150">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="5fa9d-1151">Это поле обозначает свойство, для которого необходимо выполнить операцию сопоставления.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1151">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="5fa9d-1152">**\_ Заполнение \_ CC**: это поле должно иметь длину от 0 до 3 байт.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1152">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="5fa9d-1153">Длина этого поля должна быть такой, что следующее поле начинается со смещения, кратного 4 байтам от начала сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1153">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="5fa9d-1154">Если это поле (т. е. Длина ненулевой), то значение, которое он содержит, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1154">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="5fa9d-1155">Содержимое этого поля должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1155">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="5fa9d-1156">**CC**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1156">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="5fa9d-1157">Число символов в \_ поле пвксфрасе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1157">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="5fa9d-1158">**\_ пвксфрасе**: строка Юникода, не заканчивающаяся нулем, представляющая слово или фразу для сопоставления со свойством.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1158">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="5fa9d-1159">НЕ должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1159">MUST NOT be empty.</span></span> <span data-ttu-id="5fa9d-1160">Поле "копия" содержит длину строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1160">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="5fa9d-1161">**\_ \_ код языка заполнения**: это поле должно иметь длину от 0 до 3 байт.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1161">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="5fa9d-1162">Длина этого поля должна быть такой, что следующее поле начинается со смещения, кратного 4 байтам от начала сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1162">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="5fa9d-1163">Если это поле (т. е. Длина ненулевой), то значение, которое он содержит, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1163">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="5fa9d-1164">Содержимое этого поля должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1164">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="5fa9d-1165">**LCID**: 32-разрядное целое число без знака, указывающее языковой стандарт \_ пвксфрасе, как указано в \[ приложении MS-GPSI \] A.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1165">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="5fa9d-1166">2.2.1.7 Кнодерестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1166">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="5fa9d-1167">Структура Кнодерестриктион содержит массив узлов **дерева команд** , которые указывают ограничения для запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1167">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="5fa9d-1168">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1168">0</span></span>

<span data-ttu-id="5fa9d-1169">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1169">1</span></span>

<span data-ttu-id="5fa9d-1170">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1170">2</span></span>

<span data-ttu-id="5fa9d-1171">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1171">3</span></span>

<span data-ttu-id="5fa9d-1172">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1172">4</span></span>

<span data-ttu-id="5fa9d-1173">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1173">5</span></span>

<span data-ttu-id="5fa9d-1174">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1174">6</span></span>

<span data-ttu-id="5fa9d-1175">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1175">7</span></span>

<span data-ttu-id="5fa9d-1176">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1176">8</span></span>

<span data-ttu-id="5fa9d-1177">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1177">9</span></span>

<span data-ttu-id="5fa9d-1178">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1178">1</span></span><br/> <span data-ttu-id="5fa9d-1179">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1179">0</span></span><br/>

<span data-ttu-id="5fa9d-1180">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1180">1</span></span>

<span data-ttu-id="5fa9d-1181">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1181">2</span></span>

<span data-ttu-id="5fa9d-1182">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1182">3</span></span>

<span data-ttu-id="5fa9d-1183">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1183">4</span></span>

<span data-ttu-id="5fa9d-1184">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1184">5</span></span>

<span data-ttu-id="5fa9d-1185">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1185">6</span></span>

<span data-ttu-id="5fa9d-1186">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1186">7</span></span>

<span data-ttu-id="5fa9d-1187">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1187">8</span></span>

<span data-ttu-id="5fa9d-1188">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1188">9</span></span>

<span data-ttu-id="5fa9d-1189">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1189">2</span></span><br/> <span data-ttu-id="5fa9d-1190">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1190">0</span></span><br/>

<span data-ttu-id="5fa9d-1191">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1191">1</span></span>

<span data-ttu-id="5fa9d-1192">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1192">2</span></span>

<span data-ttu-id="5fa9d-1193">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1193">3</span></span>

<span data-ttu-id="5fa9d-1194">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1194">4</span></span>

<span data-ttu-id="5fa9d-1195">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1195">5</span></span>

<span data-ttu-id="5fa9d-1196">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1196">6</span></span>

<span data-ttu-id="5fa9d-1197">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1197">7</span></span>

<span data-ttu-id="5fa9d-1198">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1198">8</span></span>

<span data-ttu-id="5fa9d-1199">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1199">9</span></span>

<span data-ttu-id="5fa9d-1200">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1200">3</span></span><br/> <span data-ttu-id="5fa9d-1201">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1201">0</span></span><br/>

<span data-ttu-id="5fa9d-1202">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1202">1</span></span>

<span data-ttu-id="5fa9d-1203">\_кноде</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1203">\_cNode</span></span>

<span data-ttu-id="5fa9d-1204">\_Паноде (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1204">\_paNode (variable)</span></span>



 

<span data-ttu-id="5fa9d-1205">**\_ кноде**: 32-разрядное целое число без знака, указывающее количество структур крестриктион, содержащихся в \_ поле паноде.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1205">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="5fa9d-1206">**\_ паноде**: массив структур крестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1206">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="5fa9d-1207">Структуры в массиве должны быть разделены от 0 до 3 байтов, так что каждая структура начинается со смещения, кратного 4 байтам от начала сообщения, содержащего этот массив.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1207">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="5fa9d-1208">Если заданы байты заполнения, то значение, которое они содержат, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1208">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="5fa9d-1209">Содержимое байтов заполнения должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1209">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="5fa9d-1210">2.2.1.8 Коккрестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1210">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="5fa9d-1211">Структура Коккрестриктион содержит расположение слова в фразе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1211">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="5fa9d-1212">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1212">0</span></span>

<span data-ttu-id="5fa9d-1213">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1213">1</span></span>

<span data-ttu-id="5fa9d-1214">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1214">2</span></span>

<span data-ttu-id="5fa9d-1215">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1215">3</span></span>

<span data-ttu-id="5fa9d-1216">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1216">4</span></span>

<span data-ttu-id="5fa9d-1217">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1217">5</span></span>

<span data-ttu-id="5fa9d-1218">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1218">6</span></span>

<span data-ttu-id="5fa9d-1219">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1219">7</span></span>

<span data-ttu-id="5fa9d-1220">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1220">8</span></span>

<span data-ttu-id="5fa9d-1221">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1221">9</span></span>

<span data-ttu-id="5fa9d-1222">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1222">1</span></span><br/> <span data-ttu-id="5fa9d-1223">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1223">0</span></span><br/>

<span data-ttu-id="5fa9d-1224">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1224">1</span></span>

<span data-ttu-id="5fa9d-1225">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1225">2</span></span>

<span data-ttu-id="5fa9d-1226">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1226">3</span></span>

<span data-ttu-id="5fa9d-1227">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1227">4</span></span>

<span data-ttu-id="5fa9d-1228">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1228">5</span></span>

<span data-ttu-id="5fa9d-1229">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1229">6</span></span>

<span data-ttu-id="5fa9d-1230">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1230">7</span></span>

<span data-ttu-id="5fa9d-1231">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1231">8</span></span>

<span data-ttu-id="5fa9d-1232">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1232">9</span></span>

<span data-ttu-id="5fa9d-1233">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1233">2</span></span><br/> <span data-ttu-id="5fa9d-1234">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1234">0</span></span><br/>

<span data-ttu-id="5fa9d-1235">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1235">1</span></span>

<span data-ttu-id="5fa9d-1236">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1236">2</span></span>

<span data-ttu-id="5fa9d-1237">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1237">3</span></span>

<span data-ttu-id="5fa9d-1238">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1238">4</span></span>

<span data-ttu-id="5fa9d-1239">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1239">5</span></span>

<span data-ttu-id="5fa9d-1240">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1240">6</span></span>

<span data-ttu-id="5fa9d-1241">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1241">7</span></span>

<span data-ttu-id="5fa9d-1242">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1242">8</span></span>

<span data-ttu-id="5fa9d-1243">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1243">9</span></span>

<span data-ttu-id="5fa9d-1244">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1244">3</span></span><br/> <span data-ttu-id="5fa9d-1245">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1245">0</span></span><br/>

<span data-ttu-id="5fa9d-1246">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1246">1</span></span>

<span data-ttu-id="5fa9d-1247">\_OCC</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1247">\_occ</span></span>

<span data-ttu-id="5fa9d-1248">\_кпревноисевордс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1248">\_cPrevNoiseWords</span></span>

<span data-ttu-id="5fa9d-1249">\_кнекстноисевордс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1249">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="5fa9d-1250">**\_ occ**: 32-разрядное целое число без знака, указывающее смещение слова в строке запроса в единицах.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1250">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="5fa9d-1251">Слово, используемое в этой спецификации, является единицей языка в любом языковом стандарте, который несет смысл.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1251">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="5fa9d-1252">**\_ кпревноисевордс**: 32-разрядное целое число без знака, содержащее количество **пропускаемых слов** , которые происходят между этим словом и предыдущим словом в фразе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1252">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="5fa9d-1253">**\_ кнекстноисевордс**: 32-разрядное целое число без знака, содержащее количество пропускаемых слов, произошедших между этим словом и следующим словом в фразе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1253">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="5fa9d-1254">2.2.1.9 Кпропертирестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1254">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="5fa9d-1255">Структура Кпропертирестриктион содержит значение свойства для сопоставления с операцией.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1255">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="5fa9d-1256">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1256">0</span></span>

<span data-ttu-id="5fa9d-1257">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1257">1</span></span>

<span data-ttu-id="5fa9d-1258">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1258">2</span></span>

<span data-ttu-id="5fa9d-1259">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1259">3</span></span>

<span data-ttu-id="5fa9d-1260">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1260">4</span></span>

<span data-ttu-id="5fa9d-1261">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1261">5</span></span>

<span data-ttu-id="5fa9d-1262">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1262">6</span></span>

<span data-ttu-id="5fa9d-1263">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1263">7</span></span>

<span data-ttu-id="5fa9d-1264">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1264">8</span></span>

<span data-ttu-id="5fa9d-1265">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1265">9</span></span>

<span data-ttu-id="5fa9d-1266">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1266">1</span></span><br/> <span data-ttu-id="5fa9d-1267">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1267">0</span></span><br/>

<span data-ttu-id="5fa9d-1268">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1268">1</span></span>

<span data-ttu-id="5fa9d-1269">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1269">2</span></span>

<span data-ttu-id="5fa9d-1270">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1270">3</span></span>

<span data-ttu-id="5fa9d-1271">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1271">4</span></span>

<span data-ttu-id="5fa9d-1272">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1272">5</span></span>

<span data-ttu-id="5fa9d-1273">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1273">6</span></span>

<span data-ttu-id="5fa9d-1274">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1274">7</span></span>

<span data-ttu-id="5fa9d-1275">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1275">8</span></span>

<span data-ttu-id="5fa9d-1276">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1276">9</span></span>

<span data-ttu-id="5fa9d-1277">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1277">2</span></span><br/> <span data-ttu-id="5fa9d-1278">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1278">0</span></span><br/>

<span data-ttu-id="5fa9d-1279">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1279">1</span></span>

<span data-ttu-id="5fa9d-1280">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1280">2</span></span>

<span data-ttu-id="5fa9d-1281">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1281">3</span></span>

<span data-ttu-id="5fa9d-1282">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1282">4</span></span>

<span data-ttu-id="5fa9d-1283">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1283">5</span></span>

<span data-ttu-id="5fa9d-1284">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1284">6</span></span>

<span data-ttu-id="5fa9d-1285">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1285">7</span></span>

<span data-ttu-id="5fa9d-1286">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1286">8</span></span>

<span data-ttu-id="5fa9d-1287">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1287">9</span></span>

<span data-ttu-id="5fa9d-1288">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1288">3</span></span><br/> <span data-ttu-id="5fa9d-1289">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1289">0</span></span><br/>

<span data-ttu-id="5fa9d-1290">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1290">1</span></span>

<span data-ttu-id="5fa9d-1291">\_RelOp</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1291">\_relop</span></span>

<span data-ttu-id="5fa9d-1292">\_Свойство (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1292">\_Property (variable)</span></span>

<span data-ttu-id="5fa9d-1293">\_првал (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1293">\_prval (variable)</span></span>



 

<span data-ttu-id="5fa9d-1294">**\_ relop**: 32-битовое целое число без знака, указывающее отношение для выполнения со свойством.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1294">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="5fa9d-1295">ДОЛЖНО иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1295">MUST be one of the following values.</span></span>



| <span data-ttu-id="5fa9d-1296">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1296">Value</span></span>                 | <span data-ttu-id="5fa9d-1297">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1297">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-1298">ПРЛТ 0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1298">PRLT 0x00000000</span></span>       | <span data-ttu-id="5fa9d-1299">Сравнение "меньше чем".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1299">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="5fa9d-1300">ПРЛЕ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1300">PRLE 0x00000001</span></span>       | <span data-ttu-id="5fa9d-1301">Сравнение "меньше или равно".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1301">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="5fa9d-1302">ПРГТ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1302">PRGT 0x00000002</span></span>       | <span data-ttu-id="5fa9d-1303">Сравнение "больше чем".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1303">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="5fa9d-1304">ПРЖЕ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1304">PRGE 0x00000003</span></span>       | <span data-ttu-id="5fa9d-1305">Сравнение "больше или равно".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1305">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="5fa9d-1306">ПРЕК 0x00000004</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1306">PREQ 0x00000004</span></span>       | <span data-ttu-id="5fa9d-1307">Сравнение на равенство.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1307">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="5fa9d-1308">ПРНЕ 0x00000005</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1308">PRNE 0x00000005</span></span>       | <span data-ttu-id="5fa9d-1309">Сравнение «не равно».</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1309">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="5fa9d-1310">ПРРЕ 0x00000006</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1310">PRRE 0x00000006</span></span>       | <span data-ttu-id="5fa9d-1311">Сравнение регулярных выражений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1311">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="5fa9d-1312">Праллбитс 0x00000007</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1312">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="5fa9d-1313">Побитовое и, возвращающее правый операнд.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1313">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="5fa9d-1314">Прсомебитс 0x00000008</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1314">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="5fa9d-1315">Побитовое и, возвращающее ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1315">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="5fa9d-1316">Пралл 0x00000100</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1316">PRAll 0x00000100</span></span>      | <span data-ttu-id="5fa9d-1317">Операция должна быть выполнена над столбцом набора строк и имеет значение true, если операция выполняется для всех строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1317">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="5fa9d-1318">ПРАНИ 0x00000200</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1318">PRAny 0x00000200</span></span>      | <span data-ttu-id="5fa9d-1319">Операция должна быть выполнена над столбцом набора строк, и имеет значение true, если операция выполняется для любой строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1319">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="5fa9d-1320">**\_ Свойство**: структура кфуллпропспек, как указано в разделе 2.2.1.2, указывающая свойство, для которого выполняется операция сопоставления.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1320">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="5fa9d-1321">**\_ првал**: структура кбасесторажевариант, как указано в разделе 2.2.1.1, содержащей значение, которое необходимо связать со свойством.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1321">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="5fa9d-1322">2.2.1.10 Кранжерестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1322">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="5fa9d-1323">Структура Кранжерестриктион содержит ограничение на диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1323">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="5fa9d-1324">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1324">0</span></span>

<span data-ttu-id="5fa9d-1325">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1325">1</span></span>

<span data-ttu-id="5fa9d-1326">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1326">2</span></span>

<span data-ttu-id="5fa9d-1327">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1327">3</span></span>

<span data-ttu-id="5fa9d-1328">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1328">4</span></span>

<span data-ttu-id="5fa9d-1329">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1329">5</span></span>

<span data-ttu-id="5fa9d-1330">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1330">6</span></span>

<span data-ttu-id="5fa9d-1331">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1331">7</span></span>

<span data-ttu-id="5fa9d-1332">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1332">8</span></span>

<span data-ttu-id="5fa9d-1333">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1333">9</span></span>

<span data-ttu-id="5fa9d-1334">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1334">1</span></span><br/> <span data-ttu-id="5fa9d-1335">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1335">0</span></span><br/>

<span data-ttu-id="5fa9d-1336">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1336">1</span></span>

<span data-ttu-id="5fa9d-1337">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1337">2</span></span>

<span data-ttu-id="5fa9d-1338">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1338">3</span></span>

<span data-ttu-id="5fa9d-1339">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1339">4</span></span>

<span data-ttu-id="5fa9d-1340">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1340">5</span></span>

<span data-ttu-id="5fa9d-1341">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1341">6</span></span>

<span data-ttu-id="5fa9d-1342">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1342">7</span></span>

<span data-ttu-id="5fa9d-1343">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1343">8</span></span>

<span data-ttu-id="5fa9d-1344">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1344">9</span></span>

<span data-ttu-id="5fa9d-1345">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1345">2</span></span><br/> <span data-ttu-id="5fa9d-1346">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1346">0</span></span><br/>

<span data-ttu-id="5fa9d-1347">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1347">1</span></span>

<span data-ttu-id="5fa9d-1348">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1348">2</span></span>

<span data-ttu-id="5fa9d-1349">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1349">3</span></span>

<span data-ttu-id="5fa9d-1350">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1350">4</span></span>

<span data-ttu-id="5fa9d-1351">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1351">5</span></span>

<span data-ttu-id="5fa9d-1352">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1352">6</span></span>

<span data-ttu-id="5fa9d-1353">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1353">7</span></span>

<span data-ttu-id="5fa9d-1354">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1354">8</span></span>

<span data-ttu-id="5fa9d-1355">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1355">9</span></span>

<span data-ttu-id="5fa9d-1356">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1356">3</span></span><br/> <span data-ttu-id="5fa9d-1357">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1357">0</span></span><br/>

<span data-ttu-id="5fa9d-1358">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1358">1</span></span>

<span data-ttu-id="5fa9d-1359">\_Кэйстарт (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1359">\_keyStart (variable)</span></span>

<span data-ttu-id="5fa9d-1360">\_Кэйенд (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1360">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="5fa9d-1361">**\_ кэйстарт**: структура ккэй, как указано в разделе 2.2.1.4, содержащей начало диапазона.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1361">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="5fa9d-1362">**\_ кэйенд**: структура ккэй, содержащая конец диапазона.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1362">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="5fa9d-1363">2.2.1.11 Кскоперестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1363">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="5fa9d-1364">Структура Кскоперестриктион содержит ограничение на файлы для поиска.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1364">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="5fa9d-1365">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1365">0</span></span>

<span data-ttu-id="5fa9d-1366">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1366">1</span></span>

<span data-ttu-id="5fa9d-1367">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1367">2</span></span>

<span data-ttu-id="5fa9d-1368">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1368">3</span></span>

<span data-ttu-id="5fa9d-1369">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1369">4</span></span>

<span data-ttu-id="5fa9d-1370">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1370">5</span></span>

<span data-ttu-id="5fa9d-1371">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1371">6</span></span>

<span data-ttu-id="5fa9d-1372">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1372">7</span></span>

<span data-ttu-id="5fa9d-1373">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1373">8</span></span>

<span data-ttu-id="5fa9d-1374">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1374">9</span></span>

<span data-ttu-id="5fa9d-1375">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1375">1</span></span><br/> <span data-ttu-id="5fa9d-1376">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1376">0</span></span><br/>

<span data-ttu-id="5fa9d-1377">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1377">1</span></span>

<span data-ttu-id="5fa9d-1378">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1378">2</span></span>

<span data-ttu-id="5fa9d-1379">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1379">3</span></span>

<span data-ttu-id="5fa9d-1380">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1380">4</span></span>

<span data-ttu-id="5fa9d-1381">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1381">5</span></span>

<span data-ttu-id="5fa9d-1382">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1382">6</span></span>

<span data-ttu-id="5fa9d-1383">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1383">7</span></span>

<span data-ttu-id="5fa9d-1384">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1384">8</span></span>

<span data-ttu-id="5fa9d-1385">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1385">9</span></span>

<span data-ttu-id="5fa9d-1386">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1386">2</span></span><br/> <span data-ttu-id="5fa9d-1387">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1387">0</span></span><br/>

<span data-ttu-id="5fa9d-1388">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1388">1</span></span>

<span data-ttu-id="5fa9d-1389">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1389">2</span></span>

<span data-ttu-id="5fa9d-1390">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1390">3</span></span>

<span data-ttu-id="5fa9d-1391">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1391">4</span></span>

<span data-ttu-id="5fa9d-1392">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1392">5</span></span>

<span data-ttu-id="5fa9d-1393">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1393">6</span></span>

<span data-ttu-id="5fa9d-1394">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1394">7</span></span>

<span data-ttu-id="5fa9d-1395">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1395">8</span></span>

<span data-ttu-id="5fa9d-1396">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1396">9</span></span>

<span data-ttu-id="5fa9d-1397">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1397">3</span></span><br/> <span data-ttu-id="5fa9d-1398">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1398">0</span></span><br/>

<span data-ttu-id="5fa9d-1399">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1399">1</span></span>

<span data-ttu-id="5fa9d-1400">ккловерпас</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1400">CcLowerPath</span></span>

<span data-ttu-id="5fa9d-1401">\_Ловерпас (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1401">\_lowerPath (variable)</span></span>

<span data-ttu-id="5fa9d-1402">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1402">...</span></span>

<span data-ttu-id="5fa9d-1403">\_Заполнение (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1403">\_padding ( variable)</span></span>

<span data-ttu-id="5fa9d-1404">\_недопустим</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1404">\_length</span></span>

<span data-ttu-id="5fa9d-1405">\_фрекурсиве</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1405">\_fRecursive</span></span>

<span data-ttu-id="5fa9d-1406">\_фвиртуал</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1406">\_fVirtual</span></span>



 

<span data-ttu-id="5fa9d-1407">**Ккловерпас**: 32-разрядное целое число без знака, содержащее количество символов Юникода в \_ поле ловерпас.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1407">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="5fa9d-1408">**\_ ловерпас**: строка в Юникоде, не заканчивающаяся нулем, представляющая **путь** , к которому должен быть ограничен запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1408">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="5fa9d-1409">Поле Ккловерпас содержит длину строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1409">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="5fa9d-1410">**\_ Заполнение**: это поле должно иметь длину от 0 до 3 байт.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1410">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="5fa9d-1411">Длина этого поля должна быть такой, что следующее поле начинается со смещения, кратного 4 байтам от начала сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1411">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="5fa9d-1412">Если это поле (т. е. Длина ненулевой), то значение, которое он содержит, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1412">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="5fa9d-1413">Содержимое этого поля должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1413">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="5fa9d-1414">**\_ length**: 32-разрядное целое число без знака, содержащее длину \_ Ловерпас в символах Юникода.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1414">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="5fa9d-1415">Это должно быть то же значение, что и Ккловерпас.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1415">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="5fa9d-1416">**\_ фрекурсиве**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1416">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="5fa9d-1417">НЕОБХОДИМО задать значение 0x00000001 или 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1417">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="5fa9d-1418">Если задано значение 0x00000001, сервер должен рекурсивно проверять все подкаталоги пути.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1418">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="5fa9d-1419">Если задано значение 0x00000000, сервер не должен проверять подкаталоги.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1419">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="5fa9d-1420">**\_ фвиртуал**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1420">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="5fa9d-1421">НЕОБХОДИМО задать значение 0x00000001 или 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1421">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="5fa9d-1422">Если задано значение 0x00000001, \_ ловерпас является виртуальным путем (URL-адресом, связанным с физическим каталогом в файловой системе) для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1422">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="5fa9d-1423">Если задано значение 0x00000000, \_ ловерпас является путем к файловой системе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1423">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="5fa9d-1424">2.2.1.12 Ксорт</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1424">2.2.1.12 CSort</span></span>

<span data-ttu-id="5fa9d-1425">Структура Ксорт определяет столбец для сортировки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1425">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="5fa9d-1426">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1426">0</span></span>

<span data-ttu-id="5fa9d-1427">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1427">1</span></span>

<span data-ttu-id="5fa9d-1428">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1428">2</span></span>

<span data-ttu-id="5fa9d-1429">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1429">3</span></span>

<span data-ttu-id="5fa9d-1430">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1430">4</span></span>

<span data-ttu-id="5fa9d-1431">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1431">5</span></span>

<span data-ttu-id="5fa9d-1432">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1432">6</span></span>

<span data-ttu-id="5fa9d-1433">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1433">7</span></span>

<span data-ttu-id="5fa9d-1434">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1434">8</span></span>

<span data-ttu-id="5fa9d-1435">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1435">9</span></span>

<span data-ttu-id="5fa9d-1436">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1436">1</span></span><br/> <span data-ttu-id="5fa9d-1437">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1437">0</span></span><br/>

<span data-ttu-id="5fa9d-1438">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1438">1</span></span>

<span data-ttu-id="5fa9d-1439">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1439">2</span></span>

<span data-ttu-id="5fa9d-1440">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1440">3</span></span>

<span data-ttu-id="5fa9d-1441">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1441">4</span></span>

<span data-ttu-id="5fa9d-1442">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1442">5</span></span>

<span data-ttu-id="5fa9d-1443">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1443">6</span></span>

<span data-ttu-id="5fa9d-1444">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1444">7</span></span>

<span data-ttu-id="5fa9d-1445">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1445">8</span></span>

<span data-ttu-id="5fa9d-1446">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1446">9</span></span>

<span data-ttu-id="5fa9d-1447">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1447">2</span></span><br/> <span data-ttu-id="5fa9d-1448">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1448">0</span></span><br/>

<span data-ttu-id="5fa9d-1449">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1449">1</span></span>

<span data-ttu-id="5fa9d-1450">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1450">2</span></span>

<span data-ttu-id="5fa9d-1451">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1451">3</span></span>

<span data-ttu-id="5fa9d-1452">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1452">4</span></span>

<span data-ttu-id="5fa9d-1453">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1453">5</span></span>

<span data-ttu-id="5fa9d-1454">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1454">6</span></span>

<span data-ttu-id="5fa9d-1455">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1455">7</span></span>

<span data-ttu-id="5fa9d-1456">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1456">8</span></span>

<span data-ttu-id="5fa9d-1457">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1457">9</span></span>

<span data-ttu-id="5fa9d-1458">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1458">3</span></span><br/> <span data-ttu-id="5fa9d-1459">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1459">0</span></span><br/>

<span data-ttu-id="5fa9d-1460">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1460">1</span></span>

<span data-ttu-id="5fa9d-1461">пидколумн</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1461">pidColumn</span></span>

<span data-ttu-id="5fa9d-1462">Параметр dwOrd</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1462">dwOrder</span></span>

<span data-ttu-id="5fa9d-1463">локаль</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1463">locale</span></span>



 

<span data-ttu-id="5fa9d-1464">**пидколумн**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1464">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="5fa9d-1465">Номер столбца, по которому выполняется сортировка.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1465">The number of the column to sort by.</span></span>

<span data-ttu-id="5fa9d-1466">**параметр DWORD**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1466">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="5fa9d-1467">ДОЛЖНО иметь одно из следующих значений, указывая способ сортировки по столбцу.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1467">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="5fa9d-1468">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1468">Value</span></span>                        | <span data-ttu-id="5fa9d-1469">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1469">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-1470">ЗАПРОС \_ сортасценд 0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1470">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="5fa9d-1471">Строки сортируются в возрастающем порядке по значениям в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1471">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="5fa9d-1472">ЗАПРОС в \_ порядке 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1472">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="5fa9d-1473">Строки сортируются в убывающем порядке на основе значений в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1473">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="5fa9d-1474">**языковой стандарт**: 32-разрядное целое число без знака, указывающее языковой стандарт, как указано в \[ приложении MS-GPSI, \] из которого находится столбец.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1474">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="5fa9d-1475">2.2.1.13 Ксинрестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1475">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="5fa9d-1476">Структура Ксинрестриктион содержит слово или его синонимы для фразы запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1476">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="5fa9d-1477">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1477">0</span></span>

<span data-ttu-id="5fa9d-1478">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1478">1</span></span>

<span data-ttu-id="5fa9d-1479">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1479">2</span></span>

<span data-ttu-id="5fa9d-1480">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1480">3</span></span>

<span data-ttu-id="5fa9d-1481">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1481">4</span></span>

<span data-ttu-id="5fa9d-1482">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1482">5</span></span>

<span data-ttu-id="5fa9d-1483">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1483">6</span></span>

<span data-ttu-id="5fa9d-1484">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1484">7</span></span>

<span data-ttu-id="5fa9d-1485">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1485">8</span></span>

<span data-ttu-id="5fa9d-1486">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1486">9</span></span>

<span data-ttu-id="5fa9d-1487">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1487">1</span></span><br/> <span data-ttu-id="5fa9d-1488">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1488">0</span></span><br/>

<span data-ttu-id="5fa9d-1489">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1489">1</span></span>

<span data-ttu-id="5fa9d-1490">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1490">2</span></span>

<span data-ttu-id="5fa9d-1491">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1491">3</span></span>

<span data-ttu-id="5fa9d-1492">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1492">4</span></span>

<span data-ttu-id="5fa9d-1493">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1493">5</span></span>

<span data-ttu-id="5fa9d-1494">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1494">6</span></span>

<span data-ttu-id="5fa9d-1495">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1495">7</span></span>

<span data-ttu-id="5fa9d-1496">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1496">8</span></span>

<span data-ttu-id="5fa9d-1497">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1497">9</span></span>

<span data-ttu-id="5fa9d-1498">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1498">2</span></span><br/> <span data-ttu-id="5fa9d-1499">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1499">0</span></span><br/>

<span data-ttu-id="5fa9d-1500">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1500">1</span></span>

<span data-ttu-id="5fa9d-1501">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1501">2</span></span>

<span data-ttu-id="5fa9d-1502">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1502">3</span></span>

<span data-ttu-id="5fa9d-1503">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1503">4</span></span>

<span data-ttu-id="5fa9d-1504">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1504">5</span></span>

<span data-ttu-id="5fa9d-1505">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1505">6</span></span>

<span data-ttu-id="5fa9d-1506">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1506">7</span></span>

<span data-ttu-id="5fa9d-1507">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1507">8</span></span>

<span data-ttu-id="5fa9d-1508">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1508">9</span></span>

<span data-ttu-id="5fa9d-1509">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1509">3</span></span><br/> <span data-ttu-id="5fa9d-1510">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1510">0</span></span><br/>

<span data-ttu-id="5fa9d-1511">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1511">1</span></span>

<span data-ttu-id="5fa9d-1512">Ограничение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1512">Restriction</span></span>

<span data-ttu-id="5fa9d-1513">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1513">...</span></span>

<span data-ttu-id="5fa9d-1514">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1514">...</span></span>

<span data-ttu-id="5fa9d-1515">ккэй</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1515">cKey</span></span>

<span data-ttu-id="5fa9d-1516">\_Кэйаррай (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1516">\_keyArray (variable)</span></span>

<span data-ttu-id="5fa9d-1517">\_Диапазон</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1517">\_isRange</span></span>



 

<span data-ttu-id="5fa9d-1518">**Ограничение**: структура коккрестриктион, указывающая расположение слова.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1518">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="5fa9d-1519">**ккэй**: 32-битовое целое число без знака, указывающее количество элементов в \_ массиве кэйаррай.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1519">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="5fa9d-1520">**\_ кэйаррай**: массив структур ккэй, задающий слово и его синонимы.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1520">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="5fa9d-1521">параметр **\_ Range**: Если задано значение 0x01, то ключи являются префиксами для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1521">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="5fa9d-1522">Если задано значение 0x00, то для соответствия ключам используются точные значения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1522">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="5fa9d-1523">\_параметру "диапазон" не должны быть присвоены никакие другие значения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1523">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="5fa9d-1524">2.2.1.14 Квекторрестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1524">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="5fa9d-1525">Структура Квекторрестриктион содержит взвешенное значение или операцию для узла дерева команд.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1525">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="5fa9d-1526">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1526">0</span></span>

<span data-ttu-id="5fa9d-1527">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1527">1</span></span>

<span data-ttu-id="5fa9d-1528">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1528">2</span></span>

<span data-ttu-id="5fa9d-1529">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1529">3</span></span>

<span data-ttu-id="5fa9d-1530">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1530">4</span></span>

<span data-ttu-id="5fa9d-1531">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1531">5</span></span>

<span data-ttu-id="5fa9d-1532">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1532">6</span></span>

<span data-ttu-id="5fa9d-1533">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1533">7</span></span>

<span data-ttu-id="5fa9d-1534">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1534">8</span></span>

<span data-ttu-id="5fa9d-1535">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1535">9</span></span>

<span data-ttu-id="5fa9d-1536">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1536">1</span></span><br/> <span data-ttu-id="5fa9d-1537">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1537">0</span></span><br/>

<span data-ttu-id="5fa9d-1538">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1538">1</span></span>

<span data-ttu-id="5fa9d-1539">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1539">2</span></span>

<span data-ttu-id="5fa9d-1540">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1540">3</span></span>

<span data-ttu-id="5fa9d-1541">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1541">4</span></span>

<span data-ttu-id="5fa9d-1542">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1542">5</span></span>

<span data-ttu-id="5fa9d-1543">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1543">6</span></span>

<span data-ttu-id="5fa9d-1544">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1544">7</span></span>

<span data-ttu-id="5fa9d-1545">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1545">8</span></span>

<span data-ttu-id="5fa9d-1546">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1546">9</span></span>

<span data-ttu-id="5fa9d-1547">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1547">2</span></span><br/> <span data-ttu-id="5fa9d-1548">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1548">0</span></span><br/>

<span data-ttu-id="5fa9d-1549">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1549">1</span></span>

<span data-ttu-id="5fa9d-1550">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1550">2</span></span>

<span data-ttu-id="5fa9d-1551">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1551">3</span></span>

<span data-ttu-id="5fa9d-1552">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1552">4</span></span>

<span data-ttu-id="5fa9d-1553">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1553">5</span></span>

<span data-ttu-id="5fa9d-1554">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1554">6</span></span>

<span data-ttu-id="5fa9d-1555">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1555">7</span></span>

<span data-ttu-id="5fa9d-1556">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1556">8</span></span>

<span data-ttu-id="5fa9d-1557">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1557">9</span></span>

<span data-ttu-id="5fa9d-1558">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1558">3</span></span><br/> <span data-ttu-id="5fa9d-1559">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1559">0</span></span><br/>

<span data-ttu-id="5fa9d-1560">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1560">1</span></span>

<span data-ttu-id="5fa9d-1561">\_Прес (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1561">\_pres (variable)</span></span>

<span data-ttu-id="5fa9d-1562">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1562">...</span></span>

<span data-ttu-id="5fa9d-1563">\_Заполнение (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1563">\_padding (variable)</span></span>

<span data-ttu-id="5fa9d-1564">\_улранкмесод</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1564">\_ulRankMethod</span></span>



 

<span data-ttu-id="5fa9d-1565">**\_ прес**: дерево команд кнодерестриктион, на основе которого выполняется ранжирование или операция.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1565">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="5fa9d-1566">**\_ Заполнение**: это поле должно иметь длину от 0 до 3 байт.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1566">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="5fa9d-1567">Длина этого поля должна быть такой, что следующее поле начинается со смещения, кратного 4 байтам от начала сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1567">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="5fa9d-1568">Если это поле (т. е. Длина ненулевой), то значение, которое он содержит, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1568">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="5fa9d-1569">Содержимое этого поля должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1569">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="5fa9d-1570">**\_ улранкмесод**: 32-битовое целое число без знака, указывающее алгоритм ранжирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1570">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="5fa9d-1571">НЕОБХОДИМО задать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1571">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="5fa9d-1572">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1572">Value</span></span>                            | <span data-ttu-id="5fa9d-1573">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1573">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="5fa9d-1574">\_Минимальное звание вектора ( \_ 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1574">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="5fa9d-1575">Используйте минимальное Салтон алгоритма \[ \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1575">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="5fa9d-1576">Максимум ВЕКТОРного \_ ранга \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1576">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="5fa9d-1577">Использовать максимальный алгоритм \[ Салтон \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1577">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="5fa9d-1578">\_Внутренний приоритетный экземпляр \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1578">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="5fa9d-1579">Использовать внутренний алгоритм продукта \[ Салтон \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1579">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="5fa9d-1580">ВЕКТОРные \_ ранжирующие \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1580">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="5fa9d-1581">Используйте алгоритм "коэффициент костей" \[ Салтон \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1581">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="5fa9d-1582">ВЕКТОР \_ ранжирования \_ джаккарда 0x00000004</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1582">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="5fa9d-1583">Используйте алгоритм Джаккарда коэффициента \[ Салтон \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1583">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="5fa9d-1584">2.2.1.15 Квордрестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1584">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="5fa9d-1585">Структура Квордрестриктион содержит слово для фразы запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1585">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="5fa9d-1586">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1586">0</span></span>

<span data-ttu-id="5fa9d-1587">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1587">1</span></span>

<span data-ttu-id="5fa9d-1588">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1588">2</span></span>

<span data-ttu-id="5fa9d-1589">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1589">3</span></span>

<span data-ttu-id="5fa9d-1590">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1590">4</span></span>

<span data-ttu-id="5fa9d-1591">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1591">5</span></span>

<span data-ttu-id="5fa9d-1592">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1592">6</span></span>

<span data-ttu-id="5fa9d-1593">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1593">7</span></span>

<span data-ttu-id="5fa9d-1594">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1594">8</span></span>

<span data-ttu-id="5fa9d-1595">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1595">9</span></span>

<span data-ttu-id="5fa9d-1596">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1596">1</span></span><br/> <span data-ttu-id="5fa9d-1597">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1597">0</span></span><br/>

<span data-ttu-id="5fa9d-1598">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1598">1</span></span>

<span data-ttu-id="5fa9d-1599">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1599">2</span></span>

<span data-ttu-id="5fa9d-1600">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1600">3</span></span>

<span data-ttu-id="5fa9d-1601">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1601">4</span></span>

<span data-ttu-id="5fa9d-1602">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1602">5</span></span>

<span data-ttu-id="5fa9d-1603">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1603">6</span></span>

<span data-ttu-id="5fa9d-1604">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1604">7</span></span>

<span data-ttu-id="5fa9d-1605">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1605">8</span></span>

<span data-ttu-id="5fa9d-1606">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1606">9</span></span>

<span data-ttu-id="5fa9d-1607">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1607">2</span></span><br/> <span data-ttu-id="5fa9d-1608">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1608">0</span></span><br/>

<span data-ttu-id="5fa9d-1609">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1609">1</span></span>

<span data-ttu-id="5fa9d-1610">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1610">2</span></span>

<span data-ttu-id="5fa9d-1611">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1611">3</span></span>

<span data-ttu-id="5fa9d-1612">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1612">4</span></span>

<span data-ttu-id="5fa9d-1613">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1613">5</span></span>

<span data-ttu-id="5fa9d-1614">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1614">6</span></span>

<span data-ttu-id="5fa9d-1615">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1615">7</span></span>

<span data-ttu-id="5fa9d-1616">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1616">8</span></span>

<span data-ttu-id="5fa9d-1617">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1617">9</span></span>

<span data-ttu-id="5fa9d-1618">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1618">3</span></span><br/> <span data-ttu-id="5fa9d-1619">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1619">0</span></span><br/>

<span data-ttu-id="5fa9d-1620">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1620">1</span></span>

<span data-ttu-id="5fa9d-1621">ограничение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1621">restriction</span></span>

<span data-ttu-id="5fa9d-1622">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1622">...</span></span>

<span data-ttu-id="5fa9d-1623">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1623">...</span></span>

<span data-ttu-id="5fa9d-1624">\_Key (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1624">\_key (variable)</span></span>

<span data-ttu-id="5fa9d-1625">\_Диапазон</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1625">\_isRange</span></span>



 

<span data-ttu-id="5fa9d-1626">**ограничение**: структура коккрестриктион, указывающая расположение слова.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1626">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="5fa9d-1627">**\_ Key**: структура ккэй, указывающая слово.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1627">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="5fa9d-1628">параметр **\_ Range**: Если задано значение 0x01, ключ является префиксом для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1628">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="5fa9d-1629">Если задано значение 0x00, то ключ является точным значением для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1629">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="5fa9d-1630">\_параметру "диапазон" не должно быть присвоено другое значение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1630">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="5fa9d-1631">2.2.1.16 Крестриктион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1631">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="5fa9d-1632">Структура Крестриктион содержит узел дерева команд запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1632">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="5fa9d-1633">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1633">0</span></span>

<span data-ttu-id="5fa9d-1634">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1634">1</span></span>

<span data-ttu-id="5fa9d-1635">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1635">2</span></span>

<span data-ttu-id="5fa9d-1636">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1636">3</span></span>

<span data-ttu-id="5fa9d-1637">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1637">4</span></span>

<span data-ttu-id="5fa9d-1638">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1638">5</span></span>

<span data-ttu-id="5fa9d-1639">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1639">6</span></span>

<span data-ttu-id="5fa9d-1640">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1640">7</span></span>

<span data-ttu-id="5fa9d-1641">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1641">8</span></span>

<span data-ttu-id="5fa9d-1642">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1642">9</span></span>

<span data-ttu-id="5fa9d-1643">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1643">1</span></span><br/> <span data-ttu-id="5fa9d-1644">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1644">0</span></span><br/>

<span data-ttu-id="5fa9d-1645">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1645">1</span></span>

<span data-ttu-id="5fa9d-1646">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1646">2</span></span>

<span data-ttu-id="5fa9d-1647">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1647">3</span></span>

<span data-ttu-id="5fa9d-1648">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1648">4</span></span>

<span data-ttu-id="5fa9d-1649">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1649">5</span></span>

<span data-ttu-id="5fa9d-1650">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1650">6</span></span>

<span data-ttu-id="5fa9d-1651">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1651">7</span></span>

<span data-ttu-id="5fa9d-1652">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1652">8</span></span>

<span data-ttu-id="5fa9d-1653">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1653">9</span></span>

<span data-ttu-id="5fa9d-1654">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1654">2</span></span><br/> <span data-ttu-id="5fa9d-1655">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1655">0</span></span><br/>

<span data-ttu-id="5fa9d-1656">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1656">1</span></span>

<span data-ttu-id="5fa9d-1657">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1657">2</span></span>

<span data-ttu-id="5fa9d-1658">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1658">3</span></span>

<span data-ttu-id="5fa9d-1659">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1659">4</span></span>

<span data-ttu-id="5fa9d-1660">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1660">5</span></span>

<span data-ttu-id="5fa9d-1661">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1661">6</span></span>

<span data-ttu-id="5fa9d-1662">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1662">7</span></span>

<span data-ttu-id="5fa9d-1663">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1663">8</span></span>

<span data-ttu-id="5fa9d-1664">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1664">9</span></span>

<span data-ttu-id="5fa9d-1665">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1665">3</span></span><br/> <span data-ttu-id="5fa9d-1666">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1666">0</span></span><br/>

<span data-ttu-id="5fa9d-1667">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1667">1</span></span>

<span data-ttu-id="5fa9d-1668">\_ултипе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1668">\_ulType</span></span>

<span data-ttu-id="5fa9d-1669">Вес</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1669">Weight</span></span>

<span data-ttu-id="5fa9d-1670">Ограничение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1670">Restriction</span></span>



 

<span data-ttu-id="5fa9d-1671">**\_ ултипе**: 32-битовое целое число без знака, указывающее тип ограничения, используемый для узла дерева команд.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1671">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="5fa9d-1672">НЕОБХОДИМО задать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1672">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="5fa9d-1673">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1673">Value</span></span>                    | <span data-ttu-id="5fa9d-1674">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1674">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-1675">Ртноне 0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1675">RTNone 0x00000000</span></span>        | <span data-ttu-id="5fa9d-1676">Узел представляет пропускаемое слово в векторном запросе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1676">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="5fa9d-1677">Ртанд 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1677">RTAnd 0x00000001</span></span>         | <span data-ttu-id="5fa9d-1678">Узел содержит Кнодерестриктион, на основе которого выполняется логическая операция.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1678">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="5fa9d-1679">РТор 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1679">RTOr 0x00000002</span></span>          | <span data-ttu-id="5fa9d-1680">Узел содержит Кнодерестриктион, для которого должна быть выполнена логическая операция или.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1680">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="5fa9d-1681">Ртнот 0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1681">RTNot 0x00000003</span></span>         | <span data-ttu-id="5fa9d-1682">Узел содержит Крестриктион, для которого не выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1682">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="5fa9d-1683">Ртконтент 0x00000004</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1683">RTContent 0x00000004</span></span>     | <span data-ttu-id="5fa9d-1684">Узел содержит Кконтентрестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1684">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="5fa9d-1685">Ртпроперти 0x00000005</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1685">RTProperty 0x00000005</span></span>    | <span data-ttu-id="5fa9d-1686">Узел содержит Кпропертирестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1686">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="5fa9d-1687">Ртпроксимити 0x00000006</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1687">RTProximity 0x00000006</span></span>   | <span data-ttu-id="5fa9d-1688">Узел содержит Кнодерестриктион, на основе которого будет выполняться ранжирование с учетом расположения,</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1688">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="5fa9d-1689">Ртвектор 0x00000007</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1689">RTVector 0x00000007</span></span>      | <span data-ttu-id="5fa9d-1690">Узел содержит Квекторрестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1690">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="5fa9d-1691">Ртнатлангуаже 0x00000008</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1691">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="5fa9d-1692">Узел содержит Кнатлангуажерестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1692">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="5fa9d-1693">Ртскопе 0x00000009</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1693">RTScope 0x00000009</span></span>       | <span data-ttu-id="5fa9d-1694">Узел содержит Кскоперестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1694">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="5fa9d-1695">ПРАНИ 0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1695">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="5fa9d-1696">Узел содержит Цинтерналпропертирестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1696">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="5fa9d-1697">Ртранже 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1697">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="5fa9d-1698">Узел содержит Кранжерестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1698">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="5fa9d-1699">Ртфрасе 0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1699">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="5fa9d-1700">Узел содержит Кнодерестриктион, для которого должно быть выполнено совпадение фразы.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1700">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="5fa9d-1701">Ртсиноним 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1701">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="5fa9d-1702">Узел содержит Ксинрестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1702">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="5fa9d-1703">Ртворд 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1703">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="5fa9d-1704">Узел содержит Квордрестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1704">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="5fa9d-1705">**Вес**: 32-битовое целое число без знака, представляющее вес узла.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1705">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="5fa9d-1706">Вес указывает на важность узла относительно других узлов в дереве команд запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1706">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="5fa9d-1707">Более важные значения веса более важны.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1707">Higher weight values are more important.</span></span>

<span data-ttu-id="5fa9d-1708">**Ограничение**: тип ограничения для узла дерева команд.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1708">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="5fa9d-1709">Синтаксис должен быть указан в \_ поле ултипе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1709">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="5fa9d-1710">2.2.1.17 Кколумнсет</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1710">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="5fa9d-1711">Структура Кколумнсет указывает возвращаемые номера столбцов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1711">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="5fa9d-1712">Эта структура всегда используется в ссылке на определенную структуру Кпидмаппер (раздел 2.2.1.23).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1712">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="5fa9d-1713">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1713">0</span></span>

<span data-ttu-id="5fa9d-1714">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1714">1</span></span>

<span data-ttu-id="5fa9d-1715">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1715">2</span></span>

<span data-ttu-id="5fa9d-1716">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1716">3</span></span>

<span data-ttu-id="5fa9d-1717">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1717">4</span></span>

<span data-ttu-id="5fa9d-1718">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1718">5</span></span>

<span data-ttu-id="5fa9d-1719">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1719">6</span></span>

<span data-ttu-id="5fa9d-1720">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1720">7</span></span>

<span data-ttu-id="5fa9d-1721">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1721">8</span></span>

<span data-ttu-id="5fa9d-1722">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1722">9</span></span>

<span data-ttu-id="5fa9d-1723">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1723">1</span></span><br/> <span data-ttu-id="5fa9d-1724">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1724">0</span></span><br/>

<span data-ttu-id="5fa9d-1725">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1725">1</span></span>

<span data-ttu-id="5fa9d-1726">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1726">2</span></span>

<span data-ttu-id="5fa9d-1727">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1727">3</span></span>

<span data-ttu-id="5fa9d-1728">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1728">4</span></span>

<span data-ttu-id="5fa9d-1729">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1729">5</span></span>

<span data-ttu-id="5fa9d-1730">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1730">6</span></span>

<span data-ttu-id="5fa9d-1731">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1731">7</span></span>

<span data-ttu-id="5fa9d-1732">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1732">8</span></span>

<span data-ttu-id="5fa9d-1733">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1733">9</span></span>

<span data-ttu-id="5fa9d-1734">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1734">2</span></span><br/> <span data-ttu-id="5fa9d-1735">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1735">0</span></span><br/>

<span data-ttu-id="5fa9d-1736">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1736">1</span></span>

<span data-ttu-id="5fa9d-1737">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1737">2</span></span>

<span data-ttu-id="5fa9d-1738">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1738">3</span></span>

<span data-ttu-id="5fa9d-1739">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1739">4</span></span>

<span data-ttu-id="5fa9d-1740">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1740">5</span></span>

<span data-ttu-id="5fa9d-1741">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1741">6</span></span>

<span data-ttu-id="5fa9d-1742">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1742">7</span></span>

<span data-ttu-id="5fa9d-1743">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1743">8</span></span>

<span data-ttu-id="5fa9d-1744">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1744">9</span></span>

<span data-ttu-id="5fa9d-1745">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1745">3</span></span><br/> <span data-ttu-id="5fa9d-1746">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1746">0</span></span><br/>

<span data-ttu-id="5fa9d-1747">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1747">1</span></span>

<span data-ttu-id="5fa9d-1748">count</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1748">count</span></span>

<span data-ttu-id="5fa9d-1749">индексы (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1749">indexes (variable)</span></span>



 

<span data-ttu-id="5fa9d-1750">**Count**: 32-разрядное целое число без знака, указывающее количество элементов в массиве индексов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1750">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="5fa9d-1751">**индексы**: массив из 4-байтных целых чисел без знака, представляющий индексы, начинающиеся с нуля, в массиве апропспек в соответствующей структуре кпидмаппер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1751">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="5fa9d-1752">2.2.1.18 Ккатегоризатионсет</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1752">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="5fa9d-1753">Структура Ккатегоризатионсет содержит сведения о группировании результирующего набора запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1753">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="5fa9d-1754">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1754">0</span></span>

<span data-ttu-id="5fa9d-1755">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1755">1</span></span>

<span data-ttu-id="5fa9d-1756">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1756">2</span></span>

<span data-ttu-id="5fa9d-1757">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1757">3</span></span>

<span data-ttu-id="5fa9d-1758">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1758">4</span></span>

<span data-ttu-id="5fa9d-1759">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1759">5</span></span>

<span data-ttu-id="5fa9d-1760">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1760">6</span></span>

<span data-ttu-id="5fa9d-1761">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1761">7</span></span>

<span data-ttu-id="5fa9d-1762">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1762">8</span></span>

<span data-ttu-id="5fa9d-1763">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1763">9</span></span>

<span data-ttu-id="5fa9d-1764">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1764">1</span></span><br/> <span data-ttu-id="5fa9d-1765">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1765">0</span></span><br/>

<span data-ttu-id="5fa9d-1766">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1766">1</span></span>

<span data-ttu-id="5fa9d-1767">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1767">2</span></span>

<span data-ttu-id="5fa9d-1768">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1768">3</span></span>

<span data-ttu-id="5fa9d-1769">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1769">4</span></span>

<span data-ttu-id="5fa9d-1770">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1770">5</span></span>

<span data-ttu-id="5fa9d-1771">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1771">6</span></span>

<span data-ttu-id="5fa9d-1772">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1772">7</span></span>

<span data-ttu-id="5fa9d-1773">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1773">8</span></span>

<span data-ttu-id="5fa9d-1774">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1774">9</span></span>

<span data-ttu-id="5fa9d-1775">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1775">2</span></span><br/> <span data-ttu-id="5fa9d-1776">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1776">0</span></span><br/>

<span data-ttu-id="5fa9d-1777">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1777">1</span></span>

<span data-ttu-id="5fa9d-1778">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1778">2</span></span>

<span data-ttu-id="5fa9d-1779">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1779">3</span></span>

<span data-ttu-id="5fa9d-1780">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1780">4</span></span>

<span data-ttu-id="5fa9d-1781">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1781">5</span></span>

<span data-ttu-id="5fa9d-1782">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1782">6</span></span>

<span data-ttu-id="5fa9d-1783">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1783">7</span></span>

<span data-ttu-id="5fa9d-1784">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1784">8</span></span>

<span data-ttu-id="5fa9d-1785">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1785">9</span></span>

<span data-ttu-id="5fa9d-1786">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1786">3</span></span><br/> <span data-ttu-id="5fa9d-1787">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1787">0</span></span><br/>

<span data-ttu-id="5fa9d-1788">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1788">1</span></span>

<span data-ttu-id="5fa9d-1789">count</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1789">count</span></span>

<span data-ttu-id="5fa9d-1790">категории (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1790">categories (variable)</span></span>



 

<span data-ttu-id="5fa9d-1791">**Count**: 32-разрядное целое число без знака, содержащее количество элементов в массиве Categories.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1791">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="5fa9d-1792">**Categories**: массив структур ккатегоризатионспек, задающий группирование запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1792">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="5fa9d-1793">2.2.1.19 Ккатегоризатионспек</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1793">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="5fa9d-1794">Структура Ккатегоризатионспек содержит группирование для результирующего набора запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1794">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="5fa9d-1795">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1795">0</span></span>

<span data-ttu-id="5fa9d-1796">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1796">1</span></span>

<span data-ttu-id="5fa9d-1797">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1797">2</span></span>

<span data-ttu-id="5fa9d-1798">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1798">3</span></span>

<span data-ttu-id="5fa9d-1799">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1799">4</span></span>

<span data-ttu-id="5fa9d-1800">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1800">5</span></span>

<span data-ttu-id="5fa9d-1801">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1801">6</span></span>

<span data-ttu-id="5fa9d-1802">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1802">7</span></span>

<span data-ttu-id="5fa9d-1803">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1803">8</span></span>

<span data-ttu-id="5fa9d-1804">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1804">9</span></span>

<span data-ttu-id="5fa9d-1805">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1805">1</span></span><br/> <span data-ttu-id="5fa9d-1806">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1806">0</span></span><br/>

<span data-ttu-id="5fa9d-1807">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1807">1</span></span>

<span data-ttu-id="5fa9d-1808">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1808">2</span></span>

<span data-ttu-id="5fa9d-1809">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1809">3</span></span>

<span data-ttu-id="5fa9d-1810">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1810">4</span></span>

<span data-ttu-id="5fa9d-1811">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1811">5</span></span>

<span data-ttu-id="5fa9d-1812">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1812">6</span></span>

<span data-ttu-id="5fa9d-1813">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1813">7</span></span>

<span data-ttu-id="5fa9d-1814">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1814">8</span></span>

<span data-ttu-id="5fa9d-1815">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1815">9</span></span>

<span data-ttu-id="5fa9d-1816">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1816">2</span></span><br/> <span data-ttu-id="5fa9d-1817">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1817">0</span></span><br/>

<span data-ttu-id="5fa9d-1818">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1818">1</span></span>

<span data-ttu-id="5fa9d-1819">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1819">2</span></span>

<span data-ttu-id="5fa9d-1820">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1820">3</span></span>

<span data-ttu-id="5fa9d-1821">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1821">4</span></span>

<span data-ttu-id="5fa9d-1822">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1822">5</span></span>

<span data-ttu-id="5fa9d-1823">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1823">6</span></span>

<span data-ttu-id="5fa9d-1824">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1824">7</span></span>

<span data-ttu-id="5fa9d-1825">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1825">8</span></span>

<span data-ttu-id="5fa9d-1826">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1826">9</span></span>

<span data-ttu-id="5fa9d-1827">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1827">3</span></span><br/> <span data-ttu-id="5fa9d-1828">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1828">0</span></span><br/>

<span data-ttu-id="5fa9d-1829">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1829">1</span></span>

<span data-ttu-id="5fa9d-1830">\_Ксколумнс (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1830">\_csColumns (variable)</span></span>

<span data-ttu-id="5fa9d-1831">\_улкатегтипе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1831">\_ulCategType</span></span>



 

<span data-ttu-id="5fa9d-1832">**\_ ксколумнс**: структура кколумнсет, указывающая столбцы, по которым будет группироваться запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1832">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="5fa9d-1833">**\_ улкатегтипе**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1833">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="5fa9d-1834">НЕОБХОДИМО задать значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1834">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="5fa9d-1835">2.2.1.20 Кдбколид</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1835">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="5fa9d-1836">Структура Кдбколид содержит столбец.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1836">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="5fa9d-1837">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1837">0</span></span>

<span data-ttu-id="5fa9d-1838">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1838">1</span></span>

<span data-ttu-id="5fa9d-1839">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1839">2</span></span>

<span data-ttu-id="5fa9d-1840">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1840">3</span></span>

<span data-ttu-id="5fa9d-1841">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1841">4</span></span>

<span data-ttu-id="5fa9d-1842">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1842">5</span></span>

<span data-ttu-id="5fa9d-1843">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1843">6</span></span>

<span data-ttu-id="5fa9d-1844">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1844">7</span></span>

<span data-ttu-id="5fa9d-1845">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1845">8</span></span>

<span data-ttu-id="5fa9d-1846">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1846">9</span></span>

<span data-ttu-id="5fa9d-1847">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1847">1</span></span><br/> <span data-ttu-id="5fa9d-1848">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1848">0</span></span><br/>

<span data-ttu-id="5fa9d-1849">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1849">1</span></span>

<span data-ttu-id="5fa9d-1850">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1850">2</span></span>

<span data-ttu-id="5fa9d-1851">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1851">3</span></span>

<span data-ttu-id="5fa9d-1852">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1852">4</span></span>

<span data-ttu-id="5fa9d-1853">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1853">5</span></span>

<span data-ttu-id="5fa9d-1854">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1854">6</span></span>

<span data-ttu-id="5fa9d-1855">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1855">7</span></span>

<span data-ttu-id="5fa9d-1856">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1856">8</span></span>

<span data-ttu-id="5fa9d-1857">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1857">9</span></span>

<span data-ttu-id="5fa9d-1858">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1858">2</span></span><br/> <span data-ttu-id="5fa9d-1859">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1859">0</span></span><br/>

<span data-ttu-id="5fa9d-1860">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1860">1</span></span>

<span data-ttu-id="5fa9d-1861">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1861">2</span></span>

<span data-ttu-id="5fa9d-1862">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1862">3</span></span>

<span data-ttu-id="5fa9d-1863">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1863">4</span></span>

<span data-ttu-id="5fa9d-1864">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1864">5</span></span>

<span data-ttu-id="5fa9d-1865">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1865">6</span></span>

<span data-ttu-id="5fa9d-1866">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1866">7</span></span>

<span data-ttu-id="5fa9d-1867">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1867">8</span></span>

<span data-ttu-id="5fa9d-1868">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1868">9</span></span>

<span data-ttu-id="5fa9d-1869">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1869">3</span></span><br/> <span data-ttu-id="5fa9d-1870">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1870">0</span></span><br/>

<span data-ttu-id="5fa9d-1871">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1871">1</span></span>

<span data-ttu-id="5fa9d-1872">Элемент ekind</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1872">eKind</span></span>

<span data-ttu-id="5fa9d-1873">Код GUID</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1873">GUID</span></span>

<span data-ttu-id="5fa9d-1874">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1874">...</span></span>

<span data-ttu-id="5fa9d-1875">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1875">...</span></span>

<span data-ttu-id="5fa9d-1876">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1876">...</span></span>

<span data-ttu-id="5fa9d-1877">улид</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1877">ulId</span></span>

<span data-ttu-id="5fa9d-1878">Встринг (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1878">vString (variable)</span></span>



 

<span data-ttu-id="5fa9d-1879">**элемент ekind**: необходимо задать одно из приведенных ниже значений, которое указывает содержимое GUID и управляемое vValue.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1879">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="5fa9d-1880">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1880">Value</span></span>                            | <span data-ttu-id="5fa9d-1881">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1881">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-1882">\_Имя GUID дбкинд \_ 0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1882">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="5fa9d-1883">Встринг содержит имя свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1883">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="5fa9d-1884">ДБКИНД \_ GUID \_ PropID 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1884">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="5fa9d-1885">Улид содержит 4-байтовое целое число, указывающее идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1885">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="5fa9d-1886">ДБКИНД \_ пгуид \_ имя 0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1886">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="5fa9d-1887">Встринг содержит имя свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1887">vString contains a property name.</span></span> <span data-ttu-id="5fa9d-1888">Это значение должно рассматриваться так же, как \_ и \_ имя GUID дбкинд.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1888">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="5fa9d-1889">ДБКИНД \_ пгуид \_ PropID 0x00000004</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1889">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="5fa9d-1890">Улид содержит 4-байтовое целое число, указывающее идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1890">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="5fa9d-1891">Это значение должно быть таким же, как и ДБКИНД \_ GUID \_ PropID.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1891">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="5fa9d-1892">**GUID**: идентификатор GUID свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1892">**GUID**: The property GUID.</span></span>

<span data-ttu-id="5fa9d-1893">**улид**: Если элемент ekind имеет значение дбкинд \_ GUID \_ PropID или дбкинд \_ пгуид \_ PropID, это поле содержит целое число без знака, в котором указывается идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1893">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="5fa9d-1894">Если элемент ekind имеет значение ДБКИНД \_ GUID \_ или имя дбкинд \_ пгуид \_ , это поле содержит целое число без знака, указывающее количество символов Юникода, содержащихся в поле встринг.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1894">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="5fa9d-1895">**встринг**: строка Юникода, не заканчивающаяся нулем, представляющая имя свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1895">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="5fa9d-1896">Его необходимо опустить, если для поля элемент ekind не задано значение ДБКИНД \_ GUID \_ Name или дбкинд \_ пгуид \_ Name.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1896">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="5fa9d-1897">2.2.1.21 Кдбпроп</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1897">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="5fa9d-1898">Структура Кдбпроп содержит свойство.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1898">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="5fa9d-1899">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1899">0</span></span>

<span data-ttu-id="5fa9d-1900">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1900">1</span></span>

<span data-ttu-id="5fa9d-1901">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1901">2</span></span>

<span data-ttu-id="5fa9d-1902">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1902">3</span></span>

<span data-ttu-id="5fa9d-1903">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1903">4</span></span>

<span data-ttu-id="5fa9d-1904">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1904">5</span></span>

<span data-ttu-id="5fa9d-1905">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1905">6</span></span>

<span data-ttu-id="5fa9d-1906">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1906">7</span></span>

<span data-ttu-id="5fa9d-1907">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1907">8</span></span>

<span data-ttu-id="5fa9d-1908">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1908">9</span></span>

<span data-ttu-id="5fa9d-1909">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1909">1</span></span><br/> <span data-ttu-id="5fa9d-1910">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1910">0</span></span><br/>

<span data-ttu-id="5fa9d-1911">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1911">1</span></span>

<span data-ttu-id="5fa9d-1912">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1912">2</span></span>

<span data-ttu-id="5fa9d-1913">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1913">3</span></span>

<span data-ttu-id="5fa9d-1914">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1914">4</span></span>

<span data-ttu-id="5fa9d-1915">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1915">5</span></span>

<span data-ttu-id="5fa9d-1916">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1916">6</span></span>

<span data-ttu-id="5fa9d-1917">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1917">7</span></span>

<span data-ttu-id="5fa9d-1918">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1918">8</span></span>

<span data-ttu-id="5fa9d-1919">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1919">9</span></span>

<span data-ttu-id="5fa9d-1920">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1920">2</span></span><br/> <span data-ttu-id="5fa9d-1921">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1921">0</span></span><br/>

<span data-ttu-id="5fa9d-1922">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1922">1</span></span>

<span data-ttu-id="5fa9d-1923">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1923">2</span></span>

<span data-ttu-id="5fa9d-1924">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1924">3</span></span>

<span data-ttu-id="5fa9d-1925">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1925">4</span></span>

<span data-ttu-id="5fa9d-1926">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1926">5</span></span>

<span data-ttu-id="5fa9d-1927">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1927">6</span></span>

<span data-ttu-id="5fa9d-1928">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1928">7</span></span>

<span data-ttu-id="5fa9d-1929">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1929">8</span></span>

<span data-ttu-id="5fa9d-1930">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1930">9</span></span>

<span data-ttu-id="5fa9d-1931">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1931">3</span></span><br/> <span data-ttu-id="5fa9d-1932">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1932">0</span></span><br/>

<span data-ttu-id="5fa9d-1933">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1933">1</span></span>

<span data-ttu-id="5fa9d-1934">дбпропид</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1934">DBPROPID</span></span>

<span data-ttu-id="5fa9d-1935">дбпропоптионс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1935">DBPROPOPTIONS</span></span>

<span data-ttu-id="5fa9d-1936">дбпропстатус</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1936">DBPROPSTATUS</span></span>

<span data-ttu-id="5fa9d-1937">идентификатора столбца (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1937">colid (variable)</span></span>

<span data-ttu-id="5fa9d-1938">Управляемое vValue (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1938">vValue (variable)</span></span>



 

<span data-ttu-id="5fa9d-1939">**Дбпропид**: 32-битовое целое число без знака, указывающее идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1939">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="5fa9d-1940">**Дбпропоптионс** : необходимо задать значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1940">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="5fa9d-1941">**Дбпропстатус**: необходимо задать значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1941">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="5fa9d-1942">**идентификатора столбца**: структура кдбколид, как указано в разделе 2.2.1.20, указывающая столбец, к которому применяется свойство.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1942">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="5fa9d-1943">**управляемое vValue**: кбасесторажевариант, содержащий значение свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1943">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="5fa9d-1944">свойства 2.2.1.21.1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1944">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="5fa9d-1945">В этом разделе описаны свойства, используемые CISP.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1945">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="5fa9d-1946">Эти свойства группируются в три набора свойств, Ident 2.2.1.21.1 ифиед в поле Гуидпропертисет структуры Кдбпропсет (раздел 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1946">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="5fa9d-1947">В следующей таблице перечислены свойства, которые являются частью \_ набора свойств DBPROPSET фсЦифрмврк \_ ext.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1947">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="5fa9d-1948">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1948">Value</span></span>                                  | <span data-ttu-id="5fa9d-1949">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1949">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-1950">DBPROP \_ CI \_ Catalog \_ имя 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1950">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="5fa9d-1951">Указывает имя каталога или каталогов для запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1951">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="5fa9d-1952">Значение должно быть VT \_ LPWSTR или \_ вектор VT \| \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="5fa9d-1953">DBPROP \_ CI \_ включает \_ области 0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1953">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="5fa9d-1954">Указывает один или несколько путей для включения в запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1954">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="5fa9d-1955">Значение должно быть VT \_ LPWSTR или \_ вектор VT \| \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1955">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="5fa9d-1956">\_ \_ Флаги области CI DBPROP \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1956">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="5fa9d-1957">Указывает, как должны обрабатываться пути, указанные в \_ \_ \_ свойстве областей DBPROP CI.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1957">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="5fa9d-1958">Значение должно быть VT \_ I4 или \_ вектор \| VT \_ i4.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1958">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="5fa9d-1959">\_ \_ Тип запроса DBPROP CI \_ 0x00000007</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1959">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="5fa9d-1960">Указывает тип запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1960">Specifies the type of query.</span></span> <span data-ttu-id="5fa9d-1961">Для Кдбколид должно быть задано значение DB \_ нуллид.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1961">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="5fa9d-1962">В следующей таблице перечислены флаги для \_ \_ \_ свойства Flags области DBPROP CI.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1962">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="5fa9d-1963">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1963">Value</span></span>                     | <span data-ttu-id="5fa9d-1964">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1964">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-1965">\_Глубокий запрос 0x01</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1965">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="5fa9d-1966">Если задано значение, указывает, что файлы в каталоге области и во всех подкаталогах включены в результаты.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1966">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="5fa9d-1967">Если задано значение Clear, в результаты включаются только файлы в каталоге области.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1967">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="5fa9d-1968">НЕ следует сочетать с QUERY \_ Deep.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1968">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="5fa9d-1969">ЗАПРОС \_ виртуального \_ пути 0x02</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1969">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="5fa9d-1970">Если задано значение, это указывает на то, что область является виртуальным путем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1970">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="5fa9d-1971">Если флажок снят, указывает, что область является физическим каталогом.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1971">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="5fa9d-1972">В следующей таблице перечислены типы запросов для \_ свойства типа "запрос CI DBPROP" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1972">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="5fa9d-1973">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1973">Value</span></span>                     | <span data-ttu-id="5fa9d-1974">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1974">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-1975">Цинормал 0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1975">CiNormal 0x00000000</span></span>       | <span data-ttu-id="5fa9d-1976">Обычный запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1976">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="5fa9d-1977">Цивиртуалрутс 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1977">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="5fa9d-1978">Запрос запрашивает список виртуальных корней каталога.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1978">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="5fa9d-1979">Для этого значения требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1979">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="5fa9d-1980">Ципропертиес 0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1980">CiProperties 0x00000003</span></span>   | <span data-ttu-id="5fa9d-1981">Запрос запрашивает список всех свойств, поддерживаемых службой индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1981">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="5fa9d-1982">Циадминоп 0x00000004</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1982">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="5fa9d-1983">Запрос является административной операцией.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1983">The query is an administrative operation.</span></span> <span data-ttu-id="5fa9d-1984">Для этого значения требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1984">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="5fa9d-1985">В следующей таблице перечислены свойства, которые являются частью \_ набора свойств DBPROPSET куерекст.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1985">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="5fa9d-1986">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1986">Value</span></span>                                      | <span data-ttu-id="5fa9d-1987">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1987">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-1988">DBPROP \_ усеконтентиндекс 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1988">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="5fa9d-1989">Указывает, как служба индексирования предназначена для обработки запросов с высокой скоростью.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1989">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="5fa9d-1990">Значение должно быть логическим значением VT \_ .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1990">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="5fa9d-1991">Значение TRUE показывает, что серверу разрешено завершать эти запросы.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1991">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="5fa9d-1992">DBPROP \_ дефернониндекседтримминг 0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1992">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="5fa9d-1993">Указывает, должна ли служба индексирования выполнять усечение результатов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1993">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="5fa9d-1994">Если значение равно TRUE, то сервер должен выполнять усечение результатов таким образом, чтобы оптимизировать время отклика клиенту.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1994">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="5fa9d-1995">Значение должно быть логическим значением VT \_ .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1995">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="5fa9d-1996">DBPROP \_ усикстендеддбтипес 0x00000004</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1996">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="5fa9d-1997">Указывает, поддерживает ли клиент \_ типы данных VT Vector.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1997">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="5fa9d-1998">Если значение — TRUE, клиент поддерживает \_ вектор VT; если значение равно false, то сервер должен преобразовать \_ векторные типы данных VT в \_ типы данных массива VT.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1998">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="5fa9d-1999">Значение должно быть логическим значением VT \_ .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-1999">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="5fa9d-2000">DBPROP \_ фирстровс 0x00000007</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2000">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="5fa9d-2001">Указывает, что строка соответствует возвращаемому значению.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2001">Indicates the row matches to return.</span></span> <span data-ttu-id="5fa9d-2002">Если значение равно TRUE, сервер должен возвращать первый набор совпадающих строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2002">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="5fa9d-2003">Если значение равно FALSE, то должны возвращаться наиболее подходящие строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2003">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="5fa9d-2004">Значение должно быть логическим значением VT \_ .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2004">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="5fa9d-2005">В следующей таблице перечислены свойства, которые являются частью \_ набора свойств DBPROPSET Цифрмврккоре \_ ext.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2005">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="5fa9d-2006">Значение/ДБПРОПИД</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2006">Value / DBPROPID</span></span>                 | <span data-ttu-id="5fa9d-2007">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2007">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-2008">DBPROP \_ машины 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2008">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="5fa9d-2009">Указывает имена компьютеров, на которых будет обрабатываться запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2009">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="5fa9d-2010">Значение должно быть либо VT \_ BSTR, либо VT \_ \| . VT \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2010">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="5fa9d-2011">\_0X00000003 DBPROP клиента \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2011">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="5fa9d-2012">Задает константу подключения для службы индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2012">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="5fa9d-2013">Значение должно быть \_ идентификатором CLSID VT, содержащим 0x2A4880706FD911D0A80800A0C906241A.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2013">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="5fa9d-2014">2.2.1.22 Кдбпропсет</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2014">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="5fa9d-2015">Структура Кдбпропсет содержит набор свойств.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2015">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="5fa9d-2016">Обратите внимание, что первое поле имеет фиксированный размер, но может не быть согласовано со смещением, которое является 4-байтовым числом, кратным началу сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2016">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="5fa9d-2017">Однако поле Кпропертиес будет выражаться таким образом, поэтому формат будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2017">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="5fa9d-2018">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2018">0</span></span>

<span data-ttu-id="5fa9d-2019">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2019">1</span></span>

<span data-ttu-id="5fa9d-2020">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2020">2</span></span>

<span data-ttu-id="5fa9d-2021">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2021">3</span></span>

<span data-ttu-id="5fa9d-2022">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2022">4</span></span>

<span data-ttu-id="5fa9d-2023">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2023">5</span></span>

<span data-ttu-id="5fa9d-2024">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2024">6</span></span>

<span data-ttu-id="5fa9d-2025">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2025">7</span></span>

<span data-ttu-id="5fa9d-2026">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2026">8</span></span>

<span data-ttu-id="5fa9d-2027">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2027">9</span></span>

<span data-ttu-id="5fa9d-2028">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2028">1</span></span><br/> <span data-ttu-id="5fa9d-2029">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2029">0</span></span><br/>

<span data-ttu-id="5fa9d-2030">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2030">1</span></span>

<span data-ttu-id="5fa9d-2031">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2031">2</span></span>

<span data-ttu-id="5fa9d-2032">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2032">3</span></span>

<span data-ttu-id="5fa9d-2033">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2033">4</span></span>

<span data-ttu-id="5fa9d-2034">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2034">5</span></span>

<span data-ttu-id="5fa9d-2035">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2035">6</span></span>

<span data-ttu-id="5fa9d-2036">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2036">7</span></span>

<span data-ttu-id="5fa9d-2037">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2037">8</span></span>

<span data-ttu-id="5fa9d-2038">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2038">9</span></span>

<span data-ttu-id="5fa9d-2039">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2039">2</span></span><br/> <span data-ttu-id="5fa9d-2040">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2040">0</span></span><br/>

<span data-ttu-id="5fa9d-2041">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2041">1</span></span>

<span data-ttu-id="5fa9d-2042">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2042">2</span></span>

<span data-ttu-id="5fa9d-2043">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2043">3</span></span>

<span data-ttu-id="5fa9d-2044">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2044">4</span></span>

<span data-ttu-id="5fa9d-2045">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2045">5</span></span>

<span data-ttu-id="5fa9d-2046">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2046">6</span></span>

<span data-ttu-id="5fa9d-2047">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2047">7</span></span>

<span data-ttu-id="5fa9d-2048">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2048">8</span></span>

<span data-ttu-id="5fa9d-2049">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2049">9</span></span>

<span data-ttu-id="5fa9d-2050">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2050">3</span></span><br/> <span data-ttu-id="5fa9d-2051">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2051">0</span></span><br/>

<span data-ttu-id="5fa9d-2052">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2052">1</span></span>

<span data-ttu-id="5fa9d-2053">гуидпропертисет</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2053">guidPropertySet</span></span>

<span data-ttu-id="5fa9d-2054">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2054">...</span></span>

<span data-ttu-id="5fa9d-2055">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2055">...</span></span>

<span data-ttu-id="5fa9d-2056">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2056">...</span></span>

<span data-ttu-id="5fa9d-2057">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2057">...</span></span>

<span data-ttu-id="5fa9d-2058">\_Заполнение (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2058">\_padding (variable)</span></span>

<span data-ttu-id="5fa9d-2059">кпропертиес</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2059">cProperties</span></span>

<span data-ttu-id="5fa9d-2060">Апропс (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2060">aProps (variable)</span></span>



 

<span data-ttu-id="5fa9d-2061">**гуидпропертисет**: идентификатор GUID, определяющий набор свойств.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2061">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="5fa9d-2062">НЕОБХОДИМО задать двоичную форму, соответствующую одному из следующих значений (отображается в форме строкового представления), определяя набор свойств свойств, содержащихся в поле Апропс.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2062">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="5fa9d-2063">Значение/GUID</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2063">Value / GUID</span></span>                                                                              | <span data-ttu-id="5fa9d-2064">Имя</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2064">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="5fa9d-2065">DBPROPSET \_ фсЦифрмврк \_ ext</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2065">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="5fa9d-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="5fa9d-2067">Набор свойств платформы индекса содержимого файловой системы</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2067">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="5fa9d-2068">DBPROPSET \_ куерекст</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2068">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="5fa9d-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="5fa9d-2070">Набор свойств расширения запроса</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2070">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="5fa9d-2071">DBPROPSET \_ Цифрмврккоре \_ ext</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2071">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="5fa9d-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="5fa9d-2073">Набор свойств Core платформы индекса содержимого</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2073">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="5fa9d-2074">**\_ Заполнение**: это поле должно иметь длину от 0 до 3 байт.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2074">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="5fa9d-2075">Длина этого поля должна быть такой, что следующее поле начинается со смещения, кратного 4 байтам от начала сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2075">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="5fa9d-2076">Если это поле имеется (т. е. Длина не равно нулю), то значение, которое он содержит, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2076">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="5fa9d-2077">Содержимое этого поля должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2077">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="5fa9d-2078">**кпропертиес**: 32-разрядное целое число без знака, содержащее количество элементов в массиве апропс.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2078">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="5fa9d-2079">**апропс**: массив структур кдбпроп, как указано в разделе 0, содержащем свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2079">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="5fa9d-2080">Структуры в массиве должны быть разделены от 0 до 3 байтов, так что каждая структура начинается со смещения, кратного 4 байтам от начала сообщения, содержащего этот массив.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2080">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="5fa9d-2081">Если заданы байты заполнения, то значение, которое они содержат, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2081">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="5fa9d-2082">Содержимое байтов заполнения должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2082">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="5fa9d-2083">2.2.1.23 Кпидмаппер</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2083">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="5fa9d-2084">Структура Кпидмаппер содержит массив идентификаторов свойств, указывающих свойства, возвращаемые в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2084">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="5fa9d-2085">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2085">0</span></span>

<span data-ttu-id="5fa9d-2086">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2086">1</span></span>

<span data-ttu-id="5fa9d-2087">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2087">2</span></span>

<span data-ttu-id="5fa9d-2088">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2088">3</span></span>

<span data-ttu-id="5fa9d-2089">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2089">4</span></span>

<span data-ttu-id="5fa9d-2090">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2090">5</span></span>

<span data-ttu-id="5fa9d-2091">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2091">6</span></span>

<span data-ttu-id="5fa9d-2092">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2092">7</span></span>

<span data-ttu-id="5fa9d-2093">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2093">8</span></span>

<span data-ttu-id="5fa9d-2094">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2094">9</span></span>

<span data-ttu-id="5fa9d-2095">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2095">1</span></span><br/> <span data-ttu-id="5fa9d-2096">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2096">0</span></span><br/>

<span data-ttu-id="5fa9d-2097">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2097">1</span></span>

<span data-ttu-id="5fa9d-2098">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2098">2</span></span>

<span data-ttu-id="5fa9d-2099">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2099">3</span></span>

<span data-ttu-id="5fa9d-2100">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2100">4</span></span>

<span data-ttu-id="5fa9d-2101">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2101">5</span></span>

<span data-ttu-id="5fa9d-2102">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2102">6</span></span>

<span data-ttu-id="5fa9d-2103">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2103">7</span></span>

<span data-ttu-id="5fa9d-2104">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2104">8</span></span>

<span data-ttu-id="5fa9d-2105">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2105">9</span></span>

<span data-ttu-id="5fa9d-2106">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2106">2</span></span><br/> <span data-ttu-id="5fa9d-2107">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2107">0</span></span><br/>

<span data-ttu-id="5fa9d-2108">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2108">1</span></span>

<span data-ttu-id="5fa9d-2109">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2109">2</span></span>

<span data-ttu-id="5fa9d-2110">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2110">3</span></span>

<span data-ttu-id="5fa9d-2111">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2111">4</span></span>

<span data-ttu-id="5fa9d-2112">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2112">5</span></span>

<span data-ttu-id="5fa9d-2113">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2113">6</span></span>

<span data-ttu-id="5fa9d-2114">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2114">7</span></span>

<span data-ttu-id="5fa9d-2115">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2115">8</span></span>

<span data-ttu-id="5fa9d-2116">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2116">9</span></span>

<span data-ttu-id="5fa9d-2117">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2117">3</span></span><br/> <span data-ttu-id="5fa9d-2118">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2118">0</span></span><br/>

<span data-ttu-id="5fa9d-2119">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2119">1</span></span>

<span data-ttu-id="5fa9d-2120">count</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2120">count</span></span>

<span data-ttu-id="5fa9d-2121">апропспек</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2121">aPropSpec</span></span>

<span data-ttu-id="5fa9d-2122">... перемен</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2122">... (variable)</span></span>



 

<span data-ttu-id="5fa9d-2123">**Count**: 32-разрядное целое число без знака, содержащее количество элементов в массиве апропспек.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2123">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="5fa9d-2124">**апропспек**: массив структур кфуллпропспек, указывающих возвращаемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2124">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="5fa9d-2125">Структуры в массиве должны быть разделены от 0 до 3 байтов с отступом таким, что каждая структура имеет 4-байтовое выравнивание от начала сообщения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2125">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="5fa9d-2126">Такое заполнение байтов может быть любым произвольным значением и не должно учитываться при получении.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2126">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="5fa9d-2127">2.2.1.24 Кровсикат</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2127">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="5fa9d-2128">Структура Кровсикат содержит смещение для получения строк в сообщении Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2128">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="5fa9d-2129">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2129">0</span></span>

<span data-ttu-id="5fa9d-2130">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2130">1</span></span>

<span data-ttu-id="5fa9d-2131">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2131">2</span></span>

<span data-ttu-id="5fa9d-2132">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2132">3</span></span>

<span data-ttu-id="5fa9d-2133">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2133">4</span></span>

<span data-ttu-id="5fa9d-2134">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2134">5</span></span>

<span data-ttu-id="5fa9d-2135">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2135">6</span></span>

<span data-ttu-id="5fa9d-2136">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2136">7</span></span>

<span data-ttu-id="5fa9d-2137">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2137">8</span></span>

<span data-ttu-id="5fa9d-2138">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2138">9</span></span>

<span data-ttu-id="5fa9d-2139">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2139">1</span></span><br/> <span data-ttu-id="5fa9d-2140">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2140">0</span></span><br/>

<span data-ttu-id="5fa9d-2141">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2141">1</span></span>

<span data-ttu-id="5fa9d-2142">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2142">2</span></span>

<span data-ttu-id="5fa9d-2143">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2143">3</span></span>

<span data-ttu-id="5fa9d-2144">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2144">4</span></span>

<span data-ttu-id="5fa9d-2145">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2145">5</span></span>

<span data-ttu-id="5fa9d-2146">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2146">6</span></span>

<span data-ttu-id="5fa9d-2147">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2147">7</span></span>

<span data-ttu-id="5fa9d-2148">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2148">8</span></span>

<span data-ttu-id="5fa9d-2149">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2149">9</span></span>

<span data-ttu-id="5fa9d-2150">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2150">2</span></span><br/> <span data-ttu-id="5fa9d-2151">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2151">0</span></span><br/>

<span data-ttu-id="5fa9d-2152">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2152">1</span></span>

<span data-ttu-id="5fa9d-2153">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2153">2</span></span>

<span data-ttu-id="5fa9d-2154">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2154">3</span></span>

<span data-ttu-id="5fa9d-2155">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2155">4</span></span>

<span data-ttu-id="5fa9d-2156">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2156">5</span></span>

<span data-ttu-id="5fa9d-2157">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2157">6</span></span>

<span data-ttu-id="5fa9d-2158">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2158">7</span></span>

<span data-ttu-id="5fa9d-2159">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2159">8</span></span>

<span data-ttu-id="5fa9d-2160">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2160">9</span></span>

<span data-ttu-id="5fa9d-2161">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2161">3</span></span><br/> <span data-ttu-id="5fa9d-2162">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2162">0</span></span><br/>

<span data-ttu-id="5fa9d-2163">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2163">1</span></span>

<span data-ttu-id="5fa9d-2164">\_хрегион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2164">\_hRegion</span></span>

<span data-ttu-id="5fa9d-2165">\_кскип</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2165">\_cskip</span></span>

<span data-ttu-id="5fa9d-2166">\_бмкоффсет</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2166">\_bmkOffset</span></span>



 

<span data-ttu-id="5fa9d-2167">**\_ хрегион**: необходимо задать значение 0x00000000, и оно должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2167">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="5fa9d-2168">**\_ кскип**: 32-битовое целое число без знака, содержащее количество строк для пропуска в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2168">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="5fa9d-2169">**\_ бмкоффсет**: 32-разрядное значение, представляющее маркер **закладки** , указывающий начальную точку, с которой следует пропускать число строк, указанное в \_ кскип, перед началом извлечения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2169">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="5fa9d-2170">2.2.1.25 Кровсикатратио</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2170">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="5fa9d-2171">Структура Кровсикатратио определяет точку, с которой начинается извлечение сообщения Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2171">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="5fa9d-2172">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2172">0</span></span>

<span data-ttu-id="5fa9d-2173">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2173">1</span></span>

<span data-ttu-id="5fa9d-2174">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2174">2</span></span>

<span data-ttu-id="5fa9d-2175">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2175">3</span></span>

<span data-ttu-id="5fa9d-2176">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2176">4</span></span>

<span data-ttu-id="5fa9d-2177">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2177">5</span></span>

<span data-ttu-id="5fa9d-2178">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2178">6</span></span>

<span data-ttu-id="5fa9d-2179">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2179">7</span></span>

<span data-ttu-id="5fa9d-2180">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2180">8</span></span>

<span data-ttu-id="5fa9d-2181">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2181">9</span></span>

<span data-ttu-id="5fa9d-2182">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2182">1</span></span><br/> <span data-ttu-id="5fa9d-2183">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2183">0</span></span><br/>

<span data-ttu-id="5fa9d-2184">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2184">1</span></span>

<span data-ttu-id="5fa9d-2185">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2185">2</span></span>

<span data-ttu-id="5fa9d-2186">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2186">3</span></span>

<span data-ttu-id="5fa9d-2187">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2187">4</span></span>

<span data-ttu-id="5fa9d-2188">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2188">5</span></span>

<span data-ttu-id="5fa9d-2189">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2189">6</span></span>

<span data-ttu-id="5fa9d-2190">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2190">7</span></span>

<span data-ttu-id="5fa9d-2191">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2191">8</span></span>

<span data-ttu-id="5fa9d-2192">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2192">9</span></span>

<span data-ttu-id="5fa9d-2193">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2193">2</span></span><br/> <span data-ttu-id="5fa9d-2194">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2194">0</span></span><br/>

<span data-ttu-id="5fa9d-2195">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2195">1</span></span>

<span data-ttu-id="5fa9d-2196">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2196">2</span></span>

<span data-ttu-id="5fa9d-2197">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2197">3</span></span>

<span data-ttu-id="5fa9d-2198">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2198">4</span></span>

<span data-ttu-id="5fa9d-2199">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2199">5</span></span>

<span data-ttu-id="5fa9d-2200">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2200">6</span></span>

<span data-ttu-id="5fa9d-2201">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2201">7</span></span>

<span data-ttu-id="5fa9d-2202">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2202">8</span></span>

<span data-ttu-id="5fa9d-2203">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2203">9</span></span>

<span data-ttu-id="5fa9d-2204">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2204">3</span></span><br/> <span data-ttu-id="5fa9d-2205">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2205">0</span></span><br/>

<span data-ttu-id="5fa9d-2206">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2206">1</span></span>

<span data-ttu-id="5fa9d-2207">Цитблчапт</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2207">CiTblChapt</span></span>

<span data-ttu-id="5fa9d-2208">\_хрегион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2208">\_hRegion</span></span>

<span data-ttu-id="5fa9d-2209">\_улнумератор</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2209">\_ulNumerator</span></span>

<span data-ttu-id="5fa9d-2210">\_улденоминатор</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2210">\_ulDenominator</span></span>



 

<span data-ttu-id="5fa9d-2211">**Цитблчапт**: 32-битовое целое число без знака, указывающее главу набора строк, из которой нужно получить строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2211">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="5fa9d-2212">**\_ хрегион**: необходимо задать значение 0x00000000, и оно должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2212">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="5fa9d-2213">**\_ улнумератор**: 32-разрядное целое число без знака, представляющее числитель количества строк в главе, с которых начинается извлечение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2213">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="5fa9d-2214">**\_ улденоминатор**: 32-разрядное целое число без знака, представляющее знаменатель отношения количества строк в главе, с которых начинается извлечение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2214">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="5fa9d-2215">ДОЛЖНО быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2215">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="5fa9d-2216">2.2.1.26 Кровсикбибукмарк</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2216">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="5fa9d-2217">Структура Кровсикбибукмарк определяет закладки, из которых начинается получение строк для сообщения Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2217">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="5fa9d-2218">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2218">0</span></span>

<span data-ttu-id="5fa9d-2219">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2219">1</span></span>

<span data-ttu-id="5fa9d-2220">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2220">2</span></span>

<span data-ttu-id="5fa9d-2221">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2221">3</span></span>

<span data-ttu-id="5fa9d-2222">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2222">4</span></span>

<span data-ttu-id="5fa9d-2223">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2223">5</span></span>

<span data-ttu-id="5fa9d-2224">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2224">6</span></span>

<span data-ttu-id="5fa9d-2225">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2225">7</span></span>

<span data-ttu-id="5fa9d-2226">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2226">8</span></span>

<span data-ttu-id="5fa9d-2227">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2227">9</span></span>

<span data-ttu-id="5fa9d-2228">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2228">1</span></span><br/> <span data-ttu-id="5fa9d-2229">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2229">0</span></span><br/>

<span data-ttu-id="5fa9d-2230">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2230">1</span></span>

<span data-ttu-id="5fa9d-2231">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2231">2</span></span>

<span data-ttu-id="5fa9d-2232">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2232">3</span></span>

<span data-ttu-id="5fa9d-2233">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2233">4</span></span>

<span data-ttu-id="5fa9d-2234">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2234">5</span></span>

<span data-ttu-id="5fa9d-2235">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2235">6</span></span>

<span data-ttu-id="5fa9d-2236">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2236">7</span></span>

<span data-ttu-id="5fa9d-2237">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2237">8</span></span>

<span data-ttu-id="5fa9d-2238">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2238">9</span></span>

<span data-ttu-id="5fa9d-2239">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2239">2</span></span><br/> <span data-ttu-id="5fa9d-2240">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2240">0</span></span><br/>

<span data-ttu-id="5fa9d-2241">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2241">1</span></span>

<span data-ttu-id="5fa9d-2242">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2242">2</span></span>

<span data-ttu-id="5fa9d-2243">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2243">3</span></span>

<span data-ttu-id="5fa9d-2244">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2244">4</span></span>

<span data-ttu-id="5fa9d-2245">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2245">5</span></span>

<span data-ttu-id="5fa9d-2246">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2246">6</span></span>

<span data-ttu-id="5fa9d-2247">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2247">7</span></span>

<span data-ttu-id="5fa9d-2248">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2248">8</span></span>

<span data-ttu-id="5fa9d-2249">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2249">9</span></span>

<span data-ttu-id="5fa9d-2250">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2250">3</span></span><br/> <span data-ttu-id="5fa9d-2251">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2251">0</span></span><br/>

<span data-ttu-id="5fa9d-2252">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2252">1</span></span>

<span data-ttu-id="5fa9d-2253">\_хрегион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2253">\_hRegion</span></span>

<span data-ttu-id="5fa9d-2254">\_кбукмаркс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2254">\_cBookmarks</span></span>

<span data-ttu-id="5fa9d-2255">\_максрет</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2255">\_maxRet</span></span>

<span data-ttu-id="5fa9d-2256">\_квалидрет</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2256">\_cValidRet</span></span>

<span data-ttu-id="5fa9d-2257">\_Абукмаркс (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2257">\_aBookmarks (variable)</span></span>

<span data-ttu-id="5fa9d-2258">\_Аскрет (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2258">\_ascRet (variable)</span></span>



 

<span data-ttu-id="5fa9d-2259">**\_ хрегион**: необходимо задать значение 0x00000000, и оно должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2259">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="5fa9d-2260">**\_ кбукмаркс**: 32-разрядное целое число без знака, представляющее число элементов в \_ массиве абукмаркс.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2260">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="5fa9d-2261">**\_ максрет**: 32-разрядное целое число без знака, представляющее число элементов в \_ массиве аскрет.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2261">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="5fa9d-2262">**\_ квалидрет**: 32-разрядное целое число без знака, представляющее число \_ допустимых элементов в массиве аскрет.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2262">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="5fa9d-2263">В массиве определены допустимые элементы, тогда как недопустимые элементы не определены.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2263">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="5fa9d-2264">**\_ абукмаркс**: массив дескрипторов закладок (каждый из которых представлен 4 байта), полученный из сообщения кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2264">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="5fa9d-2265">**\_ аскрет**: массив значений HRESULT.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2265">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="5fa9d-2266">Когда Кровсикбибукмарк отправляется как часть запроса Кпмжетровсин, число записей в массиве должно быть равно \_ кбукмаркс.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2266">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="5fa9d-2267">При отправке клиентом значения должны быть равны нулю, а сервер должен игнорировать содержимое массива.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2267">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="5fa9d-2268">При отправке сервером (в составе сообщения Кпмжетровсаут) значения в массиве указывают состояние результата для каждого извлечения строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2268">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="5fa9d-2269">2.2.1.27 Кровсикнекст</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2269">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="5fa9d-2270">Структура Кровсикнекст содержит число строк, которые необходимо пропустить в сообщении Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2270">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="5fa9d-2271">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2271">0</span></span>

<span data-ttu-id="5fa9d-2272">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2272">1</span></span>

<span data-ttu-id="5fa9d-2273">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2273">2</span></span>

<span data-ttu-id="5fa9d-2274">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2274">3</span></span>

<span data-ttu-id="5fa9d-2275">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2275">4</span></span>

<span data-ttu-id="5fa9d-2276">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2276">5</span></span>

<span data-ttu-id="5fa9d-2277">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2277">6</span></span>

<span data-ttu-id="5fa9d-2278">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2278">7</span></span>

<span data-ttu-id="5fa9d-2279">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2279">8</span></span>

<span data-ttu-id="5fa9d-2280">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2280">9</span></span>

<span data-ttu-id="5fa9d-2281">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2281">1</span></span><br/> <span data-ttu-id="5fa9d-2282">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2282">0</span></span><br/>

<span data-ttu-id="5fa9d-2283">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2283">1</span></span>

<span data-ttu-id="5fa9d-2284">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2284">2</span></span>

<span data-ttu-id="5fa9d-2285">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2285">3</span></span>

<span data-ttu-id="5fa9d-2286">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2286">4</span></span>

<span data-ttu-id="5fa9d-2287">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2287">5</span></span>

<span data-ttu-id="5fa9d-2288">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2288">6</span></span>

<span data-ttu-id="5fa9d-2289">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2289">7</span></span>

<span data-ttu-id="5fa9d-2290">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2290">8</span></span>

<span data-ttu-id="5fa9d-2291">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2291">9</span></span>

<span data-ttu-id="5fa9d-2292">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2292">2</span></span><br/> <span data-ttu-id="5fa9d-2293">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2293">0</span></span><br/>

<span data-ttu-id="5fa9d-2294">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2294">1</span></span>

<span data-ttu-id="5fa9d-2295">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2295">2</span></span>

<span data-ttu-id="5fa9d-2296">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2296">3</span></span>

<span data-ttu-id="5fa9d-2297">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2297">4</span></span>

<span data-ttu-id="5fa9d-2298">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2298">5</span></span>

<span data-ttu-id="5fa9d-2299">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2299">6</span></span>

<span data-ttu-id="5fa9d-2300">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2300">7</span></span>

<span data-ttu-id="5fa9d-2301">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2301">8</span></span>

<span data-ttu-id="5fa9d-2302">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2302">9</span></span>

<span data-ttu-id="5fa9d-2303">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2303">3</span></span><br/> <span data-ttu-id="5fa9d-2304">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2304">0</span></span><br/>

<span data-ttu-id="5fa9d-2305">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2305">1</span></span>

<span data-ttu-id="5fa9d-2306">Цитблчапт</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2306">CiTblChapt</span></span>

<span data-ttu-id="5fa9d-2307">\_хрегион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2307">\_hRegion</span></span>

<span data-ttu-id="5fa9d-2308">\_кскип</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2308">\_cskip</span></span>



 

<span data-ttu-id="5fa9d-2309">**Цитблчапт**: 32-разрядное целое число без знака, указывающее главу набора строк, из которой нужно получить строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2309">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="5fa9d-2310">**\_ хрегион**: необходимо задать значение 0x00000000, и оно должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2310">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="5fa9d-2311">**\_ кскип**: 32-разрядное целое число без знака, представляющее число строк для пропуска в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2311">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="5fa9d-2312">2.2.1.28 Кровсетпропертиес</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2312">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="5fa9d-2313">Структура Кровсетпропертиес содержит сведения о конфигурации для запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2313">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="5fa9d-2314">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2314">0</span></span>

<span data-ttu-id="5fa9d-2315">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2315">1</span></span>

<span data-ttu-id="5fa9d-2316">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2316">2</span></span>

<span data-ttu-id="5fa9d-2317">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2317">3</span></span>

<span data-ttu-id="5fa9d-2318">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2318">4</span></span>

<span data-ttu-id="5fa9d-2319">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2319">5</span></span>

<span data-ttu-id="5fa9d-2320">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2320">6</span></span>

<span data-ttu-id="5fa9d-2321">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2321">7</span></span>

<span data-ttu-id="5fa9d-2322">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2322">8</span></span>

<span data-ttu-id="5fa9d-2323">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2323">9</span></span>

<span data-ttu-id="5fa9d-2324">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2324">1</span></span><br/> <span data-ttu-id="5fa9d-2325">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2325">0</span></span><br/>

<span data-ttu-id="5fa9d-2326">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2326">1</span></span>

<span data-ttu-id="5fa9d-2327">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2327">2</span></span>

<span data-ttu-id="5fa9d-2328">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2328">3</span></span>

<span data-ttu-id="5fa9d-2329">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2329">4</span></span>

<span data-ttu-id="5fa9d-2330">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2330">5</span></span>

<span data-ttu-id="5fa9d-2331">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2331">6</span></span>

<span data-ttu-id="5fa9d-2332">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2332">7</span></span>

<span data-ttu-id="5fa9d-2333">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2333">8</span></span>

<span data-ttu-id="5fa9d-2334">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2334">9</span></span>

<span data-ttu-id="5fa9d-2335">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2335">2</span></span><br/> <span data-ttu-id="5fa9d-2336">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2336">0</span></span><br/>

<span data-ttu-id="5fa9d-2337">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2337">1</span></span>

<span data-ttu-id="5fa9d-2338">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2338">2</span></span>

<span data-ttu-id="5fa9d-2339">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2339">3</span></span>

<span data-ttu-id="5fa9d-2340">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2340">4</span></span>

<span data-ttu-id="5fa9d-2341">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2341">5</span></span>

<span data-ttu-id="5fa9d-2342">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2342">6</span></span>

<span data-ttu-id="5fa9d-2343">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2343">7</span></span>

<span data-ttu-id="5fa9d-2344">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2344">8</span></span>

<span data-ttu-id="5fa9d-2345">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2345">9</span></span>

<span data-ttu-id="5fa9d-2346">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2346">3</span></span><br/> <span data-ttu-id="5fa9d-2347">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2347">0</span></span><br/>

<span data-ttu-id="5fa9d-2348">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2348">1</span></span>

<span data-ttu-id="5fa9d-2349">\_убулеаноптионс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2349">\_uBooleanOptions</span></span>

<span data-ttu-id="5fa9d-2350">\_улмаксопенровс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2350">\_ulMaxOpenRows</span></span>

<span data-ttu-id="5fa9d-2351">\_улмеморюсаже</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2351">\_ulMemoryUsage</span></span>

<span data-ttu-id="5fa9d-2352">\_кмаксресултс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2352">\_cMaxResults</span></span>

<span data-ttu-id="5fa9d-2353">\_ккмдтимеаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2353">\_cCmdTimeout</span></span>



 

<span data-ttu-id="5fa9d-2354">**\_ убулеаноптионс**: наименее значимые 3 бита этого поля должны содержать одно из следующих трех значений:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2354">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="5fa9d-2355">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2355">Value</span></span>                  | <span data-ttu-id="5fa9d-2356">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2356">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-2357">Есекуентиал 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2357">eSequential 0x00000001</span></span> | <span data-ttu-id="5fa9d-2358">Курсор можно переместить только вперед.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2358">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="5fa9d-2359">Елокатабле 0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2359">eLocatable 0x00000003</span></span>  | <span data-ttu-id="5fa9d-2360">Курсор можно переместить в любую позицию.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2360">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="5fa9d-2361">Ескроллабле 0x00000007</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2361">eScrollable 0x00000007</span></span> | <span data-ttu-id="5fa9d-2362">Курсор можно переместить в любую позицию и получить в любом направлении.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2362">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="5fa9d-2363">Остальные биты могут быть либо понятны, либо установлены в любое сочетание следующих логических значений или совместно.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2363">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="5fa9d-2364">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2364">Value</span></span>                     | <span data-ttu-id="5fa9d-2365">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2365">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-2366">Еасинчронаус 0x00000008</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2366">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="5fa9d-2367">Клиент не будет ждать завершения выполнения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2367">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="5fa9d-2368">Ефирстровс 0x00000080</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2368">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="5fa9d-2369">Возвращение первых обнаруженных строк, а не наиболее подходящих соответствий.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2369">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="5fa9d-2370">Ехолдровс 0x00000200</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2370">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="5fa9d-2371">Сервер не должен отбрасывать строки до тех пор, пока клиент не завершит запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2371">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="5fa9d-2372">Ечаптеред 0x00000800</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2372">eChaptered 0x00000800</span></span>     | <span data-ttu-id="5fa9d-2373">Набор строк поддерживает главы.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2373">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="5fa9d-2374">ЕусеЦи 0x00001000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2374">eUseCI 0x00001000</span></span>         | <span data-ttu-id="5fa9d-2375">Отвечайте на запрос только из индекса, а не из файловой системы.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2375">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="5fa9d-2376">Едефертримминг 0x00002000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2376">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="5fa9d-2377">Служба индексирования позволяет оптимизировать время отклика клиенту при удалении результатов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2377">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="5fa9d-2378">**\_ улмаксопенровс**: 32-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2378">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="5fa9d-2379">Необходимо задать значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="5fa9d-2380">Не используется и должен игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="5fa9d-2381">**\_ улмеморюсаже**: 32-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2381">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="5fa9d-2382">Необходимо задать значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2382">Must be set to 0x00000000.</span></span> <span data-ttu-id="5fa9d-2383">Не используется и должен игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2383">Not used and MUST be ignored.</span></span>

<span data-ttu-id="5fa9d-2384">**\_ кмаксресултс**: 32-разрядное целое число без знака, указывающее максимальное количество строк, возвращаемых для запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2384">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="5fa9d-2385">**\_ ккмдтимеаут**: 32-разрядное целое число без знака, определяющее время ожидания запроса (в секундах) и автоматическое завершение, считая от момента начала выполнения запроса на сервере.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2385">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="5fa9d-2386">Значение 0x00000000 означает, что время ожидания запроса не истекло.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2386">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="5fa9d-2387">2.2.1.29 Кроввариант</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2387">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="5fa9d-2388">Структура Кроввариант содержит часть фиксированного размера типа данных переменной длины, которая хранится в сообщении Кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2388">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="5fa9d-2389">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2389">0</span></span>

<span data-ttu-id="5fa9d-2390">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2390">1</span></span>

<span data-ttu-id="5fa9d-2391">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2391">2</span></span>

<span data-ttu-id="5fa9d-2392">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2392">3</span></span>

<span data-ttu-id="5fa9d-2393">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2393">4</span></span>

<span data-ttu-id="5fa9d-2394">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2394">5</span></span>

<span data-ttu-id="5fa9d-2395">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2395">6</span></span>

<span data-ttu-id="5fa9d-2396">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2396">7</span></span>

<span data-ttu-id="5fa9d-2397">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2397">8</span></span>

<span data-ttu-id="5fa9d-2398">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2398">9</span></span>

<span data-ttu-id="5fa9d-2399">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2399">1</span></span><br/> <span data-ttu-id="5fa9d-2400">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2400">0</span></span><br/>

<span data-ttu-id="5fa9d-2401">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2401">1</span></span>

<span data-ttu-id="5fa9d-2402">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2402">2</span></span>

<span data-ttu-id="5fa9d-2403">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2403">3</span></span>

<span data-ttu-id="5fa9d-2404">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2404">4</span></span>

<span data-ttu-id="5fa9d-2405">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2405">5</span></span>

<span data-ttu-id="5fa9d-2406">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2406">6</span></span>

<span data-ttu-id="5fa9d-2407">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2407">7</span></span>

<span data-ttu-id="5fa9d-2408">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2408">8</span></span>

<span data-ttu-id="5fa9d-2409">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2409">9</span></span>

<span data-ttu-id="5fa9d-2410">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2410">2</span></span><br/> <span data-ttu-id="5fa9d-2411">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2411">0</span></span><br/>

<span data-ttu-id="5fa9d-2412">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2412">1</span></span>

<span data-ttu-id="5fa9d-2413">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2413">2</span></span>

<span data-ttu-id="5fa9d-2414">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2414">3</span></span>

<span data-ttu-id="5fa9d-2415">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2415">4</span></span>

<span data-ttu-id="5fa9d-2416">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2416">5</span></span>

<span data-ttu-id="5fa9d-2417">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2417">6</span></span>

<span data-ttu-id="5fa9d-2418">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2418">7</span></span>

<span data-ttu-id="5fa9d-2419">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2419">8</span></span>

<span data-ttu-id="5fa9d-2420">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2420">9</span></span>

<span data-ttu-id="5fa9d-2421">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2421">3</span></span><br/> <span data-ttu-id="5fa9d-2422">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2422">0</span></span><br/>

<span data-ttu-id="5fa9d-2423">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2423">1</span></span>

<span data-ttu-id="5fa9d-2424">втипе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2424">vType</span></span>

<span data-ttu-id="5fa9d-2425">reserved1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2425">reserved1</span></span>

<span data-ttu-id="5fa9d-2426">reserved2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2426">reserved2</span></span>

<span data-ttu-id="5fa9d-2427">Offset (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2427">Offset (optional)</span></span>



 

<span data-ttu-id="5fa9d-2428">**втипе**: признак типа, указывающий тип управляемое vValue.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2428">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="5fa9d-2429">Это должно быть одно из значений VARENUM, указанных в разделе 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2429">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="5fa9d-2430">**reserved1**: не используется.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2430">**reserved1**: Not used.</span></span> <span data-ttu-id="5fa9d-2431">В качестве значения можно задать любое произвольное значение. оно должно игнорироваться при получении.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2431">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="5fa9d-2432">**reserved2**: не используется.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2432">**reserved2**: Not used.</span></span> <span data-ttu-id="5fa9d-2433">В качестве значения можно задать любое произвольное значение. оно должно игнорироваться при получении.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2433">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="5fa9d-2434">**Offset**: смещение данных переменной длины (например, строка).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2434">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="5fa9d-2435">Это должно быть 32-разрядное значение (4 байта), если используется 32-разрядное смещение (согласно правилам в разделе 2.2.3.16), или значение 64-Byte (8 байт), если используется 64-разрядное смещение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2435">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="5fa9d-2436">2.2.1.30 Ксортсет</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2436">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="5fa9d-2437">Структура Ксортсет содержит порядок сортировки запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2437">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="5fa9d-2438">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2438">0</span></span>

<span data-ttu-id="5fa9d-2439">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2439">1</span></span>

<span data-ttu-id="5fa9d-2440">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2440">2</span></span>

<span data-ttu-id="5fa9d-2441">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2441">3</span></span>

<span data-ttu-id="5fa9d-2442">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2442">4</span></span>

<span data-ttu-id="5fa9d-2443">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2443">5</span></span>

<span data-ttu-id="5fa9d-2444">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2444">6</span></span>

<span data-ttu-id="5fa9d-2445">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2445">7</span></span>

<span data-ttu-id="5fa9d-2446">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2446">8</span></span>

<span data-ttu-id="5fa9d-2447">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2447">9</span></span>

<span data-ttu-id="5fa9d-2448">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2448">1</span></span><br/> <span data-ttu-id="5fa9d-2449">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2449">0</span></span><br/>

<span data-ttu-id="5fa9d-2450">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2450">1</span></span>

<span data-ttu-id="5fa9d-2451">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2451">2</span></span>

<span data-ttu-id="5fa9d-2452">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2452">3</span></span>

<span data-ttu-id="5fa9d-2453">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2453">4</span></span>

<span data-ttu-id="5fa9d-2454">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2454">5</span></span>

<span data-ttu-id="5fa9d-2455">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2455">6</span></span>

<span data-ttu-id="5fa9d-2456">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2456">7</span></span>

<span data-ttu-id="5fa9d-2457">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2457">8</span></span>

<span data-ttu-id="5fa9d-2458">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2458">9</span></span>

<span data-ttu-id="5fa9d-2459">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2459">2</span></span><br/> <span data-ttu-id="5fa9d-2460">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2460">0</span></span><br/>

<span data-ttu-id="5fa9d-2461">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2461">1</span></span>

<span data-ttu-id="5fa9d-2462">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2462">2</span></span>

<span data-ttu-id="5fa9d-2463">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2463">3</span></span>

<span data-ttu-id="5fa9d-2464">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2464">4</span></span>

<span data-ttu-id="5fa9d-2465">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2465">5</span></span>

<span data-ttu-id="5fa9d-2466">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2466">6</span></span>

<span data-ttu-id="5fa9d-2467">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2467">7</span></span>

<span data-ttu-id="5fa9d-2468">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2468">8</span></span>

<span data-ttu-id="5fa9d-2469">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2469">9</span></span>

<span data-ttu-id="5fa9d-2470">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2470">3</span></span><br/> <span data-ttu-id="5fa9d-2471">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2471">0</span></span><br/>

<span data-ttu-id="5fa9d-2472">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2472">1</span></span>

<span data-ttu-id="5fa9d-2473">Count</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2473">Count</span></span>

<span data-ttu-id="5fa9d-2474">Сортаррай (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2474">sortArray (variable)</span></span>



 

<span data-ttu-id="5fa9d-2475">**Count**: 32-разрядное целое число без знака, задающее число элементов в сортаррай.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2475">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="5fa9d-2476">**сортаррай**: массив структур ксорт, описывающих порядок сортировки результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2476">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="5fa9d-2477">Структуры в массиве должны быть разделены от 0 до 3 байтов с отступом таким, что каждая структура имеет 4-байтовое выравнивание от начала сообщения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2477">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="5fa9d-2478">Такое заполнение байтов может быть любым произвольным значением и не должно учитываться при получении.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2478">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="5fa9d-2479">2.2.1.31 Ктаблеколумн</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2479">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="5fa9d-2480">Структура Ктаблеколумн содержит столбец сообщения Кпмсетбиндингсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2480">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="5fa9d-2481">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2481">0</span></span>

<span data-ttu-id="5fa9d-2482">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2482">1</span></span>

<span data-ttu-id="5fa9d-2483">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2483">2</span></span>

<span data-ttu-id="5fa9d-2484">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2484">3</span></span>

<span data-ttu-id="5fa9d-2485">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2485">4</span></span>

<span data-ttu-id="5fa9d-2486">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2486">5</span></span>

<span data-ttu-id="5fa9d-2487">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2487">6</span></span>

<span data-ttu-id="5fa9d-2488">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2488">7</span></span>

<span data-ttu-id="5fa9d-2489">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2489">8</span></span>

<span data-ttu-id="5fa9d-2490">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2490">9</span></span>

<span data-ttu-id="5fa9d-2491">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2491">1</span></span><br/> <span data-ttu-id="5fa9d-2492">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2492">0</span></span><br/>

<span data-ttu-id="5fa9d-2493">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2493">1</span></span>

<span data-ttu-id="5fa9d-2494">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2494">2</span></span>

<span data-ttu-id="5fa9d-2495">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2495">3</span></span>

<span data-ttu-id="5fa9d-2496">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2496">4</span></span>

<span data-ttu-id="5fa9d-2497">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2497">5</span></span>

<span data-ttu-id="5fa9d-2498">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2498">6</span></span>

<span data-ttu-id="5fa9d-2499">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2499">7</span></span>

<span data-ttu-id="5fa9d-2500">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2500">8</span></span>

<span data-ttu-id="5fa9d-2501">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2501">9</span></span>

<span data-ttu-id="5fa9d-2502">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2502">2</span></span><br/> <span data-ttu-id="5fa9d-2503">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2503">0</span></span><br/>

<span data-ttu-id="5fa9d-2504">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2504">1</span></span>

<span data-ttu-id="5fa9d-2505">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2505">2</span></span>

<span data-ttu-id="5fa9d-2506">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2506">3</span></span>

<span data-ttu-id="5fa9d-2507">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2507">4</span></span>

<span data-ttu-id="5fa9d-2508">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2508">5</span></span>

<span data-ttu-id="5fa9d-2509">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2509">6</span></span>

<span data-ttu-id="5fa9d-2510">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2510">7</span></span>

<span data-ttu-id="5fa9d-2511">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2511">8</span></span>

<span data-ttu-id="5fa9d-2512">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2512">9</span></span>

<span data-ttu-id="5fa9d-2513">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2513">3</span></span><br/> <span data-ttu-id="5fa9d-2514">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2514">0</span></span><br/>

<span data-ttu-id="5fa9d-2515">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2515">1</span></span>

<span data-ttu-id="5fa9d-2516">пропспек</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2516">PropSpec</span></span>

<span data-ttu-id="5fa9d-2517">... перемен</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2517">...(variable)</span></span>

<span data-ttu-id="5fa9d-2518">втипе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2518">vType</span></span>

<span data-ttu-id="5fa9d-2519">валуеусед</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2519">ValueUsed</span></span>

<span data-ttu-id="5fa9d-2520">\_padding1 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2520">\_padding1 (optional)</span></span>

<span data-ttu-id="5fa9d-2521">Валуеоффсет (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2521">ValueOffset (optional)</span></span>

<span data-ttu-id="5fa9d-2522">Валуесизе (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2522">ValueSize (optional)</span></span>

<span data-ttu-id="5fa9d-2523">статусусед</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2523">StatusUsed</span></span>

<span data-ttu-id="5fa9d-2524">\_padding2 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2524">\_padding2 (optional)</span></span>

<span data-ttu-id="5fa9d-2525">Статусоффсет (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2525">StatusOffset (optional)</span></span>

<span data-ttu-id="5fa9d-2526">ленгсусед</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2526">LengthUsed</span></span>

<span data-ttu-id="5fa9d-2527">\_padding3 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2527">\_padding3 (optional)</span></span>

<span data-ttu-id="5fa9d-2528">Ленгсоффсет (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2528">LengthOffset (optional)</span></span>



 

<span data-ttu-id="5fa9d-2529">**Пропспек**: структура кфуллпропспек, указанная в разделе 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2529">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="5fa9d-2530">**втипе**: указывает тип значения данных, содержащегося в столбце.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2530">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="5fa9d-2531">Список значений для этого поля см. в поле Втипе в разделе 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2531">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="5fa9d-2532">**Валуеусед**: одно поле byte, которое должно иметь значение 0x01 или 0x00.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2532">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="5fa9d-2533">Если задано значение 0x01, столбец передается в пределах строки фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2533">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="5fa9d-2534">Если задано 0x00, значение столбца передается в разделе переменной длины в конце буфера.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2534">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="5fa9d-2535">**\_ padding1**: поле с одним байтом, которое должно быть вставлено перед валуеоффсет, если, без него, валуеоффсет не будет начинаться с четного смещения, начиная с начала сообщения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2535">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="5fa9d-2536">Значение этого байта является произвольным и должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2536">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="5fa9d-2537">Если Валуеусед имеет значение 0x00, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2537">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="5fa9d-2538">**Валуеоффсет**: 2-байтовое целое число без знака, указывающее смещение значения столбца в строке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2538">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="5fa9d-2539">Если Валуеусед имеет значение 0x00, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2539">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="5fa9d-2540">**Валуесизе**: 2-байтовое целое число без знака, указывающее размер значения столбца в байтах.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2540">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="5fa9d-2541">Если Валуеусед имеет значение 0x00, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2541">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="5fa9d-2542">**Статусусед**: одно поле byte, которое должно иметь значение 0x01 или 0x00.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2542">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="5fa9d-2543">Если задано значение 0x01, состояние столбца передается в строке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2543">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="5fa9d-2544">Если 0x00, состояние столбца не передается в строке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2544">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="5fa9d-2545">**\_ padding2**: поле с одним байтом, которое должно быть вставлено перед статусоффсет, если, без него, поле статусоффсет не будет начинаться с четного смещения относительно начала сообщения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2545">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="5fa9d-2546">Значение этого байта является произвольным и должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2546">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="5fa9d-2547">Если Статусусед имеет значение 0x00, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2547">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="5fa9d-2548">**Статусоффсет**: 2-байтовое целое число без знака, указывающее смещение состояния столбца в строке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2548">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="5fa9d-2549">Если Статусусед имеет значение 0x00, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2549">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="5fa9d-2550">**Ленгсусед**: одно поле byte, которое должно иметь значение 0x01 или 0x00.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2550">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="5fa9d-2551">Если задано значение 0x01, длина столбца передается внутри строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2551">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="5fa9d-2552">Если 0x00, длина столбца не должна передаваться внутри строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2552">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="5fa9d-2553">**\_ padding3**: поле с одним байтом, которое должно быть вставлено перед ленгсоффсет, если, без него, ленгсоффсет не будет начинаться с четного смещения, начиная с начала сообщения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2553">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="5fa9d-2554">Значение этого байта является произвольным и должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2554">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="5fa9d-2555">Если Ленгсусед имеет значение 0x00, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2555">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="5fa9d-2556">**Ленгсоффсет**: 2-байтовое целое число без знака, указывающее смещение длины столбца в строке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2556">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="5fa9d-2557">Если Ленгсусед имеет значение 0x00, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2557">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="5fa9d-2558">2.2.1.32 СЕРИАЛИЗЕДПРОПЕРТИВАЛУЕ</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="5fa9d-2559">Структура СЕРИАЛИЗЕДПРОПЕРТИВАЛУЕ содержит сериализованное значение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2559">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="5fa9d-2560">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2560">0</span></span>

<span data-ttu-id="5fa9d-2561">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2561">1</span></span>

<span data-ttu-id="5fa9d-2562">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2562">2</span></span>

<span data-ttu-id="5fa9d-2563">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2563">3</span></span>

<span data-ttu-id="5fa9d-2564">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2564">4</span></span>

<span data-ttu-id="5fa9d-2565">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2565">5</span></span>

<span data-ttu-id="5fa9d-2566">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2566">6</span></span>

<span data-ttu-id="5fa9d-2567">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2567">7</span></span>

<span data-ttu-id="5fa9d-2568">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2568">8</span></span>

<span data-ttu-id="5fa9d-2569">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2569">9</span></span>

<span data-ttu-id="5fa9d-2570">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2570">1</span></span><br/> <span data-ttu-id="5fa9d-2571">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2571">0</span></span><br/>

<span data-ttu-id="5fa9d-2572">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2572">1</span></span>

<span data-ttu-id="5fa9d-2573">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2573">2</span></span>

<span data-ttu-id="5fa9d-2574">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2574">3</span></span>

<span data-ttu-id="5fa9d-2575">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2575">4</span></span>

<span data-ttu-id="5fa9d-2576">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2576">5</span></span>

<span data-ttu-id="5fa9d-2577">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2577">6</span></span>

<span data-ttu-id="5fa9d-2578">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2578">7</span></span>

<span data-ttu-id="5fa9d-2579">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2579">8</span></span>

<span data-ttu-id="5fa9d-2580">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2580">9</span></span>

<span data-ttu-id="5fa9d-2581">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2581">2</span></span><br/> <span data-ttu-id="5fa9d-2582">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2582">0</span></span><br/>

<span data-ttu-id="5fa9d-2583">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2583">1</span></span>

<span data-ttu-id="5fa9d-2584">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2584">2</span></span>

<span data-ttu-id="5fa9d-2585">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2585">3</span></span>

<span data-ttu-id="5fa9d-2586">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2586">4</span></span>

<span data-ttu-id="5fa9d-2587">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2587">5</span></span>

<span data-ttu-id="5fa9d-2588">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2588">6</span></span>

<span data-ttu-id="5fa9d-2589">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2589">7</span></span>

<span data-ttu-id="5fa9d-2590">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2590">8</span></span>

<span data-ttu-id="5fa9d-2591">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2591">9</span></span>

<span data-ttu-id="5fa9d-2592">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2592">3</span></span><br/> <span data-ttu-id="5fa9d-2593">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2593">0</span></span><br/>

<span data-ttu-id="5fa9d-2594">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2594">1</span></span>

<span data-ttu-id="5fa9d-2595">двтипе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2595">dwType</span></span>

<span data-ttu-id="5fa9d-2596">RGB (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2596">rgb (variable)</span></span>



 

<span data-ttu-id="5fa9d-2597">**двтипе**: один из типов Variant, определенный в разделе 2.2.1.1, который можно сочетать с модификаторами типа Variant.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2597">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="5fa9d-2598">Для всех типов Variant, за исключением тех, которые объединены с \_ массивом VT, сериализедпропертивалуе имеет тот же макет, что и кбасесторажевариант, как указано в разделе 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2598">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="5fa9d-2599">Если тип Variant сочетается с \_ модификатором типа массива VT, то в поле Кбасесторажевариант управляемое vValue вместо SAFEARRAY используется SAFEARRAY2, заданный в разделе 2.2.1.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2599">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="5fa9d-2600">**RGB**: сериализованное значение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2600">**rgb**: Serialized value.</span></span> <span data-ttu-id="5fa9d-2601">См. подробные сведения о сериализации для управляемое vValue в 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2601">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="5fa9d-2602">Заголовки сообщений 2.2.2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2602">2.2.2 Message Headers</span></span>

<span data-ttu-id="5fa9d-2603">Все сообщения протокола службы индексирования содержимого содержат 16-байтовый заголовок.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2603">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="5fa9d-2604">Ниже приведена схема, показывающая формат заголовка сообщения протокола службы индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2604">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="5fa9d-2605">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2605">0</span></span>

<span data-ttu-id="5fa9d-2606">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2606">1</span></span>

<span data-ttu-id="5fa9d-2607">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2607">2</span></span>

<span data-ttu-id="5fa9d-2608">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2608">3</span></span>

<span data-ttu-id="5fa9d-2609">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2609">4</span></span>

<span data-ttu-id="5fa9d-2610">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2610">5</span></span>

<span data-ttu-id="5fa9d-2611">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2611">6</span></span>

<span data-ttu-id="5fa9d-2612">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2612">7</span></span>

<span data-ttu-id="5fa9d-2613">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2613">8</span></span>

<span data-ttu-id="5fa9d-2614">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2614">9</span></span>

<span data-ttu-id="5fa9d-2615">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2615">1</span></span><br/> <span data-ttu-id="5fa9d-2616">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2616">0</span></span><br/>

<span data-ttu-id="5fa9d-2617">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2617">1</span></span>

<span data-ttu-id="5fa9d-2618">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2618">2</span></span>

<span data-ttu-id="5fa9d-2619">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2619">3</span></span>

<span data-ttu-id="5fa9d-2620">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2620">4</span></span>

<span data-ttu-id="5fa9d-2621">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2621">5</span></span>

<span data-ttu-id="5fa9d-2622">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2622">6</span></span>

<span data-ttu-id="5fa9d-2623">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2623">7</span></span>

<span data-ttu-id="5fa9d-2624">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2624">8</span></span>

<span data-ttu-id="5fa9d-2625">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2625">9</span></span>

<span data-ttu-id="5fa9d-2626">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2626">2</span></span><br/> <span data-ttu-id="5fa9d-2627">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2627">0</span></span><br/>

<span data-ttu-id="5fa9d-2628">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2628">1</span></span>

<span data-ttu-id="5fa9d-2629">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2629">2</span></span>

<span data-ttu-id="5fa9d-2630">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2630">3</span></span>

<span data-ttu-id="5fa9d-2631">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2631">4</span></span>

<span data-ttu-id="5fa9d-2632">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2632">5</span></span>

<span data-ttu-id="5fa9d-2633">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2633">6</span></span>

<span data-ttu-id="5fa9d-2634">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2634">7</span></span>

<span data-ttu-id="5fa9d-2635">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2635">8</span></span>

<span data-ttu-id="5fa9d-2636">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2636">9</span></span>

<span data-ttu-id="5fa9d-2637">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2637">3</span></span><br/> <span data-ttu-id="5fa9d-2638">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2638">0</span></span><br/>

<span data-ttu-id="5fa9d-2639">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2639">1</span></span>

<span data-ttu-id="5fa9d-2640">\_об</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2640">\_msg</span></span>

<span data-ttu-id="5fa9d-2641">\_состояние</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2641">\_status</span></span>

<span data-ttu-id="5fa9d-2642">\_улчекксум</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2642">\_ulChecksum</span></span>

<span data-ttu-id="5fa9d-2643">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2643">\_ulReserved2</span></span>



 

<span data-ttu-id="5fa9d-2644">\_**MSG**: 32-разрядное целое число, определяющее тип сообщения, следующего за заголовком.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2644">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="5fa9d-2645">В следующей таблице перечислены сообщения протокола службы индексирования содержимого и целые значения, указанные для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2645">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="5fa9d-2646">Как показано в таблице, некоторые значения указывают 2 сообщения в таблице.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2646">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="5fa9d-2647">В этих экземплярах сообщение, следующее за заголовком, можно определить по направлению потока сообщений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2647">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="5fa9d-2648">Если направлением является клиент-сервер, отображается сообщение с добавлением к имени сообщения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2648">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="5fa9d-2649">Если направлением является серверный клиент, то отображается сообщение с добавлением к имени сообщения "out".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2649">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="5fa9d-2650">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2650">Value</span></span>      | <span data-ttu-id="5fa9d-2651">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2651">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="5fa9d-2652">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2652">0x000000C8</span></span> | <span data-ttu-id="5fa9d-2653">Кпмконнектин или Кпмконнектаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2653">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="5fa9d-2654">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2654">0x000000C9</span></span> | <span data-ttu-id="5fa9d-2655">кпмдисконнект</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2655">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="5fa9d-2656">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2656">0x000000CA</span></span> | <span data-ttu-id="5fa9d-2657">Кпмкреатекуерин или Кпмкреатекуерйоут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2657">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="5fa9d-2658">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2658">0x000000CB</span></span> | <span data-ttu-id="5fa9d-2659">Кпмфрикурсорин или Кпмфрикурсораут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2659">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="5fa9d-2660">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2660">0x000000CC</span></span> | <span data-ttu-id="5fa9d-2661">Кпмжетровсин или Кпмжетровсаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2661">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="5fa9d-2662">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2662">0x000000CD</span></span> | <span data-ttu-id="5fa9d-2663">Кпмратиофинишедин или Кпмратиофинишедаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2663">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="5fa9d-2664">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2664">0x000000CE</span></span> | <span data-ttu-id="5fa9d-2665">Кпмкомпаребмкин или Кпмкомпаребмкаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2665">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="5fa9d-2666">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2666">0x000000CF</span></span> | <span data-ttu-id="5fa9d-2667">Кпмжетаппроксиматепоситионин или Кпмжетаппроксиматепоситионаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2667">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="5fa9d-2668">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2668">0x000000D0</span></span> | <span data-ttu-id="5fa9d-2669">кпмсетбиндингсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2669">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="5fa9d-2670">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2670">0x000000D1</span></span> | <span data-ttu-id="5fa9d-2671">кпмжетнотифи</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2671">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="5fa9d-2672">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2672">0x000000D2</span></span> | <span data-ttu-id="5fa9d-2673">кпмсенднотифйоут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2673">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="5fa9d-2674">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2674">0x000000D7</span></span> | <span data-ttu-id="5fa9d-2675">Кпмжеткуеристатусин или Кпмжеткуеристатусаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2675">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="5fa9d-2676">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2676">0x000000D9</span></span> | <span data-ttu-id="5fa9d-2677">кпмЦистатеинаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2677">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="5fa9d-2678">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2678">0x000000E1</span></span> | <span data-ttu-id="5fa9d-2679">кпмфорцемержеин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2679">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="5fa9d-2680">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2680">0x000000E4</span></span> | <span data-ttu-id="5fa9d-2681">Кпмфетчвалуеин или Кпмфетчвалуеаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2681">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="5fa9d-2682">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2682">0x000000E6</span></span> | <span data-ttu-id="5fa9d-2683">кпмупдатедокументсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2683">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="5fa9d-2684">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2684">0x000000E7</span></span> | <span data-ttu-id="5fa9d-2685">Кпмжеткуеристатусексин или Пмжеткуеристатусексаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2685">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="5fa9d-2686">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2686">0x000000E8</span></span> | <span data-ttu-id="5fa9d-2687">кпмрестартпоситионин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2687">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="5fa9d-2688">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2688">0x000000E9</span></span> | <span data-ttu-id="5fa9d-2689">кпмстопасинчин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2689">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="5fa9d-2690">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2690">0x000000EC</span></span> | <span data-ttu-id="5fa9d-2691">Кпмсеткатстатеин или Кпмсеткатстатеаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2691">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="5fa9d-2692">\_**состояние**: HRESULT \[ MS-sys \] , указывающий состояние запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2692">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="5fa9d-2693">*Поведение Windows. Клиент всегда задает \_ для поля состояния значение 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2693">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="5fa9d-2694">**\_ УЛЧЕККСУМ**: \_ необходимо вычислить улчекксум, как указано в разделе 3.2.4 для следующих сообщений:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2694">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="5fa9d-2695">кпмконнектин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2695">CPMConnectIn</span></span>
-   <span data-ttu-id="5fa9d-2696">кпмкреатекуерин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2696">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="5fa9d-2697">кпмсетбиндингсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2697">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="5fa9d-2698">кпмжетровсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2698">CPMGetRowsIn</span></span>
-   <span data-ttu-id="5fa9d-2699">кпмфетчвалуеин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2699">CPMFetchValueIn</span></span>

<span data-ttu-id="5fa9d-2700">Для всех остальных сообщений \_ параметру УЛЧЕККСУМ должно быть присвоено значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2700">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="5fa9d-2701">Клиент должен игнорировать \_ поле улчекксум.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2701">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="5fa9d-2702">**\_ ulReserved2**: значение должно быть равно 0 и игнорируется получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2702">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="5fa9d-2703">сообщения 2.2.3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2703">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="5fa9d-2704">2.2.3.1 КпмЦистатеинаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2704">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="5fa9d-2705">Сообщение КпмЦистатеинаут содержит сведения о состоянии службы индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2705">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="5fa9d-2706">Формат сообщения КпмЦистатеинаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2706">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-2707">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2707">0</span></span>

<span data-ttu-id="5fa9d-2708">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2708">1</span></span>

<span data-ttu-id="5fa9d-2709">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2709">2</span></span>

<span data-ttu-id="5fa9d-2710">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2710">3</span></span>

<span data-ttu-id="5fa9d-2711">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2711">4</span></span>

<span data-ttu-id="5fa9d-2712">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2712">5</span></span>

<span data-ttu-id="5fa9d-2713">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2713">6</span></span>

<span data-ttu-id="5fa9d-2714">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2714">7</span></span>

<span data-ttu-id="5fa9d-2715">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2715">8</span></span>

<span data-ttu-id="5fa9d-2716">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2716">9</span></span>

<span data-ttu-id="5fa9d-2717">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2717">1</span></span><br/> <span data-ttu-id="5fa9d-2718">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2718">0</span></span><br/>

<span data-ttu-id="5fa9d-2719">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2719">1</span></span>

<span data-ttu-id="5fa9d-2720">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2720">2</span></span>

<span data-ttu-id="5fa9d-2721">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2721">3</span></span>

<span data-ttu-id="5fa9d-2722">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2722">4</span></span>

<span data-ttu-id="5fa9d-2723">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2723">5</span></span>

<span data-ttu-id="5fa9d-2724">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2724">6</span></span>

<span data-ttu-id="5fa9d-2725">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2725">7</span></span>

<span data-ttu-id="5fa9d-2726">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2726">8</span></span>

<span data-ttu-id="5fa9d-2727">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2727">9</span></span>

<span data-ttu-id="5fa9d-2728">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2728">2</span></span><br/> <span data-ttu-id="5fa9d-2729">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2729">0</span></span><br/>

<span data-ttu-id="5fa9d-2730">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2730">1</span></span>

<span data-ttu-id="5fa9d-2731">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2731">2</span></span>

<span data-ttu-id="5fa9d-2732">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2732">3</span></span>

<span data-ttu-id="5fa9d-2733">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2733">4</span></span>

<span data-ttu-id="5fa9d-2734">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2734">5</span></span>

<span data-ttu-id="5fa9d-2735">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2735">6</span></span>

<span data-ttu-id="5fa9d-2736">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2736">7</span></span>

<span data-ttu-id="5fa9d-2737">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2737">8</span></span>

<span data-ttu-id="5fa9d-2738">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2738">9</span></span>

<span data-ttu-id="5fa9d-2739">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2739">3</span></span><br/> <span data-ttu-id="5fa9d-2740">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2740">0</span></span><br/>

<span data-ttu-id="5fa9d-2741">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2741">1</span></span>

<span data-ttu-id="5fa9d-2742">кбструкт</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2742">cbStruct</span></span>

<span data-ttu-id="5fa9d-2743">квордлист</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2743">cWordList</span></span>

<span data-ttu-id="5fa9d-2744">кперсистентиндекс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2744">cPersistentIndex</span></span>

<span data-ttu-id="5fa9d-2745">ккуериес</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2745">cQueries</span></span>

<span data-ttu-id="5fa9d-2746">cDocument</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2746">cDocuments</span></span>

<span data-ttu-id="5fa9d-2747">кфрештест</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2747">cFreshTest</span></span>

<span data-ttu-id="5fa9d-2748">двмержепрогресс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2748">dwMergeProgress</span></span>

<span data-ttu-id="5fa9d-2749">Пространство</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2749">eState</span></span>

<span data-ttu-id="5fa9d-2750">кфилтереддокументс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2750">cFilteredDocuments</span></span>

<span data-ttu-id="5fa9d-2751">ктоталдокументс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2751">cTotalDocuments</span></span>

<span data-ttu-id="5fa9d-2752">кпендингсканс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2752">cPendingScans</span></span>

<span data-ttu-id="5fa9d-2753">двиндекссизе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2753">dwIndexSize</span></span>

<span data-ttu-id="5fa9d-2754">куникуекэйс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2754">cUniqueKeys</span></span>

<span data-ttu-id="5fa9d-2755">ксеккдокументс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2755">cSecQDocuments</span></span>

<span data-ttu-id="5fa9d-2756">двпропкачесизе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2756">dwPropCacheSize</span></span>



 

<span data-ttu-id="5fa9d-2757">**кбструкт**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2757">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="5fa9d-2758">Размер (в байтах) этого сообщения (за исключением общего заголовка).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2758">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="5fa9d-2759">НЕОБХОДИМО задать значение 0x0000003C.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2759">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="5fa9d-2760">**квордлист**: 32-разрядное целое число без знака, указывающее количество начальных индексов, созданных для недавно индексированных документов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2760">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="5fa9d-2761">**кперсистентиндекс**: 32-битовое целое число без знака, указывающее количество постоянных индексов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2761">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="5fa9d-2762">**ккуериес**: 32-битовое целое число без знака, указывающее количество активных запросов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2762">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="5fa9d-2763">**CDocument**: 32-разрядное целое число без знака, указывающее общее количество документов, ожидающих индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2763">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="5fa9d-2764">**кфрештест**: 32-разрядное целое число без знака, указывающее количество уникальных документов со сведениями в индексах, которые не были полностью оптимизированы для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2764">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="5fa9d-2765">**двмержепрогресс**: беззнаковое 32-разрядное целое число, определяющее процент завершения текущей полной оптимизации индексов, если в данный момент выполняется оптимизация.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2765">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="5fa9d-2766">ДОЛЖНО быть меньше или равно 100.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2766">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="5fa9d-2767">**пространство**: состояние индексирования содержимого, заданное одной или несколькими \_ константами состояния CI \_ \* , определенными в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2767">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="5fa9d-2768">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2768">Value</span></span>                                         | <span data-ttu-id="5fa9d-2769">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2769">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-2770">\_ \_ Теневое \_ Слияние состояния CI 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2770">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="5fa9d-2771">Служба индексирования находится в процессе оптимизации некоторых индексов, чтобы сократить использование памяти и повысить производительность запросов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2771">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="5fa9d-2772">\_ \_ Слияние хозяина состояния CI — \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2772">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="5fa9d-2773">Служба индексирования находится в процессе полной оптимизации для всех индексов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2773">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5fa9d-2774">\_ \_ Требуется сканирование содержимого состояния CI, \_ \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2774">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="5fa9d-2775">Некоторые документы в индексе были изменены, и службе индексирования необходимо определить, какие из них были добавлены, изменены или удалены.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2775">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5fa9d-2776">\_Состояние CI \_ отжига \_ Merge 0x00000008</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2776">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="5fa9d-2777">Служба индексирования находится в процессе оптимизации индексов, чтобы сократить использование памяти и повысить производительность запросов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2777">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="5fa9d-2778">Этот процесс является более полным, чем тот, который определяется \_ \_ значением теневого копирования состояния CI \_ , но не так, как указано в \_ \_ значении объединения с образцом состояния CI \_ .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2778">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="5fa9d-2779">Такая оптимизация зависит от конкретной реализации, так как они зависят от способа внутреннего хранения данных. оптимизация не влияет на протокол никаким способом, отличным от времени отклика.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2779">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="5fa9d-2780">\_Просмотр состояния CI \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2780">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="5fa9d-2781">Служба индексирования проверяет каталог или набор каталогов, чтобы определить, были ли файлы добавлены, удалены или обновлены со времени последнего индексирования каталога.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2781">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="5fa9d-2782">\_Восстановление состояния CI — \_ 0x00000020</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2782">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="5fa9d-2783">Служба запускается из последнего сохраненного состояния и находится в процессе восстановления.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2783">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="5fa9d-2784">\_ \_ 0x00000080 нехватка \_ памяти CI State</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2784">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="5fa9d-2785">Большая часть виртуальной памяти сервера используется.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2785">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="5fa9d-2786">\_ \_ Высокий уровень операций ввода-вывода в состоянии CI \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2786">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="5fa9d-2787">Уровень активности ввода-вывода на сервере относительно высокий.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2787">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="5fa9d-2788">\_ \_ Сводное \_ Слияние состояния CI \_ 0x00000200 приостановлено</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2788">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="5fa9d-2789">Процесс полной оптимизации для всех выполняемых индексов был приостановлен.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2789">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="5fa9d-2790">Он предоставляется исключительно в информативных целях и не влияет на CISP.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5fa9d-2791">\_Состояние CI \_ только для чтения \_ 0x00000400</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2791">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="5fa9d-2792">Часть службы индексирования, которая выбирает новые документы для индексирования, приостановлена.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2792">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="5fa9d-2793">Он предоставляется исключительно в информативных целях и не влияет на CISP.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="5fa9d-2794">Состояние элемента конфигурации \_ \_ батарея \_ Power 0x00000800</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2794">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="5fa9d-2795">Часть службы индексирования, которая выбирает новые документы для индексирования, приостановлена для сохранения времени существования аккумулятора, но по-прежнему отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2795">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="5fa9d-2796">Он предоставляется исключительно в информативных целях и не влияет на CISP.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="5fa9d-2797">\_Состояние CI \_ пользователь \_ Active 0x00001000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2797">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="5fa9d-2798">Часть службы индексирования, которая выбирает новые документы для индексирования, приостановлена из-за высокой активности пользователя (клавиатуры или мыши), но по-прежнему отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2798">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="5fa9d-2799">Он предоставляется исключительно в информативных целях и не влияет на CISP.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2799">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="5fa9d-2800">Состояние CI, \_ \_ начиная с 0x00002000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2800">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="5fa9d-2801">Служба запускается.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2801">The service is starting.</span></span> <span data-ttu-id="5fa9d-2802">Запросы можно запускать, но сканирование и уведомление еще не включены.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2802">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="5fa9d-2803">Он предоставляется исключительно в информативных целях и не влияет на CISP.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2803">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="5fa9d-2804">\_ \_ Считывание состояния CI \_ USN 0x00004000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2804">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="5fa9d-2805">Служба не прочитала журнал, который хранится в файловой системе, чтобы отследить изменения в файлах или каталогах на томе, поэтому индекс может оказаться неактуальным.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2805">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="5fa9d-2806">**кфилтереддокументс**: 32-разрядное целое число без знака, указывающее количество документов, индексированных с момента начала индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2806">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="5fa9d-2807">**ктоталдокументс**: 32-битовое целое число без знака, указывающее общее количество документов в системе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2807">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="5fa9d-2808">**кпендингсканс**: 32-битовое целое число без знака, указывающее количество ожидающих операций индексирования высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2808">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="5fa9d-2809">Значение этого параметра зависит от поставщика, но более крупные числа должны указывать на большее количество индексов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2809">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="5fa9d-2810">*Поведение Windows*. обычно это значение равно нулю, за исключением случаев, когда было начато индексирование или после того, как очередь уведомлений переполняется.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2810">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="5fa9d-2811">**двиндекссизе**: 32-разрядное целое число без знака, указывающее размер индекса (за исключением кэша свойств) в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2811">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="5fa9d-2812">**куникуекэйс**: 32-битовое целое число без знака, указывающее приблизительное количество уникальных ключей в каталоге.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2812">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="5fa9d-2813">**ксеккдокументс**: 32-разрядное целое число без знака, указывающее количество документов, которые служба индексирования будет повторно пытаться индексировать из-за сбоя во время первоначальной попытки индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2813">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="5fa9d-2814">**двпропкачесизе**: 32-разрядное целое число без знака, указывающее размер кэша свойств в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2814">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="5fa9d-2815">2.2.3.2 Кпмсеткатстатеин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2815">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="5fa9d-2816">Сообщение Кпмсеткатстатеин задает состояние каталога.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2816">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="5fa9d-2817">Формат сообщения Кпмсеткатстатеин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2817">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-2818">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2818">0</span></span>

<span data-ttu-id="5fa9d-2819">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2819">1</span></span>

<span data-ttu-id="5fa9d-2820">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2820">2</span></span>

<span data-ttu-id="5fa9d-2821">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2821">3</span></span>

<span data-ttu-id="5fa9d-2822">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2822">4</span></span>

<span data-ttu-id="5fa9d-2823">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2823">5</span></span>

<span data-ttu-id="5fa9d-2824">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2824">6</span></span>

<span data-ttu-id="5fa9d-2825">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2825">7</span></span>

<span data-ttu-id="5fa9d-2826">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2826">8</span></span>

<span data-ttu-id="5fa9d-2827">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2827">9</span></span>

<span data-ttu-id="5fa9d-2828">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2828">1</span></span><br/> <span data-ttu-id="5fa9d-2829">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2829">0</span></span><br/>

<span data-ttu-id="5fa9d-2830">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2830">1</span></span>

<span data-ttu-id="5fa9d-2831">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2831">2</span></span>

<span data-ttu-id="5fa9d-2832">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2832">3</span></span>

<span data-ttu-id="5fa9d-2833">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2833">4</span></span>

<span data-ttu-id="5fa9d-2834">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2834">5</span></span>

<span data-ttu-id="5fa9d-2835">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2835">6</span></span>

<span data-ttu-id="5fa9d-2836">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2836">7</span></span>

<span data-ttu-id="5fa9d-2837">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2837">8</span></span>

<span data-ttu-id="5fa9d-2838">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2838">9</span></span>

<span data-ttu-id="5fa9d-2839">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2839">2</span></span><br/> <span data-ttu-id="5fa9d-2840">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2840">0</span></span><br/>

<span data-ttu-id="5fa9d-2841">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2841">1</span></span>

<span data-ttu-id="5fa9d-2842">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2842">2</span></span>

<span data-ttu-id="5fa9d-2843">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2843">3</span></span>

<span data-ttu-id="5fa9d-2844">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2844">4</span></span>

<span data-ttu-id="5fa9d-2845">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2845">5</span></span>

<span data-ttu-id="5fa9d-2846">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2846">6</span></span>

<span data-ttu-id="5fa9d-2847">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2847">7</span></span>

<span data-ttu-id="5fa9d-2848">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2848">8</span></span>

<span data-ttu-id="5fa9d-2849">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2849">9</span></span>

<span data-ttu-id="5fa9d-2850">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2850">3</span></span><br/> <span data-ttu-id="5fa9d-2851">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2851">0</span></span><br/>

<span data-ttu-id="5fa9d-2852">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2852">1</span></span>

<span data-ttu-id="5fa9d-2853">\_partID</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2853">\_partID</span></span>

<span data-ttu-id="5fa9d-2854">\_двневстате</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2854">\_dwNewState</span></span>

<span data-ttu-id="5fa9d-2855">\_Катнаме (переменная, необязательный)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2855">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="5fa9d-2856">**\_ PARTID**: необходимо задать значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2856">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="5fa9d-2857">**\_ двневстате**: необходимо задать одно из следующих значений, указывающее новое состояние каталога.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2857">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="5fa9d-2858">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2858">Value</span></span>                         | <span data-ttu-id="5fa9d-2859">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2859">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-2860">ЦИКАТ \_ остановлено 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2860">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="5fa9d-2861">Каталог остановлен.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2861">The catalog is stopped.</span></span> <span data-ttu-id="5fa9d-2862">Это состояние означает, что новые файлы индексироваться не будут, а поисковые запросы обрабатываться не будут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2862">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="5fa9d-2863">ЦИКАТ \_ ReadOnly 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2863">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="5fa9d-2864">Каталог доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2864">The catalog is read-only.</span></span> <span data-ttu-id="5fa9d-2865">Нет новых файлов для индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2865">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="5fa9d-2866">ЦИКАТ, \_ доступный для записи, 0x00000004</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2866">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="5fa9d-2867">Каталог доступен для записи.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2867">The catalog is writable.</span></span> <span data-ttu-id="5fa9d-2868">Новые файлы можно индексировать, а запросы поиска — обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2868">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="5fa9d-2869">ЦИКАТ \_ без \_ запроса 0x00000008</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2869">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="5fa9d-2870">Каталог недоступен для запросов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2870">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="5fa9d-2871">ЦИКАТ \_ получить \_ состояние 0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2871">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="5fa9d-2872">Состояние каталога не должно изменяться, извлекается только.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2872">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="5fa9d-2873">ЦИКАТ \_ все \_ открытые 0x00000020</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2873">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="5fa9d-2874">Проверка того, были ли запущены все каталоги.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2874">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="5fa9d-2875">Если да, то в \_ поле дволдстате, отправленном в ответе кпмсеткатстатеаут на это сообщение, будет получено ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2875">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="5fa9d-2876">**\_ Катнаме**: имя каталога, для которого необходимо изменить состояние.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2876">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="5fa9d-2877">Имя должно быть строкой в Юникоде, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2877">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="5fa9d-2878">Это поле необходимо опустить, если \_ двневстате имеет значение Цикат \_ All \_ Opened.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2878">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="5fa9d-2879">2.2.3.3 Кпмсеткатстатеаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2879">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="5fa9d-2880">Сообщение Кпмсеткатстатеаут — это ответ на сообщение Кпмсеткатстатеин со старым состоянием каталога.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2880">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="5fa9d-2881">Формат сообщения Кпмсеткатстатеаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2881">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-2882">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2882">0</span></span>

<span data-ttu-id="5fa9d-2883">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2883">1</span></span>

<span data-ttu-id="5fa9d-2884">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2884">2</span></span>

<span data-ttu-id="5fa9d-2885">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2885">3</span></span>

<span data-ttu-id="5fa9d-2886">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2886">4</span></span>

<span data-ttu-id="5fa9d-2887">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2887">5</span></span>

<span data-ttu-id="5fa9d-2888">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2888">6</span></span>

<span data-ttu-id="5fa9d-2889">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2889">7</span></span>

<span data-ttu-id="5fa9d-2890">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2890">8</span></span>

<span data-ttu-id="5fa9d-2891">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2891">9</span></span>

<span data-ttu-id="5fa9d-2892">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2892">1</span></span><br/> <span data-ttu-id="5fa9d-2893">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2893">0</span></span><br/>

<span data-ttu-id="5fa9d-2894">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2894">1</span></span>

<span data-ttu-id="5fa9d-2895">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2895">2</span></span>

<span data-ttu-id="5fa9d-2896">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2896">3</span></span>

<span data-ttu-id="5fa9d-2897">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2897">4</span></span>

<span data-ttu-id="5fa9d-2898">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2898">5</span></span>

<span data-ttu-id="5fa9d-2899">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2899">6</span></span>

<span data-ttu-id="5fa9d-2900">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2900">7</span></span>

<span data-ttu-id="5fa9d-2901">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2901">8</span></span>

<span data-ttu-id="5fa9d-2902">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2902">9</span></span>

<span data-ttu-id="5fa9d-2903">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2903">2</span></span><br/> <span data-ttu-id="5fa9d-2904">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2904">0</span></span><br/>

<span data-ttu-id="5fa9d-2905">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2905">1</span></span>

<span data-ttu-id="5fa9d-2906">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2906">2</span></span>

<span data-ttu-id="5fa9d-2907">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2907">3</span></span>

<span data-ttu-id="5fa9d-2908">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2908">4</span></span>

<span data-ttu-id="5fa9d-2909">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2909">5</span></span>

<span data-ttu-id="5fa9d-2910">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2910">6</span></span>

<span data-ttu-id="5fa9d-2911">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2911">7</span></span>

<span data-ttu-id="5fa9d-2912">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2912">8</span></span>

<span data-ttu-id="5fa9d-2913">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2913">9</span></span>

<span data-ttu-id="5fa9d-2914">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2914">3</span></span><br/> <span data-ttu-id="5fa9d-2915">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2915">0</span></span><br/>

<span data-ttu-id="5fa9d-2916">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2916">1</span></span>

<span data-ttu-id="5fa9d-2917">\_дволдстате</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2917">\_dwOldState</span></span>



 

<span data-ttu-id="5fa9d-2918">**\_ дволдстате**: одно из следующих значений, указывающее старое состояние каталога.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2918">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="5fa9d-2919">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2919">Value</span></span>                       | <span data-ttu-id="5fa9d-2920">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2920">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="5fa9d-2921">ЦИКАТ \_ остановлено 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2921">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="5fa9d-2922">Каталог остановлен.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2922">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="5fa9d-2923">ЦИКАТ \_ ReadOnly 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2923">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="5fa9d-2924">Каталог доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2924">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="5fa9d-2925">ЦИКАТ, \_ доступный для записи, 0x00000004</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2925">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="5fa9d-2926">Каталог доступен для записи.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2926">The catalog is writable.</span></span>                   |
| <span data-ttu-id="5fa9d-2927">ЦИКАТ \_ без \_ запроса 0x00000008</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2927">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="5fa9d-2928">Каталог недоступен для запросов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2928">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="5fa9d-2929">2.2.3.4 Кпмупдатедокументсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2929">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="5fa9d-2930">Сообщение Кпмупдатедокументсин направляет сервер для индексирования указанного пути.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2930">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="5fa9d-2931">Сервер будет отвечать с заголовком сообщения Кпмупдатедокументсаут, в котором результаты запроса содержатся в \_ поле Status заголовка сообщения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2931">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="5fa9d-2932">Формат сообщения Кпмупдатедокументсин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2932">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-2933">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2933">0</span></span>

<span data-ttu-id="5fa9d-2934">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2934">1</span></span>

<span data-ttu-id="5fa9d-2935">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2935">2</span></span>

<span data-ttu-id="5fa9d-2936">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2936">3</span></span>

<span data-ttu-id="5fa9d-2937">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2937">4</span></span>

<span data-ttu-id="5fa9d-2938">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2938">5</span></span>

<span data-ttu-id="5fa9d-2939">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2939">6</span></span>

<span data-ttu-id="5fa9d-2940">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2940">7</span></span>

<span data-ttu-id="5fa9d-2941">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2941">8</span></span>

<span data-ttu-id="5fa9d-2942">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2942">9</span></span>

<span data-ttu-id="5fa9d-2943">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2943">1</span></span><br/> <span data-ttu-id="5fa9d-2944">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2944">0</span></span><br/>

<span data-ttu-id="5fa9d-2945">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2945">1</span></span>

<span data-ttu-id="5fa9d-2946">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2946">2</span></span>

<span data-ttu-id="5fa9d-2947">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2947">3</span></span>

<span data-ttu-id="5fa9d-2948">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2948">4</span></span>

<span data-ttu-id="5fa9d-2949">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2949">5</span></span>

<span data-ttu-id="5fa9d-2950">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2950">6</span></span>

<span data-ttu-id="5fa9d-2951">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2951">7</span></span>

<span data-ttu-id="5fa9d-2952">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2952">8</span></span>

<span data-ttu-id="5fa9d-2953">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2953">9</span></span>

<span data-ttu-id="5fa9d-2954">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2954">2</span></span><br/> <span data-ttu-id="5fa9d-2955">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2955">0</span></span><br/>

<span data-ttu-id="5fa9d-2956">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2956">1</span></span>

<span data-ttu-id="5fa9d-2957">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2957">2</span></span>

<span data-ttu-id="5fa9d-2958">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2958">3</span></span>

<span data-ttu-id="5fa9d-2959">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2959">4</span></span>

<span data-ttu-id="5fa9d-2960">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2960">5</span></span>

<span data-ttu-id="5fa9d-2961">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2961">6</span></span>

<span data-ttu-id="5fa9d-2962">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2962">7</span></span>

<span data-ttu-id="5fa9d-2963">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2963">8</span></span>

<span data-ttu-id="5fa9d-2964">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2964">9</span></span>

<span data-ttu-id="5fa9d-2965">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2965">3</span></span><br/> <span data-ttu-id="5fa9d-2966">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2966">0</span></span><br/>

<span data-ttu-id="5fa9d-2967">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2967">1</span></span>

<span data-ttu-id="5fa9d-2968">\_флаг (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2968">\_flag (optional)</span></span>

<span data-ttu-id="5fa9d-2969">\_Фрутпас (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2969">\_fRootPath (optional)</span></span>

<span data-ttu-id="5fa9d-2970">RootPath (переменная, необязательный)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2970">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="5fa9d-2971">**\_ флаг**: тип обновления, которое необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2971">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="5fa9d-2972">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2972">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="5fa9d-2973">В этом поле должно быть указано одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2973">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="5fa9d-2974">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2974">Value</span></span>                  | <span data-ttu-id="5fa9d-2975">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2975">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5fa9d-2976">UPD \_ инкрем 0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2976">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="5fa9d-2977">Необходимо выполнить добавочное обновление.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2977">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="5fa9d-2978">\_Полный UPD 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2978">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="5fa9d-2979">Необходимо выполнить полное обновление.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2979">A full update is to be performed.</span></span>         |
| <span data-ttu-id="5fa9d-2980">UPD \_ init 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2980">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="5fa9d-2981">Будет выполнена новая инициализация.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2981">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="5fa9d-2982">**\_ фрутпас**: логическое значение, указывающее, указывает ли поле rootpath путь для выполнения обновления.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2982">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="5fa9d-2983">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2983">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="5fa9d-2984">Для этого поля необходимо задать значение 0x00000001 или 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2984">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="5fa9d-2985">Если задано значение 0x00000001, то путь, по которому выполняется обновление, включается в RootPath.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2985">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="5fa9d-2986">Если задано значение 0x00000000, то обновление будет выполнено для всех индексированных путей.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2986">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="5fa9d-2987">**Rootpath**: имя обновляемого пути.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2987">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="5fa9d-2988">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2988">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="5fa9d-2989">Имя должно быть строкой в Юникоде, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2989">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="5fa9d-2990">Это поле необходимо опустить, если \_ для фрутпас задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2990">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="5fa9d-2991">2.2.3.5 Кпмфорцемержеин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2991">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="5fa9d-2992">Сообщение Кпмфорцемержеин запрашивает сервер для выполнения любого обслуживания, необходимого для повышения производительности запросов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2992">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="5fa9d-2993">Сервер будет отвечать с заголовком сообщения Кпмфорцемержеин, а результаты запроса содержатся в \_ поле Status (состояние).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2993">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="5fa9d-2994">Формат сообщения Кпмфорцемержеин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2994">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-2995">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2995">0</span></span>

<span data-ttu-id="5fa9d-2996">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2996">1</span></span>

<span data-ttu-id="5fa9d-2997">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2997">2</span></span>

<span data-ttu-id="5fa9d-2998">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2998">3</span></span>

<span data-ttu-id="5fa9d-2999">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-2999">4</span></span>

<span data-ttu-id="5fa9d-3000">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3000">5</span></span>

<span data-ttu-id="5fa9d-3001">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3001">6</span></span>

<span data-ttu-id="5fa9d-3002">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3002">7</span></span>

<span data-ttu-id="5fa9d-3003">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3003">8</span></span>

<span data-ttu-id="5fa9d-3004">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3004">9</span></span>

<span data-ttu-id="5fa9d-3005">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3005">1</span></span><br/> <span data-ttu-id="5fa9d-3006">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3006">0</span></span><br/>

<span data-ttu-id="5fa9d-3007">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3007">1</span></span>

<span data-ttu-id="5fa9d-3008">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3008">2</span></span>

<span data-ttu-id="5fa9d-3009">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3009">3</span></span>

<span data-ttu-id="5fa9d-3010">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3010">4</span></span>

<span data-ttu-id="5fa9d-3011">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3011">5</span></span>

<span data-ttu-id="5fa9d-3012">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3012">6</span></span>

<span data-ttu-id="5fa9d-3013">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3013">7</span></span>

<span data-ttu-id="5fa9d-3014">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3014">8</span></span>

<span data-ttu-id="5fa9d-3015">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3015">9</span></span>

<span data-ttu-id="5fa9d-3016">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3016">2</span></span><br/> <span data-ttu-id="5fa9d-3017">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3017">0</span></span><br/>

<span data-ttu-id="5fa9d-3018">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3018">1</span></span>

<span data-ttu-id="5fa9d-3019">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3019">2</span></span>

<span data-ttu-id="5fa9d-3020">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3020">3</span></span>

<span data-ttu-id="5fa9d-3021">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3021">4</span></span>

<span data-ttu-id="5fa9d-3022">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3022">5</span></span>

<span data-ttu-id="5fa9d-3023">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3023">6</span></span>

<span data-ttu-id="5fa9d-3024">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3024">7</span></span>

<span data-ttu-id="5fa9d-3025">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3025">8</span></span>

<span data-ttu-id="5fa9d-3026">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3026">9</span></span>

<span data-ttu-id="5fa9d-3027">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3027">3</span></span><br/> <span data-ttu-id="5fa9d-3028">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3028">0</span></span><br/>

<span data-ttu-id="5fa9d-3029">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3029">1</span></span>

<span data-ttu-id="5fa9d-3030">\_partID (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3030">\_partID (optional)</span></span>



 

<span data-ttu-id="5fa9d-3031">**\_ PARTID**: это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3031">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="5fa9d-3032">Если это поле указано, оно должно быть установлено в значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3032">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="5fa9d-3033">2.2.3.6 Кпмконнектин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3033">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="5fa9d-3034">Сообщение Кпмконнектин начинает сеанс между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3034">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="5fa9d-3035">Формат сообщения Кпмконнектин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3035">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3036">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3036">0</span></span>

<span data-ttu-id="5fa9d-3037">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3037">1</span></span>

<span data-ttu-id="5fa9d-3038">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3038">2</span></span>

<span data-ttu-id="5fa9d-3039">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3039">3</span></span>

<span data-ttu-id="5fa9d-3040">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3040">4</span></span>

<span data-ttu-id="5fa9d-3041">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3041">5</span></span>

<span data-ttu-id="5fa9d-3042">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3042">6</span></span>

<span data-ttu-id="5fa9d-3043">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3043">7</span></span>

<span data-ttu-id="5fa9d-3044">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3044">8</span></span>

<span data-ttu-id="5fa9d-3045">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3045">9</span></span>

<span data-ttu-id="5fa9d-3046">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3046">1</span></span><br/> <span data-ttu-id="5fa9d-3047">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3047">0</span></span><br/>

<span data-ttu-id="5fa9d-3048">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3048">1</span></span>

<span data-ttu-id="5fa9d-3049">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3049">2</span></span>

<span data-ttu-id="5fa9d-3050">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3050">3</span></span>

<span data-ttu-id="5fa9d-3051">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3051">4</span></span>

<span data-ttu-id="5fa9d-3052">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3052">5</span></span>

<span data-ttu-id="5fa9d-3053">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3053">6</span></span>

<span data-ttu-id="5fa9d-3054">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3054">7</span></span>

<span data-ttu-id="5fa9d-3055">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3055">8</span></span>

<span data-ttu-id="5fa9d-3056">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3056">9</span></span>

<span data-ttu-id="5fa9d-3057">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3057">2</span></span><br/> <span data-ttu-id="5fa9d-3058">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3058">0</span></span><br/>

<span data-ttu-id="5fa9d-3059">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3059">1</span></span>

<span data-ttu-id="5fa9d-3060">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3060">2</span></span>

<span data-ttu-id="5fa9d-3061">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3061">3</span></span>

<span data-ttu-id="5fa9d-3062">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3062">4</span></span>

<span data-ttu-id="5fa9d-3063">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3063">5</span></span>

<span data-ttu-id="5fa9d-3064">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3064">6</span></span>

<span data-ttu-id="5fa9d-3065">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3065">7</span></span>

<span data-ttu-id="5fa9d-3066">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3066">8</span></span>

<span data-ttu-id="5fa9d-3067">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3067">9</span></span>

<span data-ttu-id="5fa9d-3068">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3068">3</span></span><br/> <span data-ttu-id="5fa9d-3069">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3069">0</span></span><br/>

<span data-ttu-id="5fa9d-3070">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3070">1</span></span>

<span data-ttu-id="5fa9d-3071">\_иклиентверсион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3071">\_iClientVersion</span></span>

<span data-ttu-id="5fa9d-3072">\_фклиентисремоте</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3072">\_fClientIsRemote</span></span>

<span data-ttu-id="5fa9d-3073">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3073">\_cbBlob1</span></span>

<span data-ttu-id="5fa9d-3074">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3074">\_cbBlob2</span></span>

<span data-ttu-id="5fa9d-3075">\_заполнение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3075">\_padding</span></span>

<span data-ttu-id="5fa9d-3076">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3076">...</span></span>

<span data-ttu-id="5fa9d-3077">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3077">...</span></span>

<span data-ttu-id="5fa9d-3078">MachineName</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3078">MachineName</span></span>

<span data-ttu-id="5fa9d-3079">... перемен</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3079">... (variable)</span></span>

<span data-ttu-id="5fa9d-3080">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3080">UserName</span></span>

<span data-ttu-id="5fa9d-3081">... перемен</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3081">... (variable)</span></span>

<span data-ttu-id="5fa9d-3082">\_Паддингкпропсетс (необязательный, переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3082">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="5fa9d-3083">кпропсетс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3083">cPropSets</span></span>

<span data-ttu-id="5fa9d-3084">PropertySet1 (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3084">PropertySet1 (variable)</span></span>

<span data-ttu-id="5fa9d-3085">PropertySet2 (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3085">PropertySet2 (variable)</span></span>

<span data-ttu-id="5fa9d-3086">\_Паддинжекстпропсет (необязательный, переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3086">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="5fa9d-3087">цекстпропсет</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3087">cExtPropSet</span></span>

<span data-ttu-id="5fa9d-3088">Апропертисетс (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3088">aPropertySets (variable)</span></span>



 

<span data-ttu-id="5fa9d-3089">**\_ иклиентверсион**: 32-разрядное целое число, указывающее, должен ли сервер проверять значение контрольной суммы, указанное в \_ поле улчекксум заголовков сообщений для сообщений, отправленных клиентом.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3089">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="5fa9d-3090">Если \_ поле иклиентверсион имеет значение 0x00000008 или больше, сервер должен проверить \_ значение поля улчекксум для следующих сообщений:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3090">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="5fa9d-3091">кпмконнектин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3091">CPMConnectIn</span></span>
-   <span data-ttu-id="5fa9d-3092">кпмкреатекуерин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3092">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="5fa9d-3093">кпмфетчвалуеин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3093">CPMFetchValueIn</span></span>
-   <span data-ttu-id="5fa9d-3094">кпмжетровсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3094">CPMGetRowsIn</span></span>
-   <span data-ttu-id="5fa9d-3095">кпмсетбиндингсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3095">CPMSetBindingsIn</span></span>

<span data-ttu-id="5fa9d-3096">Дополнительные сведения о том, как сервер проверяет значение, указанное клиентом в поле Улчекксум, для сообщений, перечисленных выше, см. в разделе 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3096">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="5fa9d-3097">Если значение больше 0x00000008, предполагается, что клиент может обрабатывать 64-битные смещения в сообщениях Кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3097">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="5fa9d-3098">Дополнительные сведения см. в разделе 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3098">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="5fa9d-3099">*Поведение Windows. в клиентах Windows параметр иклиентверсион устанавливается следующим* образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3099">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="5fa9d-3100">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3100">Value</span></span>      | <span data-ttu-id="5fa9d-3101">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3101">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-3102">0x00000005</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3102">0x00000005</span></span> | <span data-ttu-id="5fa9d-3103">Клиентская ОС — Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3103">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="5fa9d-3104">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3104">0x00000008</span></span> | <span data-ttu-id="5fa9d-3105">Клиентская ОС — 32-разрядная версия Windows XP или 32-разрядная версия Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3105">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="5fa9d-3106">0x00010008</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3106">0x00010008</span></span> | <span data-ttu-id="5fa9d-3107">Клиентская ОС — 64-разрядная версия Windows XP или 64-разрядная версия Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3107">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="5fa9d-3108">\_**фклиентисремоте**: логическое значение, указывающее, работает ли клиент на компьютере, отличном от компьютера, на котором находится сервер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3108">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="5fa9d-3109">НЕОБХОДИМО задать значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3109">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="5fa9d-3110">\_**cbBlob1**: 32-разрядное целое число без знака, указывающее размер в байтах для полей Кпропсет, PropertySet1 и PropertySet2 в сочетании.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3110">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="5fa9d-3111">\_**cbBlob2**: 32-разрядное целое число без знака, указывающее размер в байтах для полей Цекспропсет и апропертисет в сочетании.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3111">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="5fa9d-3112">\_**Заполнение**: 12 байтов заполнения, которые могут содержать произвольные значения, и должны игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3112">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="5fa9d-3113">**MachineName**— имя компьютера клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3113">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="5fa9d-3114">Строка имени должна быть массивом, заканчивающимся нулем, размером менее 512 символов Юникода, включая знак завершения NULL.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3114">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="5fa9d-3115">**Username**— строка, представляющая имя пользователя, запустившего приложение, которое вызвало этот протокол.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3115">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="5fa9d-3116">Строка имени должна быть массивом, заканчивающимся нулем, размером менее 512 символов Юникода при объединении с MachineName.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3116">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="5fa9d-3117">**\_ паддингкпропсетс**: длина этого поля должна быть от 0 до 7 байт.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3117">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="5fa9d-3118">Число байтов должно быть числом, необходимым для смещения в байтах поля Кпропсетс с начала сообщения, содержащего эту структуру, кратной 8.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3118">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="5fa9d-3119">Значение байт может быть любым произвольным значением и должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3119">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="5fa9d-3120">**кпропсетс**: 32-разрядное целое число без знака, указывающее количество структур кдбпропсет, следующих за этим полем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3120">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="5fa9d-3121">Это значение должно быть равно 0x0000002.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3121">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="5fa9d-3122">**PropertySet1**: структура Кдбпропсет с гуидпропертисет, содержащей DBPROPSET \_ фсЦифрмврк \_ ext (см. раздел 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3122">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="5fa9d-3123">**PropertySet2**: структура Кдбпропсет с гуидпропертисет, содержащей DBPROPSET \_ Цифрмврккоре \_ ext (см. раздел 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3123">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="5fa9d-3124">\_**Паддинжекстпропсет**: длина этого поля должна быть от 0 до 7 байт.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3124">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="5fa9d-3125">Число байтов должно быть числом, необходимым для смещения в байтах поля Цекстпропсетс с начала сообщения, содержащего эту структуру, кратной 8.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3125">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="5fa9d-3126">Значение байт может быть любым произвольным значением и должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3126">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="5fa9d-3127">**цекстпропсет**: 32-разрядное целое число без знака, указывающее количество структур кдбпропсет, следующих за этим полем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3127">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="5fa9d-3128">**апропертисетс**: массив структур кдбпропсет, задающий другие свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3128">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="5fa9d-3129">Число элементов в этом массиве должно быть равно Цекстпропсет.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3129">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="5fa9d-3130">2.2.3.7 Кпмконнектаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3130">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="5fa9d-3131">Сообщение Кпмконнектаут содержит ответ на сообщение Кпмконнектин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3131">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="5fa9d-3132">Формат сообщения Кпмконнектаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3132">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3133">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3133">0</span></span>

<span data-ttu-id="5fa9d-3134">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3134">1</span></span>

<span data-ttu-id="5fa9d-3135">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3135">2</span></span>

<span data-ttu-id="5fa9d-3136">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3136">3</span></span>

<span data-ttu-id="5fa9d-3137">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3137">4</span></span>

<span data-ttu-id="5fa9d-3138">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3138">5</span></span>

<span data-ttu-id="5fa9d-3139">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3139">6</span></span>

<span data-ttu-id="5fa9d-3140">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3140">7</span></span>

<span data-ttu-id="5fa9d-3141">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3141">8</span></span>

<span data-ttu-id="5fa9d-3142">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3142">9</span></span>

<span data-ttu-id="5fa9d-3143">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3143">1</span></span><br/> <span data-ttu-id="5fa9d-3144">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3144">0</span></span><br/>

<span data-ttu-id="5fa9d-3145">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3145">1</span></span>

<span data-ttu-id="5fa9d-3146">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3146">2</span></span>

<span data-ttu-id="5fa9d-3147">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3147">3</span></span>

<span data-ttu-id="5fa9d-3148">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3148">4</span></span>

<span data-ttu-id="5fa9d-3149">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3149">5</span></span>

<span data-ttu-id="5fa9d-3150">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3150">6</span></span>

<span data-ttu-id="5fa9d-3151">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3151">7</span></span>

<span data-ttu-id="5fa9d-3152">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3152">8</span></span>

<span data-ttu-id="5fa9d-3153">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3153">9</span></span>

<span data-ttu-id="5fa9d-3154">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3154">2</span></span><br/> <span data-ttu-id="5fa9d-3155">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3155">0</span></span><br/>

<span data-ttu-id="5fa9d-3156">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3156">1</span></span>

<span data-ttu-id="5fa9d-3157">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3157">2</span></span>

<span data-ttu-id="5fa9d-3158">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3158">3</span></span>

<span data-ttu-id="5fa9d-3159">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3159">4</span></span>

<span data-ttu-id="5fa9d-3160">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3160">5</span></span>

<span data-ttu-id="5fa9d-3161">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3161">6</span></span>

<span data-ttu-id="5fa9d-3162">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3162">7</span></span>

<span data-ttu-id="5fa9d-3163">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3163">8</span></span>

<span data-ttu-id="5fa9d-3164">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3164">9</span></span>

<span data-ttu-id="5fa9d-3165">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3165">3</span></span><br/> <span data-ttu-id="5fa9d-3166">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3166">0</span></span><br/>

<span data-ttu-id="5fa9d-3167">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3167">1</span></span>

<span data-ttu-id="5fa9d-3168">\_serverVersion</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3168">\_serverVersion</span></span>

<span data-ttu-id="5fa9d-3169">\_зарезервировано (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3169">\_reserved (variable)</span></span>



 

<span data-ttu-id="5fa9d-3170">**\_ serverVersion**:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3170">**\_serverVersion**:</span></span>

<span data-ttu-id="5fa9d-3171">32-разрядное целое число, указывающее, может ли сервер поддерживать 64-битное смещение *.*</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3171">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="5fa9d-3172">Дополнительные сведения см. в разделе 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3172">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="5fa9d-3173">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3173">Value</span></span>      | <span data-ttu-id="5fa9d-3174">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3174">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="5fa9d-3175">0x00000007</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3175">0x00000007</span></span> | <span data-ttu-id="5fa9d-3176">Сервер может передавать только 32-разрядные смещения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3176">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="5fa9d-3177">0x00010007</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3177">0x00010007</span></span> | <span data-ttu-id="5fa9d-3178">Сервер может передавать 32 или 64-битные смещения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3178">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="5fa9d-3179">**\_ зарезервировано**: зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3179">**\_reserved**: Reserved.</span></span> <span data-ttu-id="5fa9d-3180">Сервер может отправить произвольное число произвольных значений, и клиент должен игнорировать эти значения, если они есть.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3180">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="5fa9d-3181">2.2.3.8 Кпмкреатекуерин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3181">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="5fa9d-3182">Сообщение Кпмкреатекуерин создает новый запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3182">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="5fa9d-3183">Формат сообщения Кпмкреатекуерин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3183">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3184">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3184">0</span></span>

<span data-ttu-id="5fa9d-3185">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3185">1</span></span>

<span data-ttu-id="5fa9d-3186">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3186">2</span></span>

<span data-ttu-id="5fa9d-3187">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3187">3</span></span>

<span data-ttu-id="5fa9d-3188">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3188">4</span></span>

<span data-ttu-id="5fa9d-3189">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3189">5</span></span>

<span data-ttu-id="5fa9d-3190">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3190">6</span></span>

<span data-ttu-id="5fa9d-3191">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3191">7</span></span>

<span data-ttu-id="5fa9d-3192">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3192">8</span></span>

<span data-ttu-id="5fa9d-3193">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3193">9</span></span>

<span data-ttu-id="5fa9d-3194">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3194">1</span></span><br/> <span data-ttu-id="5fa9d-3195">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3195">0</span></span><br/>

<span data-ttu-id="5fa9d-3196">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3196">1</span></span>

<span data-ttu-id="5fa9d-3197">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3197">2</span></span>

<span data-ttu-id="5fa9d-3198">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3198">3</span></span>

<span data-ttu-id="5fa9d-3199">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3199">4</span></span>

<span data-ttu-id="5fa9d-3200">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3200">5</span></span>

<span data-ttu-id="5fa9d-3201">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3201">6</span></span>

<span data-ttu-id="5fa9d-3202">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3202">7</span></span>

<span data-ttu-id="5fa9d-3203">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3203">8</span></span>

<span data-ttu-id="5fa9d-3204">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3204">9</span></span>

<span data-ttu-id="5fa9d-3205">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3205">2</span></span><br/> <span data-ttu-id="5fa9d-3206">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3206">0</span></span><br/>

<span data-ttu-id="5fa9d-3207">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3207">1</span></span>

<span data-ttu-id="5fa9d-3208">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3208">2</span></span>

<span data-ttu-id="5fa9d-3209">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3209">3</span></span>

<span data-ttu-id="5fa9d-3210">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3210">4</span></span>

<span data-ttu-id="5fa9d-3211">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3211">5</span></span>

<span data-ttu-id="5fa9d-3212">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3212">6</span></span>

<span data-ttu-id="5fa9d-3213">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3213">7</span></span>

<span data-ttu-id="5fa9d-3214">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3214">8</span></span>

<span data-ttu-id="5fa9d-3215">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3215">9</span></span>

<span data-ttu-id="5fa9d-3216">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3216">3</span></span><br/> <span data-ttu-id="5fa9d-3217">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3217">0</span></span><br/>

<span data-ttu-id="5fa9d-3218">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3218">1</span></span>

<span data-ttu-id="5fa9d-3219">Размер</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3219">Size</span></span>

<span data-ttu-id="5fa9d-3220">кколумнсетпресент</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3220">CColumnSetPresent</span></span>

<span data-ttu-id="5fa9d-3221">(Необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3221">ColumnSet (optional)</span></span>

<span data-ttu-id="5fa9d-3222">... перемен</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3222">... (variable)</span></span>

<span data-ttu-id="5fa9d-3223">Крестриктионпресент.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3223">CRestrictionPresent.</span></span>

<span data-ttu-id="5fa9d-3224">Ограничение (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3224">Restriction (optional)</span></span>

<span data-ttu-id="5fa9d-3225">... перемен</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3225">... (variable)</span></span>

<span data-ttu-id="5fa9d-3226">ксортсетпресент</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3226">CSortSetPresent</span></span>

<span data-ttu-id="5fa9d-3227">Тип сортировки (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3227">SortSet (optional)</span></span>

<span data-ttu-id="5fa9d-3228">... перемен</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3228">... (variable)</span></span>

<span data-ttu-id="5fa9d-3229">ккатегоризатионсетпресент</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3229">CCategorizationSetPresent</span></span>

<span data-ttu-id="5fa9d-3230">Категоризатионсет (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3230">CategorizationSet (optional)</span></span>

<span data-ttu-id="5fa9d-3231">... перемен</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3231">... (variable)</span></span>

<span data-ttu-id="5fa9d-3232">ровсетпропертиес</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3232">RowSetProperties</span></span>

<span data-ttu-id="5fa9d-3233">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3233">...</span></span>

<span data-ttu-id="5fa9d-3234">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3234">...</span></span>

<span data-ttu-id="5fa9d-3235">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3235">...</span></span>

<span data-ttu-id="5fa9d-3236">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3236">...</span></span>

<span data-ttu-id="5fa9d-3237">Пидмаппер (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3237">PidMapper (variable)</span></span>



 

<span data-ttu-id="5fa9d-3238">**Размер**: 32-разрядное целое число без знака, указывающее число байтов от начала этого поля до конца сообщения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3238">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="5fa9d-3239">**Кколумнсетпресент**: поле byte, указывающее, имеется ли поле с набором столбцов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3239">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="5fa9d-3240">Для этого поля необходимо задать значение 0x01 или 0x00.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3240">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="5fa9d-3241">Если задано значение 0x01, поле Кколумнсет должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3241">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="5fa9d-3242">Если задано значение 0x00, оно должно отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3242">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="5fa9d-3243">Набор **столбцов**: структура кколумнсет, содержащая номера столбцов, в которых должны возвращаться свойства кпидмаппер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3243">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="5fa9d-3244">**Крестриктионпресент**: поле byte, указывающее, имеется ли поле ограничения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3244">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="5fa9d-3245">Если задано любое ненулевое значение, поле ограничения должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3245">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="5fa9d-3246">Если задано значение 0x00, ограничение должно отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3246">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="5fa9d-3247">**Ограничение**: структура крестриктион, содержащая дерево команд запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3247">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="5fa9d-3248">**Ксортсетпресент**: поле byte, указывающее, имеется ли поле Sorting.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3248">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="5fa9d-3249">Если задано любое ненулевое значение, поле Sorting должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3249">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="5fa9d-3250">Если задано значение 0x00, то параметр Sort должен отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3250">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="5fa9d-3251">Набор **сортировки**: структура ксортсет, указывающая порядок сортировки запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3251">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="5fa9d-3252">**Ккатегоризатионсетпресент**: поле byte, указывающее, имеется ли поле ккатегоризатионсет.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3252">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="5fa9d-3253">Если задано любое ненулевое значение, поле Ккатегоризатионсет должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3253">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="5fa9d-3254">Если задано значение 0x00, Ккатегоризатионсет должно отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3254">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="5fa9d-3255">**Ккатегоризатионсет**: структура ккатегоризатионсет, содержащая группы для запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3255">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="5fa9d-3256">**Ровсетпропертиес**: структура кровсетпропертиес, предоставляющая сведения о конфигурации для запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3256">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="5fa9d-3257">**Пидмаппер**: структура кпидмаппер, содержащая свойства, возвращаемые в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3257">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="5fa9d-3258">2.2.3.9 Кпмкреатекуерйоут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3258">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="5fa9d-3259">Сообщение Кпмкреатекуерйоут содержит ответ на сообщение Кпмкреатекуерин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3259">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="5fa9d-3260">Формат сообщения Кпмкреатекуерйоут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3260">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3261">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3261">0</span></span>

<span data-ttu-id="5fa9d-3262">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3262">1</span></span>

<span data-ttu-id="5fa9d-3263">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3263">2</span></span>

<span data-ttu-id="5fa9d-3264">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3264">3</span></span>

<span data-ttu-id="5fa9d-3265">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3265">4</span></span>

<span data-ttu-id="5fa9d-3266">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3266">5</span></span>

<span data-ttu-id="5fa9d-3267">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3267">6</span></span>

<span data-ttu-id="5fa9d-3268">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3268">7</span></span>

<span data-ttu-id="5fa9d-3269">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3269">8</span></span>

<span data-ttu-id="5fa9d-3270">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3270">9</span></span>

<span data-ttu-id="5fa9d-3271">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3271">1</span></span><br/> <span data-ttu-id="5fa9d-3272">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3272">0</span></span><br/>

<span data-ttu-id="5fa9d-3273">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3273">1</span></span>

<span data-ttu-id="5fa9d-3274">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3274">2</span></span>

<span data-ttu-id="5fa9d-3275">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3275">3</span></span>

<span data-ttu-id="5fa9d-3276">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3276">4</span></span>

<span data-ttu-id="5fa9d-3277">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3277">5</span></span>

<span data-ttu-id="5fa9d-3278">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3278">6</span></span>

<span data-ttu-id="5fa9d-3279">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3279">7</span></span>

<span data-ttu-id="5fa9d-3280">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3280">8</span></span>

<span data-ttu-id="5fa9d-3281">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3281">9</span></span>

<span data-ttu-id="5fa9d-3282">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3282">2</span></span><br/> <span data-ttu-id="5fa9d-3283">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3283">0</span></span><br/>

<span data-ttu-id="5fa9d-3284">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3284">1</span></span>

<span data-ttu-id="5fa9d-3285">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3285">2</span></span>

<span data-ttu-id="5fa9d-3286">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3286">3</span></span>

<span data-ttu-id="5fa9d-3287">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3287">4</span></span>

<span data-ttu-id="5fa9d-3288">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3288">5</span></span>

<span data-ttu-id="5fa9d-3289">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3289">6</span></span>

<span data-ttu-id="5fa9d-3290">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3290">7</span></span>

<span data-ttu-id="5fa9d-3291">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3291">8</span></span>

<span data-ttu-id="5fa9d-3292">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3292">9</span></span>

<span data-ttu-id="5fa9d-3293">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3293">3</span></span><br/> <span data-ttu-id="5fa9d-3294">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3294">0</span></span><br/>

<span data-ttu-id="5fa9d-3295">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3295">1</span></span>

<span data-ttu-id="5fa9d-3296">\_фтруесекуентиал</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3296">\_fTrueSequential</span></span>

<span data-ttu-id="5fa9d-3297">\_фворкидуникуе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3297">\_fWorkIdUnique</span></span>

<span data-ttu-id="5fa9d-3298">акурсорс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3298">aCursors</span></span>



 

<span data-ttu-id="5fa9d-3299">**\_ фтруесекуентиал**: информативное логическое значение, указывающее, может ли запрос получать результаты быстрее.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3299">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="5fa9d-3300">Если для запроса, предоставленного в Кпмкреатекуерин, задано 0x00000001, сервер может использовать индекс таким образом, чтобы результаты запроса могли быть доставлены быстрее.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3300">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="5fa9d-3301">Если задано значение 0x00000000, то при доставке результатов запроса будет воздержаться задержка.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3301">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="5fa9d-3302">Не должно быть задано ни одно другое значение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3302">MUST not be set to any other value.</span></span>

<span data-ttu-id="5fa9d-3303">**\_ фворкидуникуе**: логическое значение, указывающее, являются ли идентификаторы документов, на которые указывают курсоры, уникальными в результатах запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3303">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="5fa9d-3304">Если задано значение 0x00000001, идентификаторы являются уникальными.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3304">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="5fa9d-3305">Если задано значение 0x00000000, они уникальны только во всем наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3305">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="5fa9d-3306">**акурсорс**: массив из 32-разрядных целых чисел без знака, представляющих дескрипторы курсоров, с числом элементов, равным числу категорий в поле Категоризатионсет сообщения кпмкреатекуерин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3306">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="5fa9d-3307">2.2.3.10 Кпмжеткуеристатусин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3307">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="5fa9d-3308">Сообщение Кпмжеткуеристатусин запрашивает состояние запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3308">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="5fa9d-3309">Формат сообщения Кпмжеткуеристатусин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3309">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3310">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3310">0</span></span>

<span data-ttu-id="5fa9d-3311">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3311">1</span></span>

<span data-ttu-id="5fa9d-3312">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3312">2</span></span>

<span data-ttu-id="5fa9d-3313">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3313">3</span></span>

<span data-ttu-id="5fa9d-3314">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3314">4</span></span>

<span data-ttu-id="5fa9d-3315">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3315">5</span></span>

<span data-ttu-id="5fa9d-3316">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3316">6</span></span>

<span data-ttu-id="5fa9d-3317">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3317">7</span></span>

<span data-ttu-id="5fa9d-3318">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3318">8</span></span>

<span data-ttu-id="5fa9d-3319">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3319">9</span></span>

<span data-ttu-id="5fa9d-3320">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3320">1</span></span><br/> <span data-ttu-id="5fa9d-3321">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3321">0</span></span><br/>

<span data-ttu-id="5fa9d-3322">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3322">1</span></span>

<span data-ttu-id="5fa9d-3323">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3323">2</span></span>

<span data-ttu-id="5fa9d-3324">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3324">3</span></span>

<span data-ttu-id="5fa9d-3325">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3325">4</span></span>

<span data-ttu-id="5fa9d-3326">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3326">5</span></span>

<span data-ttu-id="5fa9d-3327">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3327">6</span></span>

<span data-ttu-id="5fa9d-3328">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3328">7</span></span>

<span data-ttu-id="5fa9d-3329">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3329">8</span></span>

<span data-ttu-id="5fa9d-3330">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3330">9</span></span>

<span data-ttu-id="5fa9d-3331">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3331">2</span></span><br/> <span data-ttu-id="5fa9d-3332">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3332">0</span></span><br/>

<span data-ttu-id="5fa9d-3333">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3333">1</span></span>

<span data-ttu-id="5fa9d-3334">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3334">2</span></span>

<span data-ttu-id="5fa9d-3335">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3335">3</span></span>

<span data-ttu-id="5fa9d-3336">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3336">4</span></span>

<span data-ttu-id="5fa9d-3337">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3337">5</span></span>

<span data-ttu-id="5fa9d-3338">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3338">6</span></span>

<span data-ttu-id="5fa9d-3339">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3339">7</span></span>

<span data-ttu-id="5fa9d-3340">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3340">8</span></span>

<span data-ttu-id="5fa9d-3341">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3341">9</span></span>

<span data-ttu-id="5fa9d-3342">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3342">3</span></span><br/> <span data-ttu-id="5fa9d-3343">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3343">0</span></span><br/>

<span data-ttu-id="5fa9d-3344">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3344">1</span></span>

<span data-ttu-id="5fa9d-3345">\_хкурсор</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3345">\_hCursor</span></span>



 

<span data-ttu-id="5fa9d-3346">**\_ хкурсор**: 32-разрядное целое число без знака, представляющее маркер из сообщения кпмкреатекуерйоут, идентифицирующего запрос, для которого необходимо получить сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3346">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="5fa9d-3347">2.2.3.11 Кпмжеткуеристатусаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3347">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="5fa9d-3348">Сообщение Кпмжеткуеристатусаут отвечает на сообщение Кпмжеткуеристатусин с состоянием запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3348">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="5fa9d-3349">Формат сообщения Кпмжеткуеристатусаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3349">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3350">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3350">0</span></span>

<span data-ttu-id="5fa9d-3351">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3351">1</span></span>

<span data-ttu-id="5fa9d-3352">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3352">2</span></span>

<span data-ttu-id="5fa9d-3353">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3353">3</span></span>

<span data-ttu-id="5fa9d-3354">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3354">4</span></span>

<span data-ttu-id="5fa9d-3355">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3355">5</span></span>

<span data-ttu-id="5fa9d-3356">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3356">6</span></span>

<span data-ttu-id="5fa9d-3357">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3357">7</span></span>

<span data-ttu-id="5fa9d-3358">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3358">8</span></span>

<span data-ttu-id="5fa9d-3359">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3359">9</span></span>

<span data-ttu-id="5fa9d-3360">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3360">1</span></span><br/> <span data-ttu-id="5fa9d-3361">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3361">0</span></span><br/>

<span data-ttu-id="5fa9d-3362">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3362">1</span></span>

<span data-ttu-id="5fa9d-3363">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3363">2</span></span>

<span data-ttu-id="5fa9d-3364">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3364">3</span></span>

<span data-ttu-id="5fa9d-3365">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3365">4</span></span>

<span data-ttu-id="5fa9d-3366">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3366">5</span></span>

<span data-ttu-id="5fa9d-3367">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3367">6</span></span>

<span data-ttu-id="5fa9d-3368">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3368">7</span></span>

<span data-ttu-id="5fa9d-3369">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3369">8</span></span>

<span data-ttu-id="5fa9d-3370">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3370">9</span></span>

<span data-ttu-id="5fa9d-3371">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3371">2</span></span><br/> <span data-ttu-id="5fa9d-3372">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3372">0</span></span><br/>

<span data-ttu-id="5fa9d-3373">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3373">1</span></span>

<span data-ttu-id="5fa9d-3374">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3374">2</span></span>

<span data-ttu-id="5fa9d-3375">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3375">3</span></span>

<span data-ttu-id="5fa9d-3376">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3376">4</span></span>

<span data-ttu-id="5fa9d-3377">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3377">5</span></span>

<span data-ttu-id="5fa9d-3378">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3378">6</span></span>

<span data-ttu-id="5fa9d-3379">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3379">7</span></span>

<span data-ttu-id="5fa9d-3380">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3380">8</span></span>

<span data-ttu-id="5fa9d-3381">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3381">9</span></span>

<span data-ttu-id="5fa9d-3382">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3382">3</span></span><br/> <span data-ttu-id="5fa9d-3383">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3383">0</span></span><br/>

<span data-ttu-id="5fa9d-3384">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3384">1</span></span>

<span data-ttu-id="5fa9d-3385">\_Состояние</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3385">\_Status</span></span>



 

<span data-ttu-id="5fa9d-3386">**\_ Состояние**: битовая маска значений, определенных в таблицах ниже, которая описывает запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3386">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="5fa9d-3387">В следующей таблице перечислены \_ \* значения Stat, полученные путем выполнения побитовой операции и для \_ состояния с 0x00000007.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3387">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="5fa9d-3388">Результат должен быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3388">The result MUST be one of the following:</span></span>



| <span data-ttu-id="5fa9d-3389">Константа</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3389">Constant</span></span>                 | <span data-ttu-id="5fa9d-3390">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3390">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-3391">STAT \_ занято 0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3391">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="5fa9d-3392">Асинхронный запрос все еще выполняется.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3392">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="5fa9d-3393">\_Ошибка stat 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3393">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="5fa9d-3394">Запрос находится в состоянии ошибки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3394">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="5fa9d-3395">РЕГЛАМЕНТное \_ Завершение 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3395">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="5fa9d-3396">Запрос завершен.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3396">The query is complete.</span></span>                                                            |
| <span data-ttu-id="5fa9d-3397">STAT \_ Refresh 0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3397">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="5fa9d-3398">Запрос завершен, но обновления приводят к дополнительным вычислениям запросов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3398">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="5fa9d-3399">В следующей таблице перечислены дополнительные \_ \* биты Stat, которые можно задать независимо.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3399">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="5fa9d-3400">Константа</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3400">Constant</span></span>                                    | <span data-ttu-id="5fa9d-3401">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3401">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-3402">STAT \_ пропускаемых \_ слов 0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3402">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="5fa9d-3403">Пропускаемые слова были заменены символами-шаблонами в запросе содержимого.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3403">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="5fa9d-3404">\_ \_ \_ Неактуальное содержимое \_ stat</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3404">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="5fa9d-3405">Результаты запроса могут быть неверными, так как в запросе были внесены измененные, но неиндексированные файлы.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3405">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="5fa9d-3406">\_Неполное обновление stat \_ 0x00000040</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3406">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="5fa9d-3407">Результаты запроса могут быть неверными, так как запрос содержал измененные и повторно индексированные файлы, содержимое которых не было указано.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3407">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="5fa9d-3408">\_Неполный \_ запрос содержимого stat \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3408">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="5fa9d-3409">Запрос содержимого был слишком сложен для завершения или обязательного перечисления вместо использования индекса содержимого.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3409">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="5fa9d-3410">\_Превышено ограничение по времени stat \_ \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3410">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="5fa9d-3411">Результаты запроса могут быть неверными, так как время выполнения запроса достигло максимально допустимого времени.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3411">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="5fa9d-3412">2.2.3.12 Кпмжеткуеристатусексин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3412">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="5fa9d-3413">Сообщение Кпмжеткуеристатусексин запрашивает состояние запроса и дополнительную информацию, например количество индексируемых документов, количество документов, оставшихся для индексирования, и т. д.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3413">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="5fa9d-3414">Формат сообщения Кпмжеткуеристатусексин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3414">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3415">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3415">0</span></span>

<span data-ttu-id="5fa9d-3416">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3416">1</span></span>

<span data-ttu-id="5fa9d-3417">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3417">2</span></span>

<span data-ttu-id="5fa9d-3418">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3418">3</span></span>

<span data-ttu-id="5fa9d-3419">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3419">4</span></span>

<span data-ttu-id="5fa9d-3420">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3420">5</span></span>

<span data-ttu-id="5fa9d-3421">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3421">6</span></span>

<span data-ttu-id="5fa9d-3422">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3422">7</span></span>

<span data-ttu-id="5fa9d-3423">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3423">8</span></span>

<span data-ttu-id="5fa9d-3424">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3424">9</span></span>

<span data-ttu-id="5fa9d-3425">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3425">1</span></span><br/> <span data-ttu-id="5fa9d-3426">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3426">0</span></span><br/>

<span data-ttu-id="5fa9d-3427">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3427">1</span></span>

<span data-ttu-id="5fa9d-3428">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3428">2</span></span>

<span data-ttu-id="5fa9d-3429">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3429">3</span></span>

<span data-ttu-id="5fa9d-3430">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3430">4</span></span>

<span data-ttu-id="5fa9d-3431">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3431">5</span></span>

<span data-ttu-id="5fa9d-3432">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3432">6</span></span>

<span data-ttu-id="5fa9d-3433">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3433">7</span></span>

<span data-ttu-id="5fa9d-3434">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3434">8</span></span>

<span data-ttu-id="5fa9d-3435">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3435">9</span></span>

<span data-ttu-id="5fa9d-3436">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3436">2</span></span><br/> <span data-ttu-id="5fa9d-3437">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3437">0</span></span><br/>

<span data-ttu-id="5fa9d-3438">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3438">1</span></span>

<span data-ttu-id="5fa9d-3439">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3439">2</span></span>

<span data-ttu-id="5fa9d-3440">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3440">3</span></span>

<span data-ttu-id="5fa9d-3441">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3441">4</span></span>

<span data-ttu-id="5fa9d-3442">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3442">5</span></span>

<span data-ttu-id="5fa9d-3443">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3443">6</span></span>

<span data-ttu-id="5fa9d-3444">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3444">7</span></span>

<span data-ttu-id="5fa9d-3445">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3445">8</span></span>

<span data-ttu-id="5fa9d-3446">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3446">9</span></span>

<span data-ttu-id="5fa9d-3447">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3447">3</span></span><br/> <span data-ttu-id="5fa9d-3448">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3448">0</span></span><br/>

<span data-ttu-id="5fa9d-3449">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3449">1</span></span>

<span data-ttu-id="5fa9d-3450">\_хкурсор</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3450">\_hCursor</span></span>

<span data-ttu-id="5fa9d-3451">\_бмк</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3451">\_bmk</span></span>



 

<span data-ttu-id="5fa9d-3452">**\_ хкурсор**: 32-разрядное значение, представляющее маркер из сообщения кпмкреатекуерйоут, идентифицирующего запрос, для которого необходимо получить сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3452">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="5fa9d-3453">**\_ бмк**: 32-разрядное значение, указывающее маркер закладки, расположение которого необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3453">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="5fa9d-3454">2.2.3.13 Кпмжеткуеристатусексаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3454">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="5fa9d-3455">Сообщение Кпмжеткуеристатусексаут отвечает на сообщение Кпмжеткуеристатусексин с состоянием запроса и другими сведениями о состоянии, как описано на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3455">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="5fa9d-3456">Формат сообщения Кпмжеткуеристатусексаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3456">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3457">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3457">0</span></span>

<span data-ttu-id="5fa9d-3458">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3458">1</span></span>

<span data-ttu-id="5fa9d-3459">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3459">2</span></span>

<span data-ttu-id="5fa9d-3460">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3460">3</span></span>

<span data-ttu-id="5fa9d-3461">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3461">4</span></span>

<span data-ttu-id="5fa9d-3462">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3462">5</span></span>

<span data-ttu-id="5fa9d-3463">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3463">6</span></span>

<span data-ttu-id="5fa9d-3464">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3464">7</span></span>

<span data-ttu-id="5fa9d-3465">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3465">8</span></span>

<span data-ttu-id="5fa9d-3466">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3466">9</span></span>

<span data-ttu-id="5fa9d-3467">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3467">1</span></span><br/> <span data-ttu-id="5fa9d-3468">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3468">0</span></span><br/>

<span data-ttu-id="5fa9d-3469">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3469">1</span></span>

<span data-ttu-id="5fa9d-3470">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3470">2</span></span>

<span data-ttu-id="5fa9d-3471">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3471">3</span></span>

<span data-ttu-id="5fa9d-3472">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3472">4</span></span>

<span data-ttu-id="5fa9d-3473">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3473">5</span></span>

<span data-ttu-id="5fa9d-3474">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3474">6</span></span>

<span data-ttu-id="5fa9d-3475">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3475">7</span></span>

<span data-ttu-id="5fa9d-3476">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3476">8</span></span>

<span data-ttu-id="5fa9d-3477">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3477">9</span></span>

<span data-ttu-id="5fa9d-3478">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3478">2</span></span><br/> <span data-ttu-id="5fa9d-3479">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3479">0</span></span><br/>

<span data-ttu-id="5fa9d-3480">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3480">1</span></span>

<span data-ttu-id="5fa9d-3481">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3481">2</span></span>

<span data-ttu-id="5fa9d-3482">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3482">3</span></span>

<span data-ttu-id="5fa9d-3483">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3483">4</span></span>

<span data-ttu-id="5fa9d-3484">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3484">5</span></span>

<span data-ttu-id="5fa9d-3485">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3485">6</span></span>

<span data-ttu-id="5fa9d-3486">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3486">7</span></span>

<span data-ttu-id="5fa9d-3487">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3487">8</span></span>

<span data-ttu-id="5fa9d-3488">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3488">9</span></span>

<span data-ttu-id="5fa9d-3489">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3489">3</span></span><br/> <span data-ttu-id="5fa9d-3490">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3490">0</span></span><br/>

<span data-ttu-id="5fa9d-3491">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3491">1</span></span>

<span data-ttu-id="5fa9d-3492">\_Состояние</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3492">\_Status</span></span>

<span data-ttu-id="5fa9d-3493">\_кфилтереддокументс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3493">\_cFilteredDocuments</span></span>

<span data-ttu-id="5fa9d-3494">\_кдокументстофилтер</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3494">\_cDocumentsToFilter</span></span>

<span data-ttu-id="5fa9d-3495">\_двратиофинишедденоминатор</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3495">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="5fa9d-3496">\_двратиофинишеднумератор</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3496">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="5fa9d-3497">\_ировбмк</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3497">\_iRowBmk</span></span>

<span data-ttu-id="5fa9d-3498">\_кровстотал</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3498">\_cRowsTotal</span></span>



 

<span data-ttu-id="5fa9d-3499">**\_ Состояние**: один из stat \_ \* значения, указанные в разделе 2.2.3.11.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3499">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="5fa9d-3500">**\_ кфилтереддокументс**: 32-разрядное целое число без знака, указывающее количество индексируемых документов</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3500">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="5fa9d-3501">**\_ кдокументстофилтер**: 32-разрядное целое число без знака, указывающее количество документов, которые еще остались для индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3501">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="5fa9d-3502">**\_ двратиофинишедденоминатор**: 32-разрядное целое число без знака, указывающее знаменатель отношения документов, обработка которых завершена в результате запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3502">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="5fa9d-3503">**\_ двратиофинишеднумератор**: 32-битовое целое число без знака, указывающее числитель коэффициента документов, обработка которых завершена в результате запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3503">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="5fa9d-3504">**\_ ировбмк**: 32-разрядное целое число без знака, указывающее приблизительное расположение закладки в наборе строк с точки зрения строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3504">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="5fa9d-3505">**\_ кровстотал**: 32-битовое целое число без знака, указывающее общее количество строк в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3505">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="5fa9d-3506">2.2.3.14 Кпмсетбиндингсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3506">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="5fa9d-3507">Сообщение Кпмсетбиндингсин запрашивает привязку столбцов к набору строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3507">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="5fa9d-3508">Сервер будет отвечать на сообщение запроса Кпмсетбиндингсин, используя раздел заголовка сообщения Кпмбиндингсин с результатами запроса, содержащимся в \_ поле Status (состояние).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3508">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="5fa9d-3509">Формат сообщения Кпмсетбиндингсин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3509">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3510">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3510">0</span></span>

<span data-ttu-id="5fa9d-3511">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3511">1</span></span>

<span data-ttu-id="5fa9d-3512">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3512">2</span></span>

<span data-ttu-id="5fa9d-3513">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3513">3</span></span>

<span data-ttu-id="5fa9d-3514">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3514">4</span></span>

<span data-ttu-id="5fa9d-3515">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3515">5</span></span>

<span data-ttu-id="5fa9d-3516">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3516">6</span></span>

<span data-ttu-id="5fa9d-3517">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3517">7</span></span>

<span data-ttu-id="5fa9d-3518">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3518">8</span></span>

<span data-ttu-id="5fa9d-3519">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3519">9</span></span>

<span data-ttu-id="5fa9d-3520">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3520">1</span></span><br/> <span data-ttu-id="5fa9d-3521">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3521">0</span></span><br/>

<span data-ttu-id="5fa9d-3522">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3522">1</span></span>

<span data-ttu-id="5fa9d-3523">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3523">2</span></span>

<span data-ttu-id="5fa9d-3524">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3524">3</span></span>

<span data-ttu-id="5fa9d-3525">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3525">4</span></span>

<span data-ttu-id="5fa9d-3526">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3526">5</span></span>

<span data-ttu-id="5fa9d-3527">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3527">6</span></span>

<span data-ttu-id="5fa9d-3528">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3528">7</span></span>

<span data-ttu-id="5fa9d-3529">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3529">8</span></span>

<span data-ttu-id="5fa9d-3530">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3530">9</span></span>

<span data-ttu-id="5fa9d-3531">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3531">2</span></span><br/> <span data-ttu-id="5fa9d-3532">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3532">0</span></span><br/>

<span data-ttu-id="5fa9d-3533">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3533">1</span></span>

<span data-ttu-id="5fa9d-3534">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3534">2</span></span>

<span data-ttu-id="5fa9d-3535">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3535">3</span></span>

<span data-ttu-id="5fa9d-3536">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3536">4</span></span>

<span data-ttu-id="5fa9d-3537">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3537">5</span></span>

<span data-ttu-id="5fa9d-3538">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3538">6</span></span>

<span data-ttu-id="5fa9d-3539">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3539">7</span></span>

<span data-ttu-id="5fa9d-3540">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3540">8</span></span>

<span data-ttu-id="5fa9d-3541">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3541">9</span></span>

<span data-ttu-id="5fa9d-3542">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3542">3</span></span><br/> <span data-ttu-id="5fa9d-3543">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3543">0</span></span><br/>

<span data-ttu-id="5fa9d-3544">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3544">1</span></span>

<span data-ttu-id="5fa9d-3545">\_Хкурсор (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3545">\_hCursor (optional)</span></span>

<span data-ttu-id="5fa9d-3546">\_Кбров (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3546">\_cbRow (optional)</span></span>

<span data-ttu-id="5fa9d-3547">\_Кббиндингдеск (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3547">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="5fa9d-3548">\_фиктивный (необязательный)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3548">\_dummy (optional)</span></span>

<span data-ttu-id="5fa9d-3549">Кколумнс (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3549">cColumns (optional)</span></span>

<span data-ttu-id="5fa9d-3550">Аколумнс (переменная, необязательный)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3550">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="5fa9d-3551">**\_ хкурсор**: 32-разрядное значение, представляющее маркер из сообщения кпмкреатекуерйоут, идентифицирующего строку, для которой задаются привязки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3551">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="5fa9d-3552">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3552">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="5fa9d-3553">**\_ кбров**: 32-битовое целое число без знака, указывающее размер строки в байтах.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3553">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="5fa9d-3554">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3554">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="5fa9d-3555">**\_ кббиндингдеск**: 32-разрядное целое число без знака, указывающее длину (в байтах) полей, следующих за \_ фиктивным полем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3555">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="5fa9d-3556">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="5fa9d-3557">**\_ фиктивное**: это поле не используется и должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3557">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="5fa9d-3558">Для него можно задать любое произвольное значение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3558">It can be set to any arbitrary value.</span></span> <span data-ttu-id="5fa9d-3559">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3559">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="5fa9d-3560">**кколумнс**: 32-разрядное целое число без знака, указывающее количество элементов в массиве аколумнс.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3560">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="5fa9d-3561">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3561">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="5fa9d-3562">**аколумнс**: массив структур ктаблеколумн, описывающих столбцы строки в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3562">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="5fa9d-3563">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3563">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="5fa9d-3564">Структуры в массиве должны быть разделены от 0 до 3 байтов с отступом таким, что каждая структура имеет 4-байтовое выравнивание от начала сообщения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3564">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="5fa9d-3565">Такое заполнение байтов может быть любым произвольным значением и не должно учитываться при получении.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3565">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="5fa9d-3566">2.2.3.15 Кпмжетровсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3566">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="5fa9d-3567">Сообщение Кпмжетровсин запрашивает строки из запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3567">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="5fa9d-3568">Формат сообщения Кпмжетровсин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3568">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3569">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3569">0</span></span>

<span data-ttu-id="5fa9d-3570">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3570">1</span></span>

<span data-ttu-id="5fa9d-3571">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3571">2</span></span>

<span data-ttu-id="5fa9d-3572">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3572">3</span></span>

<span data-ttu-id="5fa9d-3573">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3573">4</span></span>

<span data-ttu-id="5fa9d-3574">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3574">5</span></span>

<span data-ttu-id="5fa9d-3575">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3575">6</span></span>

<span data-ttu-id="5fa9d-3576">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3576">7</span></span>

<span data-ttu-id="5fa9d-3577">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3577">8</span></span>

<span data-ttu-id="5fa9d-3578">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3578">9</span></span>

<span data-ttu-id="5fa9d-3579">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3579">1</span></span><br/> <span data-ttu-id="5fa9d-3580">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3580">0</span></span><br/>

<span data-ttu-id="5fa9d-3581">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3581">1</span></span>

<span data-ttu-id="5fa9d-3582">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3582">2</span></span>

<span data-ttu-id="5fa9d-3583">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3583">3</span></span>

<span data-ttu-id="5fa9d-3584">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3584">4</span></span>

<span data-ttu-id="5fa9d-3585">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3585">5</span></span>

<span data-ttu-id="5fa9d-3586">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3586">6</span></span>

<span data-ttu-id="5fa9d-3587">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3587">7</span></span>

<span data-ttu-id="5fa9d-3588">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3588">8</span></span>

<span data-ttu-id="5fa9d-3589">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3589">9</span></span>

<span data-ttu-id="5fa9d-3590">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3590">2</span></span><br/> <span data-ttu-id="5fa9d-3591">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3591">0</span></span><br/>

<span data-ttu-id="5fa9d-3592">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3592">1</span></span>

<span data-ttu-id="5fa9d-3593">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3593">2</span></span>

<span data-ttu-id="5fa9d-3594">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3594">3</span></span>

<span data-ttu-id="5fa9d-3595">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3595">4</span></span>

<span data-ttu-id="5fa9d-3596">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3596">5</span></span>

<span data-ttu-id="5fa9d-3597">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3597">6</span></span>

<span data-ttu-id="5fa9d-3598">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3598">7</span></span>

<span data-ttu-id="5fa9d-3599">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3599">8</span></span>

<span data-ttu-id="5fa9d-3600">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3600">9</span></span>

<span data-ttu-id="5fa9d-3601">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3601">3</span></span><br/> <span data-ttu-id="5fa9d-3602">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3602">0</span></span><br/>

<span data-ttu-id="5fa9d-3603">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3603">1</span></span>

<span data-ttu-id="5fa9d-3604">\_хкурсор</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3604">\_hCursor</span></span>

<span data-ttu-id="5fa9d-3605">\_кровстотрансфер</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3605">\_cRowsToTransfer</span></span>

<span data-ttu-id="5fa9d-3606">\_кброввидс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3606">\_cbRowWidth</span></span>

<span data-ttu-id="5fa9d-3607">\_кбсик</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3607">\_cbSeek</span></span>

<span data-ttu-id="5fa9d-3608">\_кбресервед</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3608">\_cbReserved</span></span>

<span data-ttu-id="5fa9d-3609">\_кбреадбуффер</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3609">\_cbReadBuffer</span></span>

<span data-ttu-id="5fa9d-3610">\_улклиентбасе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3610">\_ulClientBase</span></span>

<span data-ttu-id="5fa9d-3611">\_фбвдфетч</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3611">\_fBwdFetch</span></span>

<span data-ttu-id="5fa9d-3612">eType</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3612">eType</span></span>

<span data-ttu-id="5fa9d-3613">\_Протокол CHAP</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3613">\_chapt</span></span>

<span data-ttu-id="5fa9d-3614">сикдескриптион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3614">SeekDescription</span></span>

<span data-ttu-id="5fa9d-3615">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3615">...</span></span>

<span data-ttu-id="5fa9d-3616">... перемен</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3616">... (variable)</span></span>



 

<span data-ttu-id="5fa9d-3617">**\_ хкурсор**: 32-разрядное значение, представляющее маркер из сообщения кпмкреатекуерйоут, идентифицирующего запрос, для которого необходимо получить строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3617">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="5fa9d-3618">**\_ кровстотрансфер**: 32-разрядное целое число без знака, указывающее максимальное число строк, которое клиент хочет получить в ответ на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3618">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="5fa9d-3619">**\_ кброввидс**: 32-разрядное целое число без знака, указывающее длину строки в байтах.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3619">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="5fa9d-3620">**\_ кбсик**: 32-битовое целое число без знака, указывающее размер сообщения, начинающегося с eType.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3620">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="5fa9d-3621">**\_ кбресервед**: 32-разрядное целое число без знака, указывающее размер (в байтах) сообщения кпмжетровсаут (без полей Rows и сикдескриптионс).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3621">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="5fa9d-3622">Это значение в этом поле добавляется к значению \_ поля кбсик, а затем используется для вычисления поля смещение строк в сообщении кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3622">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="5fa9d-3623">**\_ кбреадбуффер**: 32-разрядное целое число без знака, которое должно быть равно максимальному значению параметра \_ кброввидс или 1000, равному значению \_ кровстотрансфер, округленному до ближайшего 512 байта.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3623">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="5fa9d-3624">Значение не должно превышать 0x00004000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3624">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="5fa9d-3625">**\_ улклиентбасе**: 32-разрядное целое число без знака, указывающее базовое значение, используемое для вычислений указателей в буфере строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3625">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="5fa9d-3626">Если используются 64-разрядные смещения, поле reserved2 в заголовке сообщения используется в качестве верхних 32-бит и \_ улклиентбасе в качестве младших 32 бит для 64-разрядного значения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3626">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="5fa9d-3627">Дополнительные сведения см. в разделе 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3627">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="5fa9d-3628">**\_ фбвдфетч**: 32-битовое целое число без знака, указывающее порядок получения строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3628">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="5fa9d-3629">Если задано значение 0x00000001, строки будут извлекаться в обратную последовательность.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3629">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="5fa9d-3630">Если задано значение 0x00000000, строки будут извлекаться в прямом порядке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3630">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="5fa9d-3631">НЕ должно быть задано ни одного другого значения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3631">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="5fa9d-3632">**eType**: 32-разрядное целое число без знака, содержащее одно из следующих значений для указания типа выполняемой операции.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3632">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="5fa9d-3633">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3633">Value</span></span>                         | <span data-ttu-id="5fa9d-3634">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3634">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="5fa9d-3635">Еровсикнекст 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3635">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="5fa9d-3636">Сикдескриптион содержит структуру Кровсикнекст.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3636">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="5fa9d-3637">Еровсикат 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3637">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="5fa9d-3638">Сикдескриптион содержит структуру Кровсикат.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3638">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="5fa9d-3639">Еровсикатратио 0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3639">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="5fa9d-3640">Сикдескриптион содержит структуру Кровсикатратио.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3640">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="5fa9d-3641">Еровсикбибукмарк 0x00000004</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3641">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="5fa9d-3642">Сикдескриптион содержит структуру Кровсикбибукмарк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3642">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="5fa9d-3643">**\_ chap**: 32-разрядное значение, представляющее маркер главы набора строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3643">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="5fa9d-3644">**Сикдескриптион**: это поле должно содержать структуру типа, обозначенного значением eType.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3644">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="5fa9d-3645">2.2.3.16 Кпмжетровсаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3645">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="5fa9d-3646">Сообщение Кпмжетровсаут отвечает на сообщение Кпмжетровсин со строками запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3646">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="5fa9d-3647">Серверы должны отформатировать смещения до типов данных переменной длины в поле строк следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3647">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="5fa9d-3648">Клиент указал, что он был 32-разрядной системой (0x00000008 или меньше в поле Иклиентверсион Кпмконнектин): смещениями являются 32-разрядные целые числа.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3648">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="5fa9d-3649">Клиент указал, что он был 64-разрядной системой ( \_ иклиентверсион > 0x00000008 в кпмконнектин) и сервер указал, что он был 32-разрядной системой ( \_ serverVersion установлен в 0X00000007 в кпмконнектаут): смещениями являются 32-разрядные целые числа</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3649">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="5fa9d-3650">Клиент указал, что он был 64-разрядной системой ( \_ иклиентверсион > 0x00000008 в кпмконнектин) и сервер указал, что он был 64-разрядной системой ( \_ serverVersion установлен в 0X00010007 в кпмконнектаут): смещениями являются 64-разрядные целые числа</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3650">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="5fa9d-3651">Формат сообщения Кпмжетровсаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3651">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3652">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3652">0</span></span>

<span data-ttu-id="5fa9d-3653">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3653">1</span></span>

<span data-ttu-id="5fa9d-3654">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3654">2</span></span>

<span data-ttu-id="5fa9d-3655">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3655">3</span></span>

<span data-ttu-id="5fa9d-3656">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3656">4</span></span>

<span data-ttu-id="5fa9d-3657">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3657">5</span></span>

<span data-ttu-id="5fa9d-3658">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3658">6</span></span>

<span data-ttu-id="5fa9d-3659">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3659">7</span></span>

<span data-ttu-id="5fa9d-3660">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3660">8</span></span>

<span data-ttu-id="5fa9d-3661">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3661">9</span></span>

<span data-ttu-id="5fa9d-3662">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3662">1</span></span><br/> <span data-ttu-id="5fa9d-3663">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3663">0</span></span><br/>

<span data-ttu-id="5fa9d-3664">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3664">1</span></span>

<span data-ttu-id="5fa9d-3665">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3665">2</span></span>

<span data-ttu-id="5fa9d-3666">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3666">3</span></span>

<span data-ttu-id="5fa9d-3667">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3667">4</span></span>

<span data-ttu-id="5fa9d-3668">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3668">5</span></span>

<span data-ttu-id="5fa9d-3669">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3669">6</span></span>

<span data-ttu-id="5fa9d-3670">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3670">7</span></span>

<span data-ttu-id="5fa9d-3671">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3671">8</span></span>

<span data-ttu-id="5fa9d-3672">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3672">9</span></span>

<span data-ttu-id="5fa9d-3673">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3673">2</span></span><br/> <span data-ttu-id="5fa9d-3674">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3674">0</span></span><br/>

<span data-ttu-id="5fa9d-3675">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3675">1</span></span>

<span data-ttu-id="5fa9d-3676">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3676">2</span></span>

<span data-ttu-id="5fa9d-3677">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3677">3</span></span>

<span data-ttu-id="5fa9d-3678">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3678">4</span></span>

<span data-ttu-id="5fa9d-3679">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3679">5</span></span>

<span data-ttu-id="5fa9d-3680">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3680">6</span></span>

<span data-ttu-id="5fa9d-3681">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3681">7</span></span>

<span data-ttu-id="5fa9d-3682">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3682">8</span></span>

<span data-ttu-id="5fa9d-3683">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3683">9</span></span>

<span data-ttu-id="5fa9d-3684">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3684">3</span></span><br/> <span data-ttu-id="5fa9d-3685">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3685">0</span></span><br/>

<span data-ttu-id="5fa9d-3686">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3686">1</span></span>

<span data-ttu-id="5fa9d-3687">\_кровсретурнед</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3687">\_cRowsReturned</span></span>

<span data-ttu-id="5fa9d-3688">eType</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3688">eType</span></span>

<span data-ttu-id="5fa9d-3689">\_Протокол CHAP</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3689">\_chapt</span></span>

<span data-ttu-id="5fa9d-3690">Сикдескриптион (необязательный, переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3690">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="5fa9d-3691">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3691">...</span></span>

<span data-ttu-id="5fa9d-3692">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3692">...</span></span>

<span data-ttu-id="5fa9d-3693">Паддингровс (необязательный, переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3693">paddingRows (optional, variable)</span></span>

<span data-ttu-id="5fa9d-3694">Строки</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3694">Rows</span></span>



 

<span data-ttu-id="5fa9d-3695">**\_ кровсретурнед**: 32-разрядное целое число без знака, указывающее количество строк, возвращаемых в строках.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3695">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="5fa9d-3696">**eType**: 32-разрядное целое число без знака, содержащее одно из следующих значений, указывающее тип выполняемой операции ровсик.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3696">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="5fa9d-3697">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3697">Value</span></span>                         | <span data-ttu-id="5fa9d-3698">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3698">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="5fa9d-3699">Еровссикноне 0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3699">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="5fa9d-3700">Нет Сикдескриптион, игнорировать поле Сикдескриптион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3700">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="5fa9d-3701">Еровсикнекст 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3701">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="5fa9d-3702">Сикдескриптион содержит структуру Кровсикнекст.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3702">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="5fa9d-3703">Еровсикат 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3703">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="5fa9d-3704">Сикдескриптион содержит структуру Кровсикат.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3704">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="5fa9d-3705">Еровсикатратио 0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3705">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="5fa9d-3706">Сикдескриптион содержит структуру Кровсикатратио.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3706">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="5fa9d-3707">Еровсикбибукмарк 0x00000004</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3707">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="5fa9d-3708">Сикдескриптион содержит структуру Кровсикбибукмарк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3708">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="5fa9d-3709">**\_ chap**: 32-разрядное значение, представляющее маркер главы набора строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3709">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="5fa9d-3710">**Сикдескриптион**: это поле должно содержать структуру типа, обозначенного полем eType.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3710">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="5fa9d-3711">**паддингровс**: длина этого поля должна быть достаточной (от 0 до \_ кбресервед-1 байт) для заполнения поля ROWS \_ значением кбресервед offset с начала сообщения, где \_ кбресервед — это значение в сообщении кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3711">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="5fa9d-3712">Байты заполнения, используемые в этом поле, могут быть любым произвольным значением.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3712">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="5fa9d-3713">Это поле должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3713">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="5fa9d-3714">**Строки**: данные строк форматируются в соответствии со сведениями о столбцах в последнем сообщении кпмсетбиндингсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3714">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="5fa9d-3715">Строки должны храниться в прямом порядке (например, строка 1 перед строкой 2).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3715">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="5fa9d-3716">Столбцы фиксированного размера должны храниться в смещениях, указанных последним сообщением Кпмсетбиндингсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3716">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="5fa9d-3717">Столбцы переменного размера (например, строки) должны храниться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3717">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="5fa9d-3718">Сами данные переменной (например, строка) хранятся ближе к концу буфера в порядке убывания (например, коллекция всех переменных данных для строки 1 находится в конце, строка 2 — в ближайшее и т. д.).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3718">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="5fa9d-3719">Область фиксированного размера (в начале буфера строк) должна содержать Кроввариант для каждого столбца, хранящийся в смещении, указанном в самом последнем сообщении Кпмсетбиндингсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3719">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="5fa9d-3720">Втипе должен содержать тип данных (например, VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3720">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="5fa9d-3721">Если, как определено правилами в начале раздела в этом разделе, используется 32-разрядное смещение, а поле offset в Кроввариант должно содержать 32-разрядное значение, которое является смещением данных переменной от начала сообщения Кпмжетровсаут, плюс значение \_ улклиентбасе, указанное в последнем кпмжетровсин сообщении.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3721">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="5fa9d-3722">Если используются 64-разрядные смещения, поле offset в Кроввариант должно содержать 64-разрядное значение, которое является смещением от начала сообщения Кпмжетровсаут, добавленного к 64-разрядному значению, созданному с помощью \_ улклиентбасе, в качестве младших 32-бит и \_ ulReserved2 в качестве 32 высоких-бит.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3722">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="5fa9d-3723">Например, если в сообщении Кпмсетбиндингсин указано два столбца — size (VT \_ i4) и Title (VT \_ LPWSTR), а \_ улклиентбасе from кпмжетровсин — 0x10000, то две строки будут выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3723">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="5fa9d-3724">Раздел, помеченный серым цветом, является частью буфера фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3724">The section marked in grey is the fixed-length part of the buffer.</span></span>

![Пример сообщения кпмсетбиндингсин](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="5fa9d-3726">2.2.3.17 Кпмратиофинишедин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3726">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="5fa9d-3727">Сообщение Кпмратиофинишедин запрашивает процент завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3727">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="5fa9d-3728">Формат сообщения Кпмратиофинишедин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3728">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3729">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3729">0</span></span>

<span data-ttu-id="5fa9d-3730">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3730">1</span></span>

<span data-ttu-id="5fa9d-3731">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3731">2</span></span>

<span data-ttu-id="5fa9d-3732">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3732">3</span></span>

<span data-ttu-id="5fa9d-3733">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3733">4</span></span>

<span data-ttu-id="5fa9d-3734">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3734">5</span></span>

<span data-ttu-id="5fa9d-3735">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3735">6</span></span>

<span data-ttu-id="5fa9d-3736">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3736">7</span></span>

<span data-ttu-id="5fa9d-3737">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3737">8</span></span>

<span data-ttu-id="5fa9d-3738">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3738">9</span></span>

<span data-ttu-id="5fa9d-3739">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3739">1</span></span><br/> <span data-ttu-id="5fa9d-3740">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3740">0</span></span><br/>

<span data-ttu-id="5fa9d-3741">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3741">1</span></span>

<span data-ttu-id="5fa9d-3742">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3742">2</span></span>

<span data-ttu-id="5fa9d-3743">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3743">3</span></span>

<span data-ttu-id="5fa9d-3744">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3744">4</span></span>

<span data-ttu-id="5fa9d-3745">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3745">5</span></span>

<span data-ttu-id="5fa9d-3746">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3746">6</span></span>

<span data-ttu-id="5fa9d-3747">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3747">7</span></span>

<span data-ttu-id="5fa9d-3748">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3748">8</span></span>

<span data-ttu-id="5fa9d-3749">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3749">9</span></span>

<span data-ttu-id="5fa9d-3750">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3750">2</span></span><br/> <span data-ttu-id="5fa9d-3751">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3751">0</span></span><br/>

<span data-ttu-id="5fa9d-3752">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3752">1</span></span>

<span data-ttu-id="5fa9d-3753">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3753">2</span></span>

<span data-ttu-id="5fa9d-3754">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3754">3</span></span>

<span data-ttu-id="5fa9d-3755">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3755">4</span></span>

<span data-ttu-id="5fa9d-3756">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3756">5</span></span>

<span data-ttu-id="5fa9d-3757">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3757">6</span></span>

<span data-ttu-id="5fa9d-3758">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3758">7</span></span>

<span data-ttu-id="5fa9d-3759">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3759">8</span></span>

<span data-ttu-id="5fa9d-3760">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3760">9</span></span>

<span data-ttu-id="5fa9d-3761">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3761">3</span></span><br/> <span data-ttu-id="5fa9d-3762">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3762">0</span></span><br/>

<span data-ttu-id="5fa9d-3763">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3763">1</span></span>

<span data-ttu-id="5fa9d-3764">\_хкурсор</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3764">\_hCursor</span></span>

<span data-ttu-id="5fa9d-3765">\_фкуикк</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3765">\_fQuick</span></span>



 

<span data-ttu-id="5fa9d-3766">**\_ хкурсор**: маркер из сообщения кпмкреатекуерйоут, идентифицирующего запрос, для которого запрашиваются сведения о завершении.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3766">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="5fa9d-3767">**\_ фкуикк**: необходимо задать значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3767">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="5fa9d-3768">Не используется и должен игнорироваться сервером.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3768">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="5fa9d-3769">2.2.3.18 Кпмратиофинишедаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3769">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="5fa9d-3770">Сообщение Кпмратиофинишедаут отвечает на сообщение Кпмратиофинишедин с коэффициентом завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3770">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="5fa9d-3771">Формат сообщения Кпмратиофинишедаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3771">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3772">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3772">0</span></span>

<span data-ttu-id="5fa9d-3773">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3773">1</span></span>

<span data-ttu-id="5fa9d-3774">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3774">2</span></span>

<span data-ttu-id="5fa9d-3775">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3775">3</span></span>

<span data-ttu-id="5fa9d-3776">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3776">4</span></span>

<span data-ttu-id="5fa9d-3777">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3777">5</span></span>

<span data-ttu-id="5fa9d-3778">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3778">6</span></span>

<span data-ttu-id="5fa9d-3779">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3779">7</span></span>

<span data-ttu-id="5fa9d-3780">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3780">8</span></span>

<span data-ttu-id="5fa9d-3781">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3781">9</span></span>

<span data-ttu-id="5fa9d-3782">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3782">1</span></span><br/> <span data-ttu-id="5fa9d-3783">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3783">0</span></span><br/>

<span data-ttu-id="5fa9d-3784">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3784">1</span></span>

<span data-ttu-id="5fa9d-3785">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3785">2</span></span>

<span data-ttu-id="5fa9d-3786">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3786">3</span></span>

<span data-ttu-id="5fa9d-3787">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3787">4</span></span>

<span data-ttu-id="5fa9d-3788">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3788">5</span></span>

<span data-ttu-id="5fa9d-3789">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3789">6</span></span>

<span data-ttu-id="5fa9d-3790">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3790">7</span></span>

<span data-ttu-id="5fa9d-3791">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3791">8</span></span>

<span data-ttu-id="5fa9d-3792">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3792">9</span></span>

<span data-ttu-id="5fa9d-3793">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3793">2</span></span><br/> <span data-ttu-id="5fa9d-3794">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3794">0</span></span><br/>

<span data-ttu-id="5fa9d-3795">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3795">1</span></span>

<span data-ttu-id="5fa9d-3796">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3796">2</span></span>

<span data-ttu-id="5fa9d-3797">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3797">3</span></span>

<span data-ttu-id="5fa9d-3798">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3798">4</span></span>

<span data-ttu-id="5fa9d-3799">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3799">5</span></span>

<span data-ttu-id="5fa9d-3800">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3800">6</span></span>

<span data-ttu-id="5fa9d-3801">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3801">7</span></span>

<span data-ttu-id="5fa9d-3802">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3802">8</span></span>

<span data-ttu-id="5fa9d-3803">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3803">9</span></span>

<span data-ttu-id="5fa9d-3804">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3804">3</span></span><br/> <span data-ttu-id="5fa9d-3805">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3805">0</span></span><br/>

<span data-ttu-id="5fa9d-3806">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3806">1</span></span>

<span data-ttu-id="5fa9d-3807">\_ улнумератор</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3807">\_ ulNumerator</span></span>

<span data-ttu-id="5fa9d-3808">\_улденоминатор</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3808">\_ulDenominator</span></span>

<span data-ttu-id="5fa9d-3809">\_cRows</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3809">\_cRows</span></span>

<span data-ttu-id="5fa9d-3810">\_фневровс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3810">\_fNewRows</span></span>



 

<span data-ttu-id="5fa9d-3811">**\_ улнумератор**: 32-битовое целое число без знака, указывающее числитель коэффициента завершения в терминах строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3811">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="5fa9d-3812">**\_ улденоминатор**: 32-битовое целое число без знака, указывающее знаменатель коэффициента завершения в терминах строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3812">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="5fa9d-3813">ДОЛЖНО быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3813">MUST be greater than zero.</span></span>

<span data-ttu-id="5fa9d-3814">**\_ crowset**: 32-разрядное целое число без знака, указывающее общее количество строк для запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3814">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="5fa9d-3815">**\_ фневровс**: логическое значение, указывающее, доступны ли новые строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3815">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="5fa9d-3816">Значение 0x00000001 указывает, что новые строки доступны в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3816">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="5fa9d-3817">Значение 0x00000000 указывает, что набор строк не содержит новых строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3817">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="5fa9d-3818">Для этого поля не должны быть заданы другие значения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3818">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="5fa9d-3819">2.2.3.19 Кпмфетчвалуеин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3819">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="5fa9d-3820">Сообщение Кпмфетчвалуеин запрашивает значение свойства, которое слишком велико для возвращения в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3820">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="5fa9d-3821">Как указано в разделе 3.2.4.2.5, это сообщение отправляется повторно для получения всех байтов свойства, обновляя \_ кбсофар для каждого, пока \_ поле Фмориксистс сообщения кпмфетчвалуеаут не будет установлено в **значение false**.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3821">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="5fa9d-3822">Формат сообщения Кпмфетчвалуеин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3822">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3823">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3823">0</span></span>

<span data-ttu-id="5fa9d-3824">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3824">1</span></span>

<span data-ttu-id="5fa9d-3825">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3825">2</span></span>

<span data-ttu-id="5fa9d-3826">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3826">3</span></span>

<span data-ttu-id="5fa9d-3827">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3827">4</span></span>

<span data-ttu-id="5fa9d-3828">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3828">5</span></span>

<span data-ttu-id="5fa9d-3829">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3829">6</span></span>

<span data-ttu-id="5fa9d-3830">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3830">7</span></span>

<span data-ttu-id="5fa9d-3831">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3831">8</span></span>

<span data-ttu-id="5fa9d-3832">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3832">9</span></span>

<span data-ttu-id="5fa9d-3833">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3833">1</span></span><br/> <span data-ttu-id="5fa9d-3834">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3834">0</span></span><br/>

<span data-ttu-id="5fa9d-3835">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3835">1</span></span>

<span data-ttu-id="5fa9d-3836">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3836">2</span></span>

<span data-ttu-id="5fa9d-3837">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3837">3</span></span>

<span data-ttu-id="5fa9d-3838">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3838">4</span></span>

<span data-ttu-id="5fa9d-3839">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3839">5</span></span>

<span data-ttu-id="5fa9d-3840">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3840">6</span></span>

<span data-ttu-id="5fa9d-3841">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3841">7</span></span>

<span data-ttu-id="5fa9d-3842">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3842">8</span></span>

<span data-ttu-id="5fa9d-3843">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3843">9</span></span>

<span data-ttu-id="5fa9d-3844">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3844">2</span></span><br/> <span data-ttu-id="5fa9d-3845">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3845">0</span></span><br/>

<span data-ttu-id="5fa9d-3846">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3846">1</span></span>

<span data-ttu-id="5fa9d-3847">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3847">2</span></span>

<span data-ttu-id="5fa9d-3848">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3848">3</span></span>

<span data-ttu-id="5fa9d-3849">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3849">4</span></span>

<span data-ttu-id="5fa9d-3850">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3850">5</span></span>

<span data-ttu-id="5fa9d-3851">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3851">6</span></span>

<span data-ttu-id="5fa9d-3852">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3852">7</span></span>

<span data-ttu-id="5fa9d-3853">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3853">8</span></span>

<span data-ttu-id="5fa9d-3854">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3854">9</span></span>

<span data-ttu-id="5fa9d-3855">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3855">3</span></span><br/> <span data-ttu-id="5fa9d-3856">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3856">0</span></span><br/>

<span data-ttu-id="5fa9d-3857">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3857">1</span></span>

<span data-ttu-id="5fa9d-3858">\_WID</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3858">\_wid</span></span>

<span data-ttu-id="5fa9d-3859">\_кбсофар</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3859">\_cbSoFar</span></span>

<span data-ttu-id="5fa9d-3860">\_кбпропспек</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3860">\_cbPropSpec</span></span>

<span data-ttu-id="5fa9d-3861">\_кбчунк</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3861">\_cbChunk</span></span>

<span data-ttu-id="5fa9d-3862">Пропспек (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3862">PropSpec (variable)</span></span>

<span data-ttu-id="5fa9d-3863">...</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3863">...</span></span>

<span data-ttu-id="5fa9d-3864">\_Заполнение (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3864">\_padding (variable)</span></span>



 

<span data-ttu-id="5fa9d-3865">**\_ wid**: 32-разрядное целое число без знака, представляющее идентификатор документа, определяющий документ, для которого должно быть выбрано свойство.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3865">**\_wid**: A 32-bit unsigned integer representing the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="5fa9d-3866">**\_ кбсофар**: 32-разрядное целое число без знака, содержащее число байтов, ранее переданных для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3866">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="5fa9d-3867">В первом сообщении должно быть задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3867">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="5fa9d-3868">**\_ кбпропспек**: 32-разрядное целое число без знака, содержащее размер поля пропспек в байтах.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3868">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="5fa9d-3869">**\_ кбчунк**: 32-разрядное целое число без знака, содержащее максимальное число байтов, которое отправитель может принимать в сообщении кпмфетчвалуеаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3869">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="5fa9d-3870">*Поведение Windows: для этого поля задано значение 0x00004000 для всех версий Windows.*</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3870">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="5fa9d-3871">**Пропспек**: структура кфуллпропспек, указывающая извлекаемое свойство.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3871">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="5fa9d-3872">**\_ Заполнение**: это поле должно иметь длину, необходимую (от 0 до 3 байт), для размещения сообщения до нескольких 4 байт.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3872">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="5fa9d-3873">Значение заполнения байтов может быть любым произвольным значением.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3873">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="5fa9d-3874">Это поле должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3874">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="5fa9d-3875">2.2.3.20 Кпмфетчвалуеаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3875">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="5fa9d-3876">Сообщение Кпмфетчвалуеаут отвечает на сообщение Кпмфетчвалуеин со значением свойства из предыдущего запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3876">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="5fa9d-3877">Как указано в разделе 3.1.5.2.8, это сообщение отправляется после каждого сообщения Кпмфетчвалуеин до тех пор, пока не будут переданы все байты свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3877">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="5fa9d-3878">Формат сообщения Кпмфетчвалуеаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3878">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3879">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3879">0</span></span>

<span data-ttu-id="5fa9d-3880">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3880">1</span></span>

<span data-ttu-id="5fa9d-3881">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3881">2</span></span>

<span data-ttu-id="5fa9d-3882">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3882">3</span></span>

<span data-ttu-id="5fa9d-3883">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3883">4</span></span>

<span data-ttu-id="5fa9d-3884">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3884">5</span></span>

<span data-ttu-id="5fa9d-3885">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3885">6</span></span>

<span data-ttu-id="5fa9d-3886">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3886">7</span></span>

<span data-ttu-id="5fa9d-3887">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3887">8</span></span>

<span data-ttu-id="5fa9d-3888">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3888">9</span></span>

<span data-ttu-id="5fa9d-3889">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3889">1</span></span><br/> <span data-ttu-id="5fa9d-3890">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3890">0</span></span><br/>

<span data-ttu-id="5fa9d-3891">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3891">1</span></span>

<span data-ttu-id="5fa9d-3892">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3892">2</span></span>

<span data-ttu-id="5fa9d-3893">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3893">3</span></span>

<span data-ttu-id="5fa9d-3894">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3894">4</span></span>

<span data-ttu-id="5fa9d-3895">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3895">5</span></span>

<span data-ttu-id="5fa9d-3896">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3896">6</span></span>

<span data-ttu-id="5fa9d-3897">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3897">7</span></span>

<span data-ttu-id="5fa9d-3898">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3898">8</span></span>

<span data-ttu-id="5fa9d-3899">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3899">9</span></span>

<span data-ttu-id="5fa9d-3900">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3900">2</span></span><br/> <span data-ttu-id="5fa9d-3901">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3901">0</span></span><br/>

<span data-ttu-id="5fa9d-3902">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3902">1</span></span>

<span data-ttu-id="5fa9d-3903">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3903">2</span></span>

<span data-ttu-id="5fa9d-3904">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3904">3</span></span>

<span data-ttu-id="5fa9d-3905">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3905">4</span></span>

<span data-ttu-id="5fa9d-3906">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3906">5</span></span>

<span data-ttu-id="5fa9d-3907">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3907">6</span></span>

<span data-ttu-id="5fa9d-3908">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3908">7</span></span>

<span data-ttu-id="5fa9d-3909">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3909">8</span></span>

<span data-ttu-id="5fa9d-3910">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3910">9</span></span>

<span data-ttu-id="5fa9d-3911">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3911">3</span></span><br/> <span data-ttu-id="5fa9d-3912">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3912">0</span></span><br/>

<span data-ttu-id="5fa9d-3913">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3913">1</span></span>

<span data-ttu-id="5fa9d-3914">\_кбвалуе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3914">\_cbValue</span></span>

<span data-ttu-id="5fa9d-3915">\_фмориксистс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3915">\_fMoreExists</span></span>

<span data-ttu-id="5fa9d-3916">\_фвалуиксистс</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3916">\_fValueExists</span></span>

<span data-ttu-id="5fa9d-3917">втипе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3917">vType</span></span>

<span data-ttu-id="5fa9d-3918">Управляемое vValue (переменная)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3918">vValue (variable)</span></span>



 

<span data-ttu-id="5fa9d-3919">**\_ кбвалуе**: 32-разрядное целое число без знака, содержащее общий размер в байтах в управляемое vValue.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3919">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="5fa9d-3920">**\_ фмориксистс**: логическое значение, указывающее, доступны ли дополнительные сообщения кпмфетчвалуеаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3920">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="5fa9d-3921">Если задано значение 0x00000001, то существуют дополнительные сообщения Кпмфетчвалуеаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3921">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="5fa9d-3922">Если задано значение 0x00000000, дополнительные сообщения Кпмфетчвалуеаут недоступны.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3922">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="5fa9d-3923">**\_ фвалуиксистс**: логическое значение, указывающее, имеется ли значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3923">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="5fa9d-3924">Если задано значение 0x00000001, то свойство существует.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3924">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="5fa9d-3925">Если задано 0x00000000, значение свойства не существует.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3925">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="5fa9d-3926">**втипе**. значение из перечисления VARENUM. Дополнительные сведения см. в разделе 2.2.1.1, описывающем тип свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3926">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="5fa9d-3927">**управляемое vValue**: часть массива байтов, содержащая структуру сериализедпропертивалуе, как указано в разделе 2.2.1.32, где смещение начала части является значением \_ кбсофар в кпмфетчвалуеин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3927">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="5fa9d-3928">Длина части, обозначенной \_ полем кбвалуе, должна быть равна значению \_ Кбчунк в кпмфетчвалуеин, если \_ фмориксистс имеет значение 0X00000001, и должно быть меньше или равно значению \_ кбчунк в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3928">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="5fa9d-3929">2.2.3.21 Кпмжетнотифи</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3929">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="5fa9d-3930">Сообщение Кпмжетнотифи запрашивает, что клиент хочет получать уведомления об изменениях набора строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3930">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="5fa9d-3931">Сообщение не должно включать текст. будет отправлен только заголовок сообщения, как указано в разделе 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3931">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="5fa9d-3932">2.2.3.22 Кпмсенднотифйоут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3932">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="5fa9d-3933">Сообщение Кпмсенднотифйоут уведомляет клиента об изменении результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3933">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="5fa9d-3934">Это сообщение отправляется, только когда происходит изменение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3934">This message is only sent when a change occurs.</span></span> <span data-ttu-id="5fa9d-3935">Формат сообщения Кпмсенднотифйоут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3935">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3936">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3936">0</span></span>

<span data-ttu-id="5fa9d-3937">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3937">1</span></span>

<span data-ttu-id="5fa9d-3938">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3938">2</span></span>

<span data-ttu-id="5fa9d-3939">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3939">3</span></span>

<span data-ttu-id="5fa9d-3940">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3940">4</span></span>

<span data-ttu-id="5fa9d-3941">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3941">5</span></span>

<span data-ttu-id="5fa9d-3942">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3942">6</span></span>

<span data-ttu-id="5fa9d-3943">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3943">7</span></span>

<span data-ttu-id="5fa9d-3944">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3944">8</span></span>

<span data-ttu-id="5fa9d-3945">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3945">9</span></span>

<span data-ttu-id="5fa9d-3946">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3946">1</span></span><br/> <span data-ttu-id="5fa9d-3947">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3947">0</span></span><br/>

<span data-ttu-id="5fa9d-3948">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3948">1</span></span>

<span data-ttu-id="5fa9d-3949">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3949">2</span></span>

<span data-ttu-id="5fa9d-3950">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3950">3</span></span>

<span data-ttu-id="5fa9d-3951">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3951">4</span></span>

<span data-ttu-id="5fa9d-3952">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3952">5</span></span>

<span data-ttu-id="5fa9d-3953">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3953">6</span></span>

<span data-ttu-id="5fa9d-3954">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3954">7</span></span>

<span data-ttu-id="5fa9d-3955">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3955">8</span></span>

<span data-ttu-id="5fa9d-3956">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3956">9</span></span>

<span data-ttu-id="5fa9d-3957">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3957">2</span></span><br/> <span data-ttu-id="5fa9d-3958">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3958">0</span></span><br/>

<span data-ttu-id="5fa9d-3959">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3959">1</span></span>

<span data-ttu-id="5fa9d-3960">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3960">2</span></span>

<span data-ttu-id="5fa9d-3961">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3961">3</span></span>

<span data-ttu-id="5fa9d-3962">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3962">4</span></span>

<span data-ttu-id="5fa9d-3963">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3963">5</span></span>

<span data-ttu-id="5fa9d-3964">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3964">6</span></span>

<span data-ttu-id="5fa9d-3965">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3965">7</span></span>

<span data-ttu-id="5fa9d-3966">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3966">8</span></span>

<span data-ttu-id="5fa9d-3967">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3967">9</span></span>

<span data-ttu-id="5fa9d-3968">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3968">3</span></span><br/> <span data-ttu-id="5fa9d-3969">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3969">0</span></span><br/>

<span data-ttu-id="5fa9d-3970">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3970">1</span></span>

<span data-ttu-id="5fa9d-3971">\_ватчнотифи</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3971">\_watchNotify</span></span>



 

<span data-ttu-id="5fa9d-3972">**\_ ватчнотифи**: изменение запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3972">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="5fa9d-3973">Оно должно иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3973">It MUST be one of the following values:</span></span>



| <span data-ttu-id="5fa9d-3974">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3974">Value</span></span>                                     | <span data-ttu-id="5fa9d-3975">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3975">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="5fa9d-3976">ДБВАТЧНОТИФИ \_ ровсчанжед 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3976">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="5fa9d-3977">Изменилось число строк в наборе строк запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3977">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="5fa9d-3978">ДБВАТЧНОТИФИ \_ куеридоне 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3978">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="5fa9d-3979">Запрос завершен.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3979">The query has completed.</span></span>                            |
| <span data-ttu-id="5fa9d-3980">ДБВАТЧНОТИФИ \_ куеририксекутед 0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3980">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="5fa9d-3981">Запрос был повторно выполнен.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3981">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="5fa9d-3982">2.2.3.23 Кпмжетаппроксиматепоситионин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3982">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="5fa9d-3983">Сообщение Кпмжетаппроксиматепоситионин запрашивает приблизительное расположение закладки в главе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3983">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="5fa9d-3984">Формат сообщения Кпмжетаппроксиматепоситионин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3984">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-3985">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3985">0</span></span>

<span data-ttu-id="5fa9d-3986">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3986">1</span></span>

<span data-ttu-id="5fa9d-3987">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3987">2</span></span>

<span data-ttu-id="5fa9d-3988">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3988">3</span></span>

<span data-ttu-id="5fa9d-3989">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3989">4</span></span>

<span data-ttu-id="5fa9d-3990">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3990">5</span></span>

<span data-ttu-id="5fa9d-3991">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3991">6</span></span>

<span data-ttu-id="5fa9d-3992">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3992">7</span></span>

<span data-ttu-id="5fa9d-3993">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3993">8</span></span>

<span data-ttu-id="5fa9d-3994">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3994">9</span></span>

<span data-ttu-id="5fa9d-3995">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3995">1</span></span><br/> <span data-ttu-id="5fa9d-3996">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3996">0</span></span><br/>

<span data-ttu-id="5fa9d-3997">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3997">1</span></span>

<span data-ttu-id="5fa9d-3998">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3998">2</span></span>

<span data-ttu-id="5fa9d-3999">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-3999">3</span></span>

<span data-ttu-id="5fa9d-4000">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4000">4</span></span>

<span data-ttu-id="5fa9d-4001">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4001">5</span></span>

<span data-ttu-id="5fa9d-4002">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4002">6</span></span>

<span data-ttu-id="5fa9d-4003">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4003">7</span></span>

<span data-ttu-id="5fa9d-4004">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4004">8</span></span>

<span data-ttu-id="5fa9d-4005">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4005">9</span></span>

<span data-ttu-id="5fa9d-4006">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4006">2</span></span><br/> <span data-ttu-id="5fa9d-4007">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4007">0</span></span><br/>

<span data-ttu-id="5fa9d-4008">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4008">1</span></span>

<span data-ttu-id="5fa9d-4009">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4009">2</span></span>

<span data-ttu-id="5fa9d-4010">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4010">3</span></span>

<span data-ttu-id="5fa9d-4011">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4011">4</span></span>

<span data-ttu-id="5fa9d-4012">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4012">5</span></span>

<span data-ttu-id="5fa9d-4013">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4013">6</span></span>

<span data-ttu-id="5fa9d-4014">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4014">7</span></span>

<span data-ttu-id="5fa9d-4015">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4015">8</span></span>

<span data-ttu-id="5fa9d-4016">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4016">9</span></span>

<span data-ttu-id="5fa9d-4017">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4017">3</span></span><br/> <span data-ttu-id="5fa9d-4018">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4018">0</span></span><br/>

<span data-ttu-id="5fa9d-4019">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4019">1</span></span>

<span data-ttu-id="5fa9d-4020">\_хкурсор</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4020">\_hCursor</span></span>

<span data-ttu-id="5fa9d-4021">\_Протокол CHAP</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4021">\_chapt</span></span>

<span data-ttu-id="5fa9d-4022">\_бмк</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4022">\_bmk</span></span>



 

<span data-ttu-id="5fa9d-4023">**\_ хкурсор**: 32-разрядное значение, представляющее курсор запроса, полученный из кпмкреатекуерйоут для набора строк, содержащего закладку.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4023">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="5fa9d-4024">**\_ chap**: 32-разрядное значение, представляющее маркер раздела, содержащего закладку.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4024">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="5fa9d-4025">**\_ бмк**: 32-разрядное значение, представляющее маркер закладки, для которой необходимо получить приблизительную точку.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4025">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="5fa9d-4026">2.2.3.24 Кпмжетаппроксиматепоситионаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4026">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="5fa9d-4027">Сообщение Кпмжетаппроксиматепоситионаут отвечает на сообщение Кпмжетаппроксиматепоситионин, описывающее примерное расположение закладки в главе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4027">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="5fa9d-4028">Формат сообщения Кпмжетаппроксиматепоситионаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4028">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-4029">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4029">0</span></span>

<span data-ttu-id="5fa9d-4030">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4030">1</span></span>

<span data-ttu-id="5fa9d-4031">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4031">2</span></span>

<span data-ttu-id="5fa9d-4032">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4032">3</span></span>

<span data-ttu-id="5fa9d-4033">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4033">4</span></span>

<span data-ttu-id="5fa9d-4034">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4034">5</span></span>

<span data-ttu-id="5fa9d-4035">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4035">6</span></span>

<span data-ttu-id="5fa9d-4036">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4036">7</span></span>

<span data-ttu-id="5fa9d-4037">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4037">8</span></span>

<span data-ttu-id="5fa9d-4038">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4038">9</span></span>

<span data-ttu-id="5fa9d-4039">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4039">1</span></span><br/> <span data-ttu-id="5fa9d-4040">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4040">0</span></span><br/>

<span data-ttu-id="5fa9d-4041">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4041">1</span></span>

<span data-ttu-id="5fa9d-4042">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4042">2</span></span>

<span data-ttu-id="5fa9d-4043">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4043">3</span></span>

<span data-ttu-id="5fa9d-4044">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4044">4</span></span>

<span data-ttu-id="5fa9d-4045">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4045">5</span></span>

<span data-ttu-id="5fa9d-4046">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4046">6</span></span>

<span data-ttu-id="5fa9d-4047">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4047">7</span></span>

<span data-ttu-id="5fa9d-4048">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4048">8</span></span>

<span data-ttu-id="5fa9d-4049">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4049">9</span></span>

<span data-ttu-id="5fa9d-4050">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4050">2</span></span><br/> <span data-ttu-id="5fa9d-4051">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4051">0</span></span><br/>

<span data-ttu-id="5fa9d-4052">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4052">1</span></span>

<span data-ttu-id="5fa9d-4053">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4053">2</span></span>

<span data-ttu-id="5fa9d-4054">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4054">3</span></span>

<span data-ttu-id="5fa9d-4055">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4055">4</span></span>

<span data-ttu-id="5fa9d-4056">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4056">5</span></span>

<span data-ttu-id="5fa9d-4057">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4057">6</span></span>

<span data-ttu-id="5fa9d-4058">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4058">7</span></span>

<span data-ttu-id="5fa9d-4059">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4059">8</span></span>

<span data-ttu-id="5fa9d-4060">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4060">9</span></span>

<span data-ttu-id="5fa9d-4061">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4061">3</span></span><br/> <span data-ttu-id="5fa9d-4062">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4062">0</span></span><br/>

<span data-ttu-id="5fa9d-4063">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4063">1</span></span>

<span data-ttu-id="5fa9d-4064">\_numerator</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4064">\_numerator</span></span>

<span data-ttu-id="5fa9d-4065">\_denominator</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4065">\_denominator</span></span>



 

<span data-ttu-id="5fa9d-4066">**\_ числитель**: 32-разрядное целое число без знака, содержащее номер строки закладки в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4066">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="5fa9d-4067">Если строки отсутствуют, это поле должно иметь значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4067">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="5fa9d-4068">**\_ знаменатель**: 32-битовое целое число без знака, содержащее количество строк в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4068">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="5fa9d-4069">2.2.3.25 Кпмкомпаребмкин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4069">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="5fa9d-4070">Сообщение Кпмкомпаребмкин запрашивает сравнение двух закладок в главе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4070">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="5fa9d-4071">Формат сообщения Кпмкомпаребмкин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4071">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-4072">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4072">0</span></span>

<span data-ttu-id="5fa9d-4073">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4073">1</span></span>

<span data-ttu-id="5fa9d-4074">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4074">2</span></span>

<span data-ttu-id="5fa9d-4075">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4075">3</span></span>

<span data-ttu-id="5fa9d-4076">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4076">4</span></span>

<span data-ttu-id="5fa9d-4077">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4077">5</span></span>

<span data-ttu-id="5fa9d-4078">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4078">6</span></span>

<span data-ttu-id="5fa9d-4079">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4079">7</span></span>

<span data-ttu-id="5fa9d-4080">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4080">8</span></span>

<span data-ttu-id="5fa9d-4081">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4081">9</span></span>

<span data-ttu-id="5fa9d-4082">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4082">1</span></span><br/> <span data-ttu-id="5fa9d-4083">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4083">0</span></span><br/>

<span data-ttu-id="5fa9d-4084">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4084">1</span></span>

<span data-ttu-id="5fa9d-4085">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4085">2</span></span>

<span data-ttu-id="5fa9d-4086">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4086">3</span></span>

<span data-ttu-id="5fa9d-4087">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4087">4</span></span>

<span data-ttu-id="5fa9d-4088">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4088">5</span></span>

<span data-ttu-id="5fa9d-4089">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4089">6</span></span>

<span data-ttu-id="5fa9d-4090">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4090">7</span></span>

<span data-ttu-id="5fa9d-4091">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4091">8</span></span>

<span data-ttu-id="5fa9d-4092">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4092">9</span></span>

<span data-ttu-id="5fa9d-4093">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4093">2</span></span><br/> <span data-ttu-id="5fa9d-4094">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4094">0</span></span><br/>

<span data-ttu-id="5fa9d-4095">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4095">1</span></span>

<span data-ttu-id="5fa9d-4096">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4096">2</span></span>

<span data-ttu-id="5fa9d-4097">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4097">3</span></span>

<span data-ttu-id="5fa9d-4098">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4098">4</span></span>

<span data-ttu-id="5fa9d-4099">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4099">5</span></span>

<span data-ttu-id="5fa9d-4100">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4100">6</span></span>

<span data-ttu-id="5fa9d-4101">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4101">7</span></span>

<span data-ttu-id="5fa9d-4102">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4102">8</span></span>

<span data-ttu-id="5fa9d-4103">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4103">9</span></span>

<span data-ttu-id="5fa9d-4104">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4104">3</span></span><br/> <span data-ttu-id="5fa9d-4105">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4105">0</span></span><br/>

<span data-ttu-id="5fa9d-4106">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4106">1</span></span>

<span data-ttu-id="5fa9d-4107">\_хкурсор</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4107">\_hCursor</span></span>

<span data-ttu-id="5fa9d-4108">\_Протокол CHAP</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4108">\_chapt</span></span>

<span data-ttu-id="5fa9d-4109">\_бмкфирст</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4109">\_bmkFirst</span></span>

<span data-ttu-id="5fa9d-4110">\_бмксеконд</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4110">\_bmkSecond</span></span>



 

<span data-ttu-id="5fa9d-4111">\_**хкурсор**: 32-разрядное значение, представляющее собой маркер из сообщения кпмкреатекуерйоут для набора строк, содержащего закладки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4111">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="5fa9d-4112">\_**CHAP**: 32-разрядное значение, представляющее маркер главы, содержащей закладки для сравнения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4112">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="5fa9d-4113">\_**бмкфирст**: 32-разрядное значение, представляющее маркер первой закладки для сравнения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4113">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="5fa9d-4114">\_**бмксеконд**: 32-разрядное значение, представляющее маркер для сравнения с второй закладкой.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4114">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="5fa9d-4115">2.2.3.26 Кпмкомпаребмкаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4115">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="5fa9d-4116">Сообщение Кпмкомпаребмкаут отвечает на сообщение Кпмкомпаребмкин с использованием сравнения двух закладок в главе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4116">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="5fa9d-4117">Формат сообщения Кпмкомпаребмкаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4117">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-4118">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4118">0</span></span>

<span data-ttu-id="5fa9d-4119">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4119">1</span></span>

<span data-ttu-id="5fa9d-4120">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4120">2</span></span>

<span data-ttu-id="5fa9d-4121">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4121">3</span></span>

<span data-ttu-id="5fa9d-4122">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4122">4</span></span>

<span data-ttu-id="5fa9d-4123">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4123">5</span></span>

<span data-ttu-id="5fa9d-4124">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4124">6</span></span>

<span data-ttu-id="5fa9d-4125">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4125">7</span></span>

<span data-ttu-id="5fa9d-4126">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4126">8</span></span>

<span data-ttu-id="5fa9d-4127">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4127">9</span></span>

<span data-ttu-id="5fa9d-4128">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4128">1</span></span><br/> <span data-ttu-id="5fa9d-4129">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4129">0</span></span><br/>

<span data-ttu-id="5fa9d-4130">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4130">1</span></span>

<span data-ttu-id="5fa9d-4131">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4131">2</span></span>

<span data-ttu-id="5fa9d-4132">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4132">3</span></span>

<span data-ttu-id="5fa9d-4133">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4133">4</span></span>

<span data-ttu-id="5fa9d-4134">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4134">5</span></span>

<span data-ttu-id="5fa9d-4135">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4135">6</span></span>

<span data-ttu-id="5fa9d-4136">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4136">7</span></span>

<span data-ttu-id="5fa9d-4137">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4137">8</span></span>

<span data-ttu-id="5fa9d-4138">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4138">9</span></span>

<span data-ttu-id="5fa9d-4139">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4139">2</span></span><br/> <span data-ttu-id="5fa9d-4140">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4140">0</span></span><br/>

<span data-ttu-id="5fa9d-4141">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4141">1</span></span>

<span data-ttu-id="5fa9d-4142">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4142">2</span></span>

<span data-ttu-id="5fa9d-4143">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4143">3</span></span>

<span data-ttu-id="5fa9d-4144">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4144">4</span></span>

<span data-ttu-id="5fa9d-4145">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4145">5</span></span>

<span data-ttu-id="5fa9d-4146">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4146">6</span></span>

<span data-ttu-id="5fa9d-4147">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4147">7</span></span>

<span data-ttu-id="5fa9d-4148">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4148">8</span></span>

<span data-ttu-id="5fa9d-4149">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4149">9</span></span>

<span data-ttu-id="5fa9d-4150">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4150">3</span></span><br/> <span data-ttu-id="5fa9d-4151">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4151">0</span></span><br/>

<span data-ttu-id="5fa9d-4152">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4152">1</span></span>

<span data-ttu-id="5fa9d-4153">\_двкомпарисон</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4153">\_dwComparison</span></span>



 

<span data-ttu-id="5fa9d-4154">\_**двкомпарисон**: одно из следующих значений, указывающее относительное положение двух закладок в главе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4154">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="5fa9d-4155">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4155">Value</span></span>                               | <span data-ttu-id="5fa9d-4156">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4156">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-4157">ДБКОМПАРЕ \_ lt 0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4157">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="5fa9d-4158">Первая закладка располагается перед второй.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4158">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="5fa9d-4159">ДБКОМПАРЕ \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4159">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="5fa9d-4160">Первая закладка имеет ту же самую точку, что и вторая.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4160">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="5fa9d-4161">ДБКОМПАРЕ \_ gt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4161">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="5fa9d-4162">Первая закладка размещается после второй.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4162">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="5fa9d-4163">ДБКОМПАРЕ \_ Ne 0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4163">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="5fa9d-4164">Первая закладка не совпадает с позицией второго.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4164">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="5fa9d-4165">ДБКОМПАРЕ \_ ноткомпарабле 0x00000004</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4165">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="5fa9d-4166">Первая закладка не сравнима со вторым.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4166">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="5fa9d-4167">2.2.3.27 Кпмрестартпоситионин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4167">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="5fa9d-4168">Сообщение Кпмрестартпоситионин перемещает позицию выборки для курсора в начало главы.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4168">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="5fa9d-4169">Как указано в разделе 3.1.5.2.12, сервер будет отвечать с помощью того же сообщения, а результаты запроса содержатся в \_ поле Status заголовка CISP.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4169">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="5fa9d-4170">Формат сообщения Кпмрестартпоситионин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4170">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-4171">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4171">0</span></span>

<span data-ttu-id="5fa9d-4172">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4172">1</span></span>

<span data-ttu-id="5fa9d-4173">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4173">2</span></span>

<span data-ttu-id="5fa9d-4174">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4174">3</span></span>

<span data-ttu-id="5fa9d-4175">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4175">4</span></span>

<span data-ttu-id="5fa9d-4176">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4176">5</span></span>

<span data-ttu-id="5fa9d-4177">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4177">6</span></span>

<span data-ttu-id="5fa9d-4178">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4178">7</span></span>

<span data-ttu-id="5fa9d-4179">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4179">8</span></span>

<span data-ttu-id="5fa9d-4180">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4180">9</span></span>

<span data-ttu-id="5fa9d-4181">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4181">1</span></span><br/> <span data-ttu-id="5fa9d-4182">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4182">0</span></span><br/>

<span data-ttu-id="5fa9d-4183">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4183">1</span></span>

<span data-ttu-id="5fa9d-4184">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4184">2</span></span>

<span data-ttu-id="5fa9d-4185">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4185">3</span></span>

<span data-ttu-id="5fa9d-4186">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4186">4</span></span>

<span data-ttu-id="5fa9d-4187">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4187">5</span></span>

<span data-ttu-id="5fa9d-4188">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4188">6</span></span>

<span data-ttu-id="5fa9d-4189">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4189">7</span></span>

<span data-ttu-id="5fa9d-4190">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4190">8</span></span>

<span data-ttu-id="5fa9d-4191">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4191">9</span></span>

<span data-ttu-id="5fa9d-4192">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4192">2</span></span><br/> <span data-ttu-id="5fa9d-4193">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4193">0</span></span><br/>

<span data-ttu-id="5fa9d-4194">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4194">1</span></span>

<span data-ttu-id="5fa9d-4195">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4195">2</span></span>

<span data-ttu-id="5fa9d-4196">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4196">3</span></span>

<span data-ttu-id="5fa9d-4197">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4197">4</span></span>

<span data-ttu-id="5fa9d-4198">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4198">5</span></span>

<span data-ttu-id="5fa9d-4199">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4199">6</span></span>

<span data-ttu-id="5fa9d-4200">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4200">7</span></span>

<span data-ttu-id="5fa9d-4201">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4201">8</span></span>

<span data-ttu-id="5fa9d-4202">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4202">9</span></span>

<span data-ttu-id="5fa9d-4203">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4203">3</span></span><br/> <span data-ttu-id="5fa9d-4204">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4204">0</span></span><br/>

<span data-ttu-id="5fa9d-4205">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4205">1</span></span>

<span data-ttu-id="5fa9d-4206">\_Хкурсор (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4206">\_hCursor (optional)</span></span>

<span data-ttu-id="5fa9d-4207">\_CHAP (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4207">\_chapt (optional)</span></span>



 

<span data-ttu-id="5fa9d-4208">**\_ хкурсор**: 32-разрядное значение, представляющее маркер, полученное из сообщения кпмкреатекуерйоут, которое определяет запрос, для которого нужно перезапустить эту точку.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4208">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="5fa9d-4209">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4209">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="5fa9d-4210">**\_ chap**: 32-разрядное значение, представляющее маркер главы, из которой извлекаются строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4210">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="5fa9d-4211">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4211">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="5fa9d-4212">2.2.3.28 Кпмфрикурсорин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4212">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="5fa9d-4213">Сообщение Кпмфрикурсорин запрашивает выпуск курсора.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4213">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="5fa9d-4214">Формат сообщения Кпмфрикурсорин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4214">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-4215">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4215">0</span></span>

<span data-ttu-id="5fa9d-4216">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4216">1</span></span>

<span data-ttu-id="5fa9d-4217">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4217">2</span></span>

<span data-ttu-id="5fa9d-4218">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4218">3</span></span>

<span data-ttu-id="5fa9d-4219">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4219">4</span></span>

<span data-ttu-id="5fa9d-4220">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4220">5</span></span>

<span data-ttu-id="5fa9d-4221">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4221">6</span></span>

<span data-ttu-id="5fa9d-4222">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4222">7</span></span>

<span data-ttu-id="5fa9d-4223">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4223">8</span></span>

<span data-ttu-id="5fa9d-4224">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4224">9</span></span>

<span data-ttu-id="5fa9d-4225">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4225">1</span></span><br/> <span data-ttu-id="5fa9d-4226">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4226">0</span></span><br/>

<span data-ttu-id="5fa9d-4227">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4227">1</span></span>

<span data-ttu-id="5fa9d-4228">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4228">2</span></span>

<span data-ttu-id="5fa9d-4229">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4229">3</span></span>

<span data-ttu-id="5fa9d-4230">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4230">4</span></span>

<span data-ttu-id="5fa9d-4231">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4231">5</span></span>

<span data-ttu-id="5fa9d-4232">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4232">6</span></span>

<span data-ttu-id="5fa9d-4233">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4233">7</span></span>

<span data-ttu-id="5fa9d-4234">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4234">8</span></span>

<span data-ttu-id="5fa9d-4235">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4235">9</span></span>

<span data-ttu-id="5fa9d-4236">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4236">2</span></span><br/> <span data-ttu-id="5fa9d-4237">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4237">0</span></span><br/>

<span data-ttu-id="5fa9d-4238">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4238">1</span></span>

<span data-ttu-id="5fa9d-4239">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4239">2</span></span>

<span data-ttu-id="5fa9d-4240">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4240">3</span></span>

<span data-ttu-id="5fa9d-4241">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4241">4</span></span>

<span data-ttu-id="5fa9d-4242">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4242">5</span></span>

<span data-ttu-id="5fa9d-4243">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4243">6</span></span>

<span data-ttu-id="5fa9d-4244">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4244">7</span></span>

<span data-ttu-id="5fa9d-4245">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4245">8</span></span>

<span data-ttu-id="5fa9d-4246">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4246">9</span></span>

<span data-ttu-id="5fa9d-4247">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4247">3</span></span><br/> <span data-ttu-id="5fa9d-4248">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4248">0</span></span><br/>

<span data-ttu-id="5fa9d-4249">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4249">1</span></span>

<span data-ttu-id="5fa9d-4250">\_хкурсор</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4250">\_hCursor</span></span>



 

<span data-ttu-id="5fa9d-4251">**\_ хкурсор**: 32-разрядное значение, представляющее маркер курсора из сообщения кпмкреатекуерйоут для выпуска.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4251">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="5fa9d-4252">2.2.3.29 Кпмфрикурсораут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4252">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="5fa9d-4253">Сообщение Кпмфрикурсораут отвечает на сообщение Кпмфрикурсорин с результатами освобождения курсора.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4253">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="5fa9d-4254">Формат сообщения Кпмфрикурсораут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4254">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="5fa9d-4255">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4255">0</span></span>

<span data-ttu-id="5fa9d-4256">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4256">1</span></span>

<span data-ttu-id="5fa9d-4257">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4257">2</span></span>

<span data-ttu-id="5fa9d-4258">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4258">3</span></span>

<span data-ttu-id="5fa9d-4259">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4259">4</span></span>

<span data-ttu-id="5fa9d-4260">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4260">5</span></span>

<span data-ttu-id="5fa9d-4261">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4261">6</span></span>

<span data-ttu-id="5fa9d-4262">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4262">7</span></span>

<span data-ttu-id="5fa9d-4263">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4263">8</span></span>

<span data-ttu-id="5fa9d-4264">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4264">9</span></span>

<span data-ttu-id="5fa9d-4265">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4265">1</span></span><br/> <span data-ttu-id="5fa9d-4266">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4266">0</span></span><br/>

<span data-ttu-id="5fa9d-4267">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4267">1</span></span>

<span data-ttu-id="5fa9d-4268">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4268">2</span></span>

<span data-ttu-id="5fa9d-4269">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4269">3</span></span>

<span data-ttu-id="5fa9d-4270">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4270">4</span></span>

<span data-ttu-id="5fa9d-4271">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4271">5</span></span>

<span data-ttu-id="5fa9d-4272">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4272">6</span></span>

<span data-ttu-id="5fa9d-4273">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4273">7</span></span>

<span data-ttu-id="5fa9d-4274">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4274">8</span></span>

<span data-ttu-id="5fa9d-4275">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4275">9</span></span>

<span data-ttu-id="5fa9d-4276">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4276">2</span></span><br/> <span data-ttu-id="5fa9d-4277">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4277">0</span></span><br/>

<span data-ttu-id="5fa9d-4278">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4278">1</span></span>

<span data-ttu-id="5fa9d-4279">2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4279">2</span></span>

<span data-ttu-id="5fa9d-4280">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4280">3</span></span>

<span data-ttu-id="5fa9d-4281">4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4281">4</span></span>

<span data-ttu-id="5fa9d-4282">5</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4282">5</span></span>

<span data-ttu-id="5fa9d-4283">6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4283">6</span></span>

<span data-ttu-id="5fa9d-4284">7</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4284">7</span></span>

<span data-ttu-id="5fa9d-4285">8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4285">8</span></span>

<span data-ttu-id="5fa9d-4286">9</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4286">9</span></span>

<span data-ttu-id="5fa9d-4287">3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4287">3</span></span><br/> <span data-ttu-id="5fa9d-4288">0</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4288">0</span></span><br/>

<span data-ttu-id="5fa9d-4289">1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4289">1</span></span>

<span data-ttu-id="5fa9d-4290">\_ккурсорсремаининг</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4290">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="5fa9d-4291">**\_ ккурсорсремаининг**: 32-битовое целое число без знака, указывающее количество курсоров, которые все еще используются для запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4291">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="5fa9d-4292">2.2.3.30 Кпмдисконнект</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4292">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="5fa9d-4293">Сообщение Кпмдисконнект завершает подключение к серверу</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4293">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="5fa9d-4294">Сообщение не должно включать текст. будет отправлен только заголовок сообщения, как указано в разделе 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4294">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="5fa9d-4295">ошибки 2.2.4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4295">2.2.4 Errors</span></span>

<span data-ttu-id="5fa9d-4296">Все сообщения протокола службы индексирования содержимого должны возвращать 0x00000000 при успешном выполнении; в противном случае они возвращают 32-разрядный ненулевой код ошибки, который может быть либо HRESULT, либо значением NTSTATUS (см. раздел 1,8).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4296">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="5fa9d-4297">Если буфер слишком мал и не умещается в результате, \_ должен быть возвращен код состояния недостаточно \_ ресурсов (0xC0000009A), и Неудачная операция должна быть повторена с буфером большего размера.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4297">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="5fa9d-4298">Все остальные значения ошибок должны обрабатываться одинаково.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4298">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="5fa9d-4299">(Обратите внимание, что в настоящее время пробелы в значениях HRESULT и NTSTATUS не перекрываются, за исключением идентичных значений, но даже в случае возникновения конфликтов в будущем это не вызовет никаких проблем с протоколом, если значение параметра STATUS \_ Недостаточные \_ ресурсы остаются уникальными, так как все остальные значения ошибок обрабатываются одинаково.)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4299">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="5fa9d-4300">3. Сведения о протоколе</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4300">3 Protocol Details</span></span>

-   [<span data-ttu-id="5fa9d-4301">Сведения о сервере 3,1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4301">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="5fa9d-4302">3,2. сведения о клиенте</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4302">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="5fa9d-4303">Запросы сообщений CISP для удаленного запроса каталогов службы индексирования не нуждаются в определенной последовательности.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4303">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="5fa9d-4304">Рекомендуется, чтобы более высокий уровень приступил к осмысленной последовательности сообщений, как и для сообщений, полученных из этой последовательности или с недопустимыми данными, сервер будет отвечать с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4304">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="5fa9d-4305">Некоторые сообщения также зависят от более высокого уровня, предоставляющего допустимые данные, полученные в сообщениях, предшествующих последовательности.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4305">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="5fa9d-4306">На следующей схеме показана типичная последовательность сообщений для простого запроса от клиента к удаленному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4306">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![последовательность сообщений для простого запроса](images/protocoldetails.jpg)

<span data-ttu-id="5fa9d-4308">Сообщения, представленные на предыдущей схеме, представляют собой подмножество всех сообщений CISP, используемых для запроса каталога службы удаленного индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4308">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="5fa9d-4309">Сведения о сервере 3,1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4309">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="5fa9d-4310">3.1.1. Абстрактная модель данных</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4310">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="5fa9d-4311">В следующем разделе задаются данные и состояние, поддерживаемые сервером CISP.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4311">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="5fa9d-4312">Приведенные здесь данные предназначены для упрощения объяснения того, как работает протокол.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4312">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="5fa9d-4313">Этот раздел не требует, чтобы реализации применялись к этой модели, если их внешнее поведение согласуется с, описанным в этом документе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4313">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="5fa9d-4314">Служба индексирования, реализующая CISP, должна поддерживать следующие абстрактные элементы данных:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4314">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="5fa9d-4315">Список клиентов, подключенных к серверу</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4315">The list of clients connected to the server</span></span>
-   <span data-ttu-id="5fa9d-4316">Сведения о каждом клиенте, включая:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4316">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="5fa9d-4317">Версия клиента (как указано в сообщении Кпмконнектин, указанном в разделе 2.2.3.6)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4317">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="5fa9d-4318">Каталог, связанный с клиентом (с помощью сообщения Кпмконнектин)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4318">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="5fa9d-4319">Дополнительные свойства клиента, как указано в разделе 2.2.1.21.1.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4319">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="5fa9d-4320">Поисковый запрос клиента</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4320">Client's search query</span></span>
    -   <span data-ttu-id="5fa9d-4321">Список дескрипторов курсоров для запроса и позиции в результирующем наборе для каждого дескриптора.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4321">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="5fa9d-4322">Текущий набор привязок</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4322">Current set of bindings</span></span>
    -   <span data-ttu-id="5fa9d-4323">Текущее состояние запроса, включающего (для каждого курсора):</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4323">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="5fa9d-4324">Число строк в результатах запроса</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4324">Number of rows in query result</span></span>
        -   <span data-ttu-id="5fa9d-4325">Числитель и знаменатель завершения запроса</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4325">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="5fa9d-4326">Последнее число строк, сообщаемое последним сообщением Кпмратиофинишедаут для данного курсора</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4326">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="5fa9d-4327">Будет ли запрос отслеживаться сервером на предмет изменений в результатах запроса, и если он отслеживается, что изменилось в результатах запроса с момента последнего сообщения клиенту, Кпмсенднотифйоут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4327">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="5fa9d-4328">Список обработчиков глав, обслуживаемых этим запросом клиенту.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4328">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="5fa9d-4329">Список дескрипторов закладок для каждого курсора, обслуживаемого этим запросом клиенту.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4329">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="5fa9d-4330">Текущее состояние службы индексирования, которое может быть "не инициализировано", "выполняется" или "завершение работы".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4330">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="5fa9d-4331">Обратите внимание, что большая часть времени сервера находится в состоянии "выполняется".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4331">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="5fa9d-4332">Ниже приведена схема конечного автомата для сервера.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4332">Following is the state machine diagram for the server:</span></span>

    ![схема конечного автомата сервера службы индексирования](images/abstractdatamodel.jpg)

-   <span data-ttu-id="5fa9d-4334">Сведения о каталоге: Количество индексируемых документов, размер индекса, число уникальных ключей и т. д. (см. раздел 2.2.3.1 для полного списка), State (соответствует значениям Двневстате в разделе 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4334">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="5fa9d-4335">Для каждого поддерживаемого языка база данных вариантов слов, описанная в разделе 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4335">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="5fa9d-4336">3.1.2. Таймеры</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4336">3.1.2 Timers</span></span>

<span data-ttu-id="5fa9d-4337">Таймеры протокола не требуются.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4337">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="5fa9d-4338">3.1.3. Инициализация</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4338">3.1.3 Initialization</span></span>

<span data-ttu-id="5fa9d-4339">После инициализации сервер должен установить свое состояние "не инициализировано" и начать прослушивание сообщений по именованному каналу, указанному в разделе 1,9.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4339">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="5fa9d-4340">После выполнения любой другой внутренней инициализации она должна перейти в состояние "выполняется".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4340">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="5fa9d-4341">3.1.4. Активируемые события более высокого уровня</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4341">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="5fa9d-4342">Нет.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4342">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="5fa9d-4343">Правила обработки сообщений 3.1.5. и последовательности</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4343">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="5fa9d-4344">При возникновении ошибки во время обработки сообщения, отправленного клиентом, сервер должен сообщить об ошибке обратно клиенту следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4344">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="5fa9d-4345">Прерывать обработку сообщения, отправленного клиентом</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4345">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="5fa9d-4346">Ответ с заголовком сообщения (только) сообщения, отправленного клиентом, оставляя \_ поле сообщения неизменным.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4346">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="5fa9d-4347">Задайте в \_ поле Состояние значение кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4347">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="5fa9d-4348">При поступлении сообщения сервер должен проверить \_ значение поля MSG, чтобы узнать, является ли он известным типом (см. раздел 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4348">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="5fa9d-4349">Если тип неизвестен, он должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4349">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="5fa9d-4350">После этого сервер должен проверить \_ значение поля улчекксум, если тип сообщения имеет одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4350">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="5fa9d-4351">Кпмконнектин (0x000000C8)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4351">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="5fa9d-4352">Кпмкреатекуерин (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4352">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="5fa9d-4353">Кпмсетбиндингсин (0x000000D0)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4353">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="5fa9d-4354">Кпмжетровсин (0x000000CC)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4354">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="5fa9d-4355">Кпмфетчвалуеин (0x000000E4)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4355">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="5fa9d-4356">Чтобы проверить \_ значение поля улчекксум, сервер должен проверить значение, указанное клиентом в \_ поле Иклиентверсион сообщения кпмконнектин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4356">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="5fa9d-4357">Если \_ для поля иклиентверсион не задано значение 0x00000008, а \_ для поля улчекксум не задано значение 0x00000000, сервер должен сообщить о состоянии \_ недопустимого \_ параметра (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4357">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="5fa9d-4358">Сервер не должен проверять \_ поле улчекксум для клиентов, присвойте \_ полю иклиентверсион значение меньше 0x00000008.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4358">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="5fa9d-4359">Если \_ значение поля иклиентверсионфиелд равно 0x00000008 или больше, сервер должен проверить, что \_ поле улчекксум было вычислено как указано в разделе 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4359">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="5fa9d-4360">Если \_ значение улчекксум недопустимо, сервер должен сообщить \_ \_ об ошибке состояния недопустимого параметра (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4360">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="5fa9d-4361">Затем сервер проверяет, в каком состоянии находится.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4361">Next, the server checks which state is it in.</span></span> <span data-ttu-id="5fa9d-4362">Если состояние "не инициализировано", сервер должен сообщить \_ \_ об ошибке CI E Not \_ Initialized (0x8004180B).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4362">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="5fa9d-4363">Если состояние "завершение работы", сервер должен сообщить \_ об ошибке "CI E \_ Shutdown (0x80041812)".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4363">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="5fa9d-4364">После того как заголовок определен как допустимый и сервер находится в состоянии "выполняется", дальнейшая обработка сообщений должна быть выполнена, как указано в подразделах ниже.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4364">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="5fa9d-4365">Управление каталогом службы удаленного индексирования 3.1.5.1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4365">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="5fa9d-4366">3.1.5.1.1 получение запроса КпмЦистатеинаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4366">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="5fa9d-4367">Когда сервер получает запрос сообщения КпмЦистатеинаут от клиента, сервер должен сначала проверить, находится ли клиент в списке подключенных клиентов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4367">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="5fa9d-4368">Если клиент отсутствует в списке, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4368">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="5fa9d-4369">В противном случае он должен ответить клиенту сообщением КпмЦистатеинаут, заполняя его данными о связанном с клиентом каталоге, как указано в разделе 2.2.3.1.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4369">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="5fa9d-4370">3.1.5.1.2 получение запроса Кпмсеткатстатеин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4370">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="5fa9d-4371">Когда сервер получает запрос сообщения Кпмсеткатстатеин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4371">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4372">Убедитесь, что у клиента есть административный доступ.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4372">Check that client has administrative access.</span></span> <span data-ttu-id="5fa9d-4373">Если у клиента отсутствует административный доступ, сервер должен сообщить \_ \_ об ошибке отказа в доступе (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4373">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="5fa9d-4374">Если \_ двневстате не равно Цикат \_ все открытые, \_ измените состояние каталога, указанного в поле катнаме, как указано в \_ поле двневстате.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4374">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="5fa9d-4375">Дополнительные сведения см. в разделе 2.2.3.2.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4375">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="5fa9d-4376">Если сервер не находит каталог с именем, указанным в поле Катнаме, сервер должен вернуть состояние \_ Ошибка недопустимого \_ параметра (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4376">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4377">Ответ на клиент с помощью сообщения Кпмсеткатстатеаут, где \_ ДВОЛДСТАТЕ должно быть установлено предыдущее состояние каталога.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4377">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="5fa9d-4378">Если \_ двневстате РАВЕН Цикат \_ все \_ открытые, сервер должен проверить состояние всех каталогов и, если все они запущены, должен установить \_ для дволдстате значение 0x00000001, а в противном случае задать для \_ дволдстате значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4378">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="5fa9d-4379">3.1.5.1.3 получение запроса Кпмупдатедокументсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4379">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="5fa9d-4380">Когда сервер получает запрос сообщения Кпмупдатедокументсин, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4380">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4381">Проверьте, находится ли клиент в списке подключенных клиентов (которые имеют связанный каталог).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4381">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="5fa9d-4382">Если клиент отсутствует в списке, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4382">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4383">Убедитесь, что у клиента есть административный доступ.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4383">Check that client has administrative access.</span></span> <span data-ttu-id="5fa9d-4384">Если у клиента нет прав администратора для доступа к серверу, сервер должен сообщить \_ \_ об ошибке отказа в доступе (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4384">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="5fa9d-4385">Начало процесса индексирования пути, указанного клиентом, выполнение полного или добавочного сканирования в зависимости от значения \_ поля флага в сообщении кпмупдатедокументсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4385">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="5fa9d-4386">Если путь не был ранее проиндексирован, его необходимо добавить в коллекцию индексированных расположений и выполнить полную проверку.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4386">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="5fa9d-4387">Если указано недопустимое значение \_ поля флага, сервер должен действовать так, как если бы \_ флаг был установлен в значение UPD \_ init и выполнял полную проверку.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4387">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="5fa9d-4388">Эта операция должна выполняться в каталоге, связанном с клиентом.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4388">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="5fa9d-4389">Ответьте на клиент с помощью заголовка сообщения для Кпмупдатедокументсин и задайте в \_ поле Status результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4389">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="5fa9d-4390">3.1.5.1.4 получение запроса Кпмфорцемержеин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4390">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="5fa9d-4391">Когда сервер получает запрос сообщения Кпмфорцемержеин, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4391">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4392">Проверьте, находится ли клиент в списке подключенных клиентов (которые имеют связанный каталог).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4392">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="5fa9d-4393">Если клиент отсутствует в списке, сервер должен сообщить \_ об ошибке состояния "Недопустимый \_ параметр" (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4393">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4394">Убедитесь, что у клиента есть административный доступ.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4394">Check that client has administrative access.</span></span> <span data-ttu-id="5fa9d-4395">Если у клиента отсутствует административный доступ, сервер должен сообщить \_ \_ об ошибке отказа в доступе (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4395">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="5fa9d-4396">Начните любой процесс обслуживания, необходимый для повышения производительности запросов к каталогу, связанному с клиентом.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4396">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="5fa9d-4397">Ответьте на клиент с помощью заголовка сообщения для Кпмфорцемержеин и задайте в \_ поле Status результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4397">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="5fa9d-4398">Обратите внимание, что процесс обслуживания является асинхронным и может продолжаться после того, как клиент получит ответное сообщение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4398">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="5fa9d-4399">Этот процесс не влияет непосредственно на протокол (кроме времени отклика).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4399">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="5fa9d-4400">Запросы удаленной службы индексирования 3.1.5.2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4400">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="5fa9d-4401">3.1.5.2.1 получение запроса Кпмконнектин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4401">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="5fa9d-4402">Когда сервер получает запрос Кпмконнектин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4402">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4403">Проверьте, находится ли клиент в списке подключенных клиентов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4403">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="5fa9d-4404">В этом случае сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4404">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4405">Проверяет, существует ли указанный каталог, но не находится в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4405">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="5fa9d-4406">Если это не так, то сервер должен сообщить \_ \_ об ошибке Reporting E без \_ каталога (0x8004181D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4406">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="5fa9d-4407">Добавьте клиент в список подключенных клиентов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4407">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="5fa9d-4408">Свяжите каталог с клиентом.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4408">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="5fa9d-4409">Храните в состоянии клиента сведения, передаваемые в сообщении Кпмконнектин (например, имя каталога, версия клиента и т. д.).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4409">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="5fa9d-4410">Ответ на клиент с помощью сообщения Кпмконнектаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4410">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="5fa9d-4411">3.1.5.2.2 получение запроса Кпмкреатекуерин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4411">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="5fa9d-4412">Когда сервер получает запрос сообщения Кпмкреатекуерин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4412">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4413">Проверьте, находится ли клиент в списке подключенных клиентов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4413">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="5fa9d-4414">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4414">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4415">Убедитесь, что у клиента уже есть связанный с ним запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4415">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="5fa9d-4416">В этом случае сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4416">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4417">Проверьте, находится ли каталог, связанный с клиентом, в состоянии, что позволяет обрабатывать запросы (ЦИКАТ \_ ReadOnly или Цикат с \_ возможностью записи).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4417">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="5fa9d-4418">Если это не так, сервер должен сообщить \_ \_ \_ об ошибке запроса No (0x8004160C).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4418">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="5fa9d-4419">Проанализируйте набор ограничений, порядок сортировки и группирования, указанные в запросе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4419">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="5fa9d-4420">Если сервер обнаруживает ошибку, он должен сообщить о соответствующей ошибке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4420">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="5fa9d-4421">Если по какой бы то ни было причине этот шаг завершается сбоем, сервер должен сообщить об обнаруженной ошибке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4421">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="5fa9d-4422">Сведения об ошибках запросов службы индексирования см \[ . в разделе MSDN-куерерр \] .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4422">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="5fa9d-4423">Сохраните поисковый запрос в состоянии клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4423">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="5fa9d-4424">Выполните все подготовительные действия, необходимые для обслуживания строк на клиенте, и свяжите запрос с соответствующими дескрипторами курсора (в зависимости от информации, передаваемой в сообщении Кпмкреатекуерин).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4424">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="5fa9d-4425">Добавьте эти дескрипторы в список дескрипторов курсоров клиента и инициализируйте списки дескрипторов глав и закладок.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4425">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="5fa9d-4426">Инициализировать список дескрипторов глав для каждого курсора в этом запросе на базу данных \_ со значением NULL \_ параметру hChapter</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4426">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="5fa9d-4427">Инициализируйте список дескрипторов закладок для каждого курсора в этом запросе на набор ДББМК \_ First и дббмк \_ Last.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4427">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="5fa9d-4428">Пометьте запрос как неотслеживаемый для изменений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4428">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="5fa9d-4429">Инициализирует количество строк до текущего вычисленного числа строк (может быть 0, если запрос не начал выполнение или какое-либо число, если запрос находится в процессе выполнения) и инициализирует числитель и знаменатель завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4429">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="5fa9d-4430">Ответ на клиент с помощью сообщения Кпмкреатекуерйоут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4430">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="5fa9d-4431">3.1.5.2.3 получение запроса Кпмжеткуеристатусин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4431">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="5fa9d-4432">Когда сервер получает запрос сообщения Кпмжеткуеристатусин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4432">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4433">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4433">Check if the client has query associated with it.</span></span> <span data-ttu-id="5fa9d-4434">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4434">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4435">Проверьте, находится ли дескриптор курсора в списке дескрипторов курсора клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4435">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="5fa9d-4436">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4436">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="5fa9d-4437">Подготовка сообщения Кпмжеткуеристатусаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4437">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="5fa9d-4438">Сервер должен получить текущее состояние запроса и задать его в \_ поле кстатус (см. 2.2.3.11 для возможных значений).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4438">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="5fa9d-4439">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4439">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="5fa9d-4440">Ответ на клиент с помощью сообщения Кпмжеткуеристатусаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4440">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="5fa9d-4441">3.1.5.2.4 получение запроса Кпмжеткуеристатусексин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4441">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="5fa9d-4442">Когда сервер получает запрос сообщения Кпмжеткуеристатусексин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4442">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4443">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4443">Check if the client has a query associated with it.</span></span> <span data-ttu-id="5fa9d-4444">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4444">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4445">Проверьте, находится ли переданный дескриптор курсора в списке дескрипторов курсора клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4445">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="5fa9d-4446">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4446">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="5fa9d-4447">Подготовка сообщения Кпмжеткуеристатусексаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4447">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="5fa9d-4448">Сервер должен получить текущее состояние запроса и ход выполнения запроса и задать Кстатус (см. 2.2.3.11 для возможных значений), \_ двратиофинишедденоминатор и \_ двратиофинишеднумератор соответственно.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4448">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="5fa9d-4449">Затем необходимо задать для кровстотал число строк в результатах запроса \_ .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4449">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="5fa9d-4450">Если этот шаг завершается неудачей по каким либо причинам, сервер должен сообщить о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4450">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="5fa9d-4451">Получите сведения о каталоге клиента и заполните \_ кфилтереддокументс и \_ кдокументстофилтер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4451">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="5fa9d-4452">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4452">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="5fa9d-4453">Получите расположение закладки, обозначенной маркером в \_ поле БМК, и заполните оставшееся \_ поле ировбмк в сообщении кпмжеткуеристатусексаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4453">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="5fa9d-4454">Если этот шаг завершается неудачей по каким либо причинам, сервер должен сообщить о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4454">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="5fa9d-4455">Ответ на клиент с помощью сообщения Кпмжеткуеристатусексаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4455">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="5fa9d-4456">3.1.5.2.5 получение запроса Кпмратиофинишедин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4456">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="5fa9d-4457">Когда сервер получает запрос сообщения Кпмратиофинишедин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4457">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4458">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4458">Check if the client has query associated with it.</span></span> <span data-ttu-id="5fa9d-4459">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4459">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4460">Проверьте, находится ли переданный дескриптор курсора в списке дескрипторов курсора клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4460">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="5fa9d-4461">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4461">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="5fa9d-4462">Подготовка сообщения Кпмратиофинишедаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4462">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="5fa9d-4463">Сервер должен получить состояние запроса клиента и заполнить \_ поля улнумератор, \_ улденоминатор и \_ CRowset.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4463">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="5fa9d-4464">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4464">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="5fa9d-4465">Если \_ CRowset равно последнему сообщаемому числу строк для этого запроса, установите \_ фневровс в 0x00000000, в противном случае задайте для него значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4465">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="5fa9d-4466">Обновить Последнее сообщаемое количество строк для этого запроса до значения \_ CRowset.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4466">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="5fa9d-4467">Ответ на клиент с помощью сообщения Кпмратиофинишедаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4467">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="5fa9d-4468">3.1.5.2.6 получение запроса Кпмсетбиндингсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4468">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="5fa9d-4469">Когда сервер получает запрос сообщения Кпмсетбиндингсин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4469">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4470">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4470">Check if the client has a query associated with it.</span></span> <span data-ttu-id="5fa9d-4471">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4471">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4472">Проверьте, находится ли переданный дескриптор курсора в списке дескрипторов курсора клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4472">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="5fa9d-4473">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4473">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="5fa9d-4474">Убедитесь, что сведения о привязках допустимы (т. е. столбец, по крайней мере, указывает значение, длину или состояние, которое должно быть возвращено; не пересекается в привязках для значения, длины или состояния; и значения, длины и состояния в указанном размере строки) и если не сообщать \_ \_ об ошибке DB e Бадбиндинфо (0x80040E08).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4474">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="5fa9d-4475">Сохраните сведения о привязке, связанные со столбцами, указанными в поле Аколумнс.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4475">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="5fa9d-4476">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4476">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="5fa9d-4477">Ответ на клиент с заголовком сообщения (только) с \_ установленным сообщением кпмсетбиндингсин и \_ состоянием, равным результатам указанной привязки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4477">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="5fa9d-4478">3.1.5.2.7 получение запроса Кпмжетровсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4478">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="5fa9d-4479">Когда сервер получает запрос сообщения Кпмжетровсин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4479">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4480">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4480">Check if the client has query associated with it.</span></span> <span data-ttu-id="5fa9d-4481">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4481">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4482">Убедитесь, что переданный дескриптор курсора находится в аселист дескрипторов курсора клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4482">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="5fa9d-4483">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4483">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="5fa9d-4484">Проверьте, имеет ли клиент текущий набор привязок.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4484">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="5fa9d-4485">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4485">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="5fa9d-4486">Подготовка сообщения Кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4486">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="5fa9d-4487">Сервер должен располагать курсор в результатах запроса, как указано в описании поиска.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4487">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="5fa9d-4488">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4488">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="5fa9d-4489">Выберет столько строк, сколько замещается в буфере, размер которого обозначен параметром \_ кбреадбуффер, но не больше, чем указано в \_ кровстотрансфер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4489">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="5fa9d-4490">При выборке строк сервер должен сравнить тип значения свойства выбранного столбца с типом, указанным в текущем наборе привязок клиента (раздел 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4490">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="5fa9d-4491">Если тип в привязке не является \_ вариантом VT, сервер должен попытаться преобразовать значение свойства столбца в этот тип.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4491">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="5fa9d-4492">В противном случае, если установлен \_ флаг DBPROP усикстендеддбтипес в \_ наборе свойств DBPROPSET куерекст клиента или если значение свойства столбца не является \_ векторным типом VT, значение свойства должно возвращаться в его нормальном типе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4492">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="5fa9d-4493">Если ни один из вариантов не является случайом (т. е. у сервера есть \_ Векторный тип VT, а клиент не поддерживает \_ вектор VT), сервер должен попытаться преобразовать его в \_ тип массива VT следующим образом: VT \_ i8, VT \_ UI8, VT \_ fileTime и VT \_ CLSID элементы массива не могут быть преобразованы, а завершаться ошибкой. \_Элементы массива VT LPSTR и VT \_ LPWSTR должны быть преобразованы в VT \_ BSTR; элементы массива всех остальных типов должны оставаться неизменными.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4493">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="5fa9d-4494">Наконец, если столбцы строки содержат дескрипторы глав или маркеры закладок, сервер должен обновить соответствующие списки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4494">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="5fa9d-4495">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4495">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="5fa9d-4496">Сохранение фактического числа строк, извлекаемых в \_ кровсретурнед.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4496">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="5fa9d-4497">Скопируйте описание поиска и поле раздела из Кпмжетровсин в сообщение Кпмжетровсаут для отправки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4497">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="5fa9d-4498">Сохранять полученные строки в поле строк (см. Примечание о состоянии ниже и разделе 2.2.3.16 в структуре поля строк).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4498">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="5fa9d-4499">Ответ на клиент с помощью сообщения Кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4499">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="5fa9d-4500">Примечание о поле "байт состояния":</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4500">Note on status byte field:</span></span>

<span data-ttu-id="5fa9d-4501">Если для Статусусед задано значение 0x01 в Ктаблеколумн сообщения Кпмсетбиндингин для столбца, то сервер должен установить байт состояния (который находится в Статусоффсет с начала строки) для этого столбца в одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4501">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="5fa9d-4502">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4502">Value</span></span> | <span data-ttu-id="5fa9d-4503">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4503">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="5fa9d-4504">0x00</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4504">0x00</span></span>  | <span data-ttu-id="5fa9d-4505">статусок</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4505">StatusOK</span></span>       |
| <span data-ttu-id="5fa9d-4506">0x01</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4506">0x01</span></span>  | <span data-ttu-id="5fa9d-4507">статусдеферред</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4507">StatusDeferred</span></span> |
| <span data-ttu-id="5fa9d-4508">0x02</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4508">0x02</span></span>  | <span data-ttu-id="5fa9d-4509">статуснулл</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4509">StatusNull</span></span>     |



 

<span data-ttu-id="5fa9d-4510">Если значение свойства отсутствует для этой строки, сервер должен задать для параметра Byte состояния значение Статуснулл.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4510">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="5fa9d-4511">Если значение слишком велико для передачи в сообщение Кпмжетровсаут, сервер должен задать для параметра Byte состояния значение Статусдеферред.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4511">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="5fa9d-4512">В противном случае сервер должен установить байт состояния в Статусок.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4512">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="5fa9d-4513">3.1.5.2.8 получение запроса Кпмфетчвалуеин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4513">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="5fa9d-4514">Когда сервер получает запрос сообщения Кпмфетчвалуеин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4514">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4515">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4515">Check if the client has query associated with it.</span></span> <span data-ttu-id="5fa9d-4516">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4516">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4517">Подготовка сообщения Кпмфетчвалуеаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4517">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="5fa9d-4518">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="5fa9d-4519">Найдите документ, указанный в \_ поле WID, и проверьте, доступен ли для этого клиента идентификатор свойства для этого документа (в дальнейшем именуемый как "значение свойства"), указанный в структуре пропспек.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4519">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="5fa9d-4520">Если это значение недоступно, сервер должен установить значение \_ фвалуиксистс в 0x00000000, а в противном случае задать \_ для фвалуиксистс значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4520">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="5fa9d-4521">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4521">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="5fa9d-4522">Если \_ фвалуиксистс равен 0x00000001, сервер должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4522">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="5fa9d-4523">Сериализует значение свойства в структуру СЕРИАЛИЗЕДПРОПЕРТИВАЛУЕ и копирует, начиная с \_ смещения кбсофар, \_ не более кбчунк байт (но не после конца сериализованного свойства) в поле управляемое vValue.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4523">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="5fa9d-4524">Если этот шаг завершается неудачей по каким либо причинам, сервер должен сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4524">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="5fa9d-4525">Задайте \_ для кбвалуе число байтов, скопированных на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4525">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="5fa9d-4526">Задайте для Втипе тип свойства значения свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4526">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="5fa9d-4527">Если длина сериализованного свойства больше \_ кбсофар, добавленного в \_ кбвалуе, задайте \_ для фмориксистс значение 0x00000001, в противном случае задайте для него значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4527">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="5fa9d-4528">Ответ на клиент с помощью сообщения Кпмфетчвалуеаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4528">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="5fa9d-4529">3.1.5.2.9 получение запроса Кпмжетнотифи</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4529">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="5fa9d-4530">Когда сервер получает сообщение Кпмжетнотифи от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4530">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4531">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4531">Check if the client has query associated with it.</span></span> <span data-ttu-id="5fa9d-4532">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4532">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4533">Если в результирующем наборе запроса не было изменений с момента последнего сообщения Кпмсенднотифйоут для этого клиента или если запрос в настоящий момент не отслеживает изменения в результирующем наборе, сервер должен ответить с сообщением Кпмжетнотифи и начать отслеживать запрос на изменения в наборе результатов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4533">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="5fa9d-4534">Если позднее в наборе результатов запроса произошло изменение, сервер должен отправить клиенту ровно одно сообщение Кпмсенднотифйоут и указать изменение в \_ поле ватчнотифи.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4534">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="5fa9d-4535">Если с момента последнего сообщения Кпмсенднотифйоут в результирующий набор запроса были внесены изменения, сервер должен ответить на Кпмсенднотифйоут и указать изменение в \_ поле ватчнотифи.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4535">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="5fa9d-4536">Обратите внимание, что в случае большого количества изменений в результатах запроса ДБВАТЧНОТИФИ \_ ровсчанжед имеет приоритет (т. е. Если запрос выполнен, повторное выполнение, а затем число измененных строк и запрос был выполнен повторно, то событие, о котором было отправлено, было бы дбватчнотифи \_ ровсчанжед).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4536">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="5fa9d-4537">3.1.5.2.10 получение запроса Кпмжетаппроксиматепоситионин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4537">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="5fa9d-4538">Когда сервер получает запрос сообщения Кпмжетаппроксиматепоситионин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4538">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4539">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4539">Check if the client has a query associated with it.</span></span> <span data-ttu-id="5fa9d-4540">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4540">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4541">Проверьте, находятся ли в соответствующих списках маркер курсора, маркер раздела и маркер закладки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4541">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="5fa9d-4542">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4542">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="5fa9d-4543">Найти строку, связанную с маркером закладки в результатах запроса и приблизительной позицией строки в наборе строк, на которую ссылается маркер главы, и определить числитель и знаменатель для этой должности.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4543">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="5fa9d-4544">Обратите внимание, что если маркер главы имеет \_ значение DB NULL \_ параметру hChapter, то соответствующая глава является основным набором строк запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4544">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="5fa9d-4545">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4545">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="5fa9d-4546">Ответ на клиент с помощью сообщения Кпмфетчвалуеаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4546">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="5fa9d-4547">3.1.5.2.11 получение запроса Кпмкомпаребмкин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4547">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="5fa9d-4548">Когда сервер получает запрос сообщения Кпмкомпаребмкин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4548">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4549">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4549">Check if the client has a query associated with it.</span></span> <span data-ttu-id="5fa9d-4550">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4550">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4551">Проверьте, находятся ли в соответствующих списках дескриптор курсора, дескрипторы разделов и маркеры закладок.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4551">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="5fa9d-4552">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4552">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="5fa9d-4553">Подготовка сообщения Кпмкомпаребмкаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4553">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="5fa9d-4554">Если маркеры закладки равны, \_ ДВКОМПАРИСОН должен иметь значение дбкомпаре \_ EQ.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4554">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="5fa9d-4555">В противном случае, если один из дескрипторов закладок является ДББМК \_ первым или дббмк \_ последним, \_ двкомпарисон должен иметь значение дбкомпаре \_ Ne.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4555">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="5fa9d-4556">В противном случае сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4556">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="5fa9d-4557">Поиск строк, на которые ссылается каждый маркер закладки в результатах запроса</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4557">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="5fa9d-4558">Если какая-либо из строк не входит в главу, обозначенную маркером главы в Кпмкомпаребмкин, \_ для ДВКОМПАРИСОН необходимо задать значение дбкомпаре \_ ноткомпарабле.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4558">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="5fa9d-4559">В противном случае, если обе строки находятся в одной и той же главе, сервер должен приблизительно соответствовать положению этих строк в наборе строк, на который ссылается этот маркер главы.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4559">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="5fa9d-4560">Затем он должен сравнить значения позиций и установить \_ для двкомпарисон значение дбкомпаре \_ lt, если значение первой строки меньше, чем у второй строки. в противном случае \_ двкомпарисон должно быть установлено в дбкомпаре \_ gt.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4560">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="5fa9d-4561">Ответ на клиент с заполненным сообщением Кпмкомпаребмкаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4561">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="5fa9d-4562">3.1.5.2.12 получение запроса Кпмрестартпоситионин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4562">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="5fa9d-4563">Когда сервер получает запрос сообщения Кпмрестартпоситионин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4563">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4564">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4564">Check if the client has a query associated with it.</span></span> <span data-ttu-id="5fa9d-4565">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4565">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4566">Проверьте, пройдены ли в соответствующих списках маркер курсора и маркер раздела.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4566">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="5fa9d-4567">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4567">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="5fa9d-4568">Переместить курсор в начало главы, определяемое маркером главы.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4568">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="5fa9d-4569">Обратите внимание, что если маркер главы имеет \_ значение DB NULL \_ параметру hChapter, то соответствующая глава является основным набором строк запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4569">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="5fa9d-4570">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4570">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="5fa9d-4571">Ответ на клиент с помощью сообщения Кпмрестартпоситионин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4571">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="5fa9d-4572">3.1.5.2.13 получение запроса Кпмфрикурсорин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4572">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="5fa9d-4573">Когда сервер получает запрос сообщения Кпмфрикурсорин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4573">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4574">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4574">Check if the client has a query associated with it.</span></span> <span data-ttu-id="5fa9d-4575">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4575">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="5fa9d-4576">Проверьте, находится ли переданный дескриптор курсора в списке дескрипторов курсора клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4576">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="5fa9d-4577">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4577">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="5fa9d-4578">Отпустите курсор и связанные ресурсы (см. раздел 3.1.1 для получения полного списка) для этого маркера курсора.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4578">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="5fa9d-4579">Удалить курсор из списка курсоров для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4579">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="5fa9d-4580">Ответьте на сообщение Кпмфрикурсораут, установив в \_ поле ккурсорсремаининг число оставшихся курсоров.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4580">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="5fa9d-4581">в списке этого клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4581">in this client's list.</span></span>
-   <span data-ttu-id="5fa9d-4582">Если для этого клиента больше нет курсоров, сервер должен освободить запрос и связанные с ним ресурсы (см. раздел 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4582">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="5fa9d-4583">3.1.5.2.14 получение запроса Кпмдисконнект</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4583">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="5fa9d-4584">Когда сервер получает запрос сообщения Кпмдисконнект от клиента, сервер должен удалить клиент из списка подключенных клиентов и освободить все ресурсы, связанные с клиентом.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4584">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="5fa9d-4585">События таймера 3.1.6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4585">3.1.6 Timer Events</span></span>

<span data-ttu-id="5fa9d-4586">Нет.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4586">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="5fa9d-4587">3.1.7 другие локальные события</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4587">3.1.7 Other Local Events</span></span>

<span data-ttu-id="5fa9d-4588">Когда сервер остановлен, он должен сначала перейти в состояние "завершение работы".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4588">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="5fa9d-4589">Затем он должен остановить прослушивание канала, выполнить другие задачи завершения работы, связанные с реализацией, а затем перейти в состояние "остановлено".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4589">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="5fa9d-4590">3,2. сведения о клиенте</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4590">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="5fa9d-4591">абстрактная модель данных 3.2.1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4591">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="5fa9d-4592">В следующем разделе указываются данные и состояние, поддерживаемые клиентом протокола службы индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4592">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="5fa9d-4593">Предоставленные данные предназначены для упрощения объяснения того, как работает протокол.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4593">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="5fa9d-4594">Этот раздел не требует, чтобы реализации применялись к этой модели, если их внешнее поведение согласуется с, описанным в этом документе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4594">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="5fa9d-4595">Клиент имеет следующее абстрактное состояние:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4595">A client has the following abstract state:</span></span>

-   <span data-ttu-id="5fa9d-4596">**Последнее отправленное сообщение**: копия последнего сообщения, отправленного на сервер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4596">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="5fa9d-4597">**Текущее значение свойства**: частичное значение свойства "отложено", которое находится в процессе извлечения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4597">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="5fa9d-4598">**Текущее число полученных байтов**: количество байтов, полученных для текущего значения свойства до настоящего времени.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4598">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="5fa9d-4599">**Состояние подключения именованного канала**: соединение с сервером.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4599">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="5fa9d-4600">таймеры 3.2.2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4600">3.2.2 Timers</span></span>

<span data-ttu-id="5fa9d-4601">Таймеры протокола не требуются.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4601">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="5fa9d-4602">Инициализация 3.2.3</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4602">3.2.3 Initialization</span></span>

<span data-ttu-id="5fa9d-4603">Никакие действия не выполняются до получения запроса на более высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4603">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="5fa9d-4604">3.2.4 события, активируемые Higher-Layer</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4604">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="5fa9d-4605">При получении запроса от более высокого уровня клиент должен создать соединение именованного канала с сервером, используя сведения, указанные в разделе 2,1.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4605">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="5fa9d-4606">Если это невозможно, запрос более высокого уровня должен быть неудачным.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4606">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="5fa9d-4607">Это значит, что в случае сбоя подключения следует повторить попытку, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4607">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="5fa9d-4608">Заголовок должен быть предварительно заполнен полями, заданными в разделе 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4608">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="5fa9d-4609">Для сообщений, которые задаются как запрашивающие ненулевую контрольную сумму, \_ значение УЛЧЕККСУМ должно быть вычислено следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4609">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="5fa9d-4610">Содержимое сообщения после \_ поля ulReserved2 в заголовке сообщения должно интерпретироваться как последовательность из 32 битовых целых чисел.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4610">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="5fa9d-4611">Клиент должен вычислить сумму числовых значений, заданных этими целыми числами.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4611">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="5fa9d-4612">Вычислите побитовое ИСКЛЮЧАЮЩее это значение с помощью 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4612">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="5fa9d-4613">Вычтите значение, заданное в \_ MSG, из значения, полученного в результате побитового исключающего XOR.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4613">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="5fa9d-4614">Управление каталогом службы удаленного индексирования 3.2.4.1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4614">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="5fa9d-4615">Каждое сообщение активируется запросом из более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4615">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="5fa9d-4616">Клиент для запросов сообщений CISP для удаленного управления каталогами не обеспечивает выполнение последовательности сообщений, но (за исключением сообщения Кпмсеткатстатеин) сервер будет отвечать только после успешного выполнения, если клиент ранее подключился с помощью сообщения Кпмконнектин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4616">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="5fa9d-4617">3.2.4.1.1 Отправка запроса КпмЦистатеинаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4617">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="5fa9d-4618">Как правило, более высокий уровень требует, чтобы клиент протокола отправлял сообщение КпмЦистатеинаут, когда ему требуются сведения о службах индексирования на сервере.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4618">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="5fa9d-4619">При запросе на отправку этого сообщения клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4619">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4620">Отправка сообщения КпмЦистатеинаут, как указано в разделе 2.2.3.1 на сервер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4620">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="5fa9d-4621">Ожидание получения от сервера сообщения КпмЦистатеинаут без автоматической отмены всех остальных сообщений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4621">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="5fa9d-4622">Сообщает значение \_ поля Status в ответе и, если оно прошло успешно, информационная структура возвращается к более высокому слою.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4622">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="5fa9d-4623">3.2.4.1.2 Отправка запроса Кпмсеткатстатеин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4623">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="5fa9d-4624">Как правило, более высокий уровень требует, чтобы клиент протокола отправлял сообщение Кпмсеткатстатеин, когда ему требуются сведения о каталоге или каталоге.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4624">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="5fa9d-4625">Для этого сообщения более высокий уровень должен предоставить клиенту протокола значение для \_ двневстате и, при необходимости, имя каталога.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4625">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="5fa9d-4626">При запросе на отправку этого сообщения клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4626">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4627">Отправка сообщения Кпмсеткатстатеин, указанного в 2.2.3.2, на сервер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4627">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="5fa9d-4628">Ожидание получения от сервера сообщения Кпмсеткатстатеаут без автоматической отмены всех остальных сообщений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4628">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="5fa9d-4629">Сообщает значение \_ поля Status в ответе и, если оно прошло успешно, \_ дволдстате обратно на более высокий уровень.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4629">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="5fa9d-4630">3.2.4.1.3 отправка запроса Кпмупдатедокументсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4630">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="5fa9d-4631">Более высокий уровень обычно запрашивает отправку этого сообщения, когда необходимо либо обновить документы в существующем пути, либо добавить новый путь к этому индексу.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4631">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="5fa9d-4632">Таким образом, более высокий уровень заключается в предоставлении пути и типа сканирования, указанного в разделе 2.2.3.4, где для существующих путей предназначено добавочное или полное обновление, а новая инициализация предназначена для новых путей.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4632">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="5fa9d-4633">Чтобы обслуживать запрос более высокого уровня, клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4633">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4634">Отправка сообщения Кпмупдатедокументсин, как указано в разделе 2.2.3.4 на сервер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4634">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="5fa9d-4635">Ожидание получения сообщения Кпмупдатедокументсин с сервера без автоматической отмены всех остальных сообщений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4635">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="5fa9d-4636">Сообщает значение \_ поля Status в ответе назад к более высокому слою.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4636">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="5fa9d-4637">3.2.4.1.4 Отправка запроса Кпмфорцемержеин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4637">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="5fa9d-4638">Как правило, более высокий уровень запрашивает отправку этого сообщения при необходимости улучшить производительность запросов или является частью запланированного обслуживания службы индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4638">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="5fa9d-4639">Чтобы обслуживать более высокий уровень, клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4639">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4640">Отправка сообщения Кпмфорцемержеин, указанного в разделе 2.2.3.5, на сервер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4640">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="5fa9d-4641">Ожидание получения сообщения Кпмупдатедокументсин с сервера без автоматической отмены всех остальных сообщений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4641">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="5fa9d-4642">Сообщает значение \_ поля Status в ответе назад к более высокому слою.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4642">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="5fa9d-4643">Сообщения о запросе каталога службы удаленного индексирования 3.2.4.2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4643">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="5fa9d-4644">За исключением Кпмжетровсин/Кпмжетровсаут, Кпмфетчвалуеин/Кпмфетчвалуеаут существует связь "один к одному" между CISP сообщениями и запросами более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4644">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="5fa9d-4645">Для двух упомянутых выше исключений может существовать несколько сообщений, создаваемых клиентом для удовлетворения требований к размеру или получения полного свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4645">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="5fa9d-4646">Более высокий уровень обычно отслеживает все сведения, относящиеся к запросам (например, открытые дескрипторы курсоров, допустимые значения для дескрипторов закладок и разделов, значения WID для отложенных значений свойств и т. д.), а также отслеживает, если клиент находится в подключенном состоянии, но он не применяется каким-либо образом клиентом.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4646">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="5fa9d-4647">В наглядной части схемы в разделе 3 показана эта последовательность для простого запроса службы индексирования.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4647">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="5fa9d-4648">3.2.4.2.1 Отправка запроса Кпмконнектин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4648">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="5fa9d-4649">Это сообщение обычно является первым запросом от более высокого уровня (как если бы клиент не был подключен, сервер будет завершать свою часть сообщений с исключением Кпмсеткатстатеин).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4649">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="5fa9d-4650">Более высокий уровень предоставляет клиенту протокола сведения, необходимые для подключения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4650">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="5fa9d-4651">Чтобы обслуживать более высокий уровень, клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4651">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4652">Заполните сообщение, используя сведения, предоставленные клиентом более высокого уровня (см. раздел 2.2.3.6) в \_ иклиентверсион, MachineName, username, PropertySet1, PropertySet2 и апропертисет.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4652">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="5fa9d-4653">Задайте \_ фклиентисремоте, \_ кбблоб, \_ cbBlob2, кпропсет и цекстпропсет, как указано в 2.2.3.6.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4653">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="5fa9d-4654">Задайте контрольную сумму в \_ поле улчекксум.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4654">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="5fa9d-4655">Отправка сообщения Кпмконнектин на сервер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4655">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="5fa9d-4656">Ожидание получения сообщения Кпмконнектаут с сервера без автоматической отмены всех остальных сообщений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4656">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="5fa9d-4657">Сообщает значение \_ поля Status в ответе и, если оно прошло успешно, \_ serverVersion обратно на более высокий уровень.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4657">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="5fa9d-4658">В информативных целях ожидается, что при успешном подключении более высокие уровни обычно выполняют следующие действия, но не применяются клиентом CISP.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4658">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="5fa9d-4659">Использование сообщений об управлении каталогом службы удаленного индексирования для административных задач</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4659">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="5fa9d-4660">Используйте запрос Кпмкреатекуерин, чтобы создать поисковый запрос с целью получения результатов из каталога.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4660">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="5fa9d-4661">3.2.4.2.2 Отправка запроса Кпмкреатекуерин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4661">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="5fa9d-4662">Более высокий уровень, как правило, предоставляет сведения о создании запроса после подключения клиента протокола.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4662">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="5fa9d-4663">Более высокий уровень предоставляет клиенту набор ограничений, набор столбцов, правила порядка сортировки и набор классификации (каждый из них можно опустить), свойства набора строк и структуру сопоставления ИДЕНТИФИКАТОРов свойств.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4663">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="5fa9d-4664">При получении этого запроса от более высокого уровня клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4664">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4665">Подготовьте Кпмкреатекуерйоут, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4665">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="5fa9d-4666">Если задан набор столбцов, установите для Кколумнссетпресет значение 0x01 и заполните поле Columning.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4666">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="5fa9d-4667">Если имеются ограничения, задайте для Крестриктионпресент значение 0x01 и заполните поле ограничения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4667">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="5fa9d-4668">Если указан набор сортировки, заполните поле Sorting.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4668">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="5fa9d-4669">Если задан набор классификаций, задайте для Ксортсетпресент значение 0x01 и заполните поле Категоризатионсет.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4669">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="5fa9d-4670">Установите остальные поля, как указано в 2.2.3.8.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4670">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="5fa9d-4671">Вычислите \_ поле улчекксум в заголовке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4671">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="5fa9d-4672">Отправка сообщения Кпмкреатекуерин на сервер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4672">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="5fa9d-4673">Дождитесь получения сообщения Кпмкреатекуерйоут (см. сведения в разделе 3.2.5.1.1) без автоматического удаления всех остальных сообщений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4673">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="5fa9d-4674">Сообщает значение \_ поля Status в ответе и, если оно прошло успешно, массив дескрипторов курсоров и информативные логические значения (как указано в 2.2.3.9) возвращаются к более высокому слою.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4674">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="5fa9d-4675">3.2.4.2.3 отправка запроса Кпмсетбиндингсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4675">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="5fa9d-4676">Как правило, более высокий уровень задает привязки для каждого столбца, возвращаемого в строках, если он уже имеет допустимый маркер курсора (после успешного получения Кпмкреатекуерйоут см. раздел 3.2.5.1.1).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4676">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="5fa9d-4677">Выше ожидается, что необходимо предоставить массив структур Ктаблеколумн, как указано в разделе 2.2.4.31, для поля Аколумнс и допустимого маркера курсора.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4677">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="5fa9d-4678">При получении этого запроса от более высокого уровня клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4678">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4679">Вычислите количество структур Ктаблеколумн в массиве Аколумнс и задайте для поля Кколумнс это значение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4679">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="5fa9d-4680">Вычислите общий размер в байтах для полей Кколумнс и Аколумнс и задайте \_ для поля кббиндингдеск это значение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4680">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="5fa9d-4681">Задавайте указанные поля в сообщении Кпмсетбиндингсин значениям, предоставленным более высоким уровнем приложения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4681">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="5fa9d-4682">Задайте в \_ поле улчекксум значение, вычисленное, как указано в разделе 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4682">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="5fa9d-4683">Отправка завершенного сообщения Кпмсетбиндигнсин на сервер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4683">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="5fa9d-4684">Ожидание получения сообщения Кпмсетбиндингсин от сервера, удаление других сообщений.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4684">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="5fa9d-4685">Укажите состояние из \_ поля состояние ответа на более высокий уровень.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4685">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="5fa9d-4686">Для информативных целей ожидается, что более высокие уровни обычно запрашивают у клиента сообщение Кпмжетровсин, но это не обеспечивается протоколом службы индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4686">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="5fa9d-4687">3.2.4.2.4 Отправка запроса Кпмжетровсин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4687">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="5fa9d-4688">Когда более высокий уровень собирается получить сведения о строках, он предоставит клиенту протокола допустимый маркер курсора и раздела и предложит соответствующее описание поиска.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4688">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="5fa9d-4689">Как правило, ожидается более высокий уровень, если у него есть допустимый обработчик курсора или раздела, а привязки были заданы с помощью сообщения Кпмсетбиндингсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4689">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="5fa9d-4690">Чтобы получить доступ к набору строк в главе, более высокий уровень заключается в использовании маркера раздела, полученного от сервера, в предыдущем Кпмжетровсаут сообщении.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4690">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="5fa9d-4691">При получении этого запроса от более высокого уровня клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4691">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4692">Определите, какое целочисленное значение без знака следует указать для \_ поля кбреадбуффер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4692">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="5fa9d-4693">Чтобы определить это значение, клиент должен получить максимальное значение из следующего:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4693">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="5fa9d-4694">1000. время в значении \_ поля c ровстотрансфер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4694">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="5fa9d-4695">Значение \_ кброввидс, округленное до ближайшего 512 байта с множителем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4695">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="5fa9d-4696">Передавайте большее из этих двух значений, до ограничения 16 КБ.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4696">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="5fa9d-4697">В случаях, когда размер одной строки превышает 16 КБ, сервер не может вернуть результаты в этот запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4697">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="5fa9d-4698">Укажите клиентскую базу для данных строк переменного размера в адресном пространстве клиента в \_ поле улклиентбасе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4698">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="5fa9d-4699">*Поведение Windows. для 32-разрядного клиента, говорящего на 32-разрядном сервере, или клиента 64 bit, говорящего на 64-bit Server, этому параметру присваивается адрес в памяти принимающего буфера в процессе приложения. Это позволяет указателям, полученным в поле строк Кпмжетровсаут, быть правильными указателями памяти в процессе клиентского приложения. В противном случае — значение 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4699">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="5fa9d-4700">Вычислите размер описания поиска и задайте его в \_ поле кбсик.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4700">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="5fa9d-4701">Установите значение Кбресервед (которое будет действовать как смещение для начала строк) на значение \_ кбсик плюс 0x14.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4701">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="5fa9d-4702">Отправка сообщения Кпмконнектин, указанного в 2.2.3.15, на сервер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4702">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="5fa9d-4703">3.2.4.2.5 Отправка запроса Кпмфетчвалуеин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4703">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="5fa9d-4704">Если клиент получает от сервера ответ Кпмжетровсаут с полем состояния столбца, установленным в значение Статусдеферред (0x01), это означает, что значение свойства не было указано в поле Rows сообщения Кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4704">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="5fa9d-4705">В этом случае более высокий уровень обычно запрашивает у клиента протокола получение значения с помощью сообщения Кпмфетчвалуеин, а также предоставляет значение Пропспек и \_ WID для отложенного свойства, которое клиент протокола должен использовать в первом сообщении кпмфетчвалуеин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4705">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="5fa9d-4706">Если это первое сообщение Кпмфетчвалуеин, отправленное клиентом для запроса указанного свойства, клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4706">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4707">Установите все поля в сообщении, как указано в разделе 2.2.3.19.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4707">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="5fa9d-4708">Задайте \_ для кбсофар значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4708">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="5fa9d-4709">Установка текущих байтов, полученных в значение 0.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4709">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="5fa9d-4710">Отправка сообщения Кпмфетчвалуеин на сервер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4710">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="5fa9d-4711">3.2.4.2.6 Отправка запроса Кпмфрикурсорин</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4711">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="5fa9d-4712">Когда более высокий уровень больше не использует поисковый запрос, он может освободить ресурсы на сервере, запросив клиента отправить сообщение Кпмфрикурсорин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4712">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="5fa9d-4713">При получении этого запроса клиент должен отправить сообщение Кпмфрикурсорин, как указано в 2.2.3.28, на сервер, содержащий маркер, заданный верхним слоем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4713">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="5fa9d-4714">3.2.4.2.7 Отправка сообщения Кпмдисконнект</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4714">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="5fa9d-4715">Если более высокий уровень не содержит запросов для службы индексирования, чтобы освободить больше ресурсов сервера, приложение может запросить отправку клиентом сообщения Кпмдисконнект на сервер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4715">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="5fa9d-4716">При получении этого запроса клиент должен просто отправить сообщение по запросу.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4716">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="5fa9d-4717">Нет ответа на это сообщение от сервера.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4717">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="5fa9d-4718">Правила обработки сообщений 3.2.5 и последовательности</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4718">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="5fa9d-4719">Когда клиент получает ответ на сообщение от сервера, клиент должен использовать Последнее отправленное сообщение, чтобы определить, является ли сообщение, полученное от сервера, ожидаемым клиентом.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4719">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="5fa9d-4720">Все сообщения с \_ полем MSG, отличным от одного сообщения в последней отправке, должны игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4720">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="5fa9d-4721">3.2.5.1 получение ответа Кпмкреатекуерйоут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4721">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="5fa9d-4722">Когда клиент получает от сервера ответ на сообщение Кпмкреатекуерйоут, клиент должен возвратить \_ состояние и (если состояние прошло успешно) значения маркера курсора возвращаются к более высокому слою.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4722">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="5fa9d-4723">Дальнейшие действия выполняются на более высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4723">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="5fa9d-4724">Так как более высокий уровень имеет значение для структуры запроса, он всегда будет рассчитывать правильное число дескрипторов курсора, возвращаемых в сообщении Кпмкреатеауерйоут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4724">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="5fa9d-4725">Дескрипторы курсора возвращаются в следующем порядке: первый дескриптор относится к набору строк, к которому применяется unchapter, второй — к первому разбитому на разделы набору строк (т. е. Группирование результатов на основе первой категории, указанной в поле Категоризатионсет сообщения Кпмкреатекуерин).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4725">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="5fa9d-4726">Для информативных целей ожидается, что более высокие уровни могут выполнять следующие действия, но они не применяются клиентом CISP.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4726">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="5fa9d-4727">Использование Кпмсетбиндингсин для установки привязок для отдельных столбцов и выполнения последующих действий по пути запроса</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4727">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="5fa9d-4728">Используйте Кпмжеткуеристатусин для проверки хода выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4728">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="5fa9d-4729">Используйте Кпмратиофинишедин, чтобы запросить процент завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4729">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="5fa9d-4730">3.2.5.2 получение ответа Кпмжетровсаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4730">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="5fa9d-4731">Когда клиент получает от сервера ответ на сообщение Кпмжетровсаут, клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4731">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4732">Убедитесь, что \_ поле состояния в заголовке указывает на успешное выполнение или сбой.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4732">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="5fa9d-4733">Если \_ значение состояния "БУФЕР состояния \_ \_ слишком мало" \_ (0XC0000023), клиент должен проверить состояние последнего отправленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4733">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="5fa9d-4734">Если он не содержит сообщение Кпмжетровсин, то полученное сообщение должно игнорироваться без уведомления.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4734">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="5fa9d-4735">В противном случае клиент должен отправить на сервер новое сообщение Кпмжетровсин со всеми полями, идентичными сохраненному, за исключением того, что \_ КБРЕАДБУФФЕР должен быть увеличен на 512 (но не больше, чем 0x4000).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4735">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="5fa9d-4736">Если \_ состояние \_ "буфер состояния \_ слишком \_ мал" (0XC0000023), а Последнее отправленное сообщение уже имеет \_ кбреадбуффер, равное 0x4000 Client, должен сообщить об ошибке до более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4736">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="5fa9d-4737">Если \_ значением состояния является любое другое значение ошибки, клиент должен указать на сбой до более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4737">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="5fa9d-4738">Если \_ значение состояния указывает на успешное выполнение, результаты должны указывать на более высокий уровень, запрашивающий информацию, а дальнейшие действия — на более высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4738">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="5fa9d-4739">В информативных целях предполагается, что более высокие уровни обычно выполняют следующие действия, но не применяются клиентом протокола службы индексирования содержимого:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4739">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="5fa9d-4740">Если значения в строках представляют идентификаторы документов, главы или закладки обрабатывают более высокий уровень, обычно они сохраняются для использования в последующих операциях, в которых задействованы допустимые идентификаторы документов, разделы или маркеры закладок.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4740">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="5fa9d-4741">Более высокий уровень обычно сохраняет или отображает данные из значений строк или иным образом использует их.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4741">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="5fa9d-4742">Для значений, которые были помечены как отложенные выше, будут получены значения с помощью сообщений Кпмфетчвалуеин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4742">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="5fa9d-4743">Описание поиска возвращается к более высокому слою и может быть повторно использовано или проверено более высоким уровнем.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4743">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="5fa9d-4744">В информативных целях, если более высокий уровень запросил обработку глав и закладок, полученных в строках, это может сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4744">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="5fa9d-4745">Используйте Кпмжеткуеристатусексин, чтобы проверить ход выполнения запроса, а также дополнительные сведения о состоянии, например число отфильтрованных документов, документов, которые нужно отфильтровать, отношение документов, обрабатываемых запросом, общее число строк в запросе и расположение закладки в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4745">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="5fa9d-4746">Используйте Кпмжетнотифи, чтобы запросить у сервера уведомление клиента об изменениях набора строк.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4746">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="5fa9d-4747">Используйте Кпмжетаппроксиматепоситионин для запроса приблизительного расположения закладки в главе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4747">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="5fa9d-4748">Используйте Кпмкомпаребмкин для запроса сравнения двух закладок в главе.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4748">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="5fa9d-4749">Используйте Кпмрестартпоситионин, чтобы изменить положение курсора на начало набора строк на сервере.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4749">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="5fa9d-4750">3.2.5.3 получение ответа Кпмфетчвалуеаут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4750">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="5fa9d-4751">Когда клиент получает от сервера ответ на сообщение Кпмжетровсаут, клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4751">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="5fa9d-4752">Убедитесь, что \_ поле состояния в заголовке указывает на успешное выполнение или сбой.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4752">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="5fa9d-4753">В случае сбоя уведомить более высокий уровень.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4753">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="5fa9d-4754">В противном случае продолжайте ниже.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4754">Otherwise, continue below.</span></span>
-   <span data-ttu-id="5fa9d-4755">Проверьте \_ фвалуиксист и, если задано значение 0x00000000 уведомить более высокого уровня о том, что значение не найдено.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4755">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="5fa9d-4756">В противном случае добавьте \_ кбвалуе байт из управляемое vValue в текущее значение свойства.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4756">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="5fa9d-4757">Если \_ \_ фмориксистс имеет значение 0x00000001, то Увеличьте \_ текущие байты, полученные \_ кбвалуе, и отправьте сообщение кпмфетчвалуеин на сервер, установив \_ для Кбсофар значение Current bytes Received, \_ кбпропспек to Zero и \_ кбчунк до размера буфера, который требуется более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4757">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="5fa9d-4758">Если \_ фмориксистс имеет значение 0x00000000, укажите значение свойства из текущего значения свойства в более высокий уровень.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4758">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="5fa9d-4759">3.2.5.4 получение ответа Кпмфрикурсораут</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4759">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="5fa9d-4760">Когда клиент получает успешный ответ на сообщение Кпмфрикурсораут от сервера, клиент должен вернуть \_ значение ккурсорсремаининг к более высокому слою.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4760">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="5fa9d-4761">Следующие сведения предоставляются только в информативных целях и не применяются клиентом CISP.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4761">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="5fa9d-4762">Предполагается, что более высокий уровень отслеживает дескрипторы курсора и не использует уже освобожденные объекты.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4762">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="5fa9d-4763">Когда число \_ ккурсорсремаининг равно 0x00000000, более высокий уровень может использовать соединение для указания другого запроса (с помощью сообщения кпмкреатекуерин).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4763">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="5fa9d-4764">События таймера 3.2.6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4764">3.2.6 Timer Events</span></span>

<span data-ttu-id="5fa9d-4765">Нет.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4765">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="5fa9d-4766">3.2.7 другие локальные события</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4766">3.2.7 Other Local Events</span></span>

<span data-ttu-id="5fa9d-4767">Нет.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4767">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="5fa9d-4768">4. Примеры протокола</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4768">4 Protocol Examples</span></span>

-   [<span data-ttu-id="5fa9d-4769">4,1 Пример 1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4769">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="5fa9d-4770">4,2. Пример 2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4770">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="5fa9d-4771">4,1 Пример 1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4771">4.1 Example 1</span></span>

<span data-ttu-id="5fa9d-4772">В следующем примере мы рассмотрим ситуацию, в которой пользователь Джон на компьютере а хочет получить размеры файлов, содержащих слово «Microsoft», из набора документов, хранящихся на сервере X в системе каталогов.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4772">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="5fa9d-4773">Предположим, что компьютер A работает под управлением 32-разрядной операционной системы Windows XP, а компьютер X работает под управлением 32-разрядной операционной системы Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4773">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="5fa9d-4774">Пользователь запускает приложение поиска и вводит поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4774">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="5fa9d-4775">Приложение, в свою очередь, передает поисковый запрос клиенту протокола.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4775">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="5fa9d-4776">Клиент протокола устанавливает соединение с сервером индексирования X. Клиент протокола использует элемент \\ конфигурации канала именованного \\ канала \_ скадс для подключения к серверу X через SMB.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4776">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="5fa9d-4777">Затем клиент протокола подготавливает сообщение Кпмконнектин со следующими значениями:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4777">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="5fa9d-4778">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4778">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4779">**\_ сообщение имеет значение** 0x000000C8, указывающее, что это сообщение кпмконнектин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4779">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="5fa9d-4780">для параметра **\_ Status** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4780">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="5fa9d-4781">**\_ улчекксум** содержит контрольную сумму, вычисленную, как указано в разделе 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4781">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="5fa9d-4782">для **\_ ulReserved2** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4782">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="5fa9d-4783">Текст сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4783">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4784">**\_ иклиентверсион** имеет значение 0x00000008, указывающее, что сервер должен проверять поле контрольной суммы.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4784">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="5fa9d-4785">**\_ фклиентисремоте** имеет значение 0x00000001, указывающее, что сервер является удаленным сервером.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4785">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="5fa9d-4786">**\_ cbBlob1** задает размер в байтах Объединенных полей кпропсет, PropertySet1 и PropertySet2.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4786">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="5fa9d-4787">для **\_ cbBlob2** задано значение 0x00000004 (это означает отсутствие дополнительных наборов свойств).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4787">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="5fa9d-4788">**MachineName** имеет значение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4788">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="5fa9d-4789">Параметр **username** имеет значение John.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4789">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="5fa9d-4790">для **кпропсетс** задано значение 0x00000002.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4790">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="5fa9d-4791">Поле **PropertySet1** имеет тип кдбпропсет.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4791">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="5fa9d-4792">Структура Кдбпропсет, состоящая из поля PropertySet1, заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4792">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="5fa9d-4793">Для поля **гуидпропсет** установлено значение A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ фсЦифрмврк \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4793">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="5fa9d-4794">для поля **кпропертиес** установлено значение 0x00000004.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4794">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="5fa9d-4795">поле **апропс** представляет собой массив структур кдбпроп.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4795">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="5fa9d-4796">Для элемента **апропс \[ 0 \]** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4796">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="5fa9d-4797">**PropId** имеет значение 0x00000002 ( \_ \_ имя каталога CI DBPROP \_ ).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4797">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="5fa9d-4798">Для **дбпропоптионс** задано значение 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4798">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="5fa9d-4799">Для **дбпропстатус** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4799">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="5fa9d-4800">Для элемента **идентификатора столбца** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4800">For the **ColId** element:</span></span>
                -   <span data-ttu-id="5fa9d-4801">**элемент ekind** имеет значение 0X00000001 (дбкинд \_ GUID \_ PropID)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4801">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="5fa9d-4802">**GUID** имеет значение null (все нули), то есть значение применяется к запросу, а не только к одному столбцу.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4802">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="5fa9d-4803">для **улид** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4803">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="5fa9d-4804">Для элемента **управляемое vValue** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4804">For the **vValue** element:</span></span>
                -   <span data-ttu-id="5fa9d-4805">для **втипе** задано значение 0X001F (VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4805">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="5fa9d-4806">для **управляемое vValue** задано значение System, имя нужного каталога.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4806">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="5fa9d-4807">Для элемента **апропс \[ 1 \]** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4807">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="5fa9d-4808">**PropId** имеет значение 0x00000007 ( \_ \_ тип запроса DBPROP CI \_ )</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4808">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="5fa9d-4809">Для **дбпропоптионс** задано значение 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4809">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="5fa9d-4810">**Дбпропстатус** имеет значение to0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4810">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="5fa9d-4811">Для элемента **идентификатора столбца** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4811">For the **ColId** element:</span></span>
                -   <span data-ttu-id="5fa9d-4812">**элемент ekind** имеет значение 0X00000001 (дбкинд \_ GUID \_ PropID).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4812">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="5fa9d-4813">**GUID** имеет значение null (все нули), то есть значение применяется к запросу, а не только к одному столбцу.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4813">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="5fa9d-4814">для **улид** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4814">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="5fa9d-4815">Для элемента **управляемое vValue** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4815">For the **vValue** element:</span></span>
                -   <span data-ttu-id="5fa9d-4816">для **втипе** задано значение 0X0003 (VT \_ i4).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4816">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="5fa9d-4817">**управляемое vValue** имеет значение 0X00000000 (Цинормал), то есть это обычный запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4817">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="5fa9d-4818">Для элемента **апропс \[ 2 \]** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4818">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="5fa9d-4819">**PropId** имеет значение 0x00000004 ( \_ \_ Флаги области CI DBPROP \_ ).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4819">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="5fa9d-4820">Для **дбпропоптионс** задано значение 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4820">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="5fa9d-4821">Для **дбпропстатус** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4821">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="5fa9d-4822">Для элемента **идентификатора столбца** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4822">For the **ColId** element:</span></span>
                -   <span data-ttu-id="5fa9d-4823">**элемент ekind** имеет значение 0X00000001 (дбкинд \_ GUID \_ PropID).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4823">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="5fa9d-4824">**GUID** имеет значение null (все нули), то есть значение применяется к запросу, а не только к одному столбцу.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4824">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="5fa9d-4825">для **улид** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4825">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="5fa9d-4826">Для элемента **управляемое vValue** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4826">For the **vValue** element:</span></span>
                -   <span data-ttu-id="5fa9d-4827">**втипе**: 0x1003 ( \_ вектор \| VT, \_ i4)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4827">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="5fa9d-4828">**управляемое vValue**: 0x00000001/0x00000001 (один элемент со значением 1), то есть Поиск вложенных папок</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4828">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="5fa9d-4829">Для элемента **апропс \[ 3 \]** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4829">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="5fa9d-4830">**PropId**: 0X00000003 (DBPROP \_ CI \_ включает \_ области)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4830">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="5fa9d-4831">**Дбпропоптионс**: 0x0000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4831">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="5fa9d-4832">**Дбпропстатус**: 0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4832">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="5fa9d-4833">Для элемента **идентификатора столбца** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4833">For the **ColId** element:</span></span>
                -   <span data-ttu-id="5fa9d-4834">**элемент ekind** имеет значение 0X00000001 (дбкинд \_ GUID \_ PropID).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4834">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="5fa9d-4835">**GUID** имеет значение null (все нули), то есть значение применяется к запросу, а не только к одному столбцу.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4835">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="5fa9d-4836">для **улид** задано значение 0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4836">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="5fa9d-4837">Для элемента **управляемое vValue** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4837">For the **vValue** element:</span></span>
                -   <span data-ttu-id="5fa9d-4838">для **втипе** задано значение 0x101F (VT \_ vector \| VT \_ ).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4838">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="5fa9d-4839">**управляемое vValue** имеет значение 0x00000001/0x00000002/" \\ " (один элемент с строкой, завершающейся нулевым символом NULL), то есть в корневой области.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4839">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="5fa9d-4840">Поле **PropertySet2** имеет тип кдбпропсет.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4840">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="5fa9d-4841">Структура Кдбпропсет, состоящая из поля PropertySet1, заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4841">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="5fa9d-4842">Для **гуидпропсет** задано значение AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ Цифрмврккоре \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4842">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="5fa9d-4843">поле **кпропертиес** имеет значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4843">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="5fa9d-4844">Поле **апропс** представляет собой массив структур кдбпроп.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4844">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="5fa9d-4845">Для элемента **апропс \[ 0 \]** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4845">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="5fa9d-4846">**PropId** имеет значение 0X00000002 (DBPROP \_ Machine).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4846">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="5fa9d-4847">Для **дбпропоптионс** задано значение 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4847">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="5fa9d-4848">Для **дбпропстатус** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4848">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="5fa9d-4849">Для элемента **идентификатора столбца** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4849">For the **ColId** element:</span></span>
                -   <span data-ttu-id="5fa9d-4850">**элемент ekind** имеет значение 0X00000001 (дбкинд \_ GUID \_ PropID),</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4850">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="5fa9d-4851">**GUID** имеет значение null (все нули), то есть значение применяется к запросу, а не только к одному столбцу.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4851">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="5fa9d-4852">для **улид** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4852">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="5fa9d-4853">Для элемента **управляемое vValue** :</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4853">For **vValue** element:</span></span>
                -   <span data-ttu-id="5fa9d-4854">**втипе**: 0X0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4854">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="5fa9d-4855">**управляемое vValue**: 0x04/"x" (4 байта/строка в Юникоде, заканчивающаяся нулем), означающее "X" — имя сервера.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4855">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="5fa9d-4856">для поля **цекстпропсет** установлено значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4856">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="5fa9d-4857">Массив **апропертисетс** не существует.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4857">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="5fa9d-4858">При необходимости заполняются различные поля заполнения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4858">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="5fa9d-4859">Сообщение отправляется на сервер.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4859">The message is sent to the server.</span></span>

4.  <span data-ttu-id="5fa9d-4860">Сервер проверяет правильность **\_ улчекксум** , проверяет, имеет ли пользователь разрешение на выполнение этого запроса, и реагирует на сообщение кпмконнектаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4860">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="5fa9d-4861">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4861">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4862">**\_ сообщение имеет значение** 0x000000C8, указывающее, что это сообщение кпмконнектаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4862">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="5fa9d-4863">для параметра **\_ Status** задано значение 0x0000000, означающее успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4863">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="5fa9d-4864">**\_ улчекксум** имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4864">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="5fa9d-4865">для **\_ ulReserved2** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4865">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="5fa9d-4866">Текст сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4866">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4867">для поля **\_ serverVersion** установлено значение 0x00000007 (32-разрядная версия windows XP или 32-разрядная версия Windows Server 2003).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4867">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="5fa9d-4868">**\_ зарезервированные** поля заполняются произвольными данными.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4868">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="5fa9d-4869">Клиент готовит сообщение Кпмкреатекуерин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4869">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="5fa9d-4870">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4870">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4871">**\_ сообщение имеет значение** 0x000000CA, указывающее, что это сообщение кпмкреатекуерин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4871">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="5fa9d-4872">для параметра **\_ Status** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4872">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="5fa9d-4873">**\_ улчекксум** содержит контрольную сумму, вычисленную в соответствии с 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4873">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="5fa9d-4874">для **\_ ulReserved2** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4874">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="5fa9d-4875">Текст сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4875">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4876">Поле **size (размер** ) задает размер остальной части сообщения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4876">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="5fa9d-4877">Для поля **кколумнсетпресент** задано значение 0x01.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4877">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="5fa9d-4878">Поле набора **столбцов** имеет тип кколумнсет.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4878">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="5fa9d-4879">Структура Кколумнсет, включающая в себя это поле, задается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4879">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="5fa9d-4880">поле **\_ Count** имеет значение 0x00000001, указывающее, что возвращается один столбец.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4880">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="5fa9d-4881">Массив **индексов** — это 0x00000000, указывающий первую запись в \_ апропспек.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4881">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="5fa9d-4882">Поле **крестриктионпресент** имеет значение 0x01, указывающее на наличие поля **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4882">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="5fa9d-4883">Поле **ограничения** имеет тип крестриктион и имеет значение:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4883">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="5fa9d-4884">для **\_ ултипе** задано значение 0x00000004 (ртконтент).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4884">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="5fa9d-4885">для параметра **\_ Weight** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4885">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="5fa9d-4886">Оставшаяся часть поля содержит структуру Кконтентрестриктион:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4886">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="5fa9d-4887">**\_ Задано значение GUID** B725F130-47EF-101A-A5F1-02608c9eebac/0X00000001 (для прспек \_ PropID)/0x13, представляющее тело документа.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4887">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="5fa9d-4888">Для **\_ CC** задано значение 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4888">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="5fa9d-4889">для **\_ пвксфрасе** задана строка «Microsoft».</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4889">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="5fa9d-4890">для **\_ LCID** задано значение 0X409 (для английского языка).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4890">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="5fa9d-4891">для **\_ улженератемесод** задано значение 0x00000000 (точное совпадение).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4891">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="5fa9d-4892">**Ксортпресент** имеет значение 0x00.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4892">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="5fa9d-4893">**Ккатегоризатионсетпресент** имеет значение 0x00.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4893">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="5fa9d-4894">**Ровсетпропертиес** задается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4894">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="5fa9d-4895">**\_ убулеаноптионс** имеет значение 0x00000001 (последовательный).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4895">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="5fa9d-4896">для **\_ улмаксопенровс** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4896">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="5fa9d-4897">для **\_ улмеморюсаже** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4897">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="5fa9d-4898">\_для **кмаксресултс** задано значение 0x00000100 (возвращается не более 256 строк).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4898">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="5fa9d-4899">для **\_ ккмдтимеаут** задано значение 0x00000000 (никогда не время ожидания).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4899">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="5fa9d-4900">**Пидмаппер** имеет значение:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4900">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="5fa9d-4901">для параметра **\_ Count** задано значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4901">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="5fa9d-4902">**\_ апропспек** имеет значение GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC/0X00000001 (для прспек \_ PropID)/0x0000000c, которое представляет свойство размера файла Windows.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4902">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="5fa9d-4903">Сервер обрабатывает его и реагирует на сообщение Кпмкреатекуерйоут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4903">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="5fa9d-4904">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4904">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4905">**\_ сообщение имеет значение** 0x000000CA, указывающее, что это сообщение кпмкреатекуерйоут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4905">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="5fa9d-4906">**\_ состояние** установлено в значение Success.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4906">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="5fa9d-4907">**\_ улчекксум** имеет значение 0x00000000 (или любое другое произвольное значение).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4907">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="5fa9d-4908">**\_ ulReserved2** имеет значение 0x00000000 (или любое другое произвольное значение).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4908">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="5fa9d-4909">Текст сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4909">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4910">**\_ фтруесекеунтиал** имеет значение 0x00000000, указывающее, что запрос может использовать индекс.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4910">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="5fa9d-4911">**\_ фворкидуникуе** имеет значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4911">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="5fa9d-4912">Массив **акурсорс** содержит только один элемент, представляющий маркер курсора для этого запроса.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4912">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="5fa9d-4913">Значение зависит от состояния сервера.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4913">The value depends on the state of the server.</span></span> <span data-ttu-id="5fa9d-4914">Предположим, что возвращаемое значение — 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4914">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="5fa9d-4915">Клиент выдает сообщение запроса Кпмсетбиндингсин для определения формата строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4915">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="5fa9d-4916">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4916">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4917">**\_ сообщение имеет значение** 0x000000D0, указывающее, что это сообщение кпмсетбиндингсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4917">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="5fa9d-4918">**\_ состояние** установлено в значение Success.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4918">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="5fa9d-4919">**\_ улчекксум** имеет значение 0x00000000 (или любое другое произвольное значение).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4919">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="5fa9d-4920">**\_ ulReserved2** имеет значение 0x00000000 (или любое другое произвольное значение).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4920">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="5fa9d-4921">Текст сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4921">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4922">для **\_ хкурсор** задано значение 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4922">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="5fa9d-4923">для **\_ кбров** задано значение 0x10 (достаточно большое, чтобы вместить столбцы).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4923">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="5fa9d-4924">**\_ кббиндингдеск** задается в сочетании с размером полей **\_ кколумнс** и **\_ аколумнс** .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4924">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="5fa9d-4925">**\_ кколумнс** имеет значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4925">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="5fa9d-4926">Массив **\_ аколумнс** имеет значение, содержащее одну структуру ктаблеколумн, содержащую:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4926">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="5fa9d-4927">**\_ Пропспек** имеет значение GUID b725f130-47ef-101A-A5-F1-02608c9eebac/0X00000001 (для прспек \_ PropID)/0x0000000c, которое представляет свойство размера файла Windows.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4927">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="5fa9d-4928">для **\_ втипе** задано значение 0x0015 (VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4928">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="5fa9d-4929">Для **\_ валуеусед** задано значение 0x01 (столбец передается в строке).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4929">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="5fa9d-4930">Для **\_ валуеоффсет** задано значение 0x0002 (в начале строки).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4930">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="5fa9d-4931">Для **\_ валуесизе** задано значение 0X08 (размер VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4931">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="5fa9d-4932">Для **\_ статусусед** задано значение 0x01.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4932">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="5fa9d-4933">Для **\_ статусоффсет** задано значение 0x0A.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4933">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="5fa9d-4934">**\_ Ленгсусед** имеет значение 0x00.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4934">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="5fa9d-4935">Сервер обрабатывает его и реагирует на сообщение Кпмсетбиндингсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4935">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="5fa9d-4936">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4936">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4937">для **\_ сообщения** задано значение 0x000000D0.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4937">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="5fa9d-4938">**\_ состояние** установлено в значение Success.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4938">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="5fa9d-4939">**\_ улчекксум** имеет значение 0x00000000 (или любое другое произвольное значение).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4939">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="5fa9d-4940">**\_ ulReserved2** имеет значение 0x00000000 (или любое другое произвольное значение).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4940">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="5fa9d-4941">Клиент выдает сообщение запроса Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4941">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="5fa9d-4942">Предположим, что клиент готов принять 100 строк на этом этапе и хочет, чтобы они были в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4942">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="5fa9d-4943">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4943">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4944">**\_ сообщение имеет значение** 0x000000CC, указывающее, что это сообщение кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4944">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="5fa9d-4945">для параметра **\_ Status** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4945">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="5fa9d-4946">**\_ улчекксум** содержит контрольную сумму, вычисленную в соответствии с разделом 0.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4946">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="5fa9d-4947">для **\_ ulReserved2** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4947">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="5fa9d-4948">Текст сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4948">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4949">для **\_ хкурсор** задано значение 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4949">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="5fa9d-4950">для **\_ кровстотрансфер** задано значение 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4950">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="5fa9d-4951">**\_ кроввидс** имеет значение 0x00000010 (из привязок).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4951">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="5fa9d-4952">для **\_ кбсик** задано значение 0x14, которое равно размеру полей eType, \_ CHAP и кровсикнекст.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4952">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="5fa9d-4953">для **\_ кбресервед** задано значение 0x18 (0x14 Plus \_ кбсик).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4953">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="5fa9d-4954">для **\_ кбреадбуффер** задано значение 0x800 (0x64 \* 0x10 округляется до следующего кратного 0x200).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4954">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="5fa9d-4955">для **\_ улклиентбасе** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4955">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="5fa9d-4956">**\_ фбвдфетч** имеет значение 0x00000000, указывающее, что строки должны быть получены в прямом порядке.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4956">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="5fa9d-4957">**eType** имеет значение 0x0000001, указывающее, что клиент хочет получить следующие строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4957">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="5fa9d-4958">для параметра **\_ CHAP** задано значение 0 (не в разделе результат).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4958">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="5fa9d-4959">Для **сикдескриптион** задано значение кровсикнекст.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4959">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="5fa9d-4960">Структура Кровсикнекст содержит следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4960">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="5fa9d-4961">Для **Цитблчапт** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4961">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="5fa9d-4962">для **\_ хрегион** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4962">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="5fa9d-4963">**\_ кскип** имеет значение 0, указывающее, что клиенту не нужно пропускать строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4963">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="5fa9d-4964">Сервер обрабатывает его и реагирует на сообщение Кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4964">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="5fa9d-4965">Предположим, что сервер нашел 100 документов, содержащих слово Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4965">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="5fa9d-4966">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4966">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4967">**\_ сообщение имеет значение** 0x000000CC, указывающее, что это сообщение кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4967">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="5fa9d-4968">**\_ состояние** установлено в значение Success.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4968">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="5fa9d-4969">для **\_ улчекксум** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4969">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="5fa9d-4970">для **\_ ulReserved2** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4970">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="5fa9d-4971">Текст сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4971">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4972">Для **\_ кровсретурнед** задано значение 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4972">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="5fa9d-4973">**eType** имеет значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4973">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="5fa9d-4974">для параметра **\_ CHAP** задано значение 0x00000000 (не в разделе результат).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4974">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="5fa9d-4975">**Сикдескриптион** содержит структуру кровсикнекст, заполненную следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4975">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="5fa9d-4976">Для **Цитблчапт** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4976">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="5fa9d-4977">для **\_ хрегион** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4977">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="5fa9d-4978">**\_ кскип** имеет значение 0, указывающее, что клиенту не нужно пропускать строки.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4978">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="5fa9d-4979">**Строки** содержат размер 100 документов, содержащих слово «Microsoft».</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4979">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="5fa9d-4980">Так как это данные фиксированного размера, они просто структурированы как список из 100, 8-байтных целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4980">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="5fa9d-4981">Клиент отправляет сообщение Кпмдисконнект, чтобы завершить соединение.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4981">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="5fa9d-4982">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4982">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="5fa9d-4983">**\_ сообщение имеет значение** 0x000000C9, указывающее, что это сообщение кпмдисконнект.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4983">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="5fa9d-4984">для параметра **\_ Status** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4984">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="5fa9d-4985">для **\_ улчекксум** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4985">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="5fa9d-4986">Сервер обрабатывает сообщение и удаляет все состояние клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4986">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="5fa9d-4987">4,2. Пример 2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4987">4.2 Example 2</span></span>

<span data-ttu-id="5fa9d-4988">В предыдущем примере запрос был достаточно простым.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4988">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="5fa9d-4989">Давайте теперь рассмотрим немного более сложный запрос.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4989">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="5fa9d-4990">Предположим, что пользователь хочет получить размер документов, содержащих оба слова: "Microsoft" и "Office".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4990">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="5fa9d-4991">Это указывается путем изменения поля ограничения, содержащегося в сообщении Кпмкреатекуерин, отправленном на шаге 5, следующим образом.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4991">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="5fa9d-4992">Поле **ограничения** имеет тип крестриктион и имеет значение:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4992">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="5fa9d-4993">для **\_ ултипе** задано значение 0x00000004 (ртанд).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4993">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="5fa9d-4994">для параметра **\_ Weight** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4994">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="5fa9d-4995">Оставшаяся часть поля содержит структуру Кнодерестриктион:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4995">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="5fa9d-4996">**\_ кноде** имеет значение 0x00000002, указывающее, что в массиве паноде есть два узла.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4996">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="5fa9d-4997">Поле **\_ паноде** представляет собой массив из двух структур крестриктион.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4997">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="5fa9d-4998">**\_ паноде \[ 0 \]** содержит:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4998">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="5fa9d-4999">для **\_ ултипе** задано значение 0x00000004 (ртконтент).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-4999">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="5fa9d-5000">для параметра **\_ Weight** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5000">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="5fa9d-5001">Оставшаяся часть поля содержит структуру Кконтентрестриктион:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5001">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="5fa9d-5002">Для **\_ свойства** задано значение GUID b725f130-47ef-101A-a5f1-02608c9eebac/0X00000001 (для прспек \_ PropID)/0x13.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5002">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="5fa9d-5003">Для **\_ CC** задано значение 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5003">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="5fa9d-5004">для **\_ пвксфрасе** задана строка «Microsoft».</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5004">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="5fa9d-5005">для **\_ LCID** задано значение 0X409 (для английского языка).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5005">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="5fa9d-5006">для **\_ улженератемесод** задано значение 0x00000000 (точное совпадение).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5006">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="5fa9d-5007">**\_ паноде \[ 1 \]** содержит:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5007">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="5fa9d-5008">для **\_ ултипе** задано значение 0x00000004 (ртконтент).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5008">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="5fa9d-5009">для параметра **\_ Weight** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5009">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="5fa9d-5010">Оставшаяся часть поля содержит структуру Кконтентрестриктион:</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5010">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="5fa9d-5011">Для **\_ свойства** задано значение GUID b725f130-47ef-101A-a5f1-02608c9eebac/0X00000001 (для прспек \_ PropID)/0x13.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5011">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="5fa9d-5012">Для **\_ CC** задано значение 0x00000006.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5012">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="5fa9d-5013">для **\_ пвксфрасе** задана строка "Office".</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5013">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="5fa9d-5014">для **\_ LCID** задано значение 0X409 (для английского языка).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5014">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="5fa9d-5015">для **\_ улженератемесод** задано значение 0x00000000 (точное совпадение).</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5015">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="5fa9d-5016">5. Безопасность</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5016">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="5fa9d-5017">5.1. Вопросы безопасности для разработчиков</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5017">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="5fa9d-5018">Реализации индексирования, для которых требуется индексирование защищенного содержимого, следует использовать контекст пользователя, предоставляемый SMB \[ MS-SMB, \] чтобы обрезать результаты поиска и возвратить только те, которые доступны вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5018">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="5fa9d-5019">5.2. Индекс параметров безопасности</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5019">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="5fa9d-5020">Параметр безопасности</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5020">Security Parameter</span></span>  | <span data-ttu-id="5fa9d-5021">Section</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5021">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="5fa9d-5022">Уровень олицетворения</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5022">Impersonation level</span></span> | <span data-ttu-id="5fa9d-5023">2.1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5023">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="5fa9d-5024">6 индекс поведения, зависящего от версии</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5024">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="5fa9d-5025">Поведение конкретной версии</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5025">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="5fa9d-5026">Section</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5026">Section</span></span>   | <span data-ttu-id="5fa9d-5027">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5027">Windows 2000</span></span> | <span data-ttu-id="5fa9d-5028">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5028">Windows XP</span></span> | <span data-ttu-id="5fa9d-5029">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5029">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="5fa9d-5030">Этот Протокол реализован в Windows 2000, Windows XP, Windows Server 2003 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5030">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="5fa9d-5031">1.3.2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5031">1.3.2</span></span>     | <span data-ttu-id="5fa9d-5032">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5032">X</span></span>            | <span data-ttu-id="5fa9d-5033">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5033">X</span></span>          | <span data-ttu-id="5fa9d-5034">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5034">X</span></span>                   |
| <span data-ttu-id="5fa9d-5035">Приложения обычно взаимодействуют с оболочкой интерфейса OLE DB</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5035">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="5fa9d-5036">1.4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5036">1.4</span></span>       | <span data-ttu-id="5fa9d-5037">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5037">X</span></span>            | <span data-ttu-id="5fa9d-5038">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5038">X</span></span>          | <span data-ttu-id="5fa9d-5039">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5039">X</span></span>                   |
| <span data-ttu-id="5fa9d-5040">Значения NTSTATUS</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5040">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="5fa9d-5041">1.8</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5041">1.8</span></span>       | <span data-ttu-id="5fa9d-5042">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5042">X</span></span>            | <span data-ttu-id="5fa9d-5043">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5043">X</span></span>          | <span data-ttu-id="5fa9d-5044">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5044">X</span></span>                   |
| <span data-ttu-id="5fa9d-5045">Клиент устанавливает \_ поле состояния в каждом заголовке сообщения.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5045">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="5fa9d-5046">2.2.2</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5046">2.2.2</span></span>     | <span data-ttu-id="5fa9d-5047">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5047">X</span></span>            | <span data-ttu-id="5fa9d-5048">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5048">X</span></span>          | <span data-ttu-id="5fa9d-5049">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5049">X</span></span>                   |
| <span data-ttu-id="5fa9d-5050">значение Кпендингсканс обычно равно нулю</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5050">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="5fa9d-5051">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5051">2.2.3.1</span></span>   | <span data-ttu-id="5fa9d-5052">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5052">X</span></span>            | <span data-ttu-id="5fa9d-5053">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5053">X</span></span>          | <span data-ttu-id="5fa9d-5054">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5054">X</span></span>                   |
| <span data-ttu-id="5fa9d-5055">значение Иклиентверсион</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5055">iClientVersion value</span></span>                                                                              | <span data-ttu-id="5fa9d-5056">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5056">2.2.3.6</span></span>   | <span data-ttu-id="5fa9d-5057">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5057">X</span></span>            | <span data-ttu-id="5fa9d-5058">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5058">X</span></span>          | <span data-ttu-id="5fa9d-5059">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5059">X</span></span>                   |
| <span data-ttu-id="5fa9d-5060">\_значение Кбчунк</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5060">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="5fa9d-5061">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5061">2.2.3.19</span></span>  | <span data-ttu-id="5fa9d-5062">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5062">X</span></span>            | <span data-ttu-id="5fa9d-5063">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5063">X</span></span>          | <span data-ttu-id="5fa9d-5064">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5064">X</span></span>                   |
| <span data-ttu-id="5fa9d-5065">32-разрядные и 64-разрядные адреса памяти</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5065">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="5fa9d-5066">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5066">3.2.4.2.4</span></span> | <span data-ttu-id="5fa9d-5067">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5067">X</span></span>            | <span data-ttu-id="5fa9d-5068">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5068">X</span></span>          | <span data-ttu-id="5fa9d-5069">X</span><span class="sxs-lookup"><span data-stu-id="5fa9d-5069">X</span></span>                   |



 

 

 





