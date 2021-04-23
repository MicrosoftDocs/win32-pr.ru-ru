---
description: В этом разделе описывается написание пользовательского Media Foundation преобразования (MFT).
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Запись пользовательского MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15b9d5ae655ba67d4a526aeb8a82eb9d3912da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910188"
---
# <a name="writing-a-custom-mft"></a><span data-ttu-id="37056-103">Запись пользовательского MFT</span><span class="sxs-lookup"><span data-stu-id="37056-103">Writing a Custom MFT</span></span>

<span data-ttu-id="37056-104">В этом разделе описывается написание пользовательского Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="37056-104">This section describes how to write a custom Media Foundation Transform (MFT).</span></span>

## <a name="mft-checklist"></a><span data-ttu-id="37056-105">Контрольный список MFT</span><span class="sxs-lookup"><span data-stu-id="37056-105">MFT Checklist</span></span>

<span data-ttu-id="37056-106">При реализации пользовательского MFT используйте следующий контрольный список, чтобы определить требования.</span><span class="sxs-lookup"><span data-stu-id="37056-106">When you implement a custom MFT, use the following checklist to determine the requirements:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37056-107">Все МФТС</span><span class="sxs-lookup"><span data-stu-id="37056-107">All MFTs</span></span></td>
<td><span data-ttu-id="37056-108">Все МФТС должны реализовывать <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>имфтрансформ</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37056-108">All MFTs must implement <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.</span></span><br/> <span data-ttu-id="37056-109">Следующие разделы содержат дополнительные сведения о реализации этого интерфейса:</span><span class="sxs-lookup"><span data-stu-id="37056-109">The following topics give more information about implementing this interface:</span></span>
<ul>
<li><span data-ttu-id="37056-110"><a href="basic-mft-processing-model.md">Базовая модель обработки MFT</a></span><span class="sxs-lookup"><span data-stu-id="37056-110"><a href="basic-mft-processing-model.md">Basic MFT Processing Model</a></span></span></li>
<li><span data-ttu-id="37056-111"><a href="time-stamps-and-durations.md">Метки времени и длительности</a></span><span class="sxs-lookup"><span data-stu-id="37056-111"><a href="time-stamps-and-durations.md">Time Stamps and Durations</a></span></span></li>
<li><span data-ttu-id="37056-112"><a href="handling-stream-changes.md">Обработка изменений в потоке</a></span><span class="sxs-lookup"><span data-stu-id="37056-112"><a href="handling-stream-changes.md">Handling Stream Changes</a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37056-113">Кодировщики и декодеры</span><span class="sxs-lookup"><span data-stu-id="37056-113">Encoders and decoders</span></span></td>
<td><span data-ttu-id="37056-114">Требования. см. статью <a href="implementing-a-codec-mft.md">Реализация кодека MFT</a>.</span><span class="sxs-lookup"><span data-stu-id="37056-114">Requirements: See <a href="implementing-a-codec-mft.md">Implementing a Codec MFT</a>.</span></span><br/> <span data-ttu-id="37056-115">Рекомендуется: реализуйте <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>имфкуалитядвисе</strong></a> или <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>для поддержки уведомлений качества обслуживания (QoS).</span><span class="sxs-lookup"><span data-stu-id="37056-115">Recommended: Implement <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> or <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>, to support quality-of-service (QoS) notifications.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37056-116">Видеодекодеры и обработчики видео</span><span class="sxs-lookup"><span data-stu-id="37056-116">Video decoders and video processors</span></span></td>
<td><span data-ttu-id="37056-117">Необязательно: поддержка ускорения видео DirectX.</span><span class="sxs-lookup"><span data-stu-id="37056-117">Optional: Support DirectX Video Acceleration.</span></span><br/>
<ul>
<li><span data-ttu-id="37056-118"><a href="direct3d-aware-mfts.md">МФТС с поддержкой Direct3D</a></span><span class="sxs-lookup"><span data-stu-id="37056-118"><a href="direct3d-aware-mfts.md">Direct3D-Aware MFTs</a></span></span></li>
<li><span data-ttu-id="37056-119"><a href="supporting-dxva-2-0-in-media-foundation.md">Поддержка ДКСВА 2,0 в Media Foundation</a></span><span class="sxs-lookup"><span data-stu-id="37056-119"><a href="supporting-dxva-2-0-in-media-foundation.md">Supporting DXVA 2.0 in Media Foundation</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37056-120">Аппаратные кодеки</span><span class="sxs-lookup"><span data-stu-id="37056-120">Hardware codecs</span></span></td>
<td><span data-ttu-id="37056-121">См. раздел <a href="hardware-mfts.md">Hardware МФТС</a>.</span><span class="sxs-lookup"><span data-stu-id="37056-121">See <a href="hardware-mfts.md">Hardware MFTs</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37056-122">Чтобы сделать таблицу MFT обнаруживаемой для обнаружения приложениями...</span><span class="sxs-lookup"><span data-stu-id="37056-122">To make your MFT discoverable by applications...</span></span></td>
<td><span data-ttu-id="37056-123">См. раздел <a href="registering-and-enumerating-mfts.md">Регистрация и перечисление МФТС</a>.</span><span class="sxs-lookup"><span data-stu-id="37056-123">See <a href="registering-and-enumerating-mfts.md">Registering and Enumerating MFTs</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37056-124">Асинхронная обработка данных</span><span class="sxs-lookup"><span data-stu-id="37056-124">Asynchronous data processing</span></span></td>
<td><span data-ttu-id="37056-125">Модель MFT по умолчанию использует синхронные (блокирующие) вызовы для обработки данных.</span><span class="sxs-lookup"><span data-stu-id="37056-125">The default MFT model uses synchronous (blocking) calls to process data.</span></span> <span data-ttu-id="37056-126">Для некоторых МФТС асинхронная обработка может быть более эффективной.</span><span class="sxs-lookup"><span data-stu-id="37056-126">For some MFTs, asynchronous processing can be more efficient.</span></span> <span data-ttu-id="37056-127">Однако его также сложнее реализовать.</span><span class="sxs-lookup"><span data-stu-id="37056-127">However, it is also more complex to implement.</span></span><br/> <span data-ttu-id="37056-128">Дополнительные сведения см. в разделе <a href="asynchronous-mfts.md">асинхронная МФТС</a>.</span><span class="sxs-lookup"><span data-stu-id="37056-128">For more information, see <a href="asynchronous-mfts.md">Asynchronous MFTs</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37056-129">Управление скоростью, хитрость или обратная воспроизведение</span><span class="sxs-lookup"><span data-stu-id="37056-129">Rate control, trick mode, or reverse playback</span></span></td>
<td><span data-ttu-id="37056-130">См. раздел <a href="implementing-rate-control.md">Реализация управления скоростью</a>.</span><span class="sxs-lookup"><span data-stu-id="37056-130">See <a href="implementing-rate-control.md">Implementing Rate Control</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37056-131">Если таблица MFT создает потоки...</span><span class="sxs-lookup"><span data-stu-id="37056-131">If your MFT creates threads...</span></span></td>
<td><span data-ttu-id="37056-132">Реализуйте интерфейс <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>имфреалтимеклиент</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="37056-132">Implement the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37056-133">Если в MFT есть ограничения лицензирования...</span><span class="sxs-lookup"><span data-stu-id="37056-133">If your MFT has licensing restrictions...</span></span></td>
<td><span data-ttu-id="37056-134">Рассмотрите возможность использования механизма использования поля.</span><span class="sxs-lookup"><span data-stu-id="37056-134">Consider using the field-of-use mechanism.</span></span> <span data-ttu-id="37056-135">См. <a href="field-of-use-restrictions.md">поле ограничения использования</a>.</span><span class="sxs-lookup"><span data-stu-id="37056-135">See <a href="field-of-use-restrictions.md">Field of Use Restrictions</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37056-136">При переносе существующего объекта мультимедиа DirectX (DMO)...</span><span class="sxs-lookup"><span data-stu-id="37056-136">If you are porting an existing DirectX Media Object (DMO)...</span></span></td>
<td><span data-ttu-id="37056-137">См. раздел <a href="comparison-of-mfts-and-dmos.md">Сравнение МФТС и дмос</a>.</span><span class="sxs-lookup"><span data-stu-id="37056-137">See <a href="comparison-of-mfts-and-dmos.md">Comparison of MFTs and DMOs</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="37056-138">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="37056-138">This section contains the following topics:</span></span>

-   [<span data-ttu-id="37056-139">Метки времени и длительности</span><span class="sxs-lookup"><span data-stu-id="37056-139">Time Stamps and Durations</span></span>](time-stamps-and-durations.md)
-   [<span data-ttu-id="37056-140">Обработка изменений в потоке</span><span class="sxs-lookup"><span data-stu-id="37056-140">Handling Stream Changes</span></span>](handling-stream-changes.md)
-   [<span data-ttu-id="37056-141">Реализация MFT кодека</span><span class="sxs-lookup"><span data-stu-id="37056-141">Implementing a Codec MFT</span></span>](implementing-a-codec-mft.md)
-   [<span data-ttu-id="37056-142">МФТС с поддержкой Direct3D</span><span class="sxs-lookup"><span data-stu-id="37056-142">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
-   [<span data-ttu-id="37056-143">Оборудование МФТС</span><span class="sxs-lookup"><span data-stu-id="37056-143">Hardware MFTs</span></span>](hardware-mfts.md)
-   [<span data-ttu-id="37056-144">Успешный кодек</span><span class="sxs-lookup"><span data-stu-id="37056-144">Codec Merit</span></span>](codec-merit.md)

## <a name="related-topics"></a><span data-ttu-id="37056-145">См. также</span><span class="sxs-lookup"><span data-stu-id="37056-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37056-146">Преобразования Media Foundation</span><span class="sxs-lookup"><span data-stu-id="37056-146">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




