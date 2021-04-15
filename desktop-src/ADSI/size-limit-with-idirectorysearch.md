---
title: Ограничение размера с IDirectorySearch
description: Клиент может сосредоточиться на небольшом количестве объектов, возвращаемых с сервера, и игнорировать оставшуюся часть результирующего набора.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Ограничение размера с помощью IDirectorySearch ADSI
- ADSI, поиск, IDirectorySearch, другие параметры поиска, предельный размер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25127ea945edcf669e71d7d5b3f969d9eb2cb112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654102"
---
# <a name="size-limit-with-idirectorysearch"></a><span data-ttu-id="39553-105">Ограничение размера с IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="39553-105">Size Limit with IDirectorySearch</span></span>

<span data-ttu-id="39553-106">Чтобы уменьшить потребность в памяти или в других целях, клиент может сосредоточиться на небольшом количестве объектов, возвращаемых с сервера, и игнорировать оставшуюся часть результирующего набора, который не является нужным.</span><span class="sxs-lookup"><span data-stu-id="39553-106">To reduce the memory requirement or for other purposes, the client can focus on a small number of objects returned from the server and ignore the rest of the result set that are not of interest.</span></span> <span data-ttu-id="39553-107">Для этого клиент указывает предельный размер поиска и другие соответствующие условия поиска.</span><span class="sxs-lookup"><span data-stu-id="39553-107">To accomplish this, the client specifies the search size limit and other appropriate search criteria.</span></span> <span data-ttu-id="39553-108">Например, если в каталоге хранятся результаты тестирования учебного района, можно запросить Десять ведущих учащихся с самыми высокими показателями тестирования, указав предельный размер в десять (10) и сортировку по убыванию.</span><span class="sxs-lookup"><span data-stu-id="39553-108">For example, if the directory stores the test scores of a school district, you can query the top ten students with the highest test scores by specifying a size limit of ten (10) and a descending sort order.</span></span>

<span data-ttu-id="39553-109">Значение по умолчанию для ограничения размера не ограничено.</span><span class="sxs-lookup"><span data-stu-id="39553-109">The default for size limit is no limit.</span></span> <span data-ttu-id="39553-110">Чтобы задать предельный размер, задайте для параметра поиска **\_ Сеарчпреф \_ размер \_ ADS** значение **\_ целого числа адстипе** , которое содержит максимальный размер в массиве [**\_ \_ сведений об ADS сеарчпреф**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) , переданном в метод [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="39553-110">To set a size limit, set an **ADS\_SEARCHPREF\_SIZE\_LIMIT** search option with an **ADSTYPE\_INTEGER** value that contains the maximum size in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="39553-111">В следующем примере кода показано, как задать предельный размер.</span><span class="sxs-lookup"><span data-stu-id="39553-111">The following code example shows how to set the size limit.</span></span> <span data-ttu-id="39553-112">Значение предельного размера, равное нулю, указывает на отсутствие ограничения по размеру.</span><span class="sxs-lookup"><span data-stu-id="39553-112">A size limit value of zero indicates no size limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



<span data-ttu-id="39553-113">Для Active Directory ограничение размера определяет максимальное число объектов, возвращаемых при поиске.</span><span class="sxs-lookup"><span data-stu-id="39553-113">For Active Directory, the size limit specifies the maximum number of objects to be returned by the search.</span></span> <span data-ttu-id="39553-114">Кроме того, для Active Directory максимальное количество объектов, возвращаемых функцией поиска, — 1000.</span><span class="sxs-lookup"><span data-stu-id="39553-114">Also for Active Directory, the maximum number of objects returned by a search is 1000 objects.</span></span>

 

 




