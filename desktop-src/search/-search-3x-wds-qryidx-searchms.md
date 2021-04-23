---
description: Протокол поиска — MS — это соглашение для запроса индекса поиска Windows.
ms.assetid: ab2695ed-4ef3-4687-81b0-416ca7086e5f
title: Запрос индекса с помощью протокола Search-MS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d835b6db1c9b05b97d5d075b62158069d89029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808963"
---
# <a name="querying-the-index-with-the-search-ms-protocol"></a><span data-ttu-id="04e9f-103">Запрос индекса с помощью протокола Search-MS</span><span class="sxs-lookup"><span data-stu-id="04e9f-103">Querying the Index with the search-ms Protocol</span></span>

<span data-ttu-id="04e9f-104">Протокол **поиска — MS**[](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) — это соглашение для запроса индекса поиска Windows.  </span><span class="sxs-lookup"><span data-stu-id="04e9f-104">The **search-ms**  [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is a convention for querying the Windows Search index.</span></span> <span data-ttu-id="04e9f-105">Протокол позволяет приложениям, например проводнику, запрашивать индекс с аргументами-значениями параметров, включая аргументы свойств, ранее сохраненные поисковые запросы, синтаксис расширенных запросов (АКС), синтаксис естественного запроса (НКС) и идентификаторы кода языка (LCID) как для индексатора, так и для самого запроса.</span><span class="sxs-lookup"><span data-stu-id="04e9f-105">The protocol enables applications, like Windows Explorer, to query the index with parameter-value arguments, including property arguments, previously saved searches, Advanced Query Syntax (AQS), Natural Query Syntax (NQS), and language code identifiers (LCIDs) for both the indexer and the query itself.</span></span>

<span data-ttu-id="04e9f-106">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="04e9f-106">This section is organized as follows:</span></span>

-   [<span data-ttu-id="04e9f-107">Начало работы с Parameter-Valueными аргументами</span><span class="sxs-lookup"><span data-stu-id="04e9f-107">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
-   [<span data-ttu-id="04e9f-108">Аргументы идентификатора языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="04e9f-108">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
-   [<span data-ttu-id="04e9f-109">Переданный аргумент</span><span class="sxs-lookup"><span data-stu-id="04e9f-109">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
-   [<span data-ttu-id="04e9f-110">Аргумент СИНТАКСИСа</span><span class="sxs-lookup"><span data-stu-id="04e9f-110">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
-   [<span data-ttu-id="04e9f-111">СТАККЕДБИ, аргумент</span><span class="sxs-lookup"><span data-stu-id="04e9f-111">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
-   [<span data-ttu-id="04e9f-112">Аргумент вложенного запроса</span><span class="sxs-lookup"><span data-stu-id="04e9f-112">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)

## <a name="related-topics"></a><span data-ttu-id="04e9f-113">См. также</span><span class="sxs-lookup"><span data-stu-id="04e9f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04e9f-114">Отправка программных запросов к индексу</span><span class="sxs-lookup"><span data-stu-id="04e9f-114">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="04e9f-115">Использование методов SQL и АКС для запроса индекса</span><span class="sxs-lookup"><span data-stu-id="04e9f-115">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="04e9f-116">Запрос индекса с помощью Исеарчкуерихелпер</span><span class="sxs-lookup"><span data-stu-id="04e9f-116">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="04e9f-117">Запрос к индексу с помощью синтаксиса SQL для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="04e9f-117">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="04e9f-118">Использование расширенного синтаксиса запросов программными средствами</span><span class="sxs-lookup"><span data-stu-id="04e9f-118">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 
