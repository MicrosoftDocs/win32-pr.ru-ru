---
title: Скорость
description: Скорость
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- Windows Media Format SDK, разрядные скорости
- Расширенный формат систем (ASF), скорость передачи
- ASF (Расширенный системный формат), скорость передачи
- скорость, о.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d793be8fe04746a61eea48bcf066d95d641221a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779247"
---
# <a name="bit-rate"></a><span data-ttu-id="c0a68-107">Скорость</span><span class="sxs-lookup"><span data-stu-id="c0a68-107">Bit Rate</span></span>

<span data-ttu-id="c0a68-108">Скорость потока — это объем данных в секунду, доставляемый из ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="c0a68-108">Bit rate refers to the amount of data per second that is delivered from an ASF file.</span></span> <span data-ttu-id="c0a68-109">Показатели скорости в битах в секунду (бит/с) или килобитах в секунду (кбит/с).</span><span class="sxs-lookup"><span data-stu-id="c0a68-109">Bit rate measurements are in bits per second (bps) or kilobits per second (Kbps).</span></span> <span data-ttu-id="c0a68-110">Скорость потока часто путают с пропускной способностью, которая представляет собой измерение мощности передачи данных в сети.</span><span class="sxs-lookup"><span data-stu-id="c0a68-110">Bit rate is often confused with bandwidth, which is a measurement of the data transfer capacity of a network.</span></span> <span data-ttu-id="c0a68-111">Пропускная способность также измеряется в бит/с и кбит/с.</span><span class="sxs-lookup"><span data-stu-id="c0a68-111">Bandwidth is also measured in bps and Kbps.</span></span>

<span data-ttu-id="c0a68-112">Пакет Windows Media Format SDK можно использовать для создания приложений, обеспечивающих потоковую передачу содержимого на основе Windows Media из расположений в Интернете или интрасети.</span><span class="sxs-lookup"><span data-stu-id="c0a68-112">The Windows Media Format SDK can be used to create applications that deliver streaming Windows Media-based content from Internet or intranet locations.</span></span> <span data-ttu-id="c0a68-113">При потоковой передаче данных по сети или через Интернет скорость работы конечных пользователей важна.</span><span class="sxs-lookup"><span data-stu-id="c0a68-113">When you are streaming data across a network or the Internet, the bit rate is of vital importance to the end-user experience.</span></span> <span data-ttu-id="c0a68-114">Если пропускная способность, доступная в сети, меньше, чем скорость файла ASF, воспроизведение файла будет каким-то образом прервано.</span><span class="sxs-lookup"><span data-stu-id="c0a68-114">If the bandwidth available to the network is less than the bit rate of the ASF file, the playback of the file will be interrupted in some way.</span></span> <span data-ttu-id="c0a68-115">Как правило, недостаточная пропускная способность приведет к пропуску любого из этих примеров или приостановки воспроизведения в процессе буферизации данных.</span><span class="sxs-lookup"><span data-stu-id="c0a68-115">Usually, insufficient bandwidth will result in either samples being skipped, or a pause in playback while more data is buffered.</span></span>

<span data-ttu-id="c0a68-116">Каждому файлу ASF во время создания назначается значение скорости, основанное на типе и количестве потоков, включенных в используемый профиль.</span><span class="sxs-lookup"><span data-stu-id="c0a68-116">Every ASF file is assigned a bit rate value at the time of creation, based upon the type and number of streams that are included in the profile used.</span></span> <span data-ttu-id="c0a68-117">Отдельные потоки имеют собственные скорости.</span><span class="sxs-lookup"><span data-stu-id="c0a68-117">Individual streams have their own bit rates.</span></span> <span data-ttu-id="c0a68-118">Скорость потока может быть постоянной (исходные данные сжимаются таким образом, чтобы поддерживать постоянный поток данных с одинаковой частотой) или переменной (исходные данные сжимаются таким образом, чтобы поддерживать одинаковое качество в течение всего времени, даже если это может означать неравномерное выполнение потока данных).</span><span class="sxs-lookup"><span data-stu-id="c0a68-118">Bit rates can be constant (the original data is compressed in such a way as to maintain a constant flow of data at approximately the same rate) or variable (the original data is compressed in such a way as to maintain the same quality throughout, even though this may mean uneven data flow).</span></span> <span data-ttu-id="c0a68-119">Различные типы скорости разрядов могут применяться к разным потокам в одном файле.</span><span class="sxs-lookup"><span data-stu-id="c0a68-119">Different bit rate types can be applied to different streams within the same file.</span></span>

<span data-ttu-id="c0a68-120">Вы можете кодировать одно и то же содержимое в несколько различных потоков, каждый из которых имеет разную скорость.</span><span class="sxs-lookup"><span data-stu-id="c0a68-120">You can encode the same content to several different streams, each with a different bit rate.</span></span> <span data-ttu-id="c0a68-121">Затем можно настроить потоки, чтобы они были взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="c0a68-121">Then you can configure the streams so that they are mutually exclusive.</span></span> <span data-ttu-id="c0a68-122">Это позволяет создать один файл, который можно передать пользователям с различной пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="c0a68-122">This enables you to create a single file that can be streamed to users with different bandwidths.</span></span> <span data-ttu-id="c0a68-123">Эта функция называется многоразрядной скоростью или MBR.</span><span class="sxs-lookup"><span data-stu-id="c0a68-123">This feature is called multiple bit rate, or MBR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0a68-124">См. также</span><span class="sxs-lookup"><span data-stu-id="c0a68-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0a68-125">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="c0a68-125">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="c0a68-126">**Кодирование с постоянной скоростью (CBR)**</span><span class="sxs-lookup"><span data-stu-id="c0a68-126">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="c0a68-127">**Входы, потоки и выходные данные**</span><span class="sxs-lookup"><span data-stu-id="c0a68-127">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="c0a68-128">**Профили**</span><span class="sxs-lookup"><span data-stu-id="c0a68-128">**Profiles**</span></span>](profiles.md)
</dt> <dt>

[<span data-ttu-id="c0a68-129">**Кодирование переменной скорости (VBR)**</span><span class="sxs-lookup"><span data-stu-id="c0a68-129">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




