---
title: Время презентации
description: Время презентации
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- Пакет SDK для формата Windows Media, время презентации
- Расширенный формат систем (ASF), время презентации
- ASF (Расширенный системный формат), время презентации
- время презентации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc88dbba93d1fc68905a4bfea92328a4ef600eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331707"
---
# <a name="presentation-time"></a><span data-ttu-id="38c89-107">Время презентации</span><span class="sxs-lookup"><span data-stu-id="38c89-107">Presentation Time</span></span>

<span data-ttu-id="38c89-108">Время презентации — это измерение времени от первой выборки первого потока в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="38c89-108">A presentation time is a measurement of time from the first sample of the first stream in an ASF file.</span></span> <span data-ttu-id="38c89-109">Это измерение, а также большинство других измерений времени, используемых объектами этого пакета SDK, находятся в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="38c89-109">This measurement, as well as most other measurements of time used by the objects of this SDK, is in 100-nanosecond units.</span></span> <span data-ttu-id="38c89-110">Время презентации очень важно, так как они позволяют синхронизировать различные потоки в файле.</span><span class="sxs-lookup"><span data-stu-id="38c89-110">Presentation times are important because they enable the various streams in a file to be synchronized.</span></span> <span data-ttu-id="38c89-111">Необходимо указать время презентации для каждого входного примера, передаваемого в модуль записи.</span><span class="sxs-lookup"><span data-stu-id="38c89-111">You must supply a presentation time for each input sample you pass to the writer.</span></span> <span data-ttu-id="38c89-112">С каждым объектом данных в разделе данных ASF-файла связано время презентации.</span><span class="sxs-lookup"><span data-stu-id="38c89-112">Every data object in the data section of an ASF file has a presentation time associated with it.</span></span> <span data-ttu-id="38c89-113">Каждый образец вывода, получаемый модулем чтения, также имеет время презентации.</span><span class="sxs-lookup"><span data-stu-id="38c89-113">Every output sample retrieved by the reader also has a presentation time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38c89-114">См. также</span><span class="sxs-lookup"><span data-stu-id="38c89-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38c89-115">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="38c89-115">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="38c89-116">**Входы, потоки и выходные данные**</span><span class="sxs-lookup"><span data-stu-id="38c89-116">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="38c89-117">**Примеры носителей**</span><span class="sxs-lookup"><span data-stu-id="38c89-117">**Media Samples**</span></span>](media-samples.md)
</dt> </dl>

 

 




