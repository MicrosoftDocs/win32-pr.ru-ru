---
title: Поддержка водяных знаков
description: Поддержка водяных знаков
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- Windows Media Format SDK, поддержка водяных знаков
- Windows Media Format SDK, цифровой водяной знак
- Расширенный формат систем (ASF), поддержка водяных знаков
- ASF (Расширенный системный формат), поддержка водяных знаков
- Расширенный формат систем (ASF), цифровой водяной знак
- ASF (Расширенный системный формат), цифровой водяной знак
- Пакет SDK для Windows Media Format, DMO
- Расширенный системный формат (ASF), DMO
- ASF (Расширенный системный формат), DMO
- Windows Media Format SDK, интерфейс Ивмватермаркинфо
- Расширенный системный формат (ASF), интерфейс Ивмватермаркинфо
- ASF (Расширенный системный формат), интерфейс Ивмватермаркинфо
- водяные знаки, о
- Цифровые водяные знаки
- DirectX Media Object (DMO), сведения
- DMO (мультимедийный объект DirectX), сведения
- ивмватермаркинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417012cb165c0028e71af6f8b50052fdd2fab208
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691464"
---
# <a name="watermarking-support"></a><span data-ttu-id="0444b-120">Поддержка водяных знаков</span><span class="sxs-lookup"><span data-stu-id="0444b-120">Watermarking Support</span></span>

<span data-ttu-id="0444b-121">Цифровой водяной знак — это способ внедрения авторского права или другой информации в данные потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0444b-121">Digital watermarking is a way to embed copyright or other information in the data of a media stream.</span></span> <span data-ttu-id="0444b-122">Методы создания водяных знаков в значительной степени меняются от одного решения к другому.</span><span class="sxs-lookup"><span data-stu-id="0444b-122">Techniques for watermarking vary widely from one solution to the next.</span></span> <span data-ttu-id="0444b-123">Самой простой формой водяных знаков является простое добавление идентифицирующего изображения в каждый кадр видеопотока.</span><span class="sxs-lookup"><span data-stu-id="0444b-123">The simplest form of watermarking is simply adding an identifying image to each frame of a video stream.</span></span> <span data-ttu-id="0444b-124">Телевизионные станции часто используют этот метод для вставки полупрозрачного логотипа в нижний угол вещания.</span><span class="sxs-lookup"><span data-stu-id="0444b-124">Television stations frequently use this technique to insert a semi-transparent logo in a bottom corner of their broadcast.</span></span> <span data-ttu-id="0444b-125">Более сложные формы цифровых водяных знаков незаметно для пользователя, который наблюдает за содержимым или прослушивает его.</span><span class="sxs-lookup"><span data-stu-id="0444b-125">More sophisticated forms of digital watermarking are imperceptible to the user watching or listening to the content.</span></span>

<span data-ttu-id="0444b-126">Пакет SDK Windows Media Format поддерживает использование цифровых водяных знаков [*дмос*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0444b-126">The Windows Media Format SDK supports the use of digital watermarking [*DMOs*](wmformat-glossary.md).</span></span> <span data-ttu-id="0444b-127">На практике система подложки очень похожа на кодек: она принимает примеры мультимедиа, запускает алгоритмы для данных и выводит измененные образцы.</span><span class="sxs-lookup"><span data-stu-id="0444b-127">In practice, a watermarking system is very similar to a codec: it takes media samples, runs algorithms on the data, and outputs the altered samples.</span></span> <span data-ttu-id="0444b-128">Когда для потока указана система подложки, объект модуля записи включает DMO в свою обработку входных примеров.</span><span class="sxs-lookup"><span data-stu-id="0444b-128">When a watermarking system is specified for a stream, the writer object includes the DMO in its processing of input samples.</span></span>

<span data-ttu-id="0444b-129">При настройке потока для подложки необходимо указать сведения о конфигурации водяного знака.</span><span class="sxs-lookup"><span data-stu-id="0444b-129">You must specify watermark configuration information when you configure a stream for watermarking.</span></span> <span data-ttu-id="0444b-130">Значения конфигурации будут отличаться в зависимости от подложки DMO.</span><span class="sxs-lookup"><span data-stu-id="0444b-130">The configuration values will be different depending upon the watermarking DMO.</span></span> <span data-ttu-id="0444b-131">Используемые объекты DMO должны поступать с инструкциями, описывающими поддерживаемые им значения конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0444b-131">The DMO you use should come with instructions describing the configuration values it supports.</span></span>

<span data-ttu-id="0444b-132">Сведения о параметрах, используемых для указания системы подложки, см. в разделе [ **IWMWriterAdvanced2:: сетинпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)</span><span class="sxs-lookup"><span data-stu-id="0444b-132">For information about the settings used to specify a watermarking system, see [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)</span></span>

<span data-ttu-id="0444b-133">Вы можете программировать приложение, чтобы перечислить водяные знаки дмос, установленные на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="0444b-133">You can program your application to enumerate the watermarking DMOs installed on the client computer.</span></span> <span data-ttu-id="0444b-134">Дополнительные сведения см. в описании интерфейса [**ивмватермаркинфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) .</span><span class="sxs-lookup"><span data-stu-id="0444b-134">For more information, see the [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0444b-135">См. также</span><span class="sxs-lookup"><span data-stu-id="0444b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0444b-136">**Функции записи файлов**</span><span class="sxs-lookup"><span data-stu-id="0444b-136">**File Writing Features**</span></span>](file-writing-features.md)
</dt> </dl>

 

 




