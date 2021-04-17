---
title: Компилятор каталога для Интернет-магазинов типа 1
description: Компилятор каталога для Интернет-магазинов типа 1
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Интернет-магазины проигрывателя Windows Media, компилятор каталогов
- Интернет-магазины, компилятор каталогов
- Тип 1 Интернет-магазины, компилятор каталога
- Интернет-магазины проигрывателя Windows Media, catcomp.exe
- Интернет-магазины, catcomp.exe
- Введите 1 Интернет-магазины, catcomp.exe
- компилятор каталога
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c54ffd054c5e72b04ddd32eef12c7fe6b6cc89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691430"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a><span data-ttu-id="09328-111">Компилятор каталога для Интернет-магазинов типа 1</span><span class="sxs-lookup"><span data-stu-id="09328-111">Catalog Compiler for Type 1 Online Stores</span></span>

<span data-ttu-id="09328-112">Компилятор каталога (catcomp.exe) — это средство командной строки, используемое для компиляции набора файлов с разделителями-табуляторами (TSV), содержащих данные каталога Интернет-магазина, в сжатый каталог, который может быть скачан проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="09328-112">The catalog compiler (catcomp.exe) is a command-line tool used by Type 1 online stores to compile the set of tab-separated-value (TSV) files containing the online store's catalog data into a compressed catalog that can be downloaded by Windows Media Player.</span></span> <span data-ttu-id="09328-113">Компилятор каталога также компилирует файлы обновления каталога, содержащие только сведения о каталоге, которые были изменены с момента последнего обновления каталога.</span><span class="sxs-lookup"><span data-stu-id="09328-113">The catalog compiler also compiles catalog update files containing only the catalog information that has changed since the last catalog update.</span></span>

<span data-ttu-id="09328-114">Сжатые файлы каталога или файлы обновления каталога должны быть предоставлены проигрывателю Windows Media для загрузки в реализации [ивмпконтентпартнер:: жеткаталогурл](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)подключаемого модуля интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="09328-114">The compressed catalog files or catalog update files should be provided to Windows Media Player for download in the online store plug-in's implementation of [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span>

<span data-ttu-id="09328-115">Общие задачи</span><span class="sxs-lookup"><span data-stu-id="09328-115">Common Tasks</span></span>

-   [<span data-ttu-id="09328-116">Компиляция полного каталога из TSV-файлов</span><span class="sxs-lookup"><span data-stu-id="09328-116">Compiling a Full Catalog from TSV Files</span></span>](compiling-a-full-catalog-from-tsv-files.md)
-   [<span data-ttu-id="09328-117">Компиляция обновления каталога из полных каталогов</span><span class="sxs-lookup"><span data-stu-id="09328-117">Compiling a Catalog Update from Full Catalogs</span></span>](compiling-a-catalog-update-from-full-catalogs.md)

<span data-ttu-id="09328-118">Задачи диагностики</span><span class="sxs-lookup"><span data-stu-id="09328-118">Diagnostic Tasks</span></span>

-   [<span data-ttu-id="09328-119">Отображение справки</span><span class="sxs-lookup"><span data-stu-id="09328-119">Displaying Help</span></span>](displaying-help.md)
-   [<span data-ttu-id="09328-120">Получение сведений о каталоге</span><span class="sxs-lookup"><span data-stu-id="09328-120">Retrieving Catalog Information</span></span>](retrieving-catalog-information.md)
-   [<span data-ttu-id="09328-121">Применение обновления к каталогу</span><span class="sxs-lookup"><span data-stu-id="09328-121">Applying an Update To a Catalog</span></span>](applying-an-update-to-a-catalog.md)

 

 




