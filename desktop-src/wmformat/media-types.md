---
title: Типы носителей для пакета SDK Windows Media Format
description: Сведения о типах носителей, которые могут использоваться пакетом SDK Windows Media Format. Типы мультимедиа — это значения GUID, назначенные константам в пакете SDK.
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows Media Format SDK, типы мультимедиа
- Расширенный формат систем (ASF), типы мультимедиа
- ASF (Расширенный системный формат), типы мультимедиа
- типы носителей, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6d15255ab311c67562a6c9dde83650240b0803
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187813"
---
# <a name="media-types-for-windows-media-format-sdk"></a><span data-ttu-id="39abc-108">Типы носителей для пакета SDK Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="39abc-108">Media Types for Windows Media Format SDK</span></span>

<span data-ttu-id="39abc-109">Типы носителей определяют различные типы носителей, которые могут использоваться пакетом SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="39abc-109">Media types identify the different types of media that can be used by the Windows Media Format SDK.</span></span> <span data-ttu-id="39abc-110">Все типы носителей — это значения GUID, которые были назначены константам в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="39abc-110">All media types are GUID values that have been assigned to constants in the SDK.</span></span> <span data-ttu-id="39abc-111">Значения GUID, представленные константами, перечисленными в этом разделе, перечислены в разделе [идентификаторы типов мультимедиа](media-type-identifiers.md) этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="39abc-111">The GUID values represented by the constants listed in this section are listed in the [Media Type Identifiers](media-type-identifiers.md) section of this reference.</span></span>

<span data-ttu-id="39abc-112">В следующей таблице перечислены основные типы носителей.</span><span class="sxs-lookup"><span data-stu-id="39abc-112">The following table lists major media types.</span></span> <span data-ttu-id="39abc-113">Эти константы определяют высокоуровневую классификацию цифровых носителей, поддерживаемых пакетом SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="39abc-113">These constants define the high level classification of digital media supported by the Windows Media Format SDK.</span></span>



| <span data-ttu-id="39abc-114">Основной тип</span><span class="sxs-lookup"><span data-stu-id="39abc-114">Major type</span></span>                | <span data-ttu-id="39abc-115">Описание</span><span class="sxs-lookup"><span data-stu-id="39abc-115">Description</span></span>                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39abc-116">\_Видео вммедиатипе</span><span class="sxs-lookup"><span data-stu-id="39abc-116">WMMEDIATYPE\_Video</span></span>        | <span data-ttu-id="39abc-117">Поток видео.</span><span class="sxs-lookup"><span data-stu-id="39abc-117">A video stream.</span></span>                                                                                         |
| <span data-ttu-id="39abc-118">ВММЕДИАТИПЕ \_ аудио</span><span class="sxs-lookup"><span data-stu-id="39abc-118">WMMEDIATYPE\_Audio</span></span>        | <span data-ttu-id="39abc-119">Аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="39abc-119">An audio stream.</span></span>                                                                                        |
| <span data-ttu-id="39abc-120">\_Сценарий вммедиатипе</span><span class="sxs-lookup"><span data-stu-id="39abc-120">WMMEDIATYPE\_Script</span></span>       | <span data-ttu-id="39abc-121">Поток скрипта.</span><span class="sxs-lookup"><span data-stu-id="39abc-121">A script stream.</span></span>                                                                                        |
| <span data-ttu-id="39abc-122">ВММЕДИАТИПЕ \_ филетрансфер</span><span class="sxs-lookup"><span data-stu-id="39abc-122">WMMEDIATYPE\_FileTransfer</span></span> | <span data-ttu-id="39abc-123">Поток, содержащий файлы данных.</span><span class="sxs-lookup"><span data-stu-id="39abc-123">A stream that contains data files.</span></span> <span data-ttu-id="39abc-124">Этот основной тип также имеет веб-потоки, состоящие из HTML-файлов.</span><span class="sxs-lookup"><span data-stu-id="39abc-124">Web streams, which consist of HTML files, also have this major type.</span></span> |
| <span data-ttu-id="39abc-125">\_Изображение вммедиатипе</span><span class="sxs-lookup"><span data-stu-id="39abc-125">WMMEDIATYPE\_Image</span></span>        | <span data-ttu-id="39abc-126">Поток изображений в формате JPEG для иллюстрированного звукового файла (как в показе слайдов).</span><span class="sxs-lookup"><span data-stu-id="39abc-126">A JPEG image stream for an illustrated audio file (as in a slide show).</span></span>                                 |
| <span data-ttu-id="39abc-127">ВММЕДИАТИПЕ \_ текст</span><span class="sxs-lookup"><span data-stu-id="39abc-127">WMMEDIATYPE\_Text</span></span>         | <span data-ttu-id="39abc-128">Текстовый поток.</span><span class="sxs-lookup"><span data-stu-id="39abc-128">A text stream.</span></span>                                                                                          |



 

<span data-ttu-id="39abc-129">В дополнение к явно поддерживаемым основным типам носителей можно создавать собственные произвольные типы данных.</span><span class="sxs-lookup"><span data-stu-id="39abc-129">In addition to the explicitly supported major media types, you can create your own arbitrary data types.</span></span> <span data-ttu-id="39abc-130">Для пользовательских произвольных типов данных необходимо убедиться, что используемый идентификатор GUID не соответствует существующему основному типу.</span><span class="sxs-lookup"><span data-stu-id="39abc-130">For custom arbitrary data types, you must ensure that the GUID you use does not match an existing major type.</span></span>

<span data-ttu-id="39abc-131">Поток мультимедиа часто будет иметь подтип в дополнение к его основному типу.</span><span class="sxs-lookup"><span data-stu-id="39abc-131">A media stream will often have a subtype in addition to its major type.</span></span> <span data-ttu-id="39abc-132">В следующих разделах перечислены поддерживаемые подтипы.</span><span class="sxs-lookup"><span data-stu-id="39abc-132">The following sections list the supported subtypes.</span></span>



| <span data-ttu-id="39abc-133">Section</span><span class="sxs-lookup"><span data-stu-id="39abc-133">Section</span></span>                                                        | <span data-ttu-id="39abc-134">Описание</span><span class="sxs-lookup"><span data-stu-id="39abc-134">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39abc-135">Несжатые подтипы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="39abc-135">Uncompressed Media Subtypes</span></span>](uncompressed-media-subtypes.md) | <span data-ttu-id="39abc-136">Описывает подтипы, доступные для несжатого носителя.</span><span class="sxs-lookup"><span data-stu-id="39abc-136">Describes the subtypes available for uncompressed media.</span></span> <span data-ttu-id="39abc-137">Это типы, обычно связанные с входными или выходными носителями.</span><span class="sxs-lookup"><span data-stu-id="39abc-137">These are the types typically associated with input or output media.</span></span>              |
| [<span data-ttu-id="39abc-138">Сжатые подтипы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="39abc-138">Compressed Media Subtypes</span></span>](compressed-media-subtypes.md)     | <span data-ttu-id="39abc-139">Описывает подтипы, доступные для сжатого носителя.</span><span class="sxs-lookup"><span data-stu-id="39abc-139">Describes the subtypes available for compressed media.</span></span> <span data-ttu-id="39abc-140">Это типы, обычно связанные с мультимедиа в потоке в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="39abc-140">These are the types typically associated with media in a stream within an ASF file.</span></span> |
| [<span data-ttu-id="39abc-141">Форматы входных данных видео</span><span class="sxs-lookup"><span data-stu-id="39abc-141">Video Input Formats</span></span>](video-input-formats.md)                 | <span data-ttu-id="39abc-142">Список форматов видео, принятых в качестве входных данных для кодека Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="39abc-142">Lists the video formats accepted as inputs for the Windows Media Video 9 codec.</span></span>                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="39abc-143">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="39abc-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39abc-144">**Идентификаторы типов мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="39abc-144">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="39abc-145">**Справочник по программированию**</span><span class="sxs-lookup"><span data-stu-id="39abc-145">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




