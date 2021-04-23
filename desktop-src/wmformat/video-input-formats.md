---
title: Форматы входных данных видео
description: Форматы входных данных видео
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- Windows Media Format SDK, форматы входных данных видео
- Формат расширенных систем (ASF), форматы входных данных видео
- ASF (расширенный формат систем), форматы входных данных видео
- форматы входных данных видео
- Windows Media Format SDK, форматы видео
- Расширенный формат систем (ASF), форматы видео
- ASF (расширенный формат систем), форматы видео
- форматы видео
- Кодек Windows Media Video 9, форматы входных видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "105691480"
---
# <a name="video-input-formats"></a><span data-ttu-id="58a01-112">Форматы входных данных видео</span><span class="sxs-lookup"><span data-stu-id="58a01-112">Video Input Formats</span></span>

<span data-ttu-id="58a01-113">Модуль записи принимает следующие форматы видео в качестве входных данных для сжатия с помощью кодека Windows Media Video 9:</span><span class="sxs-lookup"><span data-stu-id="58a01-113">The writer accepts the following video formats as input to be compressed using the Windows Media Video 9 codec:</span></span>

-   <span data-ttu-id="58a01-114">ВММЕДИАСУБТИПЕ \_ ийув</span><span class="sxs-lookup"><span data-stu-id="58a01-114">WMMEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="58a01-115">ВММЕДИАСУБТИПЕ \_ I420</span><span class="sxs-lookup"><span data-stu-id="58a01-115">WMMEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="58a01-116">ВММЕДИАСУБТИПЕ \_ YV12</span><span class="sxs-lookup"><span data-stu-id="58a01-116">WMMEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="58a01-117">ВММЕДИАСУБТИПЕ \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="58a01-117">WMMEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="58a01-118">ВММЕДИАСУБТИПЕ \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="58a01-118">WMMEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="58a01-119">ВММЕДИАСУБТИПЕ \_ ивю</span><span class="sxs-lookup"><span data-stu-id="58a01-119">WMMEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="58a01-120">ВММЕДИАСУБТИПЕ \_ YVU9</span><span class="sxs-lookup"><span data-stu-id="58a01-120">WMMEDIASUBTYPE\_YVU9</span></span>
-   <span data-ttu-id="58a01-121">ВММЕДИАСУБТИПЕ \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="58a01-121">WMMEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="58a01-122">ВММЕДИАСУБТИПЕ \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="58a01-122">WMMEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="58a01-123">ВММЕДИАСУБТИПЕ \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="58a01-123">WMMEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="58a01-124">ВММЕДИАСУБТИПЕ \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="58a01-124">WMMEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="58a01-125">ВММЕДИАСУБТИПЕ \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="58a01-125">WMMEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="58a01-126">Следует всегда использовать [**ивмвритер:: жетинпутформаткаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) и [**Ивмвритер:: жетинпутформат**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) для перечисления доступных входных форматов и получения входного объекта свойств носителя для требуемого формата.</span><span class="sxs-lookup"><span data-stu-id="58a01-126">You should always use [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) and [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) to enumerate the available input formats and to obtain the input media properties object for the desired format.</span></span> <span data-ttu-id="58a01-127">Видео входные свойства мультимедиа необходимо изменить, чтобы отразить размер кадра и частоту кадров входного носителя.</span><span class="sxs-lookup"><span data-stu-id="58a01-127">Video input media properties objects must be changed to reflect the frame size and frame rate of your input media.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58a01-128">См. также</span><span class="sxs-lookup"><span data-stu-id="58a01-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58a01-129">**Идентификаторы типов мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="58a01-129">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="58a01-130">**Типы носителей**</span><span class="sxs-lookup"><span data-stu-id="58a01-130">**Media Types**</span></span>](media-types.md)
</dt> </dl>

 

 




