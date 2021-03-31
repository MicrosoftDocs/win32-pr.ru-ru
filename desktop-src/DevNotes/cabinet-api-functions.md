---
description: 'Дополнительные сведения: функции API CAB-файла'
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Функции API CAB-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327490332d2fe0cb9384eeaaad11215d551f4f0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895678"
---
# <a name="cabinet-api-functions"></a><span data-ttu-id="19e78-103">Функции API CAB-файла</span><span class="sxs-lookup"><span data-stu-id="19e78-103">Cabinet API Functions</span></span>

<span data-ttu-id="19e78-104">В этом разделе описаны следующие функции API CAB-файлов:</span><span class="sxs-lookup"><span data-stu-id="19e78-104">This section describes the following Cabinet API functions:</span></span>

## <a name="fci-functions"></a><span data-ttu-id="19e78-105">Функции FCI</span><span class="sxs-lookup"><span data-stu-id="19e78-105">FCI Functions</span></span>

<span data-ttu-id="19e78-106">Библиотека FCI (интерфейс сжатия файлов) предоставляет возможность создания ящиков (также называемых CAB-файлами).</span><span class="sxs-lookup"><span data-stu-id="19e78-106">The FCI (File Compression Interface) library provides the ability to create cabinets (also known as "CAB files").</span></span> <span data-ttu-id="19e78-107">Кроме того, Библиотека обеспечивает сжатие для уменьшения размера файловых данных, хранящихся в ящиках.</span><span class="sxs-lookup"><span data-stu-id="19e78-107">Additionally, the library provides compression to reduce the size of the file data stored in cabinets.</span></span>



| <span data-ttu-id="19e78-108">Функция</span><span class="sxs-lookup"><span data-stu-id="19e78-108">Function</span></span>                                   | <span data-ttu-id="19e78-109">Описание</span><span class="sxs-lookup"><span data-stu-id="19e78-109">Description</span></span>                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19e78-110">**фЦиаддфиле**</span><span class="sxs-lookup"><span data-stu-id="19e78-110">**FCIAddFile**</span></span>](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | <span data-ttu-id="19e78-111">Добавляет файл в создается в данный момент.</span><span class="sxs-lookup"><span data-stu-id="19e78-111">Adds a file to the cabinet currently being contructed.</span></span><br/>                                           |
| [<span data-ttu-id="19e78-112">**фЦикреате**</span><span class="sxs-lookup"><span data-stu-id="19e78-112">**FCICreate**</span></span>](/windows/desktop/api/Fci/nf-fci-fcicreate)             | <span data-ttu-id="19e78-113">Создает контекст FCI.</span><span class="sxs-lookup"><span data-stu-id="19e78-113">Creates an FCI context.</span></span><br/>                                                                          |
| [<span data-ttu-id="19e78-114">**фЦидестрой**</span><span class="sxs-lookup"><span data-stu-id="19e78-114">**FCIDestroy**</span></span>](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | <span data-ttu-id="19e78-115">Удаляет открытый контекст FCI, освобождая все память и временные файлы, связанные с контекстом.</span><span class="sxs-lookup"><span data-stu-id="19e78-115">Deletes an open FCI context, freeing any memory and temporary files associated with the context.</span></span><br/> |
| [<span data-ttu-id="19e78-116">**фЦифлушкабинет**</span><span class="sxs-lookup"><span data-stu-id="19e78-116">**FCIFlushCabinet**</span></span>](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | <span data-ttu-id="19e78-117">Завершает текущий CAB-файл.</span><span class="sxs-lookup"><span data-stu-id="19e78-117">Completes the current cabinet.</span></span><br/>                                                                   |
| [<span data-ttu-id="19e78-118">**фЦифлушфолдер**</span><span class="sxs-lookup"><span data-stu-id="19e78-118">**FCIFlushFolder**</span></span>](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | <span data-ttu-id="19e78-119">Принудительное завершение текущей папки в ходе разработки.</span><span class="sxs-lookup"><span data-stu-id="19e78-119">Forces the current folder under construction to be completed immediately.</span></span><br/>                        |



 

## <a name="fdi-functions"></a><span data-ttu-id="19e78-120">Функции FDI</span><span class="sxs-lookup"><span data-stu-id="19e78-120">FDI Functions</span></span>

<span data-ttu-id="19e78-121">Библиотека FDI (интерфейс распаковки файлов) предоставляет возможность извлечения файлов из ящиков.</span><span class="sxs-lookup"><span data-stu-id="19e78-121">The FDI (File Decompression Interface) library provides the ability to extract files from cabinets.</span></span>



| <span data-ttu-id="19e78-122">Функция</span><span class="sxs-lookup"><span data-stu-id="19e78-122">Function</span></span>                                         | <span data-ttu-id="19e78-123">Описание</span><span class="sxs-lookup"><span data-stu-id="19e78-123">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19e78-124">**фдикопи**</span><span class="sxs-lookup"><span data-stu-id="19e78-124">**FDICopy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | <span data-ttu-id="19e78-125">Извлекает файлы из CAB.</span><span class="sxs-lookup"><span data-stu-id="19e78-125">Extracts files from cabinets.</span></span><br/>                                                          |
| [<span data-ttu-id="19e78-126">**фдикреате**</span><span class="sxs-lookup"><span data-stu-id="19e78-126">**FDICreate**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | <span data-ttu-id="19e78-127">Создает контекст FDI.</span><span class="sxs-lookup"><span data-stu-id="19e78-127">Creates an FDI context.</span></span><br/>                                                                |
| [<span data-ttu-id="19e78-128">**фдидестрой**</span><span class="sxs-lookup"><span data-stu-id="19e78-128">**FDIDestroy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | <span data-ttu-id="19e78-129">Удаляет открытый контекст FDI.</span><span class="sxs-lookup"><span data-stu-id="19e78-129">Deletes an open FDI context.</span></span><br/>                                                           |
| [<span data-ttu-id="19e78-130">**фдиискабинет**</span><span class="sxs-lookup"><span data-stu-id="19e78-130">**FDIIsCabinet**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | <span data-ttu-id="19e78-131">Определяет, является ли файл CAB-файлом, и, если он есть, возвращает описательные сведения.</span><span class="sxs-lookup"><span data-stu-id="19e78-131">Determines whether a file is a cabinet and, if it is, returns descriptive information.</span></span><br/> |
| [<span data-ttu-id="19e78-132">**фдитрункатекабинет**</span><span class="sxs-lookup"><span data-stu-id="19e78-132">**FDITruncateCabinet**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | <span data-ttu-id="19e78-133">Усекает CAB-файл, начиная с указанного номера папки.</span><span class="sxs-lookup"><span data-stu-id="19e78-133">Truncates a cabinet file starting at the specified folder number.</span></span><br/>                      |



 

## <a name="deprecated-functions"></a><span data-ttu-id="19e78-134">Нерекомендуемые функции</span><span class="sxs-lookup"><span data-stu-id="19e78-134">Deprecated Functions</span></span>

-   [<span data-ttu-id="19e78-135">**делетикстрактедфилес**</span><span class="sxs-lookup"><span data-stu-id="19e78-135">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
-   [<span data-ttu-id="19e78-136">**дллжетверсион**</span><span class="sxs-lookup"><span data-stu-id="19e78-136">**DllGetVersion**</span></span>](dllgetversion.md)
-   [<span data-ttu-id="19e78-137">**Распаковк**</span><span class="sxs-lookup"><span data-stu-id="19e78-137">**Extract**</span></span>](extract.md)
-   [<span data-ttu-id="19e78-138">**жетдллверсион**</span><span class="sxs-lookup"><span data-stu-id="19e78-138">**GetDllVersion**</span></span>](getdllversion.md)

## <a name="related-topics"></a><span data-ttu-id="19e78-139">См. также</span><span class="sxs-lookup"><span data-stu-id="19e78-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19e78-140">Справочник по API CAB-файлов</span><span class="sxs-lookup"><span data-stu-id="19e78-140">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="19e78-141">Использование API CAB-файла</span><span class="sxs-lookup"><span data-stu-id="19e78-141">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 




