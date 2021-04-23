---
title: Возвращение только имен атрибутов с помощью IDirectorySearch
description: Чтобы определить, какой тип данных доступен для конкретного объекта, можно выполнить поиск.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Возвращение только имен атрибутов с помощью IDirectorySearch ADSI
- ADSI, поиск, IDirectorySearch, другие параметры поиска, возвращающие только имена атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055acbb3fe19969ce95ea77a633e20b195c0257d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654107"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a><span data-ttu-id="e83e3-105">Возвращение только имен атрибутов с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="e83e3-105">Returning Only Attribute Names with IDirectorySearch</span></span>

<span data-ttu-id="e83e3-106">Чтобы определить, какой тип данных доступен для конкретного объекта, можно выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="e83e3-106">You can perform a search to determine what type of data is available for a particular object.</span></span> <span data-ttu-id="e83e3-107">В этом случае вы заинтересованы только в именах атрибутов, а не на значениях атрибутов объекта.</span><span class="sxs-lookup"><span data-stu-id="e83e3-107">In this case, you are only interested in the attributes names, not the attribute values of the object.</span></span> <span data-ttu-id="e83e3-108">Параметр **ADS \_ сеарчпреф \_ аттрибтипес \_ только** указывает, что сервер возвращает только имена атрибутов, а не значения атрибутов.</span><span class="sxs-lookup"><span data-stu-id="e83e3-108">The **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** option causes the server to only return the attribute names and not the attribute values.</span></span> <span data-ttu-id="e83e3-109">Однако результирующий набор включает только те атрибуты, которые имеют присвоенные значения.</span><span class="sxs-lookup"><span data-stu-id="e83e3-109">However, the result set includes only those attributes that have values assigned.</span></span> <span data-ttu-id="e83e3-110">Например, рассмотрим объект со следующими атрибутами:</span><span class="sxs-lookup"><span data-stu-id="e83e3-110">For example, consider an object with the following attributes:</span></span>

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

<span data-ttu-id="e83e3-111">Если установлен параметр " **ADS \_ сеарчпреф \_ аттрибтипес \_** ", результирующий набор включает:</span><span class="sxs-lookup"><span data-stu-id="e83e3-111">When the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** option is set, the result set includes:</span></span>

``` syntax
name
sn
department
phone
```

<span data-ttu-id="e83e3-112">Значение по умолчанию — для возвращаемых значений и имен атрибутов.</span><span class="sxs-lookup"><span data-stu-id="e83e3-112">The default is for both attribute values and names to be returned.</span></span>

<span data-ttu-id="e83e3-113">Чтобы получить только имена атрибутов, установите параметр **ADS \_ сеарчпреф \_ аттрибтипес \_ только** с **\_ логическим значением адстипе** , равным **true** , в массиве [**\_ \_ сведений ADS сеарчпреф**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) , переданном в метод [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="e83e3-113">To retrieve only attribute names, set an **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="e83e3-114">В следующем примере кода показано, как получить только имена атрибутов.</span><span class="sxs-lookup"><span data-stu-id="e83e3-114">The following code example shows how to retrieve attribute names only.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



<span data-ttu-id="e83e3-115">Дополнительные сведения и пример кода, демонстрирующий использование параметра поиска **ADS \_ сеарчпреф \_ аттрибтипес \_ только** , см. в разделе [пример кода для поиска атрибутов](example-code-for-searching-for-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e83e3-115">For more information and a code example that shows how to use the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search option, see [Example Code for Searching for Attributes](example-code-for-searching-for-attributes.md).</span></span>

 

 




