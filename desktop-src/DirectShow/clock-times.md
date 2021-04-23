---
description: Время суток
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Время суток
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0639fd2b38e312f30f932fcf508427cd71c054
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416488"
---
# <a name="clock-times"></a><span data-ttu-id="2d5b1-103">Время суток</span><span class="sxs-lookup"><span data-stu-id="2d5b1-103">Clock Times</span></span>

<span data-ttu-id="2d5b1-104">DirectShow определяет два связанных времени: время ссылки и время потока.</span><span class="sxs-lookup"><span data-stu-id="2d5b1-104">DirectShow defines two related clock times: reference time and stream time.</span></span>

-   <span data-ttu-id="2d5b1-105">*Время ссылки* — это абсолютное время, возвращаемое ссылочным временем.</span><span class="sxs-lookup"><span data-stu-id="2d5b1-105">*Reference time* is the absolute time returned by the reference clock.</span></span> <span data-ttu-id="2d5b1-106">(См. раздел [эталонные часы](reference-clocks.md).)</span><span class="sxs-lookup"><span data-stu-id="2d5b1-106">(See [Reference Clocks](reference-clocks.md).)</span></span>
-   <span data-ttu-id="2d5b1-107">*Время потока* определяется относительно времени последнего запуска графа.</span><span class="sxs-lookup"><span data-stu-id="2d5b1-107">*Stream time* is defined relative to when the graph last started running.</span></span>
    -   <span data-ttu-id="2d5b1-108">Во время работы графа потоковая передача равна времени ссылки минус время начала.</span><span class="sxs-lookup"><span data-stu-id="2d5b1-108">While the graph is running, stream time equals reference time minus start time.</span></span>
    -   <span data-ttu-id="2d5b1-109">Пока работа графа приостановлена, время потока остается в потоке, когда он был приостановлен.</span><span class="sxs-lookup"><span data-stu-id="2d5b1-109">While the graph is paused, stream time remains at the stream time when it was paused.</span></span>
    -   <span data-ttu-id="2d5b1-110">После операции поиска время потока сбрасывается в ноль.</span><span class="sxs-lookup"><span data-stu-id="2d5b1-110">After a seek operation, stream time resets to zero.</span></span>
    -   <span data-ttu-id="2d5b1-111">Пока граф остановлен, потоковое время не определено.</span><span class="sxs-lookup"><span data-stu-id="2d5b1-111">While the graph is stopped, stream time is undefined.</span></span>

<span data-ttu-id="2d5b1-112">Если образец носителя имеет метку времени *t*, это означает, что выборка должна быть визуализирована во время потока *t*.</span><span class="sxs-lookup"><span data-stu-id="2d5b1-112">When a media sample has a time stamp *t*, it means the sample should be rendered at stream time *t*.</span></span> <span data-ttu-id="2d5b1-113">По этой причине потоковое время также называется *временем презентации*.</span><span class="sxs-lookup"><span data-stu-id="2d5b1-113">For this reason, stream time is also called *presentation time*.</span></span>

<span data-ttu-id="2d5b1-114">Когда приложение вызывает [**имедиаконтрол:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) для запуска графа фильтра, диспетчер графа фильтров вызывает [**Имедиафилтер:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) для каждого фильтра.</span><span class="sxs-lookup"><span data-stu-id="2d5b1-114">When an application calls [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the filter graph, the Filter Graph Manager calls [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) on each filter.</span></span> <span data-ttu-id="2d5b1-115">Чтобы компенсировать незначительное время, затрачиваемое на выполнение фильтров, диспетчер графов фильтров указывает время начала в будущем.</span><span class="sxs-lookup"><span data-stu-id="2d5b1-115">To compensate for the slight amount of time it takes for the filters to start running, the Filter Graph Manager specifies a start time slightly in the future.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d5b1-116">См. также</span><span class="sxs-lookup"><span data-stu-id="2d5b1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d5b1-117">Время и часы в DirectShow</span><span class="sxs-lookup"><span data-stu-id="2d5b1-117">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="2d5b1-118">Метки времени</span><span class="sxs-lookup"><span data-stu-id="2d5b1-118">Time Stamps</span></span>](time-stamps.md)
</dt> </dl>

 

 



