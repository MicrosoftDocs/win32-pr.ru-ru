---
title: Создание графов фильтров для записи файлов ASF (КАСФ)
description: Создание графов фильтров для записи файлов ASF (КАСФ)
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- Windows Media Format SDK, создание графов фильтров (КАСФ)
- Пакет SDK для Windows Media Format, DirectShow
- Windows Media Format SDK, написание ASF-файлов (КАСФ)
- Расширенный формат систем (ASF), создание графов фильтра (КАСФ)
- ASF (Расширенный системный формат), создание графов фильтра (КАСФ)
- Расширенный формат систем (ASF), запись (КАСФ)
- ASF (Расширенный системный формат), запись (КАСФ)
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- DirectShow, создание графов фильтров (КАСФ)
- DirectShow, запись файлов ASF (КАСФ)
- Windows Media Format SDK, КАСФ
- Расширенный системный формат (ASF), КАСФ
- ASF (Расширенный системный формат), КАСФ
- DirectShow, КАСФ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a261d1502f76cebc0eb2141cd230c509029
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710027"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a><span data-ttu-id="4688c-118">Создание графов фильтров для записи файлов ASF (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="4688c-118">Building Filter Graphs to Write ASF Files (QASF)</span></span>

<span data-ttu-id="4688c-119">Приложения, основанные на DirectShow, обычно используют один из трех базовых типов графов фильтров при создании содержимого на основе Windows Media:</span><span class="sxs-lookup"><span data-stu-id="4688c-119">Applications based on DirectShow typically use one of three basic types of filter graphs when creating Windows Media–based content:</span></span>

-   <span data-ttu-id="4688c-120">Фильтрация графов для преобразования или перекодирования содержимого из другого формата в формат Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4688c-120">Filter graphs for converting or transcoding content from some other format into Windows Media Format.</span></span>
-   <span data-ttu-id="4688c-121">Фильтрация графов для вставки содержимого, не основанного на мультимедиа Windows (собственные форматы потока), в файлы ASF.</span><span class="sxs-lookup"><span data-stu-id="4688c-121">Filter graphs for inserting content that is not Windows Media-based (native stream formats) into ASF files.</span></span>
-   <span data-ttu-id="4688c-122">Фильтрация графов для записи динамических данных и их непосредственного кодирования в формате Windows Media перед сохранением на диск.</span><span class="sxs-lookup"><span data-stu-id="4688c-122">Filter graphs for capturing live data and encoding it immediately into Windows Media Format before saving it to disk.</span></span>

<span data-ttu-id="4688c-123">Каждый тип графа фильтра подробно описан в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="4688c-123">Each type of filter graph is described in more detail in the following sections.</span></span>



| <span data-ttu-id="4688c-124">Section</span><span class="sxs-lookup"><span data-stu-id="4688c-124">Section</span></span>                                                                                                             | <span data-ttu-id="4688c-125">Описание</span><span class="sxs-lookup"><span data-stu-id="4688c-125">Description</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4688c-126">Перекодирование файлов (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="4688c-126">Transcoding Files (QASF)</span></span>](transcoding-files--qasf.md)                                                             | <span data-ttu-id="4688c-127">Описывает, как создать графы фильтра для перекодирования файлов.</span><span class="sxs-lookup"><span data-stu-id="4688c-127">Describes how to create file-transcoding filter graphs.</span></span>                                               |
| [<span data-ttu-id="4688c-128">Вставка собственных форматов потока в файлы ASF (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="4688c-128">Inserting Native Stream Formats Into ASF Files (QASF)</span></span>](inserting-native-stream-formats-into-asf-files--qasf.md)   | <span data-ttu-id="4688c-129">Описание способов размещения сжатых или несжатых аудио-или видеоданных в ASF-файле.</span><span class="sxs-lookup"><span data-stu-id="4688c-129">Describes how to place any type of compressed or non-compressed audio or video data into an ASF file.</span></span> |
| [<span data-ttu-id="4688c-130">Запись непосредственно с устройства в файл ASF (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="4688c-130">Capturing Directly from a Device to an ASF File (QASF)</span></span>](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | <span data-ttu-id="4688c-131">Описывает создание графов фильтра записи, выводимых в файл ASF.</span><span class="sxs-lookup"><span data-stu-id="4688c-131">Describes how to create capture filter graphs that output to an ASF file.</span></span>                             |



 

 

 




