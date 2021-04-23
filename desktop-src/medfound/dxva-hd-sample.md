---
description: Показывает, как использовать высокое определение (ДКСВА-HD) ускорения видео Microsoft DirectX High Definition.
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: Пример ДКСВА-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896570"
---
# <a name="dxva-hd-sample"></a><span data-ttu-id="4ac02-103">Пример ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="4ac02-103">DXVA-HD Sample</span></span>

<span data-ttu-id="4ac02-104">Показывает, как использовать высокое определение (ДКСВА-HD) ускорения видео Microsoft DirectX High Definition.</span><span class="sxs-lookup"><span data-stu-id="4ac02-104">Shows how to use Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span></span>

<span data-ttu-id="4ac02-105">Этот пример по сути является портом [образца DXVA2 \_ видеопрок](dxva2-videoproc-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4ac02-105">This sample is essentially a port of the [DXVA2\_VideoProc Sample](dxva2-videoproc-sample.md).</span></span> <span data-ttu-id="4ac02-106">Он имеет те же базовые функции, и большинство команд клавиатуры одинаковы.</span><span class="sxs-lookup"><span data-stu-id="4ac02-106">It has the same basic functions, and most of the keyboard commands are the same.</span></span>

<span data-ttu-id="4ac02-107">Пример программно создает видео с первичным потоком и подпотоком.</span><span class="sxs-lookup"><span data-stu-id="4ac02-107">The sample programmatically generates video with a primary stream and a substream.</span></span> <span data-ttu-id="4ac02-108">Основной поток отображает SMPTE цветовые полосы.</span><span class="sxs-lookup"><span data-stu-id="4ac02-108">The primary stream displays SMPTE color bars.</span></span> <span data-ttu-id="4ac02-109">Подпоток смешивается с альфа-смешением в основной поток с помощью ключа яркости.</span><span class="sxs-lookup"><span data-stu-id="4ac02-109">The substream is alpha-blended onto the primary stream using luma keying.</span></span> <span data-ttu-id="4ac02-110">Пользователь может изменить параметры обработки видео, включая плоское значение альфа, прямоугольники источника и назначения, настройки цветов и цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="4ac02-110">The user can change the video processing parameters, including the planar alpha value, source and destination rectangles, color adjustments, and color space.</span></span> <span data-ttu-id="4ac02-111">На следующем рисунке показано созданное видео.</span><span class="sxs-lookup"><span data-stu-id="4ac02-111">The following image shows that video that is generated.</span></span>

![снимок экрана с примером дксва-HD](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="4ac02-113">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="4ac02-113">APIs Demonstrated</span></span>

<span data-ttu-id="4ac02-114">В этом примере демонстрируются следующие интерфейсы ДКСВА-HD:</span><span class="sxs-lookup"><span data-stu-id="4ac02-114">This sample demonstrates the following DXVA-HD interfaces:</span></span>

-   [<span data-ttu-id="4ac02-115">**\_Устройство идксвахд**</span><span class="sxs-lookup"><span data-stu-id="4ac02-115">**IDXVAHD\_Device**</span></span>](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [<span data-ttu-id="4ac02-116">**ИДКСВАХД \_ видеопроцессор**</span><span class="sxs-lookup"><span data-stu-id="4ac02-116">**IDXVAHD\_VideoProcessor**</span></span>](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a><span data-ttu-id="4ac02-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4ac02-117">Requirements</span></span>



| <span data-ttu-id="4ac02-118">Продукт</span><span class="sxs-lookup"><span data-stu-id="4ac02-118">Product</span></span>                                                        | <span data-ttu-id="4ac02-119">Version</span><span class="sxs-lookup"><span data-stu-id="4ac02-119">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="4ac02-120">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="4ac02-120">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="4ac02-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4ac02-121">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="4ac02-122">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="4ac02-122">Downloading the Sample</span></span>

<span data-ttu-id="4ac02-123">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).</span><span class="sxs-lookup"><span data-stu-id="4ac02-123">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ac02-124">См. также</span><span class="sxs-lookup"><span data-stu-id="4ac02-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ac02-125">ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="4ac02-125">DXVA-HD</span></span>](dxva-hd.md)
</dt> <dt>

[<span data-ttu-id="4ac02-126">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4ac02-126">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



