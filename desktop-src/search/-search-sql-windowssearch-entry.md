---
description: Windows Search предоставляет функции обхода содержимого и поиска, поддерживающие полнотекстовый поиск. Язык запросов, используемый службой поиска Windows, расширяет стандартный синтаксис запросов базы данных SQL-92 и SQL-99, что позволяет повысить его полезность при поиске на основе текста.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: Запрос к индексу с помощью синтаксиса SQL для поиска Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5696891b14340e8d8fe97f0c0cfbdc75db08e464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497061"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a><span data-ttu-id="fa325-104">Запрос к индексу с помощью синтаксиса SQL для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="fa325-104">Querying the Index with Windows Search SQL Syntax</span></span>

<span data-ttu-id="fa325-105">Windows Search предоставляет функции обхода содержимого и поиска, поддерживающие полнотекстовый поиск.</span><span class="sxs-lookup"><span data-stu-id="fa325-105">Windows Search provides content crawling and search features that support full-text searching.</span></span> <span data-ttu-id="fa325-106">Язык запросов, используемый службой поиска Windows, расширяет стандартный синтаксис запросов базы данных SQL-92 и SQL-99, что позволяет повысить его полезность при поиске на основе текста.</span><span class="sxs-lookup"><span data-stu-id="fa325-106">The query language used by Windows Search extends the standard SQL-92 and SQL-99 database query syntax to enhance its usefulness with text-based searches.</span></span>

<span data-ttu-id="fa325-107">Все функции Windows Search язык SQL (SQL) совместимы с Windows Search в Windows Vista и более поздних версий, включая все версии Windows 10.</span><span class="sxs-lookup"><span data-stu-id="fa325-107">All features of Windows Search Structured Query Language (SQL) are compatible with Windows Search on Windows Vista, and later, including all versions of Windows 10.</span></span>

<span data-ttu-id="fa325-108">Этот раздел содержит общие сведения о синтаксисе SQL в Windows Search и содержит следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="fa325-108">This section provides an overview of SQL syntax in Windows Search, and includes the following topics:</span></span>

- [<span data-ttu-id="fa325-109">Общие сведения о синтаксисе SQL для службы поиска Windows</span><span class="sxs-lookup"><span data-stu-id="fa325-109">Overview of Windows Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
- [<span data-ttu-id="fa325-110">Общие сведения о языке запросов</span><span class="sxs-lookup"><span data-stu-id="fa325-110">General Query Language Information</span></span>](-search-sql-generalqueryinfo.md)
- [<span data-ttu-id="fa325-111">ГРУППИРОВАТЬ ПО... Поверх... Баланс</span><span class="sxs-lookup"><span data-stu-id="fa325-111">GROUP ON ... OVER... Statement</span></span>](-search-sql-group-on-over.md)
- [<span data-ttu-id="fa325-112">Инструкция SELECT</span><span class="sxs-lookup"><span data-stu-id="fa325-112">SELECT Statement</span></span>](-search-sql-select.md)
- [<span data-ttu-id="fa325-113">Предложение FROM</span><span class="sxs-lookup"><span data-stu-id="fa325-113">FROM Clause</span></span>](-search-sql-from.md)
- [<span data-ttu-id="fa325-114">Предложения WHERE</span><span class="sxs-lookup"><span data-stu-id="fa325-114">WHERE Clause</span></span>](-search-sql-where.md)
- [<span data-ttu-id="fa325-115">Предложение ORDER BY</span><span class="sxs-lookup"><span data-stu-id="fa325-115">ORDER BY Clause</span></span>](-search-sql-orderby.md)
- [<span data-ttu-id="fa325-116">РАНЖИРОВАНие по предложению</span><span class="sxs-lookup"><span data-stu-id="fa325-116">RANK BY Clause</span></span>](-search-sql-rankby.md)
- [<span data-ttu-id="fa325-117">Инструкция SET</span><span class="sxs-lookup"><span data-stu-id="fa325-117">SET Statement</span></span>](-search-sql-set.md)
- [<span data-ttu-id="fa325-118">Свойства набора строк</span><span class="sxs-lookup"><span data-stu-id="fa325-118">Rowset Properties</span></span>](-search-sql-rowset-properties.md)

<span data-ttu-id="fa325-119">В этой документации предполагается, что вы знакомы с связыванием объектов и внедрением базы данных (OLE DB) и SQL.</span><span class="sxs-lookup"><span data-stu-id="fa325-119">This documentation assumes familiarity with Object Linking and Embedding Database (OLE DB), and SQL.</span></span>

## <a name="code-samples"></a><span data-ttu-id="fa325-120">Примеры кода</span><span class="sxs-lookup"><span data-stu-id="fa325-120">Code samples</span></span>

<span data-ttu-id="fa325-121">В примере кода ВССКЛ показано, как взаимодействовать между Microsoft OLE DB и Windows Search через SQL.</span><span class="sxs-lookup"><span data-stu-id="fa325-121">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through SQL.</span></span> <span data-ttu-id="fa325-122">В примере кода Всоледб показана библиотека ATL OLE DB доступ к приложениям поиска Windows, а также два дополнительных метода получения результатов из службы поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="fa325-122">The WSOleDB code sample illustrates Active Template Library (ATL) OLE DB access to Windows Search applications, and two additional methods for retrieving results from Windows Search.</span></span> <span data-ttu-id="fa325-123">Оба образца доступны в [примерах Windows Search](-search-samples-ovw.md) и [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span><span class="sxs-lookup"><span data-stu-id="fa325-123">Both samples are available in the [Windows Search Samples](-search-samples-ovw.md) and the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa325-124">См. также</span><span class="sxs-lookup"><span data-stu-id="fa325-124">Related topics</span></span>

[<span data-ttu-id="fa325-125">Отправка программных запросов к индексу</span><span class="sxs-lookup"><span data-stu-id="fa325-125">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="fa325-126">Использование методов SQL и АКС для запроса индекса</span><span class="sxs-lookup"><span data-stu-id="fa325-126">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="fa325-127">Запрос индекса с помощью Исеарчкуерихелпер</span><span class="sxs-lookup"><span data-stu-id="fa325-127">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)

[<span data-ttu-id="fa325-128">Запрос индекса с помощью протокола Search-MS</span><span class="sxs-lookup"><span data-stu-id="fa325-128">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)

[<span data-ttu-id="fa325-129">Запрос к индексу с помощью синтаксиса SQL для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="fa325-129">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)

[<span data-ttu-id="fa325-130">Использование расширенного синтаксиса запросов программными средствами</span><span class="sxs-lookup"><span data-stu-id="fa325-130">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
