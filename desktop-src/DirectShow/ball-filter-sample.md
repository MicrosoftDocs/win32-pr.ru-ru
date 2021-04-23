---
description: Образец фильтра шарика
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Образец фильтра шарика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b80301b233f0c1e74933c93fe86a0e1878458e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895082"
---
# <a name="ball-filter-sample"></a><span data-ttu-id="fdadd-103">Образец фильтра шарика</span><span class="sxs-lookup"><span data-stu-id="fdadd-103">Ball Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="fdadd-104">Описание</span><span class="sxs-lookup"><span data-stu-id="fdadd-104">Description</span></span>

<span data-ttu-id="fdadd-105">Фильтр шарика — это фильтр источника видео, который создает изображение вращающегося шарика.</span><span class="sxs-lookup"><span data-stu-id="fdadd-105">The Ball Filter is a video source filter that produces an image of a bouncing ball.</span></span> <span data-ttu-id="fdadd-106">Этот пример иллюстрирует согласование формата и использование базовых классов фильтров источника [**ксаурце**](csource.md) и [**ксаурцестреам**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="fdadd-106">This sample illustrates format negotiation and the use of the source filter base classes [**CSource**](csource.md) and [**CSourceStream**](csourcestream.md).</span></span>

<span data-ttu-id="fdadd-107">Код в Фбалл. h и Фбалл. cpp управляет интерфейсами фильтра.</span><span class="sxs-lookup"><span data-stu-id="fdadd-107">The code in Fball.h and Fball.cpp manages the filter interfaces.</span></span> <span data-ttu-id="fdadd-108">Эти два файла содержат примерно минимальный код, необходимый для фильтра источника.</span><span class="sxs-lookup"><span data-stu-id="fdadd-108">Those two files contain approximately the minimum code required for a source filter.</span></span> <span data-ttu-id="fdadd-109">Файлы шара. h и шар. cpp содержат код, который передает шарик.</span><span class="sxs-lookup"><span data-stu-id="fdadd-109">The Ball.h and Ball.cpp files contain the code that bounces the ball.</span></span>

<span data-ttu-id="fdadd-110">Этот фильтр имеет один выходной ПИН-код, который предоставляет видеопоток, показывающий шарик, движущийся в кадре.</span><span class="sxs-lookup"><span data-stu-id="fdadd-110">This filter has a single output pin, which provides a video stream that shows a ball bouncing around in the frame.</span></span> <span data-ttu-id="fdadd-111">Фильтр шарика также принимает запросы управления качеством от подчиненного фильтра, который иллюстрирует простую стратегию управления качеством.</span><span class="sxs-lookup"><span data-stu-id="fdadd-111">The Ball filter also accepts quality management requests from the downstream filter, which illustrates a simple quality management strategy.</span></span> <span data-ttu-id="fdadd-112">Этот фильтр реализует интерфейс [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) для этой цели.</span><span class="sxs-lookup"><span data-stu-id="fdadd-112">This filter implements the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface for that purpose.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="fdadd-113">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="fdadd-113">Downloading the Sample</span></span>

<span data-ttu-id="fdadd-114">Чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fdadd-114">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="fdadd-115">Этот пример устанавливается по следующему пути: \[ *корневые* \] \\ примеры SDK \\ мультимедийные \\ образцы \\ DirectShow \\ .</span><span class="sxs-lookup"><span data-stu-id="fdadd-115">This sample is installed under the following path: \[*SDK Root*\]\\Samples\\Multimedia\\DirectShow\\Filters\\Ball.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdadd-116">См. также</span><span class="sxs-lookup"><span data-stu-id="fdadd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdadd-117">Примеры DirectShow</span><span class="sxs-lookup"><span data-stu-id="fdadd-117">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



