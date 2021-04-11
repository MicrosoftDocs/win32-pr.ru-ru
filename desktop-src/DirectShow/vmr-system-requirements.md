---
description: Требования к системе VMR
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: Требования к системе VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d54d6d1604c3e514f3ceef379eaba4a8fa1ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265254"
---
# <a name="vmr-system-requirements"></a><span data-ttu-id="b369d-103">Требования к системе VMR</span><span class="sxs-lookup"><span data-stu-id="b369d-103">VMR System Requirements</span></span>

<span data-ttu-id="b369d-104">VMR использует возможности обработки графики только для экранной карты компьютера. VMR не выполняет никакого смешения или отрисовки видео с помощью хост-процессора, так как это существенно повлияет на частоту кадров и качество отображаемого видео.</span><span class="sxs-lookup"><span data-stu-id="b369d-104">The VMR uses the graphics-processing capabilities of the computer's display card exclusively; the VMR does not perform any blending or rendering of video using the host processor, because to do so would greatly impact the frame rate and quality of the video being displayed.</span></span> <span data-ttu-id="b369d-105">При использовании новых возможностей, предлагаемых VMR, в особенности наложения нескольких видеопотоков и/или образов приложений, Общая производительность сильно зависит от возможностей графического адаптера, используемого на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b369d-105">When taking advantage of the new features offered by the VMR, particularly blending of multiple video streams and/or application images, the overall performance obtained is highly dependent on the capabilities of the graphics card being used on the computer.</span></span> <span data-ttu-id="b369d-106">Графические карты, которые хорошо работают с VMR, имеют встроенную поддержку оборудования.</span><span class="sxs-lookup"><span data-stu-id="b369d-106">Graphics cards that perform well with the VMR have the following hardware support built into them:</span></span>

-   <span data-ttu-id="b369d-107">Поддержка YUV и "не в степени 2" поверхностей текстуры Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b369d-107">Support for YUV and "non-power of 2" Direct3D texture surfaces.</span></span>
-   <span data-ttu-id="b369d-108">Возможность Стретчблт от YUV к поверхностьм RGB DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="b369d-108">The ability to StretchBlt from YUV to RGB DirectDraw surfaces.</span></span>
-   <span data-ttu-id="b369d-109">По крайней мере 16 МБ видеопамяти, если несколько потоков видео будут смешиваться.</span><span class="sxs-lookup"><span data-stu-id="b369d-109">At least 16MB of video memory if multiple video streams are to be blended together.</span></span> <span data-ttu-id="b369d-110">Фактический объем необходимой памяти зависит от размера видеопотоков и разрешения используемого режима экрана.</span><span class="sxs-lookup"><span data-stu-id="b369d-110">The actual amount of memory required is dependent on the image size of the video streams and resolution of the display mode being used.</span></span>
-   <span data-ttu-id="b369d-111">Поддержка оверлея RGB или возможность перехода на поверхность YUV-наложения.</span><span class="sxs-lookup"><span data-stu-id="b369d-111">Support for an RGB overlay or the ability to blend to a YUV overlay surface.</span></span>
-   <span data-ttu-id="b369d-112">Видео с аппаратным ускорением (поддержка ускорения видео DirectX).</span><span class="sxs-lookup"><span data-stu-id="b369d-112">Hardware-accelerated video (support for DirectX Video Acceleration) decoding.</span></span>
-   <span data-ttu-id="b369d-113">Высокая скорость заливки пикселей.</span><span class="sxs-lookup"><span data-stu-id="b369d-113">High pixel fill rates.</span></span>

> [!Note]  
> <span data-ttu-id="b369d-114">VMR требует, чтобы для системного монитора была задана глубина цвета не менее 16 бит.</span><span class="sxs-lookup"><span data-stu-id="b369d-114">The VMR requires that the system monitor be set for a color depth of at least 16 bits.</span></span> <span data-ttu-id="b369d-115">VMR не может быть переведен в состояние выполнения, если для монитора задано значение цвета 256.</span><span class="sxs-lookup"><span data-stu-id="b369d-115">The VMR cannot be put into a run state if the monitor is set for 256 colors.</span></span> <span data-ttu-id="b369d-116">Кроме того, некоторые видеоадаптеры не могут выполнять операции Direct3D, если для дисплея установлено значение 24 бита на пиксель.</span><span class="sxs-lookup"><span data-stu-id="b369d-116">Also, some video cards cannot perform Direct3D operations when the display is set to 24 bits per pixel.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b369d-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b369d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b369d-118">О рендеринге видео</span><span class="sxs-lookup"><span data-stu-id="b369d-118">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



