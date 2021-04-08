---
description: Примеры носителей
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Примеры носителей (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e10df770f0edcdcb329cf8d2bda3d3dc46acbf6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999929"
---
# <a name="media-samples-microsoft-media-foundation"></a><span data-ttu-id="8dd27-103">Примеры носителей (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="8dd27-103">Media Samples (Microsoft Media Foundation)</span></span>

<span data-ttu-id="8dd27-104">Пример носителя — это объект, содержащий упорядоченный список из нуля или более буферов.</span><span class="sxs-lookup"><span data-stu-id="8dd27-104">A media sample is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="8dd27-105">Примеры носителей предоставляют интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="8dd27-105">Media samples expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="8dd27-106">Объем данных, содержащихся в одном образце, зависит от компонента, который создает образец и на тип данных в буферах.</span><span class="sxs-lookup"><span data-stu-id="8dd27-106">The amount of data contained in one sample depends on the component that creates the sample and on the type of data in the buffers.</span></span> <span data-ttu-id="8dd27-107">Для несжатого видео образец обычно содержит один кадр видео.</span><span class="sxs-lookup"><span data-stu-id="8dd27-107">For uncompressed video, a sample usually holds a single video frame.</span></span> <span data-ttu-id="8dd27-108">Для несжатого звука объем данных может быть разным, но обычно звуковые фреймы не охватывают два образца.</span><span class="sxs-lookup"><span data-stu-id="8dd27-108">For uncompressed audio, the amount of data can vary, but usually an audio frame does not span two samples.</span></span> <span data-ttu-id="8dd27-109">Для сжатых данных эти рекомендации могут не применяться.</span><span class="sxs-lookup"><span data-stu-id="8dd27-109">For compressed data, these guidelines might not apply.</span></span>

<span data-ttu-id="8dd27-110">Один пример может содержать несколько буферов для повышения эффективности.</span><span class="sxs-lookup"><span data-stu-id="8dd27-110">A single sample might contain multiple buffers for reasons of efficiency.</span></span> <span data-ttu-id="8dd27-111">Например, в файле ASF видеокадр часто распределяется между несколькими пакетами ASF.</span><span class="sxs-lookup"><span data-stu-id="8dd27-111">For example, in an ASF file, a video frame is often spread out among multiple ASF packets.</span></span> <span data-ttu-id="8dd27-112">Источник мультимедиа может считывать пакеты в несколько буферов.</span><span class="sxs-lookup"><span data-stu-id="8dd27-112">The media source might read the packets into multiple buffers.</span></span> <span data-ttu-id="8dd27-113">Вместо копирования каждого фрагмента в один буфер источник просто помещает все буферы в один пример.</span><span class="sxs-lookup"><span data-stu-id="8dd27-113">Instead of copying each fragment into one buffer, the source simply puts all of the buffers into one sample.</span></span> <span data-ttu-id="8dd27-114">Затем нисходящие компоненты могут решить, следует ли копировать небольшие буферы в один непрерывный буфер.</span><span class="sxs-lookup"><span data-stu-id="8dd27-114">Downstream components can then decide whether to copy the smaller buffers into one contiguous buffer.</span></span> <span data-ttu-id="8dd27-115">Как правило, при написании компонента конвейера следует предположить, что любой пример может содержать более одного буфера.</span><span class="sxs-lookup"><span data-stu-id="8dd27-115">Generally, if you are writing a pipeline component, you should assume that any sample might contain more than one buffer.</span></span>

<span data-ttu-id="8dd27-116">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="8dd27-116">This section contains the following topics.</span></span>



| <span data-ttu-id="8dd27-117">Раздел</span><span class="sxs-lookup"><span data-stu-id="8dd27-117">Topic</span></span>                                                        | <span data-ttu-id="8dd27-118">Описание</span><span class="sxs-lookup"><span data-stu-id="8dd27-118">Description</span></span>                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8dd27-119">Работа с примерами мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8dd27-119">Working with Media Samples</span></span>](working-with-media-samples.md) | <span data-ttu-id="8dd27-120">Описывает общее поведение образцов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8dd27-120">Describes the general behavior of media samples.</span></span>                                                                         |
| [<span data-ttu-id="8dd27-121">Образцы видео</span><span class="sxs-lookup"><span data-stu-id="8dd27-121">Video Samples</span></span>](video-samples.md)                           | <span data-ttu-id="8dd27-122">Описание специализированной реализации [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , предназначенной для хранения несжатых кадров видео.</span><span class="sxs-lookup"><span data-stu-id="8dd27-122">Describes a specialized implementation of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) designed for holding uncompressed video frames.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8dd27-123">См. также</span><span class="sxs-lookup"><span data-stu-id="8dd27-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dd27-124">Буферы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8dd27-124">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="8dd27-125">Примитивы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8dd27-125">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



