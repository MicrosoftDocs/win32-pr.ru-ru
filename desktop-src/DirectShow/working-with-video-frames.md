---
description: Работа с кадрами видео
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Работа с кадрами видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead597fac5a28befc9c9868485840d03b46e5185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683626"
---
# <a name="working-with-video-frames"></a><span data-ttu-id="cef06-103">Работа с кадрами видео</span><span class="sxs-lookup"><span data-stu-id="cef06-103">Working with Video Frames</span></span>

<span data-ttu-id="cef06-104">Несжатое видео — это последовательность точечных рисунков, которая воспроизводится быстро, обычно с частотой около 30 кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="cef06-104">Uncompressed video is a sequence of bitmaps played in rapid succession, typically at a rate of about 30 frames per second.</span></span> <span data-ttu-id="cef06-105">Так как большинство видео входит в граф фильтра DirectShow в сжатом формате, поток видео обычно проходит через декодер для распаковки.</span><span class="sxs-lookup"><span data-stu-id="cef06-105">Because most video enters a DirectShow filter graph in a compressed format, the video stream generally goes through a decoder for decompression.</span></span> <span data-ttu-id="cef06-106">Многие декодеры выводят выходные данные в формате YUV и передают окончательное преобразование в режим RGB для видеооборудования.</span><span class="sxs-lookup"><span data-stu-id="cef06-106">Many decoders output data in a YUV format and leave the final conversion to RGB for the video hardware just prior to rendering.</span></span> <span data-ttu-id="cef06-107">Если декодер использует ускорение видео DirectX, видеооборудование выполняет дополнительную работу для декодирования изображения.</span><span class="sxs-lookup"><span data-stu-id="cef06-107">If a decoder uses DirectX Video Acceleration, the video hardware performs additional work to decode the image.</span></span> <span data-ttu-id="cef06-108">Поэтому окончательное распаковка растровых изображений может быть не выполнено до тех пор, пока данные не достигнет видеооборудования.</span><span class="sxs-lookup"><span data-stu-id="cef06-108">Thus, final decompression of the bitmaps may not be performed until the data reaches the video hardware.</span></span>

<span data-ttu-id="cef06-109">Но для выполнения различных типов анализа, обработки и редактирования видео часто бывает необходимо работать с несжатыми точечными рисунками в формате RGB или YUV, прежде чем они будут подготавливаться к просмотру или записаны в файл.</span><span class="sxs-lookup"><span data-stu-id="cef06-109">But to perform many types of video analysis, processing, or editing, it is often necessary to work on uncompressed bitmaps in some type of RGB or YUV format before they are rendered or written to file.</span></span> <span data-ttu-id="cef06-110">Эта работа обычно выполняется в фильтре преобразования на основе базового класса [**ктрансформфилтер**](ctransformfilter.md) , а именно в методе **Transform** .</span><span class="sxs-lookup"><span data-stu-id="cef06-110">This work is typically done within a transform filter based on the [**CTransformFilter**](ctransformfilter.md) base class, specifically in the **Transform** method.</span></span> <span data-ttu-id="cef06-111">Этот метод получает указатель на объект [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) , который инкапсулирует данные видео.</span><span class="sxs-lookup"><span data-stu-id="cef06-111">This method receives a pointer to an [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) object that encapsulates the video data.</span></span> <span data-ttu-id="cef06-112">Метод **имедиасампле::-Point** возвращает указатель на первый байт необработанных данных.</span><span class="sxs-lookup"><span data-stu-id="cef06-112">The **IMediaSample::GetPointer** method returns a pointer to the first byte of the raw data.</span></span> <span data-ttu-id="cef06-113">Для несжатых кадров эти данные состоят из пикселов, которые могут быть доступны или изменены непосредственно фильтром.</span><span class="sxs-lookup"><span data-stu-id="cef06-113">For uncompressed frames, this data consists of pixels that can be accessed or modified directly by the filter.</span></span> <span data-ttu-id="cef06-114">В следующих разделах содержатся общие сведения, которые помогут эффективно работать с данными DIB.</span><span class="sxs-lookup"><span data-stu-id="cef06-114">The following sections provide background information that will help you work effectively with DIB data in this manner.</span></span>

> [!Note]  
> <span data-ttu-id="cef06-115">Можно также изменить биты с помощью функций GDI, GDI+, DirectDraw или Direct3D, но эти методы выходят за рамки этой статьи.</span><span class="sxs-lookup"><span data-stu-id="cef06-115">You can also modify the bits by using GDI, GDI+, DirectDraw or Direct3D functions, but these techniques are beyond the scope of this article.</span></span>

 

<span data-ttu-id="cef06-116">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="cef06-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="cef06-117">Сверху вниз и Bottom-Up DIB</span><span class="sxs-lookup"><span data-stu-id="cef06-117">Top-Down vs. Bottom-Up DIBs</span></span>](top-down-vs--bottom-up-dibs.md)
-   [<span data-ttu-id="cef06-118">Работа с 16-разрядным RGB</span><span class="sxs-lookup"><span data-stu-id="cef06-118">Working with 16-bit RGB</span></span>](working-with-16-bit-rgb.md)

 

 



