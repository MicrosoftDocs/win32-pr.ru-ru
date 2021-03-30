---
title: Функции записи файлов
description: Функции записи файлов
ms.assetid: 4514f463-26cf-48a4-aa0c-c25fc5a1979f
keywords:
- Windows Media Format SDK, функции записи файлов
- Windows Media Format SDK, функции
- Расширенный системный формат (ASF), функции записи файлов
- ASF (Расширенный системный формат), функции записи файлов
- Расширенный формат систем (ASF), функции
- ASF (Расширенный системный формат), функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a4764a318ac7cd420296b15bb4a5818ded06384
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067944"
---
# <a name="file-writing-features"></a><span data-ttu-id="65591-109">Функции записи файлов</span><span class="sxs-lookup"><span data-stu-id="65591-109">File Writing Features</span></span>

<span data-ttu-id="65591-110">Одной из основных возможностей пакета SDK Windows Media Format является возможность записи файлов в формате ASF.</span><span class="sxs-lookup"><span data-stu-id="65591-110">One of the primary features of the Windows Media Format SDK is the ability to write files in the Advanced Systems Format (ASF).</span></span> <span data-ttu-id="65591-111">Объект модуля записи используется для записи файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="65591-111">The writer object is used to write ASF files.</span></span> <span data-ttu-id="65591-112">Дополнительные сведения см. в разделе [объект модуля записи](writer-object.md).</span><span class="sxs-lookup"><span data-stu-id="65591-112">For more information see, [Writer Object](writer-object.md).</span></span>

<span data-ttu-id="65591-113">В самом базовом сценарии записи файлов необходимо назначить профиль для использования и имя создаваемого файла.</span><span class="sxs-lookup"><span data-stu-id="65591-113">In the most basic file writing scenario, you assign a profile to use and a name of the file to create.</span></span> <span data-ttu-id="65591-114">Вы передаете образцы в модуль записи по одному за раз.</span><span class="sxs-lookup"><span data-stu-id="65591-114">You pass samples to the writer one at a time.</span></span> <span data-ttu-id="65591-115">После завершения передачи образцов в модуль записи он завершает свои операции и завершает файл ASF.</span><span class="sxs-lookup"><span data-stu-id="65591-115">When you have finished passing samples to the writer, it finishes its operations and completes the ASF file.</span></span> <span data-ttu-id="65591-116">Дополнительные сведения о базовой записи файлов см. в разделе [запись файлов ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="65591-116">For more information about basic file writing, see [Writing ASF Files](writing-asf-files.md).</span></span>

<span data-ttu-id="65591-117">Модуль записи поддерживает несколько дополнительных функций, которые обсуждаются в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="65591-117">The writer supports several advanced features, which are discussed in the following sections.</span></span>

-   [<span data-ttu-id="65591-118">Изменение размера видео</span><span class="sxs-lookup"><span data-stu-id="65591-118">Video Resizing</span></span>](video-resizing.md)
-   [<span data-ttu-id="65591-119">Преобразование цветового пространства</span><span class="sxs-lookup"><span data-stu-id="65591-119">Color Space Conversion</span></span>](color-space-conversion.md)
-   [<span data-ttu-id="65591-120">Ресамплинг звука</span><span class="sxs-lookup"><span data-stu-id="65591-120">Audio Resampling</span></span>](audio-resampling.md)
-   [<span data-ttu-id="65591-121">Приемников</span><span class="sxs-lookup"><span data-stu-id="65591-121">Sinks</span></span>](sinks.md)
-   [<span data-ttu-id="65591-122">Поддержка водяных знаков</span><span class="sxs-lookup"><span data-stu-id="65591-122">Watermarking Support</span></span>](watermarking-support.md)
-   [<span data-ttu-id="65591-123">Форматы ввода, параметры ввода и модули данных</span><span class="sxs-lookup"><span data-stu-id="65591-123">Input Formats, Input Settings, and Data Unit Extensions</span></span>](input-formats-input-settings-and-data-unit-extensions.md)
-   [<span data-ttu-id="65591-124">Перечисление формата входных данных</span><span class="sxs-lookup"><span data-stu-id="65591-124">Input Format Enumeration</span></span>](input-format-enumeration.md)

## <a name="related-topics"></a><span data-ttu-id="65591-125">См. также</span><span class="sxs-lookup"><span data-stu-id="65591-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65591-126">**Компоненты**</span><span class="sxs-lookup"><span data-stu-id="65591-126">**Features**</span></span>](features.md)
</dt> </dl>

 

 




