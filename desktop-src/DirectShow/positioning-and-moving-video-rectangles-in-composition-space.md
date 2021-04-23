---
title: Размещение и перемещение прямоугольников видео в пространстве композиции
description: Позиционирование и перемещение прямоугольников видео в пространстве композиции
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96955fc2107036299ab6f530eeda76374a0a0315
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909632"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a><span data-ttu-id="a6aab-103">Размещение и перемещение прямоугольников видео в пространстве композиции</span><span class="sxs-lookup"><span data-stu-id="a6aab-103">Position and move video rectangles in composition space</span></span>

<span data-ttu-id="a6aab-104">Когда VMR смешивает несколько входных потоков, каждый поток размещается в нормализованном прямоугольнике с именем "пространство композиции".</span><span class="sxs-lookup"><span data-stu-id="a6aab-104">When the VMR mixes multiple input streams, it positions each stream within a normalized rectangle, called "composition space."</span></span> <span data-ttu-id="a6aab-105">В пространстве композиции координаты (0,0, 0,0) в (1,0, 1,0) формируют видимый прямоугольник видео.</span><span class="sxs-lookup"><span data-stu-id="a6aab-105">Within composition space, the coordinates (0.0, 0.0) to (1.0, 1.0) form the visible video rectangle.</span></span> <span data-ttu-id="a6aab-106">Все координаты, находящиеся за пределами этого прямоугольника, обрезаются.</span><span class="sxs-lookup"><span data-stu-id="a6aab-106">Any coordinates that fall outside of this rectangle are clipped.</span></span>

<span data-ttu-id="a6aab-107">Приложение может выполнять специальные эффекты при перемещении, растяжении и сжатии видео из входного потока, изменяя прямоугольник назначения в пространстве композиции для этого потока.</span><span class="sxs-lookup"><span data-stu-id="a6aab-107">An application can perform special effects with moving, stretching, and shrinking the video from an input stream, by changing the destination rectangle in composition space for that stream.</span></span> <span data-ttu-id="a6aab-108">Если размер указанного прямоугольника отличается от размера собственного видеопрямоугольника, то собственное видео будет сжато или растянуто по размеру.</span><span class="sxs-lookup"><span data-stu-id="a6aab-108">If the specified rectangle is a different size than the native video rectangle, the native video will be shrunk or stretched to fit.</span></span> <span data-ttu-id="a6aab-109">Прямоугольник назначения задается путем вызова метода [**ивмрмиксерконтрол:: сетаутпутрект**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) .</span><span class="sxs-lookup"><span data-stu-id="a6aab-109">The destination rectangle is specified by calling the [**IVMRMixerControl::SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) method.</span></span>

<span data-ttu-id="a6aab-110">Например, предположим, что поток 0 (соответствующий ПИН-коду 0) содержит основной видеопоток, а поток 1 (соответствующий ПИН-коду 1) содержит вторичное видео.</span><span class="sxs-lookup"><span data-stu-id="a6aab-110">For example, assume that stream 0 (which corresponds to pin 0) contains the main video stream, and stream 1 (which corresponds to pin 1) contains a secondary video.</span></span> <span data-ttu-id="a6aab-111">Поток 1 может располагаться полностью, указывая нормализованный прямоугольник {-1.0 f, 0,0 f, 0,0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="a6aab-111">Stream 1 can be positioned completely offscreen by specifying a normalized rectangle of { -1.0f, 0.0f, 0.0f, 1.0f }.</span></span> <span data-ttu-id="a6aab-112">Затем поток 1 можно переместить в видимую область, изменив левую и правую части прямоугольника при последующих вызовах **сетаутпутрект**:</span><span class="sxs-lookup"><span data-stu-id="a6aab-112">Stream 1 can then be moved into the visible area by modifying the left and right sides of the rectangle on successive calls to **SetOutputRect**:</span></span>



| <span data-ttu-id="a6aab-113">Метка</span><span class="sxs-lookup"><span data-stu-id="a6aab-113">Label</span></span> | <span data-ttu-id="a6aab-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a6aab-114">Value</span></span> |
|--------|-----------------------------|
| <span data-ttu-id="a6aab-115">время;</span><span class="sxs-lookup"><span data-stu-id="a6aab-115">Time</span></span>   | <span data-ttu-id="a6aab-116">Прямоугольник</span><span class="sxs-lookup"><span data-stu-id="a6aab-116">Rectangle</span></span>                   |
| <span data-ttu-id="a6aab-117">t + 0</span><span class="sxs-lookup"><span data-stu-id="a6aab-117">t + 0</span></span>  | <span data-ttu-id="a6aab-118">{-1.0 f, 0,0 f, 0,0 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="a6aab-118">{ -1.0f, 0.0f, 0.0f, 1.0f }</span></span> |
| <span data-ttu-id="a6aab-119">t + 1</span><span class="sxs-lookup"><span data-stu-id="a6aab-119">t + 1</span></span>  | <span data-ttu-id="a6aab-120">{-0.9 f, 0,0 f, 0,1 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="a6aab-120">{ -0.9f, 0.0f, 0.1f, 1.0f }</span></span> |
| <span data-ttu-id="a6aab-121">t + 2</span><span class="sxs-lookup"><span data-stu-id="a6aab-121">t + 2</span></span>  | <span data-ttu-id="a6aab-122">{-0,8 f, 0,0 f, 0,2 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="a6aab-122">{ -0.8f, 0.0f, 0.2f, 1.0f }</span></span> |
| <span data-ttu-id="a6aab-123">...</span><span class="sxs-lookup"><span data-stu-id="a6aab-123">...</span></span>    | <span data-ttu-id="a6aab-124">...</span><span class="sxs-lookup"><span data-stu-id="a6aab-124">...</span></span>                         |
| <span data-ttu-id="a6aab-125">t + 10</span><span class="sxs-lookup"><span data-stu-id="a6aab-125">t + 10</span></span> | <span data-ttu-id="a6aab-126">{0.0 f, 0,0 f, 1,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="a6aab-126">{ 0.0f, 0.0f, 1.0f, 1.0f }</span></span>  |



 

![Перемещение видеопотока в пространстве композиции](images/composition-space.png)

<span data-ttu-id="a6aab-128">В момент времени t + 10 видео из потока 1 отображается полностью.</span><span class="sxs-lookup"><span data-stu-id="a6aab-128">At time t+10, the video from stream 1 is completely visible.</span></span> <span data-ttu-id="a6aab-129">В этом примере собственный размер потока 1 поддерживался во время перемещения.</span><span class="sxs-lookup"><span data-stu-id="a6aab-129">In this example, the native size of stream 1 was maintained while it was moving.</span></span> <span data-ttu-id="a6aab-130">Можно также растянуть или сжать прямоугольник, чтобы получить интересные эффекты.</span><span class="sxs-lookup"><span data-stu-id="a6aab-130">You could also stretch or shrink the rectangle to produce interesting effects.</span></span> <span data-ttu-id="a6aab-131">Можно также перевернуть видео по вертикали, указав большее значение для верхней границы или зеркальное отображение видео по горизонтали, указав большее значение слева.</span><span class="sxs-lookup"><span data-stu-id="a6aab-131">You can also flip the video vertically, by specifying a greater value for the top than the bottom, or mirror the video horizontally, by specifying a greater value for the left than the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6aab-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a6aab-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6aab-133">Использование режима смешения VMR</span><span class="sxs-lookup"><span data-stu-id="a6aab-133">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



