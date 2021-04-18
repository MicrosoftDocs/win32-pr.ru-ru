---
description: Использование средства обнаружения мультимедиа
ms.assetid: 462150d5-7315-4c2b-81b0-964a788ec47d
title: Использование средства обнаружения мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebdb05eb47c7efabcc3234fb6ac2411a46e40d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105674531"
---
# <a name="using-the-media-detector"></a><span data-ttu-id="48dea-103">Использование средства обнаружения мультимедиа</span><span class="sxs-lookup"><span data-stu-id="48dea-103">Using the Media Detector</span></span>

<span data-ttu-id="48dea-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="48dea-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="48dea-105">Средство обнаружения мультимедиа — это вспомогательный объект, который может получать сведения о файле, например число потоков, их тип и длительность.</span><span class="sxs-lookup"><span data-stu-id="48dea-105">The media detector is a helper object that can retrieve information about a file, such as the number of streams, their type, and their duration.</span></span> <span data-ttu-id="48dea-106">Он также содержит методы для извлечения кадров афиши из видеопотока.</span><span class="sxs-lookup"><span data-stu-id="48dea-106">It also contains methods for retrieving poster frames from a video stream.</span></span> <span data-ttu-id="48dea-107">Он предоставляет интерфейс [**имедиадет**](imediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="48dea-107">It exposes the [**IMediaDet**](imediadet.md) interface.</span></span>

<span data-ttu-id="48dea-108">Средство обнаружения мультимедиа работает в одном из двух режимов.</span><span class="sxs-lookup"><span data-stu-id="48dea-108">The media detector operates in one of two modes.</span></span> <span data-ttu-id="48dea-109">При создании экземпляра детектора мультимедиа он не прикрепляется к определенному исходному файлу.</span><span class="sxs-lookup"><span data-stu-id="48dea-109">When you create an instance of the media detector, it is not attached to a particular source file.</span></span> <span data-ttu-id="48dea-110">В этом режиме можно получить потоковую информацию из нескольких исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="48dea-110">In this mode, you can retrieve stream information from multiple source files.</span></span> <span data-ttu-id="48dea-111">Однако после использования средства обнаружения мультимедиа для получения кадра афиши он переключается в *режим захвата точечного рисунка*.</span><span class="sxs-lookup"><span data-stu-id="48dea-111">However, once you use the media detector to obtain a poster frame, it switches to *bitmap grab mode*.</span></span> <span data-ttu-id="48dea-112">В режиме захвата растрового изображения средство обнаружения мультимедиа прикрепляется к определенному потоку видео, а методы потоковой передачи данных больше не работают.</span><span class="sxs-lookup"><span data-stu-id="48dea-112">In bitmap grab mode, the media detector is attached to a specific video stream, and the stream information methods no longer work.</span></span> <span data-ttu-id="48dea-113">Более того, невозможно переключить детектор мультимедиа обратно в режим запуска.</span><span class="sxs-lookup"><span data-stu-id="48dea-113">Moreover, there is no way to switch the media detector back to its starting mode.</span></span> <span data-ttu-id="48dea-114">Поэтому перед извлечением кадров афиши необходимо получить все необходимые сведения о потоке или создать новые экземпляры средства обнаружения мультимедиа для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="48dea-114">Therefore, obtain any stream information you need before retrieving poster frames, or else create new instances of the media detector for each stream.</span></span>

<span data-ttu-id="48dea-115">Чтобы получить сведения о потоке, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="48dea-115">To obtain stream information, do the following:</span></span>

1.  <span data-ttu-id="48dea-116">Вызовите [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) с именем исходного файла.</span><span class="sxs-lookup"><span data-stu-id="48dea-116">Call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) with the name of the source file.</span></span>
2.  <span data-ttu-id="48dea-117">Вызовите метод [**имедиадет:: Get \_ аутпутстреамс**](imediadet-get-outputstreams.md) , чтобы получить количество потоков в источнике.</span><span class="sxs-lookup"><span data-stu-id="48dea-117">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to obtain the number of streams in the source.</span></span>
3.  <span data-ttu-id="48dea-118">Укажите номер потока с помощью [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="48dea-118">Specify a stream number with [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span> <span data-ttu-id="48dea-119">Затем вызовите один или несколько из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="48dea-119">Then call one or more of the following methods:</span></span>
    -   <span data-ttu-id="48dea-120">[**Имедиадет:: Get \_ Стреамтипе**](imediadet-get-streamtype.md): получает тип носителя потока.</span><span class="sxs-lookup"><span data-stu-id="48dea-120">[**IMediaDet::get\_StreamType**](imediadet-get-streamtype.md): Retrieves the stream's media type.</span></span>
    -   <span data-ttu-id="48dea-121">[**Имедиадет:: Get \_ Стреамленгс**](imediadet-get-streamlength.md): получает длительность потока.</span><span class="sxs-lookup"><span data-stu-id="48dea-121">[**IMediaDet::get\_StreamLength**](imediadet-get-streamlength.md): Retrieves the duration of the stream.</span></span>
    -   <span data-ttu-id="48dea-122">[**Имедиадет:: Get \_ Частота кадров: получает**](imediadet-get-framerate.md)частоту кадра видеопотока.</span><span class="sxs-lookup"><span data-stu-id="48dea-122">[**IMediaDet::get\_FrameRate**](imediadet-get-framerate.md): Retrieves a video stream's frame rate.</span></span>

<span data-ttu-id="48dea-123">Чтобы получить кадр афиши, укажите номер потока, как показано на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="48dea-123">To obtain a poster frame, specify the stream number, as in the previous step.</span></span> <span data-ttu-id="48dea-124">Затем вызовите либо [**имедиадет:: жетбитмапбитс**](imediadet-getbitmapbits.md), который копирует кадр афиши в буфер, либо [**Имедиадет:: вритебитмапбитс**](imediadet-writebitmapbits.md), который сохраняет кадр афиши в файл.</span><span class="sxs-lookup"><span data-stu-id="48dea-124">Then call either [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md), which copies a poster frame into a buffer, or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md), which saves a poster frame to a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48dea-125">См. также</span><span class="sxs-lookup"><span data-stu-id="48dea-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48dea-126">Работа с источниками</span><span class="sxs-lookup"><span data-stu-id="48dea-126">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



