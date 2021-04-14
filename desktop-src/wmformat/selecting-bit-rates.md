---
title: Выбор скорости
description: Выбор скорости
ms.assetid: 466524a6-2473-4768-8ae3-0ac18807f88c
keywords:
- профили, выбор скорости
- профили, скорости
- кодеки, выбор скорости
- кодеки, поразрядные скорости
- профили, выбор скорости
- кодеки, выбор скорости
- скорость, выбор
- скорость, профили
- скорость передачи, кодеки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd8c125aacc5add255962ca37e6060af20d66f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328240"
---
# <a name="selecting-bit-rates"></a><span data-ttu-id="ad80c-112">Выбор скорости</span><span class="sxs-lookup"><span data-stu-id="ad80c-112">Selecting Bit Rates</span></span>

<span data-ttu-id="ad80c-113">Для файлов, которые будут передаваться по сети, необходимо тщательно продумать, какие скорости следует использовать.</span><span class="sxs-lookup"><span data-stu-id="ad80c-113">For files that will be streamed over a network, you must consider carefully what bit rates you should use.</span></span> <span data-ttu-id="ad80c-114">В большинстве случаев можно одновременно добавить скорость всех потоков в файле, чтобы получить общее представление о доступной пропускной способности, необходимой для потоковой передачи файла.</span><span class="sxs-lookup"><span data-stu-id="ad80c-114">Under most circumstances you can add the bit rates of all of the streams in a file together to get a general idea of the available bandwidth required to stream the file.</span></span> <span data-ttu-id="ad80c-115">Однако для каждого потока также требуется определенный объем издержек.</span><span class="sxs-lookup"><span data-stu-id="ad80c-115">However, a certain amount of overhead is also required for each stream.</span></span> <span data-ttu-id="ad80c-116">Эти дополнительные сведения приведены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ad80c-116">This overhead is summarized in the following table.</span></span>



| <span data-ttu-id="ad80c-117">Диапазон битовой скорости (кбит/с)</span><span class="sxs-lookup"><span data-stu-id="ad80c-117">Bit-rate range (Kbps)</span></span> | <span data-ttu-id="ad80c-118">Дополнительная пропускная способность, необходимая для дополнительной нагрузки (кбит/с)</span><span class="sxs-lookup"><span data-stu-id="ad80c-118">Additional bandwidth required for overhead (Kbps)</span></span> |
|-----------------------|---------------------------------------------------|
| <span data-ttu-id="ad80c-119">10 – 16</span><span class="sxs-lookup"><span data-stu-id="ad80c-119">10 – 16</span></span>               | <span data-ttu-id="ad80c-120">3</span><span class="sxs-lookup"><span data-stu-id="ad80c-120">3</span></span>                                                 |
| <span data-ttu-id="ad80c-121">17 – 30</span><span class="sxs-lookup"><span data-stu-id="ad80c-121">17 – 30</span></span>               | <span data-ttu-id="ad80c-122">4</span><span class="sxs-lookup"><span data-stu-id="ad80c-122">4</span></span>                                                 |
| <span data-ttu-id="ad80c-123">31 – 45</span><span class="sxs-lookup"><span data-stu-id="ad80c-123">31 – 45</span></span>               | <span data-ttu-id="ad80c-124">5</span><span class="sxs-lookup"><span data-stu-id="ad80c-124">5</span></span>                                                 |
| <span data-ttu-id="ad80c-125">46 – 70</span><span class="sxs-lookup"><span data-stu-id="ad80c-125">46 – 70</span></span>               | <span data-ttu-id="ad80c-126">6</span><span class="sxs-lookup"><span data-stu-id="ad80c-126">6</span></span>                                                 |
| <span data-ttu-id="ad80c-127">71 – 225</span><span class="sxs-lookup"><span data-stu-id="ad80c-127">71 – 225</span></span>              | <span data-ttu-id="ad80c-128">7</span><span class="sxs-lookup"><span data-stu-id="ad80c-128">7</span></span>                                                 |
| <span data-ttu-id="ad80c-129">>225</span><span class="sxs-lookup"><span data-stu-id="ad80c-129">>225</span></span>               | <span data-ttu-id="ad80c-130">9</span><span class="sxs-lookup"><span data-stu-id="ad80c-130">9</span></span>                                                 |



 

<span data-ttu-id="ad80c-131">Обычные затраты, необходимые для потока, не занимают расширения модулей данных.</span><span class="sxs-lookup"><span data-stu-id="ad80c-131">The normal overhead required for a stream does not take data unit extensions into account.</span></span> <span data-ttu-id="ad80c-132">Каждое расширение единицы обработки данных добавляет к размеру образца, к которому он присоединен.</span><span class="sxs-lookup"><span data-stu-id="ad80c-132">Every data unit extension adds to the size of the sample to which it is attached.</span></span> <span data-ttu-id="ad80c-133">В зависимости от типа расширения единицы данных это может значительно увеличить скорость потока.</span><span class="sxs-lookup"><span data-stu-id="ad80c-133">Depending upon the type of data unit extension, this can greatly increase the bit rate for the stream.</span></span>

<span data-ttu-id="ad80c-134">Также необходимо учитывать, что теоретическая максимальная пропускная способность, доступная через сетевое подключение, не является практичной целевой скоростью.</span><span class="sxs-lookup"><span data-stu-id="ad80c-134">You must also consider that the theoretical maximum bandwidth available over a network connection is not a practical target bit rate.</span></span> <span data-ttu-id="ad80c-135">Средняя доступная пропускная способность для любого конкретного подключения будет значительно меньше пропускной способности подключения из-за сетевого трафика и многих других факторов.</span><span class="sxs-lookup"><span data-stu-id="ad80c-135">The average available bandwidth for any given connection falls well short of the bandwidth capacity of the connection, because of network traffic and many other factors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad80c-136">См. также</span><span class="sxs-lookup"><span data-stu-id="ad80c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad80c-137">**Проектирование профилей**</span><span class="sxs-lookup"><span data-stu-id="ad80c-137">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> </dl>

 

 




