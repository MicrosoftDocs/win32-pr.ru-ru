---
title: Типы носителей
description: Типы носителей
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows Media Format SDK, типы мультимедиа
- Расширенный формат систем (ASF), типы мультимедиа
- ASF (Расширенный системный формат), типы мультимедиа
- типы носителей, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35005498e8b0625f404e9a54a51cddc65fbfd7bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104133034"
---
# <a name="media-types"></a><span data-ttu-id="fabcd-107">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="fabcd-107">Media Types</span></span>

<span data-ttu-id="fabcd-108">Типы носителей определяют различные типы носителей, которые могут использоваться пакетом SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="fabcd-108">Media types identify the different types of media that can be used by the Windows Media Format SDK.</span></span> <span data-ttu-id="fabcd-109">Все типы носителей — это значения GUID, которые были назначены константам в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="fabcd-109">All media types are GUID values that have been assigned to constants in the SDK.</span></span> <span data-ttu-id="fabcd-110">Значения GUID, представленные константами, перечисленными в этом разделе, перечислены в разделе [идентификаторы типов мультимедиа](media-type-identifiers.md) этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="fabcd-110">The GUID values represented by the constants listed in this section are listed in the [Media Type Identifiers](media-type-identifiers.md) section of this reference.</span></span>

<span data-ttu-id="fabcd-111">В следующей таблице перечислены основные типы носителей.</span><span class="sxs-lookup"><span data-stu-id="fabcd-111">The following table lists major media types.</span></span> <span data-ttu-id="fabcd-112">Эти константы определяют высокоуровневую классификацию цифровых носителей, поддерживаемых пакетом SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="fabcd-112">These constants define the high level classification of digital media supported by the Windows Media Format SDK.</span></span>



| <span data-ttu-id="fabcd-113">Основной тип</span><span class="sxs-lookup"><span data-stu-id="fabcd-113">Major type</span></span>                | <span data-ttu-id="fabcd-114">Описание</span><span class="sxs-lookup"><span data-stu-id="fabcd-114">Description</span></span>                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fabcd-115">\_Видео вммедиатипе</span><span class="sxs-lookup"><span data-stu-id="fabcd-115">WMMEDIATYPE\_Video</span></span>        | <span data-ttu-id="fabcd-116">Поток видео.</span><span class="sxs-lookup"><span data-stu-id="fabcd-116">A video stream.</span></span>                                                                                         |
| <span data-ttu-id="fabcd-117">ВММЕДИАТИПЕ \_ аудио</span><span class="sxs-lookup"><span data-stu-id="fabcd-117">WMMEDIATYPE\_Audio</span></span>        | <span data-ttu-id="fabcd-118">Аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="fabcd-118">An audio stream.</span></span>                                                                                        |
| <span data-ttu-id="fabcd-119">\_Сценарий вммедиатипе</span><span class="sxs-lookup"><span data-stu-id="fabcd-119">WMMEDIATYPE\_Script</span></span>       | <span data-ttu-id="fabcd-120">Поток скрипта.</span><span class="sxs-lookup"><span data-stu-id="fabcd-120">A script stream.</span></span>                                                                                        |
| <span data-ttu-id="fabcd-121">ВММЕДИАТИПЕ \_ филетрансфер</span><span class="sxs-lookup"><span data-stu-id="fabcd-121">WMMEDIATYPE\_FileTransfer</span></span> | <span data-ttu-id="fabcd-122">Поток, содержащий файлы данных.</span><span class="sxs-lookup"><span data-stu-id="fabcd-122">A stream that contains data files.</span></span> <span data-ttu-id="fabcd-123">Этот основной тип также имеет веб-потоки, состоящие из HTML-файлов.</span><span class="sxs-lookup"><span data-stu-id="fabcd-123">Web streams, which consist of HTML files, also have this major type.</span></span> |
| <span data-ttu-id="fabcd-124">\_Изображение вммедиатипе</span><span class="sxs-lookup"><span data-stu-id="fabcd-124">WMMEDIATYPE\_Image</span></span>        | <span data-ttu-id="fabcd-125">Поток изображений в формате JPEG для иллюстрированного звукового файла (как в показе слайдов).</span><span class="sxs-lookup"><span data-stu-id="fabcd-125">A JPEG image stream for an illustrated audio file (as in a slide show).</span></span>                                 |
| <span data-ttu-id="fabcd-126">ВММЕДИАТИПЕ \_ текст</span><span class="sxs-lookup"><span data-stu-id="fabcd-126">WMMEDIATYPE\_Text</span></span>         | <span data-ttu-id="fabcd-127">Текстовый поток.</span><span class="sxs-lookup"><span data-stu-id="fabcd-127">A text stream.</span></span>                                                                                          |



 

<span data-ttu-id="fabcd-128">В дополнение к явно поддерживаемым основным типам носителей можно создавать собственные произвольные типы данных.</span><span class="sxs-lookup"><span data-stu-id="fabcd-128">In addition to the explicitly supported major media types, you can create your own arbitrary data types.</span></span> <span data-ttu-id="fabcd-129">Для пользовательских произвольных типов данных необходимо убедиться, что используемый идентификатор GUID не соответствует существующему основному типу.</span><span class="sxs-lookup"><span data-stu-id="fabcd-129">For custom arbitrary data types, you must ensure that the GUID you use does not match an existing major type.</span></span>

<span data-ttu-id="fabcd-130">Поток мультимедиа часто будет иметь подтип в дополнение к его основному типу.</span><span class="sxs-lookup"><span data-stu-id="fabcd-130">A media stream will often have a subtype in addition to its major type.</span></span> <span data-ttu-id="fabcd-131">В следующих разделах перечислены поддерживаемые подтипы.</span><span class="sxs-lookup"><span data-stu-id="fabcd-131">The following sections list the supported subtypes.</span></span>



| <span data-ttu-id="fabcd-132">Section</span><span class="sxs-lookup"><span data-stu-id="fabcd-132">Section</span></span>                                                        | <span data-ttu-id="fabcd-133">Описание</span><span class="sxs-lookup"><span data-stu-id="fabcd-133">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fabcd-134">Несжатые подтипы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="fabcd-134">Uncompressed Media Subtypes</span></span>](uncompressed-media-subtypes.md) | <span data-ttu-id="fabcd-135">Описывает подтипы, доступные для несжатого носителя.</span><span class="sxs-lookup"><span data-stu-id="fabcd-135">Describes the subtypes available for uncompressed media.</span></span> <span data-ttu-id="fabcd-136">Это типы, обычно связанные с входными или выходными носителями.</span><span class="sxs-lookup"><span data-stu-id="fabcd-136">These are the types typically associated with input or output media.</span></span>              |
| [<span data-ttu-id="fabcd-137">Сжатые подтипы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="fabcd-137">Compressed Media Subtypes</span></span>](compressed-media-subtypes.md)     | <span data-ttu-id="fabcd-138">Описывает подтипы, доступные для сжатого носителя.</span><span class="sxs-lookup"><span data-stu-id="fabcd-138">Describes the subtypes available for compressed media.</span></span> <span data-ttu-id="fabcd-139">Это типы, обычно связанные с мультимедиа в потоке в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="fabcd-139">These are the types typically associated with media in a stream within an ASF file.</span></span> |
| [<span data-ttu-id="fabcd-140">Форматы входных данных видео</span><span class="sxs-lookup"><span data-stu-id="fabcd-140">Video Input Formats</span></span>](video-input-formats.md)                 | <span data-ttu-id="fabcd-141">Список форматов видео, принятых в качестве входных данных для кодека Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="fabcd-141">Lists the video formats accepted as inputs for the Windows Media Video 9 codec.</span></span>                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="fabcd-142">См. также</span><span class="sxs-lookup"><span data-stu-id="fabcd-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fabcd-143">**Идентификаторы типов мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="fabcd-143">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="fabcd-144">**Справочник по программированию**</span><span class="sxs-lookup"><span data-stu-id="fabcd-144">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




