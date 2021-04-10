---
title: Подкачка с помощью IDirectorySearch
description: Подкачка указывает количество строк, возвращаемых сервером клиенту.
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- Подкачка с помощью IDirectorySearch ADSI
- ADSI, поиск, IDirectorySearch, другие параметры поиска, разбиение на страницы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e9fdf001f5908f6c3fc7321c8c94cda09f1b96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986096"
---
# <a name="paging-with-idirectorysearch"></a><span data-ttu-id="add49-105">Подкачка с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="add49-105">Paging with IDirectorySearch</span></span>

<span data-ttu-id="add49-106">Подкачка указывает количество строк, возвращаемых сервером клиенту.</span><span class="sxs-lookup"><span data-stu-id="add49-106">Paging specifies how many rows that the server returns to the client.</span></span> <span data-ttu-id="add49-107">Страница может быть определена числом строк или ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="add49-107">A page can be defined by the number of rows or a time limit.</span></span> <span data-ttu-id="add49-108">COM-объект ADSI извлекает каждую страницу результатов на основе значений, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="add49-108">The ADSI COM object retrieves each page of results based on the values listed in the following table.</span></span> <span data-ttu-id="add49-109">Вызывающий объект вызывает [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) , когда он достиг конца страницы, а COM-объект ADSI извлекает следующую страницу.</span><span class="sxs-lookup"><span data-stu-id="add49-109">The caller calls [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) when it has reached the page end, and the ADSI COM object retrieves the next page.</span></span>



| <span data-ttu-id="add49-110">Значение</span><span class="sxs-lookup"><span data-stu-id="add49-110">Value</span></span>                                   | <span data-ttu-id="add49-111">Описание</span><span class="sxs-lookup"><span data-stu-id="add49-111">Description</span></span>                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="add49-112">**ADS \_ сеарчпреф \_ PAGESIZE**</span><span class="sxs-lookup"><span data-stu-id="add49-112">**ADS\_SEARCHPREF\_PAGESIZE**</span></span>           | <span data-ttu-id="add49-113">Указывает максимальное число строк, возвращаемых на странице.</span><span class="sxs-lookup"><span data-stu-id="add49-113">Specifies the maximum number of rows to return in a page.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="add49-114">**ADS \_ сеарчпреф \_ предел времени в выгружаемом страничном \_ периоде \_**</span><span class="sxs-lookup"><span data-stu-id="add49-114">**ADS\_SEARCHPREF\_PAGED\_TIME\_LIMIT**</span></span> | <span data-ttu-id="add49-115">Указывает максимальное время в секундах, которое сервер должен тратить на сбор страниц результатов, прежде чем возвратить страницу клиенту.</span><span class="sxs-lookup"><span data-stu-id="add49-115">Specifies the maximum time, in seconds, that the server should spend collecting a page of results before returning the page to the client.</span></span> <span data-ttu-id="add49-116">Если достигнут предел, сервер останавливает Поиск и возвращает строки, уже извлеченные для страницы.</span><span class="sxs-lookup"><span data-stu-id="add49-116">If the limit is reached, the server stops the search and returns the rows already retrieved for the page.</span></span> |



 

<span data-ttu-id="add49-117">Если ни одно из этих параметров поиска не задано, по умолчанию используется значение без подкачки.</span><span class="sxs-lookup"><span data-stu-id="add49-117">If neither of these search preferences is set, the default is no paging.</span></span> <span data-ttu-id="add49-118">Поиск Active Directory, выполненных без разбиения по страницам, ограничивается возвратом максимального числа первых 1000 записей, поэтому необходимо использовать страничный поиск, если существует вероятность того, что результирующий набор будет содержать более 1000 элементов.</span><span class="sxs-lookup"><span data-stu-id="add49-118">Searches of the Active Directory performed without paging are limited to returning a maximum of the first 1000 records, so you must use a paged search if there is the possibility that the result set will contain more than 1000 items.</span></span>

<span data-ttu-id="add49-119">Операция поиска может привести к возвращению большого количества объектов.</span><span class="sxs-lookup"><span data-stu-id="add49-119">A search operation may result in a large number of objects being returned.</span></span> <span data-ttu-id="add49-120">Если сервер возвращает результат в одном наборе, он может снизить производительность клиента и сервера, а также повлиять на сетевую нагрузку.</span><span class="sxs-lookup"><span data-stu-id="add49-120">If the server returns the result in one set, it could decrease the performance of the client and server, as well as affect the network load.</span></span> <span data-ttu-id="add49-121">Чтобы предотвратить это, можно использовать страничные поисковые запросы.</span><span class="sxs-lookup"><span data-stu-id="add49-121">Paged searches can be used to prevent this.</span></span> <span data-ttu-id="add49-122">При поиске с постраничным поиском клиент может принимать результаты в меньшем объеме пакетов.</span><span class="sxs-lookup"><span data-stu-id="add49-122">In a paged search, the client can accept results in smaller packets.</span></span> <span data-ttu-id="add49-123">Размер пакета называется размером страницы поиска.</span><span class="sxs-lookup"><span data-stu-id="add49-123">The size of a packet is known as the search page size.</span></span>

<span data-ttu-id="add49-124">Страничные поисковые запросы предлагают преимущества как клиенту, так и серверу.</span><span class="sxs-lookup"><span data-stu-id="add49-124">Paged searches offer benefits to both the client and the server.</span></span> <span data-ttu-id="add49-125">Клиент может более быстро реагировать на представление результатов для пользователей.</span><span class="sxs-lookup"><span data-stu-id="add49-125">The client can be more responsive in presenting the results to users.</span></span> <span data-ttu-id="add49-126">Это особенно важно для графических средств пользовательского интерфейса, которые могут начать процесс вывода окна, пока другой поток одновременно получает данные.</span><span class="sxs-lookup"><span data-stu-id="add49-126">This is especially relevant to graphical user interface tools that can begin the window display process while the other thread concurrently receives the data.</span></span>

<span data-ttu-id="add49-127">На стороне сервера страничные поисковые запросы делают операцию масштабируемой.</span><span class="sxs-lookup"><span data-stu-id="add49-127">On the server side, paged searches make the operation scalable.</span></span> <span data-ttu-id="add49-128">Например, если 100 Клиенты выдают запросы на поиск одновременно и, в среднем, каждый клиент получает 200 объектов.</span><span class="sxs-lookup"><span data-stu-id="add49-128">For example, if one hundred clients issue search requests simultaneously and, on the average, each client receives two hundred objects.</span></span> <span data-ttu-id="add49-129">Если размер страницы не указан, в худшем случае сервер должен иметь достаточный объем памяти для хранения объектов 20 000.</span><span class="sxs-lookup"><span data-stu-id="add49-129">If no page size is specified, in the worst-case scenario, the server must have sufficient memory to hold 20,000 objects.</span></span> <span data-ttu-id="add49-130">И наоборот, если каждый клиент указывает размер страницы, например десять объектов, потребность в памяти на сервере сокращается до 20.</span><span class="sxs-lookup"><span data-stu-id="add49-130">Conversely, if each client specifies a page size to be, for example, ten objects, the memory requirement on the server is thus reduced by a factor of 20.</span></span>

<span data-ttu-id="add49-131">Кроме того, с помощью страничного поиска клиент может отказаться от выполняемой операции.</span><span class="sxs-lookup"><span data-stu-id="add49-131">In addition, using a paged search, a client can abandon the operation in progress.</span></span> <span data-ttu-id="add49-132">В отличие от этого, в нестраничном поиске клиент получает результирующий набор в одном пакете.</span><span class="sxs-lookup"><span data-stu-id="add49-132">In contrast, in a non-paged search, the client receives a result set in one packet.</span></span> <span data-ttu-id="add49-133">Это может снизить производительность сети.</span><span class="sxs-lookup"><span data-stu-id="add49-133">This can decrease network performance.</span></span>

<span data-ttu-id="add49-134">ADSI обрабатывает размер страницы для клиента.</span><span class="sxs-lookup"><span data-stu-id="add49-134">ADSI handles the page size for the client.</span></span> <span data-ttu-id="add49-135">Клиенту не нужно подсчитывать количество выполняемых объектов.</span><span class="sxs-lookup"><span data-stu-id="add49-135">The client does not have to count the number of objects in progress.</span></span> <span data-ttu-id="add49-136">ADSI инкапсулирует взаимодействие сервера для клиента.</span><span class="sxs-lookup"><span data-stu-id="add49-136">ADSI encapsulates the server interaction for the client.</span></span> <span data-ttu-id="add49-137">С точки зрения клиента, поиск возвращает полный результирующий набор.</span><span class="sxs-lookup"><span data-stu-id="add49-137">From the client perspective, the search returns a complete result set.</span></span>

<span data-ttu-id="add49-138">Рекомендуется использовать разбиение на страницы.</span><span class="sxs-lookup"><span data-stu-id="add49-138">It is recommended that paging is used.</span></span>

<span data-ttu-id="add49-139">Чтобы указать максимальный размер страницы, задайте для параметра **поиска ADS \_ сеарчпреф \_ PAGESIZE** значение **адстипе \_ Integer** , равное максимальному количеству строк на страницу в массиве [**\_ \_ сведений об ADS сеарчпреф**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) , переданном в метод [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="add49-139">To specify a maximum page size, set an **ADS\_SEARCHPREF\_PAGESIZE** search option with an **ADSTYPE\_INTEGER** value set to the maximum number of rows per page in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="add49-140">В следующем примере кода показано, как задать максимальный размер страницы.</span><span class="sxs-lookup"><span data-stu-id="add49-140">The following code example shows how to set the maximum page size.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



<span data-ttu-id="add49-141">Чтобы указать время страницы, задайте для параметра **поиска ADS \_ сеарчпреф \_ страничного \_ \_ ограничения по времени** с **\_ целочисленным значением адстипе** значение, равное максимальному числу секунд, которое сервер должен потратить на получение страницы в массиве [**\_ \_ сведений об ADS сеарчпреф**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) , переданном в метод [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="add49-141">To specify a page time, set an **ADS\_SEARCHPREF\_PAGED\_TIME\_LIMIT** search option with an **ADSTYPE\_INTEGER** value set to the maximum number of seconds that the server should spend retrieving a page in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="add49-142">В следующем примере кода показано, как задать время страницы.</span><span class="sxs-lookup"><span data-stu-id="add49-142">The following code example shows how to specify page time.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




