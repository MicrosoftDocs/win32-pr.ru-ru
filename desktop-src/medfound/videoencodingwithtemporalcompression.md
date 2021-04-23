---
description: Кодирование видео с использованием временного сжатия
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Кодирование видео с временным сжатием (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee107d8bf6b1ef6b1700abff105b0bdb79f72f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702023"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a><span data-ttu-id="85c8b-103">Кодирование видео с временным сжатием (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="85c8b-103">Video Encoding with Temporal Compression (Microsoft Media Foundation)</span></span>

<span data-ttu-id="85c8b-104">Для достижения максимально возможного коэффициента сжатия видеокодеки Windows Media используют *временное сжатие*.</span><span class="sxs-lookup"><span data-stu-id="85c8b-104">To achieve the highest compression ratios possible, the Windows Media Video codecs use *temporal compression*.</span></span> <span data-ttu-id="85c8b-105">Временное сжатие — это способ уменьшения размера сжатого видео без кодирования каждого кадра в виде полного образа.</span><span class="sxs-lookup"><span data-stu-id="85c8b-105">Temporal compression is a technique of reducing compressed video size by not encoding each frame as a complete image.</span></span> <span data-ttu-id="85c8b-106">Полностью закодированные кадры (как и статическое изображение) называются *опорными кадрами*.</span><span class="sxs-lookup"><span data-stu-id="85c8b-106">The frames that are encoded completely (like a static image) are called *key frames*.</span></span> <span data-ttu-id="85c8b-107">Все остальные кадры в видео представлены данными, указывающими изменение с момента последнего кадра.</span><span class="sxs-lookup"><span data-stu-id="85c8b-107">All other frames in the video are represented by data specifying the change since the last frame.</span></span> <span data-ttu-id="85c8b-108">Эти кадры называются *разностными кадрами*.</span><span class="sxs-lookup"><span data-stu-id="85c8b-108">These frames are called *delta frames*.</span></span>

<span data-ttu-id="85c8b-109">Объем сжатия, который можно достичь с помощью временного сжатия, зависит от содержимого.</span><span class="sxs-lookup"><span data-stu-id="85c8b-109">The amount of compression that can be achieved using temporal compression depends upon the content.</span></span> <span data-ttu-id="85c8b-110">Если видео статичное, без большого количества движений или других изменений в изображении, для каждого ключевого кадра можно создать множество разностных кадров.</span><span class="sxs-lookup"><span data-stu-id="85c8b-110">If the video is static, without a lot of motion or other changes in image, many delta frames can be created for each key frame.</span></span> <span data-ttu-id="85c8b-111">Чем больше использованных разностных кадров, тем меньше закодированного видеопотока.</span><span class="sxs-lookup"><span data-stu-id="85c8b-111">The more delta frames that are used, the smaller the encoded video stream.</span></span> <span data-ttu-id="85c8b-112">Однако если видео является динамическим, с большим количеством движений или изменением цветов, преимущество использования временного сжатия меньше.</span><span class="sxs-lookup"><span data-stu-id="85c8b-112">However, if the video is dynamic, with lots of motion or changing colors, the benefit of using temporal compression is smaller.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85c8b-113">См. также</span><span class="sxs-lookup"><span data-stu-id="85c8b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85c8b-114">Работа с видео</span><span class="sxs-lookup"><span data-stu-id="85c8b-114">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



