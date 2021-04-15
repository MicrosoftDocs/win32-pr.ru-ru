---
title: Кодирование переменной скорости (VBR)
description: Кодирование переменной скорости (VBR)
ms.assetid: d3fe0cc6-64d7-44ce-8bb4-dd2eed021345
keywords:
- Windows Media Format SDK, кодирование VBR
- Windows Media Format SDK, переменная скорость (VBR)
- Windows Media Format SDK, кодирование с учетом качества VBR
- Пакет SDK для Windows Media Format, неограниченное кодирование VBR
- Windows Media Format SDK, кодирование с ограниченным объемом VBR
- кодеки, кодирование VBR
- кодеки, переменные скорость (VBR)
- кодеки, кодировка VBR на основе качества
- кодеки, неограниченное кодирование VBR
- кодеки с ограниченным кодированием VBR
- Переменная скорость (VBR), сведения
- VBR (переменная скорость), сведения
- Кодировка VBR на основе качества, сведения
- неограниченное кодирование VBR, сведения
- кодирование с ограничением VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b24a32b693cc4801f95695cc2d6e5f9ffa400c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710159"
---
# <a name="variable-bit-rate-vbr-encoding"></a><span data-ttu-id="2df0f-118">Кодирование переменной скорости (VBR)</span><span class="sxs-lookup"><span data-stu-id="2df0f-118">Variable Bit Rate (VBR) Encoding</span></span>

<span data-ttu-id="2df0f-119">Кодирование с переменной скоростью (VBR) — это альтернатива постоянной кодировке битовой скорости (CBR) и поддерживается некоторыми кодеками.</span><span class="sxs-lookup"><span data-stu-id="2df0f-119">Variable bit rate (VBR) encoding is an alternative to constant bit rate encoding (CBR) and is supported by some codecs.</span></span> <span data-ttu-id="2df0f-120">Когда CBR кодирование стремится поддерживать скорость потока закодированного носителя, VBR стремится достичь наилучшего возможного качества закодированного носителя.</span><span class="sxs-lookup"><span data-stu-id="2df0f-120">Where CBR encoding strives to maintain the bit rate of the encoded media, VBR strives to achieve the best possible quality of the encoded media.</span></span>

<span data-ttu-id="2df0f-121">Качество закодированного содержимого определяется количеством потерянных данных при сжатии и распаковке содержимого.</span><span class="sxs-lookup"><span data-stu-id="2df0f-121">The quality of encoded content is determined by the amount of data that is lost when the content is compressed and decompressed.</span></span> <span data-ttu-id="2df0f-122">На потерю данных в процессе сжатия влияют многие факторы, но в целом, чем сложнее исходные данные и чем выше степень сжатия, тем больше сведений теряется в процессе сжатия.</span><span class="sxs-lookup"><span data-stu-id="2df0f-122">Many factors affect the loss of data in the compression process, but in general, the more complex the original data and the higher the compression ratio, the more detail is lost in the compression process.</span></span>

<span data-ttu-id="2df0f-123">Существует три типа кодирования VBR: с учетом качества, неограниченным и ограниченным.</span><span class="sxs-lookup"><span data-stu-id="2df0f-123">There are three types of VBR encoding: quality-based, unconstrained, and constrained.</span></span>

## <a name="quality-based-vbr-encoding"></a><span data-ttu-id="2df0f-124">Кодировка VBR на основе качества</span><span class="sxs-lookup"><span data-stu-id="2df0f-124">Quality-based VBR Encoding</span></span>

<span data-ttu-id="2df0f-125">Первый тип кодирования VBR зависит от качества, в котором используется один проход кодирования.</span><span class="sxs-lookup"><span data-stu-id="2df0f-125">The first type of VBR encoding is quality-based, which uses one encoding pass.</span></span> <span data-ttu-id="2df0f-126">Кодировка VBR на основе качества позволяет указать уровень качества для потока цифрового мультимедиа, а не скорость.</span><span class="sxs-lookup"><span data-stu-id="2df0f-126">Quality-based VBR encoding enables you to specify a level of quality for a digital media stream instead of a bit rate.</span></span> <span data-ttu-id="2df0f-127">Затем кодек будет кодировать содержимое, чтобы все выборки были сравнимы по качеству.</span><span class="sxs-lookup"><span data-stu-id="2df0f-127">The codec will then encode the content so that all samples are of comparable quality.</span></span>

<span data-ttu-id="2df0f-128">Основным преимуществом кодирования VBR на основе качества является то, что качество одинаково в файле и от одного файла к другому.</span><span class="sxs-lookup"><span data-stu-id="2df0f-128">The main advantage of quality-based VBR encoding is that quality is consistent within a file and from one file to the next.</span></span> <span data-ttu-id="2df0f-129">Например, можно написать программу для копирования песен из компакт-диска в файлы ASF на компьютере.</span><span class="sxs-lookup"><span data-stu-id="2df0f-129">For example, you can write a program to copy songs from CD to ASF files on a computer.</span></span> <span data-ttu-id="2df0f-130">В этом случае совместимость с конечным пользователем, скорее всего, важнее, чем размер файла.</span><span class="sxs-lookup"><span data-stu-id="2df0f-130">In this case, consistent quality is probably more important to the end-user experience than consistent file size.</span></span> <span data-ttu-id="2df0f-131">Использование кодирования VBR на основе качества гарантирует, что все песни будут иметь одинаковое качество.</span><span class="sxs-lookup"><span data-stu-id="2df0f-131">Using quality-based VBR encoding would ensure that all of the songs copied are of the same quality.</span></span>

<span data-ttu-id="2df0f-132">Недостатком кодирования VBR на основе качества является то, что на самом деле нет способа выяснить размер или требования к пропускной способности закодированного носителя перед кодированием.</span><span class="sxs-lookup"><span data-stu-id="2df0f-132">The disadvantage of quality-based VBR encoding is that there is really no way to know the size or bandwidth requirements of the encoded media before encoding.</span></span> <span data-ttu-id="2df0f-133">Это может сделать файлы в кодировке с поддержкой VBR в случаях, когда ограничена память или пропускная способность, например портативные проигрыватели мультимедиа или Интернет-подключения с низкой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="2df0f-133">This can make quality-based VBR-encoded files inappropriate for circumstances where memory or bandwidth are restricted, such as portable media players, or low-bandwidth Internet connections.</span></span>

<span data-ttu-id="2df0f-134">Как правило, кодирование VBR на основе качества хорошо подходит для локального воспроизведения или подключений с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="2df0f-134">In general, quality-based VBR encoding is well suited for local playback or high bandwidth network connections.</span></span> <span data-ttu-id="2df0f-135">В таких случаях последовательное качество обеспечит лучшую работу пользователей.</span><span class="sxs-lookup"><span data-stu-id="2df0f-135">In those cases, the consistent quality will provide a better user experience.</span></span>

## <a name="unconstrained-vbr-encoding"></a><span data-ttu-id="2df0f-136">Неограниченное кодирование VBR</span><span class="sxs-lookup"><span data-stu-id="2df0f-136">Unconstrained VBR Encoding</span></span>

<span data-ttu-id="2df0f-137">Для кодирования с неограниченной VBR используется два прохода кодирования.</span><span class="sxs-lookup"><span data-stu-id="2df0f-137">Unconstrained VBR encoding uses two encoding passes.</span></span> <span data-ttu-id="2df0f-138">При использовании кодирования с неограниченным числом VBR необходимо указать скорость потока, как в случае с кодировкой CBR.</span><span class="sxs-lookup"><span data-stu-id="2df0f-138">When using unconstrained VBR encoding, you specify a bit rate for the stream, as you would with CBR encoding.</span></span> <span data-ttu-id="2df0f-139">Однако кодек использует это значение только в качестве средней скорости потока и кодируется таким образом, чтобы качество максимально велико при сохранении среднего значения.</span><span class="sxs-lookup"><span data-stu-id="2df0f-139">However, the codec uses this value only as the average bit rate for the stream and encodes so that the quality is as high as possible while maintaining the average.</span></span> <span data-ttu-id="2df0f-140">Реальная скорость потока в любой момент в закодированном потоке может сильно отличаться от среднего значения.</span><span class="sxs-lookup"><span data-stu-id="2df0f-140">The actual bit rate at any point in the encoded stream can vary greatly from the average value.</span></span>

<span data-ttu-id="2df0f-141">Не задается окно буфера для кодирования с неограниченным значением VBR, как и для потока с CBR кодировкой.</span><span class="sxs-lookup"><span data-stu-id="2df0f-141">You do not set a buffer window for unconstrained VBR encoding as you would for a CBR-encoded stream.</span></span> <span data-ttu-id="2df0f-142">Вместо этого кодек определяет размер требуемого окна буфера на основе требований закодированных образцов.</span><span class="sxs-lookup"><span data-stu-id="2df0f-142">Instead, the codec computes the size of the required buffer window based on the requirements of the encoded samples.</span></span>

<span data-ttu-id="2df0f-143">Преимуществом кодирования с неограниченным числом VBR является то, что сжатый поток имеет наивысшее возможное качество, сохраняя при этом прогнозируемую среднюю пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="2df0f-143">The advantage of unconstrained VBR encoding is that the compressed stream has the highest possible quality while staying within a predictable average bandwidth.</span></span>

## <a name="constrained-vbr-encoding"></a><span data-ttu-id="2df0f-144">Кодирование с ограничением VBR</span><span class="sxs-lookup"><span data-stu-id="2df0f-144">Constrained VBR Encoding</span></span>

<span data-ttu-id="2df0f-145">Кодирование с ограниченным количеством VBR идентично кодированию с неограниченным кодированием VBR, за исключением того, что вы указываете максимальную скорость потока и Максимальное окно буфера в профиле.</span><span class="sxs-lookup"><span data-stu-id="2df0f-145">Constrained VBR encoding is identical to unconstrained VBR encoding, except that you specify a maximum bit rate and a maximum buffer window in the profile.</span></span> <span data-ttu-id="2df0f-146">Затем кодек использует максимальные значения, чтобы определить, как сжимать данные.</span><span class="sxs-lookup"><span data-stu-id="2df0f-146">The codec then uses the maximum values to determine how to compress the data.</span></span> <span data-ttu-id="2df0f-147">Если задать максимальное значение, достаточно высокое значение, кодирование с ограниченным количеством VBR приведет к тому же закодированному потоку, что и неограниченное кодирование VBR.</span><span class="sxs-lookup"><span data-stu-id="2df0f-147">If you set the maximum values high enough, constrained VBR encoding will produce the same encoded stream as unconstrained VBR encoding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2df0f-148">См. также</span><span class="sxs-lookup"><span data-stu-id="2df0f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2df0f-149">**Выбор метода кодирования**</span><span class="sxs-lookup"><span data-stu-id="2df0f-149">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="2df0f-150">**Функции кодеков**</span><span class="sxs-lookup"><span data-stu-id="2df0f-150">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="2df0f-151">**Настройка потоков**</span><span class="sxs-lookup"><span data-stu-id="2df0f-151">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="2df0f-152">**Настройка потоков с VBR**</span><span class="sxs-lookup"><span data-stu-id="2df0f-152">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> <dt>

[<span data-ttu-id="2df0f-153">**Кодирование с постоянной скоростью (CBR)**</span><span class="sxs-lookup"><span data-stu-id="2df0f-153">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="2df0f-154">**2-проходная кодировка**</span><span class="sxs-lookup"><span data-stu-id="2df0f-154">**Two-Pass Encoding**</span></span>](two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="2df0f-155">**Использование кодировки Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="2df0f-155">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> </dl>

 

 




