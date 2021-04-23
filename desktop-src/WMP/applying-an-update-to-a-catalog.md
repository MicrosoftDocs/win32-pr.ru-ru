---
title: Применение обновления к каталогу
description: Применение обновления к каталогу
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Интернет-магазины проигрывателя Windows Media, применение обновлений к каталогам
- Интернет-магазины, применение обновлений к каталогам
- Тип 1 Интернет-магазины, применение обновлений к каталогам
- Интернет-магазины проигрывателя Windows Media, обновление каталогов
- Интернет-магазины, обновление каталогов
- Тип 1 Интернет-магазины, обновление каталогов
- Интернет-магазины проигрывателя Windows Media, обновления каталога
- Интернет-магазины, обновления каталога
- Тип 1 Интернет-магазины, обновления каталога
- обновления каталога
- Обновление каталогов
- применение обновлений к каталогам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d468edb7d09b8804fa924f7c31fc1be45d27c8fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691382"
---
# <a name="applying-an-update-to-a-catalog"></a><span data-ttu-id="b3415-115">Применение обновления к каталогу</span><span class="sxs-lookup"><span data-stu-id="b3415-115">Applying an Update To a Catalog</span></span>

> [!Note]  
> <span data-ttu-id="b3415-116">Это обычно не выполняется, за исключением целей диагностики — например, для проверки допустимости файла различий.</span><span class="sxs-lookup"><span data-stu-id="b3415-116">This is not normally done except for diagnostic purposes—for instance, to help verify that a difference file is valid.</span></span> <span data-ttu-id="b3415-117">Каталог, созданный таким образом, не сжат в форме и не должен передаваться проигрывателю Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b3415-117">The catalog generated in this way is not in compressed form and should not be passed to Windows Media Player.</span></span>

 

<span data-ttu-id="b3415-118">Новый файл каталога можно создать с помощью приведенного ниже синтаксиса, где *инпуткаталог* — это расположение исходного каталога, а *инпутдифф* — расположение файла различий для применения.</span><span class="sxs-lookup"><span data-stu-id="b3415-118">A new catalog file can be created by using the syntax below, where *inputcatalog* is the location of the original catalog, and *inputdiff* is the location of the difference file to apply.</span></span> <span data-ttu-id="b3415-119">Файлы каталога должны быть в несжатом виде.</span><span class="sxs-lookup"><span data-stu-id="b3415-119">The catalog files must be in uncompressed form.</span></span>


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



<span data-ttu-id="b3415-120">Например, в следующем примере создается новый каталог из C: \\ Catalog210 \\ Catalog. Вмдб и C: \\ Catalog210 \\ Catalog. diff.</span><span class="sxs-lookup"><span data-stu-id="b3415-120">For example, the following creates a new catalog from C:\\Catalog210\\catalog.wmdb and C:\\Catalog210\\catalog.diff.</span></span>


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



<span data-ttu-id="b3415-121">Если компиляция прошла успешно, catcomp.exe создает следующие выходные файлы.</span><span class="sxs-lookup"><span data-stu-id="b3415-121">If compilation is successful, catcomp.exe creates the follow output files.</span></span>



| <span data-ttu-id="b3415-122">Имя файла</span><span class="sxs-lookup"><span data-stu-id="b3415-122">File name</span></span>        | <span data-ttu-id="b3415-123">Описание</span><span class="sxs-lookup"><span data-stu-id="b3415-123">Description</span></span>       |
|------------------|-------------------|
| <span data-ttu-id="b3415-124">Catalog. вмдб. New</span><span class="sxs-lookup"><span data-stu-id="b3415-124">catalog.wmdb.new</span></span> | <span data-ttu-id="b3415-125">Новый файл каталога.</span><span class="sxs-lookup"><span data-stu-id="b3415-125">New catalog file.</span></span> |



 

 

 




