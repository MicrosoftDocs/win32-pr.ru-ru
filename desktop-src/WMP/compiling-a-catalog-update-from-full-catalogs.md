---
title: Компиляция обновления каталога из полных каталогов
description: Компиляция обновления каталога из полных каталогов
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Интернет-магазины проигрывателя Windows Media, компиляция каталогов
- Интернет-магазины, компиляция каталогов
- Тип 1 Интернет-магазины, компиляция каталогов
- Интернет-магазины проигрывателя Windows Media, обновления каталога
- Интернет-магазины, обновления каталога
- Тип 1 Интернет-магазины, обновления каталога
- Интернет-магазины проигрывателя Windows Media, полные каталоги
- Интернет-магазины, полные каталоги
- Тип 1 Интернет-магазины, полные каталоги
- Компиляция каталогов
- обновления каталога
- полные каталоги
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaa6d1bc0d3dbc4fefaffe1498be03259716a5e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336247"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a><span data-ttu-id="72afa-115">Компиляция обновления каталога из полных каталогов</span><span class="sxs-lookup"><span data-stu-id="72afa-115">Compiling a Catalog Update from Full Catalogs</span></span>

<span data-ttu-id="72afa-116">Обновление каталога, содержащее изменения между двумя версиями скомпилированного каталога, можно создать с помощью приведенного ниже синтаксиса, где *path1* — каталог, содержащий первый каталог, *path2* — это каталог, содержащий второй каталог, а для отображения подробных сведений об ошибках на экране можно дополнительно включить отладку.</span><span class="sxs-lookup"><span data-stu-id="72afa-116">A catalog update containing the changes between two versions of a compiled catalog can be created by using the syntax below, where *path1* is the directory containing the first catalog, *path2* is the directory containing the second catalog, and debug can be optionally included to display detailed error information on the screen.</span></span> <span data-ttu-id="72afa-117">Файлы каталога должны быть в несжатом виде — имя файла скомпилированного каталога будет Catalog. вмдб, а не Catalog. вмдб. LZ.</span><span class="sxs-lookup"><span data-stu-id="72afa-117">The catalog files must be in uncompressed form—the file name of the compiled catalog would be catalog.wmdb, rather than catalog.wmdb.lz.</span></span>


```C++
catcomp diff <path1> <path2> [debug]
```



<span data-ttu-id="72afa-118">Например, если каталог C: \\ Catalog210 \\ содержит версию 210 полного скомпилированного каталога и C: \\ Catalog211 \\ содержит версию 211, то следующая команда создает файл различий, содержащий изменения между двумя версиями:</span><span class="sxs-lookup"><span data-stu-id="72afa-118">For example, if the C:\\Catalog210\\ directory contains version 210 of a full compiled catalog and C:\\Catalog211\\ contains version 211, the following command creates a difference file that contains the changes between the two versions:</span></span>


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



<span data-ttu-id="72afa-119">Чтобы отобразить подробные сведения об ошибке, можно добавить необязательный параметр отладки следующим образом:</span><span class="sxs-lookup"><span data-stu-id="72afa-119">To display detailed error information, you can add the optional debug parameter as follows:</span></span>


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



<span data-ttu-id="72afa-120">Если компиляция прошла успешно, catcomp.exe создает указанные ниже выходные файлы и сохраняет их в каталоге, содержащем первый каталог.</span><span class="sxs-lookup"><span data-stu-id="72afa-120">If compilation is successful, catcomp.exe creates the output files listed below and saves them in the directory that contains the first catalog.</span></span>



| <span data-ttu-id="72afa-121">Имя файла</span><span class="sxs-lookup"><span data-stu-id="72afa-121">File name</span></span>             | <span data-ttu-id="72afa-122">Описание</span><span class="sxs-lookup"><span data-stu-id="72afa-122">Description</span></span>                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72afa-123">Catalog. diff</span><span class="sxs-lookup"><span data-stu-id="72afa-123">catalog.diff</span></span>          | <span data-ttu-id="72afa-124">Несжатый скомпилированный файл различий.</span><span class="sxs-lookup"><span data-stu-id="72afa-124">Uncompressed compiled difference file.</span></span>                                                                                                                                                           |
| <span data-ttu-id="72afa-125">Catalog. diff. LZ</span><span class="sxs-lookup"><span data-stu-id="72afa-125">catalog.diff.lz</span></span>       | <span data-ttu-id="72afa-126">Сжатая версия файла обновления каталога.</span><span class="sxs-lookup"><span data-stu-id="72afa-126">Compressed version of catalog update file.</span></span> <span data-ttu-id="72afa-127">Подключаемый модуль может передать расположение этого файла в проигрыватель Windows Media в [ивмпконтентпартнер:: жеткаталогурл](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="72afa-127">Your plug-in can give the location of this file to Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> |
| <span data-ttu-id="72afa-128">Catalog. вмдб. Дельта</span><span class="sxs-lookup"><span data-stu-id="72afa-128">catalog.wmdb.delta</span></span>    | <span data-ttu-id="72afa-129">Промежуточный выходной файл.</span><span class="sxs-lookup"><span data-stu-id="72afa-129">Intermediate output file.</span></span> <span data-ttu-id="72afa-130">Не используется проигрывателем Windows Media</span><span class="sxs-lookup"><span data-stu-id="72afa-130">Not used by Windows Media Player</span></span>                                                                                                                                       |
| <span data-ttu-id="72afa-131">Catalog. вмдб. Modified</span><span class="sxs-lookup"><span data-stu-id="72afa-131">catalog.wmdb.modified</span></span> | <span data-ttu-id="72afa-132">Промежуточный выходной файл.</span><span class="sxs-lookup"><span data-stu-id="72afa-132">Intermediate output file.</span></span> <span data-ttu-id="72afa-133">Не используется проигрывателем Windows Media</span><span class="sxs-lookup"><span data-stu-id="72afa-133">Not used by Windows Media Player</span></span>                                                                                                                                       |



 

 

 




