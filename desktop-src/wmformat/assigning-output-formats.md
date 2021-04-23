---
title: Назначение форматов вывода
description: Назначение форматов вывода
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows Media Format SDK, назначение форматов выходных данных
- Расширенный системный формат (ASF), назначение форматов вывода
- ASF (Расширенный системный формат), назначение форматов вывода
- Расширенный формат систем (ASF), выходные номера и форматы
- ASF (Расширенный системный формат), выходные номера и форматы
- выходные числа и форматы, назначение
- кодеки, выходные номера и форматы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633673053a2b34a2f7aed5ed3f6ae66457a7ee13
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "105654269"
---
# <a name="assigning-output-formats"></a><span data-ttu-id="2e226-110">Назначение форматов вывода</span><span class="sxs-lookup"><span data-stu-id="2e226-110">Assigning Output Formats</span></span>

<span data-ttu-id="2e226-111">Некоторые кодеки могут распаковывать цифровые мультимедийные данные в несколько несжатых форматов.</span><span class="sxs-lookup"><span data-stu-id="2e226-111">Some codecs can decompress digital media data into several uncompressed formats.</span></span> <span data-ttu-id="2e226-112">Вы можете найти все поддерживаемые форматы для определенного вывода, используя либо асинхронный читатель, либо синхронный модуль чтения.</span><span class="sxs-lookup"><span data-stu-id="2e226-112">You can find all of the supported formats for a specific output using either the asynchronous reader or the synchronous reader.</span></span>

<span data-ttu-id="2e226-113">Чтобы проверить все доступные форматы выходных данных, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2e226-113">To examine all of the available formats for an output, perform the following steps.</span></span> <span data-ttu-id="2e226-114">Эти процедуры идентичны как для асинхронного чтения, так и для синхронного модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="2e226-114">These procedures are identical for both the asynchronous reader and the synchronous reader.</span></span> <span data-ttu-id="2e226-115">Если имена интерфейсов различаются, методы синхронного чтения перечисляются в скобках после методов асинхронного модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="2e226-115">Where interface names vary, the synchronous reader methods are listed in parentheses after the methods of the asynchronous reader.</span></span>

1.  <span data-ttu-id="2e226-116">Создайте объект Reader и загрузите файл для чтения.</span><span class="sxs-lookup"><span data-stu-id="2e226-116">Create a reader object and load a file for reading.</span></span> <span data-ttu-id="2e226-117">Дополнительные сведения см. [в разделе Создание читателя и открытие файла](to-create-a-reader-and-open-a-file.md) (или [Создание синхронного средства чтения и открытие файла](to-create-a-synchronous-reader-and-open-a-file.md)).</span><span class="sxs-lookup"><span data-stu-id="2e226-117">For more information, see [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md) (or [To Create a Synchronous Reader and Open a File](to-create-a-synchronous-reader-and-open-a-file.md)).</span></span>
2.  <span data-ttu-id="2e226-118">Определите выходные данные, для которых необходимо найти доступные форматы.</span><span class="sxs-lookup"><span data-stu-id="2e226-118">Determine the output for which you want to find the available formats.</span></span> <span data-ttu-id="2e226-119">Если вы не умеете знать, какие выходные данные вы хотите использовать, можно указать выходные данные в файле, используя процедуры в [для указания выходных номеров](to-identify-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="2e226-119">If you don't already know which output you want to use, you can identify the outputs in the file using the procedures in [To Identify Output Numbers](to-identify-output-numbers.md).</span></span>
3.  <span data-ttu-id="2e226-120">Получите общее число доступных форматов для требуемых выходных данных, вызвав [**ивмреадер:: жетаутпутформаткаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (или [**Ивмсинкреадер:: жетаутпутформаткаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).</span><span class="sxs-lookup"><span data-stu-id="2e226-120">Retrieve the total number of available formats for the desired output by calling [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (or [**IWMSyncReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).</span></span>
4.  <span data-ttu-id="2e226-121">Выполните цикл по одному из доступных форматов, выполнив следующие действия для каждого из них:</span><span class="sxs-lookup"><span data-stu-id="2e226-121">Loop through the available formats one at a time, performing the following steps for each:</span></span>
    -   <span data-ttu-id="2e226-122">Получите интерфейс [**ивмаутпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) для текущего формата выходных данных, вызвав [**Ивмреадер:: Жетаутпутформат**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (или [**ивмсинкреадер:: жетаутпутформат**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).</span><span class="sxs-lookup"><span data-stu-id="2e226-122">Retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface for the current output format by calling [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (or [**IWMSyncReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).</span></span>
    -   <span data-ttu-id="2e226-123">Получите структуру [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) для выходного формата, выполнив два вызова [**ивммедиапропс:: жетмедиатипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="2e226-123">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the output format by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="2e226-124">Выполните первый вызов, чтобы получить размер структуры, затем выделите память для нее и передайте указатель на выделенную память во втором вызове.</span><span class="sxs-lookup"><span data-stu-id="2e226-124">Make the first call to get the size of the structure, then allocate memory for it and pass a pointer to the allocated memory on the second call.</span></span>
    -   <span data-ttu-id="2e226-125">Найдите подтип носителя выходного формата в формате **WM \_ Media \_ Type.** подтип.</span><span class="sxs-lookup"><span data-stu-id="2e226-125">Find the media subtype of the output format in **WM\_MEDIA\_TYPE.subtype**.</span></span>
    -   <span data-ttu-id="2e226-126">Для видео, если текущий подтип является форматом, который вы хотите использовать для вывода, прервать цикл.</span><span class="sxs-lookup"><span data-stu-id="2e226-126">For video, if the current subtype is the format you want to use for output, break out of the loop.</span></span> <span data-ttu-id="2e226-127">В противном случае перейдите к следующей итерации.</span><span class="sxs-lookup"><span data-stu-id="2e226-127">Otherwise go to the next iteration.</span></span>

        <span data-ttu-id="2e226-128">Для звука необходимо проверить значения в структуре **вавеформатекс** в соответствии с вашими требованиями.</span><span class="sxs-lookup"><span data-stu-id="2e226-128">For audio, you must check the values in the **WAVEFORMATEX** structure against your requirements.</span></span> <span data-ttu-id="2e226-129">**WM \_ MEDIA \_ Type. пбформат** указывает на структуру **вавеформатекс** для звуковых выходов.</span><span class="sxs-lookup"><span data-stu-id="2e226-129">**WM\_MEDIA\_TYPE.pbFormat** points to the **WAVEFORMATEX** structure for audio outputs.</span></span>

5.  <span data-ttu-id="2e226-130">После того как вы нашли нужные выходные данные, задайте их для использования с модулем чтения, вызвав [**ивмреадер:: сетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (или [**Ивмсинкреадер:: сетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)).</span><span class="sxs-lookup"><span data-stu-id="2e226-130">When you have found the output desired, set it for use with the reader by calling [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (or [**IWMSyncReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)).</span></span> <span data-ttu-id="2e226-131">Необходимо передать указатель на интерфейс **ивмаутпутмедиапропс** , полученный на первом шаге цикла.</span><span class="sxs-lookup"><span data-stu-id="2e226-131">You must pass a pointer to the **IWMOutputMediaProps** interface obtained in the first step of the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e226-132">См. также</span><span class="sxs-lookup"><span data-stu-id="2e226-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e226-133">**Интерфейс Ивммедиапропс**</span><span class="sxs-lookup"><span data-stu-id="2e226-133">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="2e226-134">**Интерфейс Ивмаутпутмедиапропс**</span><span class="sxs-lookup"><span data-stu-id="2e226-134">**IWMOutputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[<span data-ttu-id="2e226-135">**Интерфейс Ивмреадер**</span><span class="sxs-lookup"><span data-stu-id="2e226-135">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="2e226-136">**Интерфейс Ивмсинкреадер**</span><span class="sxs-lookup"><span data-stu-id="2e226-136">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="2e226-137">**Работа с выходами**</span><span class="sxs-lookup"><span data-stu-id="2e226-137">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




