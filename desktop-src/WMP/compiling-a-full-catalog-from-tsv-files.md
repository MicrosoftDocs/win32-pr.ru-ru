---
title: Компиляция полного каталога из TSV-файлов
description: Компиляция полного каталога из TSV-файлов
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Интернет-магазины проигрывателя Windows Media, компиляция каталогов
- Интернет-магазины, компиляция каталогов
- Тип 1 Интернет-магазины, компиляция каталогов
- Интернет-магазины проигрывателя Windows Media в Интернете, файлы TSV
- Интерактивные магазины, TSV-файлы
- Тип 1 Online Stores, TSV-файлы
- Интернет-магазины проигрывателя Windows Media, catcomp.exe
- Интернет-магазины, catcomp.exe
- Введите 1 Интернет-магазины, catcomp.exe
- catcomp.exe
- Компиляция каталогов
- файлы с разделителями-табуляторами (TSV)
- Файлы TSV (с разделителями-табуляторами-значениями)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b68af019a5e2302f52f615d5a1dba2180e27cfe5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691436"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a><span data-ttu-id="8a3c0-116">Компиляция полного каталога из TSV-файлов</span><span class="sxs-lookup"><span data-stu-id="8a3c0-116">Compiling a Full Catalog from TSV Files</span></span>

<span data-ttu-id="8a3c0-117">Новые каталоги создаются из набора файлов с разделителями-табуляциями (TSV).</span><span class="sxs-lookup"><span data-stu-id="8a3c0-117">New catalogs are created from a set of tab-separated-value (TSV) files.</span></span> <span data-ttu-id="8a3c0-118">Файлы должны быть в формате Юникода.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-118">The files must be in Unicode format.</span></span> <span data-ttu-id="8a3c0-119">Поместите необходимые TSV-файлы в папку (аргумент пути входа в catcomp.exe) и вызовите catcomp.exe, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="8a3c0-119">Place the required TSV files listed below into a folder (the input path argument to catcomp.exe), and call catcomp.exe using the following syntax:</span></span>


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



<span data-ttu-id="8a3c0-120">Если номер версии не указан, номер версии будет установлен в 0.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-120">If a version number is not provided, the version number will be set to 0.</span></span> <span data-ttu-id="8a3c0-121">Если код локали не указан, используется национальная настройка системы.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-121">If no locale ID is provided, the system locale is used.</span></span> <span data-ttu-id="8a3c0-122">Если указан только один числовой необязательный аргумент, предполагается, что это номер версии.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-122">If only one numeric optional argument is provided, it is assumed to be the version number.</span></span> <span data-ttu-id="8a3c0-123">Если указан параметр debug, выходные данные на экране будут предоставлять более подробные диагностические сведения.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-123">If debug is specified, the output to the screen will provide more detailed diagnostic information.</span></span>

<span data-ttu-id="8a3c0-124">Например, следующий код компилирует каталог из файлов в C: \\ каталогдата \\ 210 и присваивает каталогу номер версии 210:</span><span class="sxs-lookup"><span data-stu-id="8a3c0-124">For example, the following will compile a catalog from the files in C:\\CatalogData\\210 and give the catalog a version number of 210:</span></span>


```C++
catcomp C:\CatalogData\210 210
```



<span data-ttu-id="8a3c0-125">Чтобы отобразить более подробные сообщения об ошибках, можно добавить необязательный аргумент Debug, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-125">To display more detailed error messages, the optional debug argument can be added, as follows:</span></span>


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a><span data-ttu-id="8a3c0-126">Требуемые TSV файлы</span><span class="sxs-lookup"><span data-stu-id="8a3c0-126">Required TSV Files</span></span>

<span data-ttu-id="8a3c0-127">Каждый из следующих файлов должен присутствовать, но при отсутствии данных для файла можно использовать пустой файл.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-127">Each of the following files must be present, but an empty file can be used if there is no data for a file.</span></span> <span data-ttu-id="8a3c0-128">Например, если каталог не содержит радиоканалов, radio.csv может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-128">For instance, if your catalog contains no radio channels, radio.csv can be empty.</span></span> <span data-ttu-id="8a3c0-129">Файлы должны называться в точности так, как указано.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-129">The files must be named exactly as listed.</span></span>

[<span data-ttu-id="8a3c0-130">track.csv</span><span class="sxs-lookup"><span data-stu-id="8a3c0-130">track.csv</span></span>](track-csv.md)

[<span data-ttu-id="8a3c0-131">album.csv</span><span class="sxs-lookup"><span data-stu-id="8a3c0-131">album.csv</span></span>](album-csv.md)

[<span data-ttu-id="8a3c0-132">artist.csv</span><span class="sxs-lookup"><span data-stu-id="8a3c0-132">artist.csv</span></span>](artist-csv.md)

[<span data-ttu-id="8a3c0-133">genre.csv</span><span class="sxs-lookup"><span data-stu-id="8a3c0-133">genre.csv</span></span>](genre-csv.md)

[<span data-ttu-id="8a3c0-134">subgenre.csv</span><span class="sxs-lookup"><span data-stu-id="8a3c0-134">subgenre.csv</span></span>](subgenre-csv.md)

[<span data-ttu-id="8a3c0-135">list.csv</span><span class="sxs-lookup"><span data-stu-id="8a3c0-135">list.csv</span></span>](list-csv.md)

[<span data-ttu-id="8a3c0-136">listitem.csv</span><span class="sxs-lookup"><span data-stu-id="8a3c0-136">listitem.csv</span></span>](listitem-csv.md)

[<span data-ttu-id="8a3c0-137">radio.csv</span><span class="sxs-lookup"><span data-stu-id="8a3c0-137">radio.csv</span></span>](radio-csv.md)

> [!Note]  
> <span data-ttu-id="8a3c0-138">Несмотря на то, что имена файлов должны иметь расширения CSV, файлы не находятся в формате CSV.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-138">Although the file names must have .csv extensions, the files are not in Comma Separated Values (CSV) format.</span></span> <span data-ttu-id="8a3c0-139">Файлы должны быть в формате с разделителями табуляцией (TSV).</span><span class="sxs-lookup"><span data-stu-id="8a3c0-139">The files must be in Tab Separated Values (TSV) format.</span></span>

 

<span data-ttu-id="8a3c0-140">Если компиляция прошла успешно, catcomp.exe создает три выходных файла.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-140">If compilation is successful, catcomp.exe creates three output files.</span></span>



| <span data-ttu-id="8a3c0-141">Имя файла</span><span class="sxs-lookup"><span data-stu-id="8a3c0-141">File name</span></span>                   | <span data-ttu-id="8a3c0-142">Описание</span><span class="sxs-lookup"><span data-stu-id="8a3c0-142">Description</span></span>                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a3c0-143">Catalog. вмдб</span><span class="sxs-lookup"><span data-stu-id="8a3c0-143">catalog.wmdb</span></span>                | <span data-ttu-id="8a3c0-144">Несжатый скомпилированный каталог.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-144">Uncompressed compiled catalog.</span></span>                                                                                                                                                      |
| <span data-ttu-id="8a3c0-145">Catalog. вмдб. LZ</span><span class="sxs-lookup"><span data-stu-id="8a3c0-145">catalog.wmdb.lz</span></span>             | <span data-ttu-id="8a3c0-146">Каталог в сжатом формате.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-146">Catalog in compressed format.</span></span> <span data-ttu-id="8a3c0-147">Подключаемый модуль может передать расположение этого файла в проигрыватель Windows Media в [ивмпконтентпартнер:: жеткаталогурл](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="8a3c0-147">Your plug-in can give the location of this file to Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> |
| <span data-ttu-id="8a3c0-148">скомпилированные \_ уникальные \_words.txt</span><span class="sxs-lookup"><span data-stu-id="8a3c0-148">compiled\_unique\_words.txt</span></span> | <span data-ttu-id="8a3c0-149">Промежуточный выходной файл.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-149">An intermediate output file.</span></span> <span data-ttu-id="8a3c0-150">Не используется проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8a3c0-150">Not used by Windows Media Player.</span></span>                                                                                                                      |



 

 

 




