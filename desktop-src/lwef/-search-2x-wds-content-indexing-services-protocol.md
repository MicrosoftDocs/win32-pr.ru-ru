---
title: Протокол служб индексирования содержимого
description: Этот документ является спецификацией протокола службы индексирования содержимого.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14573dac5a7a6818234c086d05b52e5b81c2a1c1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119739"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="a573a-103">Протокол служб индексирования содержимого</span><span class="sxs-lookup"><span data-stu-id="a573a-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="a573a-104">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a573a-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="a573a-105">В более поздних выпусках используйте вместо этого [Поиск Windows](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="a573a-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="a573a-106">Спецификация протокола, версия 0,12</span><span class="sxs-lookup"><span data-stu-id="a573a-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="a573a-107">1 Введение</span><span class="sxs-lookup"><span data-stu-id="a573a-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="a573a-108">1.1. Глоссарий</span><span class="sxs-lookup"><span data-stu-id="a573a-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="a573a-109">1.2. Ссылки</span><span class="sxs-lookup"><span data-stu-id="a573a-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="a573a-110">Общие сведения о протоколе 1,3 (краткий обзор)</span><span class="sxs-lookup"><span data-stu-id="a573a-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="a573a-111">1.4. Связь с другими протоколами</span><span class="sxs-lookup"><span data-stu-id="a573a-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="a573a-112">1,5. Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="a573a-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="a573a-113">1.6. Постановление о пределах применения</span><span class="sxs-lookup"><span data-stu-id="a573a-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="a573a-114">1.7. Управление версиями и согласованность функций</span><span class="sxs-lookup"><span data-stu-id="a573a-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="a573a-115">1.8. Расширяемые поля поставщика</span><span class="sxs-lookup"><span data-stu-id="a573a-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="a573a-116">1.9. Назначения стандартов</span><span class="sxs-lookup"><span data-stu-id="a573a-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="a573a-117">2. Сообщения</span><span class="sxs-lookup"><span data-stu-id="a573a-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="a573a-118">2.1. Транспортировка</span><span class="sxs-lookup"><span data-stu-id="a573a-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="a573a-119">2.2. Синтаксис сообщений</span><span class="sxs-lookup"><span data-stu-id="a573a-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="a573a-120">3. Сведения о протоколе</span><span class="sxs-lookup"><span data-stu-id="a573a-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="a573a-121">Сведения о сервере 3,1</span><span class="sxs-lookup"><span data-stu-id="a573a-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="a573a-122">3,2. сведения о клиенте</span><span class="sxs-lookup"><span data-stu-id="a573a-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="a573a-123">4. Примеры протокола</span><span class="sxs-lookup"><span data-stu-id="a573a-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="a573a-124">4,1 Пример 1</span><span class="sxs-lookup"><span data-stu-id="a573a-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="a573a-125">4,2. Пример 2</span><span class="sxs-lookup"><span data-stu-id="a573a-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="a573a-126">5. Безопасность</span><span class="sxs-lookup"><span data-stu-id="a573a-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="a573a-127">5.1. Вопросы безопасности для разработчиков</span><span class="sxs-lookup"><span data-stu-id="a573a-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="a573a-128">5.2. Индекс параметров безопасности</span><span class="sxs-lookup"><span data-stu-id="a573a-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="a573a-129">6 индекс поведения, зависящего от версии</span><span class="sxs-lookup"><span data-stu-id="a573a-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="a573a-130">Этот документ является спецификацией протокола службы индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="a573a-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="a573a-131">Документация по протоколу сервера Workgroup Server (WSPP) предназначена для использования в сочетании с документацией по общедоступным стандартам, графикой программирования сети и концепциями распределенных систем Windows Workgroup, и предполагает, что читатель знаком с упомянутым материалом или имеет немедленный доступ к нему.</span><span class="sxs-lookup"><span data-stu-id="a573a-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="a573a-132">Спецификация протокола WSPP не требует использования средств программирования Майкрософт или сред программирования, чтобы лицензироваться на разработку реализации.</span><span class="sxs-lookup"><span data-stu-id="a573a-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="a573a-133">Лицензии, имеющие доступ к средствам и средам программирования Майкрософт, могут воспользоваться преимуществами этих средств.</span><span class="sxs-lookup"><span data-stu-id="a573a-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="a573a-134">1. Введение</span><span class="sxs-lookup"><span data-stu-id="a573a-134">1 Introduction</span></span>

-   [<span data-ttu-id="a573a-135">1.1. Глоссарий</span><span class="sxs-lookup"><span data-stu-id="a573a-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="a573a-136">1.2. Ссылки</span><span class="sxs-lookup"><span data-stu-id="a573a-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="a573a-137">Общие сведения о протоколе 1,3 (краткий обзор)</span><span class="sxs-lookup"><span data-stu-id="a573a-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="a573a-138">1.4. Связь с другими протоколами</span><span class="sxs-lookup"><span data-stu-id="a573a-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="a573a-139">1,5. Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="a573a-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="a573a-140">1.6. Постановление о пределах применения</span><span class="sxs-lookup"><span data-stu-id="a573a-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="a573a-141">1.7. Управление версиями и согласованность функций</span><span class="sxs-lookup"><span data-stu-id="a573a-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="a573a-142">1.8. Расширяемые поля поставщика</span><span class="sxs-lookup"><span data-stu-id="a573a-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="a573a-143">1.9. Назначения стандартов</span><span class="sxs-lookup"><span data-stu-id="a573a-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="a573a-144">1.1. Глоссарий</span><span class="sxs-lookup"><span data-stu-id="a573a-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="a573a-145">Следующие термины определены в разделе глоссария в \[ MS-sys \] :</span><span class="sxs-lookup"><span data-stu-id="a573a-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="a573a-146">Код GUID</span><span class="sxs-lookup"><span data-stu-id="a573a-146">GUID</span></span>
> -   <span data-ttu-id="a573a-147">Прямой порядок байтов</span><span class="sxs-lookup"><span data-stu-id="a573a-147">Little Endian</span></span>
> -   <span data-ttu-id="a573a-148">Именованный канал</span><span class="sxs-lookup"><span data-stu-id="a573a-148">Named Pipe</span></span>
> -   <span data-ttu-id="a573a-149">Путь</span><span class="sxs-lookup"><span data-stu-id="a573a-149">Path</span></span>

 

<span data-ttu-id="a573a-150">**Binding**: запрос на включение определенного **столбца** в возвращенный **набор строк** .</span><span class="sxs-lookup"><span data-stu-id="a573a-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="a573a-151">**Привязка** указывает свойство, включаемое в результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="a573a-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="a573a-152">**Bookmark**: маркер, однозначно определяющий строку в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="a573a-153">**Catalog**— единица организации высшего уровня в службе индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="a573a-154">Он представляет собой набор индексированных документов, по которым можно выполнять запросы с помощью протокола службы индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="a573a-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="a573a-155">**Категория**: Иерархическое группирование строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="a573a-156">Например, результат запроса, содержащий столбцы Author и Title, можно классифицировать на основе автора.</span><span class="sxs-lookup"><span data-stu-id="a573a-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="a573a-157">Каждая группа строк, содержащая одно и то же значение для автора, будет составлять категорию.</span><span class="sxs-lookup"><span data-stu-id="a573a-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="a573a-158">**Глава** : диапазон **строк** в наборе **строк** .</span><span class="sxs-lookup"><span data-stu-id="a573a-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="a573a-159">**Column**: контейнер для одного типа данных в **строке** .</span><span class="sxs-lookup"><span data-stu-id="a573a-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="a573a-160">Столбцы сопоставляются с именами свойств и указывают, какие свойства используются для элементов **дерева** **команд** в поисковом запросе.</span><span class="sxs-lookup"><span data-stu-id="a573a-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="a573a-161">**Дерево команд**: сочетание **ограничений** , **категорий** и **порядков сортировки** , заданных для поискового запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="a573a-162">**Cursor**: сущность, используемая в качестве механизма для работы с одной **строкой** или небольшим блоком **строк** за раз в наборе данных, возвращаемых в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="a573a-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="a573a-163">**Курсор** располагается на одной **строке** в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="a573a-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="a573a-164">После того как **курсор** находится в строке, операции могут выполняться над этой **строкой** или в блоке **строк** , начиная с этой позиции.</span><span class="sxs-lookup"><span data-stu-id="a573a-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="a573a-165">**Handle**— маркер, который можно использовать для распознавания и доступа к **курсорам** , **главам** и **закладкам** .</span><span class="sxs-lookup"><span data-stu-id="a573a-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="a573a-166">**Index**: Постоянная структура, содержащая текстовое содержимое, извлеченное из файлов **службой индексирования** .</span><span class="sxs-lookup"><span data-stu-id="a573a-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="a573a-167">Сюда входит список слов, которые хранятся вместе с содержащимся именем файла, расположением Word и **языковым стандартом** .</span><span class="sxs-lookup"><span data-stu-id="a573a-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="a573a-168">**Индексирование**. процесс извлечения текста и свойств из файлов и сохранения извлеченных значений в **индексах** (для текста) и в **кэше свойств** (для свойств).</span><span class="sxs-lookup"><span data-stu-id="a573a-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="a573a-169">**Служба индексирования**: служба, которая создает индексированные **каталоги** для содержимого и свойств файловых систем.</span><span class="sxs-lookup"><span data-stu-id="a573a-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="a573a-170">Приложения могут искать в каталогах сведения из файлов в индексированной файловой системе.</span><span class="sxs-lookup"><span data-stu-id="a573a-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="a573a-171">**Языковой стандарт**: идентификатор, как указано в \[ приложении MS-GPSI, \] который указывает предпочтения, связанные с языком.</span><span class="sxs-lookup"><span data-stu-id="a573a-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="a573a-172">Эти настройки указывают, как форматируются даты и время, элементы сортируются в алфавитном порядке, сравниваются по строкам и т. д.</span><span class="sxs-lookup"><span data-stu-id="a573a-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="a573a-173">**Запрос на естественном языке**. запрос, построенный на языке человека вместо синтаксиса запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="a573a-174">**Пропускаемое слово**: слово, которое игнорируется службой индексирования, если оно существует в **ограничениях** , указанных для поискового запроса, так как у него малое значение для дискриминатора.</span><span class="sxs-lookup"><span data-stu-id="a573a-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="a573a-175">Примеры на английском языке: "a", "and" и "The".</span><span class="sxs-lookup"><span data-stu-id="a573a-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="a573a-176">**Кэш свойств**: кэш свойств файла, извлеченных **службой индексирования** .</span><span class="sxs-lookup"><span data-stu-id="a573a-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="a573a-177">**Индексирование свойств**. процесс создания **индекса** **свойств типа «значение** » документа, включая автора, тему, тип, число слов, число печатных страниц и другие свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="a573a-178">**Ограничение**: набор условий, которым должен соответствовать файл, включаемый в результаты поиска, возвращенные **службой индексирования** в ответ на поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="a573a-179">**Ограничение** ограничивает фокус поискового запроса, ограничивая файлы, которые **Служба индексирования** будет включать в результаты поиска, только те, которые соответствуют условиям.</span><span class="sxs-lookup"><span data-stu-id="a573a-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="a573a-180">**Row**: коллекция **столбцов** , содержащая значения свойств, которые описывают отдельный файл из набора файлов, соответствующих **ограничениям** , указанным в поисковом запросе, отправленном в **службу индексирования** .</span><span class="sxs-lookup"><span data-stu-id="a573a-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="a573a-181">**Набор строк: набор** **строк** , возвращаемых в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="a573a-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="a573a-182">**Порядок сортировки**. набор правил в поисковом запросе, который определяет порядок строк в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="a573a-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="a573a-183">Каждое правило состоит из свойства (имя, размер и т. д.) и направления упорядочения (по возрастанию или по убыванию).</span><span class="sxs-lookup"><span data-stu-id="a573a-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="a573a-184">Несколько правил применяются последовательно.</span><span class="sxs-lookup"><span data-stu-id="a573a-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="a573a-185">**Свойство текстового типа**: свойство, которое описывает содержимое документа и имеет только неформатированный текст, связанный с его именем.</span><span class="sxs-lookup"><span data-stu-id="a573a-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="a573a-186">**Свойство типа значения**— свойство, которое описывает один атрибут всего документа.</span><span class="sxs-lookup"><span data-stu-id="a573a-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="a573a-187">Свойство типа значения имеет идентификатор типа данных и значение этого типа данных, связанное с его именем.</span><span class="sxs-lookup"><span data-stu-id="a573a-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="a573a-188">**Виртуальный корневой каталог**: альтернативный путь к папке.</span><span class="sxs-lookup"><span data-stu-id="a573a-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="a573a-189">У физической папки может быть не более одного виртуального корня.</span><span class="sxs-lookup"><span data-stu-id="a573a-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="a573a-190">Пути, начинающиеся с виртуального корня, называются виртуальными путями.</span><span class="sxs-lookup"><span data-stu-id="a573a-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="a573a-191">Например,/сервер/ванитирут может быть виртуальным корнем C: \\ IIS \\ Web \\ папка1.</span><span class="sxs-lookup"><span data-stu-id="a573a-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="a573a-192">Затем файл C: \\ IIS \\ web \\ папка1 \\default.htm будет иметь виртуальный путь/сервер/ванитирут/default.htm.</span><span class="sxs-lookup"><span data-stu-id="a573a-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="a573a-193">**Может**, не должен, не обязательно: эти термины (во всех прописных) используются, как описано в \[ RFC2119 \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="a573a-194">Во всех необязательных инструкциях используются термины MAY (ВОЗМОЖНО), SHOULD (СЛЕДУЕТ) или SHOULD NOT (НЕ СЛЕДУЕТ).</span><span class="sxs-lookup"><span data-stu-id="a573a-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="a573a-195">1.2. Ссылки</span><span class="sxs-lookup"><span data-stu-id="a573a-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="a573a-196">1.2.1. Нормативные ссылки</span><span class="sxs-lookup"><span data-stu-id="a573a-196">1.2.1 Normative References</span></span>

<span data-ttu-id="a573a-197">\[IEEE754 \] институт инженеров по стандартизации и электронике, "Standard для Floating-Point арифметических операций", IEEE 754-1985, 1985 октября, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="a573a-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="a573a-198">\[MS-DCOM \] корпорации Майкрософт, «распределенные протоколы модели объектов Distributed Component», 2006 июня.</span><span class="sxs-lookup"><span data-stu-id="a573a-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="a573a-199">\[MS-GPSI \] Microsoft Corporation, "Групповая политика установки программное расширение", июнь 2006 г.</span><span class="sxs-lookup"><span data-stu-id="a573a-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="a573a-200">\[MS-SMB \] Корпорация Майкрософт, Microsoft (протокол SMB) и расширения, май 2006.</span><span class="sxs-lookup"><span data-stu-id="a573a-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="a573a-201">\[MS-SYS Корпорация \] Майкрософт, "системный обзор v4", июль 2006.</span><span class="sxs-lookup"><span data-stu-id="a573a-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="a573a-202">\[САЛТОН \] Салтон, G., "Автоматическая обработка текста: анализ преобразования и извлечение информации по компьютерам", 1988, ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="a573a-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="a573a-203">\[Unicode \] Consortium (Unicode Standard, версия 2,0, 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="a573a-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="a573a-204">1.2.2. Справочные ссылки</span><span class="sxs-lookup"><span data-stu-id="a573a-204">1.2.2 Informative References</span></span>

<span data-ttu-id="a573a-205">\[MSDN-OLEDB \] корпорации Майкрософт, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="a573a-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="a573a-206">\[MSDN — КУЕРЕРР \] корпорации Майкрософт, Query-Execution значения https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="a573a-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="a573a-207">Общие сведения о протоколе 1,3 (краткий обзор)</span><span class="sxs-lookup"><span data-stu-id="a573a-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="a573a-208">**Служба индексирования** содержимого помогает эффективно организовывать извлеченные функции коллекции документов.</span><span class="sxs-lookup"><span data-stu-id="a573a-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="a573a-209">Протокол службы индексирования содержимого (CISP) позволяет клиенту взаимодействовать с сервером, на котором размещена служба индексирования, выдавать запросы и предоставлять администратору возможность управлять сервером индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="a573a-210">При обработке файлов служба индексирования анализирует набор документов и реорганизует их содержимое таким образом, что **Свойства** этих документов могут быть эффективно возвращены в ответ на запросы.</span><span class="sxs-lookup"><span data-stu-id="a573a-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="a573a-211">Коллекция документов, которые можно запросить, состоит из **каталога** .</span><span class="sxs-lookup"><span data-stu-id="a573a-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="a573a-212">Каталог может содержать **индекс** (для быстрого получения ссылки на текст) и **кэш свойств** (для быстрого извлечения значений свойств).</span><span class="sxs-lookup"><span data-stu-id="a573a-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="a573a-213">По сути, каталог состоит из логической "таблицы" свойств с текстом или значением и соответствующим языковым стандартом, хранящимся в **столбцах** таблицы.</span><span class="sxs-lookup"><span data-stu-id="a573a-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="a573a-214">Каждая строка таблицы соответствует отдельному документу в области каталога, а каждый столбец таблицы соответствует свойству.</span><span class="sxs-lookup"><span data-stu-id="a573a-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="a573a-215">Конкретные задачи, выполняемые CISP, группируются в две функциональные области:</span><span class="sxs-lookup"><span data-stu-id="a573a-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="a573a-216">Удаленное администрирование каталогов служб индексирования,</span><span class="sxs-lookup"><span data-stu-id="a573a-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="a573a-217">Удаленное выполнение запросов к каталогам службы индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="a573a-218">Задачи удаленного администрирования 1.3.1</span><span class="sxs-lookup"><span data-stu-id="a573a-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="a573a-219">CISP включает следующие задачи управления каталогом служб индексирования из клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="a573a-220">Запрашивает текущее состояние каталога служб индексирования на сервере.</span><span class="sxs-lookup"><span data-stu-id="a573a-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="a573a-221">Обновление состояния каталога служб индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="a573a-222">Запуск процесса индексирования для определенного набора файлов.</span><span class="sxs-lookup"><span data-stu-id="a573a-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="a573a-223">Инициация оптимизации индекса для повышения производительности запросов.</span><span class="sxs-lookup"><span data-stu-id="a573a-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="a573a-224">Все задачи удаленного администрирования следуют простой модели "запрос-ответ".</span><span class="sxs-lookup"><span data-stu-id="a573a-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="a573a-225">На клиенте не ведется никаких состояний для вызова администрирования, и административные вызовы могут выполняться в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="a573a-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="a573a-226">1.3.2 удаленный запрос</span><span class="sxs-lookup"><span data-stu-id="a573a-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="a573a-227">CISP позволяет клиентам выполнять поисковые запросы к удаленному серверу, на котором размещена служба индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="a573a-228">Отправка поискового запроса — это многоэтапный процесс, инициированный клиентом.</span><span class="sxs-lookup"><span data-stu-id="a573a-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="a573a-229">Для этого необходимо выполнить следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="a573a-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="a573a-230">Клиент запрашивает соединение с сервером, на котором размещена служба индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="a573a-231">Клиент отправляет параметры поискового запроса, в том числе следующие:</span><span class="sxs-lookup"><span data-stu-id="a573a-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="a573a-232">**Ограничения** , указывающие, какие документы должны включаться и (или) исключены из результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="a573a-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="a573a-233">Порядок, в котором должны возвращаться результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="a573a-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="a573a-234">Столбцы, возвращаемые в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="a573a-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="a573a-235">Максимальное число **строк** , которое должно быть возвращено для запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="a573a-236">Максимальное время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="a573a-237">После того как сервер подтвердил запрос клиента на инициацию запроса, клиент может запросить сведения о состоянии запроса, но это не обязательное действие.</span><span class="sxs-lookup"><span data-stu-id="a573a-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="a573a-238">Затем клиент указывает, какие свойства сервер должен включать в результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="a573a-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="a573a-239">Клиент запрашивает результирующий набор от сервера, а сервер отвечает, отправляя клиенту значения свойств для файлов, включенных в результаты поискового запроса клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="a573a-240">Если значение свойства слишком велико для одного буфера ответа, сервер не будет передавать свойство, а вместо этого установит для свойства значение отложено.</span><span class="sxs-lookup"><span data-stu-id="a573a-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="a573a-241">Затем клиент запрашивает значение свойства отдельно, используя последовательность запросов для последовательных блоков значения, а затем возобновляет запрос других значений.</span><span class="sxs-lookup"><span data-stu-id="a573a-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="a573a-242">Когда клиент завершает работу с поисковым запросом и больше не требует дополнительных результатов, клиент обращается к серверу для освобождения запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="a573a-243">После того, как сервер выпустил запрос, клиент может отправить запрос на отключение от сервера.</span><span class="sxs-lookup"><span data-stu-id="a573a-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="a573a-244">После этого соединение закрывается.</span><span class="sxs-lookup"><span data-stu-id="a573a-244">The connection is then closed.</span></span> <span data-ttu-id="a573a-245">Кроме того, клиент может отправить еще один запрос и повторить последовательность из шага 2.</span><span class="sxs-lookup"><span data-stu-id="a573a-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="a573a-246">Поведение Windows. Этот Протокол реализован в Windows 2000, Windows XP, Windows Server 2003 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a573a-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="a573a-247">1.4. Связь с другими протоколами</span><span class="sxs-lookup"><span data-stu-id="a573a-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="a573a-248">CISP использует \[ протокол SMB MS-SMB \] для передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="a573a-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="a573a-249">Никакой другой протокол не зависит непосредственно от протокола службы индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="a573a-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="a573a-250">*Поведение Windows. Обычно приложения взаимодействуют с оболочкой интерфейса OLE DB \[ MSDN-OLEDB \] (например, клиент протокола), а не напрямую с протоколом.*</span><span class="sxs-lookup"><span data-stu-id="a573a-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="a573a-251">1,5. Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="a573a-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="a573a-252">Предполагается, что клиент получил имя сервера и имя каталога перед вызовом этого протокола.</span><span class="sxs-lookup"><span data-stu-id="a573a-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="a573a-253">То, как клиент делает это, лежит вне области данной спецификации.</span><span class="sxs-lookup"><span data-stu-id="a573a-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="a573a-254">Также предполагается, что клиент и сервер имеют сопоставление безопасности, которое можно использовать с именованными каналами \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="a573a-255">1.6. Постановление о пределах применения</span><span class="sxs-lookup"><span data-stu-id="a573a-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="a573a-256">CISP предназначен для запросов и управления каталогами на удаленном сервере от клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="a573a-257">CISP является устаревшим в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a573a-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="a573a-258">1.7. Управление версиями и согласованность функций</span><span class="sxs-lookup"><span data-stu-id="a573a-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="a573a-259">Этот протокол не имеет механизмов управления версиями или согласования возможностей.</span><span class="sxs-lookup"><span data-stu-id="a573a-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="a573a-260">1.8. Расширяемые поля поставщика</span><span class="sxs-lookup"><span data-stu-id="a573a-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="a573a-261">Этот протокол использует значения HRESULT, которые являются расширяемыми поставщиками.</span><span class="sxs-lookup"><span data-stu-id="a573a-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="a573a-262">Поставщики могут выбирать собственные значения для этого поля, если бит C (0x20000000) задан в соответствии с разделом 4.1.1 в MS-SYS, что означает, что это \[ \] код клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="a573a-263">Этот протокол также использует значения NTSTATUS, взятые из числового пространства NTSTATUS, определенного в \[ MS-sys \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="a573a-264">Поставщики должны повторно использовать эти значения с указанным значением.</span><span class="sxs-lookup"><span data-stu-id="a573a-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="a573a-265">Выбор любого другого значения вызывает риск конфликта в будущем.</span><span class="sxs-lookup"><span data-stu-id="a573a-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="a573a-266">*Поведение Windows. в Windows используются только значения, указанные в разделе 4.1.3 из \[ MS-sys \] .*</span><span class="sxs-lookup"><span data-stu-id="a573a-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="a573a-267">Идентификаторы свойств 1.8.1</span><span class="sxs-lookup"><span data-stu-id="a573a-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="a573a-268">Свойства представлены идентификаторами, известными как идентификаторы свойств.</span><span class="sxs-lookup"><span data-stu-id="a573a-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="a573a-269">Каждое свойство должно иметь глобальный уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="a573a-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="a573a-270">Этот идентификатор состоит из **идентификатора GUID** , представляющего коллекцию свойств, которые называются набором свойств, а также строки или 32-разрядного целого числа для идентификации свойства в наборе.</span><span class="sxs-lookup"><span data-stu-id="a573a-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="a573a-271">Если используется целочисленная форма идентификатора, значения 0x00000000, 0xFFFFFFFF и 0xFFFFFFFE считаются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="a573a-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="a573a-272">Поставщики могут гарантировать, что их свойства определяются уникальным образом, помещая их в набор свойств, определенный их собственным идентификатором GUID.</span><span class="sxs-lookup"><span data-stu-id="a573a-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="a573a-273">1.9. Назначения стандартов</span><span class="sxs-lookup"><span data-stu-id="a573a-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="a573a-274">Этот протокол не имеет стандартных назначений, а только частные назначения, выполняемые корпорацией Майкрософт с использованием процедур распределения, заданных в других протоколах.</span><span class="sxs-lookup"><span data-stu-id="a573a-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="a573a-275">Корпорация Майкрософт выделила этот протокол именованным каналом, как указано в \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="a573a-276">Назначение:</span><span class="sxs-lookup"><span data-stu-id="a573a-276">The assignment is:</span></span>



| <span data-ttu-id="a573a-277">Параметр</span><span class="sxs-lookup"><span data-stu-id="a573a-277">Parameter</span></span> | <span data-ttu-id="a573a-278">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-278">Value</span></span>             | <span data-ttu-id="a573a-279">Справочник</span><span class="sxs-lookup"><span data-stu-id="a573a-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="a573a-280">Имя канала</span><span class="sxs-lookup"><span data-stu-id="a573a-280">Pipe name</span></span> | <span data-ttu-id="a573a-281">\\\\скадс элемента конфигурации канала \_</span><span class="sxs-lookup"><span data-stu-id="a573a-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="a573a-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="a573a-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="a573a-283">2. Сообщения</span><span class="sxs-lookup"><span data-stu-id="a573a-283">2 Messages</span></span>

-   [<span data-ttu-id="a573a-284">2.1. Транспортировка</span><span class="sxs-lookup"><span data-stu-id="a573a-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="a573a-285">2.2. Синтаксис сообщений</span><span class="sxs-lookup"><span data-stu-id="a573a-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="a573a-286">2.1. Транспортировка</span><span class="sxs-lookup"><span data-stu-id="a573a-286">2.1 Transport</span></span>

<span data-ttu-id="a573a-287">Все сообщения должны быть перенесены с помощью именованного канала, как указано в \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="a573a-288">Используется следующее имя канала:</span><span class="sxs-lookup"><span data-stu-id="a573a-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="a573a-289">\\\\скадс элемента конфигурации канала \_</span><span class="sxs-lookup"><span data-stu-id="a573a-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="a573a-290">Этот протокол использует базовый протокол именованных каналов SMB для получения удостоверения вызывающей стороны, который установил подключение, как указано в разделе 2.2.8 \[ MS-SMB \] ; клиент должен задать идентификатор безопасности в \_ качестве имперсонатионлевел в запросе, чтобы открыть именованный канал.</span><span class="sxs-lookup"><span data-stu-id="a573a-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="a573a-291">2.2. Синтаксис сообщений</span><span class="sxs-lookup"><span data-stu-id="a573a-291">2.2 Message Syntax</span></span>

<span data-ttu-id="a573a-292">Несколько структур и сообщений в следующих разделах относятся к маркерам глав или закладок.</span><span class="sxs-lookup"><span data-stu-id="a573a-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="a573a-293">Маркер представляет собой 32-разрядную непрозрачную структуру, которая однозначно определяет главу или закладку.</span><span class="sxs-lookup"><span data-stu-id="a573a-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="a573a-294">Как правило, клиентские приложения получают значения обработчиков через вызовы методов; Однако существует несколько хорошо известных значений, которые не нужно получать с сервера, значение которого указано в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="a573a-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="a573a-295">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-295">Value</span></span>                         | <span data-ttu-id="a573a-296">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-297">База данных \_ null \_ параметру hChapter 0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="a573a-298">Маркер главы для набора строк с неразбитым набором, содержащий все результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="a573a-299">ДББМК, \_ первый 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="a573a-300">Маркер закладки, указывающий первую строку в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="a573a-301">ДББМК \_ последний 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="a573a-302">Маркер закладки для закладки, определяющей последнюю строку в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="a573a-303">2.2.1 структуры</span><span class="sxs-lookup"><span data-stu-id="a573a-303">2.2.1 Structures</span></span>

<span data-ttu-id="a573a-304">В этом разделе описываются структуры данных, которые определяются и используются CISP.</span><span class="sxs-lookup"><span data-stu-id="a573a-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="a573a-305">Все 2-, 4-и 8-байтовые целые числа со знаком и без знака в следующих структурах должны передаваться с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="a573a-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="a573a-306">В следующей таблице перечислены структуры данных, определенные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="a573a-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="a573a-307">Структура</span><span class="sxs-lookup"><span data-stu-id="a573a-307">Structure</span></span>                    | <span data-ttu-id="a573a-308">Описание</span><span class="sxs-lookup"><span data-stu-id="a573a-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-309">кбасесторажевариант</span><span class="sxs-lookup"><span data-stu-id="a573a-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="a573a-310">Содержит значение, по которому выполняется операция сопоставления для свойства, указанного в структуре Кпропертирестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="a573a-311">SAFEARRAY, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="a573a-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="a573a-312">Содержит многомерный массив.</span><span class="sxs-lookup"><span data-stu-id="a573a-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="a573a-313">сафеаррайбаунд</span><span class="sxs-lookup"><span data-stu-id="a573a-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="a573a-314">Представляет границы для измерения массива, указанного в структуре SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="a573a-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="a573a-315">кфуллпропспек</span><span class="sxs-lookup"><span data-stu-id="a573a-315">CFullPropSpec</span></span>                | <span data-ttu-id="a573a-316">Содержит спецификацию свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="a573a-317">кконтентрестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-317">CContentRestriction</span></span>          | <span data-ttu-id="a573a-318">Содержит строку, соответствующую значению свойства в кэше свойств.</span><span class="sxs-lookup"><span data-stu-id="a573a-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="a573a-319">ккэй</span><span class="sxs-lookup"><span data-stu-id="a573a-319">CKey</span></span>                         | <span data-ttu-id="a573a-320">Содержит значение свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="a573a-321">Цинтерналпропертирестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="a573a-322">Содержит значение свойства для сопоставления с операцией.</span><span class="sxs-lookup"><span data-stu-id="a573a-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="a573a-323">кнатлангуажерестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="a573a-324">Содержит запрос на естественном языке для свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="a573a-325">кнодерестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-325">CNodeRestriction</span></span>             | <span data-ttu-id="a573a-326">Содержит массив узлов дерева команд, задающий ограничения для запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="a573a-327">коккрестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-327">COccRestriction</span></span>              | <span data-ttu-id="a573a-328">Содержит расположение слова в фразе.</span><span class="sxs-lookup"><span data-stu-id="a573a-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="a573a-329">кпропертирестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-329">CPropertyRestriction</span></span>         | <span data-ttu-id="a573a-330">Содержит значение свойства для сопоставления с операцией.</span><span class="sxs-lookup"><span data-stu-id="a573a-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="a573a-331">кранжерестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-331">CRangeRestriction</span></span>            | <span data-ttu-id="a573a-332">Содержит ограничение на диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="a573a-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="a573a-333">кскоперестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-333">CScopeRestriction</span></span>            | <span data-ttu-id="a573a-334">Содержит ограничение на файлы для поиска.</span><span class="sxs-lookup"><span data-stu-id="a573a-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="a573a-335">ксорт</span><span class="sxs-lookup"><span data-stu-id="a573a-335">CSort</span></span>                        | <span data-ttu-id="a573a-336">Определяет столбец для сортировки.</span><span class="sxs-lookup"><span data-stu-id="a573a-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="a573a-337">ксинрестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-337">CSynRestriction</span></span>              | <span data-ttu-id="a573a-338">Содержит слово или его синонимы для фразы запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="a573a-339">квекторрестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-339">CVectorRestriction</span></span>           | <span data-ttu-id="a573a-340">Содержит взвешенное значение или операцию для узла дерева команд.</span><span class="sxs-lookup"><span data-stu-id="a573a-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="a573a-341">квордрестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-341">CWordRestriction</span></span>             | <span data-ttu-id="a573a-342">Содержит слово для фразы запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="a573a-343">крестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-343">CRestriction</span></span>                 | <span data-ttu-id="a573a-344">Содержит узел дерева команд запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="a573a-345">кколумнсет</span><span class="sxs-lookup"><span data-stu-id="a573a-345">CColumnSet</span></span>                   | <span data-ttu-id="a573a-346">Указывает число возвращаемых столбцов.</span><span class="sxs-lookup"><span data-stu-id="a573a-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="a573a-347">ккатегоризатионсет</span><span class="sxs-lookup"><span data-stu-id="a573a-347">CCategorizationSet</span></span>           | <span data-ttu-id="a573a-348">Содержит сведения о группировании набора результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="a573a-349">ккатегоризатионспек</span><span class="sxs-lookup"><span data-stu-id="a573a-349">CCategorizationSpec</span></span>          | <span data-ttu-id="a573a-350">Содержит определение категорий, в которых будут классифицироваться результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="a573a-351">кдбколид</span><span class="sxs-lookup"><span data-stu-id="a573a-351">CDbColId</span></span>                     | <span data-ttu-id="a573a-352">Содержит столбец.</span><span class="sxs-lookup"><span data-stu-id="a573a-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="a573a-353">кдбпроп</span><span class="sxs-lookup"><span data-stu-id="a573a-353">CDbProp</span></span>                      | <span data-ttu-id="a573a-354">Содержит свойство.</span><span class="sxs-lookup"><span data-stu-id="a573a-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="a573a-355">кдбпропсет</span><span class="sxs-lookup"><span data-stu-id="a573a-355">CDbPropSet</span></span>                   | <span data-ttu-id="a573a-356">Содержит набор свойств.</span><span class="sxs-lookup"><span data-stu-id="a573a-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="a573a-357">кпидмаппер</span><span class="sxs-lookup"><span data-stu-id="a573a-357">CPidMapper</span></span>                   | <span data-ttu-id="a573a-358">Содержит массив идентификаторов свойств, указывающих свойства, возвращаемые в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="a573a-359">кровсикат</span><span class="sxs-lookup"><span data-stu-id="a573a-359">CRowSeekAt</span></span>                   | <span data-ttu-id="a573a-360">Содержит смещение для получения строк в сообщении Кпмжетровсин</span><span class="sxs-lookup"><span data-stu-id="a573a-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="a573a-361">кровсикатратио</span><span class="sxs-lookup"><span data-stu-id="a573a-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="a573a-362">Определяет точку, с которой начинается извлечение сообщения Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="a573a-363">кровсикбибукмарк</span><span class="sxs-lookup"><span data-stu-id="a573a-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="a573a-364">Определяет закладки, из которых извлекаются строки для сообщения Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="a573a-365">кровсикнекст</span><span class="sxs-lookup"><span data-stu-id="a573a-365">CRowSeekNext</span></span>                 | <span data-ttu-id="a573a-366">Содержит число строк, которые необходимо пропустить в сообщении Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="a573a-367">кровсетпропертиес</span><span class="sxs-lookup"><span data-stu-id="a573a-367">CRowsetProperties</span></span>            | <span data-ttu-id="a573a-368">Содержит сведения о конфигурации для запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="a573a-369">ксортсет</span><span class="sxs-lookup"><span data-stu-id="a573a-369">CSortSet</span></span>                     | <span data-ttu-id="a573a-370">Содержит порядок сортировки для запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="a573a-371">ктаблеколумн</span><span class="sxs-lookup"><span data-stu-id="a573a-371">CTableColumn</span></span>                 | <span data-ttu-id="a573a-372">Содержит столбец для сообщения Кпмсетбиндингс.</span><span class="sxs-lookup"><span data-stu-id="a573a-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="a573a-373">сериализедпропертивалуе</span><span class="sxs-lookup"><span data-stu-id="a573a-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="a573a-374">Содержит сериализованное значение.</span><span class="sxs-lookup"><span data-stu-id="a573a-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="a573a-375">2.2.1.1 Кбасесторажевариант</span><span class="sxs-lookup"><span data-stu-id="a573a-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="a573a-376">Структура Кбасесторажевариант содержит значение, по которому выполняется операция сопоставления для свойства, указанного в структуре Кпропертирестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="a573a-377">0</span><span class="sxs-lookup"><span data-stu-id="a573a-377">0</span></span>

<span data-ttu-id="a573a-378">1</span><span class="sxs-lookup"><span data-stu-id="a573a-378">1</span></span>

<span data-ttu-id="a573a-379">2</span><span class="sxs-lookup"><span data-stu-id="a573a-379">2</span></span>

<span data-ttu-id="a573a-380">3</span><span class="sxs-lookup"><span data-stu-id="a573a-380">3</span></span>

<span data-ttu-id="a573a-381">4</span><span class="sxs-lookup"><span data-stu-id="a573a-381">4</span></span>

<span data-ttu-id="a573a-382">5</span><span class="sxs-lookup"><span data-stu-id="a573a-382">5</span></span>

<span data-ttu-id="a573a-383">6</span><span class="sxs-lookup"><span data-stu-id="a573a-383">6</span></span>

<span data-ttu-id="a573a-384">7</span><span class="sxs-lookup"><span data-stu-id="a573a-384">7</span></span>

<span data-ttu-id="a573a-385">8</span><span class="sxs-lookup"><span data-stu-id="a573a-385">8</span></span>

<span data-ttu-id="a573a-386">9</span><span class="sxs-lookup"><span data-stu-id="a573a-386">9</span></span>

<span data-ttu-id="a573a-387">1</span><span class="sxs-lookup"><span data-stu-id="a573a-387">1</span></span><br/> <span data-ttu-id="a573a-388">0</span><span class="sxs-lookup"><span data-stu-id="a573a-388">0</span></span><br/>

<span data-ttu-id="a573a-389">1</span><span class="sxs-lookup"><span data-stu-id="a573a-389">1</span></span>

<span data-ttu-id="a573a-390">2</span><span class="sxs-lookup"><span data-stu-id="a573a-390">2</span></span>

<span data-ttu-id="a573a-391">3</span><span class="sxs-lookup"><span data-stu-id="a573a-391">3</span></span>

<span data-ttu-id="a573a-392">4</span><span class="sxs-lookup"><span data-stu-id="a573a-392">4</span></span>

<span data-ttu-id="a573a-393">5</span><span class="sxs-lookup"><span data-stu-id="a573a-393">5</span></span>

<span data-ttu-id="a573a-394">6</span><span class="sxs-lookup"><span data-stu-id="a573a-394">6</span></span>

<span data-ttu-id="a573a-395">7</span><span class="sxs-lookup"><span data-stu-id="a573a-395">7</span></span>

<span data-ttu-id="a573a-396">8</span><span class="sxs-lookup"><span data-stu-id="a573a-396">8</span></span>

<span data-ttu-id="a573a-397">9</span><span class="sxs-lookup"><span data-stu-id="a573a-397">9</span></span>

<span data-ttu-id="a573a-398">2</span><span class="sxs-lookup"><span data-stu-id="a573a-398">2</span></span><br/> <span data-ttu-id="a573a-399">0</span><span class="sxs-lookup"><span data-stu-id="a573a-399">0</span></span><br/>

<span data-ttu-id="a573a-400">1</span><span class="sxs-lookup"><span data-stu-id="a573a-400">1</span></span>

<span data-ttu-id="a573a-401">2</span><span class="sxs-lookup"><span data-stu-id="a573a-401">2</span></span>

<span data-ttu-id="a573a-402">3</span><span class="sxs-lookup"><span data-stu-id="a573a-402">3</span></span>

<span data-ttu-id="a573a-403">4</span><span class="sxs-lookup"><span data-stu-id="a573a-403">4</span></span>

<span data-ttu-id="a573a-404">5</span><span class="sxs-lookup"><span data-stu-id="a573a-404">5</span></span>

<span data-ttu-id="a573a-405">6</span><span class="sxs-lookup"><span data-stu-id="a573a-405">6</span></span>

<span data-ttu-id="a573a-406">7</span><span class="sxs-lookup"><span data-stu-id="a573a-406">7</span></span>

<span data-ttu-id="a573a-407">8</span><span class="sxs-lookup"><span data-stu-id="a573a-407">8</span></span>

<span data-ttu-id="a573a-408">9</span><span class="sxs-lookup"><span data-stu-id="a573a-408">9</span></span>

<span data-ttu-id="a573a-409">3</span><span class="sxs-lookup"><span data-stu-id="a573a-409">3</span></span><br/> <span data-ttu-id="a573a-410">0</span><span class="sxs-lookup"><span data-stu-id="a573a-410">0</span></span><br/>

<span data-ttu-id="a573a-411">1</span><span class="sxs-lookup"><span data-stu-id="a573a-411">1</span></span>

<span data-ttu-id="a573a-412">втипе</span><span class="sxs-lookup"><span data-stu-id="a573a-412">vType</span></span>

<span data-ttu-id="a573a-413">vData1</span><span class="sxs-lookup"><span data-stu-id="a573a-413">vData1</span></span>

<span data-ttu-id="a573a-414">vData2</span><span class="sxs-lookup"><span data-stu-id="a573a-414">vData2</span></span>

<span data-ttu-id="a573a-415">Управляемое vValue (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-415">vValue (variable)</span></span>



 

<span data-ttu-id="a573a-416">**втипе**: признак типа, указывающий тип управляемое vValue.</span><span class="sxs-lookup"><span data-stu-id="a573a-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="a573a-417">Это должно быть одно из значений VARENUM, указанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a573a-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="a573a-418">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-418">Value</span></span>                 | <span data-ttu-id="a573a-419">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-420">VT \_ Empty (символ 0x0000)</span><span class="sxs-lookup"><span data-stu-id="a573a-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="a573a-421">Управляемое vValue отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a573a-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="a573a-422">VT \_ null (0x0001)</span><span class="sxs-lookup"><span data-stu-id="a573a-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="a573a-423">Управляемое vValue отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a573a-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="a573a-424">VT \_ I1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="a573a-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="a573a-425">1-байтовое целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="a573a-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="a573a-426">VT \_ UI1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="a573a-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="a573a-427">1-байтовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="a573a-428">VT \_ I2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="a573a-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="a573a-429">2-байтовое целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="a573a-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="a573a-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="a573a-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="a573a-431">2-байтовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="a573a-432">Логическое значение VT \_ (0x000B)</span><span class="sxs-lookup"><span data-stu-id="a573a-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="a573a-433">Логическое значение; 2-байтовое целое число, содержащее символ 0x0000 (FALSE) или 0xFFFF (TRUE).</span><span class="sxs-lookup"><span data-stu-id="a573a-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="a573a-434">VT \_ I4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="a573a-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="a573a-435">4-байтовое целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="a573a-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="a573a-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="a573a-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="a573a-437">4-байтовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="a573a-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="a573a-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="a573a-439">32-разрядное число с плавающей запятой, определенное в \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="a573a-440">VT \_ int (0x0016)</span><span class="sxs-lookup"><span data-stu-id="a573a-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="a573a-441">4-байтовое целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="a573a-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="a573a-442">VT \_ uint (0x0017)</span><span class="sxs-lookup"><span data-stu-id="a573a-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="a573a-443">4-байтовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="a573a-444">\_Ошибка VT (0x000A)</span><span class="sxs-lookup"><span data-stu-id="a573a-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="a573a-445">4-байтовое целое число без знака, содержащее значение HRESULT, как указано в \[ MS-sys \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="a573a-446">VT \_ I8 (0x0014)</span><span class="sxs-lookup"><span data-stu-id="a573a-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="a573a-447">8 байт целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="a573a-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="a573a-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="a573a-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="a573a-449">8-байтовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="a573a-450">VT \_ R8 (0x0005)</span><span class="sxs-lookup"><span data-stu-id="a573a-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="a573a-451">64-разрядное число с плавающей запятой, определенное в \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="a573a-452">VT \_ CY (0x0006)</span><span class="sxs-lookup"><span data-stu-id="a573a-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="a573a-453">8-байтное дополнение к целому числу (с масштабированием на 10 000).</span><span class="sxs-lookup"><span data-stu-id="a573a-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="a573a-454">\_Дата VT (0x0007)</span><span class="sxs-lookup"><span data-stu-id="a573a-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="a573a-455">64-разрядное число с плавающей запятой, представляющее количество дней с момента 00:00:00 31 декабря 1899 (координированное время в формате UTC).</span><span class="sxs-lookup"><span data-stu-id="a573a-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="a573a-456">VT \_ fileTime (0x0040)</span><span class="sxs-lookup"><span data-stu-id="a573a-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="a573a-457">64-разрядное целое число, представляющее число интервалов 100-наносекундных с 00:00:00 по 1 января 1601 г. (координированное время в формате UTC).</span><span class="sxs-lookup"><span data-stu-id="a573a-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="a573a-458">VT \_ Decimal (0x000E)</span><span class="sxs-lookup"><span data-stu-id="a573a-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="a573a-459">ДЕСЯТИЧная структура, как указано в разделе 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="a573a-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="a573a-460">VT \_ CLSID (0x0048)</span><span class="sxs-lookup"><span data-stu-id="a573a-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="a573a-461">16-байтовое двоичное значение, содержащее идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="a573a-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="a573a-462">\_Большой двоичный объект VT (0x0041)</span><span class="sxs-lookup"><span data-stu-id="a573a-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="a573a-463">Целое число без знака размером 4 байта в большом двоичном объекте, за которым следует множество байтов данных.</span><span class="sxs-lookup"><span data-stu-id="a573a-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="a573a-464">VT \_ BSTR (0x0008)</span><span class="sxs-lookup"><span data-stu-id="a573a-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="a573a-465">Целое число без знака длиной 4 байта в строке, за которым следует строка, как указано ниже в разделе управляемое vValue.</span><span class="sxs-lookup"><span data-stu-id="a573a-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="a573a-466">VT \_ LPSTR (0x001E)</span><span class="sxs-lookup"><span data-stu-id="a573a-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="a573a-467">Строка ANSI, заканчивающаяся нулем.</span><span class="sxs-lookup"><span data-stu-id="a573a-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="a573a-468">VT \_ LPWSTR (0x001F)</span><span class="sxs-lookup"><span data-stu-id="a573a-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="a573a-469">Строка Юникода в Юникоде, заканчивающаяся нулем \[ \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="a573a-470">\_Вариант VT (0x000C)</span><span class="sxs-lookup"><span data-stu-id="a573a-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="a573a-471">Кбасесторажевариант.</span><span class="sxs-lookup"><span data-stu-id="a573a-471">CBaseStorageVariant.</span></span> <span data-ttu-id="a573a-472">НЕОБХОДИМО сочетать с модификатором типа в \_ массиве VT или в \_ векторе VT.</span><span class="sxs-lookup"><span data-stu-id="a573a-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="a573a-473">В следующей таблице указаны модификаторы типа для Втипе.</span><span class="sxs-lookup"><span data-stu-id="a573a-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="a573a-474">Модификаторы типа могут быть двоичными ORed с Втипе, чтобы изменить значение управляемое vValue, чтобы указать, что это один из двух возможных типов массивов.</span><span class="sxs-lookup"><span data-stu-id="a573a-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="a573a-475">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-475">Value</span></span>               | <span data-ttu-id="a573a-476">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-477">\_Вектор VT (0x1000)</span><span class="sxs-lookup"><span data-stu-id="a573a-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="a573a-478">Если индикатор типа сочетается с \_ вектором VT с помощью оператора OR, управляемое vValue является подсчитанным массивом значений указанного типа.</span><span class="sxs-lookup"><span data-stu-id="a573a-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="a573a-479">Дополнительные сведения см. в разделе 2.2.1.1.1.2.</span><span class="sxs-lookup"><span data-stu-id="a573a-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="a573a-480">Этот модификатор типа не должен сочетаться со следующими типами: VT \_ int, VT \_ uint, Decimal, VT \_ , BLOB- \_ \_ объект VT \_ .</span><span class="sxs-lookup"><span data-stu-id="a573a-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="a573a-481">\_Массив VT (0x2000)</span><span class="sxs-lookup"><span data-stu-id="a573a-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="a573a-482">Если индикатор типа сочетается с \_ массивом VT с помощью оператора OR, это значение является массивом SAFEARRAY (как указано в разделе 2.2.1.1.1.3), содержащим значения указанного типа.</span><span class="sxs-lookup"><span data-stu-id="a573a-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="a573a-483">Этот модификатор типа не должен сочетаться со следующими типами: VT \_ i8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, \_ BLOB VT, \_ \_ объект объекта VT, VT \_ LPSTR, VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="a573a-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="a573a-484">**vData1**: Если втипе имеет тип VT \_ Decimal, значение этого поля указывается в качестве поля масштабирования в разделе 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="a573a-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="a573a-485">Для всех остальных Втипес значение должно быть равно 0x00.</span><span class="sxs-lookup"><span data-stu-id="a573a-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="a573a-486">**vData2**: Если втипе имеет тип VT \_ Decimal, значение этого поля указывается как поле подписи в разделе 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="a573a-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="a573a-487">Для всех остальных Втипес значение должно быть равно 0x00.</span><span class="sxs-lookup"><span data-stu-id="a573a-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="a573a-488">**управляемое vValue**: значение для операции сопоставления.</span><span class="sxs-lookup"><span data-stu-id="a573a-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="a573a-489">Синтаксис должен быть указан в поле Втипе.</span><span class="sxs-lookup"><span data-stu-id="a573a-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="a573a-490">В следующей таблице приведены размеры для поля управляемое vValue, зависящие от поля Втипе для типов данных фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="a573a-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="a573a-491">Размер указан в байтах.</span><span class="sxs-lookup"><span data-stu-id="a573a-491">The size is in bytes.</span></span>



| <span data-ttu-id="a573a-492">втипе</span><span class="sxs-lookup"><span data-stu-id="a573a-492">vType</span></span>                                                   | <span data-ttu-id="a573a-493">Размер</span><span class="sxs-lookup"><span data-stu-id="a573a-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="a573a-494">VT \_ I1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="a573a-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="a573a-495">1</span><span class="sxs-lookup"><span data-stu-id="a573a-495">1</span></span>    |
| <span data-ttu-id="a573a-496">VT \_ I2, VT \_ UI2, логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="a573a-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="a573a-497">2</span><span class="sxs-lookup"><span data-stu-id="a573a-497">2</span></span>    |
| <span data-ttu-id="a573a-498">VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ int, VT \_ uint, \_ Ошибка VT</span><span class="sxs-lookup"><span data-stu-id="a573a-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="a573a-499">4</span><span class="sxs-lookup"><span data-stu-id="a573a-499">4</span></span>    |
| <span data-ttu-id="a573a-500">VT \_ i8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ , VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="a573a-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="a573a-501">8</span><span class="sxs-lookup"><span data-stu-id="a573a-501">8</span></span>    |
| <span data-ttu-id="a573a-502">VT \_ Decimal, VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="a573a-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="a573a-503">16</span><span class="sxs-lookup"><span data-stu-id="a573a-503">16</span></span>   |



 

<span data-ttu-id="a573a-504">Если для Втипе задано значение VT \_ BLOB, VT \_ BSTR или VT LPSTR, то \_ Структура управляемое vValue указана на следующей схеме:</span><span class="sxs-lookup"><span data-stu-id="a573a-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="a573a-505">0</span><span class="sxs-lookup"><span data-stu-id="a573a-505">0</span></span>

<span data-ttu-id="a573a-506">1</span><span class="sxs-lookup"><span data-stu-id="a573a-506">1</span></span>

<span data-ttu-id="a573a-507">2</span><span class="sxs-lookup"><span data-stu-id="a573a-507">2</span></span>

<span data-ttu-id="a573a-508">3</span><span class="sxs-lookup"><span data-stu-id="a573a-508">3</span></span>

<span data-ttu-id="a573a-509">4</span><span class="sxs-lookup"><span data-stu-id="a573a-509">4</span></span>

<span data-ttu-id="a573a-510">5</span><span class="sxs-lookup"><span data-stu-id="a573a-510">5</span></span>

<span data-ttu-id="a573a-511">6</span><span class="sxs-lookup"><span data-stu-id="a573a-511">6</span></span>

<span data-ttu-id="a573a-512">7</span><span class="sxs-lookup"><span data-stu-id="a573a-512">7</span></span>

<span data-ttu-id="a573a-513">8</span><span class="sxs-lookup"><span data-stu-id="a573a-513">8</span></span>

<span data-ttu-id="a573a-514">9</span><span class="sxs-lookup"><span data-stu-id="a573a-514">9</span></span>

<span data-ttu-id="a573a-515">1</span><span class="sxs-lookup"><span data-stu-id="a573a-515">1</span></span><br/> <span data-ttu-id="a573a-516">0</span><span class="sxs-lookup"><span data-stu-id="a573a-516">0</span></span><br/>

<span data-ttu-id="a573a-517">1</span><span class="sxs-lookup"><span data-stu-id="a573a-517">1</span></span>

<span data-ttu-id="a573a-518">2</span><span class="sxs-lookup"><span data-stu-id="a573a-518">2</span></span>

<span data-ttu-id="a573a-519">3</span><span class="sxs-lookup"><span data-stu-id="a573a-519">3</span></span>

<span data-ttu-id="a573a-520">4</span><span class="sxs-lookup"><span data-stu-id="a573a-520">4</span></span>

<span data-ttu-id="a573a-521">5</span><span class="sxs-lookup"><span data-stu-id="a573a-521">5</span></span>

<span data-ttu-id="a573a-522">6</span><span class="sxs-lookup"><span data-stu-id="a573a-522">6</span></span>

<span data-ttu-id="a573a-523">7</span><span class="sxs-lookup"><span data-stu-id="a573a-523">7</span></span>

<span data-ttu-id="a573a-524">8</span><span class="sxs-lookup"><span data-stu-id="a573a-524">8</span></span>

<span data-ttu-id="a573a-525">9</span><span class="sxs-lookup"><span data-stu-id="a573a-525">9</span></span>

<span data-ttu-id="a573a-526">2</span><span class="sxs-lookup"><span data-stu-id="a573a-526">2</span></span><br/> <span data-ttu-id="a573a-527">0</span><span class="sxs-lookup"><span data-stu-id="a573a-527">0</span></span><br/>

<span data-ttu-id="a573a-528">1</span><span class="sxs-lookup"><span data-stu-id="a573a-528">1</span></span>

<span data-ttu-id="a573a-529">2</span><span class="sxs-lookup"><span data-stu-id="a573a-529">2</span></span>

<span data-ttu-id="a573a-530">3</span><span class="sxs-lookup"><span data-stu-id="a573a-530">3</span></span>

<span data-ttu-id="a573a-531">4</span><span class="sxs-lookup"><span data-stu-id="a573a-531">4</span></span>

<span data-ttu-id="a573a-532">5</span><span class="sxs-lookup"><span data-stu-id="a573a-532">5</span></span>

<span data-ttu-id="a573a-533">6</span><span class="sxs-lookup"><span data-stu-id="a573a-533">6</span></span>

<span data-ttu-id="a573a-534">7</span><span class="sxs-lookup"><span data-stu-id="a573a-534">7</span></span>

<span data-ttu-id="a573a-535">8</span><span class="sxs-lookup"><span data-stu-id="a573a-535">8</span></span>

<span data-ttu-id="a573a-536">9</span><span class="sxs-lookup"><span data-stu-id="a573a-536">9</span></span>

<span data-ttu-id="a573a-537">3</span><span class="sxs-lookup"><span data-stu-id="a573a-537">3</span></span><br/> <span data-ttu-id="a573a-538">0</span><span class="sxs-lookup"><span data-stu-id="a573a-538">0</span></span><br/>

<span data-ttu-id="a573a-539">1</span><span class="sxs-lookup"><span data-stu-id="a573a-539">1</span></span>

<span data-ttu-id="a573a-540">кбсизе</span><span class="sxs-lookup"><span data-stu-id="a573a-540">cbSize</span></span>

<span data-ttu-id="a573a-541">Блобдата (переменная, необязательный)</span><span class="sxs-lookup"><span data-stu-id="a573a-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="a573a-542">**кбсизе**: 32-разрядное целое число без знака, указывающее размер поля блобдата в байтах.</span><span class="sxs-lookup"><span data-stu-id="a573a-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="a573a-543">Если Втипе имеет значение VT \_ BSTR или VT \_ LPSTR, для кбсизе должно быть задано значение 0x00000000, если представленная строка является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="a573a-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="a573a-544">**блобдата**: длина должна быть кбсизе в байтах.</span><span class="sxs-lookup"><span data-stu-id="a573a-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="a573a-545">Если для Втипе задано значение VT \_ BLOB, это поле будет иметь непрозрачные двоичные данные BLOB.</span><span class="sxs-lookup"><span data-stu-id="a573a-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="a573a-546">Для Втипе, установленного в VT \_ BSTR, это поле представляет собой набор символов в выбранной кодировке OEM.</span><span class="sxs-lookup"><span data-stu-id="a573a-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="a573a-547">Клиент и сервер должны быть настроены для использования набора символов с возможностью взаимодействия (по протоколу внешнего вида протокола).</span><span class="sxs-lookup"><span data-stu-id="a573a-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="a573a-548">Нет необходимости завершать его нулем.</span><span class="sxs-lookup"><span data-stu-id="a573a-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="a573a-549">Для Втипе, установленного в VT \_ LPSTR, это поле является строкой символов, завершающейся нулем, в выбранной кодировке OEM.</span><span class="sxs-lookup"><span data-stu-id="a573a-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="a573a-550">Клиент и сервер должны быть настроены для использования набора символов с возможностью взаимодействия (по протоколу внешнего вида протокола).</span><span class="sxs-lookup"><span data-stu-id="a573a-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="a573a-551">Если Втипе имеет значение VT \_ LPWSTR, структура управляемое vValue указывается на следующей схеме:</span><span class="sxs-lookup"><span data-stu-id="a573a-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="a573a-552">0</span><span class="sxs-lookup"><span data-stu-id="a573a-552">0</span></span>

<span data-ttu-id="a573a-553">1</span><span class="sxs-lookup"><span data-stu-id="a573a-553">1</span></span>

<span data-ttu-id="a573a-554">2</span><span class="sxs-lookup"><span data-stu-id="a573a-554">2</span></span>

<span data-ttu-id="a573a-555">3</span><span class="sxs-lookup"><span data-stu-id="a573a-555">3</span></span>

<span data-ttu-id="a573a-556">4</span><span class="sxs-lookup"><span data-stu-id="a573a-556">4</span></span>

<span data-ttu-id="a573a-557">5</span><span class="sxs-lookup"><span data-stu-id="a573a-557">5</span></span>

<span data-ttu-id="a573a-558">6</span><span class="sxs-lookup"><span data-stu-id="a573a-558">6</span></span>

<span data-ttu-id="a573a-559">7</span><span class="sxs-lookup"><span data-stu-id="a573a-559">7</span></span>

<span data-ttu-id="a573a-560">8</span><span class="sxs-lookup"><span data-stu-id="a573a-560">8</span></span>

<span data-ttu-id="a573a-561">9</span><span class="sxs-lookup"><span data-stu-id="a573a-561">9</span></span>

<span data-ttu-id="a573a-562">1</span><span class="sxs-lookup"><span data-stu-id="a573a-562">1</span></span><br/> <span data-ttu-id="a573a-563">0</span><span class="sxs-lookup"><span data-stu-id="a573a-563">0</span></span><br/>

<span data-ttu-id="a573a-564">1</span><span class="sxs-lookup"><span data-stu-id="a573a-564">1</span></span>

<span data-ttu-id="a573a-565">2</span><span class="sxs-lookup"><span data-stu-id="a573a-565">2</span></span>

<span data-ttu-id="a573a-566">3</span><span class="sxs-lookup"><span data-stu-id="a573a-566">3</span></span>

<span data-ttu-id="a573a-567">4</span><span class="sxs-lookup"><span data-stu-id="a573a-567">4</span></span>

<span data-ttu-id="a573a-568">5</span><span class="sxs-lookup"><span data-stu-id="a573a-568">5</span></span>

<span data-ttu-id="a573a-569">6</span><span class="sxs-lookup"><span data-stu-id="a573a-569">6</span></span>

<span data-ttu-id="a573a-570">7</span><span class="sxs-lookup"><span data-stu-id="a573a-570">7</span></span>

<span data-ttu-id="a573a-571">8</span><span class="sxs-lookup"><span data-stu-id="a573a-571">8</span></span>

<span data-ttu-id="a573a-572">9</span><span class="sxs-lookup"><span data-stu-id="a573a-572">9</span></span>

<span data-ttu-id="a573a-573">2</span><span class="sxs-lookup"><span data-stu-id="a573a-573">2</span></span><br/> <span data-ttu-id="a573a-574">0</span><span class="sxs-lookup"><span data-stu-id="a573a-574">0</span></span><br/>

<span data-ttu-id="a573a-575">1</span><span class="sxs-lookup"><span data-stu-id="a573a-575">1</span></span>

<span data-ttu-id="a573a-576">2</span><span class="sxs-lookup"><span data-stu-id="a573a-576">2</span></span>

<span data-ttu-id="a573a-577">3</span><span class="sxs-lookup"><span data-stu-id="a573a-577">3</span></span>

<span data-ttu-id="a573a-578">4</span><span class="sxs-lookup"><span data-stu-id="a573a-578">4</span></span>

<span data-ttu-id="a573a-579">5</span><span class="sxs-lookup"><span data-stu-id="a573a-579">5</span></span>

<span data-ttu-id="a573a-580">6</span><span class="sxs-lookup"><span data-stu-id="a573a-580">6</span></span>

<span data-ttu-id="a573a-581">7</span><span class="sxs-lookup"><span data-stu-id="a573a-581">7</span></span>

<span data-ttu-id="a573a-582">8</span><span class="sxs-lookup"><span data-stu-id="a573a-582">8</span></span>

<span data-ttu-id="a573a-583">9</span><span class="sxs-lookup"><span data-stu-id="a573a-583">9</span></span>

<span data-ttu-id="a573a-584">3</span><span class="sxs-lookup"><span data-stu-id="a573a-584">3</span></span><br/> <span data-ttu-id="a573a-585">0</span><span class="sxs-lookup"><span data-stu-id="a573a-585">0</span></span><br/>

<span data-ttu-id="a573a-586">1</span><span class="sxs-lookup"><span data-stu-id="a573a-586">1</span></span>

<span data-ttu-id="a573a-587">кклен</span><span class="sxs-lookup"><span data-stu-id="a573a-587">ccLen</span></span>

<span data-ttu-id="a573a-588">String (переменная, необязательная)</span><span class="sxs-lookup"><span data-stu-id="a573a-588">string (variable, optional)</span></span>



 

<span data-ttu-id="a573a-589">**кклен**: 32-разрядное целое число без знака, указывающее размер строкового поля в символах Юникода.</span><span class="sxs-lookup"><span data-stu-id="a573a-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="a573a-590">Для пустой строки необходимо задать значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="a573a-591">**строка**: строка Юникода, заканчивающаяся нулем.</span><span class="sxs-lookup"><span data-stu-id="a573a-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="a573a-592">2.2.1.1.1 Кбасесторажевариант структуры</span><span class="sxs-lookup"><span data-stu-id="a573a-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="a573a-593">В структуре Кбасесторажевариант используются следующие структуры.</span><span class="sxs-lookup"><span data-stu-id="a573a-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="a573a-594">2.2.1.1.1.1 DECIMAL</span><span class="sxs-lookup"><span data-stu-id="a573a-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="a573a-595">Значение DECIMAL используется для представления точного числового значения с фиксированной точностью и фиксированным масштабом.</span><span class="sxs-lookup"><span data-stu-id="a573a-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="a573a-596">Если для Втипе задано значение VT \_ Decimal (0x0000E), то поля vData1 и vData2 в КБАСЕСТОРАЖЕВАРИАНТ должны интерпретироваться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="a573a-597">**vData1**: количество цифр справа от десятичной запятой.</span><span class="sxs-lookup"><span data-stu-id="a573a-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="a573a-598">Значение должно находиться в диапазоне от 0 до 28.</span><span class="sxs-lookup"><span data-stu-id="a573a-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="a573a-599">**vData2**: знак числового значения.</span><span class="sxs-lookup"><span data-stu-id="a573a-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="a573a-600">Задайте значение 0x00, если положительный, 0x80, если отрицательный.</span><span class="sxs-lookup"><span data-stu-id="a573a-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="a573a-601">Формат поля управляемое vValue:</span><span class="sxs-lookup"><span data-stu-id="a573a-601">The format of the vValue field is:</span></span>



<span data-ttu-id="a573a-602">0</span><span class="sxs-lookup"><span data-stu-id="a573a-602">0</span></span>

<span data-ttu-id="a573a-603">1</span><span class="sxs-lookup"><span data-stu-id="a573a-603">1</span></span>

<span data-ttu-id="a573a-604">2</span><span class="sxs-lookup"><span data-stu-id="a573a-604">2</span></span>

<span data-ttu-id="a573a-605">3</span><span class="sxs-lookup"><span data-stu-id="a573a-605">3</span></span>

<span data-ttu-id="a573a-606">4</span><span class="sxs-lookup"><span data-stu-id="a573a-606">4</span></span>

<span data-ttu-id="a573a-607">5</span><span class="sxs-lookup"><span data-stu-id="a573a-607">5</span></span>

<span data-ttu-id="a573a-608">6</span><span class="sxs-lookup"><span data-stu-id="a573a-608">6</span></span>

<span data-ttu-id="a573a-609">7</span><span class="sxs-lookup"><span data-stu-id="a573a-609">7</span></span>

<span data-ttu-id="a573a-610">8</span><span class="sxs-lookup"><span data-stu-id="a573a-610">8</span></span>

<span data-ttu-id="a573a-611">9</span><span class="sxs-lookup"><span data-stu-id="a573a-611">9</span></span>

<span data-ttu-id="a573a-612">1</span><span class="sxs-lookup"><span data-stu-id="a573a-612">1</span></span><br/> <span data-ttu-id="a573a-613">0</span><span class="sxs-lookup"><span data-stu-id="a573a-613">0</span></span><br/>

<span data-ttu-id="a573a-614">1</span><span class="sxs-lookup"><span data-stu-id="a573a-614">1</span></span>

<span data-ttu-id="a573a-615">2</span><span class="sxs-lookup"><span data-stu-id="a573a-615">2</span></span>

<span data-ttu-id="a573a-616">3</span><span class="sxs-lookup"><span data-stu-id="a573a-616">3</span></span>

<span data-ttu-id="a573a-617">4</span><span class="sxs-lookup"><span data-stu-id="a573a-617">4</span></span>

<span data-ttu-id="a573a-618">5</span><span class="sxs-lookup"><span data-stu-id="a573a-618">5</span></span>

<span data-ttu-id="a573a-619">6</span><span class="sxs-lookup"><span data-stu-id="a573a-619">6</span></span>

<span data-ttu-id="a573a-620">7</span><span class="sxs-lookup"><span data-stu-id="a573a-620">7</span></span>

<span data-ttu-id="a573a-621">8</span><span class="sxs-lookup"><span data-stu-id="a573a-621">8</span></span>

<span data-ttu-id="a573a-622">9</span><span class="sxs-lookup"><span data-stu-id="a573a-622">9</span></span>

<span data-ttu-id="a573a-623">2</span><span class="sxs-lookup"><span data-stu-id="a573a-623">2</span></span><br/> <span data-ttu-id="a573a-624">0</span><span class="sxs-lookup"><span data-stu-id="a573a-624">0</span></span><br/>

<span data-ttu-id="a573a-625">1</span><span class="sxs-lookup"><span data-stu-id="a573a-625">1</span></span>

<span data-ttu-id="a573a-626">2</span><span class="sxs-lookup"><span data-stu-id="a573a-626">2</span></span>

<span data-ttu-id="a573a-627">3</span><span class="sxs-lookup"><span data-stu-id="a573a-627">3</span></span>

<span data-ttu-id="a573a-628">4</span><span class="sxs-lookup"><span data-stu-id="a573a-628">4</span></span>

<span data-ttu-id="a573a-629">5</span><span class="sxs-lookup"><span data-stu-id="a573a-629">5</span></span>

<span data-ttu-id="a573a-630">6</span><span class="sxs-lookup"><span data-stu-id="a573a-630">6</span></span>

<span data-ttu-id="a573a-631">7</span><span class="sxs-lookup"><span data-stu-id="a573a-631">7</span></span>

<span data-ttu-id="a573a-632">8</span><span class="sxs-lookup"><span data-stu-id="a573a-632">8</span></span>

<span data-ttu-id="a573a-633">9</span><span class="sxs-lookup"><span data-stu-id="a573a-633">9</span></span>

<span data-ttu-id="a573a-634">3</span><span class="sxs-lookup"><span data-stu-id="a573a-634">3</span></span><br/> <span data-ttu-id="a573a-635">0</span><span class="sxs-lookup"><span data-stu-id="a573a-635">0</span></span><br/>

<span data-ttu-id="a573a-636">1</span><span class="sxs-lookup"><span data-stu-id="a573a-636">1</span></span>

<span data-ttu-id="a573a-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="a573a-637">Hi32</span></span>

<span data-ttu-id="a573a-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="a573a-638">Lo32</span></span>

<span data-ttu-id="a573a-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="a573a-639">Mid32</span></span>



 

<span data-ttu-id="a573a-640">**Hi32**: наибольшее число 32 бит 96 разрядов.</span><span class="sxs-lookup"><span data-stu-id="a573a-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="a573a-641">**Lo32**: младшие 32 бита 96 разрядного целого числа.</span><span class="sxs-lookup"><span data-stu-id="a573a-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="a573a-642">**Mid32**: середина 32 бит 96 разрядного целого числа.</span><span class="sxs-lookup"><span data-stu-id="a573a-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="a573a-643">вектор 2.2.1.1.1.2 VT \_</span><span class="sxs-lookup"><span data-stu-id="a573a-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="a573a-644">\_Вектор VT используется для передачи одномерных массивов.</span><span class="sxs-lookup"><span data-stu-id="a573a-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="a573a-645">0</span><span class="sxs-lookup"><span data-stu-id="a573a-645">0</span></span>

<span data-ttu-id="a573a-646">1</span><span class="sxs-lookup"><span data-stu-id="a573a-646">1</span></span>

<span data-ttu-id="a573a-647">2</span><span class="sxs-lookup"><span data-stu-id="a573a-647">2</span></span>

<span data-ttu-id="a573a-648">3</span><span class="sxs-lookup"><span data-stu-id="a573a-648">3</span></span>

<span data-ttu-id="a573a-649">4</span><span class="sxs-lookup"><span data-stu-id="a573a-649">4</span></span>

<span data-ttu-id="a573a-650">5</span><span class="sxs-lookup"><span data-stu-id="a573a-650">5</span></span>

<span data-ttu-id="a573a-651">6</span><span class="sxs-lookup"><span data-stu-id="a573a-651">6</span></span>

<span data-ttu-id="a573a-652">7</span><span class="sxs-lookup"><span data-stu-id="a573a-652">7</span></span>

<span data-ttu-id="a573a-653">8</span><span class="sxs-lookup"><span data-stu-id="a573a-653">8</span></span>

<span data-ttu-id="a573a-654">9</span><span class="sxs-lookup"><span data-stu-id="a573a-654">9</span></span>

<span data-ttu-id="a573a-655">1</span><span class="sxs-lookup"><span data-stu-id="a573a-655">1</span></span><br/> <span data-ttu-id="a573a-656">0</span><span class="sxs-lookup"><span data-stu-id="a573a-656">0</span></span><br/>

<span data-ttu-id="a573a-657">1</span><span class="sxs-lookup"><span data-stu-id="a573a-657">1</span></span>

<span data-ttu-id="a573a-658">2</span><span class="sxs-lookup"><span data-stu-id="a573a-658">2</span></span>

<span data-ttu-id="a573a-659">3</span><span class="sxs-lookup"><span data-stu-id="a573a-659">3</span></span>

<span data-ttu-id="a573a-660">4</span><span class="sxs-lookup"><span data-stu-id="a573a-660">4</span></span>

<span data-ttu-id="a573a-661">5</span><span class="sxs-lookup"><span data-stu-id="a573a-661">5</span></span>

<span data-ttu-id="a573a-662">6</span><span class="sxs-lookup"><span data-stu-id="a573a-662">6</span></span>

<span data-ttu-id="a573a-663">7</span><span class="sxs-lookup"><span data-stu-id="a573a-663">7</span></span>

<span data-ttu-id="a573a-664">8</span><span class="sxs-lookup"><span data-stu-id="a573a-664">8</span></span>

<span data-ttu-id="a573a-665">9</span><span class="sxs-lookup"><span data-stu-id="a573a-665">9</span></span>

<span data-ttu-id="a573a-666">2</span><span class="sxs-lookup"><span data-stu-id="a573a-666">2</span></span><br/> <span data-ttu-id="a573a-667">0</span><span class="sxs-lookup"><span data-stu-id="a573a-667">0</span></span><br/>

<span data-ttu-id="a573a-668">1</span><span class="sxs-lookup"><span data-stu-id="a573a-668">1</span></span>

<span data-ttu-id="a573a-669">2</span><span class="sxs-lookup"><span data-stu-id="a573a-669">2</span></span>

<span data-ttu-id="a573a-670">3</span><span class="sxs-lookup"><span data-stu-id="a573a-670">3</span></span>

<span data-ttu-id="a573a-671">4</span><span class="sxs-lookup"><span data-stu-id="a573a-671">4</span></span>

<span data-ttu-id="a573a-672">5</span><span class="sxs-lookup"><span data-stu-id="a573a-672">5</span></span>

<span data-ttu-id="a573a-673">6</span><span class="sxs-lookup"><span data-stu-id="a573a-673">6</span></span>

<span data-ttu-id="a573a-674">7</span><span class="sxs-lookup"><span data-stu-id="a573a-674">7</span></span>

<span data-ttu-id="a573a-675">8</span><span class="sxs-lookup"><span data-stu-id="a573a-675">8</span></span>

<span data-ttu-id="a573a-676">9</span><span class="sxs-lookup"><span data-stu-id="a573a-676">9</span></span>

<span data-ttu-id="a573a-677">3</span><span class="sxs-lookup"><span data-stu-id="a573a-677">3</span></span><br/> <span data-ttu-id="a573a-678">0</span><span class="sxs-lookup"><span data-stu-id="a573a-678">0</span></span><br/>

<span data-ttu-id="a573a-679">1</span><span class="sxs-lookup"><span data-stu-id="a573a-679">1</span></span>

<span data-ttu-id="a573a-680">ввекторелементс</span><span class="sxs-lookup"><span data-stu-id="a573a-680">vVectorElements</span></span>

<span data-ttu-id="a573a-681">ввектордата</span><span class="sxs-lookup"><span data-stu-id="a573a-681">vVectorData</span></span>



 

<span data-ttu-id="a573a-682">**ввекторелементс**: 32-разрядное целое число без знака, указывающее количество элементов в поле ввектордата.</span><span class="sxs-lookup"><span data-stu-id="a573a-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="a573a-683">**ввектордата**: массив элементов, имеющих тип, обозначенный параметром втипе с сброшенным битом 0x1000.</span><span class="sxs-lookup"><span data-stu-id="a573a-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="a573a-684">Размер отдельного элемента фиксированной длины можно получить из таблицы типов данных фиксированной длины, как указано в разделе 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="a573a-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="a573a-685">Длина этого поля в байтах может быть вычислена путем умножения Ввекторелементс на размер отдельного элемента.</span><span class="sxs-lookup"><span data-stu-id="a573a-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="a573a-686">Для типов данных переменной длины Ввектордата содержит последовательность последовательных упакованных простых типов, где тип обозначается параметром Втипе с сброшенным битом 0x1000.</span><span class="sxs-lookup"><span data-stu-id="a573a-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="a573a-687">Это включает особый случай, обозначенный Втипе VT \_ array \| VT \_ (т. е. 0x100C).</span><span class="sxs-lookup"><span data-stu-id="a573a-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="a573a-688">Элементы в поле Ввектордата должны быть разделены от 0 до 3 байтов, чтобы каждый элемент начинался со смещения, кратного 4 байтам от начала сообщения, содержащего этот массив.</span><span class="sxs-lookup"><span data-stu-id="a573a-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="a573a-689">Если заданы байты заполнения, то значение, которое они содержат, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="a573a-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="a573a-690">Содержимое байтов заполнения должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="a573a-691">Для Втипе, установленного в VT \_ array \| VT \_ , тип для элементов в этой последовательности — кбасесторажевариант.</span><span class="sxs-lookup"><span data-stu-id="a573a-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="a573a-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="a573a-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="a573a-693">SAFEARRAY используется для передачи многомерных массивов.</span><span class="sxs-lookup"><span data-stu-id="a573a-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="a573a-694">Структура содержит сведения о размере массива, а также данные в массиве.</span><span class="sxs-lookup"><span data-stu-id="a573a-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="a573a-695">0</span><span class="sxs-lookup"><span data-stu-id="a573a-695">0</span></span>

<span data-ttu-id="a573a-696">1</span><span class="sxs-lookup"><span data-stu-id="a573a-696">1</span></span>

<span data-ttu-id="a573a-697">2</span><span class="sxs-lookup"><span data-stu-id="a573a-697">2</span></span>

<span data-ttu-id="a573a-698">3</span><span class="sxs-lookup"><span data-stu-id="a573a-698">3</span></span>

<span data-ttu-id="a573a-699">4</span><span class="sxs-lookup"><span data-stu-id="a573a-699">4</span></span>

<span data-ttu-id="a573a-700">5</span><span class="sxs-lookup"><span data-stu-id="a573a-700">5</span></span>

<span data-ttu-id="a573a-701">6</span><span class="sxs-lookup"><span data-stu-id="a573a-701">6</span></span>

<span data-ttu-id="a573a-702">7</span><span class="sxs-lookup"><span data-stu-id="a573a-702">7</span></span>

<span data-ttu-id="a573a-703">8</span><span class="sxs-lookup"><span data-stu-id="a573a-703">8</span></span>

<span data-ttu-id="a573a-704">9</span><span class="sxs-lookup"><span data-stu-id="a573a-704">9</span></span>

<span data-ttu-id="a573a-705">1</span><span class="sxs-lookup"><span data-stu-id="a573a-705">1</span></span><br/> <span data-ttu-id="a573a-706">0</span><span class="sxs-lookup"><span data-stu-id="a573a-706">0</span></span><br/>

<span data-ttu-id="a573a-707">1</span><span class="sxs-lookup"><span data-stu-id="a573a-707">1</span></span>

<span data-ttu-id="a573a-708">2</span><span class="sxs-lookup"><span data-stu-id="a573a-708">2</span></span>

<span data-ttu-id="a573a-709">3</span><span class="sxs-lookup"><span data-stu-id="a573a-709">3</span></span>

<span data-ttu-id="a573a-710">4</span><span class="sxs-lookup"><span data-stu-id="a573a-710">4</span></span>

<span data-ttu-id="a573a-711">5</span><span class="sxs-lookup"><span data-stu-id="a573a-711">5</span></span>

<span data-ttu-id="a573a-712">6</span><span class="sxs-lookup"><span data-stu-id="a573a-712">6</span></span>

<span data-ttu-id="a573a-713">7</span><span class="sxs-lookup"><span data-stu-id="a573a-713">7</span></span>

<span data-ttu-id="a573a-714">8</span><span class="sxs-lookup"><span data-stu-id="a573a-714">8</span></span>

<span data-ttu-id="a573a-715">9</span><span class="sxs-lookup"><span data-stu-id="a573a-715">9</span></span>

<span data-ttu-id="a573a-716">2</span><span class="sxs-lookup"><span data-stu-id="a573a-716">2</span></span><br/> <span data-ttu-id="a573a-717">0</span><span class="sxs-lookup"><span data-stu-id="a573a-717">0</span></span><br/>

<span data-ttu-id="a573a-718">1</span><span class="sxs-lookup"><span data-stu-id="a573a-718">1</span></span>

<span data-ttu-id="a573a-719">2</span><span class="sxs-lookup"><span data-stu-id="a573a-719">2</span></span>

<span data-ttu-id="a573a-720">3</span><span class="sxs-lookup"><span data-stu-id="a573a-720">3</span></span>

<span data-ttu-id="a573a-721">4</span><span class="sxs-lookup"><span data-stu-id="a573a-721">4</span></span>

<span data-ttu-id="a573a-722">5</span><span class="sxs-lookup"><span data-stu-id="a573a-722">5</span></span>

<span data-ttu-id="a573a-723">6</span><span class="sxs-lookup"><span data-stu-id="a573a-723">6</span></span>

<span data-ttu-id="a573a-724">7</span><span class="sxs-lookup"><span data-stu-id="a573a-724">7</span></span>

<span data-ttu-id="a573a-725">8</span><span class="sxs-lookup"><span data-stu-id="a573a-725">8</span></span>

<span data-ttu-id="a573a-726">9</span><span class="sxs-lookup"><span data-stu-id="a573a-726">9</span></span>

<span data-ttu-id="a573a-727">3</span><span class="sxs-lookup"><span data-stu-id="a573a-727">3</span></span><br/> <span data-ttu-id="a573a-728">0</span><span class="sxs-lookup"><span data-stu-id="a573a-728">0</span></span><br/>

<span data-ttu-id="a573a-729">1</span><span class="sxs-lookup"><span data-stu-id="a573a-729">1</span></span>

<span data-ttu-id="a573a-730">кдимс</span><span class="sxs-lookup"><span data-stu-id="a573a-730">cDims</span></span>

<span data-ttu-id="a573a-731">ффеатурес</span><span class="sxs-lookup"><span data-stu-id="a573a-731">fFeatures</span></span>

<span data-ttu-id="a573a-732">кбелементс</span><span class="sxs-lookup"><span data-stu-id="a573a-732">cbElements</span></span>

<span data-ttu-id="a573a-733">Ргсабаунд (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-733">Rgsabound (variable)</span></span>

<span data-ttu-id="a573a-734">Вдата (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-734">vData (variable)</span></span>



 

<span data-ttu-id="a573a-735">**кдимс**: 16-разрядное целое число без знака, указывающее количество измерений многомерного массива.</span><span class="sxs-lookup"><span data-stu-id="a573a-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="a573a-736">**ффеатурес**: 16-разрядное битовое значение.</span><span class="sxs-lookup"><span data-stu-id="a573a-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="a573a-737">Значения представляют функции, определенные приложениями верхнего уровня, и должны игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="a573a-738">**кбелементс**: 32-битовое целое число без знака, указывающее размер каждого элемента массива.</span><span class="sxs-lookup"><span data-stu-id="a573a-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="a573a-739">**Ргсабаунд**: массив, содержащий одну структуру сафеаррайбаунд, как указано в разделе 2.2.1.1.1.4, для измерения в массиве SafeArray.</span><span class="sxs-lookup"><span data-stu-id="a573a-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="a573a-740">В этом массиве сначала находится крайне левое измерение, а в последнем — крайнее правое измерение.</span><span class="sxs-lookup"><span data-stu-id="a573a-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="a573a-741">**вдата**: вектор упакованных элементов определенного типа, обозначенный втипеом содержащего кбасесторажевариант, с битом 0x2000.</span><span class="sxs-lookup"><span data-stu-id="a573a-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="a573a-742">Вдата маршалируется аналогично \_ вектору VT, как указано в разделе 2.2.1.1.1.2, с разницей, что число элементов не сохраняется перед вектором.</span><span class="sxs-lookup"><span data-stu-id="a573a-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="a573a-743">Вместо этого число элементов вычисляется путем умножения значения Целементс на все защищенные границы массива, заданные в поле Ргсабаунд.</span><span class="sxs-lookup"><span data-stu-id="a573a-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="a573a-744">Элементы хранятся в векторе в порядке измерений, начиная с крайнего правого измерения.</span><span class="sxs-lookup"><span data-stu-id="a573a-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="a573a-745">Следующая диаграмма наглядно представляет пример двумерного массива.</span><span class="sxs-lookup"><span data-stu-id="a573a-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="a573a-746">Первое измерение имеет Целементс, равное 4 (представлен горизонтально) и Ллбаунд равно 0, а второе измерение имеет Целементс, равное 2 (представлен вертикально), а Ллбаунд равно 0.</span><span class="sxs-lookup"><span data-stu-id="a573a-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="a573a-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-747">0x00000001</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="a573a-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-748">0x00000002</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="a573a-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-749">0x00000003</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="a573a-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="a573a-750">0x00000005</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="a573a-751">:: Row:::</span><span class="sxs-lookup"><span data-stu-id="a573a-751">::row:::</span></span>
    :::column:::
        0x00000007
    :::column-end:::
    :::column:::
        0x00000011
    :::column-end:::
    :::column:::
        0x00000013
    :::column-end:::
    :::column:::
        0x00000017
    :::column-end:::
:::row-end:::

<span data-ttu-id="a573a-752">С помощью приведенной выше схемы Вдата будет содержать следующую последовательность: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (сначала просматривая крайнее правое измерение, а затем увеличив следующее измерение).</span><span class="sxs-lookup"><span data-stu-id="a573a-752">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="a573a-753">Предыдущая Ргсабаунд (которая регистрирует Целементс и LBound) будет выглядеть следующим образом: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-753">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="a573a-754">2.2.1.1.1.4 САФЕАРРАЙБАУНД</span><span class="sxs-lookup"><span data-stu-id="a573a-754">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="a573a-755">Структура САФЕАРРАЙБАУНД представляет границы одного измерения SAFEARRAY или SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="a573a-755">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="a573a-756">Он имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="a573a-756">Its format is:</span></span>



<span data-ttu-id="a573a-757">0</span><span class="sxs-lookup"><span data-stu-id="a573a-757">0</span></span>

<span data-ttu-id="a573a-758">1</span><span class="sxs-lookup"><span data-stu-id="a573a-758">1</span></span>

<span data-ttu-id="a573a-759">2</span><span class="sxs-lookup"><span data-stu-id="a573a-759">2</span></span>

<span data-ttu-id="a573a-760">3</span><span class="sxs-lookup"><span data-stu-id="a573a-760">3</span></span>

<span data-ttu-id="a573a-761">4</span><span class="sxs-lookup"><span data-stu-id="a573a-761">4</span></span>

<span data-ttu-id="a573a-762">5</span><span class="sxs-lookup"><span data-stu-id="a573a-762">5</span></span>

<span data-ttu-id="a573a-763">6</span><span class="sxs-lookup"><span data-stu-id="a573a-763">6</span></span>

<span data-ttu-id="a573a-764">7</span><span class="sxs-lookup"><span data-stu-id="a573a-764">7</span></span>

<span data-ttu-id="a573a-765">8</span><span class="sxs-lookup"><span data-stu-id="a573a-765">8</span></span>

<span data-ttu-id="a573a-766">9</span><span class="sxs-lookup"><span data-stu-id="a573a-766">9</span></span>

<span data-ttu-id="a573a-767">1</span><span class="sxs-lookup"><span data-stu-id="a573a-767">1</span></span><br/> <span data-ttu-id="a573a-768">0</span><span class="sxs-lookup"><span data-stu-id="a573a-768">0</span></span><br/>

<span data-ttu-id="a573a-769">1</span><span class="sxs-lookup"><span data-stu-id="a573a-769">1</span></span>

<span data-ttu-id="a573a-770">2</span><span class="sxs-lookup"><span data-stu-id="a573a-770">2</span></span>

<span data-ttu-id="a573a-771">3</span><span class="sxs-lookup"><span data-stu-id="a573a-771">3</span></span>

<span data-ttu-id="a573a-772">4</span><span class="sxs-lookup"><span data-stu-id="a573a-772">4</span></span>

<span data-ttu-id="a573a-773">5</span><span class="sxs-lookup"><span data-stu-id="a573a-773">5</span></span>

<span data-ttu-id="a573a-774">6</span><span class="sxs-lookup"><span data-stu-id="a573a-774">6</span></span>

<span data-ttu-id="a573a-775">7</span><span class="sxs-lookup"><span data-stu-id="a573a-775">7</span></span>

<span data-ttu-id="a573a-776">8</span><span class="sxs-lookup"><span data-stu-id="a573a-776">8</span></span>

<span data-ttu-id="a573a-777">9</span><span class="sxs-lookup"><span data-stu-id="a573a-777">9</span></span>

<span data-ttu-id="a573a-778">2</span><span class="sxs-lookup"><span data-stu-id="a573a-778">2</span></span><br/> <span data-ttu-id="a573a-779">0</span><span class="sxs-lookup"><span data-stu-id="a573a-779">0</span></span><br/>

<span data-ttu-id="a573a-780">1</span><span class="sxs-lookup"><span data-stu-id="a573a-780">1</span></span>

<span data-ttu-id="a573a-781">2</span><span class="sxs-lookup"><span data-stu-id="a573a-781">2</span></span>

<span data-ttu-id="a573a-782">3</span><span class="sxs-lookup"><span data-stu-id="a573a-782">3</span></span>

<span data-ttu-id="a573a-783">4</span><span class="sxs-lookup"><span data-stu-id="a573a-783">4</span></span>

<span data-ttu-id="a573a-784">5</span><span class="sxs-lookup"><span data-stu-id="a573a-784">5</span></span>

<span data-ttu-id="a573a-785">6</span><span class="sxs-lookup"><span data-stu-id="a573a-785">6</span></span>

<span data-ttu-id="a573a-786">7</span><span class="sxs-lookup"><span data-stu-id="a573a-786">7</span></span>

<span data-ttu-id="a573a-787">8</span><span class="sxs-lookup"><span data-stu-id="a573a-787">8</span></span>

<span data-ttu-id="a573a-788">9</span><span class="sxs-lookup"><span data-stu-id="a573a-788">9</span></span>

<span data-ttu-id="a573a-789">3</span><span class="sxs-lookup"><span data-stu-id="a573a-789">3</span></span><br/> <span data-ttu-id="a573a-790">0</span><span class="sxs-lookup"><span data-stu-id="a573a-790">0</span></span><br/>

<span data-ttu-id="a573a-791">1</span><span class="sxs-lookup"><span data-stu-id="a573a-791">1</span></span>

<span data-ttu-id="a573a-792">целементс</span><span class="sxs-lookup"><span data-stu-id="a573a-792">cElements</span></span>

<span data-ttu-id="a573a-793">ллбаунд</span><span class="sxs-lookup"><span data-stu-id="a573a-793">lLbound</span></span>



 

<span data-ttu-id="a573a-794">**целементс**: 32-битовое целое число без знака, указывающее количество элементов в измерении.</span><span class="sxs-lookup"><span data-stu-id="a573a-794">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="a573a-795">**ллбаунд**: 32-битовое целое число без знака, задающее нижнюю границу измерения.</span><span class="sxs-lookup"><span data-stu-id="a573a-795">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="a573a-796">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="a573a-796">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="a573a-797">SAFEARRAY2 используется для передачи многомерных массивов в СЕРИАЛИЗЕДПРОПЕРТИВАЛУЕ.</span><span class="sxs-lookup"><span data-stu-id="a573a-797">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="a573a-798">Структура содержит сведения о границах, а также данные.</span><span class="sxs-lookup"><span data-stu-id="a573a-798">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="a573a-799">0</span><span class="sxs-lookup"><span data-stu-id="a573a-799">0</span></span>

<span data-ttu-id="a573a-800">1</span><span class="sxs-lookup"><span data-stu-id="a573a-800">1</span></span>

<span data-ttu-id="a573a-801">2</span><span class="sxs-lookup"><span data-stu-id="a573a-801">2</span></span>

<span data-ttu-id="a573a-802">3</span><span class="sxs-lookup"><span data-stu-id="a573a-802">3</span></span>

<span data-ttu-id="a573a-803">4</span><span class="sxs-lookup"><span data-stu-id="a573a-803">4</span></span>

<span data-ttu-id="a573a-804">5</span><span class="sxs-lookup"><span data-stu-id="a573a-804">5</span></span>

<span data-ttu-id="a573a-805">6</span><span class="sxs-lookup"><span data-stu-id="a573a-805">6</span></span>

<span data-ttu-id="a573a-806">7</span><span class="sxs-lookup"><span data-stu-id="a573a-806">7</span></span>

<span data-ttu-id="a573a-807">8</span><span class="sxs-lookup"><span data-stu-id="a573a-807">8</span></span>

<span data-ttu-id="a573a-808">9</span><span class="sxs-lookup"><span data-stu-id="a573a-808">9</span></span>

<span data-ttu-id="a573a-809">1</span><span class="sxs-lookup"><span data-stu-id="a573a-809">1</span></span><br/> <span data-ttu-id="a573a-810">0</span><span class="sxs-lookup"><span data-stu-id="a573a-810">0</span></span><br/>

<span data-ttu-id="a573a-811">1</span><span class="sxs-lookup"><span data-stu-id="a573a-811">1</span></span>

<span data-ttu-id="a573a-812">2</span><span class="sxs-lookup"><span data-stu-id="a573a-812">2</span></span>

<span data-ttu-id="a573a-813">3</span><span class="sxs-lookup"><span data-stu-id="a573a-813">3</span></span>

<span data-ttu-id="a573a-814">4</span><span class="sxs-lookup"><span data-stu-id="a573a-814">4</span></span>

<span data-ttu-id="a573a-815">5</span><span class="sxs-lookup"><span data-stu-id="a573a-815">5</span></span>

<span data-ttu-id="a573a-816">6</span><span class="sxs-lookup"><span data-stu-id="a573a-816">6</span></span>

<span data-ttu-id="a573a-817">7</span><span class="sxs-lookup"><span data-stu-id="a573a-817">7</span></span>

<span data-ttu-id="a573a-818">8</span><span class="sxs-lookup"><span data-stu-id="a573a-818">8</span></span>

<span data-ttu-id="a573a-819">9</span><span class="sxs-lookup"><span data-stu-id="a573a-819">9</span></span>

<span data-ttu-id="a573a-820">2</span><span class="sxs-lookup"><span data-stu-id="a573a-820">2</span></span><br/> <span data-ttu-id="a573a-821">0</span><span class="sxs-lookup"><span data-stu-id="a573a-821">0</span></span><br/>

<span data-ttu-id="a573a-822">1</span><span class="sxs-lookup"><span data-stu-id="a573a-822">1</span></span>

<span data-ttu-id="a573a-823">2</span><span class="sxs-lookup"><span data-stu-id="a573a-823">2</span></span>

<span data-ttu-id="a573a-824">3</span><span class="sxs-lookup"><span data-stu-id="a573a-824">3</span></span>

<span data-ttu-id="a573a-825">4</span><span class="sxs-lookup"><span data-stu-id="a573a-825">4</span></span>

<span data-ttu-id="a573a-826">5</span><span class="sxs-lookup"><span data-stu-id="a573a-826">5</span></span>

<span data-ttu-id="a573a-827">6</span><span class="sxs-lookup"><span data-stu-id="a573a-827">6</span></span>

<span data-ttu-id="a573a-828">7</span><span class="sxs-lookup"><span data-stu-id="a573a-828">7</span></span>

<span data-ttu-id="a573a-829">8</span><span class="sxs-lookup"><span data-stu-id="a573a-829">8</span></span>

<span data-ttu-id="a573a-830">9</span><span class="sxs-lookup"><span data-stu-id="a573a-830">9</span></span>

<span data-ttu-id="a573a-831">3</span><span class="sxs-lookup"><span data-stu-id="a573a-831">3</span></span><br/> <span data-ttu-id="a573a-832">0</span><span class="sxs-lookup"><span data-stu-id="a573a-832">0</span></span><br/>

<span data-ttu-id="a573a-833">1</span><span class="sxs-lookup"><span data-stu-id="a573a-833">1</span></span>

<span data-ttu-id="a573a-834">кдимс</span><span class="sxs-lookup"><span data-stu-id="a573a-834">cDims</span></span>

<span data-ttu-id="a573a-835">Ргсабаунд (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-835">Rgsabound (variable)</span></span>

<span data-ttu-id="a573a-836">Вдата (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-836">vData (variable)</span></span>



 

<span data-ttu-id="a573a-837">**кдимс**: 32-разрядное целое число без знака, указывающее количество измерений SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="a573a-837">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="a573a-838">**Ргсабаунд**: массив, содержащий одну структуру сафеаррайбаунд, как указано в разделе 2.2.1.1.1.4 для измерения в SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="a573a-838">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="a573a-839">В этом массиве сначала находится крайне левое измерение, а в последнем — крайнее правое измерение.</span><span class="sxs-lookup"><span data-stu-id="a573a-839">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="a573a-840">**вдата**: вектор упакованных элементов определенного типа, обозначенный двтипеом содержащего сериализедпропертивалуе, с битом 0x2000.</span><span class="sxs-lookup"><span data-stu-id="a573a-840">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="a573a-841">Формат Вдата, аналогичный указанному для поля Вдата массива SAFEARRAY в разделе 2.2.1.1.1.3.</span><span class="sxs-lookup"><span data-stu-id="a573a-841">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="a573a-842">2.2.1.2 Кфуллпропспек</span><span class="sxs-lookup"><span data-stu-id="a573a-842">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="a573a-843">Структура Кфуллпропспек содержит идентификатор GUID набора свойств и идентификатор свойства для уникальной идентификации свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-843">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="a573a-844">0</span><span class="sxs-lookup"><span data-stu-id="a573a-844">0</span></span>

<span data-ttu-id="a573a-845">1</span><span class="sxs-lookup"><span data-stu-id="a573a-845">1</span></span>

<span data-ttu-id="a573a-846">2</span><span class="sxs-lookup"><span data-stu-id="a573a-846">2</span></span>

<span data-ttu-id="a573a-847">3</span><span class="sxs-lookup"><span data-stu-id="a573a-847">3</span></span>

<span data-ttu-id="a573a-848">4</span><span class="sxs-lookup"><span data-stu-id="a573a-848">4</span></span>

<span data-ttu-id="a573a-849">5</span><span class="sxs-lookup"><span data-stu-id="a573a-849">5</span></span>

<span data-ttu-id="a573a-850">6</span><span class="sxs-lookup"><span data-stu-id="a573a-850">6</span></span>

<span data-ttu-id="a573a-851">7</span><span class="sxs-lookup"><span data-stu-id="a573a-851">7</span></span>

<span data-ttu-id="a573a-852">8</span><span class="sxs-lookup"><span data-stu-id="a573a-852">8</span></span>

<span data-ttu-id="a573a-853">9</span><span class="sxs-lookup"><span data-stu-id="a573a-853">9</span></span>

<span data-ttu-id="a573a-854">1</span><span class="sxs-lookup"><span data-stu-id="a573a-854">1</span></span><br/> <span data-ttu-id="a573a-855">0</span><span class="sxs-lookup"><span data-stu-id="a573a-855">0</span></span><br/>

<span data-ttu-id="a573a-856">1</span><span class="sxs-lookup"><span data-stu-id="a573a-856">1</span></span>

<span data-ttu-id="a573a-857">2</span><span class="sxs-lookup"><span data-stu-id="a573a-857">2</span></span>

<span data-ttu-id="a573a-858">3</span><span class="sxs-lookup"><span data-stu-id="a573a-858">3</span></span>

<span data-ttu-id="a573a-859">4</span><span class="sxs-lookup"><span data-stu-id="a573a-859">4</span></span>

<span data-ttu-id="a573a-860">5</span><span class="sxs-lookup"><span data-stu-id="a573a-860">5</span></span>

<span data-ttu-id="a573a-861">6</span><span class="sxs-lookup"><span data-stu-id="a573a-861">6</span></span>

<span data-ttu-id="a573a-862">7</span><span class="sxs-lookup"><span data-stu-id="a573a-862">7</span></span>

<span data-ttu-id="a573a-863">8</span><span class="sxs-lookup"><span data-stu-id="a573a-863">8</span></span>

<span data-ttu-id="a573a-864">9</span><span class="sxs-lookup"><span data-stu-id="a573a-864">9</span></span>

<span data-ttu-id="a573a-865">2</span><span class="sxs-lookup"><span data-stu-id="a573a-865">2</span></span><br/> <span data-ttu-id="a573a-866">0</span><span class="sxs-lookup"><span data-stu-id="a573a-866">0</span></span><br/>

<span data-ttu-id="a573a-867">1</span><span class="sxs-lookup"><span data-stu-id="a573a-867">1</span></span>

<span data-ttu-id="a573a-868">2</span><span class="sxs-lookup"><span data-stu-id="a573a-868">2</span></span>

<span data-ttu-id="a573a-869">3</span><span class="sxs-lookup"><span data-stu-id="a573a-869">3</span></span>

<span data-ttu-id="a573a-870">4</span><span class="sxs-lookup"><span data-stu-id="a573a-870">4</span></span>

<span data-ttu-id="a573a-871">5</span><span class="sxs-lookup"><span data-stu-id="a573a-871">5</span></span>

<span data-ttu-id="a573a-872">6</span><span class="sxs-lookup"><span data-stu-id="a573a-872">6</span></span>

<span data-ttu-id="a573a-873">7</span><span class="sxs-lookup"><span data-stu-id="a573a-873">7</span></span>

<span data-ttu-id="a573a-874">8</span><span class="sxs-lookup"><span data-stu-id="a573a-874">8</span></span>

<span data-ttu-id="a573a-875">9</span><span class="sxs-lookup"><span data-stu-id="a573a-875">9</span></span>

<span data-ttu-id="a573a-876">3</span><span class="sxs-lookup"><span data-stu-id="a573a-876">3</span></span><br/> <span data-ttu-id="a573a-877">0</span><span class="sxs-lookup"><span data-stu-id="a573a-877">0</span></span><br/>

<span data-ttu-id="a573a-878">1</span><span class="sxs-lookup"><span data-stu-id="a573a-878">1</span></span>

<span data-ttu-id="a573a-879">\_гуидпропсет</span><span class="sxs-lookup"><span data-stu-id="a573a-879">\_guidPropSet</span></span>

<span data-ttu-id="a573a-880">...</span><span class="sxs-lookup"><span data-stu-id="a573a-880">...</span></span>

<span data-ttu-id="a573a-881">...</span><span class="sxs-lookup"><span data-stu-id="a573a-881">...</span></span>

<span data-ttu-id="a573a-882">...</span><span class="sxs-lookup"><span data-stu-id="a573a-882">...</span></span>

<span data-ttu-id="a573a-883">улкинд</span><span class="sxs-lookup"><span data-stu-id="a573a-883">ulKind</span></span>

<span data-ttu-id="a573a-884">прспек</span><span class="sxs-lookup"><span data-stu-id="a573a-884">PrSpec</span></span>

<span data-ttu-id="a573a-885">Имя свойства (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-885">Property name (variable)</span></span>



 

<span data-ttu-id="a573a-886">**\_ гуидпропсет**: идентификатор GUID набора свойств, которому принадлежит свойство.</span><span class="sxs-lookup"><span data-stu-id="a573a-886">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="a573a-887">**улкинд**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-887">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="a573a-888">Одно из приведенных ниже значений, которое указывает содержимое Прспек.</span><span class="sxs-lookup"><span data-stu-id="a573a-888">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="a573a-889">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-889">Value</span></span>                                            | <span data-ttu-id="a573a-890">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-890">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-891">ПРСПЕК \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="a573a-891">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="a573a-892">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-892">0x00000000</span></span><br/> | <span data-ttu-id="a573a-893">Поле Прспек указывает число символов, отличных от NULL, в поле Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-893">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="a573a-894">ПРСПЕК \_ PropID</span><span class="sxs-lookup"><span data-stu-id="a573a-894">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="a573a-895">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-895">0x00000001</span></span><br/>  | <span data-ttu-id="a573a-896">В поле Прспек указывается идентификатор свойства (PROPID).</span><span class="sxs-lookup"><span data-stu-id="a573a-896">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="a573a-897">**Прспек**: 32-битовое целое число без знака, равное значению, указанному в поле улкинд.</span><span class="sxs-lookup"><span data-stu-id="a573a-897">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="a573a-898">**Имя свойства**: Если улкинд имеет значение прспек \_ PropID, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-898">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="a573a-899">Если для Улкинд задано значение ПРСПЕК \_ LPWSTR, то в этом поле должен содержаться массив, не учитывающий регистр, из прспек символов Юникода, отличных от NULL, содержащий имя свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-899">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="a573a-900">2.2.1.3 Кконтентрестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-900">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="a573a-901">Структура Кконтентрестриктион содержит строку, соответствующую свойству в кэше свойств.</span><span class="sxs-lookup"><span data-stu-id="a573a-901">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="a573a-902">0</span><span class="sxs-lookup"><span data-stu-id="a573a-902">0</span></span>

<span data-ttu-id="a573a-903">1</span><span class="sxs-lookup"><span data-stu-id="a573a-903">1</span></span>

<span data-ttu-id="a573a-904">2</span><span class="sxs-lookup"><span data-stu-id="a573a-904">2</span></span>

<span data-ttu-id="a573a-905">3</span><span class="sxs-lookup"><span data-stu-id="a573a-905">3</span></span>

<span data-ttu-id="a573a-906">4</span><span class="sxs-lookup"><span data-stu-id="a573a-906">4</span></span>

<span data-ttu-id="a573a-907">5</span><span class="sxs-lookup"><span data-stu-id="a573a-907">5</span></span>

<span data-ttu-id="a573a-908">6</span><span class="sxs-lookup"><span data-stu-id="a573a-908">6</span></span>

<span data-ttu-id="a573a-909">7</span><span class="sxs-lookup"><span data-stu-id="a573a-909">7</span></span>

<span data-ttu-id="a573a-910">8</span><span class="sxs-lookup"><span data-stu-id="a573a-910">8</span></span>

<span data-ttu-id="a573a-911">9</span><span class="sxs-lookup"><span data-stu-id="a573a-911">9</span></span>

<span data-ttu-id="a573a-912">1</span><span class="sxs-lookup"><span data-stu-id="a573a-912">1</span></span><br/> <span data-ttu-id="a573a-913">0</span><span class="sxs-lookup"><span data-stu-id="a573a-913">0</span></span><br/>

<span data-ttu-id="a573a-914">1</span><span class="sxs-lookup"><span data-stu-id="a573a-914">1</span></span>

<span data-ttu-id="a573a-915">2</span><span class="sxs-lookup"><span data-stu-id="a573a-915">2</span></span>

<span data-ttu-id="a573a-916">3</span><span class="sxs-lookup"><span data-stu-id="a573a-916">3</span></span>

<span data-ttu-id="a573a-917">4</span><span class="sxs-lookup"><span data-stu-id="a573a-917">4</span></span>

<span data-ttu-id="a573a-918">5</span><span class="sxs-lookup"><span data-stu-id="a573a-918">5</span></span>

<span data-ttu-id="a573a-919">6</span><span class="sxs-lookup"><span data-stu-id="a573a-919">6</span></span>

<span data-ttu-id="a573a-920">7</span><span class="sxs-lookup"><span data-stu-id="a573a-920">7</span></span>

<span data-ttu-id="a573a-921">8</span><span class="sxs-lookup"><span data-stu-id="a573a-921">8</span></span>

<span data-ttu-id="a573a-922">9</span><span class="sxs-lookup"><span data-stu-id="a573a-922">9</span></span>

<span data-ttu-id="a573a-923">2</span><span class="sxs-lookup"><span data-stu-id="a573a-923">2</span></span><br/> <span data-ttu-id="a573a-924">0</span><span class="sxs-lookup"><span data-stu-id="a573a-924">0</span></span><br/>

<span data-ttu-id="a573a-925">1</span><span class="sxs-lookup"><span data-stu-id="a573a-925">1</span></span>

<span data-ttu-id="a573a-926">2</span><span class="sxs-lookup"><span data-stu-id="a573a-926">2</span></span>

<span data-ttu-id="a573a-927">3</span><span class="sxs-lookup"><span data-stu-id="a573a-927">3</span></span>

<span data-ttu-id="a573a-928">4</span><span class="sxs-lookup"><span data-stu-id="a573a-928">4</span></span>

<span data-ttu-id="a573a-929">5</span><span class="sxs-lookup"><span data-stu-id="a573a-929">5</span></span>

<span data-ttu-id="a573a-930">6</span><span class="sxs-lookup"><span data-stu-id="a573a-930">6</span></span>

<span data-ttu-id="a573a-931">7</span><span class="sxs-lookup"><span data-stu-id="a573a-931">7</span></span>

<span data-ttu-id="a573a-932">8</span><span class="sxs-lookup"><span data-stu-id="a573a-932">8</span></span>

<span data-ttu-id="a573a-933">9</span><span class="sxs-lookup"><span data-stu-id="a573a-933">9</span></span>

<span data-ttu-id="a573a-934">3</span><span class="sxs-lookup"><span data-stu-id="a573a-934">3</span></span><br/> <span data-ttu-id="a573a-935">0</span><span class="sxs-lookup"><span data-stu-id="a573a-935">0</span></span><br/>

<span data-ttu-id="a573a-936">1</span><span class="sxs-lookup"><span data-stu-id="a573a-936">1</span></span>

<span data-ttu-id="a573a-937">\_Свойство (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-937">\_Property (variable)</span></span>

<span data-ttu-id="a573a-938">...</span><span class="sxs-lookup"><span data-stu-id="a573a-938">...</span></span>

<span data-ttu-id="a573a-939">Padding1 (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-939">Padding1 (variable)</span></span>

<span data-ttu-id="a573a-940">Копия</span><span class="sxs-lookup"><span data-stu-id="a573a-940">Cc</span></span>

<span data-ttu-id="a573a-941">\_Пвксфрасе (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-941">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="a573a-942">...</span><span class="sxs-lookup"><span data-stu-id="a573a-942">...</span></span>

<span data-ttu-id="a573a-943">Padding2 (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-943">Padding2 (variable)</span></span>

<span data-ttu-id="a573a-944">lcid</span><span class="sxs-lookup"><span data-stu-id="a573a-944">lcid</span></span>

<span data-ttu-id="a573a-945">\_улженератемесод</span><span class="sxs-lookup"><span data-stu-id="a573a-945">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="a573a-946">**\_ Свойство**: структура кфуллпропспек, как указано в разделе 2.2.1.2.</span><span class="sxs-lookup"><span data-stu-id="a573a-946">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="a573a-947">Это поле обозначает свойство, для которого необходимо выполнить операцию сопоставления.</span><span class="sxs-lookup"><span data-stu-id="a573a-947">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="a573a-948">**Padding1**: это поле должно иметь длину от 0 до 3 байт.</span><span class="sxs-lookup"><span data-stu-id="a573a-948">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="a573a-949">Длина этого поля должна быть такой, что следующее поле начинается со смещения, кратного 4 байтам от начала сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="a573a-949">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="a573a-950">Если это поле (т. е. Длина ненулевой), то значение, которое он содержит, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="a573a-950">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="a573a-951">Содержимое этого поля должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-951">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="a573a-952">**CC**: 32-битовое целое число без знака, указывающее количество символов в \_ поле пвксфрасе.</span><span class="sxs-lookup"><span data-stu-id="a573a-952">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="a573a-953">**\_ пвксфрасе**: строка Юникода, не заканчивающаяся нулем, представляющая слово или фразу для сопоставления со свойством.</span><span class="sxs-lookup"><span data-stu-id="a573a-953">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="a573a-954">Это поле не должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="a573a-954">This field MUST NOT be empty.</span></span> <span data-ttu-id="a573a-955">Поле "копия" содержит длину строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-955">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="a573a-956">**Padding2**: это поле должно иметь длину от 0 до 3 байт.</span><span class="sxs-lookup"><span data-stu-id="a573a-956">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="a573a-957">Длина этого поля должна быть такой, что следующее поле начинается со смещения, кратного 4 байтам от начала сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="a573a-957">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="a573a-958">Если это поле (т. е. Длина ненулевой), то значение, которое он содержит, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="a573a-958">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="a573a-959">Содержимое этого поля должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-959">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="a573a-960">**LCID**: 32-разрядное целое число без знака, указывающее языковой стандарт \_ пвксфрасе, как указано в \[ приложении MS-GPSI \] A.</span><span class="sxs-lookup"><span data-stu-id="a573a-960">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="a573a-961">**\_ улженератемесод**: 32-битовое целое число без знака, определяющее метод, используемый при создании альтернативных форм Word</span><span class="sxs-lookup"><span data-stu-id="a573a-961">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="a573a-962">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-962">Value</span></span>                                                       | <span data-ttu-id="a573a-963">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-963">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-964">СОЗДАТЬ \_ \_ точный метод</span><span class="sxs-lookup"><span data-stu-id="a573a-964">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="a573a-965">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-965">0x00000000</span></span><br/>    | <span data-ttu-id="a573a-966">Точное соответствие.</span><span class="sxs-lookup"><span data-stu-id="a573a-966">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a573a-967">СОЗДАТЬ \_ \_ префикс метода</span><span class="sxs-lookup"><span data-stu-id="a573a-967">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="a573a-968">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-968">0x00000001</span></span> <br/>  | <span data-ttu-id="a573a-969">Совпадение префикса.</span><span class="sxs-lookup"><span data-stu-id="a573a-969">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="a573a-970">СОЗДАТЬ \_ метод \_ инфлект</span><span class="sxs-lookup"><span data-stu-id="a573a-970">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="a573a-971">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-971">0x00000002</span></span><br/> | <span data-ttu-id="a573a-972">Соответствует Перегибам слова.</span><span class="sxs-lookup"><span data-stu-id="a573a-972">Matches inflections of a word.</span></span> <span data-ttu-id="a573a-973">Перегиб слова — это вариант корневого слова в той же части речи, который был изменен в соответствии с лингвистическими правилами данного языка.</span><span class="sxs-lookup"><span data-stu-id="a573a-973">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="a573a-974">Например, в английской версии глагола "дорожки" включает "дорожки", "купание", "Swimming" и "свам".</span><span class="sxs-lookup"><span data-stu-id="a573a-974">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="a573a-975">2.2.1.4 Ккэй</span><span class="sxs-lookup"><span data-stu-id="a573a-975">2.2.1.4 CKey</span></span>

<span data-ttu-id="a573a-976">Структура Ккэй содержит значение свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-976">The CKey structure contains a property value.</span></span>



<span data-ttu-id="a573a-977">0</span><span class="sxs-lookup"><span data-stu-id="a573a-977">0</span></span>

<span data-ttu-id="a573a-978">1</span><span class="sxs-lookup"><span data-stu-id="a573a-978">1</span></span>

<span data-ttu-id="a573a-979">2</span><span class="sxs-lookup"><span data-stu-id="a573a-979">2</span></span>

<span data-ttu-id="a573a-980">3</span><span class="sxs-lookup"><span data-stu-id="a573a-980">3</span></span>

<span data-ttu-id="a573a-981">4</span><span class="sxs-lookup"><span data-stu-id="a573a-981">4</span></span>

<span data-ttu-id="a573a-982">5</span><span class="sxs-lookup"><span data-stu-id="a573a-982">5</span></span>

<span data-ttu-id="a573a-983">6</span><span class="sxs-lookup"><span data-stu-id="a573a-983">6</span></span>

<span data-ttu-id="a573a-984">7</span><span class="sxs-lookup"><span data-stu-id="a573a-984">7</span></span>

<span data-ttu-id="a573a-985">8</span><span class="sxs-lookup"><span data-stu-id="a573a-985">8</span></span>

<span data-ttu-id="a573a-986">9</span><span class="sxs-lookup"><span data-stu-id="a573a-986">9</span></span>

<span data-ttu-id="a573a-987">1</span><span class="sxs-lookup"><span data-stu-id="a573a-987">1</span></span><br/> <span data-ttu-id="a573a-988">0</span><span class="sxs-lookup"><span data-stu-id="a573a-988">0</span></span><br/>

<span data-ttu-id="a573a-989">1</span><span class="sxs-lookup"><span data-stu-id="a573a-989">1</span></span>

<span data-ttu-id="a573a-990">2</span><span class="sxs-lookup"><span data-stu-id="a573a-990">2</span></span>

<span data-ttu-id="a573a-991">3</span><span class="sxs-lookup"><span data-stu-id="a573a-991">3</span></span>

<span data-ttu-id="a573a-992">4</span><span class="sxs-lookup"><span data-stu-id="a573a-992">4</span></span>

<span data-ttu-id="a573a-993">5</span><span class="sxs-lookup"><span data-stu-id="a573a-993">5</span></span>

<span data-ttu-id="a573a-994">6</span><span class="sxs-lookup"><span data-stu-id="a573a-994">6</span></span>

<span data-ttu-id="a573a-995">7</span><span class="sxs-lookup"><span data-stu-id="a573a-995">7</span></span>

<span data-ttu-id="a573a-996">8</span><span class="sxs-lookup"><span data-stu-id="a573a-996">8</span></span>

<span data-ttu-id="a573a-997">9</span><span class="sxs-lookup"><span data-stu-id="a573a-997">9</span></span>

<span data-ttu-id="a573a-998">2</span><span class="sxs-lookup"><span data-stu-id="a573a-998">2</span></span><br/> <span data-ttu-id="a573a-999">0</span><span class="sxs-lookup"><span data-stu-id="a573a-999">0</span></span><br/>

<span data-ttu-id="a573a-1000">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1000">1</span></span>

<span data-ttu-id="a573a-1001">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1001">2</span></span>

<span data-ttu-id="a573a-1002">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1002">3</span></span>

<span data-ttu-id="a573a-1003">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1003">4</span></span>

<span data-ttu-id="a573a-1004">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1004">5</span></span>

<span data-ttu-id="a573a-1005">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1005">6</span></span>

<span data-ttu-id="a573a-1006">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1006">7</span></span>

<span data-ttu-id="a573a-1007">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1007">8</span></span>

<span data-ttu-id="a573a-1008">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1008">9</span></span>

<span data-ttu-id="a573a-1009">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1009">3</span></span><br/> <span data-ttu-id="a573a-1010">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1010">0</span></span><br/>

<span data-ttu-id="a573a-1011">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1011">1</span></span>

<span data-ttu-id="a573a-1012">PROPID</span><span class="sxs-lookup"><span data-stu-id="a573a-1012">PROPID</span></span>

<span data-ttu-id="a573a-1013">CB</span><span class="sxs-lookup"><span data-stu-id="a573a-1013">Cb</span></span>

<span data-ttu-id="a573a-1014">buf (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1014">buf (variable)</span></span>



 

<span data-ttu-id="a573a-1015">**PropID**: 32-битовое целое число без знака, представляющее идентификатор свойства, как описано в разделе 1.8.1.</span><span class="sxs-lookup"><span data-stu-id="a573a-1015">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="a573a-1016">Хорошо известные значения:</span><span class="sxs-lookup"><span data-stu-id="a573a-1016">Well-known values are:</span></span>



| <span data-ttu-id="a573a-1017">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1017">Value</span></span>      | <span data-ttu-id="a573a-1018">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1018">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="a573a-1019">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="a573a-1019">0xFFFFFFFF</span></span> | <span data-ttu-id="a573a-1020">Представляет недопустимый идентификатор свойства и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-1020">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="a573a-1021">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="a573a-1021">0xFFFFFFFE</span></span> | <span data-ttu-id="a573a-1022">Представляет недопустимый идентификатор свойства и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-1022">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="a573a-1023">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-1023">0x00000000</span></span> | <span data-ttu-id="a573a-1024">Представляет идентификатор любого свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-1024">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="a573a-1025">**CB**: 32-разрядное целое число без знака, содержащее длину buf в байтах.</span><span class="sxs-lookup"><span data-stu-id="a573a-1025">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="a573a-1026">**buf**: последовательность байтов, представляющих значение свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-1026">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="a573a-1027">2.2.1.5 Цинтерналпропертирестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-1027">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="a573a-1028">Структура Цинтерналпропертирестриктион содержит значение свойства для сопоставления с операцией.</span><span class="sxs-lookup"><span data-stu-id="a573a-1028">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="a573a-1029">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1029">0</span></span>

<span data-ttu-id="a573a-1030">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1030">1</span></span>

<span data-ttu-id="a573a-1031">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1031">2</span></span>

<span data-ttu-id="a573a-1032">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1032">3</span></span>

<span data-ttu-id="a573a-1033">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1033">4</span></span>

<span data-ttu-id="a573a-1034">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1034">5</span></span>

<span data-ttu-id="a573a-1035">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1035">6</span></span>

<span data-ttu-id="a573a-1036">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1036">7</span></span>

<span data-ttu-id="a573a-1037">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1037">8</span></span>

<span data-ttu-id="a573a-1038">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1038">9</span></span>

<span data-ttu-id="a573a-1039">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1039">1</span></span><br/> <span data-ttu-id="a573a-1040">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1040">0</span></span><br/>

<span data-ttu-id="a573a-1041">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1041">1</span></span>

<span data-ttu-id="a573a-1042">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1042">2</span></span>

<span data-ttu-id="a573a-1043">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1043">3</span></span>

<span data-ttu-id="a573a-1044">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1044">4</span></span>

<span data-ttu-id="a573a-1045">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1045">5</span></span>

<span data-ttu-id="a573a-1046">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1046">6</span></span>

<span data-ttu-id="a573a-1047">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1047">7</span></span>

<span data-ttu-id="a573a-1048">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1048">8</span></span>

<span data-ttu-id="a573a-1049">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1049">9</span></span>

<span data-ttu-id="a573a-1050">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1050">2</span></span><br/> <span data-ttu-id="a573a-1051">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1051">0</span></span><br/>

<span data-ttu-id="a573a-1052">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1052">1</span></span>

<span data-ttu-id="a573a-1053">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1053">2</span></span>

<span data-ttu-id="a573a-1054">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1054">3</span></span>

<span data-ttu-id="a573a-1055">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1055">4</span></span>

<span data-ttu-id="a573a-1056">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1056">5</span></span>

<span data-ttu-id="a573a-1057">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1057">6</span></span>

<span data-ttu-id="a573a-1058">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1058">7</span></span>

<span data-ttu-id="a573a-1059">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1059">8</span></span>

<span data-ttu-id="a573a-1060">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1060">9</span></span>

<span data-ttu-id="a573a-1061">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1061">3</span></span><br/> <span data-ttu-id="a573a-1062">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1062">0</span></span><br/>

<span data-ttu-id="a573a-1063">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1063">1</span></span>

<span data-ttu-id="a573a-1064">\_RelOp</span><span class="sxs-lookup"><span data-stu-id="a573a-1064">\_relop</span></span>

<span data-ttu-id="a573a-1065">\_PID</span><span class="sxs-lookup"><span data-stu-id="a573a-1065">\_pid</span></span>

<span data-ttu-id="a573a-1066">\_првал (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1066">\_prval (variable)</span></span>

<span data-ttu-id="a573a-1067">рестриктионпресент</span><span class="sxs-lookup"><span data-stu-id="a573a-1067">restrictionPresent</span></span>

<span data-ttu-id="a573a-1068">Некстрестриктион (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1068">nextRestriction (variable)</span></span>



 

<span data-ttu-id="a573a-1069">**\_ relop**: 32-разрядное целое число, указывающее отношение для выполнения со свойством.</span><span class="sxs-lookup"><span data-stu-id="a573a-1069">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="a573a-1070">ДОЛЖНО иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a573a-1070">MUST be one of the following values:</span></span>



| <span data-ttu-id="a573a-1071">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1071">Value</span></span>                 | <span data-ttu-id="a573a-1072">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1072">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-1073">ПРЛТ 0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-1073">PRLT 0x00000000</span></span>       | <span data-ttu-id="a573a-1074">Сравнение "меньше чем".</span><span class="sxs-lookup"><span data-stu-id="a573a-1074">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="a573a-1075">ПРЛЕ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-1075">PRLE 0x00000001</span></span>       | <span data-ttu-id="a573a-1076">Сравнение "меньше или равно".</span><span class="sxs-lookup"><span data-stu-id="a573a-1076">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="a573a-1077">ПРГТ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-1077">PRGT 0x00000002</span></span>       | <span data-ttu-id="a573a-1078">Сравнение "больше чем".</span><span class="sxs-lookup"><span data-stu-id="a573a-1078">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="a573a-1079">ПРЖЕ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-1079">PRGE 0x00000003</span></span>       | <span data-ttu-id="a573a-1080">Сравнение "больше или равно".</span><span class="sxs-lookup"><span data-stu-id="a573a-1080">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="a573a-1081">ПРЕК 0x00000004</span><span class="sxs-lookup"><span data-stu-id="a573a-1081">PREQ 0x00000004</span></span>       | <span data-ttu-id="a573a-1082">Сравнение на равенство.</span><span class="sxs-lookup"><span data-stu-id="a573a-1082">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="a573a-1083">ПРНЕ 0x00000005</span><span class="sxs-lookup"><span data-stu-id="a573a-1083">PRNE 0x00000005</span></span>       | <span data-ttu-id="a573a-1084">Сравнение «не равно».</span><span class="sxs-lookup"><span data-stu-id="a573a-1084">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="a573a-1085">ПРРЕ 0x00000006</span><span class="sxs-lookup"><span data-stu-id="a573a-1085">PRRE 0x00000006</span></span>       | <span data-ttu-id="a573a-1086">Сравнение регулярных выражений.</span><span class="sxs-lookup"><span data-stu-id="a573a-1086">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="a573a-1087">Праллбитс 0x00000007</span><span class="sxs-lookup"><span data-stu-id="a573a-1087">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="a573a-1088">Побитовое и, возвращающее правый операнд.</span><span class="sxs-lookup"><span data-stu-id="a573a-1088">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="a573a-1089">Прсомебитс 0x00000008</span><span class="sxs-lookup"><span data-stu-id="a573a-1089">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="a573a-1090">Побитовое и, возвращающее ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a573a-1090">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="a573a-1091">Пралл 0x00000100</span><span class="sxs-lookup"><span data-stu-id="a573a-1091">PRAll 0x00000100</span></span>      | <span data-ttu-id="a573a-1092">Операция должна быть выполнена над столбцом набора строк и имеет значение true, если операция выполняется для всех строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-1092">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="a573a-1093">ПРАНИ 0x00000200</span><span class="sxs-lookup"><span data-stu-id="a573a-1093">PRAny 0x00000200</span></span>      | <span data-ttu-id="a573a-1094">Операция должна быть выполнена над столбцом набора строк, и имеет значение true, если операция выполняется для любой строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-1094">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="a573a-1095">**\_ pid**: 32-разрядное целое число без знака, представляющее идентификатор свойства (см. раздел PropID в разделе 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="a573a-1095">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="a573a-1096">**\_ Првал**: кбасесторажевариант, содержащий значение, которое необходимо связать со свойством.</span><span class="sxs-lookup"><span data-stu-id="a573a-1096">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="a573a-1097">**рестриктионпресент**: значение байта, указывающее, имеется ли поле некстрестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-1097">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="a573a-1098">НЕОБХОДИМО задать значение 0x00 или 0x01.</span><span class="sxs-lookup"><span data-stu-id="a573a-1098">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="a573a-1099">Если задано значение 0x01, Рестриктионпресент указывает на наличие поля Некстрестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-1099">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="a573a-1100">Если задано значение 0x00, Рестриктионпресент указывает, что поле Некстрестриктион отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a573a-1100">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="a573a-1101">**некстрестриктион**: структура крестриктион, как указано в разделе 2.2.1.16, с указанием дополнительного ограничения.</span><span class="sxs-lookup"><span data-stu-id="a573a-1101">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="a573a-1102">2.2.1.6 Кнатлангуажерестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-1102">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="a573a-1103">Структура Кнатлангуажерестриктион содержит запрос на **естественном языке** , соответствующий свойству.</span><span class="sxs-lookup"><span data-stu-id="a573a-1103">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="a573a-1104">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1104">0</span></span>

<span data-ttu-id="a573a-1105">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1105">1</span></span>

<span data-ttu-id="a573a-1106">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1106">2</span></span>

<span data-ttu-id="a573a-1107">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1107">3</span></span>

<span data-ttu-id="a573a-1108">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1108">4</span></span>

<span data-ttu-id="a573a-1109">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1109">5</span></span>

<span data-ttu-id="a573a-1110">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1110">6</span></span>

<span data-ttu-id="a573a-1111">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1111">7</span></span>

<span data-ttu-id="a573a-1112">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1112">8</span></span>

<span data-ttu-id="a573a-1113">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1113">9</span></span>

<span data-ttu-id="a573a-1114">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1114">1</span></span><br/> <span data-ttu-id="a573a-1115">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1115">0</span></span><br/>

<span data-ttu-id="a573a-1116">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1116">1</span></span>

<span data-ttu-id="a573a-1117">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1117">2</span></span>

<span data-ttu-id="a573a-1118">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1118">3</span></span>

<span data-ttu-id="a573a-1119">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1119">4</span></span>

<span data-ttu-id="a573a-1120">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1120">5</span></span>

<span data-ttu-id="a573a-1121">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1121">6</span></span>

<span data-ttu-id="a573a-1122">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1122">7</span></span>

<span data-ttu-id="a573a-1123">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1123">8</span></span>

<span data-ttu-id="a573a-1124">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1124">9</span></span>

<span data-ttu-id="a573a-1125">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1125">2</span></span><br/> <span data-ttu-id="a573a-1126">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1126">0</span></span><br/>

<span data-ttu-id="a573a-1127">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1127">1</span></span>

<span data-ttu-id="a573a-1128">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1128">2</span></span>

<span data-ttu-id="a573a-1129">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1129">3</span></span>

<span data-ttu-id="a573a-1130">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1130">4</span></span>

<span data-ttu-id="a573a-1131">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1131">5</span></span>

<span data-ttu-id="a573a-1132">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1132">6</span></span>

<span data-ttu-id="a573a-1133">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1133">7</span></span>

<span data-ttu-id="a573a-1134">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1134">8</span></span>

<span data-ttu-id="a573a-1135">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1135">9</span></span>

<span data-ttu-id="a573a-1136">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1136">3</span></span><br/> <span data-ttu-id="a573a-1137">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1137">0</span></span><br/>

<span data-ttu-id="a573a-1138">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1138">1</span></span>

<span data-ttu-id="a573a-1139">\_Свойство (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1139">\_Property (variable)</span></span>

<span data-ttu-id="a573a-1140">...</span><span class="sxs-lookup"><span data-stu-id="a573a-1140">...</span></span>

<span data-ttu-id="a573a-1141">\_заполнение \_ CC (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1141">\_padding\_cc (variable)</span></span>

<span data-ttu-id="a573a-1142">Копия</span><span class="sxs-lookup"><span data-stu-id="a573a-1142">Cc</span></span>

<span data-ttu-id="a573a-1143">\_Пвксфрасе (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1143">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="a573a-1144">...</span><span class="sxs-lookup"><span data-stu-id="a573a-1144">...</span></span>

<span data-ttu-id="a573a-1145">\_LCID заполнения \_ (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1145">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="a573a-1146">Код языка</span><span class="sxs-lookup"><span data-stu-id="a573a-1146">Lcid</span></span>



 

<span data-ttu-id="a573a-1147">**\_ Свойство**: структура кфуллпропспек, как указано в разделе 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="a573a-1147">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="a573a-1148">Это поле обозначает свойство, для которого необходимо выполнить операцию сопоставления.</span><span class="sxs-lookup"><span data-stu-id="a573a-1148">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="a573a-1149">**\_ Заполнение \_ CC**: это поле должно иметь длину от 0 до 3 байт.</span><span class="sxs-lookup"><span data-stu-id="a573a-1149">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="a573a-1150">Длина этого поля должна быть такой, что следующее поле начинается со смещения, кратного 4 байтам от начала сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="a573a-1150">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="a573a-1151">Если это поле (т. е. Длина ненулевой), то значение, которое он содержит, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="a573a-1151">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="a573a-1152">Содержимое этого поля должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-1152">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="a573a-1153">**CC**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-1153">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="a573a-1154">Число символов в \_ поле пвксфрасе.</span><span class="sxs-lookup"><span data-stu-id="a573a-1154">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="a573a-1155">**\_ пвксфрасе**: строка Юникода, не заканчивающаяся нулем, представляющая слово или фразу для сопоставления со свойством.</span><span class="sxs-lookup"><span data-stu-id="a573a-1155">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="a573a-1156">НЕ должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="a573a-1156">MUST NOT be empty.</span></span> <span data-ttu-id="a573a-1157">Поле "копия" содержит длину строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-1157">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="a573a-1158">**\_ \_ код языка заполнения**: это поле должно иметь длину от 0 до 3 байт.</span><span class="sxs-lookup"><span data-stu-id="a573a-1158">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="a573a-1159">Длина этого поля должна быть такой, что следующее поле начинается со смещения, кратного 4 байтам от начала сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="a573a-1159">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="a573a-1160">Если это поле (т. е. Длина ненулевой), то значение, которое он содержит, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="a573a-1160">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="a573a-1161">Содержимое этого поля должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-1161">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="a573a-1162">**LCID**: 32-разрядное целое число без знака, указывающее языковой стандарт \_ пвксфрасе, как указано в \[ приложении MS-GPSI \] A.</span><span class="sxs-lookup"><span data-stu-id="a573a-1162">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="a573a-1163">2.2.1.7 Кнодерестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-1163">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="a573a-1164">Структура Кнодерестриктион содержит массив узлов **дерева команд** , которые указывают ограничения для запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-1164">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="a573a-1165">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1165">0</span></span>

<span data-ttu-id="a573a-1166">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1166">1</span></span>

<span data-ttu-id="a573a-1167">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1167">2</span></span>

<span data-ttu-id="a573a-1168">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1168">3</span></span>

<span data-ttu-id="a573a-1169">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1169">4</span></span>

<span data-ttu-id="a573a-1170">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1170">5</span></span>

<span data-ttu-id="a573a-1171">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1171">6</span></span>

<span data-ttu-id="a573a-1172">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1172">7</span></span>

<span data-ttu-id="a573a-1173">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1173">8</span></span>

<span data-ttu-id="a573a-1174">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1174">9</span></span>

<span data-ttu-id="a573a-1175">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1175">1</span></span><br/> <span data-ttu-id="a573a-1176">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1176">0</span></span><br/>

<span data-ttu-id="a573a-1177">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1177">1</span></span>

<span data-ttu-id="a573a-1178">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1178">2</span></span>

<span data-ttu-id="a573a-1179">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1179">3</span></span>

<span data-ttu-id="a573a-1180">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1180">4</span></span>

<span data-ttu-id="a573a-1181">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1181">5</span></span>

<span data-ttu-id="a573a-1182">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1182">6</span></span>

<span data-ttu-id="a573a-1183">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1183">7</span></span>

<span data-ttu-id="a573a-1184">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1184">8</span></span>

<span data-ttu-id="a573a-1185">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1185">9</span></span>

<span data-ttu-id="a573a-1186">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1186">2</span></span><br/> <span data-ttu-id="a573a-1187">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1187">0</span></span><br/>

<span data-ttu-id="a573a-1188">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1188">1</span></span>

<span data-ttu-id="a573a-1189">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1189">2</span></span>

<span data-ttu-id="a573a-1190">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1190">3</span></span>

<span data-ttu-id="a573a-1191">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1191">4</span></span>

<span data-ttu-id="a573a-1192">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1192">5</span></span>

<span data-ttu-id="a573a-1193">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1193">6</span></span>

<span data-ttu-id="a573a-1194">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1194">7</span></span>

<span data-ttu-id="a573a-1195">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1195">8</span></span>

<span data-ttu-id="a573a-1196">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1196">9</span></span>

<span data-ttu-id="a573a-1197">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1197">3</span></span><br/> <span data-ttu-id="a573a-1198">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1198">0</span></span><br/>

<span data-ttu-id="a573a-1199">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1199">1</span></span>

<span data-ttu-id="a573a-1200">\_кноде</span><span class="sxs-lookup"><span data-stu-id="a573a-1200">\_cNode</span></span>

<span data-ttu-id="a573a-1201">\_Паноде (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1201">\_paNode (variable)</span></span>



 

<span data-ttu-id="a573a-1202">**\_ кноде**: 32-разрядное целое число без знака, указывающее количество структур крестриктион, содержащихся в \_ поле паноде.</span><span class="sxs-lookup"><span data-stu-id="a573a-1202">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="a573a-1203">**\_ паноде**: массив структур крестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-1203">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="a573a-1204">Структуры в массиве должны быть разделены от 0 до 3 байтов, так что каждая структура начинается со смещения, кратного 4 байтам от начала сообщения, содержащего этот массив.</span><span class="sxs-lookup"><span data-stu-id="a573a-1204">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="a573a-1205">Если заданы байты заполнения, то значение, которое они содержат, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="a573a-1205">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="a573a-1206">Содержимое байтов заполнения должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-1206">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="a573a-1207">2.2.1.8 Коккрестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-1207">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="a573a-1208">Структура Коккрестриктион содержит расположение слова в фразе.</span><span class="sxs-lookup"><span data-stu-id="a573a-1208">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="a573a-1209">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1209">0</span></span>

<span data-ttu-id="a573a-1210">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1210">1</span></span>

<span data-ttu-id="a573a-1211">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1211">2</span></span>

<span data-ttu-id="a573a-1212">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1212">3</span></span>

<span data-ttu-id="a573a-1213">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1213">4</span></span>

<span data-ttu-id="a573a-1214">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1214">5</span></span>

<span data-ttu-id="a573a-1215">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1215">6</span></span>

<span data-ttu-id="a573a-1216">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1216">7</span></span>

<span data-ttu-id="a573a-1217">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1217">8</span></span>

<span data-ttu-id="a573a-1218">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1218">9</span></span>

<span data-ttu-id="a573a-1219">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1219">1</span></span><br/> <span data-ttu-id="a573a-1220">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1220">0</span></span><br/>

<span data-ttu-id="a573a-1221">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1221">1</span></span>

<span data-ttu-id="a573a-1222">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1222">2</span></span>

<span data-ttu-id="a573a-1223">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1223">3</span></span>

<span data-ttu-id="a573a-1224">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1224">4</span></span>

<span data-ttu-id="a573a-1225">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1225">5</span></span>

<span data-ttu-id="a573a-1226">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1226">6</span></span>

<span data-ttu-id="a573a-1227">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1227">7</span></span>

<span data-ttu-id="a573a-1228">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1228">8</span></span>

<span data-ttu-id="a573a-1229">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1229">9</span></span>

<span data-ttu-id="a573a-1230">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1230">2</span></span><br/> <span data-ttu-id="a573a-1231">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1231">0</span></span><br/>

<span data-ttu-id="a573a-1232">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1232">1</span></span>

<span data-ttu-id="a573a-1233">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1233">2</span></span>

<span data-ttu-id="a573a-1234">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1234">3</span></span>

<span data-ttu-id="a573a-1235">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1235">4</span></span>

<span data-ttu-id="a573a-1236">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1236">5</span></span>

<span data-ttu-id="a573a-1237">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1237">6</span></span>

<span data-ttu-id="a573a-1238">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1238">7</span></span>

<span data-ttu-id="a573a-1239">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1239">8</span></span>

<span data-ttu-id="a573a-1240">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1240">9</span></span>

<span data-ttu-id="a573a-1241">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1241">3</span></span><br/> <span data-ttu-id="a573a-1242">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1242">0</span></span><br/>

<span data-ttu-id="a573a-1243">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1243">1</span></span>

<span data-ttu-id="a573a-1244">\_OCC</span><span class="sxs-lookup"><span data-stu-id="a573a-1244">\_occ</span></span>

<span data-ttu-id="a573a-1245">\_кпревноисевордс</span><span class="sxs-lookup"><span data-stu-id="a573a-1245">\_cPrevNoiseWords</span></span>

<span data-ttu-id="a573a-1246">\_кнекстноисевордс</span><span class="sxs-lookup"><span data-stu-id="a573a-1246">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="a573a-1247">**\_ occ**: 32-разрядное целое число без знака, указывающее смещение слова в строке запроса в единицах.</span><span class="sxs-lookup"><span data-stu-id="a573a-1247">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="a573a-1248">Слово, используемое в этой спецификации, является единицей языка в любом языковом стандарте, который несет смысл.</span><span class="sxs-lookup"><span data-stu-id="a573a-1248">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="a573a-1249">**\_ кпревноисевордс**: 32-разрядное целое число без знака, содержащее количество **пропускаемых слов** , которые происходят между этим словом и предыдущим словом в фразе.</span><span class="sxs-lookup"><span data-stu-id="a573a-1249">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="a573a-1250">**\_ кнекстноисевордс**: 32-разрядное целое число без знака, содержащее количество пропускаемых слов, произошедших между этим словом и следующим словом в фразе.</span><span class="sxs-lookup"><span data-stu-id="a573a-1250">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="a573a-1251">2.2.1.9 Кпропертирестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-1251">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="a573a-1252">Структура Кпропертирестриктион содержит значение свойства для сопоставления с операцией.</span><span class="sxs-lookup"><span data-stu-id="a573a-1252">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="a573a-1253">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1253">0</span></span>

<span data-ttu-id="a573a-1254">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1254">1</span></span>

<span data-ttu-id="a573a-1255">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1255">2</span></span>

<span data-ttu-id="a573a-1256">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1256">3</span></span>

<span data-ttu-id="a573a-1257">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1257">4</span></span>

<span data-ttu-id="a573a-1258">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1258">5</span></span>

<span data-ttu-id="a573a-1259">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1259">6</span></span>

<span data-ttu-id="a573a-1260">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1260">7</span></span>

<span data-ttu-id="a573a-1261">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1261">8</span></span>

<span data-ttu-id="a573a-1262">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1262">9</span></span>

<span data-ttu-id="a573a-1263">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1263">1</span></span><br/> <span data-ttu-id="a573a-1264">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1264">0</span></span><br/>

<span data-ttu-id="a573a-1265">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1265">1</span></span>

<span data-ttu-id="a573a-1266">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1266">2</span></span>

<span data-ttu-id="a573a-1267">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1267">3</span></span>

<span data-ttu-id="a573a-1268">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1268">4</span></span>

<span data-ttu-id="a573a-1269">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1269">5</span></span>

<span data-ttu-id="a573a-1270">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1270">6</span></span>

<span data-ttu-id="a573a-1271">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1271">7</span></span>

<span data-ttu-id="a573a-1272">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1272">8</span></span>

<span data-ttu-id="a573a-1273">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1273">9</span></span>

<span data-ttu-id="a573a-1274">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1274">2</span></span><br/> <span data-ttu-id="a573a-1275">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1275">0</span></span><br/>

<span data-ttu-id="a573a-1276">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1276">1</span></span>

<span data-ttu-id="a573a-1277">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1277">2</span></span>

<span data-ttu-id="a573a-1278">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1278">3</span></span>

<span data-ttu-id="a573a-1279">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1279">4</span></span>

<span data-ttu-id="a573a-1280">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1280">5</span></span>

<span data-ttu-id="a573a-1281">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1281">6</span></span>

<span data-ttu-id="a573a-1282">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1282">7</span></span>

<span data-ttu-id="a573a-1283">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1283">8</span></span>

<span data-ttu-id="a573a-1284">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1284">9</span></span>

<span data-ttu-id="a573a-1285">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1285">3</span></span><br/> <span data-ttu-id="a573a-1286">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1286">0</span></span><br/>

<span data-ttu-id="a573a-1287">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1287">1</span></span>

<span data-ttu-id="a573a-1288">\_RelOp</span><span class="sxs-lookup"><span data-stu-id="a573a-1288">\_relop</span></span>

<span data-ttu-id="a573a-1289">\_Свойство (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1289">\_Property (variable)</span></span>

<span data-ttu-id="a573a-1290">\_првал (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1290">\_prval (variable)</span></span>



 

<span data-ttu-id="a573a-1291">**\_ relop**: 32-битовое целое число без знака, указывающее отношение для выполнения со свойством.</span><span class="sxs-lookup"><span data-stu-id="a573a-1291">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="a573a-1292">ДОЛЖНО иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a573a-1292">MUST be one of the following values.</span></span>



| <span data-ttu-id="a573a-1293">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1293">Value</span></span>                 | <span data-ttu-id="a573a-1294">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1294">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-1295">ПРЛТ 0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-1295">PRLT 0x00000000</span></span>       | <span data-ttu-id="a573a-1296">Сравнение "меньше чем".</span><span class="sxs-lookup"><span data-stu-id="a573a-1296">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="a573a-1297">ПРЛЕ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-1297">PRLE 0x00000001</span></span>       | <span data-ttu-id="a573a-1298">Сравнение "меньше или равно".</span><span class="sxs-lookup"><span data-stu-id="a573a-1298">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="a573a-1299">ПРГТ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-1299">PRGT 0x00000002</span></span>       | <span data-ttu-id="a573a-1300">Сравнение "больше чем".</span><span class="sxs-lookup"><span data-stu-id="a573a-1300">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="a573a-1301">ПРЖЕ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-1301">PRGE 0x00000003</span></span>       | <span data-ttu-id="a573a-1302">Сравнение "больше или равно".</span><span class="sxs-lookup"><span data-stu-id="a573a-1302">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="a573a-1303">ПРЕК 0x00000004</span><span class="sxs-lookup"><span data-stu-id="a573a-1303">PREQ 0x00000004</span></span>       | <span data-ttu-id="a573a-1304">Сравнение на равенство.</span><span class="sxs-lookup"><span data-stu-id="a573a-1304">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="a573a-1305">ПРНЕ 0x00000005</span><span class="sxs-lookup"><span data-stu-id="a573a-1305">PRNE 0x00000005</span></span>       | <span data-ttu-id="a573a-1306">Сравнение «не равно».</span><span class="sxs-lookup"><span data-stu-id="a573a-1306">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="a573a-1307">ПРРЕ 0x00000006</span><span class="sxs-lookup"><span data-stu-id="a573a-1307">PRRE 0x00000006</span></span>       | <span data-ttu-id="a573a-1308">Сравнение регулярных выражений.</span><span class="sxs-lookup"><span data-stu-id="a573a-1308">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="a573a-1309">Праллбитс 0x00000007</span><span class="sxs-lookup"><span data-stu-id="a573a-1309">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="a573a-1310">Побитовое и, возвращающее правый операнд.</span><span class="sxs-lookup"><span data-stu-id="a573a-1310">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="a573a-1311">Прсомебитс 0x00000008</span><span class="sxs-lookup"><span data-stu-id="a573a-1311">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="a573a-1312">Побитовое и, возвращающее ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a573a-1312">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="a573a-1313">Пралл 0x00000100</span><span class="sxs-lookup"><span data-stu-id="a573a-1313">PRAll 0x00000100</span></span>      | <span data-ttu-id="a573a-1314">Операция должна быть выполнена над столбцом набора строк и имеет значение true, если операция выполняется для всех строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-1314">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="a573a-1315">ПРАНИ 0x00000200</span><span class="sxs-lookup"><span data-stu-id="a573a-1315">PRAny 0x00000200</span></span>      | <span data-ttu-id="a573a-1316">Операция должна быть выполнена над столбцом набора строк, и имеет значение true, если операция выполняется для любой строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-1316">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="a573a-1317">**\_ Свойство**: структура кфуллпропспек, как указано в разделе 2.2.1.2, указывающая свойство, для которого выполняется операция сопоставления.</span><span class="sxs-lookup"><span data-stu-id="a573a-1317">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="a573a-1318">**\_ првал**: структура кбасесторажевариант, как указано в разделе 2.2.1.1, содержащей значение, которое необходимо связать со свойством.</span><span class="sxs-lookup"><span data-stu-id="a573a-1318">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="a573a-1319">2.2.1.10 Кранжерестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-1319">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="a573a-1320">Структура Кранжерестриктион содержит ограничение на диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="a573a-1320">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="a573a-1321">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1321">0</span></span>

<span data-ttu-id="a573a-1322">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1322">1</span></span>

<span data-ttu-id="a573a-1323">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1323">2</span></span>

<span data-ttu-id="a573a-1324">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1324">3</span></span>

<span data-ttu-id="a573a-1325">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1325">4</span></span>

<span data-ttu-id="a573a-1326">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1326">5</span></span>

<span data-ttu-id="a573a-1327">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1327">6</span></span>

<span data-ttu-id="a573a-1328">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1328">7</span></span>

<span data-ttu-id="a573a-1329">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1329">8</span></span>

<span data-ttu-id="a573a-1330">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1330">9</span></span>

<span data-ttu-id="a573a-1331">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1331">1</span></span><br/> <span data-ttu-id="a573a-1332">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1332">0</span></span><br/>

<span data-ttu-id="a573a-1333">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1333">1</span></span>

<span data-ttu-id="a573a-1334">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1334">2</span></span>

<span data-ttu-id="a573a-1335">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1335">3</span></span>

<span data-ttu-id="a573a-1336">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1336">4</span></span>

<span data-ttu-id="a573a-1337">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1337">5</span></span>

<span data-ttu-id="a573a-1338">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1338">6</span></span>

<span data-ttu-id="a573a-1339">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1339">7</span></span>

<span data-ttu-id="a573a-1340">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1340">8</span></span>

<span data-ttu-id="a573a-1341">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1341">9</span></span>

<span data-ttu-id="a573a-1342">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1342">2</span></span><br/> <span data-ttu-id="a573a-1343">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1343">0</span></span><br/>

<span data-ttu-id="a573a-1344">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1344">1</span></span>

<span data-ttu-id="a573a-1345">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1345">2</span></span>

<span data-ttu-id="a573a-1346">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1346">3</span></span>

<span data-ttu-id="a573a-1347">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1347">4</span></span>

<span data-ttu-id="a573a-1348">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1348">5</span></span>

<span data-ttu-id="a573a-1349">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1349">6</span></span>

<span data-ttu-id="a573a-1350">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1350">7</span></span>

<span data-ttu-id="a573a-1351">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1351">8</span></span>

<span data-ttu-id="a573a-1352">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1352">9</span></span>

<span data-ttu-id="a573a-1353">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1353">3</span></span><br/> <span data-ttu-id="a573a-1354">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1354">0</span></span><br/>

<span data-ttu-id="a573a-1355">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1355">1</span></span>

<span data-ttu-id="a573a-1356">\_Кэйстарт (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1356">\_keyStart (variable)</span></span>

<span data-ttu-id="a573a-1357">\_Кэйенд (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1357">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="a573a-1358">**\_ кэйстарт**: структура ккэй, как указано в разделе 2.2.1.4, содержащей начало диапазона.</span><span class="sxs-lookup"><span data-stu-id="a573a-1358">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="a573a-1359">**\_ кэйенд**: структура ккэй, содержащая конец диапазона.</span><span class="sxs-lookup"><span data-stu-id="a573a-1359">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="a573a-1360">2.2.1.11 Кскоперестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-1360">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="a573a-1361">Структура Кскоперестриктион содержит ограничение на файлы для поиска.</span><span class="sxs-lookup"><span data-stu-id="a573a-1361">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="a573a-1362">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1362">0</span></span>

<span data-ttu-id="a573a-1363">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1363">1</span></span>

<span data-ttu-id="a573a-1364">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1364">2</span></span>

<span data-ttu-id="a573a-1365">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1365">3</span></span>

<span data-ttu-id="a573a-1366">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1366">4</span></span>

<span data-ttu-id="a573a-1367">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1367">5</span></span>

<span data-ttu-id="a573a-1368">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1368">6</span></span>

<span data-ttu-id="a573a-1369">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1369">7</span></span>

<span data-ttu-id="a573a-1370">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1370">8</span></span>

<span data-ttu-id="a573a-1371">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1371">9</span></span>

<span data-ttu-id="a573a-1372">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1372">1</span></span><br/> <span data-ttu-id="a573a-1373">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1373">0</span></span><br/>

<span data-ttu-id="a573a-1374">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1374">1</span></span>

<span data-ttu-id="a573a-1375">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1375">2</span></span>

<span data-ttu-id="a573a-1376">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1376">3</span></span>

<span data-ttu-id="a573a-1377">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1377">4</span></span>

<span data-ttu-id="a573a-1378">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1378">5</span></span>

<span data-ttu-id="a573a-1379">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1379">6</span></span>

<span data-ttu-id="a573a-1380">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1380">7</span></span>

<span data-ttu-id="a573a-1381">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1381">8</span></span>

<span data-ttu-id="a573a-1382">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1382">9</span></span>

<span data-ttu-id="a573a-1383">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1383">2</span></span><br/> <span data-ttu-id="a573a-1384">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1384">0</span></span><br/>

<span data-ttu-id="a573a-1385">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1385">1</span></span>

<span data-ttu-id="a573a-1386">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1386">2</span></span>

<span data-ttu-id="a573a-1387">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1387">3</span></span>

<span data-ttu-id="a573a-1388">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1388">4</span></span>

<span data-ttu-id="a573a-1389">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1389">5</span></span>

<span data-ttu-id="a573a-1390">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1390">6</span></span>

<span data-ttu-id="a573a-1391">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1391">7</span></span>

<span data-ttu-id="a573a-1392">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1392">8</span></span>

<span data-ttu-id="a573a-1393">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1393">9</span></span>

<span data-ttu-id="a573a-1394">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1394">3</span></span><br/> <span data-ttu-id="a573a-1395">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1395">0</span></span><br/>

<span data-ttu-id="a573a-1396">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1396">1</span></span>

<span data-ttu-id="a573a-1397">ккловерпас</span><span class="sxs-lookup"><span data-stu-id="a573a-1397">CcLowerPath</span></span>

<span data-ttu-id="a573a-1398">\_Ловерпас (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1398">\_lowerPath (variable)</span></span>

<span data-ttu-id="a573a-1399">...</span><span class="sxs-lookup"><span data-stu-id="a573a-1399">...</span></span>

<span data-ttu-id="a573a-1400">\_Заполнение (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1400">\_padding ( variable)</span></span>

<span data-ttu-id="a573a-1401">\_недопустим</span><span class="sxs-lookup"><span data-stu-id="a573a-1401">\_length</span></span>

<span data-ttu-id="a573a-1402">\_фрекурсиве</span><span class="sxs-lookup"><span data-stu-id="a573a-1402">\_fRecursive</span></span>

<span data-ttu-id="a573a-1403">\_фвиртуал</span><span class="sxs-lookup"><span data-stu-id="a573a-1403">\_fVirtual</span></span>



 

<span data-ttu-id="a573a-1404">**Ккловерпас**: 32-разрядное целое число без знака, содержащее количество символов Юникода в \_ поле ловерпас.</span><span class="sxs-lookup"><span data-stu-id="a573a-1404">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="a573a-1405">**\_ ловерпас**: строка в Юникоде, не заканчивающаяся нулем, представляющая **путь** , к которому должен быть ограничен запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-1405">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="a573a-1406">Поле Ккловерпас содержит длину строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-1406">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="a573a-1407">**\_ Заполнение**: это поле должно иметь длину от 0 до 3 байт.</span><span class="sxs-lookup"><span data-stu-id="a573a-1407">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="a573a-1408">Длина этого поля должна быть такой, что следующее поле начинается со смещения, кратного 4 байтам от начала сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="a573a-1408">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="a573a-1409">Если это поле (т. е. Длина ненулевой), то значение, которое он содержит, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="a573a-1409">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="a573a-1410">Содержимое этого поля должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-1410">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="a573a-1411">**\_ length**: 32-разрядное целое число без знака, содержащее длину \_ Ловерпас в символах Юникода.</span><span class="sxs-lookup"><span data-stu-id="a573a-1411">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="a573a-1412">Это должно быть то же значение, что и Ккловерпас.</span><span class="sxs-lookup"><span data-stu-id="a573a-1412">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="a573a-1413">**\_ фрекурсиве**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-1413">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="a573a-1414">НЕОБХОДИМО задать значение 0x00000001 или 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-1414">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="a573a-1415">Если задано значение 0x00000001, сервер должен рекурсивно проверять все подкаталоги пути.</span><span class="sxs-lookup"><span data-stu-id="a573a-1415">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="a573a-1416">Если задано значение 0x00000000, сервер не должен проверять подкаталоги.</span><span class="sxs-lookup"><span data-stu-id="a573a-1416">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="a573a-1417">**\_ фвиртуал**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-1417">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="a573a-1418">НЕОБХОДИМО задать значение 0x00000001 или 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-1418">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="a573a-1419">Если задано значение 0x00000001, \_ ловерпас является виртуальным путем (URL-адресом, связанным с физическим каталогом в файловой системе) для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="a573a-1419">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="a573a-1420">Если задано значение 0x00000000, \_ ловерпас является путем к файловой системе.</span><span class="sxs-lookup"><span data-stu-id="a573a-1420">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="a573a-1421">2.2.1.12 Ксорт</span><span class="sxs-lookup"><span data-stu-id="a573a-1421">2.2.1.12 CSort</span></span>

<span data-ttu-id="a573a-1422">Структура Ксорт определяет столбец для сортировки.</span><span class="sxs-lookup"><span data-stu-id="a573a-1422">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="a573a-1423">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1423">0</span></span>

<span data-ttu-id="a573a-1424">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1424">1</span></span>

<span data-ttu-id="a573a-1425">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1425">2</span></span>

<span data-ttu-id="a573a-1426">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1426">3</span></span>

<span data-ttu-id="a573a-1427">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1427">4</span></span>

<span data-ttu-id="a573a-1428">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1428">5</span></span>

<span data-ttu-id="a573a-1429">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1429">6</span></span>

<span data-ttu-id="a573a-1430">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1430">7</span></span>

<span data-ttu-id="a573a-1431">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1431">8</span></span>

<span data-ttu-id="a573a-1432">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1432">9</span></span>

<span data-ttu-id="a573a-1433">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1433">1</span></span><br/> <span data-ttu-id="a573a-1434">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1434">0</span></span><br/>

<span data-ttu-id="a573a-1435">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1435">1</span></span>

<span data-ttu-id="a573a-1436">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1436">2</span></span>

<span data-ttu-id="a573a-1437">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1437">3</span></span>

<span data-ttu-id="a573a-1438">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1438">4</span></span>

<span data-ttu-id="a573a-1439">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1439">5</span></span>

<span data-ttu-id="a573a-1440">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1440">6</span></span>

<span data-ttu-id="a573a-1441">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1441">7</span></span>

<span data-ttu-id="a573a-1442">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1442">8</span></span>

<span data-ttu-id="a573a-1443">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1443">9</span></span>

<span data-ttu-id="a573a-1444">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1444">2</span></span><br/> <span data-ttu-id="a573a-1445">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1445">0</span></span><br/>

<span data-ttu-id="a573a-1446">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1446">1</span></span>

<span data-ttu-id="a573a-1447">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1447">2</span></span>

<span data-ttu-id="a573a-1448">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1448">3</span></span>

<span data-ttu-id="a573a-1449">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1449">4</span></span>

<span data-ttu-id="a573a-1450">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1450">5</span></span>

<span data-ttu-id="a573a-1451">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1451">6</span></span>

<span data-ttu-id="a573a-1452">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1452">7</span></span>

<span data-ttu-id="a573a-1453">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1453">8</span></span>

<span data-ttu-id="a573a-1454">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1454">9</span></span>

<span data-ttu-id="a573a-1455">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1455">3</span></span><br/> <span data-ttu-id="a573a-1456">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1456">0</span></span><br/>

<span data-ttu-id="a573a-1457">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1457">1</span></span>

<span data-ttu-id="a573a-1458">пидколумн</span><span class="sxs-lookup"><span data-stu-id="a573a-1458">pidColumn</span></span>

<span data-ttu-id="a573a-1459">Параметр dwOrd</span><span class="sxs-lookup"><span data-stu-id="a573a-1459">dwOrder</span></span>

<span data-ttu-id="a573a-1460">locale</span><span class="sxs-lookup"><span data-stu-id="a573a-1460">locale</span></span>



 

<span data-ttu-id="a573a-1461">**пидколумн**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-1461">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="a573a-1462">Номер столбца, по которому выполняется сортировка.</span><span class="sxs-lookup"><span data-stu-id="a573a-1462">The number of the column to sort by.</span></span>

<span data-ttu-id="a573a-1463">**параметр DWORD**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-1463">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="a573a-1464">ДОЛЖНО иметь одно из следующих значений, указывая способ сортировки по столбцу.</span><span class="sxs-lookup"><span data-stu-id="a573a-1464">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="a573a-1465">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1465">Value</span></span>                        | <span data-ttu-id="a573a-1466">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1466">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-1467">ЗАПРОС \_ сортасценд 0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-1467">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="a573a-1468">Строки сортируются в возрастающем порядке по значениям в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="a573a-1468">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="a573a-1469">ЗАПРОС в \_ порядке 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-1469">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="a573a-1470">Строки сортируются в убывающем порядке на основе значений в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="a573a-1470">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="a573a-1471">**языковой стандарт**: 32-разрядное целое число без знака, указывающее языковой стандарт, как указано в \[ приложении MS-GPSI, \] из которого находится столбец.</span><span class="sxs-lookup"><span data-stu-id="a573a-1471">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="a573a-1472">2.2.1.13 Ксинрестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-1472">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="a573a-1473">Структура Ксинрестриктион содержит слово или его синонимы для фразы запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-1473">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="a573a-1474">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1474">0</span></span>

<span data-ttu-id="a573a-1475">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1475">1</span></span>

<span data-ttu-id="a573a-1476">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1476">2</span></span>

<span data-ttu-id="a573a-1477">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1477">3</span></span>

<span data-ttu-id="a573a-1478">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1478">4</span></span>

<span data-ttu-id="a573a-1479">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1479">5</span></span>

<span data-ttu-id="a573a-1480">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1480">6</span></span>

<span data-ttu-id="a573a-1481">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1481">7</span></span>

<span data-ttu-id="a573a-1482">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1482">8</span></span>

<span data-ttu-id="a573a-1483">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1483">9</span></span>

<span data-ttu-id="a573a-1484">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1484">1</span></span><br/> <span data-ttu-id="a573a-1485">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1485">0</span></span><br/>

<span data-ttu-id="a573a-1486">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1486">1</span></span>

<span data-ttu-id="a573a-1487">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1487">2</span></span>

<span data-ttu-id="a573a-1488">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1488">3</span></span>

<span data-ttu-id="a573a-1489">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1489">4</span></span>

<span data-ttu-id="a573a-1490">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1490">5</span></span>

<span data-ttu-id="a573a-1491">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1491">6</span></span>

<span data-ttu-id="a573a-1492">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1492">7</span></span>

<span data-ttu-id="a573a-1493">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1493">8</span></span>

<span data-ttu-id="a573a-1494">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1494">9</span></span>

<span data-ttu-id="a573a-1495">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1495">2</span></span><br/> <span data-ttu-id="a573a-1496">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1496">0</span></span><br/>

<span data-ttu-id="a573a-1497">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1497">1</span></span>

<span data-ttu-id="a573a-1498">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1498">2</span></span>

<span data-ttu-id="a573a-1499">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1499">3</span></span>

<span data-ttu-id="a573a-1500">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1500">4</span></span>

<span data-ttu-id="a573a-1501">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1501">5</span></span>

<span data-ttu-id="a573a-1502">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1502">6</span></span>

<span data-ttu-id="a573a-1503">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1503">7</span></span>

<span data-ttu-id="a573a-1504">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1504">8</span></span>

<span data-ttu-id="a573a-1505">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1505">9</span></span>

<span data-ttu-id="a573a-1506">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1506">3</span></span><br/> <span data-ttu-id="a573a-1507">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1507">0</span></span><br/>

<span data-ttu-id="a573a-1508">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1508">1</span></span>

<span data-ttu-id="a573a-1509">Ограничение</span><span class="sxs-lookup"><span data-stu-id="a573a-1509">Restriction</span></span>

<span data-ttu-id="a573a-1510">...</span><span class="sxs-lookup"><span data-stu-id="a573a-1510">...</span></span>

<span data-ttu-id="a573a-1511">...</span><span class="sxs-lookup"><span data-stu-id="a573a-1511">...</span></span>

<span data-ttu-id="a573a-1512">ккэй</span><span class="sxs-lookup"><span data-stu-id="a573a-1512">cKey</span></span>

<span data-ttu-id="a573a-1513">\_Кэйаррай (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1513">\_keyArray (variable)</span></span>

<span data-ttu-id="a573a-1514">\_Диапазон</span><span class="sxs-lookup"><span data-stu-id="a573a-1514">\_isRange</span></span>



 

<span data-ttu-id="a573a-1515">**Ограничение**: структура коккрестриктион, указывающая расположение слова.</span><span class="sxs-lookup"><span data-stu-id="a573a-1515">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="a573a-1516">**ккэй**: 32-битовое целое число без знака, указывающее количество элементов в \_ массиве кэйаррай.</span><span class="sxs-lookup"><span data-stu-id="a573a-1516">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="a573a-1517">**\_ кэйаррай**: массив структур ккэй, задающий слово и его синонимы.</span><span class="sxs-lookup"><span data-stu-id="a573a-1517">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="a573a-1518">параметр **\_ Range**: Если задано значение 0x01, то ключи являются префиксами для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="a573a-1518">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="a573a-1519">Если задано значение 0x00, то для соответствия ключам используются точные значения.</span><span class="sxs-lookup"><span data-stu-id="a573a-1519">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="a573a-1520">\_параметру "диапазон" не должны быть присвоены никакие другие значения.</span><span class="sxs-lookup"><span data-stu-id="a573a-1520">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="a573a-1521">2.2.1.14 Квекторрестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-1521">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="a573a-1522">Структура Квекторрестриктион содержит взвешенное значение или операцию для узла дерева команд.</span><span class="sxs-lookup"><span data-stu-id="a573a-1522">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="a573a-1523">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1523">0</span></span>

<span data-ttu-id="a573a-1524">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1524">1</span></span>

<span data-ttu-id="a573a-1525">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1525">2</span></span>

<span data-ttu-id="a573a-1526">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1526">3</span></span>

<span data-ttu-id="a573a-1527">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1527">4</span></span>

<span data-ttu-id="a573a-1528">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1528">5</span></span>

<span data-ttu-id="a573a-1529">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1529">6</span></span>

<span data-ttu-id="a573a-1530">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1530">7</span></span>

<span data-ttu-id="a573a-1531">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1531">8</span></span>

<span data-ttu-id="a573a-1532">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1532">9</span></span>

<span data-ttu-id="a573a-1533">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1533">1</span></span><br/> <span data-ttu-id="a573a-1534">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1534">0</span></span><br/>

<span data-ttu-id="a573a-1535">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1535">1</span></span>

<span data-ttu-id="a573a-1536">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1536">2</span></span>

<span data-ttu-id="a573a-1537">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1537">3</span></span>

<span data-ttu-id="a573a-1538">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1538">4</span></span>

<span data-ttu-id="a573a-1539">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1539">5</span></span>

<span data-ttu-id="a573a-1540">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1540">6</span></span>

<span data-ttu-id="a573a-1541">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1541">7</span></span>

<span data-ttu-id="a573a-1542">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1542">8</span></span>

<span data-ttu-id="a573a-1543">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1543">9</span></span>

<span data-ttu-id="a573a-1544">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1544">2</span></span><br/> <span data-ttu-id="a573a-1545">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1545">0</span></span><br/>

<span data-ttu-id="a573a-1546">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1546">1</span></span>

<span data-ttu-id="a573a-1547">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1547">2</span></span>

<span data-ttu-id="a573a-1548">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1548">3</span></span>

<span data-ttu-id="a573a-1549">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1549">4</span></span>

<span data-ttu-id="a573a-1550">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1550">5</span></span>

<span data-ttu-id="a573a-1551">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1551">6</span></span>

<span data-ttu-id="a573a-1552">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1552">7</span></span>

<span data-ttu-id="a573a-1553">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1553">8</span></span>

<span data-ttu-id="a573a-1554">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1554">9</span></span>

<span data-ttu-id="a573a-1555">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1555">3</span></span><br/> <span data-ttu-id="a573a-1556">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1556">0</span></span><br/>

<span data-ttu-id="a573a-1557">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1557">1</span></span>

<span data-ttu-id="a573a-1558">\_Прес (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1558">\_pres (variable)</span></span>

<span data-ttu-id="a573a-1559">...</span><span class="sxs-lookup"><span data-stu-id="a573a-1559">...</span></span>

<span data-ttu-id="a573a-1560">\_Заполнение (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1560">\_padding (variable)</span></span>

<span data-ttu-id="a573a-1561">\_улранкмесод</span><span class="sxs-lookup"><span data-stu-id="a573a-1561">\_ulRankMethod</span></span>



 

<span data-ttu-id="a573a-1562">**\_ прес**: дерево команд кнодерестриктион, на основе которого выполняется ранжирование или операция.</span><span class="sxs-lookup"><span data-stu-id="a573a-1562">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="a573a-1563">**\_ Заполнение**: это поле должно иметь длину от 0 до 3 байт.</span><span class="sxs-lookup"><span data-stu-id="a573a-1563">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="a573a-1564">Длина этого поля должна быть такой, что следующее поле начинается со смещения, кратного 4 байтам от начала сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="a573a-1564">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="a573a-1565">Если это поле (т. е. Длина ненулевой), то значение, которое он содержит, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="a573a-1565">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="a573a-1566">Содержимое этого поля должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-1566">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="a573a-1567">**\_ улранкмесод**: 32-битовое целое число без знака, указывающее алгоритм ранжирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-1567">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="a573a-1568">НЕОБХОДИМО задать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a573a-1568">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="a573a-1569">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1569">Value</span></span>                            | <span data-ttu-id="a573a-1570">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1570">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="a573a-1571">\_Минимальное звание вектора ( \_ 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="a573a-1571">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="a573a-1572">Используйте минимальное Салтон алгоритма \[ \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-1572">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="a573a-1573">Максимум ВЕКТОРного \_ ранга \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-1573">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="a573a-1574">Использовать максимальный алгоритм \[ Салтон \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-1574">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="a573a-1575">\_Внутренний приоритетный экземпляр \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-1575">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="a573a-1576">Использовать внутренний алгоритм продукта \[ Салтон \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-1576">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="a573a-1577">ВЕКТОРные \_ ранжирующие \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-1577">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="a573a-1578">Используйте алгоритм "коэффициент костей" \[ Салтон \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-1578">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="a573a-1579">ВЕКТОР \_ ранжирования \_ джаккарда 0x00000004</span><span class="sxs-lookup"><span data-stu-id="a573a-1579">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="a573a-1580">Используйте алгоритм Джаккарда коэффициента \[ Салтон \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-1580">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="a573a-1581">2.2.1.15 Квордрестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-1581">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="a573a-1582">Структура Квордрестриктион содержит слово для фразы запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-1582">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="a573a-1583">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1583">0</span></span>

<span data-ttu-id="a573a-1584">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1584">1</span></span>

<span data-ttu-id="a573a-1585">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1585">2</span></span>

<span data-ttu-id="a573a-1586">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1586">3</span></span>

<span data-ttu-id="a573a-1587">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1587">4</span></span>

<span data-ttu-id="a573a-1588">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1588">5</span></span>

<span data-ttu-id="a573a-1589">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1589">6</span></span>

<span data-ttu-id="a573a-1590">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1590">7</span></span>

<span data-ttu-id="a573a-1591">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1591">8</span></span>

<span data-ttu-id="a573a-1592">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1592">9</span></span>

<span data-ttu-id="a573a-1593">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1593">1</span></span><br/> <span data-ttu-id="a573a-1594">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1594">0</span></span><br/>

<span data-ttu-id="a573a-1595">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1595">1</span></span>

<span data-ttu-id="a573a-1596">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1596">2</span></span>

<span data-ttu-id="a573a-1597">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1597">3</span></span>

<span data-ttu-id="a573a-1598">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1598">4</span></span>

<span data-ttu-id="a573a-1599">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1599">5</span></span>

<span data-ttu-id="a573a-1600">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1600">6</span></span>

<span data-ttu-id="a573a-1601">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1601">7</span></span>

<span data-ttu-id="a573a-1602">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1602">8</span></span>

<span data-ttu-id="a573a-1603">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1603">9</span></span>

<span data-ttu-id="a573a-1604">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1604">2</span></span><br/> <span data-ttu-id="a573a-1605">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1605">0</span></span><br/>

<span data-ttu-id="a573a-1606">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1606">1</span></span>

<span data-ttu-id="a573a-1607">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1607">2</span></span>

<span data-ttu-id="a573a-1608">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1608">3</span></span>

<span data-ttu-id="a573a-1609">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1609">4</span></span>

<span data-ttu-id="a573a-1610">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1610">5</span></span>

<span data-ttu-id="a573a-1611">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1611">6</span></span>

<span data-ttu-id="a573a-1612">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1612">7</span></span>

<span data-ttu-id="a573a-1613">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1613">8</span></span>

<span data-ttu-id="a573a-1614">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1614">9</span></span>

<span data-ttu-id="a573a-1615">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1615">3</span></span><br/> <span data-ttu-id="a573a-1616">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1616">0</span></span><br/>

<span data-ttu-id="a573a-1617">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1617">1</span></span>

<span data-ttu-id="a573a-1618">ограничение</span><span class="sxs-lookup"><span data-stu-id="a573a-1618">restriction</span></span>

<span data-ttu-id="a573a-1619">...</span><span class="sxs-lookup"><span data-stu-id="a573a-1619">...</span></span>

<span data-ttu-id="a573a-1620">...</span><span class="sxs-lookup"><span data-stu-id="a573a-1620">...</span></span>

<span data-ttu-id="a573a-1621">\_Key (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1621">\_key (variable)</span></span>

<span data-ttu-id="a573a-1622">\_Диапазон</span><span class="sxs-lookup"><span data-stu-id="a573a-1622">\_isRange</span></span>



 

<span data-ttu-id="a573a-1623">**ограничение**: структура коккрестриктион, указывающая расположение слова.</span><span class="sxs-lookup"><span data-stu-id="a573a-1623">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="a573a-1624">**\_ Key**: структура ккэй, указывающая слово.</span><span class="sxs-lookup"><span data-stu-id="a573a-1624">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="a573a-1625">параметр **\_ Range**: Если задано значение 0x01, ключ является префиксом для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="a573a-1625">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="a573a-1626">Если задано значение 0x00, то ключ является точным значением для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="a573a-1626">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="a573a-1627">\_параметру "диапазон" не должно быть присвоено другое значение.</span><span class="sxs-lookup"><span data-stu-id="a573a-1627">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="a573a-1628">2.2.1.16 Крестриктион</span><span class="sxs-lookup"><span data-stu-id="a573a-1628">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="a573a-1629">Структура Крестриктион содержит узел дерева команд запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-1629">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="a573a-1630">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1630">0</span></span>

<span data-ttu-id="a573a-1631">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1631">1</span></span>

<span data-ttu-id="a573a-1632">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1632">2</span></span>

<span data-ttu-id="a573a-1633">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1633">3</span></span>

<span data-ttu-id="a573a-1634">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1634">4</span></span>

<span data-ttu-id="a573a-1635">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1635">5</span></span>

<span data-ttu-id="a573a-1636">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1636">6</span></span>

<span data-ttu-id="a573a-1637">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1637">7</span></span>

<span data-ttu-id="a573a-1638">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1638">8</span></span>

<span data-ttu-id="a573a-1639">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1639">9</span></span>

<span data-ttu-id="a573a-1640">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1640">1</span></span><br/> <span data-ttu-id="a573a-1641">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1641">0</span></span><br/>

<span data-ttu-id="a573a-1642">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1642">1</span></span>

<span data-ttu-id="a573a-1643">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1643">2</span></span>

<span data-ttu-id="a573a-1644">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1644">3</span></span>

<span data-ttu-id="a573a-1645">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1645">4</span></span>

<span data-ttu-id="a573a-1646">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1646">5</span></span>

<span data-ttu-id="a573a-1647">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1647">6</span></span>

<span data-ttu-id="a573a-1648">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1648">7</span></span>

<span data-ttu-id="a573a-1649">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1649">8</span></span>

<span data-ttu-id="a573a-1650">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1650">9</span></span>

<span data-ttu-id="a573a-1651">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1651">2</span></span><br/> <span data-ttu-id="a573a-1652">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1652">0</span></span><br/>

<span data-ttu-id="a573a-1653">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1653">1</span></span>

<span data-ttu-id="a573a-1654">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1654">2</span></span>

<span data-ttu-id="a573a-1655">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1655">3</span></span>

<span data-ttu-id="a573a-1656">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1656">4</span></span>

<span data-ttu-id="a573a-1657">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1657">5</span></span>

<span data-ttu-id="a573a-1658">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1658">6</span></span>

<span data-ttu-id="a573a-1659">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1659">7</span></span>

<span data-ttu-id="a573a-1660">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1660">8</span></span>

<span data-ttu-id="a573a-1661">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1661">9</span></span>

<span data-ttu-id="a573a-1662">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1662">3</span></span><br/> <span data-ttu-id="a573a-1663">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1663">0</span></span><br/>

<span data-ttu-id="a573a-1664">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1664">1</span></span>

<span data-ttu-id="a573a-1665">\_ултипе</span><span class="sxs-lookup"><span data-stu-id="a573a-1665">\_ulType</span></span>

<span data-ttu-id="a573a-1666">Вес</span><span class="sxs-lookup"><span data-stu-id="a573a-1666">Weight</span></span>

<span data-ttu-id="a573a-1667">Ограничение</span><span class="sxs-lookup"><span data-stu-id="a573a-1667">Restriction</span></span>



 

<span data-ttu-id="a573a-1668">**\_ ултипе**: 32-битовое целое число без знака, указывающее тип ограничения, используемый для узла дерева команд.</span><span class="sxs-lookup"><span data-stu-id="a573a-1668">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="a573a-1669">НЕОБХОДИМО задать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a573a-1669">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="a573a-1670">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1670">Value</span></span>                    | <span data-ttu-id="a573a-1671">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1671">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-1672">Ртноне 0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-1672">RTNone 0x00000000</span></span>        | <span data-ttu-id="a573a-1673">Узел представляет пропускаемое слово в векторном запросе.</span><span class="sxs-lookup"><span data-stu-id="a573a-1673">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="a573a-1674">Ртанд 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-1674">RTAnd 0x00000001</span></span>         | <span data-ttu-id="a573a-1675">Узел содержит Кнодерестриктион, на основе которого выполняется логическая операция.</span><span class="sxs-lookup"><span data-stu-id="a573a-1675">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="a573a-1676">РТор 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-1676">RTOr 0x00000002</span></span>          | <span data-ttu-id="a573a-1677">Узел содержит Кнодерестриктион, для которого должна быть выполнена логическая операция или.</span><span class="sxs-lookup"><span data-stu-id="a573a-1677">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="a573a-1678">Ртнот 0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-1678">RTNot 0x00000003</span></span>         | <span data-ttu-id="a573a-1679">Узел содержит Крестриктион, для которого не выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="a573a-1679">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="a573a-1680">Ртконтент 0x00000004</span><span class="sxs-lookup"><span data-stu-id="a573a-1680">RTContent 0x00000004</span></span>     | <span data-ttu-id="a573a-1681">Узел содержит Кконтентрестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-1681">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="a573a-1682">Ртпроперти 0x00000005</span><span class="sxs-lookup"><span data-stu-id="a573a-1682">RTProperty 0x00000005</span></span>    | <span data-ttu-id="a573a-1683">Узел содержит Кпропертирестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-1683">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="a573a-1684">Ртпроксимити 0x00000006</span><span class="sxs-lookup"><span data-stu-id="a573a-1684">RTProximity 0x00000006</span></span>   | <span data-ttu-id="a573a-1685">Узел содержит Кнодерестриктион, на основе которого будет выполняться ранжирование с учетом расположения,</span><span class="sxs-lookup"><span data-stu-id="a573a-1685">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="a573a-1686">Ртвектор 0x00000007</span><span class="sxs-lookup"><span data-stu-id="a573a-1686">RTVector 0x00000007</span></span>      | <span data-ttu-id="a573a-1687">Узел содержит Квекторрестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-1687">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="a573a-1688">Ртнатлангуаже 0x00000008</span><span class="sxs-lookup"><span data-stu-id="a573a-1688">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="a573a-1689">Узел содержит Кнатлангуажерестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-1689">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="a573a-1690">Ртскопе 0x00000009</span><span class="sxs-lookup"><span data-stu-id="a573a-1690">RTScope 0x00000009</span></span>       | <span data-ttu-id="a573a-1691">Узел содержит Кскоперестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-1691">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="a573a-1692">ПРАНИ 0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="a573a-1692">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="a573a-1693">Узел содержит Цинтерналпропертирестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-1693">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="a573a-1694">Ртранже 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="a573a-1694">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="a573a-1695">Узел содержит Кранжерестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-1695">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="a573a-1696">Ртфрасе 0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="a573a-1696">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="a573a-1697">Узел содержит Кнодерестриктион, для которого должно быть выполнено совпадение фразы.</span><span class="sxs-lookup"><span data-stu-id="a573a-1697">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="a573a-1698">Ртсиноним 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="a573a-1698">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="a573a-1699">Узел содержит Ксинрестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-1699">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="a573a-1700">Ртворд 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="a573a-1700">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="a573a-1701">Узел содержит Квордрестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-1701">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="a573a-1702">**Вес**: 32-битовое целое число без знака, представляющее вес узла.</span><span class="sxs-lookup"><span data-stu-id="a573a-1702">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="a573a-1703">Вес указывает на важность узла относительно других узлов в дереве команд запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-1703">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="a573a-1704">Более важные значения веса более важны.</span><span class="sxs-lookup"><span data-stu-id="a573a-1704">Higher weight values are more important.</span></span>

<span data-ttu-id="a573a-1705">**Ограничение**: тип ограничения для узла дерева команд.</span><span class="sxs-lookup"><span data-stu-id="a573a-1705">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="a573a-1706">Синтаксис должен быть указан в \_ поле ултипе.</span><span class="sxs-lookup"><span data-stu-id="a573a-1706">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="a573a-1707">2.2.1.17 Кколумнсет</span><span class="sxs-lookup"><span data-stu-id="a573a-1707">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="a573a-1708">Структура Кколумнсет указывает возвращаемые номера столбцов.</span><span class="sxs-lookup"><span data-stu-id="a573a-1708">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="a573a-1709">Эта структура всегда используется в ссылке на определенную структуру Кпидмаппер (раздел 2.2.1.23).</span><span class="sxs-lookup"><span data-stu-id="a573a-1709">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="a573a-1710">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1710">0</span></span>

<span data-ttu-id="a573a-1711">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1711">1</span></span>

<span data-ttu-id="a573a-1712">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1712">2</span></span>

<span data-ttu-id="a573a-1713">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1713">3</span></span>

<span data-ttu-id="a573a-1714">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1714">4</span></span>

<span data-ttu-id="a573a-1715">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1715">5</span></span>

<span data-ttu-id="a573a-1716">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1716">6</span></span>

<span data-ttu-id="a573a-1717">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1717">7</span></span>

<span data-ttu-id="a573a-1718">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1718">8</span></span>

<span data-ttu-id="a573a-1719">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1719">9</span></span>

<span data-ttu-id="a573a-1720">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1720">1</span></span><br/> <span data-ttu-id="a573a-1721">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1721">0</span></span><br/>

<span data-ttu-id="a573a-1722">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1722">1</span></span>

<span data-ttu-id="a573a-1723">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1723">2</span></span>

<span data-ttu-id="a573a-1724">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1724">3</span></span>

<span data-ttu-id="a573a-1725">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1725">4</span></span>

<span data-ttu-id="a573a-1726">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1726">5</span></span>

<span data-ttu-id="a573a-1727">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1727">6</span></span>

<span data-ttu-id="a573a-1728">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1728">7</span></span>

<span data-ttu-id="a573a-1729">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1729">8</span></span>

<span data-ttu-id="a573a-1730">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1730">9</span></span>

<span data-ttu-id="a573a-1731">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1731">2</span></span><br/> <span data-ttu-id="a573a-1732">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1732">0</span></span><br/>

<span data-ttu-id="a573a-1733">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1733">1</span></span>

<span data-ttu-id="a573a-1734">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1734">2</span></span>

<span data-ttu-id="a573a-1735">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1735">3</span></span>

<span data-ttu-id="a573a-1736">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1736">4</span></span>

<span data-ttu-id="a573a-1737">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1737">5</span></span>

<span data-ttu-id="a573a-1738">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1738">6</span></span>

<span data-ttu-id="a573a-1739">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1739">7</span></span>

<span data-ttu-id="a573a-1740">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1740">8</span></span>

<span data-ttu-id="a573a-1741">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1741">9</span></span>

<span data-ttu-id="a573a-1742">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1742">3</span></span><br/> <span data-ttu-id="a573a-1743">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1743">0</span></span><br/>

<span data-ttu-id="a573a-1744">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1744">1</span></span>

<span data-ttu-id="a573a-1745">count</span><span class="sxs-lookup"><span data-stu-id="a573a-1745">count</span></span>

<span data-ttu-id="a573a-1746">индексы (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1746">indexes (variable)</span></span>



 

<span data-ttu-id="a573a-1747">**Count**: 32-разрядное целое число без знака, указывающее количество элементов в массиве индексов.</span><span class="sxs-lookup"><span data-stu-id="a573a-1747">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="a573a-1748">**индексы**: массив из 4-байтных целых чисел без знака, представляющий индексы, начинающиеся с нуля, в массиве апропспек в соответствующей структуре кпидмаппер.</span><span class="sxs-lookup"><span data-stu-id="a573a-1748">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="a573a-1749">2.2.1.18 Ккатегоризатионсет</span><span class="sxs-lookup"><span data-stu-id="a573a-1749">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="a573a-1750">Структура Ккатегоризатионсет содержит сведения о группировании результирующего набора запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-1750">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="a573a-1751">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1751">0</span></span>

<span data-ttu-id="a573a-1752">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1752">1</span></span>

<span data-ttu-id="a573a-1753">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1753">2</span></span>

<span data-ttu-id="a573a-1754">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1754">3</span></span>

<span data-ttu-id="a573a-1755">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1755">4</span></span>

<span data-ttu-id="a573a-1756">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1756">5</span></span>

<span data-ttu-id="a573a-1757">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1757">6</span></span>

<span data-ttu-id="a573a-1758">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1758">7</span></span>

<span data-ttu-id="a573a-1759">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1759">8</span></span>

<span data-ttu-id="a573a-1760">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1760">9</span></span>

<span data-ttu-id="a573a-1761">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1761">1</span></span><br/> <span data-ttu-id="a573a-1762">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1762">0</span></span><br/>

<span data-ttu-id="a573a-1763">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1763">1</span></span>

<span data-ttu-id="a573a-1764">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1764">2</span></span>

<span data-ttu-id="a573a-1765">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1765">3</span></span>

<span data-ttu-id="a573a-1766">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1766">4</span></span>

<span data-ttu-id="a573a-1767">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1767">5</span></span>

<span data-ttu-id="a573a-1768">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1768">6</span></span>

<span data-ttu-id="a573a-1769">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1769">7</span></span>

<span data-ttu-id="a573a-1770">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1770">8</span></span>

<span data-ttu-id="a573a-1771">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1771">9</span></span>

<span data-ttu-id="a573a-1772">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1772">2</span></span><br/> <span data-ttu-id="a573a-1773">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1773">0</span></span><br/>

<span data-ttu-id="a573a-1774">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1774">1</span></span>

<span data-ttu-id="a573a-1775">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1775">2</span></span>

<span data-ttu-id="a573a-1776">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1776">3</span></span>

<span data-ttu-id="a573a-1777">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1777">4</span></span>

<span data-ttu-id="a573a-1778">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1778">5</span></span>

<span data-ttu-id="a573a-1779">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1779">6</span></span>

<span data-ttu-id="a573a-1780">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1780">7</span></span>

<span data-ttu-id="a573a-1781">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1781">8</span></span>

<span data-ttu-id="a573a-1782">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1782">9</span></span>

<span data-ttu-id="a573a-1783">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1783">3</span></span><br/> <span data-ttu-id="a573a-1784">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1784">0</span></span><br/>

<span data-ttu-id="a573a-1785">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1785">1</span></span>

<span data-ttu-id="a573a-1786">count</span><span class="sxs-lookup"><span data-stu-id="a573a-1786">count</span></span>

<span data-ttu-id="a573a-1787">категории (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1787">categories (variable)</span></span>



 

<span data-ttu-id="a573a-1788">**Count**: 32-разрядное целое число без знака, содержащее количество элементов в массиве Categories.</span><span class="sxs-lookup"><span data-stu-id="a573a-1788">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="a573a-1789">**Categories**: массив структур ккатегоризатионспек, задающий группирование запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-1789">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="a573a-1790">2.2.1.19 Ккатегоризатионспек</span><span class="sxs-lookup"><span data-stu-id="a573a-1790">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="a573a-1791">Структура Ккатегоризатионспек содержит группирование для результирующего набора запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-1791">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="a573a-1792">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1792">0</span></span>

<span data-ttu-id="a573a-1793">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1793">1</span></span>

<span data-ttu-id="a573a-1794">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1794">2</span></span>

<span data-ttu-id="a573a-1795">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1795">3</span></span>

<span data-ttu-id="a573a-1796">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1796">4</span></span>

<span data-ttu-id="a573a-1797">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1797">5</span></span>

<span data-ttu-id="a573a-1798">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1798">6</span></span>

<span data-ttu-id="a573a-1799">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1799">7</span></span>

<span data-ttu-id="a573a-1800">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1800">8</span></span>

<span data-ttu-id="a573a-1801">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1801">9</span></span>

<span data-ttu-id="a573a-1802">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1802">1</span></span><br/> <span data-ttu-id="a573a-1803">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1803">0</span></span><br/>

<span data-ttu-id="a573a-1804">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1804">1</span></span>

<span data-ttu-id="a573a-1805">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1805">2</span></span>

<span data-ttu-id="a573a-1806">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1806">3</span></span>

<span data-ttu-id="a573a-1807">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1807">4</span></span>

<span data-ttu-id="a573a-1808">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1808">5</span></span>

<span data-ttu-id="a573a-1809">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1809">6</span></span>

<span data-ttu-id="a573a-1810">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1810">7</span></span>

<span data-ttu-id="a573a-1811">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1811">8</span></span>

<span data-ttu-id="a573a-1812">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1812">9</span></span>

<span data-ttu-id="a573a-1813">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1813">2</span></span><br/> <span data-ttu-id="a573a-1814">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1814">0</span></span><br/>

<span data-ttu-id="a573a-1815">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1815">1</span></span>

<span data-ttu-id="a573a-1816">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1816">2</span></span>

<span data-ttu-id="a573a-1817">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1817">3</span></span>

<span data-ttu-id="a573a-1818">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1818">4</span></span>

<span data-ttu-id="a573a-1819">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1819">5</span></span>

<span data-ttu-id="a573a-1820">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1820">6</span></span>

<span data-ttu-id="a573a-1821">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1821">7</span></span>

<span data-ttu-id="a573a-1822">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1822">8</span></span>

<span data-ttu-id="a573a-1823">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1823">9</span></span>

<span data-ttu-id="a573a-1824">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1824">3</span></span><br/> <span data-ttu-id="a573a-1825">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1825">0</span></span><br/>

<span data-ttu-id="a573a-1826">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1826">1</span></span>

<span data-ttu-id="a573a-1827">\_Ксколумнс (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1827">\_csColumns (variable)</span></span>

<span data-ttu-id="a573a-1828">\_улкатегтипе</span><span class="sxs-lookup"><span data-stu-id="a573a-1828">\_ulCategType</span></span>



 

<span data-ttu-id="a573a-1829">**\_ ксколумнс**: структура кколумнсет, указывающая столбцы, по которым будет группироваться запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-1829">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="a573a-1830">**\_ улкатегтипе**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-1830">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="a573a-1831">НЕОБХОДИМО задать значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-1831">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="a573a-1832">2.2.1.20 Кдбколид</span><span class="sxs-lookup"><span data-stu-id="a573a-1832">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="a573a-1833">Структура Кдбколид содержит столбец.</span><span class="sxs-lookup"><span data-stu-id="a573a-1833">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="a573a-1834">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1834">0</span></span>

<span data-ttu-id="a573a-1835">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1835">1</span></span>

<span data-ttu-id="a573a-1836">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1836">2</span></span>

<span data-ttu-id="a573a-1837">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1837">3</span></span>

<span data-ttu-id="a573a-1838">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1838">4</span></span>

<span data-ttu-id="a573a-1839">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1839">5</span></span>

<span data-ttu-id="a573a-1840">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1840">6</span></span>

<span data-ttu-id="a573a-1841">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1841">7</span></span>

<span data-ttu-id="a573a-1842">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1842">8</span></span>

<span data-ttu-id="a573a-1843">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1843">9</span></span>

<span data-ttu-id="a573a-1844">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1844">1</span></span><br/> <span data-ttu-id="a573a-1845">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1845">0</span></span><br/>

<span data-ttu-id="a573a-1846">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1846">1</span></span>

<span data-ttu-id="a573a-1847">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1847">2</span></span>

<span data-ttu-id="a573a-1848">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1848">3</span></span>

<span data-ttu-id="a573a-1849">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1849">4</span></span>

<span data-ttu-id="a573a-1850">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1850">5</span></span>

<span data-ttu-id="a573a-1851">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1851">6</span></span>

<span data-ttu-id="a573a-1852">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1852">7</span></span>

<span data-ttu-id="a573a-1853">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1853">8</span></span>

<span data-ttu-id="a573a-1854">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1854">9</span></span>

<span data-ttu-id="a573a-1855">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1855">2</span></span><br/> <span data-ttu-id="a573a-1856">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1856">0</span></span><br/>

<span data-ttu-id="a573a-1857">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1857">1</span></span>

<span data-ttu-id="a573a-1858">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1858">2</span></span>

<span data-ttu-id="a573a-1859">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1859">3</span></span>

<span data-ttu-id="a573a-1860">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1860">4</span></span>

<span data-ttu-id="a573a-1861">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1861">5</span></span>

<span data-ttu-id="a573a-1862">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1862">6</span></span>

<span data-ttu-id="a573a-1863">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1863">7</span></span>

<span data-ttu-id="a573a-1864">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1864">8</span></span>

<span data-ttu-id="a573a-1865">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1865">9</span></span>

<span data-ttu-id="a573a-1866">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1866">3</span></span><br/> <span data-ttu-id="a573a-1867">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1867">0</span></span><br/>

<span data-ttu-id="a573a-1868">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1868">1</span></span>

<span data-ttu-id="a573a-1869">Элемент ekind</span><span class="sxs-lookup"><span data-stu-id="a573a-1869">eKind</span></span>

<span data-ttu-id="a573a-1870">Код GUID</span><span class="sxs-lookup"><span data-stu-id="a573a-1870">GUID</span></span>

<span data-ttu-id="a573a-1871">...</span><span class="sxs-lookup"><span data-stu-id="a573a-1871">...</span></span>

<span data-ttu-id="a573a-1872">...</span><span class="sxs-lookup"><span data-stu-id="a573a-1872">...</span></span>

<span data-ttu-id="a573a-1873">...</span><span class="sxs-lookup"><span data-stu-id="a573a-1873">...</span></span>

<span data-ttu-id="a573a-1874">улид</span><span class="sxs-lookup"><span data-stu-id="a573a-1874">ulId</span></span>

<span data-ttu-id="a573a-1875">Встринг (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1875">vString (variable)</span></span>



 

<span data-ttu-id="a573a-1876">**элемент ekind**: необходимо задать одно из приведенных ниже значений, которое указывает содержимое GUID и управляемое vValue.</span><span class="sxs-lookup"><span data-stu-id="a573a-1876">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="a573a-1877">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1877">Value</span></span>                            | <span data-ttu-id="a573a-1878">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1878">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-1879">\_Имя GUID дбкинд \_ 0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-1879">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="a573a-1880">Встринг содержит имя свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-1880">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="a573a-1881">ДБКИНД \_ GUID \_ PropID 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-1881">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="a573a-1882">Улид содержит 4-байтовое целое число, указывающее идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-1882">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="a573a-1883">ДБКИНД \_ пгуид \_ имя 0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-1883">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="a573a-1884">Встринг содержит имя свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-1884">vString contains a property name.</span></span> <span data-ttu-id="a573a-1885">Это значение должно рассматриваться так же, как \_ и \_ имя GUID дбкинд.</span><span class="sxs-lookup"><span data-stu-id="a573a-1885">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="a573a-1886">ДБКИНД \_ пгуид \_ PropID 0x00000004</span><span class="sxs-lookup"><span data-stu-id="a573a-1886">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="a573a-1887">Улид содержит 4-байтовое целое число, указывающее идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-1887">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="a573a-1888">Это значение должно быть таким же, как и ДБКИНД \_ GUID \_ PropID.</span><span class="sxs-lookup"><span data-stu-id="a573a-1888">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="a573a-1889">**GUID**: идентификатор GUID свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-1889">**GUID**: The property GUID.</span></span>

<span data-ttu-id="a573a-1890">**улид**: Если элемент ekind имеет значение дбкинд \_ GUID \_ PropID или дбкинд \_ пгуид \_ PropID, это поле содержит целое число без знака, в котором указывается идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-1890">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="a573a-1891">Если элемент ekind имеет значение ДБКИНД \_ GUID \_ или имя дбкинд \_ пгуид \_ , это поле содержит целое число без знака, указывающее количество символов Юникода, содержащихся в поле встринг.</span><span class="sxs-lookup"><span data-stu-id="a573a-1891">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="a573a-1892">**встринг**: строка Юникода, не заканчивающаяся нулем, представляющая имя свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-1892">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="a573a-1893">Его необходимо опустить, если для поля элемент ekind не задано значение ДБКИНД \_ GUID \_ Name или дбкинд \_ пгуид \_ Name.</span><span class="sxs-lookup"><span data-stu-id="a573a-1893">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="a573a-1894">2.2.1.21 Кдбпроп</span><span class="sxs-lookup"><span data-stu-id="a573a-1894">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="a573a-1895">Структура Кдбпроп содержит свойство.</span><span class="sxs-lookup"><span data-stu-id="a573a-1895">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="a573a-1896">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1896">0</span></span>

<span data-ttu-id="a573a-1897">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1897">1</span></span>

<span data-ttu-id="a573a-1898">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1898">2</span></span>

<span data-ttu-id="a573a-1899">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1899">3</span></span>

<span data-ttu-id="a573a-1900">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1900">4</span></span>

<span data-ttu-id="a573a-1901">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1901">5</span></span>

<span data-ttu-id="a573a-1902">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1902">6</span></span>

<span data-ttu-id="a573a-1903">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1903">7</span></span>

<span data-ttu-id="a573a-1904">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1904">8</span></span>

<span data-ttu-id="a573a-1905">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1905">9</span></span>

<span data-ttu-id="a573a-1906">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1906">1</span></span><br/> <span data-ttu-id="a573a-1907">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1907">0</span></span><br/>

<span data-ttu-id="a573a-1908">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1908">1</span></span>

<span data-ttu-id="a573a-1909">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1909">2</span></span>

<span data-ttu-id="a573a-1910">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1910">3</span></span>

<span data-ttu-id="a573a-1911">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1911">4</span></span>

<span data-ttu-id="a573a-1912">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1912">5</span></span>

<span data-ttu-id="a573a-1913">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1913">6</span></span>

<span data-ttu-id="a573a-1914">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1914">7</span></span>

<span data-ttu-id="a573a-1915">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1915">8</span></span>

<span data-ttu-id="a573a-1916">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1916">9</span></span>

<span data-ttu-id="a573a-1917">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1917">2</span></span><br/> <span data-ttu-id="a573a-1918">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1918">0</span></span><br/>

<span data-ttu-id="a573a-1919">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1919">1</span></span>

<span data-ttu-id="a573a-1920">2</span><span class="sxs-lookup"><span data-stu-id="a573a-1920">2</span></span>

<span data-ttu-id="a573a-1921">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1921">3</span></span>

<span data-ttu-id="a573a-1922">4</span><span class="sxs-lookup"><span data-stu-id="a573a-1922">4</span></span>

<span data-ttu-id="a573a-1923">5</span><span class="sxs-lookup"><span data-stu-id="a573a-1923">5</span></span>

<span data-ttu-id="a573a-1924">6</span><span class="sxs-lookup"><span data-stu-id="a573a-1924">6</span></span>

<span data-ttu-id="a573a-1925">7</span><span class="sxs-lookup"><span data-stu-id="a573a-1925">7</span></span>

<span data-ttu-id="a573a-1926">8</span><span class="sxs-lookup"><span data-stu-id="a573a-1926">8</span></span>

<span data-ttu-id="a573a-1927">9</span><span class="sxs-lookup"><span data-stu-id="a573a-1927">9</span></span>

<span data-ttu-id="a573a-1928">3</span><span class="sxs-lookup"><span data-stu-id="a573a-1928">3</span></span><br/> <span data-ttu-id="a573a-1929">0</span><span class="sxs-lookup"><span data-stu-id="a573a-1929">0</span></span><br/>

<span data-ttu-id="a573a-1930">1</span><span class="sxs-lookup"><span data-stu-id="a573a-1930">1</span></span>

<span data-ttu-id="a573a-1931">дбпропид</span><span class="sxs-lookup"><span data-stu-id="a573a-1931">DBPROPID</span></span>

<span data-ttu-id="a573a-1932">дбпропоптионс</span><span class="sxs-lookup"><span data-stu-id="a573a-1932">DBPROPOPTIONS</span></span>

<span data-ttu-id="a573a-1933">дбпропстатус</span><span class="sxs-lookup"><span data-stu-id="a573a-1933">DBPROPSTATUS</span></span>

<span data-ttu-id="a573a-1934">идентификатора столбца (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1934">colid (variable)</span></span>

<span data-ttu-id="a573a-1935">Управляемое vValue (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-1935">vValue (variable)</span></span>



 

<span data-ttu-id="a573a-1936">**Дбпропид**: 32-битовое целое число без знака, указывающее идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-1936">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="a573a-1937">**Дбпропоптионс** : необходимо задать значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-1937">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="a573a-1938">**Дбпропстатус**: необходимо задать значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-1938">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="a573a-1939">**идентификатора столбца**: структура кдбколид, как указано в разделе 2.2.1.20, указывающая столбец, к которому применяется свойство.</span><span class="sxs-lookup"><span data-stu-id="a573a-1939">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="a573a-1940">**управляемое vValue**: кбасесторажевариант, содержащий значение свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-1940">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="a573a-1941">свойства 2.2.1.21.1</span><span class="sxs-lookup"><span data-stu-id="a573a-1941">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="a573a-1942">В этом разделе описаны свойства, используемые CISP.</span><span class="sxs-lookup"><span data-stu-id="a573a-1942">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="a573a-1943">Эти свойства группируются в три набора свойств, Ident 2.2.1.21.1 ифиед в поле Гуидпропертисет структуры Кдбпропсет (раздел 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="a573a-1943">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="a573a-1944">В следующей таблице перечислены свойства, которые являются частью \_ набора свойств DBPROPSET фсЦифрмврк \_ ext.</span><span class="sxs-lookup"><span data-stu-id="a573a-1944">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="a573a-1945">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1945">Value</span></span>                                  | <span data-ttu-id="a573a-1946">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1946">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-1947">DBPROP \_ CI \_ Catalog \_ имя 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-1947">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="a573a-1948">Указывает имя каталога или каталогов для запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-1948">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="a573a-1949">Значение должно быть VT \_ LPWSTR или \_ вектор VT \| \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="a573a-1949">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="a573a-1950">DBPROP \_ CI \_ включает \_ области 0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-1950">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="a573a-1951">Указывает один или несколько путей для включения в запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-1951">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="a573a-1952">Значение должно быть VT \_ LPWSTR или \_ вектор VT \| \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="a573a-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="a573a-1953">\_ \_ Флаги области CI DBPROP \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="a573a-1953">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="a573a-1954">Указывает, как должны обрабатываться пути, указанные в \_ \_ \_ свойстве областей DBPROP CI.</span><span class="sxs-lookup"><span data-stu-id="a573a-1954">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="a573a-1955">Значение должно быть VT \_ I4 или \_ вектор \| VT \_ i4.</span><span class="sxs-lookup"><span data-stu-id="a573a-1955">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="a573a-1956">\_ \_ Тип запроса DBPROP CI \_ 0x00000007</span><span class="sxs-lookup"><span data-stu-id="a573a-1956">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="a573a-1957">Указывает тип запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-1957">Specifies the type of query.</span></span> <span data-ttu-id="a573a-1958">Для Кдбколид должно быть задано значение DB \_ нуллид.</span><span class="sxs-lookup"><span data-stu-id="a573a-1958">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="a573a-1959">В следующей таблице перечислены флаги для \_ \_ \_ свойства Flags области DBPROP CI.</span><span class="sxs-lookup"><span data-stu-id="a573a-1959">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="a573a-1960">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1960">Value</span></span>                     | <span data-ttu-id="a573a-1961">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1961">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-1962">\_Глубокий запрос 0x01</span><span class="sxs-lookup"><span data-stu-id="a573a-1962">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="a573a-1963">Если задано значение, указывает, что файлы в каталоге области и во всех подкаталогах включены в результаты.</span><span class="sxs-lookup"><span data-stu-id="a573a-1963">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="a573a-1964">Если задано значение Clear, в результаты включаются только файлы в каталоге области.</span><span class="sxs-lookup"><span data-stu-id="a573a-1964">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="a573a-1965">НЕ следует сочетать с QUERY \_ Deep.</span><span class="sxs-lookup"><span data-stu-id="a573a-1965">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="a573a-1966">ЗАПРОС \_ виртуального \_ пути 0x02</span><span class="sxs-lookup"><span data-stu-id="a573a-1966">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="a573a-1967">Если задано значение, это указывает на то, что область является виртуальным путем.</span><span class="sxs-lookup"><span data-stu-id="a573a-1967">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="a573a-1968">Если флажок снят, указывает, что область является физическим каталогом.</span><span class="sxs-lookup"><span data-stu-id="a573a-1968">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="a573a-1969">В следующей таблице перечислены типы запросов для \_ свойства типа "запрос CI DBPROP" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a573a-1969">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="a573a-1970">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1970">Value</span></span>                     | <span data-ttu-id="a573a-1971">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1971">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-1972">Цинормал 0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-1972">CiNormal 0x00000000</span></span>       | <span data-ttu-id="a573a-1973">Обычный запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-1973">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="a573a-1974">Цивиртуалрутс 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-1974">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="a573a-1975">Запрос запрашивает список виртуальных корней каталога.</span><span class="sxs-lookup"><span data-stu-id="a573a-1975">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="a573a-1976">Для этого значения требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="a573a-1976">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="a573a-1977">Ципропертиес 0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-1977">CiProperties 0x00000003</span></span>   | <span data-ttu-id="a573a-1978">Запрос запрашивает список всех свойств, поддерживаемых службой индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-1978">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="a573a-1979">Циадминоп 0x00000004</span><span class="sxs-lookup"><span data-stu-id="a573a-1979">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="a573a-1980">Запрос является административной операцией.</span><span class="sxs-lookup"><span data-stu-id="a573a-1980">The query is an administrative operation.</span></span> <span data-ttu-id="a573a-1981">Для этого значения требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="a573a-1981">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="a573a-1982">В следующей таблице перечислены свойства, которые являются частью \_ набора свойств DBPROPSET куерекст.</span><span class="sxs-lookup"><span data-stu-id="a573a-1982">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="a573a-1983">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1983">Value</span></span>                                      | <span data-ttu-id="a573a-1984">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-1984">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-1985">DBPROP \_ усеконтентиндекс 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-1985">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="a573a-1986">Указывает, как служба индексирования предназначена для обработки запросов с высокой скоростью.</span><span class="sxs-lookup"><span data-stu-id="a573a-1986">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="a573a-1987">Значение должно быть логическим значением VT \_ .</span><span class="sxs-lookup"><span data-stu-id="a573a-1987">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="a573a-1988">Значение TRUE показывает, что серверу разрешено завершать эти запросы.</span><span class="sxs-lookup"><span data-stu-id="a573a-1988">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="a573a-1989">DBPROP \_ дефернониндекседтримминг 0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-1989">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="a573a-1990">Указывает, должна ли служба индексирования выполнять усечение результатов.</span><span class="sxs-lookup"><span data-stu-id="a573a-1990">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="a573a-1991">Если значение равно TRUE, то сервер должен выполнять усечение результатов таким образом, чтобы оптимизировать время отклика клиенту.</span><span class="sxs-lookup"><span data-stu-id="a573a-1991">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="a573a-1992">Значение должно быть логическим значением VT \_ .</span><span class="sxs-lookup"><span data-stu-id="a573a-1992">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="a573a-1993">DBPROP \_ усикстендеддбтипес 0x00000004</span><span class="sxs-lookup"><span data-stu-id="a573a-1993">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="a573a-1994">Указывает, поддерживает ли клиент \_ типы данных VT Vector.</span><span class="sxs-lookup"><span data-stu-id="a573a-1994">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="a573a-1995">Если значение — TRUE, клиент поддерживает \_ вектор VT; если значение равно false, то сервер должен преобразовать \_ векторные типы данных VT в \_ типы данных массива VT.</span><span class="sxs-lookup"><span data-stu-id="a573a-1995">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="a573a-1996">Значение должно быть логическим значением VT \_ .</span><span class="sxs-lookup"><span data-stu-id="a573a-1996">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="a573a-1997">DBPROP \_ фирстровс 0x00000007</span><span class="sxs-lookup"><span data-stu-id="a573a-1997">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="a573a-1998">Указывает, что строка соответствует возвращаемому значению.</span><span class="sxs-lookup"><span data-stu-id="a573a-1998">Indicates the row matches to return.</span></span> <span data-ttu-id="a573a-1999">Если значение равно TRUE, сервер должен возвращать первый набор совпадающих строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-1999">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="a573a-2000">Если значение равно FALSE, то должны возвращаться наиболее подходящие строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-2000">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="a573a-2001">Значение должно быть логическим значением VT \_ .</span><span class="sxs-lookup"><span data-stu-id="a573a-2001">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="a573a-2002">В следующей таблице перечислены свойства, которые являются частью \_ набора свойств DBPROPSET Цифрмврккоре \_ ext.</span><span class="sxs-lookup"><span data-stu-id="a573a-2002">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="a573a-2003">Значение/ДБПРОПИД</span><span class="sxs-lookup"><span data-stu-id="a573a-2003">Value / DBPROPID</span></span>                 | <span data-ttu-id="a573a-2004">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2004">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-2005">DBPROP \_ машины 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-2005">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="a573a-2006">Указывает имена компьютеров, на которых будет обрабатываться запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-2006">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="a573a-2007">Значение должно быть либо VT \_ BSTR, либо VT \_ \| . VT \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="a573a-2007">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="a573a-2008">\_0X00000003 DBPROP клиента \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="a573a-2008">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="a573a-2009">Задает константу подключения для службы индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-2009">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="a573a-2010">Значение должно быть \_ идентификатором CLSID VT, содержащим 0x2A4880706FD911D0A80800A0C906241A.</span><span class="sxs-lookup"><span data-stu-id="a573a-2010">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="a573a-2011">2.2.1.22 Кдбпропсет</span><span class="sxs-lookup"><span data-stu-id="a573a-2011">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="a573a-2012">Структура Кдбпропсет содержит набор свойств.</span><span class="sxs-lookup"><span data-stu-id="a573a-2012">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="a573a-2013">Обратите внимание, что первое поле имеет фиксированный размер, но может не быть согласовано со смещением, которое является 4-байтовым числом, кратным началу сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="a573a-2013">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="a573a-2014">Однако поле Кпропертиес будет выражаться таким образом, поэтому формат будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-2014">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="a573a-2015">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2015">0</span></span>

<span data-ttu-id="a573a-2016">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2016">1</span></span>

<span data-ttu-id="a573a-2017">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2017">2</span></span>

<span data-ttu-id="a573a-2018">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2018">3</span></span>

<span data-ttu-id="a573a-2019">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2019">4</span></span>

<span data-ttu-id="a573a-2020">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2020">5</span></span>

<span data-ttu-id="a573a-2021">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2021">6</span></span>

<span data-ttu-id="a573a-2022">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2022">7</span></span>

<span data-ttu-id="a573a-2023">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2023">8</span></span>

<span data-ttu-id="a573a-2024">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2024">9</span></span>

<span data-ttu-id="a573a-2025">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2025">1</span></span><br/> <span data-ttu-id="a573a-2026">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2026">0</span></span><br/>

<span data-ttu-id="a573a-2027">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2027">1</span></span>

<span data-ttu-id="a573a-2028">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2028">2</span></span>

<span data-ttu-id="a573a-2029">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2029">3</span></span>

<span data-ttu-id="a573a-2030">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2030">4</span></span>

<span data-ttu-id="a573a-2031">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2031">5</span></span>

<span data-ttu-id="a573a-2032">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2032">6</span></span>

<span data-ttu-id="a573a-2033">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2033">7</span></span>

<span data-ttu-id="a573a-2034">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2034">8</span></span>

<span data-ttu-id="a573a-2035">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2035">9</span></span>

<span data-ttu-id="a573a-2036">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2036">2</span></span><br/> <span data-ttu-id="a573a-2037">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2037">0</span></span><br/>

<span data-ttu-id="a573a-2038">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2038">1</span></span>

<span data-ttu-id="a573a-2039">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2039">2</span></span>

<span data-ttu-id="a573a-2040">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2040">3</span></span>

<span data-ttu-id="a573a-2041">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2041">4</span></span>

<span data-ttu-id="a573a-2042">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2042">5</span></span>

<span data-ttu-id="a573a-2043">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2043">6</span></span>

<span data-ttu-id="a573a-2044">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2044">7</span></span>

<span data-ttu-id="a573a-2045">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2045">8</span></span>

<span data-ttu-id="a573a-2046">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2046">9</span></span>

<span data-ttu-id="a573a-2047">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2047">3</span></span><br/> <span data-ttu-id="a573a-2048">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2048">0</span></span><br/>

<span data-ttu-id="a573a-2049">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2049">1</span></span>

<span data-ttu-id="a573a-2050">гуидпропертисет</span><span class="sxs-lookup"><span data-stu-id="a573a-2050">guidPropertySet</span></span>

<span data-ttu-id="a573a-2051">...</span><span class="sxs-lookup"><span data-stu-id="a573a-2051">...</span></span>

<span data-ttu-id="a573a-2052">...</span><span class="sxs-lookup"><span data-stu-id="a573a-2052">...</span></span>

<span data-ttu-id="a573a-2053">...</span><span class="sxs-lookup"><span data-stu-id="a573a-2053">...</span></span>

<span data-ttu-id="a573a-2054">...</span><span class="sxs-lookup"><span data-stu-id="a573a-2054">...</span></span>

<span data-ttu-id="a573a-2055">\_Заполнение (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-2055">\_padding (variable)</span></span>

<span data-ttu-id="a573a-2056">кпропертиес</span><span class="sxs-lookup"><span data-stu-id="a573a-2056">cProperties</span></span>

<span data-ttu-id="a573a-2057">Апропс (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-2057">aProps (variable)</span></span>



 

<span data-ttu-id="a573a-2058">**гуидпропертисет**: идентификатор GUID, определяющий набор свойств.</span><span class="sxs-lookup"><span data-stu-id="a573a-2058">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="a573a-2059">НЕОБХОДИМО задать двоичную форму, соответствующую одному из следующих значений (отображается в форме строкового представления), определяя набор свойств свойств, содержащихся в поле Апропс.</span><span class="sxs-lookup"><span data-stu-id="a573a-2059">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="a573a-2060">Значение/GUID</span><span class="sxs-lookup"><span data-stu-id="a573a-2060">Value / GUID</span></span>                                                                              | <span data-ttu-id="a573a-2061">Имя</span><span class="sxs-lookup"><span data-stu-id="a573a-2061">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="a573a-2062">DBPROPSET \_ фсЦифрмврк \_ ext</span><span class="sxs-lookup"><span data-stu-id="a573a-2062">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="a573a-2063">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="a573a-2063">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="a573a-2064">Набор свойств платформы индекса содержимого файловой системы</span><span class="sxs-lookup"><span data-stu-id="a573a-2064">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="a573a-2065">DBPROPSET \_ куерекст</span><span class="sxs-lookup"><span data-stu-id="a573a-2065">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="a573a-2066">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="a573a-2066">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="a573a-2067">Набор свойств расширения запроса</span><span class="sxs-lookup"><span data-stu-id="a573a-2067">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="a573a-2068">DBPROPSET \_ Цифрмврккоре \_ ext</span><span class="sxs-lookup"><span data-stu-id="a573a-2068">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="a573a-2069">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="a573a-2069">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="a573a-2070">Набор свойств Core платформы индекса содержимого</span><span class="sxs-lookup"><span data-stu-id="a573a-2070">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="a573a-2071">**\_ Заполнение**: это поле должно иметь длину от 0 до 3 байт.</span><span class="sxs-lookup"><span data-stu-id="a573a-2071">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="a573a-2072">Длина этого поля должна быть такой, что следующее поле начинается со смещения, кратного 4 байтам от начала сообщения, содержащего эту структуру.</span><span class="sxs-lookup"><span data-stu-id="a573a-2072">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="a573a-2073">Если это поле имеется (т. е. Длина не равно нулю), то значение, которое он содержит, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="a573a-2073">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="a573a-2074">Содержимое этого поля должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-2074">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="a573a-2075">**кпропертиес**: 32-разрядное целое число без знака, содержащее количество элементов в массиве апропс.</span><span class="sxs-lookup"><span data-stu-id="a573a-2075">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="a573a-2076">**апропс**: массив структур кдбпроп, как указано в разделе 0, содержащем свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-2076">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="a573a-2077">Структуры в массиве должны быть разделены от 0 до 3 байтов, так что каждая структура начинается со смещения, кратного 4 байтам от начала сообщения, содержащего этот массив.</span><span class="sxs-lookup"><span data-stu-id="a573a-2077">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="a573a-2078">Если заданы байты заполнения, то значение, которое они содержат, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="a573a-2078">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="a573a-2079">Содержимое байтов заполнения должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-2079">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="a573a-2080">2.2.1.23 Кпидмаппер</span><span class="sxs-lookup"><span data-stu-id="a573a-2080">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="a573a-2081">Структура Кпидмаппер содержит массив идентификаторов свойств, указывающих свойства, возвращаемые в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-2081">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="a573a-2082">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2082">0</span></span>

<span data-ttu-id="a573a-2083">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2083">1</span></span>

<span data-ttu-id="a573a-2084">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2084">2</span></span>

<span data-ttu-id="a573a-2085">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2085">3</span></span>

<span data-ttu-id="a573a-2086">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2086">4</span></span>

<span data-ttu-id="a573a-2087">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2087">5</span></span>

<span data-ttu-id="a573a-2088">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2088">6</span></span>

<span data-ttu-id="a573a-2089">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2089">7</span></span>

<span data-ttu-id="a573a-2090">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2090">8</span></span>

<span data-ttu-id="a573a-2091">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2091">9</span></span>

<span data-ttu-id="a573a-2092">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2092">1</span></span><br/> <span data-ttu-id="a573a-2093">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2093">0</span></span><br/>

<span data-ttu-id="a573a-2094">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2094">1</span></span>

<span data-ttu-id="a573a-2095">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2095">2</span></span>

<span data-ttu-id="a573a-2096">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2096">3</span></span>

<span data-ttu-id="a573a-2097">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2097">4</span></span>

<span data-ttu-id="a573a-2098">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2098">5</span></span>

<span data-ttu-id="a573a-2099">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2099">6</span></span>

<span data-ttu-id="a573a-2100">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2100">7</span></span>

<span data-ttu-id="a573a-2101">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2101">8</span></span>

<span data-ttu-id="a573a-2102">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2102">9</span></span>

<span data-ttu-id="a573a-2103">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2103">2</span></span><br/> <span data-ttu-id="a573a-2104">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2104">0</span></span><br/>

<span data-ttu-id="a573a-2105">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2105">1</span></span>

<span data-ttu-id="a573a-2106">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2106">2</span></span>

<span data-ttu-id="a573a-2107">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2107">3</span></span>

<span data-ttu-id="a573a-2108">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2108">4</span></span>

<span data-ttu-id="a573a-2109">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2109">5</span></span>

<span data-ttu-id="a573a-2110">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2110">6</span></span>

<span data-ttu-id="a573a-2111">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2111">7</span></span>

<span data-ttu-id="a573a-2112">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2112">8</span></span>

<span data-ttu-id="a573a-2113">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2113">9</span></span>

<span data-ttu-id="a573a-2114">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2114">3</span></span><br/> <span data-ttu-id="a573a-2115">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2115">0</span></span><br/>

<span data-ttu-id="a573a-2116">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2116">1</span></span>

<span data-ttu-id="a573a-2117">count</span><span class="sxs-lookup"><span data-stu-id="a573a-2117">count</span></span>

<span data-ttu-id="a573a-2118">апропспек</span><span class="sxs-lookup"><span data-stu-id="a573a-2118">aPropSpec</span></span>

<span data-ttu-id="a573a-2119">... перемен</span><span class="sxs-lookup"><span data-stu-id="a573a-2119">... (variable)</span></span>



 

<span data-ttu-id="a573a-2120">**Count**: 32-разрядное целое число без знака, содержащее количество элементов в массиве апропспек.</span><span class="sxs-lookup"><span data-stu-id="a573a-2120">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="a573a-2121">**апропспек**: массив структур кфуллпропспек, указывающих возвращаемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-2121">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="a573a-2122">Структуры в массиве должны быть разделены от 0 до 3 байтов с отступом таким, что каждая структура имеет 4-байтовое выравнивание от начала сообщения.</span><span class="sxs-lookup"><span data-stu-id="a573a-2122">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="a573a-2123">Такое заполнение байтов может быть любым произвольным значением и не должно учитываться при получении.</span><span class="sxs-lookup"><span data-stu-id="a573a-2123">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="a573a-2124">2.2.1.24 Кровсикат</span><span class="sxs-lookup"><span data-stu-id="a573a-2124">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="a573a-2125">Структура Кровсикат содержит смещение для получения строк в сообщении Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-2125">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="a573a-2126">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2126">0</span></span>

<span data-ttu-id="a573a-2127">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2127">1</span></span>

<span data-ttu-id="a573a-2128">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2128">2</span></span>

<span data-ttu-id="a573a-2129">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2129">3</span></span>

<span data-ttu-id="a573a-2130">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2130">4</span></span>

<span data-ttu-id="a573a-2131">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2131">5</span></span>

<span data-ttu-id="a573a-2132">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2132">6</span></span>

<span data-ttu-id="a573a-2133">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2133">7</span></span>

<span data-ttu-id="a573a-2134">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2134">8</span></span>

<span data-ttu-id="a573a-2135">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2135">9</span></span>

<span data-ttu-id="a573a-2136">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2136">1</span></span><br/> <span data-ttu-id="a573a-2137">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2137">0</span></span><br/>

<span data-ttu-id="a573a-2138">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2138">1</span></span>

<span data-ttu-id="a573a-2139">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2139">2</span></span>

<span data-ttu-id="a573a-2140">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2140">3</span></span>

<span data-ttu-id="a573a-2141">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2141">4</span></span>

<span data-ttu-id="a573a-2142">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2142">5</span></span>

<span data-ttu-id="a573a-2143">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2143">6</span></span>

<span data-ttu-id="a573a-2144">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2144">7</span></span>

<span data-ttu-id="a573a-2145">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2145">8</span></span>

<span data-ttu-id="a573a-2146">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2146">9</span></span>

<span data-ttu-id="a573a-2147">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2147">2</span></span><br/> <span data-ttu-id="a573a-2148">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2148">0</span></span><br/>

<span data-ttu-id="a573a-2149">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2149">1</span></span>

<span data-ttu-id="a573a-2150">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2150">2</span></span>

<span data-ttu-id="a573a-2151">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2151">3</span></span>

<span data-ttu-id="a573a-2152">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2152">4</span></span>

<span data-ttu-id="a573a-2153">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2153">5</span></span>

<span data-ttu-id="a573a-2154">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2154">6</span></span>

<span data-ttu-id="a573a-2155">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2155">7</span></span>

<span data-ttu-id="a573a-2156">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2156">8</span></span>

<span data-ttu-id="a573a-2157">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2157">9</span></span>

<span data-ttu-id="a573a-2158">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2158">3</span></span><br/> <span data-ttu-id="a573a-2159">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2159">0</span></span><br/>

<span data-ttu-id="a573a-2160">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2160">1</span></span>

<span data-ttu-id="a573a-2161">\_хрегион</span><span class="sxs-lookup"><span data-stu-id="a573a-2161">\_hRegion</span></span>

<span data-ttu-id="a573a-2162">\_кскип</span><span class="sxs-lookup"><span data-stu-id="a573a-2162">\_cskip</span></span>

<span data-ttu-id="a573a-2163">\_бмкоффсет</span><span class="sxs-lookup"><span data-stu-id="a573a-2163">\_bmkOffset</span></span>



 

<span data-ttu-id="a573a-2164">**\_ хрегион**: необходимо задать значение 0x00000000, и оно должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-2164">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="a573a-2165">**\_ кскип**: 32-битовое целое число без знака, содержащее количество строк для пропуска в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-2165">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="a573a-2166">**\_ бмкоффсет**: 32-разрядное значение, представляющее маркер **закладки** , указывающий начальную точку, с которой следует пропускать число строк, указанное в \_ кскип, перед началом извлечения.</span><span class="sxs-lookup"><span data-stu-id="a573a-2166">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="a573a-2167">2.2.1.25 Кровсикатратио</span><span class="sxs-lookup"><span data-stu-id="a573a-2167">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="a573a-2168">Структура Кровсикатратио определяет точку, с которой начинается извлечение сообщения Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-2168">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="a573a-2169">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2169">0</span></span>

<span data-ttu-id="a573a-2170">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2170">1</span></span>

<span data-ttu-id="a573a-2171">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2171">2</span></span>

<span data-ttu-id="a573a-2172">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2172">3</span></span>

<span data-ttu-id="a573a-2173">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2173">4</span></span>

<span data-ttu-id="a573a-2174">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2174">5</span></span>

<span data-ttu-id="a573a-2175">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2175">6</span></span>

<span data-ttu-id="a573a-2176">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2176">7</span></span>

<span data-ttu-id="a573a-2177">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2177">8</span></span>

<span data-ttu-id="a573a-2178">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2178">9</span></span>

<span data-ttu-id="a573a-2179">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2179">1</span></span><br/> <span data-ttu-id="a573a-2180">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2180">0</span></span><br/>

<span data-ttu-id="a573a-2181">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2181">1</span></span>

<span data-ttu-id="a573a-2182">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2182">2</span></span>

<span data-ttu-id="a573a-2183">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2183">3</span></span>

<span data-ttu-id="a573a-2184">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2184">4</span></span>

<span data-ttu-id="a573a-2185">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2185">5</span></span>

<span data-ttu-id="a573a-2186">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2186">6</span></span>

<span data-ttu-id="a573a-2187">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2187">7</span></span>

<span data-ttu-id="a573a-2188">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2188">8</span></span>

<span data-ttu-id="a573a-2189">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2189">9</span></span>

<span data-ttu-id="a573a-2190">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2190">2</span></span><br/> <span data-ttu-id="a573a-2191">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2191">0</span></span><br/>

<span data-ttu-id="a573a-2192">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2192">1</span></span>

<span data-ttu-id="a573a-2193">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2193">2</span></span>

<span data-ttu-id="a573a-2194">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2194">3</span></span>

<span data-ttu-id="a573a-2195">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2195">4</span></span>

<span data-ttu-id="a573a-2196">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2196">5</span></span>

<span data-ttu-id="a573a-2197">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2197">6</span></span>

<span data-ttu-id="a573a-2198">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2198">7</span></span>

<span data-ttu-id="a573a-2199">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2199">8</span></span>

<span data-ttu-id="a573a-2200">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2200">9</span></span>

<span data-ttu-id="a573a-2201">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2201">3</span></span><br/> <span data-ttu-id="a573a-2202">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2202">0</span></span><br/>

<span data-ttu-id="a573a-2203">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2203">1</span></span>

<span data-ttu-id="a573a-2204">Цитблчапт</span><span class="sxs-lookup"><span data-stu-id="a573a-2204">CiTblChapt</span></span>

<span data-ttu-id="a573a-2205">\_хрегион</span><span class="sxs-lookup"><span data-stu-id="a573a-2205">\_hRegion</span></span>

<span data-ttu-id="a573a-2206">\_улнумератор</span><span class="sxs-lookup"><span data-stu-id="a573a-2206">\_ulNumerator</span></span>

<span data-ttu-id="a573a-2207">\_улденоминатор</span><span class="sxs-lookup"><span data-stu-id="a573a-2207">\_ulDenominator</span></span>



 

<span data-ttu-id="a573a-2208">**Цитблчапт**: 32-битовое целое число без знака, указывающее главу набора строк, из которой нужно получить строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-2208">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="a573a-2209">**\_ хрегион**: необходимо задать значение 0x00000000, и оно должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-2209">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="a573a-2210">**\_ улнумератор**: 32-разрядное целое число без знака, представляющее числитель количества строк в главе, с которых начинается извлечение.</span><span class="sxs-lookup"><span data-stu-id="a573a-2210">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="a573a-2211">**\_ улденоминатор**: 32-разрядное целое число без знака, представляющее знаменатель отношения количества строк в главе, с которых начинается извлечение.</span><span class="sxs-lookup"><span data-stu-id="a573a-2211">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="a573a-2212">ДОЛЖНО быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="a573a-2212">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="a573a-2213">2.2.1.26 Кровсикбибукмарк</span><span class="sxs-lookup"><span data-stu-id="a573a-2213">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="a573a-2214">Структура Кровсикбибукмарк определяет закладки, из которых начинается получение строк для сообщения Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-2214">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="a573a-2215">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2215">0</span></span>

<span data-ttu-id="a573a-2216">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2216">1</span></span>

<span data-ttu-id="a573a-2217">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2217">2</span></span>

<span data-ttu-id="a573a-2218">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2218">3</span></span>

<span data-ttu-id="a573a-2219">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2219">4</span></span>

<span data-ttu-id="a573a-2220">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2220">5</span></span>

<span data-ttu-id="a573a-2221">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2221">6</span></span>

<span data-ttu-id="a573a-2222">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2222">7</span></span>

<span data-ttu-id="a573a-2223">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2223">8</span></span>

<span data-ttu-id="a573a-2224">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2224">9</span></span>

<span data-ttu-id="a573a-2225">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2225">1</span></span><br/> <span data-ttu-id="a573a-2226">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2226">0</span></span><br/>

<span data-ttu-id="a573a-2227">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2227">1</span></span>

<span data-ttu-id="a573a-2228">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2228">2</span></span>

<span data-ttu-id="a573a-2229">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2229">3</span></span>

<span data-ttu-id="a573a-2230">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2230">4</span></span>

<span data-ttu-id="a573a-2231">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2231">5</span></span>

<span data-ttu-id="a573a-2232">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2232">6</span></span>

<span data-ttu-id="a573a-2233">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2233">7</span></span>

<span data-ttu-id="a573a-2234">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2234">8</span></span>

<span data-ttu-id="a573a-2235">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2235">9</span></span>

<span data-ttu-id="a573a-2236">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2236">2</span></span><br/> <span data-ttu-id="a573a-2237">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2237">0</span></span><br/>

<span data-ttu-id="a573a-2238">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2238">1</span></span>

<span data-ttu-id="a573a-2239">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2239">2</span></span>

<span data-ttu-id="a573a-2240">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2240">3</span></span>

<span data-ttu-id="a573a-2241">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2241">4</span></span>

<span data-ttu-id="a573a-2242">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2242">5</span></span>

<span data-ttu-id="a573a-2243">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2243">6</span></span>

<span data-ttu-id="a573a-2244">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2244">7</span></span>

<span data-ttu-id="a573a-2245">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2245">8</span></span>

<span data-ttu-id="a573a-2246">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2246">9</span></span>

<span data-ttu-id="a573a-2247">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2247">3</span></span><br/> <span data-ttu-id="a573a-2248">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2248">0</span></span><br/>

<span data-ttu-id="a573a-2249">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2249">1</span></span>

<span data-ttu-id="a573a-2250">\_хрегион</span><span class="sxs-lookup"><span data-stu-id="a573a-2250">\_hRegion</span></span>

<span data-ttu-id="a573a-2251">\_кбукмаркс</span><span class="sxs-lookup"><span data-stu-id="a573a-2251">\_cBookmarks</span></span>

<span data-ttu-id="a573a-2252">\_максрет</span><span class="sxs-lookup"><span data-stu-id="a573a-2252">\_maxRet</span></span>

<span data-ttu-id="a573a-2253">\_квалидрет</span><span class="sxs-lookup"><span data-stu-id="a573a-2253">\_cValidRet</span></span>

<span data-ttu-id="a573a-2254">\_Абукмаркс (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-2254">\_aBookmarks (variable)</span></span>

<span data-ttu-id="a573a-2255">\_Аскрет (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-2255">\_ascRet (variable)</span></span>



 

<span data-ttu-id="a573a-2256">**\_ хрегион**: необходимо задать значение 0x00000000, и оно должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-2256">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="a573a-2257">**\_ кбукмаркс**: 32-разрядное целое число без знака, представляющее число элементов в \_ массиве абукмаркс.</span><span class="sxs-lookup"><span data-stu-id="a573a-2257">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="a573a-2258">**\_ максрет**: 32-разрядное целое число без знака, представляющее число элементов в \_ массиве аскрет.</span><span class="sxs-lookup"><span data-stu-id="a573a-2258">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="a573a-2259">**\_ квалидрет**: 32-разрядное целое число без знака, представляющее число \_ допустимых элементов в массиве аскрет.</span><span class="sxs-lookup"><span data-stu-id="a573a-2259">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="a573a-2260">В массиве определены допустимые элементы, тогда как недопустимые элементы не определены.</span><span class="sxs-lookup"><span data-stu-id="a573a-2260">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="a573a-2261">**\_ абукмаркс**: массив дескрипторов закладок (каждый из которых представлен 4 байта), полученный из сообщения кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-2261">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="a573a-2262">**\_ аскрет**: массив значений HRESULT.</span><span class="sxs-lookup"><span data-stu-id="a573a-2262">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="a573a-2263">Когда Кровсикбибукмарк отправляется как часть запроса Кпмжетровсин, число записей в массиве должно быть равно \_ кбукмаркс.</span><span class="sxs-lookup"><span data-stu-id="a573a-2263">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="a573a-2264">При отправке клиентом значения должны быть равны нулю, а сервер должен игнорировать содержимое массива.</span><span class="sxs-lookup"><span data-stu-id="a573a-2264">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="a573a-2265">При отправке сервером (в составе сообщения Кпмжетровсаут) значения в массиве указывают состояние результата для каждого извлечения строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-2265">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="a573a-2266">2.2.1.27 Кровсикнекст</span><span class="sxs-lookup"><span data-stu-id="a573a-2266">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="a573a-2267">Структура Кровсикнекст содержит число строк, которые необходимо пропустить в сообщении Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-2267">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="a573a-2268">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2268">0</span></span>

<span data-ttu-id="a573a-2269">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2269">1</span></span>

<span data-ttu-id="a573a-2270">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2270">2</span></span>

<span data-ttu-id="a573a-2271">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2271">3</span></span>

<span data-ttu-id="a573a-2272">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2272">4</span></span>

<span data-ttu-id="a573a-2273">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2273">5</span></span>

<span data-ttu-id="a573a-2274">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2274">6</span></span>

<span data-ttu-id="a573a-2275">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2275">7</span></span>

<span data-ttu-id="a573a-2276">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2276">8</span></span>

<span data-ttu-id="a573a-2277">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2277">9</span></span>

<span data-ttu-id="a573a-2278">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2278">1</span></span><br/> <span data-ttu-id="a573a-2279">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2279">0</span></span><br/>

<span data-ttu-id="a573a-2280">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2280">1</span></span>

<span data-ttu-id="a573a-2281">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2281">2</span></span>

<span data-ttu-id="a573a-2282">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2282">3</span></span>

<span data-ttu-id="a573a-2283">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2283">4</span></span>

<span data-ttu-id="a573a-2284">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2284">5</span></span>

<span data-ttu-id="a573a-2285">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2285">6</span></span>

<span data-ttu-id="a573a-2286">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2286">7</span></span>

<span data-ttu-id="a573a-2287">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2287">8</span></span>

<span data-ttu-id="a573a-2288">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2288">9</span></span>

<span data-ttu-id="a573a-2289">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2289">2</span></span><br/> <span data-ttu-id="a573a-2290">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2290">0</span></span><br/>

<span data-ttu-id="a573a-2291">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2291">1</span></span>

<span data-ttu-id="a573a-2292">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2292">2</span></span>

<span data-ttu-id="a573a-2293">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2293">3</span></span>

<span data-ttu-id="a573a-2294">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2294">4</span></span>

<span data-ttu-id="a573a-2295">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2295">5</span></span>

<span data-ttu-id="a573a-2296">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2296">6</span></span>

<span data-ttu-id="a573a-2297">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2297">7</span></span>

<span data-ttu-id="a573a-2298">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2298">8</span></span>

<span data-ttu-id="a573a-2299">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2299">9</span></span>

<span data-ttu-id="a573a-2300">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2300">3</span></span><br/> <span data-ttu-id="a573a-2301">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2301">0</span></span><br/>

<span data-ttu-id="a573a-2302">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2302">1</span></span>

<span data-ttu-id="a573a-2303">Цитблчапт</span><span class="sxs-lookup"><span data-stu-id="a573a-2303">CiTblChapt</span></span>

<span data-ttu-id="a573a-2304">\_хрегион</span><span class="sxs-lookup"><span data-stu-id="a573a-2304">\_hRegion</span></span>

<span data-ttu-id="a573a-2305">\_кскип</span><span class="sxs-lookup"><span data-stu-id="a573a-2305">\_cskip</span></span>



 

<span data-ttu-id="a573a-2306">**Цитблчапт**: 32-разрядное целое число без знака, указывающее главу набора строк, из которой нужно получить строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-2306">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="a573a-2307">**\_ хрегион**: необходимо задать значение 0x00000000, и оно должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-2307">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="a573a-2308">**\_ кскип**: 32-разрядное целое число без знака, представляющее число строк для пропуска в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-2308">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="a573a-2309">2.2.1.28 Кровсетпропертиес</span><span class="sxs-lookup"><span data-stu-id="a573a-2309">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="a573a-2310">Структура Кровсетпропертиес содержит сведения о конфигурации для запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-2310">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="a573a-2311">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2311">0</span></span>

<span data-ttu-id="a573a-2312">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2312">1</span></span>

<span data-ttu-id="a573a-2313">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2313">2</span></span>

<span data-ttu-id="a573a-2314">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2314">3</span></span>

<span data-ttu-id="a573a-2315">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2315">4</span></span>

<span data-ttu-id="a573a-2316">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2316">5</span></span>

<span data-ttu-id="a573a-2317">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2317">6</span></span>

<span data-ttu-id="a573a-2318">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2318">7</span></span>

<span data-ttu-id="a573a-2319">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2319">8</span></span>

<span data-ttu-id="a573a-2320">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2320">9</span></span>

<span data-ttu-id="a573a-2321">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2321">1</span></span><br/> <span data-ttu-id="a573a-2322">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2322">0</span></span><br/>

<span data-ttu-id="a573a-2323">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2323">1</span></span>

<span data-ttu-id="a573a-2324">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2324">2</span></span>

<span data-ttu-id="a573a-2325">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2325">3</span></span>

<span data-ttu-id="a573a-2326">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2326">4</span></span>

<span data-ttu-id="a573a-2327">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2327">5</span></span>

<span data-ttu-id="a573a-2328">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2328">6</span></span>

<span data-ttu-id="a573a-2329">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2329">7</span></span>

<span data-ttu-id="a573a-2330">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2330">8</span></span>

<span data-ttu-id="a573a-2331">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2331">9</span></span>

<span data-ttu-id="a573a-2332">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2332">2</span></span><br/> <span data-ttu-id="a573a-2333">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2333">0</span></span><br/>

<span data-ttu-id="a573a-2334">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2334">1</span></span>

<span data-ttu-id="a573a-2335">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2335">2</span></span>

<span data-ttu-id="a573a-2336">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2336">3</span></span>

<span data-ttu-id="a573a-2337">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2337">4</span></span>

<span data-ttu-id="a573a-2338">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2338">5</span></span>

<span data-ttu-id="a573a-2339">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2339">6</span></span>

<span data-ttu-id="a573a-2340">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2340">7</span></span>

<span data-ttu-id="a573a-2341">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2341">8</span></span>

<span data-ttu-id="a573a-2342">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2342">9</span></span>

<span data-ttu-id="a573a-2343">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2343">3</span></span><br/> <span data-ttu-id="a573a-2344">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2344">0</span></span><br/>

<span data-ttu-id="a573a-2345">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2345">1</span></span>

<span data-ttu-id="a573a-2346">\_убулеаноптионс</span><span class="sxs-lookup"><span data-stu-id="a573a-2346">\_uBooleanOptions</span></span>

<span data-ttu-id="a573a-2347">\_улмаксопенровс</span><span class="sxs-lookup"><span data-stu-id="a573a-2347">\_ulMaxOpenRows</span></span>

<span data-ttu-id="a573a-2348">\_улмеморюсаже</span><span class="sxs-lookup"><span data-stu-id="a573a-2348">\_ulMemoryUsage</span></span>

<span data-ttu-id="a573a-2349">\_кмаксресултс</span><span class="sxs-lookup"><span data-stu-id="a573a-2349">\_cMaxResults</span></span>

<span data-ttu-id="a573a-2350">\_ккмдтимеаут</span><span class="sxs-lookup"><span data-stu-id="a573a-2350">\_cCmdTimeout</span></span>



 

<span data-ttu-id="a573a-2351">**\_ убулеаноптионс**: наименее значимые 3 бита этого поля должны содержать одно из следующих трех значений:</span><span class="sxs-lookup"><span data-stu-id="a573a-2351">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="a573a-2352">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2352">Value</span></span>                  | <span data-ttu-id="a573a-2353">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2353">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a573a-2354">Есекуентиал 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-2354">eSequential 0x00000001</span></span> | <span data-ttu-id="a573a-2355">Курсор можно переместить только вперед.</span><span class="sxs-lookup"><span data-stu-id="a573a-2355">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="a573a-2356">Елокатабле 0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-2356">eLocatable 0x00000003</span></span>  | <span data-ttu-id="a573a-2357">Курсор можно переместить в любую позицию.</span><span class="sxs-lookup"><span data-stu-id="a573a-2357">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="a573a-2358">Ескроллабле 0x00000007</span><span class="sxs-lookup"><span data-stu-id="a573a-2358">eScrollable 0x00000007</span></span> | <span data-ttu-id="a573a-2359">Курсор можно переместить в любую позицию и получить в любом направлении.</span><span class="sxs-lookup"><span data-stu-id="a573a-2359">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="a573a-2360">Остальные биты могут быть либо понятны, либо установлены в любое сочетание следующих логических значений или совместно.</span><span class="sxs-lookup"><span data-stu-id="a573a-2360">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="a573a-2361">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2361">Value</span></span>                     | <span data-ttu-id="a573a-2362">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2362">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-2363">Еасинчронаус 0x00000008</span><span class="sxs-lookup"><span data-stu-id="a573a-2363">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="a573a-2364">Клиент не будет ждать завершения выполнения.</span><span class="sxs-lookup"><span data-stu-id="a573a-2364">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="a573a-2365">Ефирстровс 0x00000080</span><span class="sxs-lookup"><span data-stu-id="a573a-2365">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="a573a-2366">Возвращение первых обнаруженных строк, а не наиболее подходящих соответствий.</span><span class="sxs-lookup"><span data-stu-id="a573a-2366">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="a573a-2367">Ехолдровс 0x00000200</span><span class="sxs-lookup"><span data-stu-id="a573a-2367">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="a573a-2368">Сервер не должен отбрасывать строки до тех пор, пока клиент не завершит запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-2368">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="a573a-2369">Ечаптеред 0x00000800</span><span class="sxs-lookup"><span data-stu-id="a573a-2369">eChaptered 0x00000800</span></span>     | <span data-ttu-id="a573a-2370">Набор строк поддерживает главы.</span><span class="sxs-lookup"><span data-stu-id="a573a-2370">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="a573a-2371">ЕусеЦи 0x00001000</span><span class="sxs-lookup"><span data-stu-id="a573a-2371">eUseCI 0x00001000</span></span>         | <span data-ttu-id="a573a-2372">Отвечайте на запрос только из индекса, а не из файловой системы.</span><span class="sxs-lookup"><span data-stu-id="a573a-2372">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="a573a-2373">Едефертримминг 0x00002000</span><span class="sxs-lookup"><span data-stu-id="a573a-2373">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="a573a-2374">Служба индексирования позволяет оптимизировать время отклика клиенту при удалении результатов.</span><span class="sxs-lookup"><span data-stu-id="a573a-2374">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="a573a-2375">**\_ улмаксопенровс**: 32-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-2375">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="a573a-2376">Необходимо задать значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-2376">Must be set to 0x00000000.</span></span> <span data-ttu-id="a573a-2377">Не используется и должен игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-2377">Not used and MUST be ignored.</span></span>

<span data-ttu-id="a573a-2378">**\_ улмеморюсаже**: 32-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-2378">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="a573a-2379">Необходимо задать значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="a573a-2380">Не используется и должен игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="a573a-2381">**\_ кмаксресултс**: 32-разрядное целое число без знака, указывающее максимальное количество строк, возвращаемых для запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-2381">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="a573a-2382">**\_ ккмдтимеаут**: 32-разрядное целое число без знака, определяющее время ожидания запроса (в секундах) и автоматическое завершение, считая от момента начала выполнения запроса на сервере.</span><span class="sxs-lookup"><span data-stu-id="a573a-2382">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="a573a-2383">Значение 0x00000000 означает, что время ожидания запроса не истекло.</span><span class="sxs-lookup"><span data-stu-id="a573a-2383">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="a573a-2384">2.2.1.29 Кроввариант</span><span class="sxs-lookup"><span data-stu-id="a573a-2384">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="a573a-2385">Структура Кроввариант содержит часть фиксированного размера типа данных переменной длины, которая хранится в сообщении Кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-2385">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="a573a-2386">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2386">0</span></span>

<span data-ttu-id="a573a-2387">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2387">1</span></span>

<span data-ttu-id="a573a-2388">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2388">2</span></span>

<span data-ttu-id="a573a-2389">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2389">3</span></span>

<span data-ttu-id="a573a-2390">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2390">4</span></span>

<span data-ttu-id="a573a-2391">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2391">5</span></span>

<span data-ttu-id="a573a-2392">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2392">6</span></span>

<span data-ttu-id="a573a-2393">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2393">7</span></span>

<span data-ttu-id="a573a-2394">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2394">8</span></span>

<span data-ttu-id="a573a-2395">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2395">9</span></span>

<span data-ttu-id="a573a-2396">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2396">1</span></span><br/> <span data-ttu-id="a573a-2397">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2397">0</span></span><br/>

<span data-ttu-id="a573a-2398">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2398">1</span></span>

<span data-ttu-id="a573a-2399">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2399">2</span></span>

<span data-ttu-id="a573a-2400">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2400">3</span></span>

<span data-ttu-id="a573a-2401">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2401">4</span></span>

<span data-ttu-id="a573a-2402">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2402">5</span></span>

<span data-ttu-id="a573a-2403">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2403">6</span></span>

<span data-ttu-id="a573a-2404">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2404">7</span></span>

<span data-ttu-id="a573a-2405">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2405">8</span></span>

<span data-ttu-id="a573a-2406">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2406">9</span></span>

<span data-ttu-id="a573a-2407">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2407">2</span></span><br/> <span data-ttu-id="a573a-2408">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2408">0</span></span><br/>

<span data-ttu-id="a573a-2409">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2409">1</span></span>

<span data-ttu-id="a573a-2410">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2410">2</span></span>

<span data-ttu-id="a573a-2411">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2411">3</span></span>

<span data-ttu-id="a573a-2412">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2412">4</span></span>

<span data-ttu-id="a573a-2413">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2413">5</span></span>

<span data-ttu-id="a573a-2414">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2414">6</span></span>

<span data-ttu-id="a573a-2415">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2415">7</span></span>

<span data-ttu-id="a573a-2416">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2416">8</span></span>

<span data-ttu-id="a573a-2417">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2417">9</span></span>

<span data-ttu-id="a573a-2418">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2418">3</span></span><br/> <span data-ttu-id="a573a-2419">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2419">0</span></span><br/>

<span data-ttu-id="a573a-2420">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2420">1</span></span>

<span data-ttu-id="a573a-2421">втипе</span><span class="sxs-lookup"><span data-stu-id="a573a-2421">vType</span></span>

<span data-ttu-id="a573a-2422">reserved1</span><span class="sxs-lookup"><span data-stu-id="a573a-2422">reserved1</span></span>

<span data-ttu-id="a573a-2423">reserved2</span><span class="sxs-lookup"><span data-stu-id="a573a-2423">reserved2</span></span>

<span data-ttu-id="a573a-2424">Offset (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-2424">Offset (optional)</span></span>



 

<span data-ttu-id="a573a-2425">**втипе**: признак типа, указывающий тип управляемое vValue.</span><span class="sxs-lookup"><span data-stu-id="a573a-2425">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="a573a-2426">Это должно быть одно из значений VARENUM, указанных в разделе 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="a573a-2426">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="a573a-2427">**reserved1**: не используется.</span><span class="sxs-lookup"><span data-stu-id="a573a-2427">**reserved1**: Not used.</span></span> <span data-ttu-id="a573a-2428">В качестве значения можно задать любое произвольное значение. оно должно игнорироваться при получении.</span><span class="sxs-lookup"><span data-stu-id="a573a-2428">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="a573a-2429">**reserved2**: не используется.</span><span class="sxs-lookup"><span data-stu-id="a573a-2429">**reserved2**: Not used.</span></span> <span data-ttu-id="a573a-2430">В качестве значения можно задать любое произвольное значение. оно должно игнорироваться при получении.</span><span class="sxs-lookup"><span data-stu-id="a573a-2430">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="a573a-2431">**Offset**: смещение данных переменной длины (например, строка).</span><span class="sxs-lookup"><span data-stu-id="a573a-2431">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="a573a-2432">Это должно быть 32-разрядное значение (4 байта), если используется 32-разрядное смещение (согласно правилам в разделе 2.2.3.16), или значение 64-Byte (8 байт), если используется 64-разрядное смещение.</span><span class="sxs-lookup"><span data-stu-id="a573a-2432">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="a573a-2433">2.2.1.30 Ксортсет</span><span class="sxs-lookup"><span data-stu-id="a573a-2433">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="a573a-2434">Структура Ксортсет содержит порядок сортировки запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-2434">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="a573a-2435">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2435">0</span></span>

<span data-ttu-id="a573a-2436">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2436">1</span></span>

<span data-ttu-id="a573a-2437">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2437">2</span></span>

<span data-ttu-id="a573a-2438">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2438">3</span></span>

<span data-ttu-id="a573a-2439">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2439">4</span></span>

<span data-ttu-id="a573a-2440">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2440">5</span></span>

<span data-ttu-id="a573a-2441">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2441">6</span></span>

<span data-ttu-id="a573a-2442">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2442">7</span></span>

<span data-ttu-id="a573a-2443">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2443">8</span></span>

<span data-ttu-id="a573a-2444">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2444">9</span></span>

<span data-ttu-id="a573a-2445">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2445">1</span></span><br/> <span data-ttu-id="a573a-2446">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2446">0</span></span><br/>

<span data-ttu-id="a573a-2447">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2447">1</span></span>

<span data-ttu-id="a573a-2448">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2448">2</span></span>

<span data-ttu-id="a573a-2449">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2449">3</span></span>

<span data-ttu-id="a573a-2450">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2450">4</span></span>

<span data-ttu-id="a573a-2451">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2451">5</span></span>

<span data-ttu-id="a573a-2452">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2452">6</span></span>

<span data-ttu-id="a573a-2453">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2453">7</span></span>

<span data-ttu-id="a573a-2454">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2454">8</span></span>

<span data-ttu-id="a573a-2455">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2455">9</span></span>

<span data-ttu-id="a573a-2456">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2456">2</span></span><br/> <span data-ttu-id="a573a-2457">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2457">0</span></span><br/>

<span data-ttu-id="a573a-2458">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2458">1</span></span>

<span data-ttu-id="a573a-2459">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2459">2</span></span>

<span data-ttu-id="a573a-2460">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2460">3</span></span>

<span data-ttu-id="a573a-2461">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2461">4</span></span>

<span data-ttu-id="a573a-2462">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2462">5</span></span>

<span data-ttu-id="a573a-2463">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2463">6</span></span>

<span data-ttu-id="a573a-2464">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2464">7</span></span>

<span data-ttu-id="a573a-2465">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2465">8</span></span>

<span data-ttu-id="a573a-2466">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2466">9</span></span>

<span data-ttu-id="a573a-2467">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2467">3</span></span><br/> <span data-ttu-id="a573a-2468">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2468">0</span></span><br/>

<span data-ttu-id="a573a-2469">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2469">1</span></span>

<span data-ttu-id="a573a-2470">Count</span><span class="sxs-lookup"><span data-stu-id="a573a-2470">Count</span></span>

<span data-ttu-id="a573a-2471">Сортаррай (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-2471">sortArray (variable)</span></span>



 

<span data-ttu-id="a573a-2472">**Count**: 32-разрядное целое число без знака, задающее число элементов в сортаррай.</span><span class="sxs-lookup"><span data-stu-id="a573a-2472">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="a573a-2473">**сортаррай**: массив структур ксорт, описывающих порядок сортировки результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-2473">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="a573a-2474">Структуры в массиве должны быть разделены от 0 до 3 байтов с отступом таким, что каждая структура имеет 4-байтовое выравнивание от начала сообщения.</span><span class="sxs-lookup"><span data-stu-id="a573a-2474">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="a573a-2475">Такое заполнение байтов может быть любым произвольным значением и не должно учитываться при получении.</span><span class="sxs-lookup"><span data-stu-id="a573a-2475">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="a573a-2476">2.2.1.31 Ктаблеколумн</span><span class="sxs-lookup"><span data-stu-id="a573a-2476">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="a573a-2477">Структура Ктаблеколумн содержит столбец сообщения Кпмсетбиндингсин</span><span class="sxs-lookup"><span data-stu-id="a573a-2477">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="a573a-2478">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2478">0</span></span>

<span data-ttu-id="a573a-2479">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2479">1</span></span>

<span data-ttu-id="a573a-2480">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2480">2</span></span>

<span data-ttu-id="a573a-2481">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2481">3</span></span>

<span data-ttu-id="a573a-2482">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2482">4</span></span>

<span data-ttu-id="a573a-2483">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2483">5</span></span>

<span data-ttu-id="a573a-2484">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2484">6</span></span>

<span data-ttu-id="a573a-2485">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2485">7</span></span>

<span data-ttu-id="a573a-2486">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2486">8</span></span>

<span data-ttu-id="a573a-2487">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2487">9</span></span>

<span data-ttu-id="a573a-2488">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2488">1</span></span><br/> <span data-ttu-id="a573a-2489">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2489">0</span></span><br/>

<span data-ttu-id="a573a-2490">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2490">1</span></span>

<span data-ttu-id="a573a-2491">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2491">2</span></span>

<span data-ttu-id="a573a-2492">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2492">3</span></span>

<span data-ttu-id="a573a-2493">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2493">4</span></span>

<span data-ttu-id="a573a-2494">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2494">5</span></span>

<span data-ttu-id="a573a-2495">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2495">6</span></span>

<span data-ttu-id="a573a-2496">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2496">7</span></span>

<span data-ttu-id="a573a-2497">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2497">8</span></span>

<span data-ttu-id="a573a-2498">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2498">9</span></span>

<span data-ttu-id="a573a-2499">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2499">2</span></span><br/> <span data-ttu-id="a573a-2500">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2500">0</span></span><br/>

<span data-ttu-id="a573a-2501">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2501">1</span></span>

<span data-ttu-id="a573a-2502">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2502">2</span></span>

<span data-ttu-id="a573a-2503">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2503">3</span></span>

<span data-ttu-id="a573a-2504">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2504">4</span></span>

<span data-ttu-id="a573a-2505">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2505">5</span></span>

<span data-ttu-id="a573a-2506">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2506">6</span></span>

<span data-ttu-id="a573a-2507">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2507">7</span></span>

<span data-ttu-id="a573a-2508">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2508">8</span></span>

<span data-ttu-id="a573a-2509">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2509">9</span></span>

<span data-ttu-id="a573a-2510">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2510">3</span></span><br/> <span data-ttu-id="a573a-2511">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2511">0</span></span><br/>

<span data-ttu-id="a573a-2512">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2512">1</span></span>

<span data-ttu-id="a573a-2513">пропспек</span><span class="sxs-lookup"><span data-stu-id="a573a-2513">PropSpec</span></span>

<span data-ttu-id="a573a-2514">... перемен</span><span class="sxs-lookup"><span data-stu-id="a573a-2514">...(variable)</span></span>

<span data-ttu-id="a573a-2515">втипе</span><span class="sxs-lookup"><span data-stu-id="a573a-2515">vType</span></span>

<span data-ttu-id="a573a-2516">валуеусед</span><span class="sxs-lookup"><span data-stu-id="a573a-2516">ValueUsed</span></span>

<span data-ttu-id="a573a-2517">\_padding1 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-2517">\_padding1 (optional)</span></span>

<span data-ttu-id="a573a-2518">Валуеоффсет (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-2518">ValueOffset (optional)</span></span>

<span data-ttu-id="a573a-2519">Валуесизе (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-2519">ValueSize (optional)</span></span>

<span data-ttu-id="a573a-2520">статусусед</span><span class="sxs-lookup"><span data-stu-id="a573a-2520">StatusUsed</span></span>

<span data-ttu-id="a573a-2521">\_padding2 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-2521">\_padding2 (optional)</span></span>

<span data-ttu-id="a573a-2522">Статусоффсет (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-2522">StatusOffset (optional)</span></span>

<span data-ttu-id="a573a-2523">ленгсусед</span><span class="sxs-lookup"><span data-stu-id="a573a-2523">LengthUsed</span></span>

<span data-ttu-id="a573a-2524">\_padding3 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-2524">\_padding3 (optional)</span></span>

<span data-ttu-id="a573a-2525">Ленгсоффсет (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-2525">LengthOffset (optional)</span></span>



 

<span data-ttu-id="a573a-2526">**Пропспек**: структура кфуллпропспек, указанная в разделе 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="a573a-2526">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="a573a-2527">**втипе**: указывает тип значения данных, содержащегося в столбце.</span><span class="sxs-lookup"><span data-stu-id="a573a-2527">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="a573a-2528">Список значений для этого поля см. в поле Втипе в разделе 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="a573a-2528">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="a573a-2529">**Валуеусед**: одно поле byte, которое должно иметь значение 0x01 или 0x00.</span><span class="sxs-lookup"><span data-stu-id="a573a-2529">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="a573a-2530">Если задано значение 0x01, столбец передается в пределах строки фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="a573a-2530">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="a573a-2531">Если задано 0x00, значение столбца передается в разделе переменной длины в конце буфера.</span><span class="sxs-lookup"><span data-stu-id="a573a-2531">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="a573a-2532">**\_ padding1**: поле с одним байтом, которое должно быть вставлено перед валуеоффсет, если, без него, валуеоффсет не будет начинаться с четного смещения, начиная с начала сообщения.</span><span class="sxs-lookup"><span data-stu-id="a573a-2532">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="a573a-2533">Значение этого байта является произвольным и должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-2533">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="a573a-2534">Если Валуеусед имеет значение 0x00, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-2534">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="a573a-2535">**Валуеоффсет**: 2-байтовое целое число без знака, указывающее смещение значения столбца в строке.</span><span class="sxs-lookup"><span data-stu-id="a573a-2535">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="a573a-2536">Если Валуеусед имеет значение 0x00, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-2536">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="a573a-2537">**Валуесизе**: 2-байтовое целое число без знака, указывающее размер значения столбца в байтах.</span><span class="sxs-lookup"><span data-stu-id="a573a-2537">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="a573a-2538">Если Валуеусед имеет значение 0x00, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-2538">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="a573a-2539">**Статусусед**: одно поле byte, которое должно иметь значение 0x01 или 0x00.</span><span class="sxs-lookup"><span data-stu-id="a573a-2539">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="a573a-2540">Если задано значение 0x01, состояние столбца передается в строке.</span><span class="sxs-lookup"><span data-stu-id="a573a-2540">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="a573a-2541">Если 0x00, состояние столбца не передается в строке.</span><span class="sxs-lookup"><span data-stu-id="a573a-2541">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="a573a-2542">**\_ padding2**: поле с одним байтом, которое должно быть вставлено перед статусоффсет, если, без него, поле статусоффсет не будет начинаться с четного смещения относительно начала сообщения.</span><span class="sxs-lookup"><span data-stu-id="a573a-2542">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="a573a-2543">Значение этого байта является произвольным и должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-2543">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="a573a-2544">Если Статусусед имеет значение 0x00, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-2544">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="a573a-2545">**Статусоффсет**: 2-байтовое целое число без знака, указывающее смещение состояния столбца в строке.</span><span class="sxs-lookup"><span data-stu-id="a573a-2545">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="a573a-2546">Если Статусусед имеет значение 0x00, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-2546">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="a573a-2547">**Ленгсусед**: одно поле byte, которое должно иметь значение 0x01 или 0x00.</span><span class="sxs-lookup"><span data-stu-id="a573a-2547">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="a573a-2548">Если задано значение 0x01, длина столбца передается внутри строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-2548">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="a573a-2549">Если 0x00, длина столбца не должна передаваться внутри строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-2549">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="a573a-2550">**\_ padding3**: поле с одним байтом, которое должно быть вставлено перед ленгсоффсет, если, без него, ленгсоффсет не будет начинаться с четного смещения, начиная с начала сообщения.</span><span class="sxs-lookup"><span data-stu-id="a573a-2550">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="a573a-2551">Значение этого байта является произвольным и должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-2551">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="a573a-2552">Если Ленгсусед имеет значение 0x00, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-2552">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="a573a-2553">**Ленгсоффсет**: 2-байтовое целое число без знака, указывающее смещение длины столбца в строке.</span><span class="sxs-lookup"><span data-stu-id="a573a-2553">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="a573a-2554">Если Ленгсусед имеет значение 0x00, это поле не должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-2554">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="a573a-2555">2.2.1.32 СЕРИАЛИЗЕДПРОПЕРТИВАЛУЕ</span><span class="sxs-lookup"><span data-stu-id="a573a-2555">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="a573a-2556">Структура СЕРИАЛИЗЕДПРОПЕРТИВАЛУЕ содержит сериализованное значение.</span><span class="sxs-lookup"><span data-stu-id="a573a-2556">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="a573a-2557">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2557">0</span></span>

<span data-ttu-id="a573a-2558">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2558">1</span></span>

<span data-ttu-id="a573a-2559">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2559">2</span></span>

<span data-ttu-id="a573a-2560">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2560">3</span></span>

<span data-ttu-id="a573a-2561">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2561">4</span></span>

<span data-ttu-id="a573a-2562">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2562">5</span></span>

<span data-ttu-id="a573a-2563">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2563">6</span></span>

<span data-ttu-id="a573a-2564">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2564">7</span></span>

<span data-ttu-id="a573a-2565">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2565">8</span></span>

<span data-ttu-id="a573a-2566">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2566">9</span></span>

<span data-ttu-id="a573a-2567">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2567">1</span></span><br/> <span data-ttu-id="a573a-2568">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2568">0</span></span><br/>

<span data-ttu-id="a573a-2569">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2569">1</span></span>

<span data-ttu-id="a573a-2570">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2570">2</span></span>

<span data-ttu-id="a573a-2571">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2571">3</span></span>

<span data-ttu-id="a573a-2572">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2572">4</span></span>

<span data-ttu-id="a573a-2573">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2573">5</span></span>

<span data-ttu-id="a573a-2574">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2574">6</span></span>

<span data-ttu-id="a573a-2575">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2575">7</span></span>

<span data-ttu-id="a573a-2576">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2576">8</span></span>

<span data-ttu-id="a573a-2577">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2577">9</span></span>

<span data-ttu-id="a573a-2578">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2578">2</span></span><br/> <span data-ttu-id="a573a-2579">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2579">0</span></span><br/>

<span data-ttu-id="a573a-2580">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2580">1</span></span>

<span data-ttu-id="a573a-2581">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2581">2</span></span>

<span data-ttu-id="a573a-2582">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2582">3</span></span>

<span data-ttu-id="a573a-2583">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2583">4</span></span>

<span data-ttu-id="a573a-2584">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2584">5</span></span>

<span data-ttu-id="a573a-2585">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2585">6</span></span>

<span data-ttu-id="a573a-2586">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2586">7</span></span>

<span data-ttu-id="a573a-2587">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2587">8</span></span>

<span data-ttu-id="a573a-2588">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2588">9</span></span>

<span data-ttu-id="a573a-2589">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2589">3</span></span><br/> <span data-ttu-id="a573a-2590">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2590">0</span></span><br/>

<span data-ttu-id="a573a-2591">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2591">1</span></span>

<span data-ttu-id="a573a-2592">двтипе</span><span class="sxs-lookup"><span data-stu-id="a573a-2592">dwType</span></span>

<span data-ttu-id="a573a-2593">RGB (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-2593">rgb (variable)</span></span>



 

<span data-ttu-id="a573a-2594">**двтипе**: один из типов Variant, определенный в разделе 2.2.1.1, который можно сочетать с модификаторами типа Variant.</span><span class="sxs-lookup"><span data-stu-id="a573a-2594">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="a573a-2595">Для всех типов Variant, за исключением тех, которые объединены с \_ массивом VT, сериализедпропертивалуе имеет тот же макет, что и кбасесторажевариант, как указано в разделе 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="a573a-2595">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="a573a-2596">Если тип Variant сочетается с \_ модификатором типа массива VT, то в поле Кбасесторажевариант управляемое vValue вместо SAFEARRAY используется SAFEARRAY2, заданный в разделе 2.2.1.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="a573a-2596">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="a573a-2597">**RGB**: сериализованное значение.</span><span class="sxs-lookup"><span data-stu-id="a573a-2597">**rgb**: Serialized value.</span></span> <span data-ttu-id="a573a-2598">См. подробные сведения о сериализации для управляемое vValue в 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="a573a-2598">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="a573a-2599">Заголовки сообщений 2.2.2</span><span class="sxs-lookup"><span data-stu-id="a573a-2599">2.2.2 Message Headers</span></span>

<span data-ttu-id="a573a-2600">Все сообщения протокола службы индексирования содержимого содержат 16-байтовый заголовок.</span><span class="sxs-lookup"><span data-stu-id="a573a-2600">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="a573a-2601">Ниже приведена схема, показывающая формат заголовка сообщения протокола службы индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="a573a-2601">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="a573a-2602">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2602">0</span></span>

<span data-ttu-id="a573a-2603">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2603">1</span></span>

<span data-ttu-id="a573a-2604">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2604">2</span></span>

<span data-ttu-id="a573a-2605">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2605">3</span></span>

<span data-ttu-id="a573a-2606">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2606">4</span></span>

<span data-ttu-id="a573a-2607">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2607">5</span></span>

<span data-ttu-id="a573a-2608">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2608">6</span></span>

<span data-ttu-id="a573a-2609">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2609">7</span></span>

<span data-ttu-id="a573a-2610">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2610">8</span></span>

<span data-ttu-id="a573a-2611">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2611">9</span></span>

<span data-ttu-id="a573a-2612">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2612">1</span></span><br/> <span data-ttu-id="a573a-2613">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2613">0</span></span><br/>

<span data-ttu-id="a573a-2614">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2614">1</span></span>

<span data-ttu-id="a573a-2615">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2615">2</span></span>

<span data-ttu-id="a573a-2616">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2616">3</span></span>

<span data-ttu-id="a573a-2617">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2617">4</span></span>

<span data-ttu-id="a573a-2618">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2618">5</span></span>

<span data-ttu-id="a573a-2619">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2619">6</span></span>

<span data-ttu-id="a573a-2620">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2620">7</span></span>

<span data-ttu-id="a573a-2621">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2621">8</span></span>

<span data-ttu-id="a573a-2622">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2622">9</span></span>

<span data-ttu-id="a573a-2623">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2623">2</span></span><br/> <span data-ttu-id="a573a-2624">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2624">0</span></span><br/>

<span data-ttu-id="a573a-2625">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2625">1</span></span>

<span data-ttu-id="a573a-2626">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2626">2</span></span>

<span data-ttu-id="a573a-2627">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2627">3</span></span>

<span data-ttu-id="a573a-2628">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2628">4</span></span>

<span data-ttu-id="a573a-2629">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2629">5</span></span>

<span data-ttu-id="a573a-2630">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2630">6</span></span>

<span data-ttu-id="a573a-2631">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2631">7</span></span>

<span data-ttu-id="a573a-2632">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2632">8</span></span>

<span data-ttu-id="a573a-2633">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2633">9</span></span>

<span data-ttu-id="a573a-2634">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2634">3</span></span><br/> <span data-ttu-id="a573a-2635">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2635">0</span></span><br/>

<span data-ttu-id="a573a-2636">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2636">1</span></span>

<span data-ttu-id="a573a-2637">\_msg</span><span class="sxs-lookup"><span data-stu-id="a573a-2637">\_msg</span></span>

<span data-ttu-id="a573a-2638">\_состояние</span><span class="sxs-lookup"><span data-stu-id="a573a-2638">\_status</span></span>

<span data-ttu-id="a573a-2639">\_улчекксум</span><span class="sxs-lookup"><span data-stu-id="a573a-2639">\_ulChecksum</span></span>

<span data-ttu-id="a573a-2640">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="a573a-2640">\_ulReserved2</span></span>



 

<span data-ttu-id="a573a-2641">\_**MSG**: 32-разрядное целое число, определяющее тип сообщения, следующего за заголовком.</span><span class="sxs-lookup"><span data-stu-id="a573a-2641">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="a573a-2642">В следующей таблице перечислены сообщения протокола службы индексирования содержимого и целые значения, указанные для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="a573a-2642">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="a573a-2643">Как показано в таблице, некоторые значения указывают 2 сообщения в таблице.</span><span class="sxs-lookup"><span data-stu-id="a573a-2643">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="a573a-2644">В этих экземплярах сообщение, следующее за заголовком, можно определить по направлению потока сообщений.</span><span class="sxs-lookup"><span data-stu-id="a573a-2644">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="a573a-2645">Если направлением является клиент-сервер, отображается сообщение с добавлением к имени сообщения.</span><span class="sxs-lookup"><span data-stu-id="a573a-2645">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="a573a-2646">Если направлением является серверный клиент, то отображается сообщение с добавлением к имени сообщения "out".</span><span class="sxs-lookup"><span data-stu-id="a573a-2646">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="a573a-2647">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2647">Value</span></span>      | <span data-ttu-id="a573a-2648">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2648">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="a573a-2649">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="a573a-2649">0x000000C8</span></span> | <span data-ttu-id="a573a-2650">Кпмконнектин или Кпмконнектаут</span><span class="sxs-lookup"><span data-stu-id="a573a-2650">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="a573a-2651">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="a573a-2651">0x000000C9</span></span> | <span data-ttu-id="a573a-2652">кпмдисконнект</span><span class="sxs-lookup"><span data-stu-id="a573a-2652">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="a573a-2653">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="a573a-2653">0x000000CA</span></span> | <span data-ttu-id="a573a-2654">Кпмкреатекуерин или Кпмкреатекуерйоут</span><span class="sxs-lookup"><span data-stu-id="a573a-2654">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="a573a-2655">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="a573a-2655">0x000000CB</span></span> | <span data-ttu-id="a573a-2656">Кпмфрикурсорин или Кпмфрикурсораут</span><span class="sxs-lookup"><span data-stu-id="a573a-2656">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="a573a-2657">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="a573a-2657">0x000000CC</span></span> | <span data-ttu-id="a573a-2658">Кпмжетровсин или Кпмжетровсаут</span><span class="sxs-lookup"><span data-stu-id="a573a-2658">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="a573a-2659">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="a573a-2659">0x000000CD</span></span> | <span data-ttu-id="a573a-2660">Кпмратиофинишедин или Кпмратиофинишедаут</span><span class="sxs-lookup"><span data-stu-id="a573a-2660">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="a573a-2661">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="a573a-2661">0x000000CE</span></span> | <span data-ttu-id="a573a-2662">Кпмкомпаребмкин или Кпмкомпаребмкаут</span><span class="sxs-lookup"><span data-stu-id="a573a-2662">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="a573a-2663">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="a573a-2663">0x000000CF</span></span> | <span data-ttu-id="a573a-2664">Кпмжетаппроксиматепоситионин или Кпмжетаппроксиматепоситионаут</span><span class="sxs-lookup"><span data-stu-id="a573a-2664">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="a573a-2665">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="a573a-2665">0x000000D0</span></span> | <span data-ttu-id="a573a-2666">кпмсетбиндингсин</span><span class="sxs-lookup"><span data-stu-id="a573a-2666">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="a573a-2667">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="a573a-2667">0x000000D1</span></span> | <span data-ttu-id="a573a-2668">кпмжетнотифи</span><span class="sxs-lookup"><span data-stu-id="a573a-2668">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="a573a-2669">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="a573a-2669">0x000000D2</span></span> | <span data-ttu-id="a573a-2670">кпмсенднотифйоут</span><span class="sxs-lookup"><span data-stu-id="a573a-2670">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="a573a-2671">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="a573a-2671">0x000000D7</span></span> | <span data-ttu-id="a573a-2672">Кпмжеткуеристатусин или Кпмжеткуеристатусаут</span><span class="sxs-lookup"><span data-stu-id="a573a-2672">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="a573a-2673">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="a573a-2673">0x000000D9</span></span> | <span data-ttu-id="a573a-2674">кпмЦистатеинаут</span><span class="sxs-lookup"><span data-stu-id="a573a-2674">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="a573a-2675">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="a573a-2675">0x000000E1</span></span> | <span data-ttu-id="a573a-2676">кпмфорцемержеин</span><span class="sxs-lookup"><span data-stu-id="a573a-2676">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="a573a-2677">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="a573a-2677">0x000000E4</span></span> | <span data-ttu-id="a573a-2678">Кпмфетчвалуеин или Кпмфетчвалуеаут</span><span class="sxs-lookup"><span data-stu-id="a573a-2678">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="a573a-2679">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="a573a-2679">0x000000E6</span></span> | <span data-ttu-id="a573a-2680">кпмупдатедокументсин</span><span class="sxs-lookup"><span data-stu-id="a573a-2680">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="a573a-2681">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="a573a-2681">0x000000E7</span></span> | <span data-ttu-id="a573a-2682">Кпмжеткуеристатусексин или Пмжеткуеристатусексаут</span><span class="sxs-lookup"><span data-stu-id="a573a-2682">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="a573a-2683">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="a573a-2683">0x000000E8</span></span> | <span data-ttu-id="a573a-2684">кпмрестартпоситионин</span><span class="sxs-lookup"><span data-stu-id="a573a-2684">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="a573a-2685">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="a573a-2685">0x000000E9</span></span> | <span data-ttu-id="a573a-2686">кпмстопасинчин</span><span class="sxs-lookup"><span data-stu-id="a573a-2686">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="a573a-2687">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="a573a-2687">0x000000EC</span></span> | <span data-ttu-id="a573a-2688">Кпмсеткатстатеин или Кпмсеткатстатеаут</span><span class="sxs-lookup"><span data-stu-id="a573a-2688">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="a573a-2689">\_**состояние**: HRESULT \[ MS-sys \] , указывающий состояние запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="a573a-2689">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="a573a-2690">*Поведение Windows. Клиент всегда задает \_ для поля состояния значение 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="a573a-2690">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="a573a-2691">**\_ УЛЧЕККСУМ**: \_ необходимо вычислить улчекксум, как указано в разделе 3.2.4 для следующих сообщений:</span><span class="sxs-lookup"><span data-stu-id="a573a-2691">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="a573a-2692">кпмконнектин</span><span class="sxs-lookup"><span data-stu-id="a573a-2692">CPMConnectIn</span></span>
-   <span data-ttu-id="a573a-2693">кпмкреатекуерин</span><span class="sxs-lookup"><span data-stu-id="a573a-2693">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="a573a-2694">кпмсетбиндингсин</span><span class="sxs-lookup"><span data-stu-id="a573a-2694">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="a573a-2695">кпмжетровсин</span><span class="sxs-lookup"><span data-stu-id="a573a-2695">CPMGetRowsIn</span></span>
-   <span data-ttu-id="a573a-2696">кпмфетчвалуеин</span><span class="sxs-lookup"><span data-stu-id="a573a-2696">CPMFetchValueIn</span></span>

<span data-ttu-id="a573a-2697">Для всех остальных сообщений \_ параметру УЛЧЕККСУМ должно быть присвоено значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-2697">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="a573a-2698">Клиент должен игнорировать \_ поле улчекксум.</span><span class="sxs-lookup"><span data-stu-id="a573a-2698">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="a573a-2699">**\_ ulReserved2**: значение должно быть равно 0 и игнорируется получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-2699">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="a573a-2700">сообщения 2.2.3</span><span class="sxs-lookup"><span data-stu-id="a573a-2700">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="a573a-2701">2.2.3.1 КпмЦистатеинаут</span><span class="sxs-lookup"><span data-stu-id="a573a-2701">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="a573a-2702">Сообщение КпмЦистатеинаут содержит сведения о состоянии службы индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-2702">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="a573a-2703">Формат сообщения КпмЦистатеинаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-2703">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="a573a-2704">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2704">0</span></span>

<span data-ttu-id="a573a-2705">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2705">1</span></span>

<span data-ttu-id="a573a-2706">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2706">2</span></span>

<span data-ttu-id="a573a-2707">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2707">3</span></span>

<span data-ttu-id="a573a-2708">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2708">4</span></span>

<span data-ttu-id="a573a-2709">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2709">5</span></span>

<span data-ttu-id="a573a-2710">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2710">6</span></span>

<span data-ttu-id="a573a-2711">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2711">7</span></span>

<span data-ttu-id="a573a-2712">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2712">8</span></span>

<span data-ttu-id="a573a-2713">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2713">9</span></span>

<span data-ttu-id="a573a-2714">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2714">1</span></span><br/> <span data-ttu-id="a573a-2715">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2715">0</span></span><br/>

<span data-ttu-id="a573a-2716">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2716">1</span></span>

<span data-ttu-id="a573a-2717">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2717">2</span></span>

<span data-ttu-id="a573a-2718">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2718">3</span></span>

<span data-ttu-id="a573a-2719">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2719">4</span></span>

<span data-ttu-id="a573a-2720">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2720">5</span></span>

<span data-ttu-id="a573a-2721">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2721">6</span></span>

<span data-ttu-id="a573a-2722">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2722">7</span></span>

<span data-ttu-id="a573a-2723">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2723">8</span></span>

<span data-ttu-id="a573a-2724">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2724">9</span></span>

<span data-ttu-id="a573a-2725">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2725">2</span></span><br/> <span data-ttu-id="a573a-2726">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2726">0</span></span><br/>

<span data-ttu-id="a573a-2727">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2727">1</span></span>

<span data-ttu-id="a573a-2728">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2728">2</span></span>

<span data-ttu-id="a573a-2729">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2729">3</span></span>

<span data-ttu-id="a573a-2730">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2730">4</span></span>

<span data-ttu-id="a573a-2731">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2731">5</span></span>

<span data-ttu-id="a573a-2732">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2732">6</span></span>

<span data-ttu-id="a573a-2733">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2733">7</span></span>

<span data-ttu-id="a573a-2734">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2734">8</span></span>

<span data-ttu-id="a573a-2735">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2735">9</span></span>

<span data-ttu-id="a573a-2736">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2736">3</span></span><br/> <span data-ttu-id="a573a-2737">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2737">0</span></span><br/>

<span data-ttu-id="a573a-2738">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2738">1</span></span>

<span data-ttu-id="a573a-2739">кбструкт</span><span class="sxs-lookup"><span data-stu-id="a573a-2739">cbStruct</span></span>

<span data-ttu-id="a573a-2740">квордлист</span><span class="sxs-lookup"><span data-stu-id="a573a-2740">cWordList</span></span>

<span data-ttu-id="a573a-2741">кперсистентиндекс</span><span class="sxs-lookup"><span data-stu-id="a573a-2741">cPersistentIndex</span></span>

<span data-ttu-id="a573a-2742">ккуериес</span><span class="sxs-lookup"><span data-stu-id="a573a-2742">cQueries</span></span>

<span data-ttu-id="a573a-2743">cDocument</span><span class="sxs-lookup"><span data-stu-id="a573a-2743">cDocuments</span></span>

<span data-ttu-id="a573a-2744">кфрештест</span><span class="sxs-lookup"><span data-stu-id="a573a-2744">cFreshTest</span></span>

<span data-ttu-id="a573a-2745">двмержепрогресс</span><span class="sxs-lookup"><span data-stu-id="a573a-2745">dwMergeProgress</span></span>

<span data-ttu-id="a573a-2746">Пространство</span><span class="sxs-lookup"><span data-stu-id="a573a-2746">eState</span></span>

<span data-ttu-id="a573a-2747">кфилтереддокументс</span><span class="sxs-lookup"><span data-stu-id="a573a-2747">cFilteredDocuments</span></span>

<span data-ttu-id="a573a-2748">ктоталдокументс</span><span class="sxs-lookup"><span data-stu-id="a573a-2748">cTotalDocuments</span></span>

<span data-ttu-id="a573a-2749">кпендингсканс</span><span class="sxs-lookup"><span data-stu-id="a573a-2749">cPendingScans</span></span>

<span data-ttu-id="a573a-2750">двиндекссизе</span><span class="sxs-lookup"><span data-stu-id="a573a-2750">dwIndexSize</span></span>

<span data-ttu-id="a573a-2751">куникуекэйс</span><span class="sxs-lookup"><span data-stu-id="a573a-2751">cUniqueKeys</span></span>

<span data-ttu-id="a573a-2752">ксеккдокументс</span><span class="sxs-lookup"><span data-stu-id="a573a-2752">cSecQDocuments</span></span>

<span data-ttu-id="a573a-2753">двпропкачесизе</span><span class="sxs-lookup"><span data-stu-id="a573a-2753">dwPropCacheSize</span></span>



 

<span data-ttu-id="a573a-2754">**кбструкт**: 32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-2754">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="a573a-2755">Размер (в байтах) этого сообщения (за исключением общего заголовка).</span><span class="sxs-lookup"><span data-stu-id="a573a-2755">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="a573a-2756">НЕОБХОДИМО задать значение 0x0000003C.</span><span class="sxs-lookup"><span data-stu-id="a573a-2756">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="a573a-2757">**квордлист**: 32-разрядное целое число без знака, указывающее количество начальных индексов, созданных для недавно индексированных документов.</span><span class="sxs-lookup"><span data-stu-id="a573a-2757">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="a573a-2758">**кперсистентиндекс**: 32-битовое целое число без знака, указывающее количество постоянных индексов.</span><span class="sxs-lookup"><span data-stu-id="a573a-2758">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="a573a-2759">**ккуериес**: 32-битовое целое число без знака, указывающее количество активных запросов.</span><span class="sxs-lookup"><span data-stu-id="a573a-2759">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="a573a-2760">**CDocument**: 32-разрядное целое число без знака, указывающее общее количество документов, ожидающих индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-2760">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="a573a-2761">**кфрештест**: 32-разрядное целое число без знака, указывающее количество уникальных документов со сведениями в индексах, которые не были полностью оптимизированы для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="a573a-2761">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="a573a-2762">**двмержепрогресс**: беззнаковое 32-разрядное целое число, определяющее процент завершения текущей полной оптимизации индексов, если в данный момент выполняется оптимизация.</span><span class="sxs-lookup"><span data-stu-id="a573a-2762">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="a573a-2763">ДОЛЖНО быть меньше или равно 100.</span><span class="sxs-lookup"><span data-stu-id="a573a-2763">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="a573a-2764">**пространство**: состояние индексирования содержимого, заданное одной или несколькими \_ константами состояния CI \_ \* , определенными в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="a573a-2764">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="a573a-2765">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2765">Value</span></span>                                         | <span data-ttu-id="a573a-2766">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2766">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-2767">\_ \_ Теневое \_ Слияние состояния CI 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-2767">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="a573a-2768">Служба индексирования находится в процессе оптимизации некоторых индексов, чтобы сократить использование памяти и повысить производительность запросов.</span><span class="sxs-lookup"><span data-stu-id="a573a-2768">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="a573a-2769">\_ \_ Слияние хозяина состояния CI — \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-2769">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="a573a-2770">Служба индексирования находится в процессе полной оптимизации для всех индексов.</span><span class="sxs-lookup"><span data-stu-id="a573a-2770">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a573a-2771">\_ \_ Требуется сканирование содержимого состояния CI, \_ \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="a573a-2771">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="a573a-2772">Некоторые документы в индексе были изменены, и службе индексирования необходимо определить, какие из них были добавлены, изменены или удалены.</span><span class="sxs-lookup"><span data-stu-id="a573a-2772">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a573a-2773">\_Состояние CI \_ отжига \_ Merge 0x00000008</span><span class="sxs-lookup"><span data-stu-id="a573a-2773">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="a573a-2774">Служба индексирования находится в процессе оптимизации индексов, чтобы сократить использование памяти и повысить производительность запросов.</span><span class="sxs-lookup"><span data-stu-id="a573a-2774">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="a573a-2775">Этот процесс является более полным, чем тот, который определяется \_ \_ значением теневого копирования состояния CI \_ , но не так, как указано в \_ \_ значении объединения с образцом состояния CI \_ .</span><span class="sxs-lookup"><span data-stu-id="a573a-2775">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="a573a-2776">Такая оптимизация зависит от конкретной реализации, так как они зависят от способа внутреннего хранения данных. оптимизация не влияет на протокол никаким способом, отличным от времени отклика.</span><span class="sxs-lookup"><span data-stu-id="a573a-2776">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="a573a-2777">\_Просмотр состояния CI \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="a573a-2777">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="a573a-2778">Служба индексирования проверяет каталог или набор каталогов, чтобы определить, были ли файлы добавлены, удалены или обновлены со времени последнего индексирования каталога.</span><span class="sxs-lookup"><span data-stu-id="a573a-2778">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a573a-2779">\_Восстановление состояния CI — \_ 0x00000020</span><span class="sxs-lookup"><span data-stu-id="a573a-2779">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="a573a-2780">Служба запускается из последнего сохраненного состояния и находится в процессе восстановления.</span><span class="sxs-lookup"><span data-stu-id="a573a-2780">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a573a-2781">\_ \_ 0x00000080 нехватка \_ памяти CI State</span><span class="sxs-lookup"><span data-stu-id="a573a-2781">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="a573a-2782">Большая часть виртуальной памяти сервера используется.</span><span class="sxs-lookup"><span data-stu-id="a573a-2782">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a573a-2783">\_ \_ Высокий уровень операций ввода-вывода в состоянии CI \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="a573a-2783">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="a573a-2784">Уровень активности ввода-вывода на сервере относительно высокий.</span><span class="sxs-lookup"><span data-stu-id="a573a-2784">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="a573a-2785">\_ \_ Сводное \_ Слияние состояния CI \_ 0x00000200 приостановлено</span><span class="sxs-lookup"><span data-stu-id="a573a-2785">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="a573a-2786">Процесс полной оптимизации для всех выполняемых индексов был приостановлен.</span><span class="sxs-lookup"><span data-stu-id="a573a-2786">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="a573a-2787">Он предоставляется исключительно в информативных целях и не влияет на CISP.</span><span class="sxs-lookup"><span data-stu-id="a573a-2787">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a573a-2788">\_Состояние CI \_ только для чтения \_ 0x00000400</span><span class="sxs-lookup"><span data-stu-id="a573a-2788">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="a573a-2789">Часть службы индексирования, которая выбирает новые документы для индексирования, приостановлена.</span><span class="sxs-lookup"><span data-stu-id="a573a-2789">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="a573a-2790">Он предоставляется исключительно в информативных целях и не влияет на CISP.</span><span class="sxs-lookup"><span data-stu-id="a573a-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a573a-2791">Состояние элемента конфигурации \_ \_ батарея \_ Power 0x00000800</span><span class="sxs-lookup"><span data-stu-id="a573a-2791">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="a573a-2792">Часть службы индексирования, которая выбирает новые документы для индексирования, приостановлена для сохранения времени существования аккумулятора, но по-прежнему отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="a573a-2792">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="a573a-2793">Он предоставляется исключительно в информативных целях и не влияет на CISP.</span><span class="sxs-lookup"><span data-stu-id="a573a-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a573a-2794">\_Состояние CI \_ пользователь \_ Active 0x00001000</span><span class="sxs-lookup"><span data-stu-id="a573a-2794">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="a573a-2795">Часть службы индексирования, которая выбирает новые документы для индексирования, приостановлена из-за высокой активности пользователя (клавиатуры или мыши), но по-прежнему отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="a573a-2795">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="a573a-2796">Он предоставляется исключительно в информативных целях и не влияет на CISP.</span><span class="sxs-lookup"><span data-stu-id="a573a-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="a573a-2797">Состояние CI, \_ \_ начиная с 0x00002000</span><span class="sxs-lookup"><span data-stu-id="a573a-2797">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="a573a-2798">Служба запускается.</span><span class="sxs-lookup"><span data-stu-id="a573a-2798">The service is starting.</span></span> <span data-ttu-id="a573a-2799">Запросы можно запускать, но сканирование и уведомление еще не включены.</span><span class="sxs-lookup"><span data-stu-id="a573a-2799">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="a573a-2800">Он предоставляется исключительно в информативных целях и не влияет на CISP.</span><span class="sxs-lookup"><span data-stu-id="a573a-2800">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a573a-2801">\_ \_ Считывание состояния CI \_ USN 0x00004000</span><span class="sxs-lookup"><span data-stu-id="a573a-2801">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="a573a-2802">Служба не прочитала журнал, который хранится в файловой системе, чтобы отследить изменения в файлах или каталогах на томе, поэтому индекс может оказаться неактуальным.</span><span class="sxs-lookup"><span data-stu-id="a573a-2802">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="a573a-2803">**кфилтереддокументс**: 32-разрядное целое число без знака, указывающее количество документов, индексированных с момента начала индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="a573a-2803">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="a573a-2804">**ктоталдокументс**: 32-битовое целое число без знака, указывающее общее количество документов в системе.</span><span class="sxs-lookup"><span data-stu-id="a573a-2804">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="a573a-2805">**кпендингсканс**: 32-битовое целое число без знака, указывающее количество ожидающих операций индексирования высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="a573a-2805">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="a573a-2806">Значение этого параметра зависит от поставщика, но более крупные числа должны указывать на большее количество индексов.</span><span class="sxs-lookup"><span data-stu-id="a573a-2806">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="a573a-2807">*Поведение Windows*. обычно это значение равно нулю, за исключением случаев, когда было начато индексирование или после того, как очередь уведомлений переполняется.</span><span class="sxs-lookup"><span data-stu-id="a573a-2807">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="a573a-2808">**двиндекссизе**: 32-разрядное целое число без знака, указывающее размер индекса (за исключением кэша свойств) в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="a573a-2808">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="a573a-2809">**куникуекэйс**: 32-битовое целое число без знака, указывающее приблизительное количество уникальных ключей в каталоге.</span><span class="sxs-lookup"><span data-stu-id="a573a-2809">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="a573a-2810">**ксеккдокументс**: 32-разрядное целое число без знака, указывающее количество документов, которые служба индексирования будет повторно пытаться индексировать из-за сбоя во время первоначальной попытки индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-2810">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="a573a-2811">**двпропкачесизе**: 32-разрядное целое число без знака, указывающее размер кэша свойств в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="a573a-2811">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="a573a-2812">2.2.3.2 Кпмсеткатстатеин</span><span class="sxs-lookup"><span data-stu-id="a573a-2812">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="a573a-2813">Сообщение Кпмсеткатстатеин задает состояние каталога.</span><span class="sxs-lookup"><span data-stu-id="a573a-2813">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="a573a-2814">Формат сообщения Кпмсеткатстатеин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-2814">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-2815">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2815">0</span></span>

<span data-ttu-id="a573a-2816">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2816">1</span></span>

<span data-ttu-id="a573a-2817">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2817">2</span></span>

<span data-ttu-id="a573a-2818">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2818">3</span></span>

<span data-ttu-id="a573a-2819">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2819">4</span></span>

<span data-ttu-id="a573a-2820">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2820">5</span></span>

<span data-ttu-id="a573a-2821">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2821">6</span></span>

<span data-ttu-id="a573a-2822">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2822">7</span></span>

<span data-ttu-id="a573a-2823">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2823">8</span></span>

<span data-ttu-id="a573a-2824">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2824">9</span></span>

<span data-ttu-id="a573a-2825">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2825">1</span></span><br/> <span data-ttu-id="a573a-2826">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2826">0</span></span><br/>

<span data-ttu-id="a573a-2827">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2827">1</span></span>

<span data-ttu-id="a573a-2828">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2828">2</span></span>

<span data-ttu-id="a573a-2829">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2829">3</span></span>

<span data-ttu-id="a573a-2830">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2830">4</span></span>

<span data-ttu-id="a573a-2831">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2831">5</span></span>

<span data-ttu-id="a573a-2832">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2832">6</span></span>

<span data-ttu-id="a573a-2833">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2833">7</span></span>

<span data-ttu-id="a573a-2834">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2834">8</span></span>

<span data-ttu-id="a573a-2835">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2835">9</span></span>

<span data-ttu-id="a573a-2836">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2836">2</span></span><br/> <span data-ttu-id="a573a-2837">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2837">0</span></span><br/>

<span data-ttu-id="a573a-2838">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2838">1</span></span>

<span data-ttu-id="a573a-2839">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2839">2</span></span>

<span data-ttu-id="a573a-2840">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2840">3</span></span>

<span data-ttu-id="a573a-2841">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2841">4</span></span>

<span data-ttu-id="a573a-2842">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2842">5</span></span>

<span data-ttu-id="a573a-2843">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2843">6</span></span>

<span data-ttu-id="a573a-2844">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2844">7</span></span>

<span data-ttu-id="a573a-2845">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2845">8</span></span>

<span data-ttu-id="a573a-2846">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2846">9</span></span>

<span data-ttu-id="a573a-2847">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2847">3</span></span><br/> <span data-ttu-id="a573a-2848">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2848">0</span></span><br/>

<span data-ttu-id="a573a-2849">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2849">1</span></span>

<span data-ttu-id="a573a-2850">\_partID</span><span class="sxs-lookup"><span data-stu-id="a573a-2850">\_partID</span></span>

<span data-ttu-id="a573a-2851">\_двневстате</span><span class="sxs-lookup"><span data-stu-id="a573a-2851">\_dwNewState</span></span>

<span data-ttu-id="a573a-2852">\_Катнаме (переменная, необязательный)</span><span class="sxs-lookup"><span data-stu-id="a573a-2852">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="a573a-2853">**\_ PARTID**: необходимо задать значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="a573a-2853">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="a573a-2854">**\_ двневстате**: необходимо задать одно из следующих значений, указывающее новое состояние каталога.</span><span class="sxs-lookup"><span data-stu-id="a573a-2854">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="a573a-2855">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2855">Value</span></span>                         | <span data-ttu-id="a573a-2856">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2856">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-2857">ЦИКАТ \_ остановлено 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-2857">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="a573a-2858">Каталог остановлен.</span><span class="sxs-lookup"><span data-stu-id="a573a-2858">The catalog is stopped.</span></span> <span data-ttu-id="a573a-2859">Это состояние означает, что новые файлы индексироваться не будут, а поисковые запросы обрабатываться не будут.</span><span class="sxs-lookup"><span data-stu-id="a573a-2859">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="a573a-2860">ЦИКАТ \_ ReadOnly 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-2860">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="a573a-2861">Каталог доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a573a-2861">The catalog is read-only.</span></span> <span data-ttu-id="a573a-2862">Нет новых файлов для индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-2862">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="a573a-2863">ЦИКАТ, \_ доступный для записи, 0x00000004</span><span class="sxs-lookup"><span data-stu-id="a573a-2863">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="a573a-2864">Каталог доступен для записи.</span><span class="sxs-lookup"><span data-stu-id="a573a-2864">The catalog is writable.</span></span> <span data-ttu-id="a573a-2865">Новые файлы можно индексировать, а запросы поиска — обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="a573a-2865">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="a573a-2866">ЦИКАТ \_ без \_ запроса 0x00000008</span><span class="sxs-lookup"><span data-stu-id="a573a-2866">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="a573a-2867">Каталог недоступен для запросов.</span><span class="sxs-lookup"><span data-stu-id="a573a-2867">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="a573a-2868">ЦИКАТ \_ получить \_ состояние 0x00000010</span><span class="sxs-lookup"><span data-stu-id="a573a-2868">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="a573a-2869">Состояние каталога не должно изменяться, извлекается только.</span><span class="sxs-lookup"><span data-stu-id="a573a-2869">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="a573a-2870">ЦИКАТ \_ все \_ открытые 0x00000020</span><span class="sxs-lookup"><span data-stu-id="a573a-2870">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="a573a-2871">Проверка того, были ли запущены все каталоги.</span><span class="sxs-lookup"><span data-stu-id="a573a-2871">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="a573a-2872">Если да, то в \_ поле дволдстате, отправленном в ответе кпмсеткатстатеаут на это сообщение, будет получено ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a573a-2872">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="a573a-2873">**\_ Катнаме**: имя каталога, для которого необходимо изменить состояние.</span><span class="sxs-lookup"><span data-stu-id="a573a-2873">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="a573a-2874">Имя должно быть строкой в Юникоде, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="a573a-2874">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="a573a-2875">Это поле необходимо опустить, если \_ двневстате имеет значение Цикат \_ All \_ Opened.</span><span class="sxs-lookup"><span data-stu-id="a573a-2875">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="a573a-2876">2.2.3.3 Кпмсеткатстатеаут</span><span class="sxs-lookup"><span data-stu-id="a573a-2876">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="a573a-2877">Сообщение Кпмсеткатстатеаут — это ответ на сообщение Кпмсеткатстатеин со старым состоянием каталога.</span><span class="sxs-lookup"><span data-stu-id="a573a-2877">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="a573a-2878">Формат сообщения Кпмсеткатстатеаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-2878">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="a573a-2879">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2879">0</span></span>

<span data-ttu-id="a573a-2880">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2880">1</span></span>

<span data-ttu-id="a573a-2881">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2881">2</span></span>

<span data-ttu-id="a573a-2882">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2882">3</span></span>

<span data-ttu-id="a573a-2883">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2883">4</span></span>

<span data-ttu-id="a573a-2884">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2884">5</span></span>

<span data-ttu-id="a573a-2885">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2885">6</span></span>

<span data-ttu-id="a573a-2886">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2886">7</span></span>

<span data-ttu-id="a573a-2887">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2887">8</span></span>

<span data-ttu-id="a573a-2888">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2888">9</span></span>

<span data-ttu-id="a573a-2889">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2889">1</span></span><br/> <span data-ttu-id="a573a-2890">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2890">0</span></span><br/>

<span data-ttu-id="a573a-2891">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2891">1</span></span>

<span data-ttu-id="a573a-2892">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2892">2</span></span>

<span data-ttu-id="a573a-2893">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2893">3</span></span>

<span data-ttu-id="a573a-2894">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2894">4</span></span>

<span data-ttu-id="a573a-2895">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2895">5</span></span>

<span data-ttu-id="a573a-2896">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2896">6</span></span>

<span data-ttu-id="a573a-2897">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2897">7</span></span>

<span data-ttu-id="a573a-2898">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2898">8</span></span>

<span data-ttu-id="a573a-2899">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2899">9</span></span>

<span data-ttu-id="a573a-2900">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2900">2</span></span><br/> <span data-ttu-id="a573a-2901">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2901">0</span></span><br/>

<span data-ttu-id="a573a-2902">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2902">1</span></span>

<span data-ttu-id="a573a-2903">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2903">2</span></span>

<span data-ttu-id="a573a-2904">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2904">3</span></span>

<span data-ttu-id="a573a-2905">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2905">4</span></span>

<span data-ttu-id="a573a-2906">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2906">5</span></span>

<span data-ttu-id="a573a-2907">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2907">6</span></span>

<span data-ttu-id="a573a-2908">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2908">7</span></span>

<span data-ttu-id="a573a-2909">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2909">8</span></span>

<span data-ttu-id="a573a-2910">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2910">9</span></span>

<span data-ttu-id="a573a-2911">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2911">3</span></span><br/> <span data-ttu-id="a573a-2912">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2912">0</span></span><br/>

<span data-ttu-id="a573a-2913">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2913">1</span></span>

<span data-ttu-id="a573a-2914">\_дволдстате</span><span class="sxs-lookup"><span data-stu-id="a573a-2914">\_dwOldState</span></span>



 

<span data-ttu-id="a573a-2915">**\_ дволдстате**: одно из следующих значений, указывающее старое состояние каталога.</span><span class="sxs-lookup"><span data-stu-id="a573a-2915">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="a573a-2916">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2916">Value</span></span>                       | <span data-ttu-id="a573a-2917">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2917">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="a573a-2918">ЦИКАТ \_ остановлено 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-2918">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="a573a-2919">Каталог остановлен.</span><span class="sxs-lookup"><span data-stu-id="a573a-2919">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="a573a-2920">ЦИКАТ \_ ReadOnly 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-2920">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="a573a-2921">Каталог доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a573a-2921">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="a573a-2922">ЦИКАТ, \_ доступный для записи, 0x00000004</span><span class="sxs-lookup"><span data-stu-id="a573a-2922">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="a573a-2923">Каталог доступен для записи.</span><span class="sxs-lookup"><span data-stu-id="a573a-2923">The catalog is writable.</span></span>                   |
| <span data-ttu-id="a573a-2924">ЦИКАТ \_ без \_ запроса 0x00000008</span><span class="sxs-lookup"><span data-stu-id="a573a-2924">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="a573a-2925">Каталог недоступен для запросов.</span><span class="sxs-lookup"><span data-stu-id="a573a-2925">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="a573a-2926">2.2.3.4 Кпмупдатедокументсин</span><span class="sxs-lookup"><span data-stu-id="a573a-2926">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="a573a-2927">Сообщение Кпмупдатедокументсин направляет сервер для индексирования указанного пути.</span><span class="sxs-lookup"><span data-stu-id="a573a-2927">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="a573a-2928">Сервер будет отвечать с заголовком сообщения Кпмупдатедокументсаут, в котором результаты запроса содержатся в \_ поле Status заголовка сообщения.</span><span class="sxs-lookup"><span data-stu-id="a573a-2928">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="a573a-2929">Формат сообщения Кпмупдатедокументсин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-2929">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-2930">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2930">0</span></span>

<span data-ttu-id="a573a-2931">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2931">1</span></span>

<span data-ttu-id="a573a-2932">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2932">2</span></span>

<span data-ttu-id="a573a-2933">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2933">3</span></span>

<span data-ttu-id="a573a-2934">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2934">4</span></span>

<span data-ttu-id="a573a-2935">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2935">5</span></span>

<span data-ttu-id="a573a-2936">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2936">6</span></span>

<span data-ttu-id="a573a-2937">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2937">7</span></span>

<span data-ttu-id="a573a-2938">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2938">8</span></span>

<span data-ttu-id="a573a-2939">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2939">9</span></span>

<span data-ttu-id="a573a-2940">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2940">1</span></span><br/> <span data-ttu-id="a573a-2941">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2941">0</span></span><br/>

<span data-ttu-id="a573a-2942">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2942">1</span></span>

<span data-ttu-id="a573a-2943">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2943">2</span></span>

<span data-ttu-id="a573a-2944">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2944">3</span></span>

<span data-ttu-id="a573a-2945">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2945">4</span></span>

<span data-ttu-id="a573a-2946">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2946">5</span></span>

<span data-ttu-id="a573a-2947">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2947">6</span></span>

<span data-ttu-id="a573a-2948">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2948">7</span></span>

<span data-ttu-id="a573a-2949">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2949">8</span></span>

<span data-ttu-id="a573a-2950">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2950">9</span></span>

<span data-ttu-id="a573a-2951">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2951">2</span></span><br/> <span data-ttu-id="a573a-2952">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2952">0</span></span><br/>

<span data-ttu-id="a573a-2953">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2953">1</span></span>

<span data-ttu-id="a573a-2954">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2954">2</span></span>

<span data-ttu-id="a573a-2955">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2955">3</span></span>

<span data-ttu-id="a573a-2956">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2956">4</span></span>

<span data-ttu-id="a573a-2957">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2957">5</span></span>

<span data-ttu-id="a573a-2958">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2958">6</span></span>

<span data-ttu-id="a573a-2959">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2959">7</span></span>

<span data-ttu-id="a573a-2960">8</span><span class="sxs-lookup"><span data-stu-id="a573a-2960">8</span></span>

<span data-ttu-id="a573a-2961">9</span><span class="sxs-lookup"><span data-stu-id="a573a-2961">9</span></span>

<span data-ttu-id="a573a-2962">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2962">3</span></span><br/> <span data-ttu-id="a573a-2963">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2963">0</span></span><br/>

<span data-ttu-id="a573a-2964">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2964">1</span></span>

<span data-ttu-id="a573a-2965">\_флаг (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-2965">\_flag (optional)</span></span>

<span data-ttu-id="a573a-2966">\_Фрутпас (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-2966">\_fRootPath (optional)</span></span>

<span data-ttu-id="a573a-2967">RootPath (переменная, необязательный)</span><span class="sxs-lookup"><span data-stu-id="a573a-2967">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="a573a-2968">**\_ флаг**: тип обновления, которое необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="a573a-2968">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="a573a-2969">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="a573a-2969">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="a573a-2970">В этом поле должно быть указано одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a573a-2970">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="a573a-2971">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2971">Value</span></span>                  | <span data-ttu-id="a573a-2972">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-2972">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a573a-2973">UPD \_ инкрем 0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-2973">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="a573a-2974">Необходимо выполнить добавочное обновление.</span><span class="sxs-lookup"><span data-stu-id="a573a-2974">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="a573a-2975">\_Полный UPD 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-2975">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="a573a-2976">Необходимо выполнить полное обновление.</span><span class="sxs-lookup"><span data-stu-id="a573a-2976">A full update is to be performed.</span></span>         |
| <span data-ttu-id="a573a-2977">UPD \_ init 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-2977">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="a573a-2978">Будет выполнена новая инициализация.</span><span class="sxs-lookup"><span data-stu-id="a573a-2978">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="a573a-2979">**\_ фрутпас**: логическое значение, указывающее, указывает ли поле rootpath путь для выполнения обновления.</span><span class="sxs-lookup"><span data-stu-id="a573a-2979">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="a573a-2980">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="a573a-2980">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="a573a-2981">Для этого поля необходимо задать значение 0x00000001 или 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-2981">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="a573a-2982">Если задано значение 0x00000001, то путь, по которому выполняется обновление, включается в RootPath.</span><span class="sxs-lookup"><span data-stu-id="a573a-2982">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="a573a-2983">Если задано значение 0x00000000, то обновление будет выполнено для всех индексированных путей.</span><span class="sxs-lookup"><span data-stu-id="a573a-2983">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="a573a-2984">**Rootpath**: имя обновляемого пути.</span><span class="sxs-lookup"><span data-stu-id="a573a-2984">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="a573a-2985">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="a573a-2985">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="a573a-2986">Имя должно быть строкой в Юникоде, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="a573a-2986">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="a573a-2987">Это поле необходимо опустить, если \_ для фрутпас задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-2987">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="a573a-2988">2.2.3.5 Кпмфорцемержеин</span><span class="sxs-lookup"><span data-stu-id="a573a-2988">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="a573a-2989">Сообщение Кпмфорцемержеин запрашивает сервер для выполнения любого обслуживания, необходимого для повышения производительности запросов.</span><span class="sxs-lookup"><span data-stu-id="a573a-2989">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="a573a-2990">Сервер будет отвечать с заголовком сообщения Кпмфорцемержеин, а результаты запроса содержатся в \_ поле Status (состояние).</span><span class="sxs-lookup"><span data-stu-id="a573a-2990">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="a573a-2991">Формат сообщения Кпмфорцемержеин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-2991">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-2992">0</span><span class="sxs-lookup"><span data-stu-id="a573a-2992">0</span></span>

<span data-ttu-id="a573a-2993">1</span><span class="sxs-lookup"><span data-stu-id="a573a-2993">1</span></span>

<span data-ttu-id="a573a-2994">2</span><span class="sxs-lookup"><span data-stu-id="a573a-2994">2</span></span>

<span data-ttu-id="a573a-2995">3</span><span class="sxs-lookup"><span data-stu-id="a573a-2995">3</span></span>

<span data-ttu-id="a573a-2996">4</span><span class="sxs-lookup"><span data-stu-id="a573a-2996">4</span></span>

<span data-ttu-id="a573a-2997">5</span><span class="sxs-lookup"><span data-stu-id="a573a-2997">5</span></span>

<span data-ttu-id="a573a-2998">6</span><span class="sxs-lookup"><span data-stu-id="a573a-2998">6</span></span>

<span data-ttu-id="a573a-2999">7</span><span class="sxs-lookup"><span data-stu-id="a573a-2999">7</span></span>

<span data-ttu-id="a573a-3000">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3000">8</span></span>

<span data-ttu-id="a573a-3001">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3001">9</span></span>

<span data-ttu-id="a573a-3002">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3002">1</span></span><br/> <span data-ttu-id="a573a-3003">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3003">0</span></span><br/>

<span data-ttu-id="a573a-3004">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3004">1</span></span>

<span data-ttu-id="a573a-3005">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3005">2</span></span>

<span data-ttu-id="a573a-3006">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3006">3</span></span>

<span data-ttu-id="a573a-3007">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3007">4</span></span>

<span data-ttu-id="a573a-3008">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3008">5</span></span>

<span data-ttu-id="a573a-3009">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3009">6</span></span>

<span data-ttu-id="a573a-3010">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3010">7</span></span>

<span data-ttu-id="a573a-3011">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3011">8</span></span>

<span data-ttu-id="a573a-3012">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3012">9</span></span>

<span data-ttu-id="a573a-3013">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3013">2</span></span><br/> <span data-ttu-id="a573a-3014">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3014">0</span></span><br/>

<span data-ttu-id="a573a-3015">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3015">1</span></span>

<span data-ttu-id="a573a-3016">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3016">2</span></span>

<span data-ttu-id="a573a-3017">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3017">3</span></span>

<span data-ttu-id="a573a-3018">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3018">4</span></span>

<span data-ttu-id="a573a-3019">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3019">5</span></span>

<span data-ttu-id="a573a-3020">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3020">6</span></span>

<span data-ttu-id="a573a-3021">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3021">7</span></span>

<span data-ttu-id="a573a-3022">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3022">8</span></span>

<span data-ttu-id="a573a-3023">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3023">9</span></span>

<span data-ttu-id="a573a-3024">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3024">3</span></span><br/> <span data-ttu-id="a573a-3025">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3025">0</span></span><br/>

<span data-ttu-id="a573a-3026">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3026">1</span></span>

<span data-ttu-id="a573a-3027">\_partID (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-3027">\_partID (optional)</span></span>



 

<span data-ttu-id="a573a-3028">**\_ PARTID**: это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="a573a-3028">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="a573a-3029">Если это поле указано, оно должно быть установлено в значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="a573a-3029">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="a573a-3030">2.2.3.6 Кпмконнектин</span><span class="sxs-lookup"><span data-stu-id="a573a-3030">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="a573a-3031">Сообщение Кпмконнектин начинает сеанс между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="a573a-3031">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="a573a-3032">Формат сообщения Кпмконнектин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3032">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-3033">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3033">0</span></span>

<span data-ttu-id="a573a-3034">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3034">1</span></span>

<span data-ttu-id="a573a-3035">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3035">2</span></span>

<span data-ttu-id="a573a-3036">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3036">3</span></span>

<span data-ttu-id="a573a-3037">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3037">4</span></span>

<span data-ttu-id="a573a-3038">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3038">5</span></span>

<span data-ttu-id="a573a-3039">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3039">6</span></span>

<span data-ttu-id="a573a-3040">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3040">7</span></span>

<span data-ttu-id="a573a-3041">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3041">8</span></span>

<span data-ttu-id="a573a-3042">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3042">9</span></span>

<span data-ttu-id="a573a-3043">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3043">1</span></span><br/> <span data-ttu-id="a573a-3044">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3044">0</span></span><br/>

<span data-ttu-id="a573a-3045">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3045">1</span></span>

<span data-ttu-id="a573a-3046">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3046">2</span></span>

<span data-ttu-id="a573a-3047">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3047">3</span></span>

<span data-ttu-id="a573a-3048">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3048">4</span></span>

<span data-ttu-id="a573a-3049">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3049">5</span></span>

<span data-ttu-id="a573a-3050">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3050">6</span></span>

<span data-ttu-id="a573a-3051">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3051">7</span></span>

<span data-ttu-id="a573a-3052">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3052">8</span></span>

<span data-ttu-id="a573a-3053">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3053">9</span></span>

<span data-ttu-id="a573a-3054">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3054">2</span></span><br/> <span data-ttu-id="a573a-3055">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3055">0</span></span><br/>

<span data-ttu-id="a573a-3056">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3056">1</span></span>

<span data-ttu-id="a573a-3057">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3057">2</span></span>

<span data-ttu-id="a573a-3058">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3058">3</span></span>

<span data-ttu-id="a573a-3059">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3059">4</span></span>

<span data-ttu-id="a573a-3060">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3060">5</span></span>

<span data-ttu-id="a573a-3061">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3061">6</span></span>

<span data-ttu-id="a573a-3062">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3062">7</span></span>

<span data-ttu-id="a573a-3063">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3063">8</span></span>

<span data-ttu-id="a573a-3064">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3064">9</span></span>

<span data-ttu-id="a573a-3065">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3065">3</span></span><br/> <span data-ttu-id="a573a-3066">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3066">0</span></span><br/>

<span data-ttu-id="a573a-3067">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3067">1</span></span>

<span data-ttu-id="a573a-3068">\_иклиентверсион</span><span class="sxs-lookup"><span data-stu-id="a573a-3068">\_iClientVersion</span></span>

<span data-ttu-id="a573a-3069">\_фклиентисремоте</span><span class="sxs-lookup"><span data-stu-id="a573a-3069">\_fClientIsRemote</span></span>

<span data-ttu-id="a573a-3070">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="a573a-3070">\_cbBlob1</span></span>

<span data-ttu-id="a573a-3071">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="a573a-3071">\_cbBlob2</span></span>

<span data-ttu-id="a573a-3072">\_заполнение</span><span class="sxs-lookup"><span data-stu-id="a573a-3072">\_padding</span></span>

<span data-ttu-id="a573a-3073">...</span><span class="sxs-lookup"><span data-stu-id="a573a-3073">...</span></span>

<span data-ttu-id="a573a-3074">...</span><span class="sxs-lookup"><span data-stu-id="a573a-3074">...</span></span>

<span data-ttu-id="a573a-3075">MachineName</span><span class="sxs-lookup"><span data-stu-id="a573a-3075">MachineName</span></span>

<span data-ttu-id="a573a-3076">... перемен</span><span class="sxs-lookup"><span data-stu-id="a573a-3076">... (variable)</span></span>

<span data-ttu-id="a573a-3077">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="a573a-3077">UserName</span></span>

<span data-ttu-id="a573a-3078">... перемен</span><span class="sxs-lookup"><span data-stu-id="a573a-3078">... (variable)</span></span>

<span data-ttu-id="a573a-3079">\_Паддингкпропсетс (необязательный, переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-3079">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="a573a-3080">кпропсетс</span><span class="sxs-lookup"><span data-stu-id="a573a-3080">cPropSets</span></span>

<span data-ttu-id="a573a-3081">PropertySet1 (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-3081">PropertySet1 (variable)</span></span>

<span data-ttu-id="a573a-3082">PropertySet2 (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-3082">PropertySet2 (variable)</span></span>

<span data-ttu-id="a573a-3083">\_Паддинжекстпропсет (необязательный, переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-3083">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="a573a-3084">цекстпропсет</span><span class="sxs-lookup"><span data-stu-id="a573a-3084">cExtPropSet</span></span>

<span data-ttu-id="a573a-3085">Апропертисетс (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-3085">aPropertySets (variable)</span></span>



 

<span data-ttu-id="a573a-3086">**\_ иклиентверсион**: 32-разрядное целое число, указывающее, должен ли сервер проверять значение контрольной суммы, указанное в \_ поле улчекксум заголовков сообщений для сообщений, отправленных клиентом.</span><span class="sxs-lookup"><span data-stu-id="a573a-3086">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="a573a-3087">Если \_ поле иклиентверсион имеет значение 0x00000008 или больше, сервер должен проверить \_ значение поля улчекксум для следующих сообщений:</span><span class="sxs-lookup"><span data-stu-id="a573a-3087">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="a573a-3088">кпмконнектин</span><span class="sxs-lookup"><span data-stu-id="a573a-3088">CPMConnectIn</span></span>
-   <span data-ttu-id="a573a-3089">кпмкреатекуерин</span><span class="sxs-lookup"><span data-stu-id="a573a-3089">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="a573a-3090">кпмфетчвалуеин</span><span class="sxs-lookup"><span data-stu-id="a573a-3090">CPMFetchValueIn</span></span>
-   <span data-ttu-id="a573a-3091">кпмжетровсин</span><span class="sxs-lookup"><span data-stu-id="a573a-3091">CPMGetRowsIn</span></span>
-   <span data-ttu-id="a573a-3092">кпмсетбиндингсин</span><span class="sxs-lookup"><span data-stu-id="a573a-3092">CPMSetBindingsIn</span></span>

<span data-ttu-id="a573a-3093">Дополнительные сведения о том, как сервер проверяет значение, указанное клиентом в поле Улчекксум, для сообщений, перечисленных выше, см. в разделе 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="a573a-3093">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="a573a-3094">Если значение больше 0x00000008, предполагается, что клиент может обрабатывать 64-битные смещения в сообщениях Кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-3094">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="a573a-3095">Дополнительные сведения см. в разделе 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="a573a-3095">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="a573a-3096">*Поведение Windows. в клиентах Windows параметр иклиентверсион устанавливается следующим* образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-3096">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="a573a-3097">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-3097">Value</span></span>      | <span data-ttu-id="a573a-3098">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-3098">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="a573a-3099">0x00000005</span><span class="sxs-lookup"><span data-stu-id="a573a-3099">0x00000005</span></span> | <span data-ttu-id="a573a-3100">Клиентская ОС — Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a573a-3100">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="a573a-3101">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a573a-3101">0x00000008</span></span> | <span data-ttu-id="a573a-3102">Клиентская ОС — 32-разрядная версия Windows XP или 32-разрядная версия Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a573a-3102">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="a573a-3103">0x00010008</span><span class="sxs-lookup"><span data-stu-id="a573a-3103">0x00010008</span></span> | <span data-ttu-id="a573a-3104">Клиентская ОС — 64-разрядная версия Windows XP или 64-разрядная версия Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a573a-3104">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="a573a-3105">\_**фклиентисремоте**: логическое значение, указывающее, работает ли клиент на компьютере, отличном от компьютера, на котором находится сервер.</span><span class="sxs-lookup"><span data-stu-id="a573a-3105">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="a573a-3106">НЕОБХОДИМО задать значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="a573a-3106">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="a573a-3107">\_**cbBlob1**: 32-разрядное целое число без знака, указывающее размер в байтах для полей Кпропсет, PropertySet1 и PropertySet2 в сочетании.</span><span class="sxs-lookup"><span data-stu-id="a573a-3107">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="a573a-3108">\_**cbBlob2**: 32-разрядное целое число без знака, указывающее размер в байтах для полей Цекспропсет и апропертисет в сочетании.</span><span class="sxs-lookup"><span data-stu-id="a573a-3108">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="a573a-3109">\_**Заполнение**: 12 байтов заполнения, которые могут содержать произвольные значения, и должны игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-3109">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="a573a-3110">**MachineName**— имя компьютера клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-3110">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="a573a-3111">Строка имени должна быть массивом, заканчивающимся нулем, размером менее 512 символов Юникода, включая знак завершения NULL.</span><span class="sxs-lookup"><span data-stu-id="a573a-3111">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="a573a-3112">**Username**— строка, представляющая имя пользователя, запустившего приложение, которое вызвало этот протокол.</span><span class="sxs-lookup"><span data-stu-id="a573a-3112">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="a573a-3113">Строка имени должна быть массивом, заканчивающимся нулем, размером менее 512 символов Юникода при объединении с MachineName.</span><span class="sxs-lookup"><span data-stu-id="a573a-3113">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="a573a-3114">**\_ паддингкпропсетс**: длина этого поля должна быть от 0 до 7 байт.</span><span class="sxs-lookup"><span data-stu-id="a573a-3114">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="a573a-3115">Число байтов должно быть числом, необходимым для смещения в байтах поля Кпропсетс с начала сообщения, содержащего эту структуру, кратной 8.</span><span class="sxs-lookup"><span data-stu-id="a573a-3115">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="a573a-3116">Значение байт может быть любым произвольным значением и должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-3116">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="a573a-3117">**кпропсетс**: 32-разрядное целое число без знака, указывающее количество структур кдбпропсет, следующих за этим полем.</span><span class="sxs-lookup"><span data-stu-id="a573a-3117">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="a573a-3118">Это значение должно быть равно 0x0000002.</span><span class="sxs-lookup"><span data-stu-id="a573a-3118">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="a573a-3119">**PropertySet1**: структура Кдбпропсет с гуидпропертисет, содержащей DBPROPSET \_ фсЦифрмврк \_ ext (см. раздел 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="a573a-3119">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="a573a-3120">**PropertySet2**: структура Кдбпропсет с гуидпропертисет, содержащей DBPROPSET \_ Цифрмврккоре \_ ext (см. раздел 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="a573a-3120">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="a573a-3121">\_**Паддинжекстпропсет**: длина этого поля должна быть от 0 до 7 байт.</span><span class="sxs-lookup"><span data-stu-id="a573a-3121">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="a573a-3122">Число байтов должно быть числом, необходимым для смещения в байтах поля Цекстпропсетс с начала сообщения, содержащего эту структуру, кратной 8.</span><span class="sxs-lookup"><span data-stu-id="a573a-3122">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="a573a-3123">Значение байт может быть любым произвольным значением и должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-3123">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="a573a-3124">**цекстпропсет**: 32-разрядное целое число без знака, указывающее количество структур кдбпропсет, следующих за этим полем.</span><span class="sxs-lookup"><span data-stu-id="a573a-3124">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="a573a-3125">**апропертисетс**: массив структур кдбпропсет, задающий другие свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-3125">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="a573a-3126">Число элементов в этом массиве должно быть равно Цекстпропсет.</span><span class="sxs-lookup"><span data-stu-id="a573a-3126">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="a573a-3127">2.2.3.7 Кпмконнектаут</span><span class="sxs-lookup"><span data-stu-id="a573a-3127">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="a573a-3128">Сообщение Кпмконнектаут содержит ответ на сообщение Кпмконнектин.</span><span class="sxs-lookup"><span data-stu-id="a573a-3128">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="a573a-3129">Формат сообщения Кпмконнектаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3129">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="a573a-3130">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3130">0</span></span>

<span data-ttu-id="a573a-3131">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3131">1</span></span>

<span data-ttu-id="a573a-3132">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3132">2</span></span>

<span data-ttu-id="a573a-3133">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3133">3</span></span>

<span data-ttu-id="a573a-3134">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3134">4</span></span>

<span data-ttu-id="a573a-3135">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3135">5</span></span>

<span data-ttu-id="a573a-3136">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3136">6</span></span>

<span data-ttu-id="a573a-3137">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3137">7</span></span>

<span data-ttu-id="a573a-3138">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3138">8</span></span>

<span data-ttu-id="a573a-3139">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3139">9</span></span>

<span data-ttu-id="a573a-3140">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3140">1</span></span><br/> <span data-ttu-id="a573a-3141">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3141">0</span></span><br/>

<span data-ttu-id="a573a-3142">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3142">1</span></span>

<span data-ttu-id="a573a-3143">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3143">2</span></span>

<span data-ttu-id="a573a-3144">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3144">3</span></span>

<span data-ttu-id="a573a-3145">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3145">4</span></span>

<span data-ttu-id="a573a-3146">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3146">5</span></span>

<span data-ttu-id="a573a-3147">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3147">6</span></span>

<span data-ttu-id="a573a-3148">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3148">7</span></span>

<span data-ttu-id="a573a-3149">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3149">8</span></span>

<span data-ttu-id="a573a-3150">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3150">9</span></span>

<span data-ttu-id="a573a-3151">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3151">2</span></span><br/> <span data-ttu-id="a573a-3152">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3152">0</span></span><br/>

<span data-ttu-id="a573a-3153">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3153">1</span></span>

<span data-ttu-id="a573a-3154">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3154">2</span></span>

<span data-ttu-id="a573a-3155">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3155">3</span></span>

<span data-ttu-id="a573a-3156">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3156">4</span></span>

<span data-ttu-id="a573a-3157">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3157">5</span></span>

<span data-ttu-id="a573a-3158">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3158">6</span></span>

<span data-ttu-id="a573a-3159">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3159">7</span></span>

<span data-ttu-id="a573a-3160">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3160">8</span></span>

<span data-ttu-id="a573a-3161">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3161">9</span></span>

<span data-ttu-id="a573a-3162">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3162">3</span></span><br/> <span data-ttu-id="a573a-3163">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3163">0</span></span><br/>

<span data-ttu-id="a573a-3164">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3164">1</span></span>

<span data-ttu-id="a573a-3165">\_serverVersion</span><span class="sxs-lookup"><span data-stu-id="a573a-3165">\_serverVersion</span></span>

<span data-ttu-id="a573a-3166">\_зарезервировано (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-3166">\_reserved (variable)</span></span>



 

<span data-ttu-id="a573a-3167">**\_ serverVersion**:</span><span class="sxs-lookup"><span data-stu-id="a573a-3167">**\_serverVersion**:</span></span>

<span data-ttu-id="a573a-3168">32-разрядное целое число, указывающее, может ли сервер поддерживать 64-битное смещение *.*</span><span class="sxs-lookup"><span data-stu-id="a573a-3168">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="a573a-3169">Дополнительные сведения см. в разделе 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="a573a-3169">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="a573a-3170">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-3170">Value</span></span>      | <span data-ttu-id="a573a-3171">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-3171">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="a573a-3172">0x00000007</span><span class="sxs-lookup"><span data-stu-id="a573a-3172">0x00000007</span></span> | <span data-ttu-id="a573a-3173">Сервер может передавать только 32-разрядные смещения.</span><span class="sxs-lookup"><span data-stu-id="a573a-3173">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="a573a-3174">0x00010007</span><span class="sxs-lookup"><span data-stu-id="a573a-3174">0x00010007</span></span> | <span data-ttu-id="a573a-3175">Сервер может передавать 32 или 64-битные смещения.</span><span class="sxs-lookup"><span data-stu-id="a573a-3175">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="a573a-3176">**\_ зарезервировано**: зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="a573a-3176">**\_reserved**: Reserved.</span></span> <span data-ttu-id="a573a-3177">Сервер может отправить произвольное число произвольных значений, и клиент должен игнорировать эти значения, если они есть.</span><span class="sxs-lookup"><span data-stu-id="a573a-3177">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="a573a-3178">2.2.3.8 Кпмкреатекуерин</span><span class="sxs-lookup"><span data-stu-id="a573a-3178">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="a573a-3179">Сообщение Кпмкреатекуерин создает новый запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-3179">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="a573a-3180">Формат сообщения Кпмкреатекуерин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3180">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-3181">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3181">0</span></span>

<span data-ttu-id="a573a-3182">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3182">1</span></span>

<span data-ttu-id="a573a-3183">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3183">2</span></span>

<span data-ttu-id="a573a-3184">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3184">3</span></span>

<span data-ttu-id="a573a-3185">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3185">4</span></span>

<span data-ttu-id="a573a-3186">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3186">5</span></span>

<span data-ttu-id="a573a-3187">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3187">6</span></span>

<span data-ttu-id="a573a-3188">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3188">7</span></span>

<span data-ttu-id="a573a-3189">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3189">8</span></span>

<span data-ttu-id="a573a-3190">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3190">9</span></span>

<span data-ttu-id="a573a-3191">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3191">1</span></span><br/> <span data-ttu-id="a573a-3192">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3192">0</span></span><br/>

<span data-ttu-id="a573a-3193">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3193">1</span></span>

<span data-ttu-id="a573a-3194">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3194">2</span></span>

<span data-ttu-id="a573a-3195">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3195">3</span></span>

<span data-ttu-id="a573a-3196">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3196">4</span></span>

<span data-ttu-id="a573a-3197">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3197">5</span></span>

<span data-ttu-id="a573a-3198">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3198">6</span></span>

<span data-ttu-id="a573a-3199">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3199">7</span></span>

<span data-ttu-id="a573a-3200">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3200">8</span></span>

<span data-ttu-id="a573a-3201">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3201">9</span></span>

<span data-ttu-id="a573a-3202">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3202">2</span></span><br/> <span data-ttu-id="a573a-3203">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3203">0</span></span><br/>

<span data-ttu-id="a573a-3204">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3204">1</span></span>

<span data-ttu-id="a573a-3205">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3205">2</span></span>

<span data-ttu-id="a573a-3206">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3206">3</span></span>

<span data-ttu-id="a573a-3207">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3207">4</span></span>

<span data-ttu-id="a573a-3208">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3208">5</span></span>

<span data-ttu-id="a573a-3209">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3209">6</span></span>

<span data-ttu-id="a573a-3210">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3210">7</span></span>

<span data-ttu-id="a573a-3211">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3211">8</span></span>

<span data-ttu-id="a573a-3212">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3212">9</span></span>

<span data-ttu-id="a573a-3213">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3213">3</span></span><br/> <span data-ttu-id="a573a-3214">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3214">0</span></span><br/>

<span data-ttu-id="a573a-3215">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3215">1</span></span>

<span data-ttu-id="a573a-3216">Размер</span><span class="sxs-lookup"><span data-stu-id="a573a-3216">Size</span></span>

<span data-ttu-id="a573a-3217">кколумнсетпресент</span><span class="sxs-lookup"><span data-stu-id="a573a-3217">CColumnSetPresent</span></span>

<span data-ttu-id="a573a-3218">(Необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-3218">ColumnSet (optional)</span></span>

<span data-ttu-id="a573a-3219">... перемен</span><span class="sxs-lookup"><span data-stu-id="a573a-3219">... (variable)</span></span>

<span data-ttu-id="a573a-3220">Крестриктионпресент.</span><span class="sxs-lookup"><span data-stu-id="a573a-3220">CRestrictionPresent.</span></span>

<span data-ttu-id="a573a-3221">Ограничение (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-3221">Restriction (optional)</span></span>

<span data-ttu-id="a573a-3222">... перемен</span><span class="sxs-lookup"><span data-stu-id="a573a-3222">... (variable)</span></span>

<span data-ttu-id="a573a-3223">ксортсетпресент</span><span class="sxs-lookup"><span data-stu-id="a573a-3223">CSortSetPresent</span></span>

<span data-ttu-id="a573a-3224">Тип сортировки (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-3224">SortSet (optional)</span></span>

<span data-ttu-id="a573a-3225">... перемен</span><span class="sxs-lookup"><span data-stu-id="a573a-3225">... (variable)</span></span>

<span data-ttu-id="a573a-3226">ккатегоризатионсетпресент</span><span class="sxs-lookup"><span data-stu-id="a573a-3226">CCategorizationSetPresent</span></span>

<span data-ttu-id="a573a-3227">Категоризатионсет (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-3227">CategorizationSet (optional)</span></span>

<span data-ttu-id="a573a-3228">... перемен</span><span class="sxs-lookup"><span data-stu-id="a573a-3228">... (variable)</span></span>

<span data-ttu-id="a573a-3229">ровсетпропертиес</span><span class="sxs-lookup"><span data-stu-id="a573a-3229">RowSetProperties</span></span>

<span data-ttu-id="a573a-3230">...</span><span class="sxs-lookup"><span data-stu-id="a573a-3230">...</span></span>

<span data-ttu-id="a573a-3231">...</span><span class="sxs-lookup"><span data-stu-id="a573a-3231">...</span></span>

<span data-ttu-id="a573a-3232">...</span><span class="sxs-lookup"><span data-stu-id="a573a-3232">...</span></span>

<span data-ttu-id="a573a-3233">...</span><span class="sxs-lookup"><span data-stu-id="a573a-3233">...</span></span>

<span data-ttu-id="a573a-3234">Пидмаппер (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-3234">PidMapper (variable)</span></span>



 

<span data-ttu-id="a573a-3235">**Размер**: 32-разрядное целое число без знака, указывающее число байтов от начала этого поля до конца сообщения.</span><span class="sxs-lookup"><span data-stu-id="a573a-3235">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="a573a-3236">**Кколумнсетпресент**: поле byte, указывающее, имеется ли поле с набором столбцов.</span><span class="sxs-lookup"><span data-stu-id="a573a-3236">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="a573a-3237">Для этого поля необходимо задать значение 0x01 или 0x00.</span><span class="sxs-lookup"><span data-stu-id="a573a-3237">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="a573a-3238">Если задано значение 0x01, поле Кколумнсет должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-3238">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="a573a-3239">Если задано значение 0x00, оно должно отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-3239">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="a573a-3240">Набор **столбцов**: структура кколумнсет, содержащая номера столбцов, в которых должны возвращаться свойства кпидмаппер.</span><span class="sxs-lookup"><span data-stu-id="a573a-3240">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="a573a-3241">**Крестриктионпресент**: поле byte, указывающее, имеется ли поле ограничения.</span><span class="sxs-lookup"><span data-stu-id="a573a-3241">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="a573a-3242">Если задано любое ненулевое значение, поле ограничения должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-3242">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="a573a-3243">Если задано значение 0x00, ограничение должно отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-3243">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="a573a-3244">**Ограничение**: структура крестриктион, содержащая дерево команд запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3244">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="a573a-3245">**Ксортсетпресент**: поле byte, указывающее, имеется ли поле Sorting.</span><span class="sxs-lookup"><span data-stu-id="a573a-3245">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="a573a-3246">Если задано любое ненулевое значение, поле Sorting должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-3246">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="a573a-3247">Если задано значение 0x00, то параметр Sort должен отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-3247">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="a573a-3248">Набор **сортировки**: структура ксортсет, указывающая порядок сортировки запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3248">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="a573a-3249">**Ккатегоризатионсетпресент**: поле byte, указывающее, имеется ли поле ккатегоризатионсет.</span><span class="sxs-lookup"><span data-stu-id="a573a-3249">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="a573a-3250">Если задано любое ненулевое значение, поле Ккатегоризатионсет должно присутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-3250">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="a573a-3251">Если задано значение 0x00, Ккатегоризатионсет должно отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="a573a-3251">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="a573a-3252">**Ккатегоризатионсет**: структура ккатегоризатионсет, содержащая группы для запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3252">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="a573a-3253">**Ровсетпропертиес**: структура кровсетпропертиес, предоставляющая сведения о конфигурации для запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3253">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="a573a-3254">**Пидмаппер**: структура кпидмаппер, содержащая свойства, возвращаемые в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3254">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="a573a-3255">2.2.3.9 Кпмкреатекуерйоут</span><span class="sxs-lookup"><span data-stu-id="a573a-3255">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="a573a-3256">Сообщение Кпмкреатекуерйоут содержит ответ на сообщение Кпмкреатекуерин.</span><span class="sxs-lookup"><span data-stu-id="a573a-3256">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="a573a-3257">Формат сообщения Кпмкреатекуерйоут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3257">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="a573a-3258">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3258">0</span></span>

<span data-ttu-id="a573a-3259">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3259">1</span></span>

<span data-ttu-id="a573a-3260">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3260">2</span></span>

<span data-ttu-id="a573a-3261">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3261">3</span></span>

<span data-ttu-id="a573a-3262">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3262">4</span></span>

<span data-ttu-id="a573a-3263">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3263">5</span></span>

<span data-ttu-id="a573a-3264">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3264">6</span></span>

<span data-ttu-id="a573a-3265">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3265">7</span></span>

<span data-ttu-id="a573a-3266">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3266">8</span></span>

<span data-ttu-id="a573a-3267">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3267">9</span></span>

<span data-ttu-id="a573a-3268">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3268">1</span></span><br/> <span data-ttu-id="a573a-3269">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3269">0</span></span><br/>

<span data-ttu-id="a573a-3270">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3270">1</span></span>

<span data-ttu-id="a573a-3271">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3271">2</span></span>

<span data-ttu-id="a573a-3272">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3272">3</span></span>

<span data-ttu-id="a573a-3273">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3273">4</span></span>

<span data-ttu-id="a573a-3274">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3274">5</span></span>

<span data-ttu-id="a573a-3275">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3275">6</span></span>

<span data-ttu-id="a573a-3276">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3276">7</span></span>

<span data-ttu-id="a573a-3277">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3277">8</span></span>

<span data-ttu-id="a573a-3278">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3278">9</span></span>

<span data-ttu-id="a573a-3279">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3279">2</span></span><br/> <span data-ttu-id="a573a-3280">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3280">0</span></span><br/>

<span data-ttu-id="a573a-3281">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3281">1</span></span>

<span data-ttu-id="a573a-3282">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3282">2</span></span>

<span data-ttu-id="a573a-3283">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3283">3</span></span>

<span data-ttu-id="a573a-3284">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3284">4</span></span>

<span data-ttu-id="a573a-3285">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3285">5</span></span>

<span data-ttu-id="a573a-3286">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3286">6</span></span>

<span data-ttu-id="a573a-3287">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3287">7</span></span>

<span data-ttu-id="a573a-3288">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3288">8</span></span>

<span data-ttu-id="a573a-3289">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3289">9</span></span>

<span data-ttu-id="a573a-3290">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3290">3</span></span><br/> <span data-ttu-id="a573a-3291">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3291">0</span></span><br/>

<span data-ttu-id="a573a-3292">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3292">1</span></span>

<span data-ttu-id="a573a-3293">\_фтруесекуентиал</span><span class="sxs-lookup"><span data-stu-id="a573a-3293">\_fTrueSequential</span></span>

<span data-ttu-id="a573a-3294">\_фворкидуникуе</span><span class="sxs-lookup"><span data-stu-id="a573a-3294">\_fWorkIdUnique</span></span>

<span data-ttu-id="a573a-3295">акурсорс</span><span class="sxs-lookup"><span data-stu-id="a573a-3295">aCursors</span></span>



 

<span data-ttu-id="a573a-3296">**\_ фтруесекуентиал**: информативное логическое значение, указывающее, может ли запрос получать результаты быстрее.</span><span class="sxs-lookup"><span data-stu-id="a573a-3296">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="a573a-3297">Если для запроса, предоставленного в Кпмкреатекуерин, задано 0x00000001, сервер может использовать индекс таким образом, чтобы результаты запроса могли быть доставлены быстрее.</span><span class="sxs-lookup"><span data-stu-id="a573a-3297">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="a573a-3298">Если задано значение 0x00000000, то при доставке результатов запроса будет воздержаться задержка.</span><span class="sxs-lookup"><span data-stu-id="a573a-3298">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="a573a-3299">Не должно быть задано ни одно другое значение.</span><span class="sxs-lookup"><span data-stu-id="a573a-3299">MUST not be set to any other value.</span></span>

<span data-ttu-id="a573a-3300">**\_ фворкидуникуе**: логическое значение, указывающее, являются ли идентификаторы документов, на которые указывают курсоры, уникальными в результатах запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3300">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="a573a-3301">Если задано значение 0x00000001, идентификаторы являются уникальными.</span><span class="sxs-lookup"><span data-stu-id="a573a-3301">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="a573a-3302">Если задано значение 0x00000000, они уникальны только во всем наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3302">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="a573a-3303">**акурсорс**: массив из 32-разрядных целых чисел без знака, представляющих дескрипторы курсоров, с числом элементов, равным числу категорий в поле Категоризатионсет сообщения кпмкреатекуерин.</span><span class="sxs-lookup"><span data-stu-id="a573a-3303">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="a573a-3304">2.2.3.10 Кпмжеткуеристатусин</span><span class="sxs-lookup"><span data-stu-id="a573a-3304">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="a573a-3305">Сообщение Кпмжеткуеристатусин запрашивает состояние запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3305">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="a573a-3306">Формат сообщения Кпмжеткуеристатусин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3306">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-3307">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3307">0</span></span>

<span data-ttu-id="a573a-3308">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3308">1</span></span>

<span data-ttu-id="a573a-3309">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3309">2</span></span>

<span data-ttu-id="a573a-3310">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3310">3</span></span>

<span data-ttu-id="a573a-3311">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3311">4</span></span>

<span data-ttu-id="a573a-3312">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3312">5</span></span>

<span data-ttu-id="a573a-3313">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3313">6</span></span>

<span data-ttu-id="a573a-3314">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3314">7</span></span>

<span data-ttu-id="a573a-3315">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3315">8</span></span>

<span data-ttu-id="a573a-3316">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3316">9</span></span>

<span data-ttu-id="a573a-3317">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3317">1</span></span><br/> <span data-ttu-id="a573a-3318">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3318">0</span></span><br/>

<span data-ttu-id="a573a-3319">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3319">1</span></span>

<span data-ttu-id="a573a-3320">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3320">2</span></span>

<span data-ttu-id="a573a-3321">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3321">3</span></span>

<span data-ttu-id="a573a-3322">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3322">4</span></span>

<span data-ttu-id="a573a-3323">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3323">5</span></span>

<span data-ttu-id="a573a-3324">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3324">6</span></span>

<span data-ttu-id="a573a-3325">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3325">7</span></span>

<span data-ttu-id="a573a-3326">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3326">8</span></span>

<span data-ttu-id="a573a-3327">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3327">9</span></span>

<span data-ttu-id="a573a-3328">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3328">2</span></span><br/> <span data-ttu-id="a573a-3329">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3329">0</span></span><br/>

<span data-ttu-id="a573a-3330">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3330">1</span></span>

<span data-ttu-id="a573a-3331">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3331">2</span></span>

<span data-ttu-id="a573a-3332">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3332">3</span></span>

<span data-ttu-id="a573a-3333">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3333">4</span></span>

<span data-ttu-id="a573a-3334">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3334">5</span></span>

<span data-ttu-id="a573a-3335">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3335">6</span></span>

<span data-ttu-id="a573a-3336">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3336">7</span></span>

<span data-ttu-id="a573a-3337">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3337">8</span></span>

<span data-ttu-id="a573a-3338">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3338">9</span></span>

<span data-ttu-id="a573a-3339">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3339">3</span></span><br/> <span data-ttu-id="a573a-3340">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3340">0</span></span><br/>

<span data-ttu-id="a573a-3341">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3341">1</span></span>

<span data-ttu-id="a573a-3342">\_хкурсор</span><span class="sxs-lookup"><span data-stu-id="a573a-3342">\_hCursor</span></span>



 

<span data-ttu-id="a573a-3343">**\_ хкурсор**: 32-разрядное целое число без знака, представляющее маркер из сообщения кпмкреатекуерйоут, идентифицирующего запрос, для которого необходимо получить сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="a573a-3343">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="a573a-3344">2.2.3.11 Кпмжеткуеристатусаут</span><span class="sxs-lookup"><span data-stu-id="a573a-3344">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="a573a-3345">Сообщение Кпмжеткуеристатусаут отвечает на сообщение Кпмжеткуеристатусин с состоянием запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3345">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="a573a-3346">Формат сообщения Кпмжеткуеристатусаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3346">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="a573a-3347">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3347">0</span></span>

<span data-ttu-id="a573a-3348">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3348">1</span></span>

<span data-ttu-id="a573a-3349">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3349">2</span></span>

<span data-ttu-id="a573a-3350">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3350">3</span></span>

<span data-ttu-id="a573a-3351">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3351">4</span></span>

<span data-ttu-id="a573a-3352">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3352">5</span></span>

<span data-ttu-id="a573a-3353">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3353">6</span></span>

<span data-ttu-id="a573a-3354">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3354">7</span></span>

<span data-ttu-id="a573a-3355">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3355">8</span></span>

<span data-ttu-id="a573a-3356">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3356">9</span></span>

<span data-ttu-id="a573a-3357">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3357">1</span></span><br/> <span data-ttu-id="a573a-3358">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3358">0</span></span><br/>

<span data-ttu-id="a573a-3359">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3359">1</span></span>

<span data-ttu-id="a573a-3360">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3360">2</span></span>

<span data-ttu-id="a573a-3361">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3361">3</span></span>

<span data-ttu-id="a573a-3362">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3362">4</span></span>

<span data-ttu-id="a573a-3363">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3363">5</span></span>

<span data-ttu-id="a573a-3364">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3364">6</span></span>

<span data-ttu-id="a573a-3365">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3365">7</span></span>

<span data-ttu-id="a573a-3366">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3366">8</span></span>

<span data-ttu-id="a573a-3367">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3367">9</span></span>

<span data-ttu-id="a573a-3368">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3368">2</span></span><br/> <span data-ttu-id="a573a-3369">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3369">0</span></span><br/>

<span data-ttu-id="a573a-3370">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3370">1</span></span>

<span data-ttu-id="a573a-3371">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3371">2</span></span>

<span data-ttu-id="a573a-3372">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3372">3</span></span>

<span data-ttu-id="a573a-3373">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3373">4</span></span>

<span data-ttu-id="a573a-3374">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3374">5</span></span>

<span data-ttu-id="a573a-3375">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3375">6</span></span>

<span data-ttu-id="a573a-3376">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3376">7</span></span>

<span data-ttu-id="a573a-3377">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3377">8</span></span>

<span data-ttu-id="a573a-3378">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3378">9</span></span>

<span data-ttu-id="a573a-3379">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3379">3</span></span><br/> <span data-ttu-id="a573a-3380">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3380">0</span></span><br/>

<span data-ttu-id="a573a-3381">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3381">1</span></span>

<span data-ttu-id="a573a-3382">\_Состояние</span><span class="sxs-lookup"><span data-stu-id="a573a-3382">\_Status</span></span>



 

<span data-ttu-id="a573a-3383">**\_ Состояние**: битовая маска значений, определенных в таблицах ниже, которая описывает запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-3383">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="a573a-3384">В следующей таблице перечислены \_ \* значения Stat, полученные путем выполнения побитовой операции и для \_ состояния с 0x00000007.</span><span class="sxs-lookup"><span data-stu-id="a573a-3384">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="a573a-3385">Результат должен быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="a573a-3385">The result MUST be one of the following:</span></span>



| <span data-ttu-id="a573a-3386">Константа</span><span class="sxs-lookup"><span data-stu-id="a573a-3386">Constant</span></span>                 | <span data-ttu-id="a573a-3387">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-3387">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-3388">STAT \_ занято 0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-3388">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="a573a-3389">Асинхронный запрос все еще выполняется.</span><span class="sxs-lookup"><span data-stu-id="a573a-3389">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="a573a-3390">\_Ошибка stat 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-3390">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="a573a-3391">Запрос находится в состоянии ошибки.</span><span class="sxs-lookup"><span data-stu-id="a573a-3391">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="a573a-3392">РЕГЛАМЕНТное \_ Завершение 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-3392">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="a573a-3393">Запрос завершен.</span><span class="sxs-lookup"><span data-stu-id="a573a-3393">The query is complete.</span></span>                                                            |
| <span data-ttu-id="a573a-3394">STAT \_ Refresh 0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-3394">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="a573a-3395">Запрос завершен, но обновления приводят к дополнительным вычислениям запросов.</span><span class="sxs-lookup"><span data-stu-id="a573a-3395">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="a573a-3396">В следующей таблице перечислены дополнительные \_ \* биты Stat, которые можно задать независимо.</span><span class="sxs-lookup"><span data-stu-id="a573a-3396">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="a573a-3397">Константа</span><span class="sxs-lookup"><span data-stu-id="a573a-3397">Constant</span></span>                                    | <span data-ttu-id="a573a-3398">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-3398">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a573a-3399">STAT \_ пропускаемых \_ слов 0x00000010</span><span class="sxs-lookup"><span data-stu-id="a573a-3399">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="a573a-3400">Пропускаемые слова были заменены символами-шаблонами в запросе содержимого.</span><span class="sxs-lookup"><span data-stu-id="a573a-3400">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="a573a-3401">\_ \_ \_ Неактуальное содержимое \_ stat</span><span class="sxs-lookup"><span data-stu-id="a573a-3401">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="a573a-3402">Результаты запроса могут быть неверными, так как в запросе были внесены измененные, но неиндексированные файлы.</span><span class="sxs-lookup"><span data-stu-id="a573a-3402">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="a573a-3403">\_Неполное обновление stat \_ 0x00000040</span><span class="sxs-lookup"><span data-stu-id="a573a-3403">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="a573a-3404">Результаты запроса могут быть неверными, так как запрос содержал измененные и повторно индексированные файлы, содержимое которых не было указано.</span><span class="sxs-lookup"><span data-stu-id="a573a-3404">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="a573a-3405">\_Неполный \_ запрос содержимого stat \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="a573a-3405">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="a573a-3406">Запрос содержимого был слишком сложен для завершения или обязательного перечисления вместо использования индекса содержимого.</span><span class="sxs-lookup"><span data-stu-id="a573a-3406">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="a573a-3407">\_Превышено ограничение по времени stat \_ \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="a573a-3407">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="a573a-3408">Результаты запроса могут быть неверными, так как время выполнения запроса достигло максимально допустимого времени.</span><span class="sxs-lookup"><span data-stu-id="a573a-3408">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="a573a-3409">2.2.3.12 Кпмжеткуеристатусексин</span><span class="sxs-lookup"><span data-stu-id="a573a-3409">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="a573a-3410">Сообщение Кпмжеткуеристатусексин запрашивает состояние запроса и дополнительную информацию, например количество индексируемых документов, количество документов, оставшихся для индексирования, и т. д.</span><span class="sxs-lookup"><span data-stu-id="a573a-3410">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="a573a-3411">Формат сообщения Кпмжеткуеристатусексин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3411">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-3412">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3412">0</span></span>

<span data-ttu-id="a573a-3413">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3413">1</span></span>

<span data-ttu-id="a573a-3414">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3414">2</span></span>

<span data-ttu-id="a573a-3415">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3415">3</span></span>

<span data-ttu-id="a573a-3416">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3416">4</span></span>

<span data-ttu-id="a573a-3417">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3417">5</span></span>

<span data-ttu-id="a573a-3418">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3418">6</span></span>

<span data-ttu-id="a573a-3419">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3419">7</span></span>

<span data-ttu-id="a573a-3420">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3420">8</span></span>

<span data-ttu-id="a573a-3421">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3421">9</span></span>

<span data-ttu-id="a573a-3422">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3422">1</span></span><br/> <span data-ttu-id="a573a-3423">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3423">0</span></span><br/>

<span data-ttu-id="a573a-3424">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3424">1</span></span>

<span data-ttu-id="a573a-3425">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3425">2</span></span>

<span data-ttu-id="a573a-3426">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3426">3</span></span>

<span data-ttu-id="a573a-3427">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3427">4</span></span>

<span data-ttu-id="a573a-3428">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3428">5</span></span>

<span data-ttu-id="a573a-3429">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3429">6</span></span>

<span data-ttu-id="a573a-3430">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3430">7</span></span>

<span data-ttu-id="a573a-3431">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3431">8</span></span>

<span data-ttu-id="a573a-3432">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3432">9</span></span>

<span data-ttu-id="a573a-3433">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3433">2</span></span><br/> <span data-ttu-id="a573a-3434">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3434">0</span></span><br/>

<span data-ttu-id="a573a-3435">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3435">1</span></span>

<span data-ttu-id="a573a-3436">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3436">2</span></span>

<span data-ttu-id="a573a-3437">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3437">3</span></span>

<span data-ttu-id="a573a-3438">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3438">4</span></span>

<span data-ttu-id="a573a-3439">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3439">5</span></span>

<span data-ttu-id="a573a-3440">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3440">6</span></span>

<span data-ttu-id="a573a-3441">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3441">7</span></span>

<span data-ttu-id="a573a-3442">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3442">8</span></span>

<span data-ttu-id="a573a-3443">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3443">9</span></span>

<span data-ttu-id="a573a-3444">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3444">3</span></span><br/> <span data-ttu-id="a573a-3445">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3445">0</span></span><br/>

<span data-ttu-id="a573a-3446">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3446">1</span></span>

<span data-ttu-id="a573a-3447">\_хкурсор</span><span class="sxs-lookup"><span data-stu-id="a573a-3447">\_hCursor</span></span>

<span data-ttu-id="a573a-3448">\_бмк</span><span class="sxs-lookup"><span data-stu-id="a573a-3448">\_bmk</span></span>



 

<span data-ttu-id="a573a-3449">**\_ хкурсор**: 32-разрядное значение, представляющее маркер из сообщения кпмкреатекуерйоут, идентифицирующего запрос, для которого необходимо получить сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="a573a-3449">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="a573a-3450">**\_ бмк**: 32-разрядное значение, указывающее маркер закладки, расположение которого необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="a573a-3450">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="a573a-3451">2.2.3.13 Кпмжеткуеристатусексаут</span><span class="sxs-lookup"><span data-stu-id="a573a-3451">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="a573a-3452">Сообщение Кпмжеткуеристатусексаут отвечает на сообщение Кпмжеткуеристатусексин с состоянием запроса и другими сведениями о состоянии, как описано на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="a573a-3452">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="a573a-3453">Формат сообщения Кпмжеткуеристатусексаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3453">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="a573a-3454">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3454">0</span></span>

<span data-ttu-id="a573a-3455">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3455">1</span></span>

<span data-ttu-id="a573a-3456">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3456">2</span></span>

<span data-ttu-id="a573a-3457">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3457">3</span></span>

<span data-ttu-id="a573a-3458">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3458">4</span></span>

<span data-ttu-id="a573a-3459">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3459">5</span></span>

<span data-ttu-id="a573a-3460">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3460">6</span></span>

<span data-ttu-id="a573a-3461">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3461">7</span></span>

<span data-ttu-id="a573a-3462">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3462">8</span></span>

<span data-ttu-id="a573a-3463">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3463">9</span></span>

<span data-ttu-id="a573a-3464">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3464">1</span></span><br/> <span data-ttu-id="a573a-3465">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3465">0</span></span><br/>

<span data-ttu-id="a573a-3466">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3466">1</span></span>

<span data-ttu-id="a573a-3467">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3467">2</span></span>

<span data-ttu-id="a573a-3468">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3468">3</span></span>

<span data-ttu-id="a573a-3469">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3469">4</span></span>

<span data-ttu-id="a573a-3470">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3470">5</span></span>

<span data-ttu-id="a573a-3471">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3471">6</span></span>

<span data-ttu-id="a573a-3472">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3472">7</span></span>

<span data-ttu-id="a573a-3473">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3473">8</span></span>

<span data-ttu-id="a573a-3474">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3474">9</span></span>

<span data-ttu-id="a573a-3475">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3475">2</span></span><br/> <span data-ttu-id="a573a-3476">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3476">0</span></span><br/>

<span data-ttu-id="a573a-3477">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3477">1</span></span>

<span data-ttu-id="a573a-3478">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3478">2</span></span>

<span data-ttu-id="a573a-3479">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3479">3</span></span>

<span data-ttu-id="a573a-3480">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3480">4</span></span>

<span data-ttu-id="a573a-3481">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3481">5</span></span>

<span data-ttu-id="a573a-3482">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3482">6</span></span>

<span data-ttu-id="a573a-3483">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3483">7</span></span>

<span data-ttu-id="a573a-3484">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3484">8</span></span>

<span data-ttu-id="a573a-3485">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3485">9</span></span>

<span data-ttu-id="a573a-3486">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3486">3</span></span><br/> <span data-ttu-id="a573a-3487">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3487">0</span></span><br/>

<span data-ttu-id="a573a-3488">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3488">1</span></span>

<span data-ttu-id="a573a-3489">\_Состояние</span><span class="sxs-lookup"><span data-stu-id="a573a-3489">\_Status</span></span>

<span data-ttu-id="a573a-3490">\_кфилтереддокументс</span><span class="sxs-lookup"><span data-stu-id="a573a-3490">\_cFilteredDocuments</span></span>

<span data-ttu-id="a573a-3491">\_кдокументстофилтер</span><span class="sxs-lookup"><span data-stu-id="a573a-3491">\_cDocumentsToFilter</span></span>

<span data-ttu-id="a573a-3492">\_двратиофинишедденоминатор</span><span class="sxs-lookup"><span data-stu-id="a573a-3492">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="a573a-3493">\_двратиофинишеднумератор</span><span class="sxs-lookup"><span data-stu-id="a573a-3493">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="a573a-3494">\_ировбмк</span><span class="sxs-lookup"><span data-stu-id="a573a-3494">\_iRowBmk</span></span>

<span data-ttu-id="a573a-3495">\_кровстотал</span><span class="sxs-lookup"><span data-stu-id="a573a-3495">\_cRowsTotal</span></span>



 

<span data-ttu-id="a573a-3496">**\_ Состояние**: один из stat \_ \* значения, указанные в разделе 2.2.3.11.</span><span class="sxs-lookup"><span data-stu-id="a573a-3496">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="a573a-3497">**\_ кфилтереддокументс**: 32-разрядное целое число без знака, указывающее количество индексируемых документов</span><span class="sxs-lookup"><span data-stu-id="a573a-3497">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="a573a-3498">**\_ кдокументстофилтер**: 32-разрядное целое число без знака, указывающее количество документов, которые еще остались для индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-3498">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="a573a-3499">**\_ двратиофинишедденоминатор**: 32-разрядное целое число без знака, указывающее знаменатель отношения документов, обработка которых завершена в результате запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3499">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="a573a-3500">**\_ двратиофинишеднумератор**: 32-битовое целое число без знака, указывающее числитель коэффициента документов, обработка которых завершена в результате запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3500">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="a573a-3501">**\_ ировбмк**: 32-разрядное целое число без знака, указывающее приблизительное расположение закладки в наборе строк с точки зрения строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3501">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="a573a-3502">**\_ кровстотал**: 32-битовое целое число без знака, указывающее общее количество строк в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3502">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="a573a-3503">2.2.3.14 Кпмсетбиндингсин</span><span class="sxs-lookup"><span data-stu-id="a573a-3503">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="a573a-3504">Сообщение Кпмсетбиндингсин запрашивает привязку столбцов к набору строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3504">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="a573a-3505">Сервер будет отвечать на сообщение запроса Кпмсетбиндингсин, используя раздел заголовка сообщения Кпмбиндингсин с результатами запроса, содержащимся в \_ поле Status (состояние).</span><span class="sxs-lookup"><span data-stu-id="a573a-3505">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="a573a-3506">Формат сообщения Кпмсетбиндингсин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3506">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-3507">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3507">0</span></span>

<span data-ttu-id="a573a-3508">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3508">1</span></span>

<span data-ttu-id="a573a-3509">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3509">2</span></span>

<span data-ttu-id="a573a-3510">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3510">3</span></span>

<span data-ttu-id="a573a-3511">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3511">4</span></span>

<span data-ttu-id="a573a-3512">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3512">5</span></span>

<span data-ttu-id="a573a-3513">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3513">6</span></span>

<span data-ttu-id="a573a-3514">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3514">7</span></span>

<span data-ttu-id="a573a-3515">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3515">8</span></span>

<span data-ttu-id="a573a-3516">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3516">9</span></span>

<span data-ttu-id="a573a-3517">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3517">1</span></span><br/> <span data-ttu-id="a573a-3518">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3518">0</span></span><br/>

<span data-ttu-id="a573a-3519">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3519">1</span></span>

<span data-ttu-id="a573a-3520">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3520">2</span></span>

<span data-ttu-id="a573a-3521">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3521">3</span></span>

<span data-ttu-id="a573a-3522">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3522">4</span></span>

<span data-ttu-id="a573a-3523">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3523">5</span></span>

<span data-ttu-id="a573a-3524">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3524">6</span></span>

<span data-ttu-id="a573a-3525">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3525">7</span></span>

<span data-ttu-id="a573a-3526">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3526">8</span></span>

<span data-ttu-id="a573a-3527">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3527">9</span></span>

<span data-ttu-id="a573a-3528">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3528">2</span></span><br/> <span data-ttu-id="a573a-3529">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3529">0</span></span><br/>

<span data-ttu-id="a573a-3530">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3530">1</span></span>

<span data-ttu-id="a573a-3531">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3531">2</span></span>

<span data-ttu-id="a573a-3532">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3532">3</span></span>

<span data-ttu-id="a573a-3533">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3533">4</span></span>

<span data-ttu-id="a573a-3534">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3534">5</span></span>

<span data-ttu-id="a573a-3535">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3535">6</span></span>

<span data-ttu-id="a573a-3536">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3536">7</span></span>

<span data-ttu-id="a573a-3537">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3537">8</span></span>

<span data-ttu-id="a573a-3538">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3538">9</span></span>

<span data-ttu-id="a573a-3539">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3539">3</span></span><br/> <span data-ttu-id="a573a-3540">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3540">0</span></span><br/>

<span data-ttu-id="a573a-3541">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3541">1</span></span>

<span data-ttu-id="a573a-3542">\_Хкурсор (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-3542">\_hCursor (optional)</span></span>

<span data-ttu-id="a573a-3543">\_Кбров (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-3543">\_cbRow (optional)</span></span>

<span data-ttu-id="a573a-3544">\_Кббиндингдеск (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-3544">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="a573a-3545">\_фиктивный (необязательный)</span><span class="sxs-lookup"><span data-stu-id="a573a-3545">\_dummy (optional)</span></span>

<span data-ttu-id="a573a-3546">Кколумнс (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-3546">cColumns (optional)</span></span>

<span data-ttu-id="a573a-3547">Аколумнс (переменная, необязательный)</span><span class="sxs-lookup"><span data-stu-id="a573a-3547">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="a573a-3548">**\_ хкурсор**: 32-разрядное значение, представляющее маркер из сообщения кпмкреатекуерйоут, идентифицирующего строку, для которой задаются привязки.</span><span class="sxs-lookup"><span data-stu-id="a573a-3548">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="a573a-3549">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="a573a-3549">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="a573a-3550">**\_ кбров**: 32-битовое целое число без знака, указывающее размер строки в байтах.</span><span class="sxs-lookup"><span data-stu-id="a573a-3550">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="a573a-3551">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="a573a-3551">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="a573a-3552">**\_ кббиндингдеск**: 32-разрядное целое число без знака, указывающее длину (в байтах) полей, следующих за \_ фиктивным полем.</span><span class="sxs-lookup"><span data-stu-id="a573a-3552">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="a573a-3553">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="a573a-3553">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="a573a-3554">**\_ фиктивное**: это поле не используется и должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-3554">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="a573a-3555">Для него можно задать любое произвольное значение.</span><span class="sxs-lookup"><span data-stu-id="a573a-3555">It can be set to any arbitrary value.</span></span> <span data-ttu-id="a573a-3556">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="a573a-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="a573a-3557">**кколумнс**: 32-разрядное целое число без знака, указывающее количество элементов в массиве аколумнс.</span><span class="sxs-lookup"><span data-stu-id="a573a-3557">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="a573a-3558">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="a573a-3558">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="a573a-3559">**аколумнс**: массив структур ктаблеколумн, описывающих столбцы строки в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3559">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="a573a-3560">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="a573a-3560">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="a573a-3561">Структуры в массиве должны быть разделены от 0 до 3 байтов с отступом таким, что каждая структура имеет 4-байтовое выравнивание от начала сообщения.</span><span class="sxs-lookup"><span data-stu-id="a573a-3561">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="a573a-3562">Такое заполнение байтов может быть любым произвольным значением и не должно учитываться при получении.</span><span class="sxs-lookup"><span data-stu-id="a573a-3562">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="a573a-3563">2.2.3.15 Кпмжетровсин</span><span class="sxs-lookup"><span data-stu-id="a573a-3563">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="a573a-3564">Сообщение Кпмжетровсин запрашивает строки из запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3564">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="a573a-3565">Формат сообщения Кпмжетровсин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3565">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-3566">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3566">0</span></span>

<span data-ttu-id="a573a-3567">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3567">1</span></span>

<span data-ttu-id="a573a-3568">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3568">2</span></span>

<span data-ttu-id="a573a-3569">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3569">3</span></span>

<span data-ttu-id="a573a-3570">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3570">4</span></span>

<span data-ttu-id="a573a-3571">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3571">5</span></span>

<span data-ttu-id="a573a-3572">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3572">6</span></span>

<span data-ttu-id="a573a-3573">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3573">7</span></span>

<span data-ttu-id="a573a-3574">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3574">8</span></span>

<span data-ttu-id="a573a-3575">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3575">9</span></span>

<span data-ttu-id="a573a-3576">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3576">1</span></span><br/> <span data-ttu-id="a573a-3577">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3577">0</span></span><br/>

<span data-ttu-id="a573a-3578">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3578">1</span></span>

<span data-ttu-id="a573a-3579">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3579">2</span></span>

<span data-ttu-id="a573a-3580">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3580">3</span></span>

<span data-ttu-id="a573a-3581">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3581">4</span></span>

<span data-ttu-id="a573a-3582">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3582">5</span></span>

<span data-ttu-id="a573a-3583">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3583">6</span></span>

<span data-ttu-id="a573a-3584">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3584">7</span></span>

<span data-ttu-id="a573a-3585">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3585">8</span></span>

<span data-ttu-id="a573a-3586">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3586">9</span></span>

<span data-ttu-id="a573a-3587">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3587">2</span></span><br/> <span data-ttu-id="a573a-3588">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3588">0</span></span><br/>

<span data-ttu-id="a573a-3589">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3589">1</span></span>

<span data-ttu-id="a573a-3590">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3590">2</span></span>

<span data-ttu-id="a573a-3591">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3591">3</span></span>

<span data-ttu-id="a573a-3592">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3592">4</span></span>

<span data-ttu-id="a573a-3593">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3593">5</span></span>

<span data-ttu-id="a573a-3594">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3594">6</span></span>

<span data-ttu-id="a573a-3595">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3595">7</span></span>

<span data-ttu-id="a573a-3596">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3596">8</span></span>

<span data-ttu-id="a573a-3597">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3597">9</span></span>

<span data-ttu-id="a573a-3598">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3598">3</span></span><br/> <span data-ttu-id="a573a-3599">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3599">0</span></span><br/>

<span data-ttu-id="a573a-3600">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3600">1</span></span>

<span data-ttu-id="a573a-3601">\_хкурсор</span><span class="sxs-lookup"><span data-stu-id="a573a-3601">\_hCursor</span></span>

<span data-ttu-id="a573a-3602">\_кровстотрансфер</span><span class="sxs-lookup"><span data-stu-id="a573a-3602">\_cRowsToTransfer</span></span>

<span data-ttu-id="a573a-3603">\_кброввидс</span><span class="sxs-lookup"><span data-stu-id="a573a-3603">\_cbRowWidth</span></span>

<span data-ttu-id="a573a-3604">\_кбсик</span><span class="sxs-lookup"><span data-stu-id="a573a-3604">\_cbSeek</span></span>

<span data-ttu-id="a573a-3605">\_кбресервед</span><span class="sxs-lookup"><span data-stu-id="a573a-3605">\_cbReserved</span></span>

<span data-ttu-id="a573a-3606">\_кбреадбуффер</span><span class="sxs-lookup"><span data-stu-id="a573a-3606">\_cbReadBuffer</span></span>

<span data-ttu-id="a573a-3607">\_улклиентбасе</span><span class="sxs-lookup"><span data-stu-id="a573a-3607">\_ulClientBase</span></span>

<span data-ttu-id="a573a-3608">\_фбвдфетч</span><span class="sxs-lookup"><span data-stu-id="a573a-3608">\_fBwdFetch</span></span>

<span data-ttu-id="a573a-3609">eType</span><span class="sxs-lookup"><span data-stu-id="a573a-3609">eType</span></span>

<span data-ttu-id="a573a-3610">\_Протокол CHAP</span><span class="sxs-lookup"><span data-stu-id="a573a-3610">\_chapt</span></span>

<span data-ttu-id="a573a-3611">сикдескриптион</span><span class="sxs-lookup"><span data-stu-id="a573a-3611">SeekDescription</span></span>

<span data-ttu-id="a573a-3612">...</span><span class="sxs-lookup"><span data-stu-id="a573a-3612">...</span></span>

<span data-ttu-id="a573a-3613">... перемен</span><span class="sxs-lookup"><span data-stu-id="a573a-3613">... (variable)</span></span>



 

<span data-ttu-id="a573a-3614">**\_ хкурсор**: 32-разрядное значение, представляющее маркер из сообщения кпмкреатекуерйоут, идентифицирующего запрос, для которого необходимо получить строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-3614">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="a573a-3615">**\_ кровстотрансфер**: 32-разрядное целое число без знака, указывающее максимальное число строк, которое клиент хочет получить в ответ на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="a573a-3615">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="a573a-3616">**\_ кброввидс**: 32-разрядное целое число без знака, указывающее длину строки в байтах.</span><span class="sxs-lookup"><span data-stu-id="a573a-3616">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="a573a-3617">**\_ кбсик**: 32-битовое целое число без знака, указывающее размер сообщения, начинающегося с eType.</span><span class="sxs-lookup"><span data-stu-id="a573a-3617">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="a573a-3618">**\_ кбресервед**: 32-разрядное целое число без знака, указывающее размер (в байтах) сообщения кпмжетровсаут (без полей Rows и сикдескриптионс).</span><span class="sxs-lookup"><span data-stu-id="a573a-3618">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="a573a-3619">Это значение в этом поле добавляется к значению \_ поля кбсик, а затем используется для вычисления поля смещение строк в сообщении кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-3619">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="a573a-3620">**\_ кбреадбуффер**: 32-разрядное целое число без знака, которое должно быть равно максимальному значению параметра \_ кброввидс или 1000, равному значению \_ кровстотрансфер, округленному до ближайшего 512 байта.</span><span class="sxs-lookup"><span data-stu-id="a573a-3620">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="a573a-3621">Значение не должно превышать 0x00004000.</span><span class="sxs-lookup"><span data-stu-id="a573a-3621">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="a573a-3622">**\_ улклиентбасе**: 32-разрядное целое число без знака, указывающее базовое значение, используемое для вычислений указателей в буфере строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3622">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="a573a-3623">Если используются 64-разрядные смещения, поле reserved2 в заголовке сообщения используется в качестве верхних 32-бит и \_ улклиентбасе в качестве младших 32 бит для 64-разрядного значения.</span><span class="sxs-lookup"><span data-stu-id="a573a-3623">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="a573a-3624">Дополнительные сведения см. в разделе 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="a573a-3624">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="a573a-3625">**\_ фбвдфетч**: 32-битовое целое число без знака, указывающее порядок получения строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3625">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="a573a-3626">Если задано значение 0x00000001, строки будут извлекаться в обратную последовательность.</span><span class="sxs-lookup"><span data-stu-id="a573a-3626">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="a573a-3627">Если задано значение 0x00000000, строки будут извлекаться в прямом порядке.</span><span class="sxs-lookup"><span data-stu-id="a573a-3627">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="a573a-3628">НЕ должно быть задано ни одного другого значения.</span><span class="sxs-lookup"><span data-stu-id="a573a-3628">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="a573a-3629">**eType**: 32-разрядное целое число без знака, содержащее одно из следующих значений для указания типа выполняемой операции.</span><span class="sxs-lookup"><span data-stu-id="a573a-3629">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="a573a-3630">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-3630">Value</span></span>                         | <span data-ttu-id="a573a-3631">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-3631">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="a573a-3632">Еровсикнекст 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-3632">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="a573a-3633">Сикдескриптион содержит структуру Кровсикнекст.</span><span class="sxs-lookup"><span data-stu-id="a573a-3633">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="a573a-3634">Еровсикат 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-3634">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="a573a-3635">Сикдескриптион содержит структуру Кровсикат.</span><span class="sxs-lookup"><span data-stu-id="a573a-3635">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="a573a-3636">Еровсикатратио 0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-3636">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="a573a-3637">Сикдескриптион содержит структуру Кровсикатратио.</span><span class="sxs-lookup"><span data-stu-id="a573a-3637">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="a573a-3638">Еровсикбибукмарк 0x00000004</span><span class="sxs-lookup"><span data-stu-id="a573a-3638">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="a573a-3639">Сикдескриптион содержит структуру Кровсикбибукмарк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3639">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="a573a-3640">**\_ chap**: 32-разрядное значение, представляющее маркер главы набора строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3640">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="a573a-3641">**Сикдескриптион**: это поле должно содержать структуру типа, обозначенного значением eType.</span><span class="sxs-lookup"><span data-stu-id="a573a-3641">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="a573a-3642">2.2.3.16 Кпмжетровсаут</span><span class="sxs-lookup"><span data-stu-id="a573a-3642">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="a573a-3643">Сообщение Кпмжетровсаут отвечает на сообщение Кпмжетровсин со строками запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3643">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="a573a-3644">Серверы должны отформатировать смещения до типов данных переменной длины в поле строк следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-3644">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="a573a-3645">Клиент указал, что он был 32-разрядной системой (0x00000008 или меньше в поле Иклиентверсион Кпмконнектин): смещениями являются 32-разрядные целые числа.</span><span class="sxs-lookup"><span data-stu-id="a573a-3645">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="a573a-3646">Клиент указал, что он был 64-разрядной системой ( \_ иклиентверсион > 0x00000008 в кпмконнектин) и сервер указал, что он был 32-разрядной системой ( \_ serverVersion установлен в 0X00000007 в кпмконнектаут): смещениями являются 32-разрядные целые числа</span><span class="sxs-lookup"><span data-stu-id="a573a-3646">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="a573a-3647">Клиент указал, что он был 64-разрядной системой ( \_ иклиентверсион > 0x00000008 в кпмконнектин) и сервер указал, что он был 64-разрядной системой ( \_ serverVersion установлен в 0X00010007 в кпмконнектаут): смещениями являются 64-разрядные целые числа</span><span class="sxs-lookup"><span data-stu-id="a573a-3647">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="a573a-3648">Формат сообщения Кпмжетровсаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3648">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="a573a-3649">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3649">0</span></span>

<span data-ttu-id="a573a-3650">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3650">1</span></span>

<span data-ttu-id="a573a-3651">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3651">2</span></span>

<span data-ttu-id="a573a-3652">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3652">3</span></span>

<span data-ttu-id="a573a-3653">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3653">4</span></span>

<span data-ttu-id="a573a-3654">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3654">5</span></span>

<span data-ttu-id="a573a-3655">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3655">6</span></span>

<span data-ttu-id="a573a-3656">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3656">7</span></span>

<span data-ttu-id="a573a-3657">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3657">8</span></span>

<span data-ttu-id="a573a-3658">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3658">9</span></span>

<span data-ttu-id="a573a-3659">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3659">1</span></span><br/> <span data-ttu-id="a573a-3660">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3660">0</span></span><br/>

<span data-ttu-id="a573a-3661">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3661">1</span></span>

<span data-ttu-id="a573a-3662">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3662">2</span></span>

<span data-ttu-id="a573a-3663">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3663">3</span></span>

<span data-ttu-id="a573a-3664">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3664">4</span></span>

<span data-ttu-id="a573a-3665">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3665">5</span></span>

<span data-ttu-id="a573a-3666">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3666">6</span></span>

<span data-ttu-id="a573a-3667">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3667">7</span></span>

<span data-ttu-id="a573a-3668">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3668">8</span></span>

<span data-ttu-id="a573a-3669">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3669">9</span></span>

<span data-ttu-id="a573a-3670">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3670">2</span></span><br/> <span data-ttu-id="a573a-3671">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3671">0</span></span><br/>

<span data-ttu-id="a573a-3672">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3672">1</span></span>

<span data-ttu-id="a573a-3673">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3673">2</span></span>

<span data-ttu-id="a573a-3674">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3674">3</span></span>

<span data-ttu-id="a573a-3675">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3675">4</span></span>

<span data-ttu-id="a573a-3676">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3676">5</span></span>

<span data-ttu-id="a573a-3677">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3677">6</span></span>

<span data-ttu-id="a573a-3678">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3678">7</span></span>

<span data-ttu-id="a573a-3679">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3679">8</span></span>

<span data-ttu-id="a573a-3680">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3680">9</span></span>

<span data-ttu-id="a573a-3681">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3681">3</span></span><br/> <span data-ttu-id="a573a-3682">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3682">0</span></span><br/>

<span data-ttu-id="a573a-3683">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3683">1</span></span>

<span data-ttu-id="a573a-3684">\_кровсретурнед</span><span class="sxs-lookup"><span data-stu-id="a573a-3684">\_cRowsReturned</span></span>

<span data-ttu-id="a573a-3685">eType</span><span class="sxs-lookup"><span data-stu-id="a573a-3685">eType</span></span>

<span data-ttu-id="a573a-3686">\_Протокол CHAP</span><span class="sxs-lookup"><span data-stu-id="a573a-3686">\_chapt</span></span>

<span data-ttu-id="a573a-3687">Сикдескриптион (необязательный, переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-3687">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="a573a-3688">...</span><span class="sxs-lookup"><span data-stu-id="a573a-3688">...</span></span>

<span data-ttu-id="a573a-3689">...</span><span class="sxs-lookup"><span data-stu-id="a573a-3689">...</span></span>

<span data-ttu-id="a573a-3690">Паддингровс (необязательный, переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-3690">paddingRows (optional, variable)</span></span>

<span data-ttu-id="a573a-3691">Строки</span><span class="sxs-lookup"><span data-stu-id="a573a-3691">Rows</span></span>



 

<span data-ttu-id="a573a-3692">**\_ кровсретурнед**: 32-разрядное целое число без знака, указывающее количество строк, возвращаемых в строках.</span><span class="sxs-lookup"><span data-stu-id="a573a-3692">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="a573a-3693">**eType**: 32-разрядное целое число без знака, содержащее одно из следующих значений, указывающее тип выполняемой операции ровсик.</span><span class="sxs-lookup"><span data-stu-id="a573a-3693">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="a573a-3694">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-3694">Value</span></span>                         | <span data-ttu-id="a573a-3695">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-3695">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="a573a-3696">Еровссикноне 0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-3696">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="a573a-3697">Нет Сикдескриптион, игнорировать поле Сикдескриптион.</span><span class="sxs-lookup"><span data-stu-id="a573a-3697">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="a573a-3698">Еровсикнекст 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-3698">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="a573a-3699">Сикдескриптион содержит структуру Кровсикнекст.</span><span class="sxs-lookup"><span data-stu-id="a573a-3699">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="a573a-3700">Еровсикат 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-3700">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="a573a-3701">Сикдескриптион содержит структуру Кровсикат.</span><span class="sxs-lookup"><span data-stu-id="a573a-3701">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="a573a-3702">Еровсикатратио 0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-3702">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="a573a-3703">Сикдескриптион содержит структуру Кровсикатратио.</span><span class="sxs-lookup"><span data-stu-id="a573a-3703">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="a573a-3704">Еровсикбибукмарк 0x00000004</span><span class="sxs-lookup"><span data-stu-id="a573a-3704">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="a573a-3705">Сикдескриптион содержит структуру Кровсикбибукмарк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3705">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="a573a-3706">**\_ chap**: 32-разрядное значение, представляющее маркер главы набора строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3706">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="a573a-3707">**Сикдескриптион**: это поле должно содержать структуру типа, обозначенного полем eType.</span><span class="sxs-lookup"><span data-stu-id="a573a-3707">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="a573a-3708">**паддингровс**: длина этого поля должна быть достаточной (от 0 до \_ кбресервед-1 байт) для заполнения поля ROWS \_ значением кбресервед offset с начала сообщения, где \_ кбресервед — это значение в сообщении кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-3708">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="a573a-3709">Байты заполнения, используемые в этом поле, могут быть любым произвольным значением.</span><span class="sxs-lookup"><span data-stu-id="a573a-3709">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="a573a-3710">Это поле должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-3710">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="a573a-3711">**Строки**: данные строк форматируются в соответствии со сведениями о столбцах в последнем сообщении кпмсетбиндингсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-3711">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="a573a-3712">Строки должны храниться в прямом порядке (например, строка 1 перед строкой 2).</span><span class="sxs-lookup"><span data-stu-id="a573a-3712">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="a573a-3713">Столбцы фиксированного размера должны храниться в смещениях, указанных последним сообщением Кпмсетбиндингсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-3713">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="a573a-3714">Столбцы переменного размера (например, строки) должны храниться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-3714">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="a573a-3715">Сами данные переменной (например, строка) хранятся ближе к концу буфера в порядке убывания (например, коллекция всех переменных данных для строки 1 находится в конце, строка 2 — в ближайшее и т. д.).</span><span class="sxs-lookup"><span data-stu-id="a573a-3715">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="a573a-3716">Область фиксированного размера (в начале буфера строк) должна содержать Кроввариант для каждого столбца, хранящийся в смещении, указанном в самом последнем сообщении Кпмсетбиндингсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-3716">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="a573a-3717">Втипе должен содержать тип данных (например, VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="a573a-3717">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="a573a-3718">Если, как определено правилами в начале раздела в этом разделе, используется 32-разрядное смещение, а поле offset в Кроввариант должно содержать 32-разрядное значение, которое является смещением данных переменной от начала сообщения Кпмжетровсаут, плюс значение \_ улклиентбасе, указанное в последнем кпмжетровсин сообщении.</span><span class="sxs-lookup"><span data-stu-id="a573a-3718">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="a573a-3719">Если используются 64-разрядные смещения, поле offset в Кроввариант должно содержать 64-разрядное значение, которое является смещением от начала сообщения Кпмжетровсаут, добавленного к 64-разрядному значению, созданному с помощью \_ улклиентбасе, в качестве младших 32-бит и \_ ulReserved2 в качестве 32 высоких-бит.</span><span class="sxs-lookup"><span data-stu-id="a573a-3719">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="a573a-3720">Например, если в сообщении Кпмсетбиндингсин указано два столбца — size (VT \_ i4) и Title (VT \_ LPWSTR), а \_ улклиентбасе from кпмжетровсин — 0x10000, то две строки будут выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a573a-3720">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="a573a-3721">Раздел, помеченный серым цветом, является частью буфера фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="a573a-3721">The section marked in grey is the fixed-length part of the buffer.</span></span>

![Пример сообщения кпмсетбиндингсин](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="a573a-3723">2.2.3.17 Кпмратиофинишедин</span><span class="sxs-lookup"><span data-stu-id="a573a-3723">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="a573a-3724">Сообщение Кпмратиофинишедин запрашивает процент завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3724">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="a573a-3725">Формат сообщения Кпмратиофинишедин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3725">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-3726">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3726">0</span></span>

<span data-ttu-id="a573a-3727">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3727">1</span></span>

<span data-ttu-id="a573a-3728">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3728">2</span></span>

<span data-ttu-id="a573a-3729">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3729">3</span></span>

<span data-ttu-id="a573a-3730">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3730">4</span></span>

<span data-ttu-id="a573a-3731">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3731">5</span></span>

<span data-ttu-id="a573a-3732">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3732">6</span></span>

<span data-ttu-id="a573a-3733">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3733">7</span></span>

<span data-ttu-id="a573a-3734">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3734">8</span></span>

<span data-ttu-id="a573a-3735">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3735">9</span></span>

<span data-ttu-id="a573a-3736">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3736">1</span></span><br/> <span data-ttu-id="a573a-3737">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3737">0</span></span><br/>

<span data-ttu-id="a573a-3738">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3738">1</span></span>

<span data-ttu-id="a573a-3739">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3739">2</span></span>

<span data-ttu-id="a573a-3740">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3740">3</span></span>

<span data-ttu-id="a573a-3741">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3741">4</span></span>

<span data-ttu-id="a573a-3742">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3742">5</span></span>

<span data-ttu-id="a573a-3743">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3743">6</span></span>

<span data-ttu-id="a573a-3744">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3744">7</span></span>

<span data-ttu-id="a573a-3745">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3745">8</span></span>

<span data-ttu-id="a573a-3746">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3746">9</span></span>

<span data-ttu-id="a573a-3747">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3747">2</span></span><br/> <span data-ttu-id="a573a-3748">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3748">0</span></span><br/>

<span data-ttu-id="a573a-3749">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3749">1</span></span>

<span data-ttu-id="a573a-3750">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3750">2</span></span>

<span data-ttu-id="a573a-3751">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3751">3</span></span>

<span data-ttu-id="a573a-3752">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3752">4</span></span>

<span data-ttu-id="a573a-3753">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3753">5</span></span>

<span data-ttu-id="a573a-3754">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3754">6</span></span>

<span data-ttu-id="a573a-3755">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3755">7</span></span>

<span data-ttu-id="a573a-3756">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3756">8</span></span>

<span data-ttu-id="a573a-3757">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3757">9</span></span>

<span data-ttu-id="a573a-3758">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3758">3</span></span><br/> <span data-ttu-id="a573a-3759">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3759">0</span></span><br/>

<span data-ttu-id="a573a-3760">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3760">1</span></span>

<span data-ttu-id="a573a-3761">\_хкурсор</span><span class="sxs-lookup"><span data-stu-id="a573a-3761">\_hCursor</span></span>

<span data-ttu-id="a573a-3762">\_фкуикк</span><span class="sxs-lookup"><span data-stu-id="a573a-3762">\_fQuick</span></span>



 

<span data-ttu-id="a573a-3763">**\_ хкурсор**: маркер из сообщения кпмкреатекуерйоут, идентифицирующего запрос, для которого запрашиваются сведения о завершении.</span><span class="sxs-lookup"><span data-stu-id="a573a-3763">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="a573a-3764">**\_ фкуикк**: необходимо задать значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="a573a-3764">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="a573a-3765">Не используется и должен игнорироваться сервером.</span><span class="sxs-lookup"><span data-stu-id="a573a-3765">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="a573a-3766">2.2.3.18 Кпмратиофинишедаут</span><span class="sxs-lookup"><span data-stu-id="a573a-3766">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="a573a-3767">Сообщение Кпмратиофинишедаут отвечает на сообщение Кпмратиофинишедин с коэффициентом завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3767">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="a573a-3768">Формат сообщения Кпмратиофинишедаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3768">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="a573a-3769">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3769">0</span></span>

<span data-ttu-id="a573a-3770">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3770">1</span></span>

<span data-ttu-id="a573a-3771">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3771">2</span></span>

<span data-ttu-id="a573a-3772">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3772">3</span></span>

<span data-ttu-id="a573a-3773">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3773">4</span></span>

<span data-ttu-id="a573a-3774">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3774">5</span></span>

<span data-ttu-id="a573a-3775">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3775">6</span></span>

<span data-ttu-id="a573a-3776">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3776">7</span></span>

<span data-ttu-id="a573a-3777">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3777">8</span></span>

<span data-ttu-id="a573a-3778">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3778">9</span></span>

<span data-ttu-id="a573a-3779">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3779">1</span></span><br/> <span data-ttu-id="a573a-3780">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3780">0</span></span><br/>

<span data-ttu-id="a573a-3781">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3781">1</span></span>

<span data-ttu-id="a573a-3782">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3782">2</span></span>

<span data-ttu-id="a573a-3783">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3783">3</span></span>

<span data-ttu-id="a573a-3784">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3784">4</span></span>

<span data-ttu-id="a573a-3785">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3785">5</span></span>

<span data-ttu-id="a573a-3786">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3786">6</span></span>

<span data-ttu-id="a573a-3787">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3787">7</span></span>

<span data-ttu-id="a573a-3788">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3788">8</span></span>

<span data-ttu-id="a573a-3789">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3789">9</span></span>

<span data-ttu-id="a573a-3790">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3790">2</span></span><br/> <span data-ttu-id="a573a-3791">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3791">0</span></span><br/>

<span data-ttu-id="a573a-3792">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3792">1</span></span>

<span data-ttu-id="a573a-3793">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3793">2</span></span>

<span data-ttu-id="a573a-3794">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3794">3</span></span>

<span data-ttu-id="a573a-3795">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3795">4</span></span>

<span data-ttu-id="a573a-3796">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3796">5</span></span>

<span data-ttu-id="a573a-3797">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3797">6</span></span>

<span data-ttu-id="a573a-3798">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3798">7</span></span>

<span data-ttu-id="a573a-3799">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3799">8</span></span>

<span data-ttu-id="a573a-3800">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3800">9</span></span>

<span data-ttu-id="a573a-3801">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3801">3</span></span><br/> <span data-ttu-id="a573a-3802">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3802">0</span></span><br/>

<span data-ttu-id="a573a-3803">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3803">1</span></span>

<span data-ttu-id="a573a-3804">\_ улнумератор</span><span class="sxs-lookup"><span data-stu-id="a573a-3804">\_ ulNumerator</span></span>

<span data-ttu-id="a573a-3805">\_улденоминатор</span><span class="sxs-lookup"><span data-stu-id="a573a-3805">\_ulDenominator</span></span>

<span data-ttu-id="a573a-3806">\_cRows</span><span class="sxs-lookup"><span data-stu-id="a573a-3806">\_cRows</span></span>

<span data-ttu-id="a573a-3807">\_фневровс</span><span class="sxs-lookup"><span data-stu-id="a573a-3807">\_fNewRows</span></span>



 

<span data-ttu-id="a573a-3808">**\_ улнумератор**: 32-битовое целое число без знака, указывающее числитель коэффициента завершения в терминах строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3808">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="a573a-3809">**\_ улденоминатор**: 32-битовое целое число без знака, указывающее знаменатель коэффициента завершения в терминах строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3809">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="a573a-3810">ДОЛЖНО быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="a573a-3810">MUST be greater than zero.</span></span>

<span data-ttu-id="a573a-3811">**\_ crowset**: 32-разрядное целое число без знака, указывающее общее количество строк для запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3811">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="a573a-3812">**\_ фневровс**: логическое значение, указывающее, доступны ли новые строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-3812">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="a573a-3813">Значение 0x00000001 указывает, что новые строки доступны в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3813">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="a573a-3814">Значение 0x00000000 указывает, что набор строк не содержит новых строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3814">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="a573a-3815">Для этого поля не должны быть заданы другие значения.</span><span class="sxs-lookup"><span data-stu-id="a573a-3815">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="a573a-3816">2.2.3.19 Кпмфетчвалуеин</span><span class="sxs-lookup"><span data-stu-id="a573a-3816">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="a573a-3817">Сообщение Кпмфетчвалуеин запрашивает значение свойства, которое слишком велико для возвращения в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3817">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="a573a-3818">Как указано в разделе 3.2.4.2.5, это сообщение отправляется повторно для получения всех байтов свойства, обновляя \_ кбсофар для каждого, пока \_ поле Фмориксистс сообщения кпмфетчвалуеаут не будет установлено в **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a573a-3818">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="a573a-3819">Формат сообщения Кпмфетчвалуеин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3819">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-3820">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3820">0</span></span>

<span data-ttu-id="a573a-3821">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3821">1</span></span>

<span data-ttu-id="a573a-3822">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3822">2</span></span>

<span data-ttu-id="a573a-3823">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3823">3</span></span>

<span data-ttu-id="a573a-3824">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3824">4</span></span>

<span data-ttu-id="a573a-3825">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3825">5</span></span>

<span data-ttu-id="a573a-3826">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3826">6</span></span>

<span data-ttu-id="a573a-3827">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3827">7</span></span>

<span data-ttu-id="a573a-3828">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3828">8</span></span>

<span data-ttu-id="a573a-3829">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3829">9</span></span>

<span data-ttu-id="a573a-3830">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3830">1</span></span><br/> <span data-ttu-id="a573a-3831">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3831">0</span></span><br/>

<span data-ttu-id="a573a-3832">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3832">1</span></span>

<span data-ttu-id="a573a-3833">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3833">2</span></span>

<span data-ttu-id="a573a-3834">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3834">3</span></span>

<span data-ttu-id="a573a-3835">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3835">4</span></span>

<span data-ttu-id="a573a-3836">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3836">5</span></span>

<span data-ttu-id="a573a-3837">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3837">6</span></span>

<span data-ttu-id="a573a-3838">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3838">7</span></span>

<span data-ttu-id="a573a-3839">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3839">8</span></span>

<span data-ttu-id="a573a-3840">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3840">9</span></span>

<span data-ttu-id="a573a-3841">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3841">2</span></span><br/> <span data-ttu-id="a573a-3842">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3842">0</span></span><br/>

<span data-ttu-id="a573a-3843">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3843">1</span></span>

<span data-ttu-id="a573a-3844">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3844">2</span></span>

<span data-ttu-id="a573a-3845">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3845">3</span></span>

<span data-ttu-id="a573a-3846">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3846">4</span></span>

<span data-ttu-id="a573a-3847">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3847">5</span></span>

<span data-ttu-id="a573a-3848">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3848">6</span></span>

<span data-ttu-id="a573a-3849">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3849">7</span></span>

<span data-ttu-id="a573a-3850">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3850">8</span></span>

<span data-ttu-id="a573a-3851">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3851">9</span></span>

<span data-ttu-id="a573a-3852">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3852">3</span></span><br/> <span data-ttu-id="a573a-3853">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3853">0</span></span><br/>

<span data-ttu-id="a573a-3854">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3854">1</span></span>

<span data-ttu-id="a573a-3855">\_WID</span><span class="sxs-lookup"><span data-stu-id="a573a-3855">\_wid</span></span>

<span data-ttu-id="a573a-3856">\_кбсофар</span><span class="sxs-lookup"><span data-stu-id="a573a-3856">\_cbSoFar</span></span>

<span data-ttu-id="a573a-3857">\_кбпропспек</span><span class="sxs-lookup"><span data-stu-id="a573a-3857">\_cbPropSpec</span></span>

<span data-ttu-id="a573a-3858">\_кбчунк</span><span class="sxs-lookup"><span data-stu-id="a573a-3858">\_cbChunk</span></span>

<span data-ttu-id="a573a-3859">Пропспек (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-3859">PropSpec (variable)</span></span>

<span data-ttu-id="a573a-3860">...</span><span class="sxs-lookup"><span data-stu-id="a573a-3860">...</span></span>

<span data-ttu-id="a573a-3861">\_Заполнение (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-3861">\_padding (variable)</span></span>



 

<span data-ttu-id="a573a-3862">**\_ wid**: 32-разрядное целое число без знака, содержащее сведения об идентификаторе документа, определяющего документ, для которого должно быть выбрано свойство.</span><span class="sxs-lookup"><span data-stu-id="a573a-3862">**\_wid**: A 32-bit unsigned integer containing information about the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="a573a-3863">**\_ кбсофар**: 32-разрядное целое число без знака, содержащее число байтов, ранее переданных для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-3863">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="a573a-3864">В первом сообщении должно быть задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-3864">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="a573a-3865">**\_ кбпропспек**: 32-разрядное целое число без знака, содержащее размер поля пропспек в байтах.</span><span class="sxs-lookup"><span data-stu-id="a573a-3865">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="a573a-3866">**\_ кбчунк**: 32-разрядное целое число без знака, содержащее максимальное число байтов, которое отправитель может принимать в сообщении кпмфетчвалуеаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-3866">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="a573a-3867">*Поведение Windows: для этого поля задано значение 0x00004000 для всех версий Windows.*</span><span class="sxs-lookup"><span data-stu-id="a573a-3867">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="a573a-3868">**Пропспек**: структура кфуллпропспек, указывающая извлекаемое свойство.</span><span class="sxs-lookup"><span data-stu-id="a573a-3868">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="a573a-3869">**\_ Заполнение**: это поле должно иметь длину, необходимую (от 0 до 3 байт), для размещения сообщения до нескольких 4 байт.</span><span class="sxs-lookup"><span data-stu-id="a573a-3869">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="a573a-3870">Значение заполнения байтов может быть любым произвольным значением.</span><span class="sxs-lookup"><span data-stu-id="a573a-3870">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="a573a-3871">Это поле должно игнорироваться получателем.</span><span class="sxs-lookup"><span data-stu-id="a573a-3871">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="a573a-3872">2.2.3.20 Кпмфетчвалуеаут</span><span class="sxs-lookup"><span data-stu-id="a573a-3872">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="a573a-3873">Сообщение Кпмфетчвалуеаут отвечает на сообщение Кпмфетчвалуеин со значением свойства из предыдущего запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3873">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="a573a-3874">Как указано в разделе 3.1.5.2.8, это сообщение отправляется после каждого сообщения Кпмфетчвалуеин до тех пор, пока не будут переданы все байты свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-3874">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="a573a-3875">Формат сообщения Кпмфетчвалуеаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3875">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="a573a-3876">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3876">0</span></span>

<span data-ttu-id="a573a-3877">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3877">1</span></span>

<span data-ttu-id="a573a-3878">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3878">2</span></span>

<span data-ttu-id="a573a-3879">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3879">3</span></span>

<span data-ttu-id="a573a-3880">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3880">4</span></span>

<span data-ttu-id="a573a-3881">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3881">5</span></span>

<span data-ttu-id="a573a-3882">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3882">6</span></span>

<span data-ttu-id="a573a-3883">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3883">7</span></span>

<span data-ttu-id="a573a-3884">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3884">8</span></span>

<span data-ttu-id="a573a-3885">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3885">9</span></span>

<span data-ttu-id="a573a-3886">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3886">1</span></span><br/> <span data-ttu-id="a573a-3887">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3887">0</span></span><br/>

<span data-ttu-id="a573a-3888">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3888">1</span></span>

<span data-ttu-id="a573a-3889">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3889">2</span></span>

<span data-ttu-id="a573a-3890">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3890">3</span></span>

<span data-ttu-id="a573a-3891">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3891">4</span></span>

<span data-ttu-id="a573a-3892">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3892">5</span></span>

<span data-ttu-id="a573a-3893">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3893">6</span></span>

<span data-ttu-id="a573a-3894">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3894">7</span></span>

<span data-ttu-id="a573a-3895">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3895">8</span></span>

<span data-ttu-id="a573a-3896">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3896">9</span></span>

<span data-ttu-id="a573a-3897">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3897">2</span></span><br/> <span data-ttu-id="a573a-3898">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3898">0</span></span><br/>

<span data-ttu-id="a573a-3899">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3899">1</span></span>

<span data-ttu-id="a573a-3900">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3900">2</span></span>

<span data-ttu-id="a573a-3901">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3901">3</span></span>

<span data-ttu-id="a573a-3902">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3902">4</span></span>

<span data-ttu-id="a573a-3903">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3903">5</span></span>

<span data-ttu-id="a573a-3904">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3904">6</span></span>

<span data-ttu-id="a573a-3905">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3905">7</span></span>

<span data-ttu-id="a573a-3906">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3906">8</span></span>

<span data-ttu-id="a573a-3907">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3907">9</span></span>

<span data-ttu-id="a573a-3908">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3908">3</span></span><br/> <span data-ttu-id="a573a-3909">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3909">0</span></span><br/>

<span data-ttu-id="a573a-3910">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3910">1</span></span>

<span data-ttu-id="a573a-3911">\_кбвалуе</span><span class="sxs-lookup"><span data-stu-id="a573a-3911">\_cbValue</span></span>

<span data-ttu-id="a573a-3912">\_фмориксистс</span><span class="sxs-lookup"><span data-stu-id="a573a-3912">\_fMoreExists</span></span>

<span data-ttu-id="a573a-3913">\_фвалуиксистс</span><span class="sxs-lookup"><span data-stu-id="a573a-3913">\_fValueExists</span></span>

<span data-ttu-id="a573a-3914">втипе</span><span class="sxs-lookup"><span data-stu-id="a573a-3914">vType</span></span>

<span data-ttu-id="a573a-3915">Управляемое vValue (переменная)</span><span class="sxs-lookup"><span data-stu-id="a573a-3915">vValue (variable)</span></span>



 

<span data-ttu-id="a573a-3916">**\_ кбвалуе**: 32-разрядное целое число без знака, содержащее общий размер в байтах в управляемое vValue.</span><span class="sxs-lookup"><span data-stu-id="a573a-3916">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="a573a-3917">**\_ фмориксистс**: логическое значение, указывающее, доступны ли дополнительные сообщения кпмфетчвалуеаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-3917">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="a573a-3918">Если задано значение 0x00000001, то существуют дополнительные сообщения Кпмфетчвалуеаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-3918">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="a573a-3919">Если задано значение 0x00000000, дополнительные сообщения Кпмфетчвалуеаут недоступны.</span><span class="sxs-lookup"><span data-stu-id="a573a-3919">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="a573a-3920">**\_ фвалуиксистс**: логическое значение, указывающее, имеется ли значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-3920">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="a573a-3921">Если задано значение 0x00000001, то свойство существует.</span><span class="sxs-lookup"><span data-stu-id="a573a-3921">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="a573a-3922">Если задано 0x00000000, значение свойства не существует.</span><span class="sxs-lookup"><span data-stu-id="a573a-3922">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="a573a-3923">**втипе**. значение из перечисления VARENUM. Дополнительные сведения см. в разделе 2.2.1.1, описывающем тип свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-3923">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="a573a-3924">**управляемое vValue**: часть массива байтов, содержащая структуру сериализедпропертивалуе, как указано в разделе 2.2.1.32, где смещение начала части является значением \_ кбсофар в кпмфетчвалуеин.</span><span class="sxs-lookup"><span data-stu-id="a573a-3924">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="a573a-3925">Длина части, обозначенной \_ полем кбвалуе, должна быть равна значению \_ Кбчунк в кпмфетчвалуеин, если \_ фмориксистс имеет значение 0X00000001, и должно быть меньше или равно значению \_ кбчунк в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a573a-3925">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="a573a-3926">2.2.3.21 Кпмжетнотифи</span><span class="sxs-lookup"><span data-stu-id="a573a-3926">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="a573a-3927">Сообщение Кпмжетнотифи запрашивает, что клиент хочет получать уведомления об изменениях набора строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-3927">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="a573a-3928">Сообщение не должно включать текст. будет отправлен только заголовок сообщения, как указано в разделе 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="a573a-3928">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="a573a-3929">2.2.3.22 Кпмсенднотифйоут</span><span class="sxs-lookup"><span data-stu-id="a573a-3929">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="a573a-3930">Сообщение Кпмсенднотифйоут уведомляет клиента об изменении результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3930">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="a573a-3931">Это сообщение отправляется, только когда происходит изменение.</span><span class="sxs-lookup"><span data-stu-id="a573a-3931">This message is only sent when a change occurs.</span></span> <span data-ttu-id="a573a-3932">Формат сообщения Кпмсенднотифйоут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3932">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="a573a-3933">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3933">0</span></span>

<span data-ttu-id="a573a-3934">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3934">1</span></span>

<span data-ttu-id="a573a-3935">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3935">2</span></span>

<span data-ttu-id="a573a-3936">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3936">3</span></span>

<span data-ttu-id="a573a-3937">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3937">4</span></span>

<span data-ttu-id="a573a-3938">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3938">5</span></span>

<span data-ttu-id="a573a-3939">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3939">6</span></span>

<span data-ttu-id="a573a-3940">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3940">7</span></span>

<span data-ttu-id="a573a-3941">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3941">8</span></span>

<span data-ttu-id="a573a-3942">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3942">9</span></span>

<span data-ttu-id="a573a-3943">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3943">1</span></span><br/> <span data-ttu-id="a573a-3944">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3944">0</span></span><br/>

<span data-ttu-id="a573a-3945">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3945">1</span></span>

<span data-ttu-id="a573a-3946">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3946">2</span></span>

<span data-ttu-id="a573a-3947">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3947">3</span></span>

<span data-ttu-id="a573a-3948">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3948">4</span></span>

<span data-ttu-id="a573a-3949">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3949">5</span></span>

<span data-ttu-id="a573a-3950">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3950">6</span></span>

<span data-ttu-id="a573a-3951">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3951">7</span></span>

<span data-ttu-id="a573a-3952">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3952">8</span></span>

<span data-ttu-id="a573a-3953">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3953">9</span></span>

<span data-ttu-id="a573a-3954">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3954">2</span></span><br/> <span data-ttu-id="a573a-3955">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3955">0</span></span><br/>

<span data-ttu-id="a573a-3956">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3956">1</span></span>

<span data-ttu-id="a573a-3957">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3957">2</span></span>

<span data-ttu-id="a573a-3958">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3958">3</span></span>

<span data-ttu-id="a573a-3959">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3959">4</span></span>

<span data-ttu-id="a573a-3960">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3960">5</span></span>

<span data-ttu-id="a573a-3961">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3961">6</span></span>

<span data-ttu-id="a573a-3962">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3962">7</span></span>

<span data-ttu-id="a573a-3963">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3963">8</span></span>

<span data-ttu-id="a573a-3964">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3964">9</span></span>

<span data-ttu-id="a573a-3965">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3965">3</span></span><br/> <span data-ttu-id="a573a-3966">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3966">0</span></span><br/>

<span data-ttu-id="a573a-3967">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3967">1</span></span>

<span data-ttu-id="a573a-3968">\_ватчнотифи</span><span class="sxs-lookup"><span data-stu-id="a573a-3968">\_watchNotify</span></span>



 

<span data-ttu-id="a573a-3969">**\_ ватчнотифи**: изменение запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3969">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="a573a-3970">Оно должно иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a573a-3970">It MUST be one of the following values:</span></span>



| <span data-ttu-id="a573a-3971">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-3971">Value</span></span>                                     | <span data-ttu-id="a573a-3972">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-3972">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="a573a-3973">ДБВАТЧНОТИФИ \_ ровсчанжед 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-3973">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="a573a-3974">Изменилось число строк в наборе строк запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-3974">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="a573a-3975">ДБВАТЧНОТИФИ \_ куеридоне 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-3975">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="a573a-3976">Запрос завершен.</span><span class="sxs-lookup"><span data-stu-id="a573a-3976">The query has completed.</span></span>                            |
| <span data-ttu-id="a573a-3977">ДБВАТЧНОТИФИ \_ куеририксекутед 0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-3977">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="a573a-3978">Запрос был повторно выполнен.</span><span class="sxs-lookup"><span data-stu-id="a573a-3978">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="a573a-3979">2.2.3.23 Кпмжетаппроксиматепоситионин</span><span class="sxs-lookup"><span data-stu-id="a573a-3979">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="a573a-3980">Сообщение Кпмжетаппроксиматепоситионин запрашивает приблизительное расположение закладки в главе.</span><span class="sxs-lookup"><span data-stu-id="a573a-3980">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="a573a-3981">Формат сообщения Кпмжетаппроксиматепоситионин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-3981">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-3982">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3982">0</span></span>

<span data-ttu-id="a573a-3983">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3983">1</span></span>

<span data-ttu-id="a573a-3984">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3984">2</span></span>

<span data-ttu-id="a573a-3985">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3985">3</span></span>

<span data-ttu-id="a573a-3986">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3986">4</span></span>

<span data-ttu-id="a573a-3987">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3987">5</span></span>

<span data-ttu-id="a573a-3988">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3988">6</span></span>

<span data-ttu-id="a573a-3989">7</span><span class="sxs-lookup"><span data-stu-id="a573a-3989">7</span></span>

<span data-ttu-id="a573a-3990">8</span><span class="sxs-lookup"><span data-stu-id="a573a-3990">8</span></span>

<span data-ttu-id="a573a-3991">9</span><span class="sxs-lookup"><span data-stu-id="a573a-3991">9</span></span>

<span data-ttu-id="a573a-3992">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3992">1</span></span><br/> <span data-ttu-id="a573a-3993">0</span><span class="sxs-lookup"><span data-stu-id="a573a-3993">0</span></span><br/>

<span data-ttu-id="a573a-3994">1</span><span class="sxs-lookup"><span data-stu-id="a573a-3994">1</span></span>

<span data-ttu-id="a573a-3995">2</span><span class="sxs-lookup"><span data-stu-id="a573a-3995">2</span></span>

<span data-ttu-id="a573a-3996">3</span><span class="sxs-lookup"><span data-stu-id="a573a-3996">3</span></span>

<span data-ttu-id="a573a-3997">4</span><span class="sxs-lookup"><span data-stu-id="a573a-3997">4</span></span>

<span data-ttu-id="a573a-3998">5</span><span class="sxs-lookup"><span data-stu-id="a573a-3998">5</span></span>

<span data-ttu-id="a573a-3999">6</span><span class="sxs-lookup"><span data-stu-id="a573a-3999">6</span></span>

<span data-ttu-id="a573a-4000">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4000">7</span></span>

<span data-ttu-id="a573a-4001">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4001">8</span></span>

<span data-ttu-id="a573a-4002">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4002">9</span></span>

<span data-ttu-id="a573a-4003">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4003">2</span></span><br/> <span data-ttu-id="a573a-4004">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4004">0</span></span><br/>

<span data-ttu-id="a573a-4005">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4005">1</span></span>

<span data-ttu-id="a573a-4006">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4006">2</span></span>

<span data-ttu-id="a573a-4007">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4007">3</span></span>

<span data-ttu-id="a573a-4008">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4008">4</span></span>

<span data-ttu-id="a573a-4009">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4009">5</span></span>

<span data-ttu-id="a573a-4010">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4010">6</span></span>

<span data-ttu-id="a573a-4011">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4011">7</span></span>

<span data-ttu-id="a573a-4012">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4012">8</span></span>

<span data-ttu-id="a573a-4013">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4013">9</span></span>

<span data-ttu-id="a573a-4014">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4014">3</span></span><br/> <span data-ttu-id="a573a-4015">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4015">0</span></span><br/>

<span data-ttu-id="a573a-4016">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4016">1</span></span>

<span data-ttu-id="a573a-4017">\_хкурсор</span><span class="sxs-lookup"><span data-stu-id="a573a-4017">\_hCursor</span></span>

<span data-ttu-id="a573a-4018">\_Протокол CHAP</span><span class="sxs-lookup"><span data-stu-id="a573a-4018">\_chapt</span></span>

<span data-ttu-id="a573a-4019">\_бмк</span><span class="sxs-lookup"><span data-stu-id="a573a-4019">\_bmk</span></span>



 

<span data-ttu-id="a573a-4020">**\_ хкурсор**: 32-разрядное значение, представляющее курсор запроса, полученный из кпмкреатекуерйоут для набора строк, содержащего закладку.</span><span class="sxs-lookup"><span data-stu-id="a573a-4020">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="a573a-4021">**\_ chap**: 32-разрядное значение, представляющее маркер раздела, содержащего закладку.</span><span class="sxs-lookup"><span data-stu-id="a573a-4021">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="a573a-4022">**\_ бмк**: 32-разрядное значение, представляющее маркер закладки, для которой необходимо получить приблизительную точку.</span><span class="sxs-lookup"><span data-stu-id="a573a-4022">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="a573a-4023">2.2.3.24 Кпмжетаппроксиматепоситионаут</span><span class="sxs-lookup"><span data-stu-id="a573a-4023">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="a573a-4024">Сообщение Кпмжетаппроксиматепоситионаут отвечает на сообщение Кпмжетаппроксиматепоситионин, описывающее примерное расположение закладки в главе.</span><span class="sxs-lookup"><span data-stu-id="a573a-4024">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="a573a-4025">Формат сообщения Кпмжетаппроксиматепоситионаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-4025">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="a573a-4026">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4026">0</span></span>

<span data-ttu-id="a573a-4027">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4027">1</span></span>

<span data-ttu-id="a573a-4028">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4028">2</span></span>

<span data-ttu-id="a573a-4029">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4029">3</span></span>

<span data-ttu-id="a573a-4030">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4030">4</span></span>

<span data-ttu-id="a573a-4031">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4031">5</span></span>

<span data-ttu-id="a573a-4032">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4032">6</span></span>

<span data-ttu-id="a573a-4033">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4033">7</span></span>

<span data-ttu-id="a573a-4034">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4034">8</span></span>

<span data-ttu-id="a573a-4035">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4035">9</span></span>

<span data-ttu-id="a573a-4036">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4036">1</span></span><br/> <span data-ttu-id="a573a-4037">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4037">0</span></span><br/>

<span data-ttu-id="a573a-4038">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4038">1</span></span>

<span data-ttu-id="a573a-4039">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4039">2</span></span>

<span data-ttu-id="a573a-4040">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4040">3</span></span>

<span data-ttu-id="a573a-4041">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4041">4</span></span>

<span data-ttu-id="a573a-4042">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4042">5</span></span>

<span data-ttu-id="a573a-4043">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4043">6</span></span>

<span data-ttu-id="a573a-4044">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4044">7</span></span>

<span data-ttu-id="a573a-4045">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4045">8</span></span>

<span data-ttu-id="a573a-4046">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4046">9</span></span>

<span data-ttu-id="a573a-4047">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4047">2</span></span><br/> <span data-ttu-id="a573a-4048">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4048">0</span></span><br/>

<span data-ttu-id="a573a-4049">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4049">1</span></span>

<span data-ttu-id="a573a-4050">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4050">2</span></span>

<span data-ttu-id="a573a-4051">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4051">3</span></span>

<span data-ttu-id="a573a-4052">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4052">4</span></span>

<span data-ttu-id="a573a-4053">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4053">5</span></span>

<span data-ttu-id="a573a-4054">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4054">6</span></span>

<span data-ttu-id="a573a-4055">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4055">7</span></span>

<span data-ttu-id="a573a-4056">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4056">8</span></span>

<span data-ttu-id="a573a-4057">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4057">9</span></span>

<span data-ttu-id="a573a-4058">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4058">3</span></span><br/> <span data-ttu-id="a573a-4059">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4059">0</span></span><br/>

<span data-ttu-id="a573a-4060">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4060">1</span></span>

<span data-ttu-id="a573a-4061">\_numerator</span><span class="sxs-lookup"><span data-stu-id="a573a-4061">\_numerator</span></span>

<span data-ttu-id="a573a-4062">\_denominator</span><span class="sxs-lookup"><span data-stu-id="a573a-4062">\_denominator</span></span>



 

<span data-ttu-id="a573a-4063">**\_ числитель**: 32-разрядное целое число без знака, содержащее номер строки закладки в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-4063">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="a573a-4064">Если строки отсутствуют, это поле должно иметь значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4064">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="a573a-4065">**\_ знаменатель**: 32-битовое целое число без знака, содержащее количество строк в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-4065">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="a573a-4066">2.2.3.25 Кпмкомпаребмкин</span><span class="sxs-lookup"><span data-stu-id="a573a-4066">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="a573a-4067">Сообщение Кпмкомпаребмкин запрашивает сравнение двух закладок в главе.</span><span class="sxs-lookup"><span data-stu-id="a573a-4067">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="a573a-4068">Формат сообщения Кпмкомпаребмкин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-4068">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-4069">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4069">0</span></span>

<span data-ttu-id="a573a-4070">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4070">1</span></span>

<span data-ttu-id="a573a-4071">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4071">2</span></span>

<span data-ttu-id="a573a-4072">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4072">3</span></span>

<span data-ttu-id="a573a-4073">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4073">4</span></span>

<span data-ttu-id="a573a-4074">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4074">5</span></span>

<span data-ttu-id="a573a-4075">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4075">6</span></span>

<span data-ttu-id="a573a-4076">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4076">7</span></span>

<span data-ttu-id="a573a-4077">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4077">8</span></span>

<span data-ttu-id="a573a-4078">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4078">9</span></span>

<span data-ttu-id="a573a-4079">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4079">1</span></span><br/> <span data-ttu-id="a573a-4080">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4080">0</span></span><br/>

<span data-ttu-id="a573a-4081">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4081">1</span></span>

<span data-ttu-id="a573a-4082">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4082">2</span></span>

<span data-ttu-id="a573a-4083">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4083">3</span></span>

<span data-ttu-id="a573a-4084">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4084">4</span></span>

<span data-ttu-id="a573a-4085">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4085">5</span></span>

<span data-ttu-id="a573a-4086">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4086">6</span></span>

<span data-ttu-id="a573a-4087">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4087">7</span></span>

<span data-ttu-id="a573a-4088">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4088">8</span></span>

<span data-ttu-id="a573a-4089">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4089">9</span></span>

<span data-ttu-id="a573a-4090">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4090">2</span></span><br/> <span data-ttu-id="a573a-4091">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4091">0</span></span><br/>

<span data-ttu-id="a573a-4092">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4092">1</span></span>

<span data-ttu-id="a573a-4093">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4093">2</span></span>

<span data-ttu-id="a573a-4094">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4094">3</span></span>

<span data-ttu-id="a573a-4095">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4095">4</span></span>

<span data-ttu-id="a573a-4096">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4096">5</span></span>

<span data-ttu-id="a573a-4097">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4097">6</span></span>

<span data-ttu-id="a573a-4098">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4098">7</span></span>

<span data-ttu-id="a573a-4099">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4099">8</span></span>

<span data-ttu-id="a573a-4100">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4100">9</span></span>

<span data-ttu-id="a573a-4101">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4101">3</span></span><br/> <span data-ttu-id="a573a-4102">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4102">0</span></span><br/>

<span data-ttu-id="a573a-4103">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4103">1</span></span>

<span data-ttu-id="a573a-4104">\_хкурсор</span><span class="sxs-lookup"><span data-stu-id="a573a-4104">\_hCursor</span></span>

<span data-ttu-id="a573a-4105">\_Протокол CHAP</span><span class="sxs-lookup"><span data-stu-id="a573a-4105">\_chapt</span></span>

<span data-ttu-id="a573a-4106">\_бмкфирст</span><span class="sxs-lookup"><span data-stu-id="a573a-4106">\_bmkFirst</span></span>

<span data-ttu-id="a573a-4107">\_бмксеконд</span><span class="sxs-lookup"><span data-stu-id="a573a-4107">\_bmkSecond</span></span>



 

<span data-ttu-id="a573a-4108">\_**хкурсор**: 32-разрядное значение, представляющее собой маркер из сообщения кпмкреатекуерйоут для набора строк, содержащего закладки.</span><span class="sxs-lookup"><span data-stu-id="a573a-4108">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="a573a-4109">\_**CHAP**: 32-разрядное значение, представляющее маркер главы, содержащей закладки для сравнения.</span><span class="sxs-lookup"><span data-stu-id="a573a-4109">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="a573a-4110">\_**бмкфирст**: 32-разрядное значение, представляющее маркер первой закладки для сравнения.</span><span class="sxs-lookup"><span data-stu-id="a573a-4110">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="a573a-4111">\_**бмксеконд**: 32-разрядное значение, представляющее маркер для сравнения с второй закладкой.</span><span class="sxs-lookup"><span data-stu-id="a573a-4111">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="a573a-4112">2.2.3.26 Кпмкомпаребмкаут</span><span class="sxs-lookup"><span data-stu-id="a573a-4112">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="a573a-4113">Сообщение Кпмкомпаребмкаут отвечает на сообщение Кпмкомпаребмкин с использованием сравнения двух закладок в главе.</span><span class="sxs-lookup"><span data-stu-id="a573a-4113">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="a573a-4114">Формат сообщения Кпмкомпаребмкаут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-4114">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="a573a-4115">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4115">0</span></span>

<span data-ttu-id="a573a-4116">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4116">1</span></span>

<span data-ttu-id="a573a-4117">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4117">2</span></span>

<span data-ttu-id="a573a-4118">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4118">3</span></span>

<span data-ttu-id="a573a-4119">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4119">4</span></span>

<span data-ttu-id="a573a-4120">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4120">5</span></span>

<span data-ttu-id="a573a-4121">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4121">6</span></span>

<span data-ttu-id="a573a-4122">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4122">7</span></span>

<span data-ttu-id="a573a-4123">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4123">8</span></span>

<span data-ttu-id="a573a-4124">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4124">9</span></span>

<span data-ttu-id="a573a-4125">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4125">1</span></span><br/> <span data-ttu-id="a573a-4126">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4126">0</span></span><br/>

<span data-ttu-id="a573a-4127">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4127">1</span></span>

<span data-ttu-id="a573a-4128">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4128">2</span></span>

<span data-ttu-id="a573a-4129">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4129">3</span></span>

<span data-ttu-id="a573a-4130">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4130">4</span></span>

<span data-ttu-id="a573a-4131">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4131">5</span></span>

<span data-ttu-id="a573a-4132">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4132">6</span></span>

<span data-ttu-id="a573a-4133">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4133">7</span></span>

<span data-ttu-id="a573a-4134">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4134">8</span></span>

<span data-ttu-id="a573a-4135">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4135">9</span></span>

<span data-ttu-id="a573a-4136">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4136">2</span></span><br/> <span data-ttu-id="a573a-4137">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4137">0</span></span><br/>

<span data-ttu-id="a573a-4138">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4138">1</span></span>

<span data-ttu-id="a573a-4139">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4139">2</span></span>

<span data-ttu-id="a573a-4140">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4140">3</span></span>

<span data-ttu-id="a573a-4141">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4141">4</span></span>

<span data-ttu-id="a573a-4142">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4142">5</span></span>

<span data-ttu-id="a573a-4143">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4143">6</span></span>

<span data-ttu-id="a573a-4144">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4144">7</span></span>

<span data-ttu-id="a573a-4145">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4145">8</span></span>

<span data-ttu-id="a573a-4146">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4146">9</span></span>

<span data-ttu-id="a573a-4147">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4147">3</span></span><br/> <span data-ttu-id="a573a-4148">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4148">0</span></span><br/>

<span data-ttu-id="a573a-4149">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4149">1</span></span>

<span data-ttu-id="a573a-4150">\_двкомпарисон</span><span class="sxs-lookup"><span data-stu-id="a573a-4150">\_dwComparison</span></span>



 

<span data-ttu-id="a573a-4151">\_**двкомпарисон**: одно из следующих значений, указывающее относительное положение двух закладок в главе.</span><span class="sxs-lookup"><span data-stu-id="a573a-4151">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="a573a-4152">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-4152">Value</span></span>                               | <span data-ttu-id="a573a-4153">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-4153">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a573a-4154">ДБКОМПАРЕ \_ lt 0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-4154">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="a573a-4155">Первая закладка располагается перед второй.</span><span class="sxs-lookup"><span data-stu-id="a573a-4155">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="a573a-4156">ДБКОМПАРЕ \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="a573a-4156">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="a573a-4157">Первая закладка имеет ту же самую точку, что и вторая.</span><span class="sxs-lookup"><span data-stu-id="a573a-4157">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="a573a-4158">ДБКОМПАРЕ \_ gt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="a573a-4158">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="a573a-4159">Первая закладка размещается после второй.</span><span class="sxs-lookup"><span data-stu-id="a573a-4159">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="a573a-4160">ДБКОМПАРЕ \_ Ne 0x00000003</span><span class="sxs-lookup"><span data-stu-id="a573a-4160">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="a573a-4161">Первая закладка не совпадает с позицией второго.</span><span class="sxs-lookup"><span data-stu-id="a573a-4161">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="a573a-4162">ДБКОМПАРЕ \_ ноткомпарабле 0x00000004</span><span class="sxs-lookup"><span data-stu-id="a573a-4162">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="a573a-4163">Первая закладка не сравнима со вторым.</span><span class="sxs-lookup"><span data-stu-id="a573a-4163">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="a573a-4164">2.2.3.27 Кпмрестартпоситионин</span><span class="sxs-lookup"><span data-stu-id="a573a-4164">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="a573a-4165">Сообщение Кпмрестартпоситионин перемещает позицию выборки для курсора в начало главы.</span><span class="sxs-lookup"><span data-stu-id="a573a-4165">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="a573a-4166">Как указано в разделе 3.1.5.2.12, сервер будет отвечать с помощью того же сообщения, а результаты запроса содержатся в \_ поле Status заголовка CISP.</span><span class="sxs-lookup"><span data-stu-id="a573a-4166">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="a573a-4167">Формат сообщения Кпмрестартпоситионин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-4167">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-4168">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4168">0</span></span>

<span data-ttu-id="a573a-4169">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4169">1</span></span>

<span data-ttu-id="a573a-4170">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4170">2</span></span>

<span data-ttu-id="a573a-4171">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4171">3</span></span>

<span data-ttu-id="a573a-4172">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4172">4</span></span>

<span data-ttu-id="a573a-4173">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4173">5</span></span>

<span data-ttu-id="a573a-4174">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4174">6</span></span>

<span data-ttu-id="a573a-4175">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4175">7</span></span>

<span data-ttu-id="a573a-4176">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4176">8</span></span>

<span data-ttu-id="a573a-4177">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4177">9</span></span>

<span data-ttu-id="a573a-4178">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4178">1</span></span><br/> <span data-ttu-id="a573a-4179">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4179">0</span></span><br/>

<span data-ttu-id="a573a-4180">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4180">1</span></span>

<span data-ttu-id="a573a-4181">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4181">2</span></span>

<span data-ttu-id="a573a-4182">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4182">3</span></span>

<span data-ttu-id="a573a-4183">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4183">4</span></span>

<span data-ttu-id="a573a-4184">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4184">5</span></span>

<span data-ttu-id="a573a-4185">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4185">6</span></span>

<span data-ttu-id="a573a-4186">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4186">7</span></span>

<span data-ttu-id="a573a-4187">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4187">8</span></span>

<span data-ttu-id="a573a-4188">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4188">9</span></span>

<span data-ttu-id="a573a-4189">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4189">2</span></span><br/> <span data-ttu-id="a573a-4190">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4190">0</span></span><br/>

<span data-ttu-id="a573a-4191">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4191">1</span></span>

<span data-ttu-id="a573a-4192">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4192">2</span></span>

<span data-ttu-id="a573a-4193">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4193">3</span></span>

<span data-ttu-id="a573a-4194">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4194">4</span></span>

<span data-ttu-id="a573a-4195">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4195">5</span></span>

<span data-ttu-id="a573a-4196">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4196">6</span></span>

<span data-ttu-id="a573a-4197">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4197">7</span></span>

<span data-ttu-id="a573a-4198">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4198">8</span></span>

<span data-ttu-id="a573a-4199">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4199">9</span></span>

<span data-ttu-id="a573a-4200">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4200">3</span></span><br/> <span data-ttu-id="a573a-4201">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4201">0</span></span><br/>

<span data-ttu-id="a573a-4202">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4202">1</span></span>

<span data-ttu-id="a573a-4203">\_Хкурсор (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-4203">\_hCursor (optional)</span></span>

<span data-ttu-id="a573a-4204">\_CHAP (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a573a-4204">\_chapt (optional)</span></span>



 

<span data-ttu-id="a573a-4205">**\_ хкурсор**: 32-разрядное значение, представляющее маркер, полученное из сообщения кпмкреатекуерйоут, которое определяет запрос, для которого нужно перезапустить эту точку.</span><span class="sxs-lookup"><span data-stu-id="a573a-4205">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="a573a-4206">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="a573a-4206">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="a573a-4207">**\_ chap**: 32-разрядное значение, представляющее маркер главы, из которой извлекаются строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-4207">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="a573a-4208">Это поле должно присутствовать, когда клиент отправляет сообщение, и должно отсутствовать, когда сервер отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="a573a-4208">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="a573a-4209">2.2.3.28 Кпмфрикурсорин</span><span class="sxs-lookup"><span data-stu-id="a573a-4209">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="a573a-4210">Сообщение Кпмфрикурсорин запрашивает выпуск курсора.</span><span class="sxs-lookup"><span data-stu-id="a573a-4210">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="a573a-4211">Формат сообщения Кпмфрикурсорин, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-4211">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="a573a-4212">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4212">0</span></span>

<span data-ttu-id="a573a-4213">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4213">1</span></span>

<span data-ttu-id="a573a-4214">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4214">2</span></span>

<span data-ttu-id="a573a-4215">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4215">3</span></span>

<span data-ttu-id="a573a-4216">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4216">4</span></span>

<span data-ttu-id="a573a-4217">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4217">5</span></span>

<span data-ttu-id="a573a-4218">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4218">6</span></span>

<span data-ttu-id="a573a-4219">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4219">7</span></span>

<span data-ttu-id="a573a-4220">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4220">8</span></span>

<span data-ttu-id="a573a-4221">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4221">9</span></span>

<span data-ttu-id="a573a-4222">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4222">1</span></span><br/> <span data-ttu-id="a573a-4223">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4223">0</span></span><br/>

<span data-ttu-id="a573a-4224">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4224">1</span></span>

<span data-ttu-id="a573a-4225">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4225">2</span></span>

<span data-ttu-id="a573a-4226">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4226">3</span></span>

<span data-ttu-id="a573a-4227">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4227">4</span></span>

<span data-ttu-id="a573a-4228">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4228">5</span></span>

<span data-ttu-id="a573a-4229">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4229">6</span></span>

<span data-ttu-id="a573a-4230">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4230">7</span></span>

<span data-ttu-id="a573a-4231">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4231">8</span></span>

<span data-ttu-id="a573a-4232">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4232">9</span></span>

<span data-ttu-id="a573a-4233">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4233">2</span></span><br/> <span data-ttu-id="a573a-4234">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4234">0</span></span><br/>

<span data-ttu-id="a573a-4235">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4235">1</span></span>

<span data-ttu-id="a573a-4236">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4236">2</span></span>

<span data-ttu-id="a573a-4237">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4237">3</span></span>

<span data-ttu-id="a573a-4238">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4238">4</span></span>

<span data-ttu-id="a573a-4239">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4239">5</span></span>

<span data-ttu-id="a573a-4240">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4240">6</span></span>

<span data-ttu-id="a573a-4241">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4241">7</span></span>

<span data-ttu-id="a573a-4242">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4242">8</span></span>

<span data-ttu-id="a573a-4243">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4243">9</span></span>

<span data-ttu-id="a573a-4244">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4244">3</span></span><br/> <span data-ttu-id="a573a-4245">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4245">0</span></span><br/>

<span data-ttu-id="a573a-4246">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4246">1</span></span>

<span data-ttu-id="a573a-4247">\_хкурсор</span><span class="sxs-lookup"><span data-stu-id="a573a-4247">\_hCursor</span></span>



 

<span data-ttu-id="a573a-4248">**\_ хкурсор**: 32-разрядное значение, представляющее маркер курсора из сообщения кпмкреатекуерйоут для выпуска.</span><span class="sxs-lookup"><span data-stu-id="a573a-4248">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="a573a-4249">2.2.3.29 Кпмфрикурсораут</span><span class="sxs-lookup"><span data-stu-id="a573a-4249">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="a573a-4250">Сообщение Кпмфрикурсораут отвечает на сообщение Кпмфрикурсорин с результатами освобождения курсора.</span><span class="sxs-lookup"><span data-stu-id="a573a-4250">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="a573a-4251">Формат сообщения Кпмфрикурсораут, следующий за заголовком:</span><span class="sxs-lookup"><span data-stu-id="a573a-4251">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="a573a-4252">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4252">0</span></span>

<span data-ttu-id="a573a-4253">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4253">1</span></span>

<span data-ttu-id="a573a-4254">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4254">2</span></span>

<span data-ttu-id="a573a-4255">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4255">3</span></span>

<span data-ttu-id="a573a-4256">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4256">4</span></span>

<span data-ttu-id="a573a-4257">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4257">5</span></span>

<span data-ttu-id="a573a-4258">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4258">6</span></span>

<span data-ttu-id="a573a-4259">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4259">7</span></span>

<span data-ttu-id="a573a-4260">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4260">8</span></span>

<span data-ttu-id="a573a-4261">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4261">9</span></span>

<span data-ttu-id="a573a-4262">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4262">1</span></span><br/> <span data-ttu-id="a573a-4263">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4263">0</span></span><br/>

<span data-ttu-id="a573a-4264">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4264">1</span></span>

<span data-ttu-id="a573a-4265">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4265">2</span></span>

<span data-ttu-id="a573a-4266">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4266">3</span></span>

<span data-ttu-id="a573a-4267">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4267">4</span></span>

<span data-ttu-id="a573a-4268">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4268">5</span></span>

<span data-ttu-id="a573a-4269">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4269">6</span></span>

<span data-ttu-id="a573a-4270">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4270">7</span></span>

<span data-ttu-id="a573a-4271">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4271">8</span></span>

<span data-ttu-id="a573a-4272">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4272">9</span></span>

<span data-ttu-id="a573a-4273">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4273">2</span></span><br/> <span data-ttu-id="a573a-4274">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4274">0</span></span><br/>

<span data-ttu-id="a573a-4275">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4275">1</span></span>

<span data-ttu-id="a573a-4276">2</span><span class="sxs-lookup"><span data-stu-id="a573a-4276">2</span></span>

<span data-ttu-id="a573a-4277">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4277">3</span></span>

<span data-ttu-id="a573a-4278">4</span><span class="sxs-lookup"><span data-stu-id="a573a-4278">4</span></span>

<span data-ttu-id="a573a-4279">5</span><span class="sxs-lookup"><span data-stu-id="a573a-4279">5</span></span>

<span data-ttu-id="a573a-4280">6</span><span class="sxs-lookup"><span data-stu-id="a573a-4280">6</span></span>

<span data-ttu-id="a573a-4281">7</span><span class="sxs-lookup"><span data-stu-id="a573a-4281">7</span></span>

<span data-ttu-id="a573a-4282">8</span><span class="sxs-lookup"><span data-stu-id="a573a-4282">8</span></span>

<span data-ttu-id="a573a-4283">9</span><span class="sxs-lookup"><span data-stu-id="a573a-4283">9</span></span>

<span data-ttu-id="a573a-4284">3</span><span class="sxs-lookup"><span data-stu-id="a573a-4284">3</span></span><br/> <span data-ttu-id="a573a-4285">0</span><span class="sxs-lookup"><span data-stu-id="a573a-4285">0</span></span><br/>

<span data-ttu-id="a573a-4286">1</span><span class="sxs-lookup"><span data-stu-id="a573a-4286">1</span></span>

<span data-ttu-id="a573a-4287">\_ккурсорсремаининг</span><span class="sxs-lookup"><span data-stu-id="a573a-4287">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="a573a-4288">**\_ ккурсорсремаининг**: 32-битовое целое число без знака, указывающее количество курсоров, которые все еще используются для запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-4288">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="a573a-4289">2.2.3.30 Кпмдисконнект</span><span class="sxs-lookup"><span data-stu-id="a573a-4289">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="a573a-4290">Сообщение Кпмдисконнект завершает подключение к серверу</span><span class="sxs-lookup"><span data-stu-id="a573a-4290">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="a573a-4291">Сообщение не должно включать текст. будет отправлен только заголовок сообщения, как указано в разделе 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="a573a-4291">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="a573a-4292">ошибки 2.2.4</span><span class="sxs-lookup"><span data-stu-id="a573a-4292">2.2.4 Errors</span></span>

<span data-ttu-id="a573a-4293">Все сообщения протокола службы индексирования содержимого должны возвращать 0x00000000 при успешном выполнении; в противном случае они возвращают 32-разрядный ненулевой код ошибки, который может быть либо HRESULT, либо значением NTSTATUS (см. раздел 1,8).</span><span class="sxs-lookup"><span data-stu-id="a573a-4293">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="a573a-4294">Если буфер слишком мал и не умещается в результате, \_ должен быть возвращен код состояния недостаточно \_ ресурсов (0xC0000009A), и Неудачная операция должна быть повторена с буфером большего размера.</span><span class="sxs-lookup"><span data-stu-id="a573a-4294">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="a573a-4295">Все остальные значения ошибок должны обрабатываться одинаково.</span><span class="sxs-lookup"><span data-stu-id="a573a-4295">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="a573a-4296">(Обратите внимание, что в настоящее время пробелы в значениях HRESULT и NTSTATUS не перекрываются, за исключением идентичных значений, но даже в случае возникновения конфликтов в будущем это не вызовет никаких проблем с протоколом, если значение параметра STATUS \_ Недостаточные \_ ресурсы остаются уникальными, так как все остальные значения ошибок обрабатываются одинаково.)</span><span class="sxs-lookup"><span data-stu-id="a573a-4296">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="a573a-4297">3. Сведения о протоколе</span><span class="sxs-lookup"><span data-stu-id="a573a-4297">3 Protocol Details</span></span>

-   [<span data-ttu-id="a573a-4298">Сведения о сервере 3,1</span><span class="sxs-lookup"><span data-stu-id="a573a-4298">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="a573a-4299">3,2. сведения о клиенте</span><span class="sxs-lookup"><span data-stu-id="a573a-4299">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="a573a-4300">Запросы сообщений CISP для удаленного запроса каталогов службы индексирования не нуждаются в определенной последовательности.</span><span class="sxs-lookup"><span data-stu-id="a573a-4300">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="a573a-4301">Рекомендуется, чтобы более высокий уровень приступил к осмысленной последовательности сообщений, как и для сообщений, полученных из этой последовательности или с недопустимыми данными, сервер будет отвечать с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a573a-4301">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="a573a-4302">Некоторые сообщения также зависят от более высокого уровня, предоставляющего допустимые данные, полученные в сообщениях, предшествующих последовательности.</span><span class="sxs-lookup"><span data-stu-id="a573a-4302">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="a573a-4303">На следующей схеме показана типичная последовательность сообщений для простого запроса от клиента к удаленному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="a573a-4303">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![последовательность сообщений для простого запроса](images/protocoldetails.jpg)

<span data-ttu-id="a573a-4305">Сообщения, представленные на предыдущей схеме, представляют собой подмножество всех сообщений CISP, используемых для запроса каталога службы удаленного индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-4305">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="a573a-4306">Сведения о сервере 3,1</span><span class="sxs-lookup"><span data-stu-id="a573a-4306">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="a573a-4307">3.1.1. Абстрактная модель данных</span><span class="sxs-lookup"><span data-stu-id="a573a-4307">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="a573a-4308">В следующем разделе задаются данные и состояние, поддерживаемые сервером CISP.</span><span class="sxs-lookup"><span data-stu-id="a573a-4308">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="a573a-4309">Приведенные здесь данные предназначены для упрощения объяснения того, как работает протокол.</span><span class="sxs-lookup"><span data-stu-id="a573a-4309">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="a573a-4310">Этот раздел не требует, чтобы реализации применялись к этой модели, если их внешнее поведение согласуется с, описанным в этом документе.</span><span class="sxs-lookup"><span data-stu-id="a573a-4310">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="a573a-4311">Служба индексирования, реализующая CISP, должна поддерживать следующие абстрактные элементы данных:</span><span class="sxs-lookup"><span data-stu-id="a573a-4311">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="a573a-4312">Список клиентов, подключенных к серверу</span><span class="sxs-lookup"><span data-stu-id="a573a-4312">The list of clients connected to the server</span></span>
-   <span data-ttu-id="a573a-4313">Сведения о каждом клиенте, включая:</span><span class="sxs-lookup"><span data-stu-id="a573a-4313">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="a573a-4314">Версия клиента (как указано в сообщении Кпмконнектин, указанном в разделе 2.2.3.6)</span><span class="sxs-lookup"><span data-stu-id="a573a-4314">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="a573a-4315">Каталог, связанный с клиентом (с помощью сообщения Кпмконнектин)</span><span class="sxs-lookup"><span data-stu-id="a573a-4315">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="a573a-4316">Дополнительные свойства клиента, как указано в разделе 2.2.1.21.1.</span><span class="sxs-lookup"><span data-stu-id="a573a-4316">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="a573a-4317">Поисковый запрос клиента</span><span class="sxs-lookup"><span data-stu-id="a573a-4317">Client's search query</span></span>
    -   <span data-ttu-id="a573a-4318">Список дескрипторов курсоров для запроса и позиции в результирующем наборе для каждого дескриптора.</span><span class="sxs-lookup"><span data-stu-id="a573a-4318">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="a573a-4319">Текущий набор привязок</span><span class="sxs-lookup"><span data-stu-id="a573a-4319">Current set of bindings</span></span>
    -   <span data-ttu-id="a573a-4320">Текущее состояние запроса, включающего (для каждого курсора):</span><span class="sxs-lookup"><span data-stu-id="a573a-4320">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="a573a-4321">Число строк в результатах запроса</span><span class="sxs-lookup"><span data-stu-id="a573a-4321">Number of rows in query result</span></span>
        -   <span data-ttu-id="a573a-4322">Числитель и знаменатель завершения запроса</span><span class="sxs-lookup"><span data-stu-id="a573a-4322">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="a573a-4323">Последнее число строк, сообщаемое последним сообщением Кпмратиофинишедаут для данного курсора</span><span class="sxs-lookup"><span data-stu-id="a573a-4323">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="a573a-4324">Будет ли запрос отслеживаться сервером на предмет изменений в результатах запроса, и если он отслеживается, что изменилось в результатах запроса с момента последнего сообщения клиенту, Кпмсенднотифйоут</span><span class="sxs-lookup"><span data-stu-id="a573a-4324">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="a573a-4325">Список обработчиков глав, обслуживаемых этим запросом клиенту.</span><span class="sxs-lookup"><span data-stu-id="a573a-4325">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="a573a-4326">Список дескрипторов закладок для каждого курсора, обслуживаемого этим запросом клиенту.</span><span class="sxs-lookup"><span data-stu-id="a573a-4326">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="a573a-4327">Текущее состояние службы индексирования, которое может быть "не инициализировано", "выполняется" или "завершение работы".</span><span class="sxs-lookup"><span data-stu-id="a573a-4327">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="a573a-4328">Обратите внимание, что большая часть времени сервера находится в состоянии "выполняется".</span><span class="sxs-lookup"><span data-stu-id="a573a-4328">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="a573a-4329">Ниже приведена схема конечного автомата для сервера.</span><span class="sxs-lookup"><span data-stu-id="a573a-4329">Following is the state machine diagram for the server:</span></span>

    ![схема конечного автомата сервера службы индексирования](images/abstractdatamodel.jpg)

-   <span data-ttu-id="a573a-4331">Сведения о каталоге: Количество индексируемых документов, размер индекса, число уникальных ключей и т. д. (см. раздел 2.2.3.1 для полного списка), State (соответствует значениям Двневстате в разделе 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="a573a-4331">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="a573a-4332">Для каждого поддерживаемого языка база данных вариантов слов, описанная в разделе 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="a573a-4332">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="a573a-4333">3.1.2. Таймеры</span><span class="sxs-lookup"><span data-stu-id="a573a-4333">3.1.2 Timers</span></span>

<span data-ttu-id="a573a-4334">Таймеры протокола не требуются.</span><span class="sxs-lookup"><span data-stu-id="a573a-4334">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="a573a-4335">3.1.3. Инициализация</span><span class="sxs-lookup"><span data-stu-id="a573a-4335">3.1.3 Initialization</span></span>

<span data-ttu-id="a573a-4336">После инициализации сервер должен установить свое состояние "не инициализировано" и начать прослушивание сообщений по именованному каналу, указанному в разделе 1,9.</span><span class="sxs-lookup"><span data-stu-id="a573a-4336">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="a573a-4337">После выполнения любой другой внутренней инициализации она должна перейти в состояние "выполняется".</span><span class="sxs-lookup"><span data-stu-id="a573a-4337">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="a573a-4338">3.1.4. Активируемые события более высокого уровня</span><span class="sxs-lookup"><span data-stu-id="a573a-4338">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="a573a-4339">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a573a-4339">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="a573a-4340">Правила обработки сообщений 3.1.5. и последовательности</span><span class="sxs-lookup"><span data-stu-id="a573a-4340">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="a573a-4341">При возникновении ошибки во время обработки сообщения, отправленного клиентом, сервер должен сообщить об ошибке обратно клиенту следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4341">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="a573a-4342">Прерывать обработку сообщения, отправленного клиентом</span><span class="sxs-lookup"><span data-stu-id="a573a-4342">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="a573a-4343">Ответ с заголовком сообщения (только) сообщения, отправленного клиентом, оставляя \_ поле сообщения неизменным.</span><span class="sxs-lookup"><span data-stu-id="a573a-4343">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="a573a-4344">Задайте в \_ поле Состояние значение кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="a573a-4344">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="a573a-4345">При поступлении сообщения сервер должен проверить \_ значение поля MSG, чтобы узнать, является ли он известным типом (см. раздел 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="a573a-4345">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="a573a-4346">Если тип неизвестен, он должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4346">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="a573a-4347">После этого сервер должен проверить \_ значение поля улчекксум, если тип сообщения имеет одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a573a-4347">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="a573a-4348">Кпмконнектин (0x000000C8)</span><span class="sxs-lookup"><span data-stu-id="a573a-4348">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="a573a-4349">Кпмкреатекуерин (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="a573a-4349">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="a573a-4350">Кпмсетбиндингсин (0x000000D0)</span><span class="sxs-lookup"><span data-stu-id="a573a-4350">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="a573a-4351">Кпмжетровсин (0x000000CC)</span><span class="sxs-lookup"><span data-stu-id="a573a-4351">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="a573a-4352">Кпмфетчвалуеин (0x000000E4)</span><span class="sxs-lookup"><span data-stu-id="a573a-4352">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="a573a-4353">Чтобы проверить \_ значение поля улчекксум, сервер должен проверить значение, указанное клиентом в \_ поле Иклиентверсион сообщения кпмконнектин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4353">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="a573a-4354">Если \_ для поля иклиентверсион не задано значение 0x00000008, а \_ для поля улчекксум не задано значение 0x00000000, сервер должен сообщить о состоянии \_ недопустимого \_ параметра (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4354">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="a573a-4355">Сервер не должен проверять \_ поле улчекксум для клиентов, присвойте \_ полю иклиентверсион значение меньше 0x00000008.</span><span class="sxs-lookup"><span data-stu-id="a573a-4355">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="a573a-4356">Если \_ значение поля иклиентверсионфиелд равно 0x00000008 или больше, сервер должен проверить, что \_ поле улчекксум было вычислено как указано в разделе 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="a573a-4356">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="a573a-4357">Если \_ значение улчекксум недопустимо, сервер должен сообщить \_ \_ об ошибке состояния недопустимого параметра (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4357">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="a573a-4358">Затем сервер проверяет, в каком состоянии находится.</span><span class="sxs-lookup"><span data-stu-id="a573a-4358">Next, the server checks which state is it in.</span></span> <span data-ttu-id="a573a-4359">Если состояние "не инициализировано", сервер должен сообщить \_ \_ об ошибке CI E Not \_ Initialized (0x8004180B).</span><span class="sxs-lookup"><span data-stu-id="a573a-4359">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="a573a-4360">Если состояние "завершение работы", сервер должен сообщить \_ об ошибке "CI E \_ Shutdown (0x80041812)".</span><span class="sxs-lookup"><span data-stu-id="a573a-4360">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="a573a-4361">После того как заголовок определен как допустимый и сервер находится в состоянии "выполняется", дальнейшая обработка сообщений должна быть выполнена, как указано в подразделах ниже.</span><span class="sxs-lookup"><span data-stu-id="a573a-4361">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="a573a-4362">Управление каталогом службы удаленного индексирования 3.1.5.1</span><span class="sxs-lookup"><span data-stu-id="a573a-4362">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="a573a-4363">3.1.5.1.1 получение запроса КпмЦистатеинаут</span><span class="sxs-lookup"><span data-stu-id="a573a-4363">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="a573a-4364">Когда сервер получает запрос сообщения КпмЦистатеинаут от клиента, сервер должен сначала проверить, находится ли клиент в списке подключенных клиентов.</span><span class="sxs-lookup"><span data-stu-id="a573a-4364">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="a573a-4365">Если клиент отсутствует в списке, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4365">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="a573a-4366">В противном случае он должен ответить клиенту сообщением КпмЦистатеинаут, заполняя его данными о связанном с клиентом каталоге, как указано в разделе 2.2.3.1.</span><span class="sxs-lookup"><span data-stu-id="a573a-4366">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="a573a-4367">3.1.5.1.2 получение запроса Кпмсеткатстатеин</span><span class="sxs-lookup"><span data-stu-id="a573a-4367">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="a573a-4368">Когда сервер получает запрос сообщения Кпмсеткатстатеин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4368">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4369">Убедитесь, что у клиента есть административный доступ.</span><span class="sxs-lookup"><span data-stu-id="a573a-4369">Check that client has administrative access.</span></span> <span data-ttu-id="a573a-4370">Если у клиента отсутствует административный доступ, сервер должен сообщить \_ \_ об ошибке отказа в доступе (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="a573a-4370">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="a573a-4371">Если \_ двневстате не равно Цикат \_ все открытые, \_ измените состояние каталога, указанного в поле катнаме, как указано в \_ поле двневстате.</span><span class="sxs-lookup"><span data-stu-id="a573a-4371">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="a573a-4372">Дополнительные сведения см. в разделе 2.2.3.2.</span><span class="sxs-lookup"><span data-stu-id="a573a-4372">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="a573a-4373">Если сервер не находит каталог с именем, указанным в поле Катнаме, сервер должен вернуть состояние \_ Ошибка недопустимого \_ параметра (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4373">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4374">Ответ на клиент с помощью сообщения Кпмсеткатстатеаут, где \_ ДВОЛДСТАТЕ должно быть установлено предыдущее состояние каталога.</span><span class="sxs-lookup"><span data-stu-id="a573a-4374">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="a573a-4375">Если \_ двневстате РАВЕН Цикат \_ все \_ открытые, сервер должен проверить состояние всех каталогов и, если все они запущены, должен установить \_ для дволдстате значение 0x00000001, а в противном случае задать для \_ дволдстате значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4375">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="a573a-4376">3.1.5.1.3 получение запроса Кпмупдатедокументсин</span><span class="sxs-lookup"><span data-stu-id="a573a-4376">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="a573a-4377">Когда сервер получает запрос сообщения Кпмупдатедокументсин, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4377">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4378">Проверьте, находится ли клиент в списке подключенных клиентов (которые имеют связанный каталог).</span><span class="sxs-lookup"><span data-stu-id="a573a-4378">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="a573a-4379">Если клиент отсутствует в списке, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4379">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4380">Убедитесь, что у клиента есть административный доступ.</span><span class="sxs-lookup"><span data-stu-id="a573a-4380">Check that client has administrative access.</span></span> <span data-ttu-id="a573a-4381">Если у клиента нет прав администратора для доступа к серверу, сервер должен сообщить \_ \_ об ошибке отказа в доступе (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="a573a-4381">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="a573a-4382">Начало процесса индексирования пути, указанного клиентом, выполнение полного или добавочного сканирования в зависимости от значения \_ поля флага в сообщении кпмупдатедокументсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4382">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="a573a-4383">Если путь не был ранее проиндексирован, его необходимо добавить в коллекцию индексированных расположений и выполнить полную проверку.</span><span class="sxs-lookup"><span data-stu-id="a573a-4383">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="a573a-4384">Если указано недопустимое значение \_ поля флага, сервер должен действовать так, как если бы \_ флаг был установлен в значение UPD \_ init и выполнял полную проверку.</span><span class="sxs-lookup"><span data-stu-id="a573a-4384">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="a573a-4385">Эта операция должна выполняться в каталоге, связанном с клиентом.</span><span class="sxs-lookup"><span data-stu-id="a573a-4385">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="a573a-4386">Ответьте на клиент с помощью заголовка сообщения для Кпмупдатедокументсин и задайте в \_ поле Status результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-4386">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="a573a-4387">3.1.5.1.4 получение запроса Кпмфорцемержеин</span><span class="sxs-lookup"><span data-stu-id="a573a-4387">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="a573a-4388">Когда сервер получает запрос сообщения Кпмфорцемержеин, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4388">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4389">Проверьте, находится ли клиент в списке подключенных клиентов (которые имеют связанный каталог).</span><span class="sxs-lookup"><span data-stu-id="a573a-4389">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="a573a-4390">Если клиент отсутствует в списке, сервер должен сообщить \_ об ошибке состояния "Недопустимый \_ параметр" (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4390">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4391">Убедитесь, что у клиента есть административный доступ.</span><span class="sxs-lookup"><span data-stu-id="a573a-4391">Check that client has administrative access.</span></span> <span data-ttu-id="a573a-4392">Если у клиента отсутствует административный доступ, сервер должен сообщить \_ \_ об ошибке отказа в доступе (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="a573a-4392">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="a573a-4393">Начните любой процесс обслуживания, необходимый для повышения производительности запросов к каталогу, связанному с клиентом.</span><span class="sxs-lookup"><span data-stu-id="a573a-4393">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="a573a-4394">Ответьте на клиент с помощью заголовка сообщения для Кпмфорцемержеин и задайте в \_ поле Status результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-4394">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="a573a-4395">Обратите внимание, что процесс обслуживания является асинхронным и может продолжаться после того, как клиент получит ответное сообщение.</span><span class="sxs-lookup"><span data-stu-id="a573a-4395">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="a573a-4396">Этот процесс не влияет непосредственно на протокол (кроме времени отклика).</span><span class="sxs-lookup"><span data-stu-id="a573a-4396">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="a573a-4397">Запросы удаленной службы индексирования 3.1.5.2</span><span class="sxs-lookup"><span data-stu-id="a573a-4397">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="a573a-4398">3.1.5.2.1 получение запроса Кпмконнектин</span><span class="sxs-lookup"><span data-stu-id="a573a-4398">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="a573a-4399">Когда сервер получает запрос Кпмконнектин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4399">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4400">Проверьте, находится ли клиент в списке подключенных клиентов.</span><span class="sxs-lookup"><span data-stu-id="a573a-4400">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="a573a-4401">В этом случае сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4401">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4402">Проверяет, существует ли указанный каталог, но не находится в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="a573a-4402">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="a573a-4403">Если это не так, то сервер должен сообщить \_ \_ об ошибке Reporting E без \_ каталога (0x8004181D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4403">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="a573a-4404">Добавьте клиент в список подключенных клиентов.</span><span class="sxs-lookup"><span data-stu-id="a573a-4404">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="a573a-4405">Свяжите каталог с клиентом.</span><span class="sxs-lookup"><span data-stu-id="a573a-4405">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="a573a-4406">Храните в состоянии клиента сведения, передаваемые в сообщении Кпмконнектин (например, имя каталога, версия клиента и т. д.).</span><span class="sxs-lookup"><span data-stu-id="a573a-4406">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="a573a-4407">Ответ на клиент с помощью сообщения Кпмконнектаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4407">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="a573a-4408">3.1.5.2.2 получение запроса Кпмкреатекуерин</span><span class="sxs-lookup"><span data-stu-id="a573a-4408">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="a573a-4409">Когда сервер получает запрос сообщения Кпмкреатекуерин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4409">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4410">Проверьте, находится ли клиент в списке подключенных клиентов.</span><span class="sxs-lookup"><span data-stu-id="a573a-4410">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="a573a-4411">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4411">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4412">Убедитесь, что у клиента уже есть связанный с ним запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4412">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="a573a-4413">В этом случае сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4413">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4414">Проверьте, находится ли каталог, связанный с клиентом, в состоянии, что позволяет обрабатывать запросы (ЦИКАТ \_ ReadOnly или Цикат с \_ возможностью записи).</span><span class="sxs-lookup"><span data-stu-id="a573a-4414">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="a573a-4415">Если это не так, сервер должен сообщить \_ \_ \_ об ошибке запроса No (0x8004160C).</span><span class="sxs-lookup"><span data-stu-id="a573a-4415">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="a573a-4416">Проанализируйте набор ограничений, порядок сортировки и группирования, указанные в запросе.</span><span class="sxs-lookup"><span data-stu-id="a573a-4416">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="a573a-4417">Если сервер обнаруживает ошибку, он должен сообщить о соответствующей ошибке.</span><span class="sxs-lookup"><span data-stu-id="a573a-4417">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="a573a-4418">Если по какой бы то ни было причине этот шаг завершается сбоем, сервер должен сообщить об обнаруженной ошибке.</span><span class="sxs-lookup"><span data-stu-id="a573a-4418">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="a573a-4419">Сведения об ошибках запросов службы индексирования см \[ . в разделе MSDN-куерерр \] .</span><span class="sxs-lookup"><span data-stu-id="a573a-4419">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="a573a-4420">Сохраните поисковый запрос в состоянии клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-4420">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="a573a-4421">Выполните все подготовительные действия, необходимые для обслуживания строк на клиенте, и свяжите запрос с соответствующими дескрипторами курсора (в зависимости от информации, передаваемой в сообщении Кпмкреатекуерин).</span><span class="sxs-lookup"><span data-stu-id="a573a-4421">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="a573a-4422">Добавьте эти дескрипторы в список дескрипторов курсоров клиента и инициализируйте списки дескрипторов глав и закладок.</span><span class="sxs-lookup"><span data-stu-id="a573a-4422">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="a573a-4423">Инициализировать список дескрипторов глав для каждого курсора в этом запросе на базу данных \_ со значением NULL \_ параметру hChapter</span><span class="sxs-lookup"><span data-stu-id="a573a-4423">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="a573a-4424">Инициализируйте список дескрипторов закладок для каждого курсора в этом запросе на набор ДББМК \_ First и дббмк \_ Last.</span><span class="sxs-lookup"><span data-stu-id="a573a-4424">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="a573a-4425">Пометьте запрос как неотслеживаемый для изменений.</span><span class="sxs-lookup"><span data-stu-id="a573a-4425">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="a573a-4426">Инициализирует количество строк до текущего вычисленного числа строк (может быть 0, если запрос не начал выполнение или какое-либо число, если запрос находится в процессе выполнения) и инициализирует числитель и знаменатель завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-4426">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="a573a-4427">Ответ на клиент с помощью сообщения Кпмкреатекуерйоут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4427">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="a573a-4428">3.1.5.2.3 получение запроса Кпмжеткуеристатусин</span><span class="sxs-lookup"><span data-stu-id="a573a-4428">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="a573a-4429">Когда сервер получает запрос сообщения Кпмжеткуеристатусин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4429">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4430">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4430">Check if the client has query associated with it.</span></span> <span data-ttu-id="a573a-4431">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4431">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4432">Проверьте, находится ли дескриптор курсора в списке дескрипторов курсора клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-4432">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="a573a-4433">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="a573a-4433">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="a573a-4434">Подготовка сообщения Кпмжеткуеристатусаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4434">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="a573a-4435">Сервер должен получить текущее состояние запроса и задать его в \_ поле кстатус (см. 2.2.3.11 для возможных значений).</span><span class="sxs-lookup"><span data-stu-id="a573a-4435">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="a573a-4436">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a573a-4436">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="a573a-4437">Ответ на клиент с помощью сообщения Кпмжеткуеристатусаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4437">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="a573a-4438">3.1.5.2.4 получение запроса Кпмжеткуеристатусексин</span><span class="sxs-lookup"><span data-stu-id="a573a-4438">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="a573a-4439">Когда сервер получает запрос сообщения Кпмжеткуеристатусексин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4439">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4440">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4440">Check if the client has a query associated with it.</span></span> <span data-ttu-id="a573a-4441">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4441">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4442">Проверьте, находится ли переданный дескриптор курсора в списке дескрипторов курсора клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-4442">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="a573a-4443">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="a573a-4443">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="a573a-4444">Подготовка сообщения Кпмжеткуеристатусексаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4444">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="a573a-4445">Сервер должен получить текущее состояние запроса и ход выполнения запроса и задать Кстатус (см. 2.2.3.11 для возможных значений), \_ двратиофинишедденоминатор и \_ двратиофинишеднумератор соответственно.</span><span class="sxs-lookup"><span data-stu-id="a573a-4445">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="a573a-4446">Затем необходимо задать для кровстотал число строк в результатах запроса \_ .</span><span class="sxs-lookup"><span data-stu-id="a573a-4446">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="a573a-4447">Если этот шаг завершается неудачей по каким либо причинам, сервер должен сообщить о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="a573a-4447">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="a573a-4448">Получите сведения о каталоге клиента и заполните \_ кфилтереддокументс и \_ кдокументстофилтер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4448">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="a573a-4449">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="a573a-4449">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="a573a-4450">Получите расположение закладки, обозначенной маркером в \_ поле БМК, и заполните оставшееся \_ поле ировбмк в сообщении кпмжеткуеристатусексаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4450">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="a573a-4451">Если этот шаг завершается неудачей по каким либо причинам, сервер должен сообщить о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="a573a-4451">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="a573a-4452">Ответ на клиент с помощью сообщения Кпмжеткуеристатусексаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4452">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="a573a-4453">3.1.5.2.5 получение запроса Кпмратиофинишедин</span><span class="sxs-lookup"><span data-stu-id="a573a-4453">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="a573a-4454">Когда сервер получает запрос сообщения Кпмратиофинишедин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4454">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4455">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4455">Check if the client has query associated with it.</span></span> <span data-ttu-id="a573a-4456">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4456">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4457">Проверьте, находится ли переданный дескриптор курсора в списке дескрипторов курсора клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-4457">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="a573a-4458">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="a573a-4458">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="a573a-4459">Подготовка сообщения Кпмратиофинишедаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4459">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="a573a-4460">Сервер должен получить состояние запроса клиента и заполнить \_ поля улнумератор, \_ улденоминатор и \_ CRowset.</span><span class="sxs-lookup"><span data-stu-id="a573a-4460">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="a573a-4461">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="a573a-4461">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="a573a-4462">Если \_ CRowset равно последнему сообщаемому числу строк для этого запроса, установите \_ фневровс в 0x00000000, в противном случае задайте для него значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="a573a-4462">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="a573a-4463">Обновить Последнее сообщаемое количество строк для этого запроса до значения \_ CRowset.</span><span class="sxs-lookup"><span data-stu-id="a573a-4463">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="a573a-4464">Ответ на клиент с помощью сообщения Кпмратиофинишедаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4464">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="a573a-4465">3.1.5.2.6 получение запроса Кпмсетбиндингсин</span><span class="sxs-lookup"><span data-stu-id="a573a-4465">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="a573a-4466">Когда сервер получает запрос сообщения Кпмсетбиндингсин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4466">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4467">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4467">Check if the client has a query associated with it.</span></span> <span data-ttu-id="a573a-4468">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4468">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4469">Проверьте, находится ли переданный дескриптор курсора в списке дескрипторов курсора клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-4469">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="a573a-4470">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="a573a-4470">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="a573a-4471">Убедитесь, что сведения о привязках допустимы (т. е. столбец, по крайней мере, указывает значение, длину или состояние, которое должно быть возвращено; не пересекается в привязках для значения, длины или состояния; и значения, длины и состояния в указанном размере строки) и если не сообщать \_ \_ об ошибке DB e Бадбиндинфо (0x80040E08).</span><span class="sxs-lookup"><span data-stu-id="a573a-4471">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="a573a-4472">Сохраните сведения о привязке, связанные со столбцами, указанными в поле Аколумнс.</span><span class="sxs-lookup"><span data-stu-id="a573a-4472">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="a573a-4473">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="a573a-4473">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="a573a-4474">Ответ на клиент с заголовком сообщения (только) с \_ установленным сообщением кпмсетбиндингсин и \_ состоянием, равным результатам указанной привязки.</span><span class="sxs-lookup"><span data-stu-id="a573a-4474">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="a573a-4475">3.1.5.2.7 получение запроса Кпмжетровсин</span><span class="sxs-lookup"><span data-stu-id="a573a-4475">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="a573a-4476">Когда сервер получает запрос сообщения Кпмжетровсин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4476">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4477">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4477">Check if the client has query associated with it.</span></span> <span data-ttu-id="a573a-4478">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4478">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4479">Убедитесь, что переданный дескриптор курсора находится в аселист дескрипторов курсора клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-4479">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="a573a-4480">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="a573a-4480">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="a573a-4481">Проверьте, имеет ли клиент текущий набор привязок.</span><span class="sxs-lookup"><span data-stu-id="a573a-4481">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="a573a-4482">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="a573a-4482">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="a573a-4483">Подготовка сообщения Кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4483">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="a573a-4484">Сервер должен располагать курсор в результатах запроса, как указано в описании поиска.</span><span class="sxs-lookup"><span data-stu-id="a573a-4484">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="a573a-4485">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="a573a-4485">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="a573a-4486">Выберет столько строк, сколько замещается в буфере, размер которого обозначен параметром \_ кбреадбуффер, но не больше, чем указано в \_ кровстотрансфер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4486">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="a573a-4487">При выборке строк сервер должен сравнить тип значения свойства выбранного столбца с типом, указанным в текущем наборе привязок клиента (раздел 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="a573a-4487">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="a573a-4488">Если тип в привязке не является \_ вариантом VT, сервер должен попытаться преобразовать значение свойства столбца в этот тип.</span><span class="sxs-lookup"><span data-stu-id="a573a-4488">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="a573a-4489">В противном случае, если установлен \_ флаг DBPROP усикстендеддбтипес в \_ наборе свойств DBPROPSET куерекст клиента или если значение свойства столбца не является \_ векторным типом VT, значение свойства должно возвращаться в его нормальном типе.</span><span class="sxs-lookup"><span data-stu-id="a573a-4489">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="a573a-4490">Если ни один из вариантов не является случайом (т. е. у сервера есть \_ Векторный тип VT, а клиент не поддерживает \_ вектор VT), сервер должен попытаться преобразовать его в \_ тип массива VT следующим образом: VT \_ i8, VT \_ UI8, VT \_ fileTime и VT \_ CLSID элементы массива не могут быть преобразованы, а завершаться ошибкой. \_Элементы массива VT LPSTR и VT \_ LPWSTR должны быть преобразованы в VT \_ BSTR; элементы массива всех остальных типов должны оставаться неизменными.</span><span class="sxs-lookup"><span data-stu-id="a573a-4490">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="a573a-4491">Наконец, если столбцы строки содержат дескрипторы глав или маркеры закладок, сервер должен обновить соответствующие списки.</span><span class="sxs-lookup"><span data-stu-id="a573a-4491">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="a573a-4492">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="a573a-4492">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="a573a-4493">Сохранение фактического числа строк, извлекаемых в \_ кровсретурнед.</span><span class="sxs-lookup"><span data-stu-id="a573a-4493">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="a573a-4494">Скопируйте описание поиска и поле раздела из Кпмжетровсин в сообщение Кпмжетровсаут для отправки.</span><span class="sxs-lookup"><span data-stu-id="a573a-4494">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="a573a-4495">Сохранять полученные строки в поле строк (см. Примечание о состоянии ниже и разделе 2.2.3.16 в структуре поля строк).</span><span class="sxs-lookup"><span data-stu-id="a573a-4495">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="a573a-4496">Ответ на клиент с помощью сообщения Кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4496">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="a573a-4497">Примечание о поле "байт состояния":</span><span class="sxs-lookup"><span data-stu-id="a573a-4497">Note on status byte field:</span></span>

<span data-ttu-id="a573a-4498">Если для Статусусед задано значение 0x01 в Ктаблеколумн сообщения Кпмсетбиндингин для столбца, то сервер должен установить байт состояния (который находится в Статусоффсет с начала строки) для этого столбца в одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a573a-4498">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="a573a-4499">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-4499">Value</span></span> | <span data-ttu-id="a573a-4500">Значение</span><span class="sxs-lookup"><span data-stu-id="a573a-4500">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="a573a-4501">0x00</span><span class="sxs-lookup"><span data-stu-id="a573a-4501">0x00</span></span>  | <span data-ttu-id="a573a-4502">статусок</span><span class="sxs-lookup"><span data-stu-id="a573a-4502">StatusOK</span></span>       |
| <span data-ttu-id="a573a-4503">0x01</span><span class="sxs-lookup"><span data-stu-id="a573a-4503">0x01</span></span>  | <span data-ttu-id="a573a-4504">статусдеферред</span><span class="sxs-lookup"><span data-stu-id="a573a-4504">StatusDeferred</span></span> |
| <span data-ttu-id="a573a-4505">0x02</span><span class="sxs-lookup"><span data-stu-id="a573a-4505">0x02</span></span>  | <span data-ttu-id="a573a-4506">статуснулл</span><span class="sxs-lookup"><span data-stu-id="a573a-4506">StatusNull</span></span>     |



 

<span data-ttu-id="a573a-4507">Если значение свойства отсутствует для этой строки, сервер должен задать для параметра Byte состояния значение Статуснулл.</span><span class="sxs-lookup"><span data-stu-id="a573a-4507">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="a573a-4508">Если значение слишком велико для передачи в сообщение Кпмжетровсаут, сервер должен задать для параметра Byte состояния значение Статусдеферред.</span><span class="sxs-lookup"><span data-stu-id="a573a-4508">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="a573a-4509">В противном случае сервер должен установить байт состояния в Статусок.</span><span class="sxs-lookup"><span data-stu-id="a573a-4509">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="a573a-4510">3.1.5.2.8 получение запроса Кпмфетчвалуеин</span><span class="sxs-lookup"><span data-stu-id="a573a-4510">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="a573a-4511">Когда сервер получает запрос сообщения Кпмфетчвалуеин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4511">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4512">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4512">Check if the client has query associated with it.</span></span> <span data-ttu-id="a573a-4513">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4513">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4514">Подготовка сообщения Кпмфетчвалуеаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4514">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="a573a-4515">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a573a-4515">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="a573a-4516">Найдите документ, указанный в \_ поле WID, и проверьте, доступен ли для этого клиента идентификатор свойства для этого документа (в дальнейшем именуемый как "значение свойства"), указанный в структуре пропспек.</span><span class="sxs-lookup"><span data-stu-id="a573a-4516">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="a573a-4517">Если это значение недоступно, сервер должен установить значение \_ фвалуиксистс в 0x00000000, а в противном случае задать \_ для фвалуиксистс значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="a573a-4517">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="a573a-4518">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a573a-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="a573a-4519">Если \_ фвалуиксистс равен 0x00000001, сервер должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a573a-4519">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="a573a-4520">Сериализует значение свойства в структуру СЕРИАЛИЗЕДПРОПЕРТИВАЛУЕ и копирует, начиная с \_ смещения кбсофар, \_ не более кбчунк байт (но не после конца сериализованного свойства) в поле управляемое vValue.</span><span class="sxs-lookup"><span data-stu-id="a573a-4520">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="a573a-4521">Если этот шаг завершается неудачей по каким либо причинам, сервер должен сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a573a-4521">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="a573a-4522">Задайте \_ для кбвалуе число байтов, скопированных на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="a573a-4522">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="a573a-4523">Задайте для Втипе тип свойства значения свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-4523">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="a573a-4524">Если длина сериализованного свойства больше \_ кбсофар, добавленного в \_ кбвалуе, задайте \_ для фмориксистс значение 0x00000001, в противном случае задайте для него значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4524">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="a573a-4525">Ответ на клиент с помощью сообщения Кпмфетчвалуеаут</span><span class="sxs-lookup"><span data-stu-id="a573a-4525">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="a573a-4526">3.1.5.2.9 получение запроса Кпмжетнотифи</span><span class="sxs-lookup"><span data-stu-id="a573a-4526">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="a573a-4527">Когда сервер получает сообщение Кпмжетнотифи от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4527">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4528">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4528">Check if the client has query associated with it.</span></span> <span data-ttu-id="a573a-4529">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4529">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4530">Если в результирующем наборе запроса не было изменений с момента последнего сообщения Кпмсенднотифйоут для этого клиента или если запрос в настоящий момент не отслеживает изменения в результирующем наборе, сервер должен ответить с сообщением Кпмжетнотифи и начать отслеживать запрос на изменения в наборе результатов.</span><span class="sxs-lookup"><span data-stu-id="a573a-4530">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="a573a-4531">Если позднее в наборе результатов запроса произошло изменение, сервер должен отправить клиенту ровно одно сообщение Кпмсенднотифйоут и указать изменение в \_ поле ватчнотифи.</span><span class="sxs-lookup"><span data-stu-id="a573a-4531">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="a573a-4532">Если с момента последнего сообщения Кпмсенднотифйоут в результирующий набор запроса были внесены изменения, сервер должен ответить на Кпмсенднотифйоут и указать изменение в \_ поле ватчнотифи.</span><span class="sxs-lookup"><span data-stu-id="a573a-4532">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="a573a-4533">Обратите внимание, что в случае большого количества изменений в результатах запроса ДБВАТЧНОТИФИ \_ ровсчанжед имеет приоритет (т. е. Если запрос выполнен, повторное выполнение, а затем число измененных строк и запрос был выполнен повторно, то событие, о котором было отправлено, было бы дбватчнотифи \_ ровсчанжед).</span><span class="sxs-lookup"><span data-stu-id="a573a-4533">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="a573a-4534">3.1.5.2.10 получение запроса Кпмжетаппроксиматепоситионин</span><span class="sxs-lookup"><span data-stu-id="a573a-4534">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="a573a-4535">Когда сервер получает запрос сообщения Кпмжетаппроксиматепоситионин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4535">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4536">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4536">Check if the client has a query associated with it.</span></span> <span data-ttu-id="a573a-4537">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4537">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4538">Проверьте, находятся ли в соответствующих списках маркер курсора, маркер раздела и маркер закладки.</span><span class="sxs-lookup"><span data-stu-id="a573a-4538">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="a573a-4539">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="a573a-4539">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="a573a-4540">Найти строку, связанную с маркером закладки в результатах запроса и приблизительной позицией строки в наборе строк, на которую ссылается маркер главы, и определить числитель и знаменатель для этой должности.</span><span class="sxs-lookup"><span data-stu-id="a573a-4540">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="a573a-4541">Обратите внимание, что если маркер главы имеет \_ значение DB NULL \_ параметру hChapter, то соответствующая глава является основным набором строк запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-4541">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="a573a-4542">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a573a-4542">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="a573a-4543">Ответ на клиент с помощью сообщения Кпмфетчвалуеаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4543">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="a573a-4544">3.1.5.2.11 получение запроса Кпмкомпаребмкин</span><span class="sxs-lookup"><span data-stu-id="a573a-4544">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="a573a-4545">Когда сервер получает запрос сообщения Кпмкомпаребмкин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4545">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4546">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4546">Check if the client has a query associated with it.</span></span> <span data-ttu-id="a573a-4547">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4547">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4548">Проверьте, находятся ли в соответствующих списках дескриптор курсора, дескрипторы разделов и маркеры закладок.</span><span class="sxs-lookup"><span data-stu-id="a573a-4548">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="a573a-4549">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="a573a-4549">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="a573a-4550">Подготовка сообщения Кпмкомпаребмкаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4550">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="a573a-4551">Если маркеры закладки равны, \_ ДВКОМПАРИСОН должен иметь значение дбкомпаре \_ EQ.</span><span class="sxs-lookup"><span data-stu-id="a573a-4551">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="a573a-4552">В противном случае, если один из дескрипторов закладок является ДББМК \_ первым или дббмк \_ последним, \_ двкомпарисон должен иметь значение дбкомпаре \_ Ne.</span><span class="sxs-lookup"><span data-stu-id="a573a-4552">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="a573a-4553">В противном случае сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4553">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="a573a-4554">Поиск строк, на которые ссылается каждый маркер закладки в результатах запроса</span><span class="sxs-lookup"><span data-stu-id="a573a-4554">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="a573a-4555">Если какая-либо из строк не входит в главу, обозначенную маркером главы в Кпмкомпаребмкин, \_ для ДВКОМПАРИСОН необходимо задать значение дбкомпаре \_ ноткомпарабле.</span><span class="sxs-lookup"><span data-stu-id="a573a-4555">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="a573a-4556">В противном случае, если обе строки находятся в одной и той же главе, сервер должен приблизительно соответствовать положению этих строк в наборе строк, на который ссылается этот маркер главы.</span><span class="sxs-lookup"><span data-stu-id="a573a-4556">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="a573a-4557">Затем он должен сравнить значения позиций и установить \_ для двкомпарисон значение дбкомпаре \_ lt, если значение первой строки меньше, чем у второй строки. в противном случае \_ двкомпарисон должно быть установлено в дбкомпаре \_ gt.</span><span class="sxs-lookup"><span data-stu-id="a573a-4557">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="a573a-4558">Ответ на клиент с заполненным сообщением Кпмкомпаребмкаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4558">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="a573a-4559">3.1.5.2.12 получение запроса Кпмрестартпоситионин</span><span class="sxs-lookup"><span data-stu-id="a573a-4559">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="a573a-4560">Когда сервер получает запрос сообщения Кпмрестартпоситионин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4560">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4561">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4561">Check if the client has a query associated with it.</span></span> <span data-ttu-id="a573a-4562">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4562">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4563">Проверьте, пройдены ли в соответствующих списках маркер курсора и маркер раздела.</span><span class="sxs-lookup"><span data-stu-id="a573a-4563">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="a573a-4564">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="a573a-4564">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="a573a-4565">Переместить курсор в начало главы, определяемое маркером главы.</span><span class="sxs-lookup"><span data-stu-id="a573a-4565">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="a573a-4566">Обратите внимание, что если маркер главы имеет \_ значение DB NULL \_ параметру hChapter, то соответствующая глава является основным набором строк запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-4566">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="a573a-4567">Если по какой бы то ни было причине выполнить этот шаг не удается, сервер должен сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a573a-4567">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="a573a-4568">Ответ на клиент с помощью сообщения Кпмрестартпоситионин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4568">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="a573a-4569">3.1.5.2.13 получение запроса Кпмфрикурсорин</span><span class="sxs-lookup"><span data-stu-id="a573a-4569">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="a573a-4570">Когда сервер получает запрос сообщения Кпмфрикурсорин от клиента, сервер должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a573a-4570">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4571">Проверьте, связан ли с клиентом запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4571">Check if the client has a query associated with it.</span></span> <span data-ttu-id="a573a-4572">Если это не так, сервер должен сообщить \_ \_ об ошибке Status (недопустимый параметр) (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="a573a-4572">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="a573a-4573">Проверьте, находится ли переданный дескриптор курсора в списке дескрипторов курсора клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-4573">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="a573a-4574">Если это не так, сервер должен сообщить \_ об ошибке E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="a573a-4574">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="a573a-4575">Отпустите курсор и связанные ресурсы (см. раздел 3.1.1 для получения полного списка) для этого маркера курсора.</span><span class="sxs-lookup"><span data-stu-id="a573a-4575">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="a573a-4576">Удалить курсор из списка курсоров для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-4576">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="a573a-4577">Ответьте на сообщение Кпмфрикурсораут, установив в \_ поле ккурсорсремаининг число оставшихся курсоров.</span><span class="sxs-lookup"><span data-stu-id="a573a-4577">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="a573a-4578">в списке этого клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-4578">in this client's list.</span></span>
-   <span data-ttu-id="a573a-4579">Если для этого клиента больше нет курсоров, сервер должен освободить запрос и связанные с ним ресурсы (см. раздел 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="a573a-4579">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="a573a-4580">3.1.5.2.14 получение запроса Кпмдисконнект</span><span class="sxs-lookup"><span data-stu-id="a573a-4580">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="a573a-4581">Когда сервер получает запрос сообщения Кпмдисконнект от клиента, сервер должен удалить клиент из списка подключенных клиентов и освободить все ресурсы, связанные с клиентом.</span><span class="sxs-lookup"><span data-stu-id="a573a-4581">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="a573a-4582">События таймера 3.1.6</span><span class="sxs-lookup"><span data-stu-id="a573a-4582">3.1.6 Timer Events</span></span>

<span data-ttu-id="a573a-4583">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a573a-4583">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="a573a-4584">3.1.7 другие локальные события</span><span class="sxs-lookup"><span data-stu-id="a573a-4584">3.1.7 Other Local Events</span></span>

<span data-ttu-id="a573a-4585">Когда сервер остановлен, он должен сначала перейти в состояние "завершение работы".</span><span class="sxs-lookup"><span data-stu-id="a573a-4585">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="a573a-4586">Затем он должен остановить прослушивание канала, выполнить другие задачи завершения работы, связанные с реализацией, а затем перейти в состояние "остановлено".</span><span class="sxs-lookup"><span data-stu-id="a573a-4586">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="a573a-4587">3,2. сведения о клиенте</span><span class="sxs-lookup"><span data-stu-id="a573a-4587">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="a573a-4588">абстрактная модель данных 3.2.1</span><span class="sxs-lookup"><span data-stu-id="a573a-4588">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="a573a-4589">В следующем разделе указываются данные и состояние, поддерживаемые клиентом протокола службы индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="a573a-4589">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="a573a-4590">Предоставленные данные предназначены для упрощения объяснения того, как работает протокол.</span><span class="sxs-lookup"><span data-stu-id="a573a-4590">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="a573a-4591">Этот раздел не требует, чтобы реализации применялись к этой модели, если их внешнее поведение согласуется с, описанным в этом документе.</span><span class="sxs-lookup"><span data-stu-id="a573a-4591">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="a573a-4592">Клиент имеет следующее абстрактное состояние:</span><span class="sxs-lookup"><span data-stu-id="a573a-4592">A client has the following abstract state:</span></span>

-   <span data-ttu-id="a573a-4593">**Последнее отправленное сообщение**: копия последнего сообщения, отправленного на сервер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4593">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="a573a-4594">**Текущее значение свойства**: частичное значение свойства "отложено", которое находится в процессе извлечения.</span><span class="sxs-lookup"><span data-stu-id="a573a-4594">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="a573a-4595">**Текущее число полученных байтов**: количество байтов, полученных для текущего значения свойства до настоящего времени.</span><span class="sxs-lookup"><span data-stu-id="a573a-4595">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="a573a-4596">**Состояние подключения именованного канала**: соединение с сервером.</span><span class="sxs-lookup"><span data-stu-id="a573a-4596">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="a573a-4597">таймеры 3.2.2</span><span class="sxs-lookup"><span data-stu-id="a573a-4597">3.2.2 Timers</span></span>

<span data-ttu-id="a573a-4598">Таймеры протокола не требуются.</span><span class="sxs-lookup"><span data-stu-id="a573a-4598">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="a573a-4599">Инициализация 3.2.3</span><span class="sxs-lookup"><span data-stu-id="a573a-4599">3.2.3 Initialization</span></span>

<span data-ttu-id="a573a-4600">Никакие действия не выполняются до получения запроса на более высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="a573a-4600">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="a573a-4601">3.2.4 события, активируемые Higher-Layer</span><span class="sxs-lookup"><span data-stu-id="a573a-4601">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="a573a-4602">При получении запроса от более высокого уровня клиент должен создать соединение именованного канала с сервером, используя сведения, указанные в разделе 2,1.</span><span class="sxs-lookup"><span data-stu-id="a573a-4602">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="a573a-4603">Если это невозможно, запрос более высокого уровня должен быть неудачным.</span><span class="sxs-lookup"><span data-stu-id="a573a-4603">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="a573a-4604">Это значит, что в случае сбоя подключения следует повторить попытку, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="a573a-4604">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="a573a-4605">Заголовок должен быть предварительно заполнен полями, заданными в разделе 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="a573a-4605">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="a573a-4606">Для сообщений, которые задаются как запрашивающие ненулевую контрольную сумму, \_ значение УЛЧЕККСУМ должно быть вычислено следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4606">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="a573a-4607">Содержимое сообщения после \_ поля ulReserved2 в заголовке сообщения должно интерпретироваться как последовательность из 32 битовых целых чисел.</span><span class="sxs-lookup"><span data-stu-id="a573a-4607">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="a573a-4608">Клиент должен вычислить сумму числовых значений, заданных этими целыми числами.</span><span class="sxs-lookup"><span data-stu-id="a573a-4608">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="a573a-4609">Вычислите побитовое ИСКЛЮЧАЮЩее это значение с помощью 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="a573a-4609">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="a573a-4610">Вычтите значение, заданное в \_ MSG, из значения, полученного в результате побитового исключающего XOR.</span><span class="sxs-lookup"><span data-stu-id="a573a-4610">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="a573a-4611">Управление каталогом службы удаленного индексирования 3.2.4.1</span><span class="sxs-lookup"><span data-stu-id="a573a-4611">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="a573a-4612">Каждое сообщение активируется запросом из более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="a573a-4612">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="a573a-4613">Клиент для запросов сообщений CISP для удаленного управления каталогами не обеспечивает выполнение последовательности сообщений, но (за исключением сообщения Кпмсеткатстатеин) сервер будет отвечать только после успешного выполнения, если клиент ранее подключился с помощью сообщения Кпмконнектин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4613">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="a573a-4614">3.2.4.1.1 Отправка запроса КпмЦистатеинаут</span><span class="sxs-lookup"><span data-stu-id="a573a-4614">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="a573a-4615">Как правило, более высокий уровень требует, чтобы клиент протокола отправлял сообщение КпмЦистатеинаут, когда ему требуются сведения о службах индексирования на сервере.</span><span class="sxs-lookup"><span data-stu-id="a573a-4615">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="a573a-4616">При запросе на отправку этого сообщения клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a573a-4616">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4617">Отправка сообщения КпмЦистатеинаут, как указано в разделе 2.2.3.1 на сервер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4617">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="a573a-4618">Ожидание получения от сервера сообщения КпмЦистатеинаут без автоматической отмены всех остальных сообщений.</span><span class="sxs-lookup"><span data-stu-id="a573a-4618">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="a573a-4619">Сообщает значение \_ поля Status в ответе и, если оно прошло успешно, информационная структура возвращается к более высокому слою.</span><span class="sxs-lookup"><span data-stu-id="a573a-4619">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="a573a-4620">3.2.4.1.2 Отправка запроса Кпмсеткатстатеин</span><span class="sxs-lookup"><span data-stu-id="a573a-4620">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="a573a-4621">Как правило, более высокий уровень требует, чтобы клиент протокола отправлял сообщение Кпмсеткатстатеин, когда ему требуются сведения о каталоге или каталоге.</span><span class="sxs-lookup"><span data-stu-id="a573a-4621">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="a573a-4622">Для этого сообщения более высокий уровень должен предоставить клиенту протокола значение для \_ двневстате и, при необходимости, имя каталога.</span><span class="sxs-lookup"><span data-stu-id="a573a-4622">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="a573a-4623">При запросе на отправку этого сообщения клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a573a-4623">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4624">Отправка сообщения Кпмсеткатстатеин, указанного в 2.2.3.2, на сервер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4624">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="a573a-4625">Ожидание получения от сервера сообщения Кпмсеткатстатеаут без автоматической отмены всех остальных сообщений.</span><span class="sxs-lookup"><span data-stu-id="a573a-4625">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="a573a-4626">Сообщает значение \_ поля Status в ответе и, если оно прошло успешно, \_ дволдстате обратно на более высокий уровень.</span><span class="sxs-lookup"><span data-stu-id="a573a-4626">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="a573a-4627">3.2.4.1.3 отправка запроса Кпмупдатедокументсин</span><span class="sxs-lookup"><span data-stu-id="a573a-4627">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="a573a-4628">Более высокий уровень обычно запрашивает отправку этого сообщения, когда необходимо либо обновить документы в существующем пути, либо добавить новый путь к этому индексу.</span><span class="sxs-lookup"><span data-stu-id="a573a-4628">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="a573a-4629">Таким образом, более высокий уровень заключается в предоставлении пути и типа сканирования, указанного в разделе 2.2.3.4, где для существующих путей предназначено добавочное или полное обновление, а новая инициализация предназначена для новых путей.</span><span class="sxs-lookup"><span data-stu-id="a573a-4629">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="a573a-4630">Чтобы обслуживать запрос более высокого уровня, клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a573a-4630">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4631">Отправка сообщения Кпмупдатедокументсин, как указано в разделе 2.2.3.4 на сервер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4631">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="a573a-4632">Ожидание получения сообщения Кпмупдатедокументсин с сервера без автоматической отмены всех остальных сообщений.</span><span class="sxs-lookup"><span data-stu-id="a573a-4632">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="a573a-4633">Сообщает значение \_ поля Status в ответе назад к более высокому слою.</span><span class="sxs-lookup"><span data-stu-id="a573a-4633">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="a573a-4634">3.2.4.1.4 Отправка запроса Кпмфорцемержеин</span><span class="sxs-lookup"><span data-stu-id="a573a-4634">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="a573a-4635">Как правило, более высокий уровень запрашивает отправку этого сообщения при необходимости улучшить производительность запросов или является частью запланированного обслуживания службы индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-4635">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="a573a-4636">Чтобы обслуживать более высокий уровень, клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a573a-4636">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4637">Отправка сообщения Кпмфорцемержеин, указанного в разделе 2.2.3.5, на сервер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4637">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="a573a-4638">Ожидание получения сообщения Кпмупдатедокументсин с сервера без автоматической отмены всех остальных сообщений.</span><span class="sxs-lookup"><span data-stu-id="a573a-4638">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="a573a-4639">Сообщает значение \_ поля Status в ответе назад к более высокому слою.</span><span class="sxs-lookup"><span data-stu-id="a573a-4639">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="a573a-4640">Сообщения о запросе каталога службы удаленного индексирования 3.2.4.2</span><span class="sxs-lookup"><span data-stu-id="a573a-4640">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="a573a-4641">За исключением Кпмжетровсин/Кпмжетровсаут, Кпмфетчвалуеин/Кпмфетчвалуеаут существует связь "один к одному" между CISP сообщениями и запросами более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="a573a-4641">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="a573a-4642">Для двух упомянутых выше исключений может существовать несколько сообщений, создаваемых клиентом для удовлетворения требований к размеру или получения полного свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-4642">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="a573a-4643">Более высокий уровень обычно отслеживает все сведения, относящиеся к запросам (например, открытые дескрипторы курсоров, допустимые значения для дескрипторов закладок и разделов, значения WID для отложенных значений свойств и т. д.), а также отслеживает, если клиент находится в подключенном состоянии, но он не применяется каким-либо образом клиентом.</span><span class="sxs-lookup"><span data-stu-id="a573a-4643">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="a573a-4644">В наглядной части схемы в разделе 3 показана эта последовательность для простого запроса службы индексирования.</span><span class="sxs-lookup"><span data-stu-id="a573a-4644">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="a573a-4645">3.2.4.2.1 Отправка запроса Кпмконнектин</span><span class="sxs-lookup"><span data-stu-id="a573a-4645">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="a573a-4646">Это сообщение обычно является первым запросом от более высокого уровня (как если бы клиент не был подключен, сервер будет завершать свою часть сообщений с исключением Кпмсеткатстатеин).</span><span class="sxs-lookup"><span data-stu-id="a573a-4646">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="a573a-4647">Более высокий уровень предоставляет клиенту протокола сведения, необходимые для подключения.</span><span class="sxs-lookup"><span data-stu-id="a573a-4647">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="a573a-4648">Чтобы обслуживать более высокий уровень, клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a573a-4648">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4649">Заполните сообщение, используя сведения, предоставленные клиентом более высокого уровня (см. раздел 2.2.3.6) в \_ иклиентверсион, MachineName, username, PropertySet1, PropertySet2 и апропертисет.</span><span class="sxs-lookup"><span data-stu-id="a573a-4649">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="a573a-4650">Задайте \_ фклиентисремоте, \_ кбблоб, \_ cbBlob2, кпропсет и цекстпропсет, как указано в 2.2.3.6.</span><span class="sxs-lookup"><span data-stu-id="a573a-4650">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="a573a-4651">Задайте контрольную сумму в \_ поле улчекксум.</span><span class="sxs-lookup"><span data-stu-id="a573a-4651">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="a573a-4652">Отправка сообщения Кпмконнектин на сервер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4652">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="a573a-4653">Ожидание получения сообщения Кпмконнектаут с сервера без автоматической отмены всех остальных сообщений.</span><span class="sxs-lookup"><span data-stu-id="a573a-4653">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="a573a-4654">Сообщает значение \_ поля Status в ответе и, если оно прошло успешно, \_ serverVersion обратно на более высокий уровень.</span><span class="sxs-lookup"><span data-stu-id="a573a-4654">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="a573a-4655">В информативных целях ожидается, что при успешном подключении более высокие уровни обычно выполняют следующие действия, но не применяются клиентом CISP.</span><span class="sxs-lookup"><span data-stu-id="a573a-4655">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="a573a-4656">Использование сообщений об управлении каталогом службы удаленного индексирования для административных задач</span><span class="sxs-lookup"><span data-stu-id="a573a-4656">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="a573a-4657">Используйте запрос Кпмкреатекуерин, чтобы создать поисковый запрос с целью получения результатов из каталога.</span><span class="sxs-lookup"><span data-stu-id="a573a-4657">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="a573a-4658">3.2.4.2.2 Отправка запроса Кпмкреатекуерин</span><span class="sxs-lookup"><span data-stu-id="a573a-4658">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="a573a-4659">Более высокий уровень, как правило, предоставляет сведения о создании запроса после подключения клиента протокола.</span><span class="sxs-lookup"><span data-stu-id="a573a-4659">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="a573a-4660">Более высокий уровень предоставляет клиенту набор ограничений, набор столбцов, правила порядка сортировки и набор классификации (каждый из них можно опустить), свойства набора строк и структуру сопоставления ИДЕНТИФИКАТОРов свойств.</span><span class="sxs-lookup"><span data-stu-id="a573a-4660">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="a573a-4661">При получении этого запроса от более высокого уровня клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a573a-4661">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4662">Подготовьте Кпмкреатекуерйоут, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="a573a-4662">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="a573a-4663">Если задан набор столбцов, установите для Кколумнссетпресет значение 0x01 и заполните поле Columning.</span><span class="sxs-lookup"><span data-stu-id="a573a-4663">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="a573a-4664">Если имеются ограничения, задайте для Крестриктионпресент значение 0x01 и заполните поле ограничения.</span><span class="sxs-lookup"><span data-stu-id="a573a-4664">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="a573a-4665">Если указан набор сортировки, заполните поле Sorting.</span><span class="sxs-lookup"><span data-stu-id="a573a-4665">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="a573a-4666">Если задан набор классификаций, задайте для Ксортсетпресент значение 0x01 и заполните поле Категоризатионсет.</span><span class="sxs-lookup"><span data-stu-id="a573a-4666">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="a573a-4667">Установите остальные поля, как указано в 2.2.3.8.</span><span class="sxs-lookup"><span data-stu-id="a573a-4667">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="a573a-4668">Вычислите \_ поле улчекксум в заголовке.</span><span class="sxs-lookup"><span data-stu-id="a573a-4668">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="a573a-4669">Отправка сообщения Кпмкреатекуерин на сервер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4669">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="a573a-4670">Дождитесь получения сообщения Кпмкреатекуерйоут (см. сведения в разделе 3.2.5.1.1) без автоматического удаления всех остальных сообщений.</span><span class="sxs-lookup"><span data-stu-id="a573a-4670">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="a573a-4671">Сообщает значение \_ поля Status в ответе и, если оно прошло успешно, массив дескрипторов курсоров и информативные логические значения (как указано в 2.2.3.9) возвращаются к более высокому слою.</span><span class="sxs-lookup"><span data-stu-id="a573a-4671">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="a573a-4672">3.2.4.2.3 отправка запроса Кпмсетбиндингсин</span><span class="sxs-lookup"><span data-stu-id="a573a-4672">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="a573a-4673">Как правило, более высокий уровень задает привязки для каждого столбца, возвращаемого в строках, если он уже имеет допустимый маркер курсора (после успешного получения Кпмкреатекуерйоут см. раздел 3.2.5.1.1).</span><span class="sxs-lookup"><span data-stu-id="a573a-4673">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="a573a-4674">Выше ожидается, что необходимо предоставить массив структур Ктаблеколумн, как указано в разделе 2.2.4.31, для поля Аколумнс и допустимого маркера курсора.</span><span class="sxs-lookup"><span data-stu-id="a573a-4674">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="a573a-4675">При получении этого запроса от более высокого уровня клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a573a-4675">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4676">Вычислите количество структур Ктаблеколумн в массиве Аколумнс и задайте для поля Кколумнс это значение.</span><span class="sxs-lookup"><span data-stu-id="a573a-4676">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="a573a-4677">Вычислите общий размер в байтах для полей Кколумнс и Аколумнс и задайте \_ для поля кббиндингдеск это значение.</span><span class="sxs-lookup"><span data-stu-id="a573a-4677">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="a573a-4678">Задавайте указанные поля в сообщении Кпмсетбиндингсин значениям, предоставленным более высоким уровнем приложения.</span><span class="sxs-lookup"><span data-stu-id="a573a-4678">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="a573a-4679">Задайте в \_ поле улчекксум значение, вычисленное, как указано в разделе 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="a573a-4679">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="a573a-4680">Отправка завершенного сообщения Кпмсетбиндигнсин на сервер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4680">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="a573a-4681">Ожидание получения сообщения Кпмсетбиндингсин от сервера, удаление других сообщений.</span><span class="sxs-lookup"><span data-stu-id="a573a-4681">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="a573a-4682">Укажите состояние из \_ поля состояние ответа на более высокий уровень.</span><span class="sxs-lookup"><span data-stu-id="a573a-4682">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="a573a-4683">Для информативных целей ожидается, что более высокие уровни обычно запрашивают у клиента сообщение Кпмжетровсин, но это не обеспечивается протоколом службы индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="a573a-4683">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="a573a-4684">3.2.4.2.4 Отправка запроса Кпмжетровсин</span><span class="sxs-lookup"><span data-stu-id="a573a-4684">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="a573a-4685">Когда более высокий уровень собирается получить сведения о строках, он предоставит клиенту протокола допустимый маркер курсора и раздела и предложит соответствующее описание поиска.</span><span class="sxs-lookup"><span data-stu-id="a573a-4685">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="a573a-4686">Как правило, ожидается более высокий уровень, если у него есть допустимый обработчик курсора или раздела, а привязки были заданы с помощью сообщения Кпмсетбиндингсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4686">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="a573a-4687">Чтобы получить доступ к набору строк в главе, более высокий уровень заключается в использовании маркера раздела, полученного от сервера, в предыдущем Кпмжетровсаут сообщении.</span><span class="sxs-lookup"><span data-stu-id="a573a-4687">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="a573a-4688">При получении этого запроса от более высокого уровня клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a573a-4688">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4689">Определите, какое целочисленное значение без знака следует указать для \_ поля кбреадбуффер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4689">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="a573a-4690">Чтобы определить это значение, клиент должен получить максимальное значение из следующего:</span><span class="sxs-lookup"><span data-stu-id="a573a-4690">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="a573a-4691">1000. время в значении \_ поля c ровстотрансфер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4691">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="a573a-4692">Значение \_ кброввидс, округленное до ближайшего 512 байта с множителем.</span><span class="sxs-lookup"><span data-stu-id="a573a-4692">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="a573a-4693">Передавайте большее из этих двух значений, до ограничения 16 КБ.</span><span class="sxs-lookup"><span data-stu-id="a573a-4693">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="a573a-4694">В случаях, когда размер одной строки превышает 16 КБ, сервер не может вернуть результаты в этот запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4694">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="a573a-4695">Укажите клиентскую базу для данных строк переменного размера в адресном пространстве клиента в \_ поле улклиентбасе.</span><span class="sxs-lookup"><span data-stu-id="a573a-4695">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="a573a-4696">*Поведение Windows. для 32-разрядного клиента, говорящего на 32-разрядном сервере, или клиента 64 bit, говорящего на 64-bit Server, этому параметру присваивается адрес в памяти принимающего буфера в процессе приложения. Это позволяет указателям, полученным в поле строк Кпмжетровсаут, быть правильными указателями памяти в процессе клиентского приложения. В противном случае — значение 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="a573a-4696">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="a573a-4697">Вычислите размер описания поиска и задайте его в \_ поле кбсик.</span><span class="sxs-lookup"><span data-stu-id="a573a-4697">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="a573a-4698">Установите значение Кбресервед (которое будет действовать как смещение для начала строк) на значение \_ кбсик плюс 0x14.</span><span class="sxs-lookup"><span data-stu-id="a573a-4698">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="a573a-4699">Отправка сообщения Кпмконнектин, указанного в 2.2.3.15, на сервер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4699">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="a573a-4700">3.2.4.2.5 Отправка запроса Кпмфетчвалуеин</span><span class="sxs-lookup"><span data-stu-id="a573a-4700">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="a573a-4701">Если клиент получает от сервера ответ Кпмжетровсаут с полем состояния столбца, установленным в значение Статусдеферред (0x01), это означает, что значение свойства не было указано в поле Rows сообщения Кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4701">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="a573a-4702">В этом случае более высокий уровень обычно запрашивает у клиента протокола получение значения с помощью сообщения Кпмфетчвалуеин, а также предоставляет значение Пропспек и \_ WID для отложенного свойства, которое клиент протокола должен использовать в первом сообщении кпмфетчвалуеин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4702">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="a573a-4703">Если это первое сообщение Кпмфетчвалуеин, отправленное клиентом для запроса указанного свойства, клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a573a-4703">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4704">Установите все поля в сообщении, как указано в разделе 2.2.3.19.</span><span class="sxs-lookup"><span data-stu-id="a573a-4704">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="a573a-4705">Задайте \_ для кбсофар значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4705">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="a573a-4706">Установка текущих байтов, полученных в значение 0.</span><span class="sxs-lookup"><span data-stu-id="a573a-4706">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="a573a-4707">Отправка сообщения Кпмфетчвалуеин на сервер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4707">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="a573a-4708">3.2.4.2.6 Отправка запроса Кпмфрикурсорин</span><span class="sxs-lookup"><span data-stu-id="a573a-4708">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="a573a-4709">Когда более высокий уровень больше не использует поисковый запрос, он может освободить ресурсы на сервере, запросив клиента отправить сообщение Кпмфрикурсорин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4709">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="a573a-4710">При получении этого запроса клиент должен отправить сообщение Кпмфрикурсорин, как указано в 2.2.3.28, на сервер, содержащий маркер, заданный верхним слоем.</span><span class="sxs-lookup"><span data-stu-id="a573a-4710">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="a573a-4711">3.2.4.2.7 Отправка сообщения Кпмдисконнект</span><span class="sxs-lookup"><span data-stu-id="a573a-4711">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="a573a-4712">Если более высокий уровень не содержит запросов для службы индексирования, чтобы освободить больше ресурсов сервера, приложение может запросить отправку клиентом сообщения Кпмдисконнект на сервер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4712">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="a573a-4713">При получении этого запроса клиент должен просто отправить сообщение по запросу.</span><span class="sxs-lookup"><span data-stu-id="a573a-4713">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="a573a-4714">Нет ответа на это сообщение от сервера.</span><span class="sxs-lookup"><span data-stu-id="a573a-4714">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="a573a-4715">Правила обработки сообщений 3.2.5 и последовательности</span><span class="sxs-lookup"><span data-stu-id="a573a-4715">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="a573a-4716">Когда клиент получает ответ на сообщение от сервера, клиент должен использовать Последнее отправленное сообщение, чтобы определить, является ли сообщение, полученное от сервера, ожидаемым клиентом.</span><span class="sxs-lookup"><span data-stu-id="a573a-4716">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="a573a-4717">Все сообщения с \_ полем MSG, отличным от одного сообщения в последней отправке, должны игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a573a-4717">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="a573a-4718">3.2.5.1 получение ответа Кпмкреатекуерйоут</span><span class="sxs-lookup"><span data-stu-id="a573a-4718">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="a573a-4719">Когда клиент получает от сервера ответ на сообщение Кпмкреатекуерйоут, клиент должен возвратить \_ состояние и (если состояние прошло успешно) значения маркера курсора возвращаются к более высокому слою.</span><span class="sxs-lookup"><span data-stu-id="a573a-4719">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="a573a-4720">Дальнейшие действия выполняются на более высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="a573a-4720">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="a573a-4721">Так как более высокий уровень имеет значение для структуры запроса, он всегда будет рассчитывать правильное число дескрипторов курсора, возвращаемых в сообщении Кпмкреатеауерйоут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4721">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="a573a-4722">Дескрипторы курсора возвращаются в следующем порядке: первый дескриптор относится к набору строк, к которому применяется unchapter, второй — к первому разбитому на разделы набору строк (т. е. Группирование результатов на основе первой категории, указанной в поле Категоризатионсет сообщения Кпмкреатекуерин).</span><span class="sxs-lookup"><span data-stu-id="a573a-4722">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="a573a-4723">Для информативных целей ожидается, что более высокие уровни могут выполнять следующие действия, но они не применяются клиентом CISP.</span><span class="sxs-lookup"><span data-stu-id="a573a-4723">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="a573a-4724">Использование Кпмсетбиндингсин для установки привязок для отдельных столбцов и выполнения последующих действий по пути запроса</span><span class="sxs-lookup"><span data-stu-id="a573a-4724">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="a573a-4725">Используйте Кпмжеткуеристатусин для проверки хода выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-4725">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="a573a-4726">Используйте Кпмратиофинишедин, чтобы запросить процент завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-4726">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="a573a-4727">3.2.5.2 получение ответа Кпмжетровсаут</span><span class="sxs-lookup"><span data-stu-id="a573a-4727">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="a573a-4728">Когда клиент получает от сервера ответ на сообщение Кпмжетровсаут, клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a573a-4728">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4729">Убедитесь, что \_ поле состояния в заголовке указывает на успешное выполнение или сбой.</span><span class="sxs-lookup"><span data-stu-id="a573a-4729">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="a573a-4730">Если \_ значение состояния "БУФЕР состояния \_ \_ слишком мало" \_ (0XC0000023), клиент должен проверить состояние последнего отправленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="a573a-4730">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="a573a-4731">Если он не содержит сообщение Кпмжетровсин, то полученное сообщение должно игнорироваться без уведомления.</span><span class="sxs-lookup"><span data-stu-id="a573a-4731">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="a573a-4732">В противном случае клиент должен отправить на сервер новое сообщение Кпмжетровсин со всеми полями, идентичными сохраненному, за исключением того, что \_ КБРЕАДБУФФЕР должен быть увеличен на 512 (но не больше, чем 0x4000).</span><span class="sxs-lookup"><span data-stu-id="a573a-4732">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="a573a-4733">Если \_ состояние \_ "буфер состояния \_ слишком \_ мал" (0XC0000023), а Последнее отправленное сообщение уже имеет \_ кбреадбуффер, равное 0x4000 Client, должен сообщить об ошибке до более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="a573a-4733">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="a573a-4734">Если \_ значением состояния является любое другое значение ошибки, клиент должен указать на сбой до более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="a573a-4734">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="a573a-4735">Если \_ значение состояния указывает на успешное выполнение, результаты должны указывать на более высокий уровень, запрашивающий информацию, а дальнейшие действия — на более высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="a573a-4735">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="a573a-4736">В информативных целях предполагается, что более высокие уровни обычно выполняют следующие действия, но не применяются клиентом протокола службы индексирования содержимого:</span><span class="sxs-lookup"><span data-stu-id="a573a-4736">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="a573a-4737">Если значения в строках представляют идентификаторы документов, главы или закладки обрабатывают более высокий уровень, обычно они сохраняются для использования в последующих операциях, в которых задействованы допустимые идентификаторы документов, разделы или маркеры закладок.</span><span class="sxs-lookup"><span data-stu-id="a573a-4737">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="a573a-4738">Более высокий уровень обычно сохраняет или отображает данные из значений строк или иным образом использует их.</span><span class="sxs-lookup"><span data-stu-id="a573a-4738">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="a573a-4739">Для значений, которые были помечены как отложенные выше, будут получены значения с помощью сообщений Кпмфетчвалуеин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4739">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="a573a-4740">Описание поиска возвращается к более высокому слою и может быть повторно использовано или проверено более высоким уровнем.</span><span class="sxs-lookup"><span data-stu-id="a573a-4740">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="a573a-4741">В информативных целях, если более высокий уровень запросил обработку глав и закладок, полученных в строках, это может сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="a573a-4741">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="a573a-4742">Используйте Кпмжеткуеристатусексин, чтобы проверить ход выполнения запроса, а также дополнительные сведения о состоянии, например число отфильтрованных документов, документов, которые нужно отфильтровать, отношение документов, обрабатываемых запросом, общее число строк в запросе и расположение закладки в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-4742">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="a573a-4743">Используйте Кпмжетнотифи, чтобы запросить у сервера уведомление клиента об изменениях набора строк.</span><span class="sxs-lookup"><span data-stu-id="a573a-4743">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="a573a-4744">Используйте Кпмжетаппроксиматепоситионин для запроса приблизительного расположения закладки в главе.</span><span class="sxs-lookup"><span data-stu-id="a573a-4744">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="a573a-4745">Используйте Кпмкомпаребмкин для запроса сравнения двух закладок в главе.</span><span class="sxs-lookup"><span data-stu-id="a573a-4745">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="a573a-4746">Используйте Кпмрестартпоситионин, чтобы изменить положение курсора на начало набора строк на сервере.</span><span class="sxs-lookup"><span data-stu-id="a573a-4746">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="a573a-4747">3.2.5.3 получение ответа Кпмфетчвалуеаут</span><span class="sxs-lookup"><span data-stu-id="a573a-4747">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="a573a-4748">Когда клиент получает от сервера ответ на сообщение Кпмжетровсаут, клиент должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a573a-4748">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="a573a-4749">Убедитесь, что \_ поле состояния в заголовке указывает на успешное выполнение или сбой.</span><span class="sxs-lookup"><span data-stu-id="a573a-4749">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="a573a-4750">В случае сбоя уведомить более высокий уровень.</span><span class="sxs-lookup"><span data-stu-id="a573a-4750">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="a573a-4751">В противном случае продолжайте ниже.</span><span class="sxs-lookup"><span data-stu-id="a573a-4751">Otherwise, continue below.</span></span>
-   <span data-ttu-id="a573a-4752">Проверьте \_ фвалуиксист и, если задано значение 0x00000000 уведомить более высокого уровня о том, что значение не найдено.</span><span class="sxs-lookup"><span data-stu-id="a573a-4752">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="a573a-4753">В противном случае добавьте \_ кбвалуе байт из управляемое vValue в текущее значение свойства.</span><span class="sxs-lookup"><span data-stu-id="a573a-4753">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="a573a-4754">Если \_ \_ фмориксистс имеет значение 0x00000001, то Увеличьте \_ текущие байты, полученные \_ кбвалуе, и отправьте сообщение кпмфетчвалуеин на сервер, установив \_ для Кбсофар значение Current bytes Received, \_ кбпропспек to Zero и \_ кбчунк до размера буфера, который требуется более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="a573a-4754">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="a573a-4755">Если \_ фмориксистс имеет значение 0x00000000, укажите значение свойства из текущего значения свойства в более высокий уровень.</span><span class="sxs-lookup"><span data-stu-id="a573a-4755">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="a573a-4756">3.2.5.4 получение ответа Кпмфрикурсораут</span><span class="sxs-lookup"><span data-stu-id="a573a-4756">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="a573a-4757">Когда клиент получает успешный ответ на сообщение Кпмфрикурсораут от сервера, клиент должен вернуть \_ значение ккурсорсремаининг к более высокому слою.</span><span class="sxs-lookup"><span data-stu-id="a573a-4757">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="a573a-4758">Следующие сведения предоставляются только в информативных целях и не применяются клиентом CISP.</span><span class="sxs-lookup"><span data-stu-id="a573a-4758">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="a573a-4759">Предполагается, что более высокий уровень отслеживает дескрипторы курсора и не использует уже освобожденные объекты.</span><span class="sxs-lookup"><span data-stu-id="a573a-4759">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="a573a-4760">Когда число \_ ккурсорсремаининг равно 0x00000000, более высокий уровень может использовать соединение для указания другого запроса (с помощью сообщения кпмкреатекуерин).</span><span class="sxs-lookup"><span data-stu-id="a573a-4760">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="a573a-4761">События таймера 3.2.6</span><span class="sxs-lookup"><span data-stu-id="a573a-4761">3.2.6 Timer Events</span></span>

<span data-ttu-id="a573a-4762">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a573a-4762">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="a573a-4763">3.2.7 другие локальные события</span><span class="sxs-lookup"><span data-stu-id="a573a-4763">3.2.7 Other Local Events</span></span>

<span data-ttu-id="a573a-4764">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a573a-4764">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="a573a-4765">4. Примеры протокола</span><span class="sxs-lookup"><span data-stu-id="a573a-4765">4 Protocol Examples</span></span>

-   [<span data-ttu-id="a573a-4766">4,1 Пример 1</span><span class="sxs-lookup"><span data-stu-id="a573a-4766">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="a573a-4767">4,2. Пример 2</span><span class="sxs-lookup"><span data-stu-id="a573a-4767">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="a573a-4768">4,1 Пример 1</span><span class="sxs-lookup"><span data-stu-id="a573a-4768">4.1 Example 1</span></span>

<span data-ttu-id="a573a-4769">В следующем примере мы рассмотрим ситуацию, в которой пользователь Джон на компьютере а хочет получить размеры файлов, содержащих слово «Microsoft», из набора документов, хранящихся на сервере X в системе каталогов.</span><span class="sxs-lookup"><span data-stu-id="a573a-4769">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="a573a-4770">Предположим, что компьютер A работает под управлением 32-разрядной операционной системы Windows XP, а компьютер X работает под управлением 32-разрядной операционной системы Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a573a-4770">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="a573a-4771">Пользователь запускает приложение поиска и вводит поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4771">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="a573a-4772">Приложение, в свою очередь, передает поисковый запрос клиенту протокола.</span><span class="sxs-lookup"><span data-stu-id="a573a-4772">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="a573a-4773">Клиент протокола устанавливает соединение с сервером индексирования X. Клиент протокола использует элемент \\ конфигурации канала именованного \\ канала \_ скадс для подключения к серверу X через SMB.</span><span class="sxs-lookup"><span data-stu-id="a573a-4773">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="a573a-4774">Затем клиент протокола подготавливает сообщение Кпмконнектин со следующими значениями:</span><span class="sxs-lookup"><span data-stu-id="a573a-4774">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="a573a-4775">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4775">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4776">**\_ сообщение имеет значение** 0x000000C8, указывающее, что это сообщение кпмконнектин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4776">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="a573a-4777">для параметра **\_ Status** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4777">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="a573a-4778">**\_ улчекксум** содержит контрольную сумму, вычисленную, как указано в разделе 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="a573a-4778">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="a573a-4779">для **\_ ulReserved2** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4779">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="a573a-4780">Текст сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4780">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4781">**\_ иклиентверсион** имеет значение 0x00000008, указывающее, что сервер должен проверять поле контрольной суммы.</span><span class="sxs-lookup"><span data-stu-id="a573a-4781">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="a573a-4782">**\_ фклиентисремоте** имеет значение 0x00000001, указывающее, что сервер является удаленным сервером.</span><span class="sxs-lookup"><span data-stu-id="a573a-4782">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="a573a-4783">**\_ cbBlob1** задает размер в байтах Объединенных полей кпропсет, PropertySet1 и PropertySet2.</span><span class="sxs-lookup"><span data-stu-id="a573a-4783">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="a573a-4784">для **\_ cbBlob2** задано значение 0x00000004 (это означает отсутствие дополнительных наборов свойств).</span><span class="sxs-lookup"><span data-stu-id="a573a-4784">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="a573a-4785">**MachineName** имеет значение.</span><span class="sxs-lookup"><span data-stu-id="a573a-4785">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="a573a-4786">Параметр **username** имеет значение John.</span><span class="sxs-lookup"><span data-stu-id="a573a-4786">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="a573a-4787">для **кпропсетс** задано значение 0x00000002.</span><span class="sxs-lookup"><span data-stu-id="a573a-4787">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="a573a-4788">Поле **PropertySet1** имеет тип кдбпропсет.</span><span class="sxs-lookup"><span data-stu-id="a573a-4788">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="a573a-4789">Структура Кдбпропсет, состоящая из поля PropertySet1, заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4789">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="a573a-4790">Для поля **гуидпропсет** установлено значение A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ фсЦифрмврк \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="a573a-4790">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="a573a-4791">для поля **кпропертиес** установлено значение 0x00000004.</span><span class="sxs-lookup"><span data-stu-id="a573a-4791">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="a573a-4792">поле **апропс** представляет собой массив структур кдбпроп.</span><span class="sxs-lookup"><span data-stu-id="a573a-4792">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="a573a-4793">Для элемента **апропс \[ 0 \]** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4793">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="a573a-4794">**PropId** имеет значение 0x00000002 ( \_ \_ имя каталога CI DBPROP \_ ).</span><span class="sxs-lookup"><span data-stu-id="a573a-4794">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="a573a-4795">Для **дбпропоптионс** задано значение 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4795">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="a573a-4796">Для **дбпропстатус** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4796">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="a573a-4797">Для элемента **идентификатора столбца** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4797">For the **ColId** element:</span></span>
                -   <span data-ttu-id="a573a-4798">**элемент ekind** имеет значение 0X00000001 (дбкинд \_ GUID \_ PropID)</span><span class="sxs-lookup"><span data-stu-id="a573a-4798">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="a573a-4799">**GUID** имеет значение null (все нули), то есть значение применяется к запросу, а не только к одному столбцу.</span><span class="sxs-lookup"><span data-stu-id="a573a-4799">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="a573a-4800">для **улид** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4800">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="a573a-4801">Для элемента **управляемое vValue** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4801">For the **vValue** element:</span></span>
                -   <span data-ttu-id="a573a-4802">для **втипе** задано значение 0X001F (VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="a573a-4802">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="a573a-4803">для **управляемое vValue** задано значение System, имя нужного каталога.</span><span class="sxs-lookup"><span data-stu-id="a573a-4803">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="a573a-4804">Для элемента **апропс \[ 1 \]** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4804">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="a573a-4805">**PropId** имеет значение 0x00000007 ( \_ \_ тип запроса DBPROP CI \_ )</span><span class="sxs-lookup"><span data-stu-id="a573a-4805">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="a573a-4806">Для **дбпропоптионс** задано значение 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4806">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="a573a-4807">**Дбпропстатус** имеет значение to0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4807">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="a573a-4808">Для элемента **идентификатора столбца** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4808">For the **ColId** element:</span></span>
                -   <span data-ttu-id="a573a-4809">**элемент ekind** имеет значение 0X00000001 (дбкинд \_ GUID \_ PropID).</span><span class="sxs-lookup"><span data-stu-id="a573a-4809">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="a573a-4810">**GUID** имеет значение null (все нули), то есть значение применяется к запросу, а не только к одному столбцу.</span><span class="sxs-lookup"><span data-stu-id="a573a-4810">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="a573a-4811">для **улид** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4811">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="a573a-4812">Для элемента **управляемое vValue** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4812">For the **vValue** element:</span></span>
                -   <span data-ttu-id="a573a-4813">для **втипе** задано значение 0X0003 (VT \_ i4).</span><span class="sxs-lookup"><span data-stu-id="a573a-4813">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="a573a-4814">**управляемое vValue** имеет значение 0X00000000 (Цинормал), то есть это обычный запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4814">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="a573a-4815">Для элемента **апропс \[ 2 \]** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4815">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="a573a-4816">**PropId** имеет значение 0x00000004 ( \_ \_ Флаги области CI DBPROP \_ ).</span><span class="sxs-lookup"><span data-stu-id="a573a-4816">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="a573a-4817">Для **дбпропоптионс** задано значение 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4817">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="a573a-4818">Для **дбпропстатус** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4818">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="a573a-4819">Для элемента **идентификатора столбца** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4819">For the **ColId** element:</span></span>
                -   <span data-ttu-id="a573a-4820">**элемент ekind** имеет значение 0X00000001 (дбкинд \_ GUID \_ PropID).</span><span class="sxs-lookup"><span data-stu-id="a573a-4820">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="a573a-4821">**GUID** имеет значение null (все нули), то есть значение применяется к запросу, а не только к одному столбцу.</span><span class="sxs-lookup"><span data-stu-id="a573a-4821">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="a573a-4822">для **улид** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4822">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="a573a-4823">Для элемента **управляемое vValue** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4823">For the **vValue** element:</span></span>
                -   <span data-ttu-id="a573a-4824">**втипе**: 0x1003 ( \_ вектор \| VT, \_ i4)</span><span class="sxs-lookup"><span data-stu-id="a573a-4824">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="a573a-4825">**управляемое vValue**: 0x00000001/0x00000001 (один элемент со значением 1), то есть Поиск вложенных папок</span><span class="sxs-lookup"><span data-stu-id="a573a-4825">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="a573a-4826">Для элемента **апропс \[ 3 \]** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4826">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="a573a-4827">**PropId**: 0X00000003 (DBPROP \_ CI \_ включает \_ области)</span><span class="sxs-lookup"><span data-stu-id="a573a-4827">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="a573a-4828">**Дбпропоптионс**: 0x0000000</span><span class="sxs-lookup"><span data-stu-id="a573a-4828">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="a573a-4829">**Дбпропстатус**: 0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-4829">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="a573a-4830">Для элемента **идентификатора столбца** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4830">For the **ColId** element:</span></span>
                -   <span data-ttu-id="a573a-4831">**элемент ekind** имеет значение 0X00000001 (дбкинд \_ GUID \_ PropID).</span><span class="sxs-lookup"><span data-stu-id="a573a-4831">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="a573a-4832">**GUID** имеет значение null (все нули), то есть значение применяется к запросу, а не только к одному столбцу.</span><span class="sxs-lookup"><span data-stu-id="a573a-4832">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="a573a-4833">для **улид** задано значение 0x00000000</span><span class="sxs-lookup"><span data-stu-id="a573a-4833">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="a573a-4834">Для элемента **управляемое vValue** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4834">For the **vValue** element:</span></span>
                -   <span data-ttu-id="a573a-4835">для **втипе** задано значение 0x101F (VT \_ vector \| VT \_ ).</span><span class="sxs-lookup"><span data-stu-id="a573a-4835">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="a573a-4836">**управляемое vValue** имеет значение 0x00000001/0x00000002/" \\ " (один элемент с строкой, завершающейся нулевым символом NULL), то есть в корневой области.</span><span class="sxs-lookup"><span data-stu-id="a573a-4836">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="a573a-4837">Поле **PropertySet2** имеет тип кдбпропсет.</span><span class="sxs-lookup"><span data-stu-id="a573a-4837">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="a573a-4838">Структура Кдбпропсет, состоящая из поля PropertySet1, заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4838">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="a573a-4839">Для **гуидпропсет** задано значение AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ Цифрмврккоре \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="a573a-4839">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="a573a-4840">поле **кпропертиес** имеет значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="a573a-4840">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="a573a-4841">Поле **апропс** представляет собой массив структур кдбпроп.</span><span class="sxs-lookup"><span data-stu-id="a573a-4841">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="a573a-4842">Для элемента **апропс \[ 0 \]** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4842">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="a573a-4843">**PropId** имеет значение 0X00000002 (DBPROP \_ Machine).</span><span class="sxs-lookup"><span data-stu-id="a573a-4843">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="a573a-4844">Для **дбпропоптионс** задано значение 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4844">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="a573a-4845">Для **дбпропстатус** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4845">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="a573a-4846">Для элемента **идентификатора столбца** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4846">For the **ColId** element:</span></span>
                -   <span data-ttu-id="a573a-4847">**элемент ekind** имеет значение 0X00000001 (дбкинд \_ GUID \_ PropID),</span><span class="sxs-lookup"><span data-stu-id="a573a-4847">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="a573a-4848">**GUID** имеет значение null (все нули), то есть значение применяется к запросу, а не только к одному столбцу.</span><span class="sxs-lookup"><span data-stu-id="a573a-4848">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="a573a-4849">для **улид** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4849">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="a573a-4850">Для элемента **управляемое vValue** :</span><span class="sxs-lookup"><span data-stu-id="a573a-4850">For **vValue** element:</span></span>
                -   <span data-ttu-id="a573a-4851">**втипе**: 0X0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="a573a-4851">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="a573a-4852">**управляемое vValue**: 0x04/"x" (4 байта/строка в Юникоде, заканчивающаяся нулем), означающее "X" — имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a573a-4852">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="a573a-4853">для поля **цекстпропсет** установлено значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4853">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="a573a-4854">Массив **апропертисетс** не существует.</span><span class="sxs-lookup"><span data-stu-id="a573a-4854">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="a573a-4855">При необходимости заполняются различные поля заполнения.</span><span class="sxs-lookup"><span data-stu-id="a573a-4855">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="a573a-4856">Сообщение отправляется на сервер.</span><span class="sxs-lookup"><span data-stu-id="a573a-4856">The message is sent to the server.</span></span>

4.  <span data-ttu-id="a573a-4857">Сервер проверяет правильность **\_ улчекксум** , проверяет, имеет ли пользователь разрешение на выполнение этого запроса, и реагирует на сообщение кпмконнектаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4857">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="a573a-4858">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4858">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4859">**\_ сообщение имеет значение** 0x000000C8, указывающее, что это сообщение кпмконнектаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4859">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="a573a-4860">для параметра **\_ Status** задано значение 0x0000000, означающее успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="a573a-4860">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="a573a-4861">**\_ улчекксум** имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="a573a-4861">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="a573a-4862">для **\_ ulReserved2** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4862">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="a573a-4863">Текст сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4863">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4864">для поля **\_ serverVersion** установлено значение 0x00000007 (32-разрядная версия windows XP или 32-разрядная версия Windows Server 2003).</span><span class="sxs-lookup"><span data-stu-id="a573a-4864">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="a573a-4865">**\_ зарезервированные** поля заполняются произвольными данными.</span><span class="sxs-lookup"><span data-stu-id="a573a-4865">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="a573a-4866">Клиент готовит сообщение Кпмкреатекуерин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4866">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="a573a-4867">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4867">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4868">**\_ сообщение имеет значение** 0x000000CA, указывающее, что это сообщение кпмкреатекуерин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4868">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="a573a-4869">для параметра **\_ Status** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4869">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="a573a-4870">**\_ улчекксум** содержит контрольную сумму, вычисленную в соответствии с 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="a573a-4870">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="a573a-4871">для **\_ ulReserved2** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4871">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="a573a-4872">Текст сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4872">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4873">Поле **size (размер** ) задает размер остальной части сообщения.</span><span class="sxs-lookup"><span data-stu-id="a573a-4873">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="a573a-4874">Для поля **кколумнсетпресент** задано значение 0x01.</span><span class="sxs-lookup"><span data-stu-id="a573a-4874">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="a573a-4875">Поле набора **столбцов** имеет тип кколумнсет.</span><span class="sxs-lookup"><span data-stu-id="a573a-4875">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="a573a-4876">Структура Кколумнсет, включающая в себя это поле, задается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4876">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="a573a-4877">поле **\_ Count** имеет значение 0x00000001, указывающее, что возвращается один столбец.</span><span class="sxs-lookup"><span data-stu-id="a573a-4877">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="a573a-4878">Массив **индексов** — это 0x00000000, указывающий первую запись в \_ апропспек.</span><span class="sxs-lookup"><span data-stu-id="a573a-4878">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="a573a-4879">Поле **крестриктионпресент** имеет значение 0x01, указывающее на наличие поля **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="a573a-4879">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="a573a-4880">Поле **ограничения** имеет тип крестриктион и имеет значение:</span><span class="sxs-lookup"><span data-stu-id="a573a-4880">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="a573a-4881">для **\_ ултипе** задано значение 0x00000004 (ртконтент).</span><span class="sxs-lookup"><span data-stu-id="a573a-4881">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="a573a-4882">для параметра **\_ Weight** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4882">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="a573a-4883">Оставшаяся часть поля содержит структуру Кконтентрестриктион:</span><span class="sxs-lookup"><span data-stu-id="a573a-4883">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="a573a-4884">**\_ Задано значение GUID** B725F130-47EF-101A-A5F1-02608c9eebac/0X00000001 (для прспек \_ PropID)/0x13, представляющее тело документа.</span><span class="sxs-lookup"><span data-stu-id="a573a-4884">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="a573a-4885">Для **\_ CC** задано значение 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="a573a-4885">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="a573a-4886">для **\_ пвксфрасе** задана строка «Microsoft».</span><span class="sxs-lookup"><span data-stu-id="a573a-4886">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="a573a-4887">для **\_ LCID** задано значение 0X409 (для английского языка).</span><span class="sxs-lookup"><span data-stu-id="a573a-4887">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="a573a-4888">для **\_ улженератемесод** задано значение 0x00000000 (точное совпадение).</span><span class="sxs-lookup"><span data-stu-id="a573a-4888">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="a573a-4889">**Ксортпресент** имеет значение 0x00.</span><span class="sxs-lookup"><span data-stu-id="a573a-4889">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="a573a-4890">**Ккатегоризатионсетпресент** имеет значение 0x00.</span><span class="sxs-lookup"><span data-stu-id="a573a-4890">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="a573a-4891">**Ровсетпропертиес** задается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4891">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="a573a-4892">**\_ убулеаноптионс** имеет значение 0x00000001 (последовательный).</span><span class="sxs-lookup"><span data-stu-id="a573a-4892">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="a573a-4893">для **\_ улмаксопенровс** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4893">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="a573a-4894">для **\_ улмеморюсаже** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4894">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="a573a-4895">\_для **кмаксресултс** задано значение 0x00000100 (возвращается не более 256 строк).</span><span class="sxs-lookup"><span data-stu-id="a573a-4895">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="a573a-4896">для **\_ ккмдтимеаут** задано значение 0x00000000 (никогда не время ожидания).</span><span class="sxs-lookup"><span data-stu-id="a573a-4896">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="a573a-4897">**Пидмаппер** имеет значение:</span><span class="sxs-lookup"><span data-stu-id="a573a-4897">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="a573a-4898">для параметра **\_ Count** задано значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="a573a-4898">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="a573a-4899">**\_ апропспек** имеет значение GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC/0X00000001 (для прспек \_ PropID)/0x0000000c, которое представляет свойство размера файла Windows.</span><span class="sxs-lookup"><span data-stu-id="a573a-4899">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="a573a-4900">Сервер обрабатывает его и реагирует на сообщение Кпмкреатекуерйоут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4900">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="a573a-4901">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4901">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4902">**\_ сообщение имеет значение** 0x000000CA, указывающее, что это сообщение кпмкреатекуерйоут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4902">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="a573a-4903">**\_ состояние** установлено в значение Success.</span><span class="sxs-lookup"><span data-stu-id="a573a-4903">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="a573a-4904">**\_ улчекксум** имеет значение 0x00000000 (или любое другое произвольное значение).</span><span class="sxs-lookup"><span data-stu-id="a573a-4904">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="a573a-4905">**\_ ulReserved2** имеет значение 0x00000000 (или любое другое произвольное значение).</span><span class="sxs-lookup"><span data-stu-id="a573a-4905">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="a573a-4906">Текст сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4906">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4907">**\_ фтруесекеунтиал** имеет значение 0x00000000, указывающее, что запрос может использовать индекс.</span><span class="sxs-lookup"><span data-stu-id="a573a-4907">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="a573a-4908">**\_ фворкидуникуе** имеет значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="a573a-4908">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="a573a-4909">Массив **акурсорс** содержит только один элемент, представляющий маркер курсора для этого запроса.</span><span class="sxs-lookup"><span data-stu-id="a573a-4909">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="a573a-4910">Значение зависит от состояния сервера.</span><span class="sxs-lookup"><span data-stu-id="a573a-4910">The value depends on the state of the server.</span></span> <span data-ttu-id="a573a-4911">Предположим, что возвращаемое значение — 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="a573a-4911">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="a573a-4912">Клиент выдает сообщение запроса Кпмсетбиндингсин для определения формата строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-4912">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="a573a-4913">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4913">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4914">**\_ сообщение имеет значение** 0x000000D0, указывающее, что это сообщение кпмсетбиндингсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4914">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="a573a-4915">**\_ состояние** установлено в значение Success.</span><span class="sxs-lookup"><span data-stu-id="a573a-4915">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="a573a-4916">**\_ улчекксум** имеет значение 0x00000000 (или любое другое произвольное значение).</span><span class="sxs-lookup"><span data-stu-id="a573a-4916">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="a573a-4917">**\_ ulReserved2** имеет значение 0x00000000 (или любое другое произвольное значение).</span><span class="sxs-lookup"><span data-stu-id="a573a-4917">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="a573a-4918">Текст сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4918">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4919">для **\_ хкурсор** задано значение 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="a573a-4919">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="a573a-4920">для **\_ кбров** задано значение 0x10 (достаточно большое, чтобы вместить столбцы).</span><span class="sxs-lookup"><span data-stu-id="a573a-4920">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="a573a-4921">**\_ кббиндингдеск** задается в сочетании с размером полей **\_ кколумнс** и **\_ аколумнс** .</span><span class="sxs-lookup"><span data-stu-id="a573a-4921">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="a573a-4922">**\_ кколумнс** имеет значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="a573a-4922">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="a573a-4923">Массив **\_ аколумнс** имеет значение, содержащее одну структуру ктаблеколумн, содержащую:</span><span class="sxs-lookup"><span data-stu-id="a573a-4923">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="a573a-4924">**\_ Пропспек** имеет значение GUID b725f130-47ef-101A-A5-F1-02608c9eebac/0X00000001 (для прспек \_ PropID)/0x0000000c, которое представляет свойство размера файла Windows.</span><span class="sxs-lookup"><span data-stu-id="a573a-4924">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="a573a-4925">для **\_ втипе** задано значение 0x0015 (VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="a573a-4925">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="a573a-4926">Для **\_ валуеусед** задано значение 0x01 (столбец передается в строке).</span><span class="sxs-lookup"><span data-stu-id="a573a-4926">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="a573a-4927">Для **\_ валуеоффсет** задано значение 0x0002 (в начале строки).</span><span class="sxs-lookup"><span data-stu-id="a573a-4927">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="a573a-4928">Для **\_ валуесизе** задано значение 0X08 (размер VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="a573a-4928">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="a573a-4929">Для **\_ статусусед** задано значение 0x01.</span><span class="sxs-lookup"><span data-stu-id="a573a-4929">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="a573a-4930">Для **\_ статусоффсет** задано значение 0x0A.</span><span class="sxs-lookup"><span data-stu-id="a573a-4930">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="a573a-4931">**\_ Ленгсусед** имеет значение 0x00.</span><span class="sxs-lookup"><span data-stu-id="a573a-4931">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="a573a-4932">Сервер обрабатывает его и реагирует на сообщение Кпмсетбиндингсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4932">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="a573a-4933">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4933">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4934">для **\_ сообщения** задано значение 0x000000D0.</span><span class="sxs-lookup"><span data-stu-id="a573a-4934">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="a573a-4935">**\_ состояние** установлено в значение Success.</span><span class="sxs-lookup"><span data-stu-id="a573a-4935">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="a573a-4936">**\_ улчекксум** имеет значение 0x00000000 (или любое другое произвольное значение).</span><span class="sxs-lookup"><span data-stu-id="a573a-4936">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="a573a-4937">**\_ ulReserved2** имеет значение 0x00000000 (или любое другое произвольное значение).</span><span class="sxs-lookup"><span data-stu-id="a573a-4937">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="a573a-4938">Клиент выдает сообщение запроса Кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4938">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="a573a-4939">Предположим, что клиент готов принять 100 строк на этом этапе и хочет, чтобы они были в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="a573a-4939">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="a573a-4940">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4940">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4941">**\_ сообщение имеет значение** 0x000000CC, указывающее, что это сообщение кпмжетровсин.</span><span class="sxs-lookup"><span data-stu-id="a573a-4941">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="a573a-4942">для параметра **\_ Status** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4942">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="a573a-4943">**\_ улчекксум** содержит контрольную сумму, вычисленную в соответствии с разделом 0.</span><span class="sxs-lookup"><span data-stu-id="a573a-4943">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="a573a-4944">для **\_ ulReserved2** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4944">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="a573a-4945">Текст сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4945">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4946">для **\_ хкурсор** задано значение 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="a573a-4946">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="a573a-4947">для **\_ кровстотрансфер** задано значение 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="a573a-4947">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="a573a-4948">**\_ кроввидс** имеет значение 0x00000010 (из привязок).</span><span class="sxs-lookup"><span data-stu-id="a573a-4948">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="a573a-4949">для **\_ кбсик** задано значение 0x14, которое равно размеру полей eType, \_ CHAP и кровсикнекст.</span><span class="sxs-lookup"><span data-stu-id="a573a-4949">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="a573a-4950">для **\_ кбресервед** задано значение 0x18 (0x14 Plus \_ кбсик).</span><span class="sxs-lookup"><span data-stu-id="a573a-4950">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="a573a-4951">для **\_ кбреадбуффер** задано значение 0x800 (0x64 \* 0x10 округляется до следующего кратного 0x200).</span><span class="sxs-lookup"><span data-stu-id="a573a-4951">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="a573a-4952">для **\_ улклиентбасе** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4952">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="a573a-4953">**\_ фбвдфетч** имеет значение 0x00000000, указывающее, что строки должны быть получены в прямом порядке.</span><span class="sxs-lookup"><span data-stu-id="a573a-4953">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="a573a-4954">**eType** имеет значение 0x0000001, указывающее, что клиент хочет получить следующие строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-4954">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="a573a-4955">для параметра **\_ CHAP** задано значение 0 (не в разделе результат).</span><span class="sxs-lookup"><span data-stu-id="a573a-4955">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="a573a-4956">Для **сикдескриптион** задано значение кровсикнекст.</span><span class="sxs-lookup"><span data-stu-id="a573a-4956">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="a573a-4957">Структура Кровсикнекст содержит следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a573a-4957">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="a573a-4958">Для **Цитблчапт** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4958">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="a573a-4959">для **\_ хрегион** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4959">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="a573a-4960">**\_ кскип** имеет значение 0, указывающее, что клиенту не нужно пропускать строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-4960">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="a573a-4961">Сервер обрабатывает его и реагирует на сообщение Кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4961">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="a573a-4962">Предположим, что сервер нашел 100 документов, содержащих слово Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a573a-4962">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="a573a-4963">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4963">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4964">**\_ сообщение имеет значение** 0x000000CC, указывающее, что это сообщение кпмжетровсаут.</span><span class="sxs-lookup"><span data-stu-id="a573a-4964">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="a573a-4965">**\_ состояние** установлено в значение Success.</span><span class="sxs-lookup"><span data-stu-id="a573a-4965">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="a573a-4966">для **\_ улчекксум** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4966">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="a573a-4967">для **\_ ulReserved2** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4967">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="a573a-4968">Текст сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4968">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4969">Для **\_ кровсретурнед** задано значение 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="a573a-4969">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="a573a-4970">**eType** имеет значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="a573a-4970">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="a573a-4971">для параметра **\_ CHAP** задано значение 0x00000000 (не в разделе результат).</span><span class="sxs-lookup"><span data-stu-id="a573a-4971">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="a573a-4972">**Сикдескриптион** содержит структуру кровсикнекст, заполненную следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4972">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="a573a-4973">Для **Цитблчапт** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4973">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="a573a-4974">для **\_ хрегион** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4974">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="a573a-4975">**\_ кскип** имеет значение 0, указывающее, что клиенту не нужно пропускать строки.</span><span class="sxs-lookup"><span data-stu-id="a573a-4975">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="a573a-4976">**Строки** содержат размер 100 документов, содержащих слово «Microsoft».</span><span class="sxs-lookup"><span data-stu-id="a573a-4976">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="a573a-4977">Так как это данные фиксированного размера, они просто структурированы как список из 100, 8-байтных целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="a573a-4977">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="a573a-4978">Клиент отправляет сообщение Кпмдисконнект, чтобы завершить соединение.</span><span class="sxs-lookup"><span data-stu-id="a573a-4978">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="a573a-4979">Заголовок сообщения заполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a573a-4979">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="a573a-4980">**\_ сообщение имеет значение** 0x000000C9, указывающее, что это сообщение кпмдисконнект.</span><span class="sxs-lookup"><span data-stu-id="a573a-4980">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="a573a-4981">для параметра **\_ Status** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4981">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="a573a-4982">для **\_ улчекксум** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4982">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="a573a-4983">Сервер обрабатывает сообщение и удаляет все состояние клиента.</span><span class="sxs-lookup"><span data-stu-id="a573a-4983">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="a573a-4984">4,2. Пример 2</span><span class="sxs-lookup"><span data-stu-id="a573a-4984">4.2 Example 2</span></span>

<span data-ttu-id="a573a-4985">В предыдущем примере запрос был достаточно простым.</span><span class="sxs-lookup"><span data-stu-id="a573a-4985">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="a573a-4986">Давайте теперь рассмотрим немного более сложный запрос.</span><span class="sxs-lookup"><span data-stu-id="a573a-4986">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="a573a-4987">Предположим, что пользователь хочет получить размер документов, содержащих оба слова: "Microsoft" и "Office".</span><span class="sxs-lookup"><span data-stu-id="a573a-4987">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="a573a-4988">Это указывается путем изменения поля ограничения, содержащегося в сообщении Кпмкреатекуерин, отправленном на шаге 5, следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a573a-4988">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="a573a-4989">Поле **ограничения** имеет тип крестриктион и имеет значение:</span><span class="sxs-lookup"><span data-stu-id="a573a-4989">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="a573a-4990">для **\_ ултипе** задано значение 0x00000004 (ртанд).</span><span class="sxs-lookup"><span data-stu-id="a573a-4990">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="a573a-4991">для параметра **\_ Weight** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4991">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="a573a-4992">Оставшаяся часть поля содержит структуру Кнодерестриктион:</span><span class="sxs-lookup"><span data-stu-id="a573a-4992">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="a573a-4993">**\_ кноде** имеет значение 0x00000002, указывающее, что в массиве паноде есть два узла.</span><span class="sxs-lookup"><span data-stu-id="a573a-4993">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="a573a-4994">Поле **\_ паноде** представляет собой массив из двух структур крестриктион.</span><span class="sxs-lookup"><span data-stu-id="a573a-4994">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="a573a-4995">**\_ паноде \[ 0 \]** содержит:</span><span class="sxs-lookup"><span data-stu-id="a573a-4995">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="a573a-4996">для **\_ ултипе** задано значение 0x00000004 (ртконтент).</span><span class="sxs-lookup"><span data-stu-id="a573a-4996">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="a573a-4997">для параметра **\_ Weight** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-4997">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="a573a-4998">Оставшаяся часть поля содержит структуру Кконтентрестриктион:</span><span class="sxs-lookup"><span data-stu-id="a573a-4998">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="a573a-4999">Для **\_ свойства** задано значение GUID b725f130-47ef-101A-a5f1-02608c9eebac/0X00000001 (для прспек \_ PropID)/0x13.</span><span class="sxs-lookup"><span data-stu-id="a573a-4999">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="a573a-5000">Для **\_ CC** задано значение 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="a573a-5000">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="a573a-5001">для **\_ пвксфрасе** задана строка «Microsoft».</span><span class="sxs-lookup"><span data-stu-id="a573a-5001">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="a573a-5002">для **\_ LCID** задано значение 0X409 (для английского языка).</span><span class="sxs-lookup"><span data-stu-id="a573a-5002">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="a573a-5003">для **\_ улженератемесод** задано значение 0x00000000 (точное совпадение).</span><span class="sxs-lookup"><span data-stu-id="a573a-5003">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="a573a-5004">**\_ паноде \[ 1 \]** содержит:</span><span class="sxs-lookup"><span data-stu-id="a573a-5004">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="a573a-5005">для **\_ ултипе** задано значение 0x00000004 (ртконтент).</span><span class="sxs-lookup"><span data-stu-id="a573a-5005">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="a573a-5006">для параметра **\_ Weight** задано значение 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a573a-5006">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="a573a-5007">Оставшаяся часть поля содержит структуру Кконтентрестриктион:</span><span class="sxs-lookup"><span data-stu-id="a573a-5007">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="a573a-5008">Для **\_ свойства** задано значение GUID b725f130-47ef-101A-a5f1-02608c9eebac/0X00000001 (для прспек \_ PropID)/0x13.</span><span class="sxs-lookup"><span data-stu-id="a573a-5008">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="a573a-5009">Для **\_ CC** задано значение 0x00000006.</span><span class="sxs-lookup"><span data-stu-id="a573a-5009">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="a573a-5010">для **\_ пвксфрасе** задана строка "Office".</span><span class="sxs-lookup"><span data-stu-id="a573a-5010">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="a573a-5011">для **\_ LCID** задано значение 0X409 (для английского языка).</span><span class="sxs-lookup"><span data-stu-id="a573a-5011">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="a573a-5012">для **\_ улженератемесод** задано значение 0x00000000 (точное совпадение).</span><span class="sxs-lookup"><span data-stu-id="a573a-5012">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="a573a-5013">5. Безопасность</span><span class="sxs-lookup"><span data-stu-id="a573a-5013">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="a573a-5014">5.1. Вопросы безопасности для разработчиков</span><span class="sxs-lookup"><span data-stu-id="a573a-5014">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="a573a-5015">Реализации индексирования, для которых требуется индексирование защищенного содержимого, следует использовать контекст пользователя, предоставляемый SMB \[ MS-SMB, \] чтобы обрезать результаты поиска и возвратить только те, которые доступны вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="a573a-5015">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="a573a-5016">5.2. Индекс параметров безопасности</span><span class="sxs-lookup"><span data-stu-id="a573a-5016">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="a573a-5017">Параметр безопасности</span><span class="sxs-lookup"><span data-stu-id="a573a-5017">Security Parameter</span></span>  | <span data-ttu-id="a573a-5018">Section</span><span class="sxs-lookup"><span data-stu-id="a573a-5018">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="a573a-5019">Уровень олицетворения</span><span class="sxs-lookup"><span data-stu-id="a573a-5019">Impersonation level</span></span> | <span data-ttu-id="a573a-5020">2.1</span><span class="sxs-lookup"><span data-stu-id="a573a-5020">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="a573a-5021">6 индекс поведения, зависящего от версии</span><span class="sxs-lookup"><span data-stu-id="a573a-5021">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="a573a-5022">Поведение конкретной версии</span><span class="sxs-lookup"><span data-stu-id="a573a-5022">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="a573a-5023">Section</span><span class="sxs-lookup"><span data-stu-id="a573a-5023">Section</span></span>   | <span data-ttu-id="a573a-5024">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a573a-5024">Windows 2000</span></span> | <span data-ttu-id="a573a-5025">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a573a-5025">Windows XP</span></span> | <span data-ttu-id="a573a-5026">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a573a-5026">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="a573a-5027">Этот Протокол реализован в Windows 2000, Windows XP, Windows Server 2003 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a573a-5027">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="a573a-5028">1.3.2</span><span class="sxs-lookup"><span data-stu-id="a573a-5028">1.3.2</span></span>     | <span data-ttu-id="a573a-5029">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5029">X</span></span>            | <span data-ttu-id="a573a-5030">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5030">X</span></span>          | <span data-ttu-id="a573a-5031">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5031">X</span></span>                   |
| <span data-ttu-id="a573a-5032">Приложения обычно взаимодействуют с оболочкой интерфейса OLE DB</span><span class="sxs-lookup"><span data-stu-id="a573a-5032">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="a573a-5033">1.4</span><span class="sxs-lookup"><span data-stu-id="a573a-5033">1.4</span></span>       | <span data-ttu-id="a573a-5034">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5034">X</span></span>            | <span data-ttu-id="a573a-5035">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5035">X</span></span>          | <span data-ttu-id="a573a-5036">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5036">X</span></span>                   |
| <span data-ttu-id="a573a-5037">Значения NTSTATUS</span><span class="sxs-lookup"><span data-stu-id="a573a-5037">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="a573a-5038">1.8</span><span class="sxs-lookup"><span data-stu-id="a573a-5038">1.8</span></span>       | <span data-ttu-id="a573a-5039">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5039">X</span></span>            | <span data-ttu-id="a573a-5040">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5040">X</span></span>          | <span data-ttu-id="a573a-5041">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5041">X</span></span>                   |
| <span data-ttu-id="a573a-5042">Клиент устанавливает \_ поле состояния в каждом заголовке сообщения.</span><span class="sxs-lookup"><span data-stu-id="a573a-5042">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="a573a-5043">2.2.2</span><span class="sxs-lookup"><span data-stu-id="a573a-5043">2.2.2</span></span>     | <span data-ttu-id="a573a-5044">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5044">X</span></span>            | <span data-ttu-id="a573a-5045">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5045">X</span></span>          | <span data-ttu-id="a573a-5046">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5046">X</span></span>                   |
| <span data-ttu-id="a573a-5047">значение Кпендингсканс обычно равно нулю</span><span class="sxs-lookup"><span data-stu-id="a573a-5047">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="a573a-5048">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="a573a-5048">2.2.3.1</span></span>   | <span data-ttu-id="a573a-5049">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5049">X</span></span>            | <span data-ttu-id="a573a-5050">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5050">X</span></span>          | <span data-ttu-id="a573a-5051">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5051">X</span></span>                   |
| <span data-ttu-id="a573a-5052">значение Иклиентверсион</span><span class="sxs-lookup"><span data-stu-id="a573a-5052">iClientVersion value</span></span>                                                                              | <span data-ttu-id="a573a-5053">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="a573a-5053">2.2.3.6</span></span>   | <span data-ttu-id="a573a-5054">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5054">X</span></span>            | <span data-ttu-id="a573a-5055">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5055">X</span></span>          | <span data-ttu-id="a573a-5056">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5056">X</span></span>                   |
| <span data-ttu-id="a573a-5057">\_значение Кбчунк</span><span class="sxs-lookup"><span data-stu-id="a573a-5057">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="a573a-5058">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="a573a-5058">2.2.3.19</span></span>  | <span data-ttu-id="a573a-5059">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5059">X</span></span>            | <span data-ttu-id="a573a-5060">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5060">X</span></span>          | <span data-ttu-id="a573a-5061">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5061">X</span></span>                   |
| <span data-ttu-id="a573a-5062">32-разрядные и 64-разрядные адреса памяти</span><span class="sxs-lookup"><span data-stu-id="a573a-5062">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="a573a-5063">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="a573a-5063">3.2.4.2.4</span></span> | <span data-ttu-id="a573a-5064">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5064">X</span></span>            | <span data-ttu-id="a573a-5065">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5065">X</span></span>          | <span data-ttu-id="a573a-5066">X</span><span class="sxs-lookup"><span data-stu-id="a573a-5066">X</span></span>                   |



 

 

 





