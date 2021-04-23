---
title: Управление задержкой записи
description: Управление задержкой записи
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- Расширенный системный формат (ASF), Управление задержкой записи
- ASF (Расширенный системный формат), Управление задержкой записи
- Расширенный системный формат (ASF), задержка записи
- ASF (Расширенный системный формат), задержка записи
- Задержка записи
- Задержка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3260be03344f1bf13252007b10614746ceda3e96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105681582"
---
# <a name="to-manage-writer-latency"></a><span data-ttu-id="a624c-109">Управление задержкой записи</span><span class="sxs-lookup"><span data-stu-id="a624c-109">To Manage Writer Latency</span></span>

<span data-ttu-id="a624c-110">Для обработки образцов модуль записи занимает некоторое время.</span><span class="sxs-lookup"><span data-stu-id="a624c-110">It takes time for the writer to process samples.</span></span> <span data-ttu-id="a624c-111">Промежуток времени между передачей образца входных данных и записью образца вывода называется задержкой модуля записи.</span><span class="sxs-lookup"><span data-stu-id="a624c-111">The amount of time between passing an input sample and the writing of an output sample is called the latency of the writer.</span></span> <span data-ttu-id="a624c-112">Ряд факторов влияет на задержку записи, и его можно сократить несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="a624c-112">A number of factors contribute to writer latency, and you can reduce it in several ways.</span></span>

<span data-ttu-id="a624c-113">Наиболее очевидным фактором, связанным с задержкой модуля записи, является время, затрачиваемое на сжатие образца.</span><span class="sxs-lookup"><span data-stu-id="a624c-113">The most obvious factor involved in writer latency is the time it takes to compress a sample.</span></span> <span data-ttu-id="a624c-114">В большинстве случаев вы будете иметь немало контроля над этим.</span><span class="sxs-lookup"><span data-stu-id="a624c-114">Under most circumstances, you will have little or no control over this.</span></span> <span data-ttu-id="a624c-115">Если пропускная способность не важна, снизить задержку можно с помощью меньшего сжатия.</span><span class="sxs-lookup"><span data-stu-id="a624c-115">If bandwidth is not a big concern, you can reduce latency by using less compression.</span></span> <span data-ttu-id="a624c-116">Конечно, можно достичь наименьшей задержки, передавая уже сжатые образцы.</span><span class="sxs-lookup"><span data-stu-id="a624c-116">Of course, you can achieve the least latency by passing samples that are already compressed.</span></span>

<span data-ttu-id="a624c-117">Следующий фактор, в котором обычно есть управление, — это порядок, в котором образцы передаются модулю чтения.</span><span class="sxs-lookup"><span data-stu-id="a624c-117">The next factor, and one over which you usually do have control, is the order in which samples are passed to the reader.</span></span> <span data-ttu-id="a624c-118">Можно достичь более высокой задержки, передав образцы в порядке времени презентации и убедившись, что входные образцы хорошо синхронизированы между всеми входными потоками.</span><span class="sxs-lookup"><span data-stu-id="a624c-118">You can achieve better latency by passing samples in order of presentation time, and by ensuring that the input samples are well synchronized between all input streams.</span></span> <span data-ttu-id="a624c-119">Чем больше разница во времени показа между образцами для различных потоков, тем больше задержка будет возникать.</span><span class="sxs-lookup"><span data-stu-id="a624c-119">The greater the discrepancy in presentation times between the samples for different streams, the more latency will result.</span></span> <span data-ttu-id="a624c-120">Вы можете задать максимальное значение для несоответствия между входными образцами, вызвав [**ивмвритерадванцед:: сетсинктолеранце**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span><span class="sxs-lookup"><span data-stu-id="a624c-120">You can set a maximum for the discrepancy between input samples by calling [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a624c-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a624c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a624c-122">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="a624c-122">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




