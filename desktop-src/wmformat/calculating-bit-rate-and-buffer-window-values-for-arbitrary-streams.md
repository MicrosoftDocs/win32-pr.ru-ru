---
title: Вычисление скорости потока и значений окна буфера для произвольных потоков
description: Вычисление скорости потока и значений окна буфера для произвольных потоков
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- потоки, скорость передачи
- кодеки, вычисление битовых ставок для произвольных потоков
- скорость, вычисление для произвольных потоков
- потоки, вычисление битовых ставок для произвольных потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d704352d414b1fe5079fb068593c2d0d8b2f8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067400"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a><span data-ttu-id="aab14-107">Вычисление скорости потока и значений окна буфера для произвольных потоков</span><span class="sxs-lookup"><span data-stu-id="aab14-107">Calculating Bit Rate and Buffer Window Values for Arbitrary Streams</span></span>

<span data-ttu-id="aab14-108">Вычисление правильной скорости потока и окна буфера для произвольного типа потоков не является точным науком.</span><span class="sxs-lookup"><span data-stu-id="aab14-108">Calculating the proper bit rate and buffer window for an arbitrary stream type is not an exact science.</span></span> <span data-ttu-id="aab14-109">Один из простых подходов заключается в том, чтобы установить скорость в соответствии с размером потока, деленного на его длину (в секундах).</span><span class="sxs-lookup"><span data-stu-id="aab14-109">One simple approach is to set the bit rate to match the size of the stream divided by its length, in seconds.</span></span> <span data-ttu-id="aab14-110">Например, поток, содержащий 68000 бит, продолжающийся 20 секунд, может иметь скорость в 3400 бит/с (68000 бит/20 секунд = 3400 бит в секунду).</span><span class="sxs-lookup"><span data-stu-id="aab14-110">For example, a stream containing a total of 68000 bits lasting 20 seconds might have a bit rate of 3400 bits per second (68000 bits / 20 seconds = 3400 bits per second).</span></span>

<span data-ttu-id="aab14-111">Проблема, связанная с этим простым методом назначения битовой скорости, заключается в том, что она не учитывает распределение данных в потоке.</span><span class="sxs-lookup"><span data-stu-id="aab14-111">The problem with this simple technique of assigning bit rate is that it does not take into account the distribution of data within the stream.</span></span> <span data-ttu-id="aab14-112">Многие произвольные потоки содержат большие объемы данных с интервалами на временной шкале файла.</span><span class="sxs-lookup"><span data-stu-id="aab14-112">Many arbitrary streams contain larger amounts of data at intervals along the timeline of the file.</span></span> <span data-ttu-id="aab14-113">Например, потоки изображений имеют довольно большие примеры, но обычно находятся в нескольких секундах.</span><span class="sxs-lookup"><span data-stu-id="aab14-113">Image streams, for example, have samples that are rather large, but are usually spaced several seconds apart.</span></span> <span data-ttu-id="aab14-114">Окно буфера должно быть установлено, чтобы гарантировать, что буфер не будет переполнен.</span><span class="sxs-lookup"><span data-stu-id="aab14-114">The buffer window must be set to ensure that the buffer will not overflow.</span></span>

<span data-ttu-id="aab14-115">Чтобы проверить окно буфера, умножьте скорость потока (бит в секунду) на окно буфера (в секундах) и разделите на 1000, чтобы получить размер буфера в битах.</span><span class="sxs-lookup"><span data-stu-id="aab14-115">To check the buffer window, multiply the bit rate (bits per second) by the buffer window (in seconds) and divide by 1000 to get the size, in bits, of the buffer for the stream.</span></span> <span data-ttu-id="aab14-116">Затем убедитесь, что размер буфера достаточно велик для хранения любой комбинации образцов в потоке, которые меньше, чем окно буфера, разбивается на время презентации.</span><span class="sxs-lookup"><span data-stu-id="aab14-116">Then make sure that the buffer size is large enough to hold any combination of samples in the stream that are less than the buffer window apart in presentation time.</span></span> <span data-ttu-id="aab14-117">Если вы сомневаетесь, задайте оба значения немного выше, чем вы считаете, что они нужны.</span><span class="sxs-lookup"><span data-stu-id="aab14-117">When in doubt, set both values a little higher than you think you need them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aab14-118">См. также</span><span class="sxs-lookup"><span data-stu-id="aab14-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aab14-119">**Буферизация содержимого**</span><span class="sxs-lookup"><span data-stu-id="aab14-119">**Buffering Content**</span></span>](buffering-content.md)
</dt> <dt>

[<span data-ttu-id="aab14-120">**Настройка произвольных типов потоков**</span><span class="sxs-lookup"><span data-stu-id="aab14-120">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




