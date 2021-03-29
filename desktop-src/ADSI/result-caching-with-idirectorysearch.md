---
title: Кэширование результатов с помощью IDirectorySearch
description: Параметр ADS \_ сеарчпреф \_ кэша \_ результатов кэширует результирующий набор на клиенте.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Кэширование результатов с помощью IDirectorySearch ADSI
- ADSI, поиск, IDirectorySearch, другие параметры поиска, кэширование результатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95016699eb4de36344b7e40f35e1a4a9cce761b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328371"
---
# <a name="result-caching-with-idirectorysearch"></a><span data-ttu-id="6e738-105">Кэширование результатов с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="6e738-105">Result Caching with IDirectorySearch</span></span>

<span data-ttu-id="6e738-106">Параметр **ADS \_ сеарчпреф \_ кэша \_ результатов** кэширует результирующий набор на клиенте.</span><span class="sxs-lookup"><span data-stu-id="6e738-106">The **ADS\_SEARCHPREF\_CACHE\_RESULTS** preference caches the result set on the client.</span></span> <span data-ttu-id="6e738-107">Кэширование результатов позволяет приложению хранить полученный результирующий набор и повторно проходить извлеченные строки.</span><span class="sxs-lookup"><span data-stu-id="6e738-107">Result caching enables an application to retain a retrieved result set and go through the retrieved rows again.</span></span> <span data-ttu-id="6e738-108">Он также обеспечивает поддержку курсора, где методы [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) и [**IDirectorySearch:: жетпревиаусров**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) можно использовать для перемещения результирующего набора вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="6e738-108">It also enables cursor support where the [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) and [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) methods can be used to move up and down the result set.</span></span>

<span data-ttu-id="6e738-109">По умолчанию кэширование результатов отключено.</span><span class="sxs-lookup"><span data-stu-id="6e738-109">By default, result caching is disabled.</span></span> <span data-ttu-id="6e738-110">Кэширование результатов должно быть включено, если выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="6e738-110">Result caching should be enabled if any one of the following is true:</span></span>

-   <span data-ttu-id="6e738-111">Значение, если один и тот же результирующий набор необходимо перечислить несколько раз без повторного выполнения поиска на сервере.</span><span class="sxs-lookup"><span data-stu-id="6e738-111">If the same result set must be enumerated multiple times without performing the search again on the server.</span></span>
-   <span data-ttu-id="6e738-112">Если выполнение поиска занимает много ресурсов на сервере (медленное подключение, большой результирующий набор или сложный запрос).</span><span class="sxs-lookup"><span data-stu-id="6e738-112">If performing the search is resource-intensive on the server (slow connection, large result set, or complex query).</span></span>
-   <span data-ttu-id="6e738-113">Значение, если требуется поддержка курсора.</span><span class="sxs-lookup"><span data-stu-id="6e738-113">If cursor support is required.</span></span>

<span data-ttu-id="6e738-114">Отключите кэширование, если приложение должно уменьшить требования к памяти для кэширования большого результирующего набора на клиенте.</span><span class="sxs-lookup"><span data-stu-id="6e738-114">Turn off caching if your application must reduce memory requirements for caching a large result set at the client.</span></span>

<span data-ttu-id="6e738-115">Кэширование результатов увеличивает требования к памяти на клиенте, поэтому кэширование результатов должно быть отключено, если это является проблемой.</span><span class="sxs-lookup"><span data-stu-id="6e738-115">Result caching increases the memory requirements on the client, so result caching should be disabled if this is a concern.</span></span>

<span data-ttu-id="6e738-116">Чтобы включить кэширование результатов, установите параметр поиска **\_ \_ \_ результатов кэша Сеарчпреф** с логическим значением **адстипе \_** , равным **true** , в массиве [**\_ \_ сведений об ADS сеарчпреф**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) , переданном в метод [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="6e738-116">To enable result caching, set an **ADS\_SEARCHPREF\_CACHE\_RESULTS** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="6e738-117">В следующем примере кода показано, как включить кэширование результатов.</span><span class="sxs-lookup"><span data-stu-id="6e738-117">The following code example shows how to enable result caching.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




