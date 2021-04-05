---
title: Указание других параметров поиска с помощью IDirectorySearch
description: Интерфейс IDirectorySearch обеспечивает дополнительный контроль над выполнением поиска с помощью параметров поиска.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Указание других параметров поиска с помощью IDirectorySearch ADSI
- ADSI, поиск, IDirectorySearch, другие параметры поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7064a291c3a299a5435ec454a17b1a666f20d0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986086"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a><span data-ttu-id="19fd1-105">Указание других параметров поиска с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="19fd1-105">Specifying Other Search Options with IDirectorySearch</span></span>

<span data-ttu-id="19fd1-106">Интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) обеспечивает дополнительный контроль над выполнением поиска с помощью параметров поиска.</span><span class="sxs-lookup"><span data-stu-id="19fd1-106">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provide additional control over how the search is performed through the use of search options.</span></span> <span data-ttu-id="19fd1-107">Эти параметры поиска задаются путем заполнения массива структур [**\_ \_ сведений сеарчпреф ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) и вызова метода [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="19fd1-107">These search options are set by filling in an array of [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) structures and calling the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="19fd1-108">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="19fd1-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="19fd1-109">Использование метода Сетсеарчпреференце</span><span class="sxs-lookup"><span data-stu-id="19fd1-109">Using the SetSearchPreference Method</span></span>](using-the-setsearchpreference-method.md)
-   [<span data-ttu-id="19fd1-110">Синхронный и асинхронный поиск с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="19fd1-110">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [<span data-ttu-id="19fd1-111">Подкачка с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="19fd1-111">Paging with IDirectorySearch</span></span>](paging-with-idirectorysearch.md)
-   [<span data-ttu-id="19fd1-112">Кэширование результатов с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="19fd1-112">Result Caching with IDirectorySearch</span></span>](result-caching-with-idirectorysearch.md)
-   [<span data-ttu-id="19fd1-113">Выполнение запроса к области атрибута</span><span class="sxs-lookup"><span data-stu-id="19fd1-113">Performing an Attribute Scope Query</span></span>](performing-an-attribute-scoped-query.md)
-   [<span data-ttu-id="19fd1-114">Сортировка результатов поиска с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="19fd1-114">Sorting the Search Results with IDirectorySearch</span></span>](sorting-the-search-results-with-idirectorysearch.md)
-   [<span data-ttu-id="19fd1-115">Отслеживание ссылок с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="19fd1-115">Referral Chasing with IDirectorySearch</span></span>](referral-chasing-with-idirectorysearch.md)
-   [<span data-ttu-id="19fd1-116">Ограничение размера с IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="19fd1-116">Size Limit with IDirectorySearch</span></span>](size-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="19fd1-117">Ограничение времени сервера на IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="19fd1-117">Server Time Limit with IDirectorySearch</span></span>](server-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="19fd1-118">Ограничение времени клиента с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="19fd1-118">Client Time Limit with IDirectorySearch</span></span>](client-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="19fd1-119">Возвращение только имен атрибутов с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="19fd1-119">Returning Only Attribute Names with IDirectorySearch</span></span>](returning-only-attribute-names-with-idirectorysearch.md)

 

 




