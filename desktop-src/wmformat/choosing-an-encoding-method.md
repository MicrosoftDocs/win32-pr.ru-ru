---
title: Выбор метода кодирования
description: Выбор метода кодирования
ms.assetid: 095245a6-39eb-4228-86ac-ade94dde3695
keywords:
- профили, выбор методов кодировки
- профили, методы кодирования
- кодеки, выбор методов кодировки
- кодеки, методы кодирования
- профили, выбор методов кодирования
- кодеки, выбор методов кодирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54c5bd099e5aaf8b3a735594c8b87a335fc2594
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691206"
---
# <a name="choosing-an-encoding-method"></a><span data-ttu-id="5f2d7-109">Выбор метода кодирования</span><span class="sxs-lookup"><span data-stu-id="5f2d7-109">Choosing an Encoding Method</span></span>

<span data-ttu-id="5f2d7-110">Некоторые кодеки, например кодек Windows Media Video 9, поддерживают несколько методов кодирования.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-110">Some codecs, like the Windows Media Video 9 codec, support multiple encoding methods.</span></span> <span data-ttu-id="5f2d7-111">Метод кодирования, выбранный для потока, будет зависеть от способа доставки потока.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-111">The encoding method that you choose for a stream will depend upon how the stream is to be delivered.</span></span> <span data-ttu-id="5f2d7-112">В следующей таблице описано, когда использовать различные методы кодирования.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-112">The following table describes when to use the various encoding methods.</span></span>



| <span data-ttu-id="5f2d7-113">Метод Encoding</span><span class="sxs-lookup"><span data-stu-id="5f2d7-113">Encoding method</span></span>                | <span data-ttu-id="5f2d7-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5f2d7-114">Description</span></span>                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f2d7-115">1 — постоянная скорость передачи (CBR)</span><span class="sxs-lookup"><span data-stu-id="5f2d7-115">1-pass Constant Bit Rate (CBR)</span></span> | <span data-ttu-id="5f2d7-116">Единственный параметр для потоковой передачи в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-116">The only option for live streaming.</span></span> <span data-ttu-id="5f2d7-117">Кодируется в прогнозируемую скорость и обеспечивает самое низкое качество всех методов кодирования.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-117">Encodes to a predictable bit rate and delivers the lowest quality of all encoding methods.</span></span>                                                                    |
| <span data-ttu-id="5f2d7-118">2. Передача CBR</span><span class="sxs-lookup"><span data-stu-id="5f2d7-118">2-pass CBR</span></span>                     | <span data-ttu-id="5f2d7-119">Используйте для файлов, которые будут передаваться по сети клиентскому модулю чтения, но не будут рассылаться из источника в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-119">Use for files that will be streamed over a network to a client reader, but that are not broadcast from a live source.</span></span> <span data-ttu-id="5f2d7-120">Кодируется в прогнозируемую скорость, но имеет более высокое качество, чем 1-проход CBR.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-120">Encodes to a predictable bit rate, but with better quality than 1-pass CBR.</span></span> |
| <span data-ttu-id="5f2d7-121">1 — скорость передачи переменной (VBR)</span><span class="sxs-lookup"><span data-stu-id="5f2d7-121">1-pass Variable Bit Rate (VBR)</span></span> | <span data-ttu-id="5f2d7-122">Используется, если необходимо указать качество закодированных выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-122">Use when you need to specify the quality of the encoded output.</span></span> <span data-ttu-id="5f2d7-123">Обеспечивает наиболее стабильное качество всех методов кодирования.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-123">Delivers the most consistent quality of all encoding methods.</span></span> <span data-ttu-id="5f2d7-124">Используйте только для локальных файлов или для загрузки.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-124">Use only for local files or for downloading.</span></span>                        |
| <span data-ttu-id="5f2d7-125">2-проходные с неограниченными</span><span class="sxs-lookup"><span data-stu-id="5f2d7-125">2-pass VBR – unconstrained</span></span>     | <span data-ttu-id="5f2d7-126">Используйте, если необходимо указать пропускную способность, но колебания, окружающие указанную пропускную способность, приемлемы.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-126">Use when you need to specify a bandwidth, but fluctuations around the specified bandwidth are acceptable.</span></span> <span data-ttu-id="5f2d7-127">Для локальных файлов или только для загрузки.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-127">For local files or downloading only.</span></span>                                                    |
| <span data-ttu-id="5f2d7-128">2 — пропускная мощность — ограниченная</span><span class="sxs-lookup"><span data-stu-id="5f2d7-128">2-pass VBR – constrained</span></span>       | <span data-ttu-id="5f2d7-129">Используйте в тех же условиях, что и без ограничений, но если необходимо указать максимальную скорость в течение некоторого времени.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-129">Use under the same circumstances as unconstrained, but when you need to specify a maximum momentary bit rate.</span></span> <span data-ttu-id="5f2d7-130">Для локальных файлов или только для загрузки.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-130">For local files or downloading only.</span></span>                                                |



 

<span data-ttu-id="5f2d7-131">В следующей таблице перечислены методы кодирования, поддерживаемые кодеками, поставляемыми с пакетом SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="5f2d7-131">The following table lists the encoding methods that are supported by the codecs that ship with the Windows Media Format SDK.</span></span>



| <span data-ttu-id="5f2d7-132">Кодек</span><span class="sxs-lookup"><span data-stu-id="5f2d7-132">Codec</span></span>                                  | <span data-ttu-id="5f2d7-133">CBR</span><span class="sxs-lookup"><span data-stu-id="5f2d7-133">CBR</span></span> | <span data-ttu-id="5f2d7-134">2. Передача CBR</span><span class="sxs-lookup"><span data-stu-id="5f2d7-134">2-pass CBR</span></span> | <span data-ttu-id="5f2d7-135">VBR</span><span class="sxs-lookup"><span data-stu-id="5f2d7-135">VBR</span></span> | <span data-ttu-id="5f2d7-136">2 — прохождение VBR</span><span class="sxs-lookup"><span data-stu-id="5f2d7-136">2-pass VBR</span></span> |
|----------------------------------------|-----|------------|-----|------------|
| <span data-ttu-id="5f2d7-137">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="5f2d7-137">Windows Media Video 9</span></span>                  | <span data-ttu-id="5f2d7-138">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-138">X</span></span>   | <span data-ttu-id="5f2d7-139">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-139">X</span></span>          | <span data-ttu-id="5f2d7-140">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-140">X</span></span>   | <span data-ttu-id="5f2d7-141">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-141">X</span></span>          |
| <span data-ttu-id="5f2d7-142">Windows Media Audio 9 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="5f2d7-142">Windows Media Audio 9 and later</span></span>        | <span data-ttu-id="5f2d7-143">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-143">X</span></span>   | <span data-ttu-id="5f2d7-144">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-144">X</span></span>          | <span data-ttu-id="5f2d7-145">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-145">X</span></span>   | <span data-ttu-id="5f2d7-146">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-146">X</span></span>          |
| <span data-ttu-id="5f2d7-147">Экран Windows Media видео 9</span><span class="sxs-lookup"><span data-stu-id="5f2d7-147">Windows Media Video 9 Screen</span></span>           | <span data-ttu-id="5f2d7-148">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-148">X</span></span>   |            | <span data-ttu-id="5f2d7-149">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-149">X</span></span>   |            |
| <span data-ttu-id="5f2d7-150">Голосовая связь Windows Media Audio 9</span><span class="sxs-lookup"><span data-stu-id="5f2d7-150">Windows Media Audio 9 Voice</span></span>            | <span data-ttu-id="5f2d7-151">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-151">X</span></span>   |            |     |            |
| <span data-ttu-id="5f2d7-152">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="5f2d7-152">Windows Media Audio Professional</span></span>       | <span data-ttu-id="5f2d7-153">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-153">X</span></span>   | <span data-ttu-id="5f2d7-154">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-154">X</span></span>          | <span data-ttu-id="5f2d7-155">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-155">X</span></span>   | <span data-ttu-id="5f2d7-156">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-156">X</span></span>          |
| <span data-ttu-id="5f2d7-157">Windows Media Audio без потерь</span><span class="sxs-lookup"><span data-stu-id="5f2d7-157">Windows Media Audio Lossless</span></span>           |     |            | <span data-ttu-id="5f2d7-158">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-158">X</span></span>   |            |
| <span data-ttu-id="5f2d7-159">Изображение Windows Media Video 9 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="5f2d7-159">Windows Media Video 9 Image and later</span></span>  | <span data-ttu-id="5f2d7-160">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-160">X</span></span>   |            | <span data-ttu-id="5f2d7-161">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-161">X</span></span>   |            |
| <span data-ttu-id="5f2d7-162">Расширенный профиль Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="5f2d7-162">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="5f2d7-163">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-163">X</span></span>   | <span data-ttu-id="5f2d7-164">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-164">X</span></span>          | <span data-ttu-id="5f2d7-165">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-165">X</span></span>   | <span data-ttu-id="5f2d7-166">X</span><span class="sxs-lookup"><span data-stu-id="5f2d7-166">X</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="5f2d7-167">См. также</span><span class="sxs-lookup"><span data-stu-id="5f2d7-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f2d7-168">**Проектирование профилей**</span><span class="sxs-lookup"><span data-stu-id="5f2d7-168">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> <dt>

[<span data-ttu-id="5f2d7-169">**Кодирование с постоянной скоростью (CBR)**</span><span class="sxs-lookup"><span data-stu-id="5f2d7-169">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="5f2d7-170">**2-проходная кодировка**</span><span class="sxs-lookup"><span data-stu-id="5f2d7-170">**Two-Pass Encoding**</span></span>](two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="5f2d7-171">**Кодирование переменной скорости (VBR)**</span><span class="sxs-lookup"><span data-stu-id="5f2d7-171">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




