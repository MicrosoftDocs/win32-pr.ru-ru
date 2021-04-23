---
title: Получение диапазона атрибутов
description: Атрибут с несколькими значениями может иметь почти любое количество значений. Во многих случаях может оказаться целесообразным или даже необходимым для ограничения диапазона значений, извлекаемых запросом.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- Получение диапазона атрибутов ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8787eb0b2aba30d1926b4d9cbb7e566e0f59c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986119"
---
# <a name="attribute-range-retrieval"></a><span data-ttu-id="8599f-105">Получение диапазона атрибутов</span><span class="sxs-lookup"><span data-stu-id="8599f-105">Attribute Range Retrieval</span></span>

<span data-ttu-id="8599f-106">Атрибут с несколькими значениями может иметь почти любое количество значений.</span><span class="sxs-lookup"><span data-stu-id="8599f-106">A multi-valued attribute can have almost any number of values.</span></span> <span data-ttu-id="8599f-107">Во многих случаях может оказаться целесообразным или даже необходимым для ограничения диапазона значений, извлекаемых запросом.</span><span class="sxs-lookup"><span data-stu-id="8599f-107">In many cases, it may be advantageous, or even necessary, to limit the range of values that are retrieved by a query.</span></span>

<span data-ttu-id="8599f-108">Извлечение диапазона включает в себя запрос ограниченного числа значений атрибутов в одном запросе.</span><span class="sxs-lookup"><span data-stu-id="8599f-108">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="8599f-109">Количество запрошенных значений должно быть меньше или равно максимальному количеству значений, поддерживаемых сервером.</span><span class="sxs-lookup"><span data-stu-id="8599f-109">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="8599f-110">Чтобы сократить количество обращений запроса к серверу, количество запрошенных значений должно быть максимально близко к максимальному.</span><span class="sxs-lookup"><span data-stu-id="8599f-110">To reduce the number of times the query must contact the server, the number of values requested should be as close to this maximum as possible.</span></span> <span data-ttu-id="8599f-111">Чтобы обеспечить правильную работу приложения со всеми серверами Windows, следует использовать максимальное число 1000.</span><span class="sxs-lookup"><span data-stu-id="8599f-111">To enable an application to work correctly with all Windows servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="8599f-112">Описатели диапазона для запроса свойства должны иметь следующую форму:</span><span class="sxs-lookup"><span data-stu-id="8599f-112">The range specifiers for a property query require the following form:</span></span>


```C++
range=<low range>-<high range>
```



<span data-ttu-id="8599f-113">где " &lt; младший диапазон &gt; " — Отсчитываемый от нуля индекс первого значения свойства для извлечения, а " &lt; Верхний диапазон &gt; " — Отсчитываемый от нуля индекс последнего значения свойства, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="8599f-113">where "&lt;low range&gt;" is the zero-based index of the first property value to retrieve and "&lt;high range&gt;" is the zero-based index of the last property value to retrieve.</span></span> <span data-ttu-id="8599f-114">Ноль используется для " &lt; неограниченный диапазон &gt; " для указания первой записи.</span><span class="sxs-lookup"><span data-stu-id="8599f-114">Zero is used for "&lt;low range&gt;" to specify the first entry.</span></span> <span data-ttu-id="8599f-115">Подстановочный знак ( \* ) можно использовать для " &lt; верхнего диапазона &gt; ", чтобы указать все оставшиеся записи.</span><span class="sxs-lookup"><span data-stu-id="8599f-115">The wildcard character (\*) can be used for "&lt;high range&gt;" to specify all remaining entries.</span></span>

<span data-ttu-id="8599f-116">В следующей таблице приведены примеры описателей диапазонов.</span><span class="sxs-lookup"><span data-stu-id="8599f-116">The following table lists examples of range specifiers.</span></span>



| <span data-ttu-id="8599f-117">Пример</span><span class="sxs-lookup"><span data-stu-id="8599f-117">Example</span></span>      | <span data-ttu-id="8599f-118">Описание</span><span class="sxs-lookup"><span data-stu-id="8599f-118">Description</span></span>                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8599f-119">Range = 0-\*</span><span class="sxs-lookup"><span data-stu-id="8599f-119">range=0-\*</span></span>   | <span data-ttu-id="8599f-120">Получение всех значений свойств.</span><span class="sxs-lookup"><span data-stu-id="8599f-120">Retrieve all property values.</span></span> <span data-ttu-id="8599f-121">Это зависит от ограничений, наложенных сервером.</span><span class="sxs-lookup"><span data-stu-id="8599f-121">This is subject to limits imposed by the server.</span></span>                |
| <span data-ttu-id="8599f-122">Range = 0 – 500</span><span class="sxs-lookup"><span data-stu-id="8599f-122">range=0-500</span></span>  | <span data-ttu-id="8599f-123">Извлеките из 1-го в 501st значения включительно.</span><span class="sxs-lookup"><span data-stu-id="8599f-123">Retrieve from 1st to 501st values inclusively.</span></span>                                                |
| <span data-ttu-id="8599f-124">диапазон = 2 – 3</span><span class="sxs-lookup"><span data-stu-id="8599f-124">range=2-3</span></span>    | <span data-ttu-id="8599f-125">Получение значений 3 и 4.</span><span class="sxs-lookup"><span data-stu-id="8599f-125">Retrieve 3rd and 4th values.</span></span>                                                                  |
| <span data-ttu-id="8599f-126">диапазон = 501-\*</span><span class="sxs-lookup"><span data-stu-id="8599f-126">range=501-\*</span></span> | <span data-ttu-id="8599f-127">Получение 502nd и всех оставшихся значений.</span><span class="sxs-lookup"><span data-stu-id="8599f-127">Retrieve the 502nd and all remaining values.</span></span> <span data-ttu-id="8599f-128">Это зависит от ограничений, наложенных сервером.</span><span class="sxs-lookup"><span data-stu-id="8599f-128">This is subject to limits imposed by the server.</span></span> |



 

<span data-ttu-id="8599f-129">Существует несколько различных способов получения диапазона значений свойств.</span><span class="sxs-lookup"><span data-stu-id="8599f-129">There are several different ways to retrieve a range of property values.</span></span> <span data-ttu-id="8599f-130">Метод [**iAds. жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) можно использовать как на языке автоматизации, так и в C++.</span><span class="sxs-lookup"><span data-stu-id="8599f-130">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method can be used in either an automation language or C++.</span></span> <span data-ttu-id="8599f-131">Метод **iAds. жетинфоекс** является предпочтительным способом выполнения извлечения диапазона.</span><span class="sxs-lookup"><span data-stu-id="8599f-131">The **IADs.GetInfoEx** method is the preferred method of performing range retrieval.</span></span> <span data-ttu-id="8599f-132">Дополнительные сведения об использовании метода **iAds. жетинфоекс** для получения диапазона см. в разделе [Использование функции iAds:: Жетинфоекс для получения диапазона](using-iads--getinfoex-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="8599f-132">For more information about using **IADs.GetInfoEx** for range retrieval, see [Using IADs::GetInfoEx for Range Retrieval](using-iads--getinfoex-for-range-retrieval.md).</span></span>

<span data-ttu-id="8599f-133">Если используется язык автоматизации, то для получения диапазона значений свойств можно использовать объекты каталогов ActiveX (ADO).</span><span class="sxs-lookup"><span data-stu-id="8599f-133">If an automation language is used, the ActiveX Directory Objects (ADO) can be used to retrieve a range of property values.</span></span> <span data-ttu-id="8599f-134">Дополнительные сведения об использовании ADO для получения диапазона см. в разделе [Использование ADO для получения диапазона](using-ado-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="8599f-134">For more information about using ADO for range retrieval, see [Using ADO for Range Retrieval](using-ado-for-range-retrieval.md).</span></span>

<span data-ttu-id="8599f-135">Если используется C++, интерфейсы [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) и [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) можно использовать для получения диапазона значений свойств.</span><span class="sxs-lookup"><span data-stu-id="8599f-135">If C++ is used, the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) and [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interfaces can be used to retrieve a range of property values.</span></span> <span data-ttu-id="8599f-136">Дополнительные сведения об использовании **IDirectorySearch** и **идиректорйобжект** для извлечения диапазона см. в разделе [Использование IDirectorySearch и идиректорйобжект для получения диапазона](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="8599f-136">For more information about using **IDirectorySearch** and **IDirectoryObject** for range retrieval, see [Using IDirectorySearch and IDirectoryObject for Range Retrieval](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).</span></span>

 

 




