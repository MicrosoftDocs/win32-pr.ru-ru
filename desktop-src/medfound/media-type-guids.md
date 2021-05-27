---
description: Основные типы носителей
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Основные типы носителей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56553ac635f0e767e43e057b2a468027dcefb730
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549579"
---
# <a name="major-media-types"></a><span data-ttu-id="ff83a-103">Основные типы носителей</span><span class="sxs-lookup"><span data-stu-id="ff83a-103">Major Media Types</span></span>

<span data-ttu-id="ff83a-104">В типе мультимедиа *основной тип* описывает общую категорию данных, например аудио или видео.</span><span class="sxs-lookup"><span data-stu-id="ff83a-104">In a media type, the *major type* describes the overall category of the data, such as audio or video.</span></span> <span data-ttu-id="ff83a-105">*Подтип*, если он есть, дополнительно уточните основной тип.</span><span class="sxs-lookup"><span data-stu-id="ff83a-105">The *subtype*, if present, further refines the major type.</span></span> <span data-ttu-id="ff83a-106">Например, если основной тип — Video, подтип может быть 32-разрядным видео RGB.</span><span class="sxs-lookup"><span data-stu-id="ff83a-106">For example, if the major type is video, the subtype might be 32-bit RGB video.</span></span> <span data-ttu-id="ff83a-107">Подтипы также отличают закодированные форматы, такие как видео H. 264, от несжатых форматов.</span><span class="sxs-lookup"><span data-stu-id="ff83a-107">Subtypes also distinguish encoded formats, such as H.264 video, from uncompressed formats.</span></span>

<span data-ttu-id="ff83a-108">Основной тип и подтип идентифицируются по идентификаторам GUID и хранятся в следующих атрибутах:</span><span class="sxs-lookup"><span data-stu-id="ff83a-108">Major type and subtype are identified by GUIDs and stored in the following attributes:</span></span>



| <span data-ttu-id="ff83a-109">Атрибут</span><span class="sxs-lookup"><span data-stu-id="ff83a-109">Attribute</span></span>                                             | <span data-ttu-id="ff83a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ff83a-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| [<span data-ttu-id="ff83a-111">\_ \_ основной тип MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="ff83a-111">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="ff83a-112">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="ff83a-112">Major type.</span></span> |
| [<span data-ttu-id="ff83a-113">подтип MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="ff83a-113">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="ff83a-114">Подтип.</span><span class="sxs-lookup"><span data-stu-id="ff83a-114">Subtype.</span></span>    |



 

<span data-ttu-id="ff83a-115">Определены следующие основные типы.</span><span class="sxs-lookup"><span data-stu-id="ff83a-115">The following major types are defined.</span></span>



| <span data-ttu-id="ff83a-116">Основной тип</span><span class="sxs-lookup"><span data-stu-id="ff83a-116">Major Type</span></span>                    | <span data-ttu-id="ff83a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="ff83a-117">Description</span></span>                                                                                                                                                | <span data-ttu-id="ff83a-118">Подтипы</span><span class="sxs-lookup"><span data-stu-id="ff83a-118">Subtypes</span></span>                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff83a-119">**Мфмедиатипе \_ аудио**</span><span class="sxs-lookup"><span data-stu-id="ff83a-119">**MFMediaType\_Audio**</span></span>        | <span data-ttu-id="ff83a-120">Аудиосигнал.</span><span class="sxs-lookup"><span data-stu-id="ff83a-120">Audio.</span></span>                                                                                                                                                     | <span data-ttu-id="ff83a-121">[Идентификаторы GUID для звуковых подтипов](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="ff83a-121">[Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>      |
| <span data-ttu-id="ff83a-122">**\_Двоичный файл мфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="ff83a-122">**MFMediaType\_Binary**</span></span>       | <span data-ttu-id="ff83a-123">Двоичный поток.</span><span class="sxs-lookup"><span data-stu-id="ff83a-123">Binary stream.</span></span>                                                                                                                                             | <span data-ttu-id="ff83a-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="ff83a-124">None.</span></span>                                                |
| <span data-ttu-id="ff83a-125">**Мфмедиатипе \_ филетрансфер**</span><span class="sxs-lookup"><span data-stu-id="ff83a-125">**MFMediaType\_FileTransfer**</span></span> | <span data-ttu-id="ff83a-126">Поток, содержащий файлы данных.</span><span class="sxs-lookup"><span data-stu-id="ff83a-126">A stream that contains data files.</span></span>                                                                                                                         | <span data-ttu-id="ff83a-127">Нет.</span><span class="sxs-lookup"><span data-stu-id="ff83a-127">None.</span></span>                                                |
| <span data-ttu-id="ff83a-128">**Мфмедиатипе \_ HTML**</span><span class="sxs-lookup"><span data-stu-id="ff83a-128">**MFMediaType\_HTML**</span></span>         | <span data-ttu-id="ff83a-129">Поток HTML.</span><span class="sxs-lookup"><span data-stu-id="ff83a-129">HTML stream.</span></span>                                                                                                                                               | <span data-ttu-id="ff83a-130">Нет.</span><span class="sxs-lookup"><span data-stu-id="ff83a-130">None.</span></span>                                                |
| <span data-ttu-id="ff83a-131">**\_Изображение мфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="ff83a-131">**MFMediaType\_Image**</span></span>        | <span data-ttu-id="ff83a-132">Поток изображений по-прежнему.</span><span class="sxs-lookup"><span data-stu-id="ff83a-132">Still image stream.</span></span>                                                                                                                                        | <span data-ttu-id="ff83a-133">[Идентификаторы GUID и CLSID WIC](../wic/-wic-guids-clsids.md).</span><span class="sxs-lookup"><span data-stu-id="ff83a-133">[WIC GUIDs and CLSIDs](../wic/-wic-guids-clsids.md).</span></span>       |
| <span data-ttu-id="ff83a-134">**\_Метаданные мфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="ff83a-134">**MFMediaType\_Metadata**</span></span>        | <span data-ttu-id="ff83a-135">Поток метаданных.</span><span class="sxs-lookup"><span data-stu-id="ff83a-135">Metadata stream.</span></span>                                                                                                                                        | <span data-ttu-id="ff83a-136">Нет.</span><span class="sxs-lookup"><span data-stu-id="ff83a-136">None.</span></span>       |
| <span data-ttu-id="ff83a-137">**Мфмедиатипе с \_ защитой**</span><span class="sxs-lookup"><span data-stu-id="ff83a-137">**MFMediaType\_Protected**</span></span>    | <span data-ttu-id="ff83a-138">Защищенный носитель.</span><span class="sxs-lookup"><span data-stu-id="ff83a-138">Protected media.</span></span>                                                                                                                                           | <span data-ttu-id="ff83a-139">Подтип определяет схему защиты содержимого.</span><span class="sxs-lookup"><span data-stu-id="ff83a-139">The subtype specifies the content protection scheme.</span></span> |
| <span data-ttu-id="ff83a-140">**\_Восприятие мфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="ff83a-140">**MFMediaType\_Perception**</span></span>   | <span data-ttu-id="ff83a-141">Потоки из датчика камеры или единицы обработки, которые являются причиной и распознающи необработанные видеоданные и позволяют понять окружающую среду и людей.</span><span class="sxs-lookup"><span data-stu-id="ff83a-141">Streams from a camera sensor or processing unit that reasons and understands raw video data and provides understanding of the environment or humans in it.</span></span> | <span data-ttu-id="ff83a-142">Нет.</span><span class="sxs-lookup"><span data-stu-id="ff83a-142">None.</span></span>                                                |
| <span data-ttu-id="ff83a-143">**Мфмедиатипе \_ Sami**</span><span class="sxs-lookup"><span data-stu-id="ff83a-143">**MFMediaType\_SAMI**</span></span>         | <span data-ttu-id="ff83a-144">Синхронизированные доступные субтитры обмена мультимедиа (SAMI).</span><span class="sxs-lookup"><span data-stu-id="ff83a-144">Synchronized Accessible Media Interchange (SAMI) captions.</span></span>                                                                                                 | <span data-ttu-id="ff83a-145">Нет.</span><span class="sxs-lookup"><span data-stu-id="ff83a-145">None.</span></span>                                                |
| <span data-ttu-id="ff83a-146">**\_Сценарий мфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="ff83a-146">**MFMediaType\_Script**</span></span>       | <span data-ttu-id="ff83a-147">Поток скрипта.</span><span class="sxs-lookup"><span data-stu-id="ff83a-147">Script stream.</span></span>                                                                                                                                             | <span data-ttu-id="ff83a-148">Нет.</span><span class="sxs-lookup"><span data-stu-id="ff83a-148">None.</span></span>                                                |
| <span data-ttu-id="ff83a-149">**\_Поток мфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="ff83a-149">**MFMediaType\_Stream**</span></span>       | <span data-ttu-id="ff83a-150">Мультиплексированный поток или простейший поток.</span><span class="sxs-lookup"><span data-stu-id="ff83a-150">Multiplexed stream or elementary stream.</span></span>                                                                                                                   | [<span data-ttu-id="ff83a-151">Идентификаторы GUID подтипов потока</span><span class="sxs-lookup"><span data-stu-id="ff83a-151">Stream Subtype GUIDs</span></span>](stream-subtype-guids.md)     |
| <span data-ttu-id="ff83a-152">**\_Видео мфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="ff83a-152">**MFMediaType\_Video**</span></span>        | <span data-ttu-id="ff83a-153">Видео.</span><span class="sxs-lookup"><span data-stu-id="ff83a-153">Video.</span></span>                                                                                                                                                     | <span data-ttu-id="ff83a-154">[Идентификаторы GUID для подтипов видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="ff83a-154">[Video Subtype GUIDs](video-subtype-guids.md).</span></span>      |



 

<span data-ttu-id="ff83a-155">Сторонние компоненты могут определять новые основные типы и новые подтипы.</span><span class="sxs-lookup"><span data-stu-id="ff83a-155">Third-party components can define new major types and new subtypes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff83a-156">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ff83a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff83a-157">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="ff83a-157">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ff83a-158">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="ff83a-158">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
