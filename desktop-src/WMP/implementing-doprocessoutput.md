---
title: Реализация Допроцессаутпут
description: Реализация Допроцессаутпут
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- Подключаемые модули проигрывателя Windows Media, DSP аудиоподсистемы
- подключаемые модули, DSP аудиоподсистемы
- подключаемые модули обработки цифровых сигналов, Допроцессаутпут
- Подключаемые модули DSP, Допроцессаутпут
- подключаемые модули DSP аудиоподсистемы, Допроцессаутпут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68562444a3a8f0bfacad26fc5246181d33cefa2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411059"
---
# <a name="implementing-doprocessoutput"></a><span data-ttu-id="ea978-108">Реализация Допроцессаутпут</span><span class="sxs-lookup"><span data-stu-id="ea978-108">Implementing DoProcessOutput</span></span>

<span data-ttu-id="ea978-109">Для обработки звуковых данных необходимо выполнить несколько шагов в **допроцессаутпут**.</span><span class="sxs-lookup"><span data-stu-id="ea978-109">To process audio data, you'll need to perform several steps in **DoProcessOutput**.</span></span> <span data-ttu-id="ea978-110">Следующие шаги используют образец кода мастера подключаемых модулей в качестве примеров.</span><span class="sxs-lookup"><span data-stu-id="ea978-110">The following steps use the plug-in wizard sample code as examples.</span></span> <span data-ttu-id="ea978-111">Если вы хотите создать подключаемый модуль DSP для аудио, который обрабатывает мультимедийное содержимое того же типа, что и образец кода мастера подключаемого модуля, вам потребуется только изменить фактический код обработки, на который ссылается в шаге 6.</span><span class="sxs-lookup"><span data-stu-id="ea978-111">If you want to create an audio DSP plug-in that processes media content of the same type that the plug-in wizard sample code does, you'll only need to change the actual processing code referred to in step 6.</span></span> <span data-ttu-id="ea978-112">Ниже приведены все действия, реализованные в **допроцессаутпут**.</span><span class="sxs-lookup"><span data-stu-id="ea978-112">Following are all the steps implemented in **DoProcessOutput**:</span></span>

-   <span data-ttu-id="ea978-113">Если подключаемый модуль в данный момент не включен, просто скопируйте данные без изменений в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="ea978-113">If the plug-in is not currently enabled, simply copy the data unchanged into the output buffer.</span></span> <span data-ttu-id="ea978-114">Если подключаемый модуль преобразует данные в другой формат, необходимо также выполнить обработку преобразования здесь.</span><span class="sxs-lookup"><span data-stu-id="ea978-114">If your plug-in converts the data into a different format, you must also do the conversion processing here.</span></span>

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   <span data-ttu-id="ea978-115">Получение указателя на структуру формата входных данных.</span><span class="sxs-lookup"><span data-stu-id="ea978-115">Retrieve a pointer to the input format structure.</span></span> <span data-ttu-id="ea978-116">Необходимо получить данные элементов из этой структуры, поэтому скопируйте указатель из *m \_ мтинпут*.**пбформат** в локальную переменную указателя типа, которая соответствует типу структуры формата.</span><span class="sxs-lookup"><span data-stu-id="ea978-116">You'll need to retrieve member data from this structure, so copy the pointer from *m\_mtInput*.**pbformat** to a local pointer variable of a type that matches the format structure type.</span></span> <span data-ttu-id="ea978-117">В следующем примере сохраняется указатель на структуру формата входных данных **вавеформатекс** :</span><span class="sxs-lookup"><span data-stu-id="ea978-117">The following example stores a pointer to a **WAVEFORMATEX** input format structure:</span></span>

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   <span data-ttu-id="ea978-118">Вычислите количество обрабатываемых выборок.</span><span class="sxs-lookup"><span data-stu-id="ea978-118">Calculate the number of samples to process.</span></span> <span data-ttu-id="ea978-119">Пример кода, создаваемый мастером подключаемых модулей, выполняет этот шаг, разделив число байтов для обработки элементом **нблоккалигн** структуры входного формата вавеформатекс, а затем умножив результат на количество каналов, которые хранились в элементе **нчаннелс** .</span><span class="sxs-lookup"><span data-stu-id="ea978-119">The sample code that the plug-in wizard generates performs this step by dividing the number of bytes to process by the **nBlockAlign** member of the WAVEFORMATEX input format structure, and then multiplying the result by the number of channels, which was stored in the **nChannels** member.</span></span> <span data-ttu-id="ea978-120">Ниже приведен пример кода из мастера подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="ea978-120">The following example is from the plug-in wizard sample code:</span></span>

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  <span data-ttu-id="ea978-121">Определите битовую глубину звука.</span><span class="sxs-lookup"><span data-stu-id="ea978-121">Determine the bit depth of the audio.</span></span> <span data-ttu-id="ea978-122">Образец кода мастера подключаемого модуля определяет 8-битный или 16-битный звук путем проверки элемента **вбитсперсампле** структуры **вавеформатекс** .</span><span class="sxs-lookup"><span data-stu-id="ea978-122">The plug-in wizard sample code determines 8-bit or 16-bit audio by inspecting the **wBitsPerSample** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="ea978-123">Затем оно использует это значение в операторе switch, чтобы предоставить отдельные подпрограммы обработки для каждой битовой глубины.</span><span class="sxs-lookup"><span data-stu-id="ea978-123">It then uses that value in a switch statement to provide separate processing routines for each bit depth.</span></span> <span data-ttu-id="ea978-124">При работе с другими типами форматов и глубиной бит может потребоваться использовать другой метод.</span><span class="sxs-lookup"><span data-stu-id="ea978-124">You may need to use a different technique when dealing with other format types and bit depths.</span></span>
    2.  <span data-ttu-id="ea978-125">Создайте цикл для пошагового просмотра звуковых образцов во входном буфере.</span><span class="sxs-lookup"><span data-stu-id="ea978-125">Create a loop to step through the audio samples in the input buffer.</span></span>
    3.  <span data-ttu-id="ea978-126">Получение примера из входного буфера.</span><span class="sxs-lookup"><span data-stu-id="ea978-126">Retrieve a sample from the input buffer.</span></span> <span data-ttu-id="ea978-127">Это делается путем разыменования указателя входных данных и сохранения результата в переменную типа int. Для 16-разрядного звука необходимо повторно привести указатель БАЙТа к короткому указателю для обработки большей точности звукового образца.</span><span class="sxs-lookup"><span data-stu-id="ea978-127">You do this by dereferencing the input data pointer and storing the result in a variable of type int. For 16-bit audio, you must recast the BYTE pointer to a short pointer to handle the greater audio sample precision.</span></span> <span data-ttu-id="ea978-128">После получения значения можно сразу увеличить указатель *пбинпутдата* , чтобы он указывал на следующий образец.</span><span class="sxs-lookup"><span data-stu-id="ea978-128">Once you have the value, you can immediately increment the *pbInputData* pointer so that it points to the next sample.</span></span> <span data-ttu-id="ea978-129">Это продемонстрировано в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="ea978-129">The following examples demonstrate this:</span></span>

    ```C++
    // For 8-bit audio.
    int i = *pbInputData++;  
    
    ```

    

    <span data-ttu-id="ea978-130">-или-</span><span class="sxs-lookup"><span data-stu-id="ea978-130">-or-</span></span>

    ```C++
    // For 16-bit audio.
    // Recast the pointer.
    short *pwInputData = (short *) pbInputData; 

    // Enter the loop and then get the input sample.
    int i = *pwInputData++;
    
    ```

    

    1.  <span data-ttu-id="ea978-131">Выполните обработку.</span><span class="sxs-lookup"><span data-stu-id="ea978-131">Perform the processing.</span></span> <span data-ttu-id="ea978-132">Здесь вы применяете алгоритмы, которые изменяют пример каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="ea978-132">This is where you apply the algorithms that change the sample somehow.</span></span> <span data-ttu-id="ea978-133">Вот что вы сделаете здесь.</span><span class="sxs-lookup"><span data-stu-id="ea978-133">What you do here is up to you.</span></span>
    2.  <span data-ttu-id="ea978-134">Запишите обработанные данные в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="ea978-134">Write the processed data to the output buffer.</span></span> <span data-ttu-id="ea978-135">Немедленно Увеличьте указатель до выходного буфера, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="ea978-135">Immediately increment the pointer to the output buffer, as in the following example:</span></span>

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  <span data-ttu-id="ea978-136">Повторите цикл, пока не будут обработаны все образцы.</span><span class="sxs-lookup"><span data-stu-id="ea978-136">Repeat the loop until all the samples have been processed.</span></span>
    2.  <span data-ttu-id="ea978-137">Возврат соответствующего **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ea978-137">Return an appropriate **HRESULT**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea978-138">См. также</span><span class="sxs-lookup"><span data-stu-id="ea978-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea978-139">**Реализация подключаемого модуля DSP аудиоподсистемы**</span><span class="sxs-lookup"><span data-stu-id="ea978-139">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




