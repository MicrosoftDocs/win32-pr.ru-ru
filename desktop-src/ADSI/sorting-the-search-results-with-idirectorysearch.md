---
title: Сортировка результатов поиска с помощью IDirectorySearch
description: По умолчанию результаты поиска возвращаются в ненадежном порядке. Сеарчпреф, \_ \_ отсортированный \_ по параметру ADS, сообщает серверу о необходимости сортировки результирующего набора по указанному значению атрибута, прежде чем он будет возвращен клиенту.
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- Сортировка результатов поиска с помощью IDirectorySearch
- ADSI, поиск, IDirectorySearch, другие параметры поиска, сортировка результатов поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433d24b06ac4d361d6520d8af3376ea12acac1f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793830"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a><span data-ttu-id="e7358-106">Сортировка результатов поиска с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="e7358-106">Sorting the Search Results with IDirectorySearch</span></span>

<span data-ttu-id="e7358-107">По умолчанию результаты поиска возвращаются в ненадежном порядке.</span><span class="sxs-lookup"><span data-stu-id="e7358-107">By default, the results of a search are returned in no guaranteed order.</span></span> <span data-ttu-id="e7358-108">**Сеарчпреф, \_ \_ отсортированный \_ по** параметру ADS, сообщает серверу о необходимости сортировки результирующего набора по указанному значению атрибута, прежде чем он будет возвращен клиенту.</span><span class="sxs-lookup"><span data-stu-id="e7358-108">The **ADS\_SEARCHPREF\_SORT\_ON** preference instructs the server to sort the result set on a specified attribute value before it is returned to the client.</span></span>

<span data-ttu-id="e7358-109">Для сортировки рекомендуется использовать индексированные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="e7358-109">It is recommended that indexed attributes be used for sorting.</span></span> <span data-ttu-id="e7358-110">В противном случае сервер должен получить полный результирующий набор и отсортировать его перед отправкой результатов клиенту.</span><span class="sxs-lookup"><span data-stu-id="e7358-110">Otherwise, the server must retrieve the complete result set and sort it before sending any results to the client.</span></span> <span data-ttu-id="e7358-111">Это также относится к страничным поисковым операциям.</span><span class="sxs-lookup"><span data-stu-id="e7358-111">This also applies to paged searches.</span></span> <span data-ttu-id="e7358-112">Имейте в виду, что производительность отсортированного поиска будет увеличена, если фильтр включает индексированный атрибут, и этот атрибут указан в качестве ключа сортировки. в этом случае Active Directory может удовлетворить сортировку при обработке фильтра.</span><span class="sxs-lookup"><span data-stu-id="e7358-112">Be aware that performance of a sorted search will be increased if the filter includes an indexed attribute and that attribute is specified as the sort key; in this case, Active Directory can satisfy the sort while processing the filter.</span></span> <span data-ttu-id="e7358-113">Например, эффективный запрос на сортировку для набора пользователей может иметь фильтр, который включается (SN>Смит) и ключ сортировки Sn.</span><span class="sxs-lookup"><span data-stu-id="e7358-113">For example, an efficient sort query for a set of users could have a filter that included (sn>smith) and a sort key of sn.</span></span>

<span data-ttu-id="e7358-114">Сортировка на стороне сервера с помощью параметра **ADS \_ сеарчпреф \_ Сортировать \_ по** поиску снизит производительность сервера.</span><span class="sxs-lookup"><span data-stu-id="e7358-114">Server-side sorting with the **ADS\_SEARCHPREF\_SORT\_ON** search option will reduce the performance of the server.</span></span> <span data-ttu-id="e7358-115">Если вы будете выполнять много операций поиска, рассмотрите возможность сортировки результатов вручную на стороне клиента, чтобы уменьшить рабочую нагрузку на сервер.</span><span class="sxs-lookup"><span data-stu-id="e7358-115">If you will be performing many searches, consider sorting the results manually on the client side to reduce the workload on the server.</span></span>

<span data-ttu-id="e7358-116">По умолчанию сортировка результатов отключена.</span><span class="sxs-lookup"><span data-stu-id="e7358-116">By default, result sorting is disabled.</span></span> <span data-ttu-id="e7358-117">Чтобы включить сортировку результатов, установите **параметр \_ сеарчпреф \_ Sort \_** by Search с **адстипе \_ Prov \_** , указывающий на структуру [**ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) в массиве ADS, который передается в метод [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . [**\_ \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)</span><span class="sxs-lookup"><span data-stu-id="e7358-117">To enable result sorting, set an **ADS\_SEARCHPREF\_SORT\_ON** search option with an **ADSTYPE\_PROV\_SPECIFIC** that points to an [**ADS\_SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) structure in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="e7358-118">Структура **ADS \_ SORTKEY** используется для указания атрибута, по которому выполняется сортировка, и порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="e7358-118">The **ADS\_SORTKEY** structure is used to specify the attribute to sort on and the order of the sort.</span></span>

<span data-ttu-id="e7358-119">В следующем примере кода показано, как включить сортировку результатов.</span><span class="sxs-lookup"><span data-stu-id="e7358-119">The following code example shows how to enable result sorting.</span></span>


```C++
ADS_SORTKEY SortKey;
SortKey.pszAttrType = L"cn";
SortKey.pszReserved = NULL;
SortKey.fReverseorder = FALSE;

ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SORT_ON;
SearchPref.vValue.dwType = ADSTYPE_PROV_SPECIFIC;
SearchPref.vValue.ProviderSpecific.dwLength = sizeof(SortKey);
SearchPref.vValue.ProviderSpecific.lpValue = (LPBYTE)&SortKey;
```



<span data-ttu-id="e7358-120">Active Directory не поддерживает сортировку сконструированных атрибутов, поэтому невозможно указать сконструированный атрибут для сортировки.</span><span class="sxs-lookup"><span data-stu-id="e7358-120">Active Directory does not support sorting on constructed attributes, so it is not possible to specify a constructed attribute for sorting.</span></span> <span data-ttu-id="e7358-121">Атрибут [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) также нельзя использовать для сортировки.</span><span class="sxs-lookup"><span data-stu-id="e7358-121">The [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) attribute also cannot be used for sorting.</span></span> <span data-ttu-id="e7358-122">Active Directory также не допускает сортировку более чем по одному атрибуту, поэтому параметр **AD \_ сеарчпреф \_ Sort \_ On** Search может содержать только [**\_ одну структуру ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) .</span><span class="sxs-lookup"><span data-stu-id="e7358-122">Active Directory also does not allow sorting on more than one attribute, so the **ADS\_SEARCHPREF\_SORT\_ON** search option can only contain one [**ADS\_SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) structure.</span></span>

 

 