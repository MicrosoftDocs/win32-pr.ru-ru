---
title: Реализация Имедиаобжект Аллокатестреамингресаурцес
description: Реализация Имедиаобжект Аллокатестреамингресаурцес
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Подключаемые модули проигрывателя Windows Media, эхо-образцы ресурсов потоковой передачи
- подключаемые модули, эхо-образцы ресурсов
- подключаемые модули обработки цифровых сигналов, образцы эхо-потоков
- Подключаемые модули DSP, потоковая передача образцов ресурсов
- Пример подключаемого модуля "Echo DSP", потоковая передача ресурсов
- Пример подключаемого модуля Echo DSP, буфер задержки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e347e35eaabbcbcc00a586e4cba0d8ad31cc6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411079"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a><span data-ttu-id="55673-109">Реализация Имедиаобжект:: Аллокатестреамингресаурцес</span><span class="sxs-lookup"><span data-stu-id="55673-109">Implementing IMediaObject::AllocateStreamingResources</span></span>

<span data-ttu-id="55673-110">В образце Echo метод **аллокатестреамингресаурцес** создает буфер задержки.</span><span class="sxs-lookup"><span data-stu-id="55673-110">In the Echo sample, the **AllocateStreamingResources** method creates the delay buffer.</span></span> <span data-ttu-id="55673-111">Для этого выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="55673-111">It does this by doing the following:</span></span>

1.  <span data-ttu-id="55673-112">Вычисление размера буфера, соответствующего указанному времени задержки для заданного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="55673-112">Calculating a size for the buffer that corresponds to the specified delay time for the given media type.</span></span>
2.  <span data-ttu-id="55673-113">Либо выделяйте новую память, либо Перераспределите размер буфера, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="55673-113">Either allocating new memory or reallocating the buffer size if it already exists.</span></span>
3.  <span data-ttu-id="55673-114">Вызов метода, который заполняет буфер значениями, представляющими тишину.</span><span class="sxs-lookup"><span data-stu-id="55673-114">Calling a method that fills the buffer with values representing silence.</span></span>

<span data-ttu-id="55673-115">Значение тишины различается в зависимости от глубины бита.</span><span class="sxs-lookup"><span data-stu-id="55673-115">The value for silence is different depending upon the bit depth.</span></span> <span data-ttu-id="55673-116">Для 8-разрядного звукового сигнала тишина представлено шестнадцатеричным значением 80; для 16-разрядного звукового сигнала тишина представляется нулем.</span><span class="sxs-lookup"><span data-stu-id="55673-116">For 8-bit audio, silence is represented by the hex value 80; for 16-bit audio, silence is represented by zero.</span></span>

## <a name="calculating-the-delay-buffer-size"></a><span data-ttu-id="55673-117">Вычисление размера буфера задержки</span><span class="sxs-lookup"><span data-stu-id="55673-117">Calculating the Delay Buffer Size</span></span>

<span data-ttu-id="55673-118">Чтобы вычислить требуемый размер буфера задержки, сначала необходимо получить структуру **вавеформатекс** , содержащую сведения о звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="55673-118">In order to calculate the size required for the delay buffer, you must first retrieve a **WAVEFORMATEX** structure that contains information about the audio data.</span></span> <span data-ttu-id="55673-119">В следующем примере извлекается указатель на эту структуру из входной структуры **\_ \_ типа мультимедиа DMO** :</span><span class="sxs-lookup"><span data-stu-id="55673-119">The following example retrieves a pointer to this structure from the input **DMO\_MEDIA\_TYPE** structure:</span></span>


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



<span data-ttu-id="55673-120">После сохранения указателя на соответствующую структуру **вавеформатекс** можно проверить ее элементы и использовать их для вычисления требуемого размера буфера.</span><span class="sxs-lookup"><span data-stu-id="55673-120">Once you have stored a pointer to the proper **WAVEFORMATEX** structure, you can inspect its members and use them to calculate the required buffer size.</span></span> <span data-ttu-id="55673-121">Это показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="55673-121">The following code example demonstrates this:</span></span>


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



<span data-ttu-id="55673-122">Этот алгоритм вычисляет размер буфера, умножая время задержки (в миллисекундах) на число выборок в миллисекунду, затем умножая результат на число каналов, а затем умножая результат на число байтов на выборку.</span><span class="sxs-lookup"><span data-stu-id="55673-122">This algorithm computes the buffer size by multiplying the delay time, in milliseconds, by the number of samples per millisecond, then multiplying the result by the number of channels, and then multiplying the result by the number of bytes per sample.</span></span> <span data-ttu-id="55673-123">Количество каналов и количество байт на выборку не очевидны. они кодируются в члене Нблоккалигн.</span><span class="sxs-lookup"><span data-stu-id="55673-123">The number of channels and the number of bytes per sample are not obvious; they are encoded in the nBlockAlign member.</span></span> <span data-ttu-id="55673-124">Деление на 1000 сокращает значение Нсамплесперсек до выборки в миллисекундах; миллисекунда является требуемой единицей, так как время задержки выражается в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="55673-124">Dividing by 1000 reduces the nSamplesPerSec value to samples per millisecond; the millisecond is the desired unit because the delay time is expressed in milliseconds.</span></span>

## <a name="allocating-the-delay-buffer-memory"></a><span data-ttu-id="55673-125">Выделение памяти буфера задержки</span><span class="sxs-lookup"><span data-stu-id="55673-125">Allocating the Delay Buffer Memory</span></span>

<span data-ttu-id="55673-126">После вычисления требований к памяти можно выделить буфер.</span><span class="sxs-lookup"><span data-stu-id="55673-126">Once you have calculated the memory requirements, you can allocate the buffer.</span></span> <span data-ttu-id="55673-127">Буфер может потребоваться удалить, если он существует, например, когда пользователь вызывает страницу свойств для изменения значения времени задержки.</span><span class="sxs-lookup"><span data-stu-id="55673-127">The buffer may need to be deleted if it exists, such as when the user invokes the property page to change the delay time value.</span></span> <span data-ttu-id="55673-128">Следующий код демонстрирует выделение буфера задержки:</span><span class="sxs-lookup"><span data-stu-id="55673-128">The following code demonstrates allocating the delay buffer:</span></span>


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    // A buffer already exists.
    // Delete the delay buffer.
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
}

// Allocate the buffer.
m_pbDelayBuffer = new BYTE[m_cbDelayBuffer];

if (!m_pbDelayBuffer)
    return E_OUTOFMEMORY;
```



<span data-ttu-id="55673-129">Если буфер успешно выделен, переместите перемещаемый указатель на заголовок буфера, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="55673-129">If the buffer is successfully allocated, you should move the movable pointer to the head of the buffer, as demonstrated in the following example:</span></span>


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a><span data-ttu-id="55673-130">Заполнение буфера задержки с помощью тишины</span><span class="sxs-lookup"><span data-stu-id="55673-130">Filling the Delay Buffer with Silence</span></span>

<span data-ttu-id="55673-131">Удобно написать метод для заполнения буфера задержки значениями, представляющими тишину.</span><span class="sxs-lookup"><span data-stu-id="55673-131">It is convenient to write a method to fill the delay buffer with values representing silence.</span></span> <span data-ttu-id="55673-132">Метод должен получить указатель на допустимую структуру ВАВЕФОРМАТЕКС, а затем проверить элемент Вбитсперсампле, чтобы определить, является ли звук 8-разрядным или более высоким.</span><span class="sxs-lookup"><span data-stu-id="55673-132">The method should receive the pointer to the valid WAVEFORMATEX structure and then inspect the wBitsPerSample member to determine whether the audio is 8-bit or higher.</span></span> <span data-ttu-id="55673-133">В следующем примере буфер задержки заполняется правильным значением тишины:</span><span class="sxs-lookup"><span data-stu-id="55673-133">The following example fills the delay buffer with the correct value for silence:</span></span>


```
void CEcho::FillBufferWithSilence(WAVEFORMATEX *pWfex)
{
    if (8 == pWfex->wBitsPerSample)
    {
    ::FillMemory(m_pbDelayBuffer, m_cbDelayBuffer, 0x80);
    }
    else
    ::ZeroMemory(m_pbDelayBuffer, m_cbDelayBuffer);
}
```



<span data-ttu-id="55673-134">Не забудьте добавить прямую декларацию для функции в файл заголовка Echo. h в частном разделе:</span><span class="sxs-lookup"><span data-stu-id="55673-134">Remember to add the forward declaration for the function to the header file Echo.h in the private section:</span></span>


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



<span data-ttu-id="55673-135">Необходимо добавить код в конце Аллокатестреамингресаурцес для вызова этого метода каждый раз при создании или изменении размера буфера задержки.</span><span class="sxs-lookup"><span data-stu-id="55673-135">You should add code at the end of AllocateStreamingResources to call this method each time the delay buffer is created or resized.</span></span> <span data-ttu-id="55673-136">В следующем примере кода в новый метод передается указатель ВАВЕФОРМАТЕКС с именем Пваве:</span><span class="sxs-lookup"><span data-stu-id="55673-136">The following example code passes the WAVEFORMATEX pointer named pWave to the new method:</span></span>


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a><span data-ttu-id="55673-137">Перераспределение памяти буфера задержки</span><span class="sxs-lookup"><span data-stu-id="55673-137">Reallocating the Delay Buffer Memory</span></span>

<span data-ttu-id="55673-138">Когда пользователь изменяет время задержки с помощью страницы свойств, размер буфера задержки также должен измениться.</span><span class="sxs-lookup"><span data-stu-id="55673-138">When the user changes the delay time by using the property page, the size of the delay buffer must change as well.</span></span> <span data-ttu-id="55673-139">Вы уже добавили код в Аллокатестреамингресаурцес для изменения размера буфера, но вам нужно добавить строку кода в Цечо::p UT \_ delay, чтобы вызвать метод выделения ресурсов при каждом изменении значения свойства.</span><span class="sxs-lookup"><span data-stu-id="55673-139">You've already added the code to AllocateStreamingResources to resize the buffer, but you need to add a line of code to CEcho::put\_delay to call the resource allocation method each time the property value changes.</span></span> <span data-ttu-id="55673-140">Ниже приведен код:</span><span class="sxs-lookup"><span data-stu-id="55673-140">Here is the code:</span></span>


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a><span data-ttu-id="55673-141">См. также</span><span class="sxs-lookup"><span data-stu-id="55673-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55673-142">**Работа с потоковой передачей ресурсов**</span><span class="sxs-lookup"><span data-stu-id="55673-142">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




