---
title: Создание эффекта эха
description: Создание эффекта эха
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Подключаемые модули проигрывателя Windows Media, метод Echo Sample Допроцессаутпут
- подключаемые модули, метод Echo Sample Допроцессаутпут
- подключаемые модули обработки цифровых сигналов, метод Echo Sample Допроцессаутпут
- Подключаемые модули DSP, метод Echo Sample Допроцессаутпут
- Пример подключаемого модуля Echo DSP, метод Допроцессаутпут
- Пример подключаемого модуля Echo DSP, создание эффекта эха
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e978562ff4cdee016f92409d183990cd4bb178b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067412"
---
# <a name="creating-the-echo-effect"></a><span data-ttu-id="23bf2-109">Создание эффекта эха</span><span class="sxs-lookup"><span data-stu-id="23bf2-109">Creating the Echo Effect</span></span>

<span data-ttu-id="23bf2-110">Сначала необходимо удалить код из образца мастера, который масштабирует звук.</span><span class="sxs-lookup"><span data-stu-id="23bf2-110">You must first remove the code from the wizard sample that scales the audio.</span></span> <span data-ttu-id="23bf2-111">Из 8-разрядного раздела удалите следующий код:</span><span class="sxs-lookup"><span data-stu-id="23bf2-111">From the 8-bit section, remove the following code:</span></span>


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



<span data-ttu-id="23bf2-112">(Помните, что m \_ фскалефактор был заменен на m \_ двделайтиме.)</span><span class="sxs-lookup"><span data-stu-id="23bf2-112">(Remember that m\_fScaleFactor was replaced by m\_dwDelayTime.)</span></span>

<span data-ttu-id="23bf2-113">Из 16-разрядного раздела удалите следующий код:</span><span class="sxs-lookup"><span data-stu-id="23bf2-113">From the 16-bit section, remove the following code:</span></span>


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



<span data-ttu-id="23bf2-114">Реализация **допроцессаутпут** , предоставляемая в примере кода мастера подключаемых модулей, создает цикл while, который выполняет итерацию один раз для каждого образца во входном буфере, предоставленном проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="23bf2-114">The implementation of **DoProcessOutput** provided by the plug-in wizard sample code creates a while loop that iterates one time for each sample in the input buffer provided by Windows Media Player.</span></span> <span data-ttu-id="23bf2-115">Этот цикл работает одинаково как для 8-разрядных, так и для 16-разрядных аудио, хотя для каждого из них требуется отдельный цикл.</span><span class="sxs-lookup"><span data-stu-id="23bf2-115">This loop works the same way for both 8-bit and 16-bit audio, although a separate loop is required for each.</span></span> <span data-ttu-id="23bf2-116">В каждом случае цикл инициируется следующим тестом:</span><span class="sxs-lookup"><span data-stu-id="23bf2-116">In each case, the loop initiates with the following test:</span></span>


```C++
while (dwSamplesToProcess--)

```



<span data-ttu-id="23bf2-117">Внутри цикла подпрограммы обработки очень похожи на 8-разрядные и 16-разрядные аудио.</span><span class="sxs-lookup"><span data-stu-id="23bf2-117">Once inside the loop, the processing routines are very similar for 8-bit and 16-bit audio.</span></span> <span data-ttu-id="23bf2-118">Основное отличие состоит в том, что код в 8-битном разделе изменяет диапазон значений данных на-128 до 127, а затем преобразует диапазон обратно перед записью данных в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="23bf2-118">The main difference is that the code in the 8-bit section changes the range of data values to -128 through 127, and then converts the range back again before writing the data to the output buffer.</span></span> <span data-ttu-id="23bf2-119">Это важно для удержания симметрии звуковой волны во время обработки.</span><span class="sxs-lookup"><span data-stu-id="23bf2-119">This is important to retain the symmetry of the audio waveform during processing.</span></span>

<span data-ttu-id="23bf2-120">Теперь можно приступить к добавлению и замене кода в цикле обработки.</span><span class="sxs-lookup"><span data-stu-id="23bf2-120">Now you can begin to add and replace code in the processing loop.</span></span>

## <a name="retrieve-a-sample-from-the-input-buffer"></a><span data-ttu-id="23bf2-121">Получение примера из входного буфера</span><span class="sxs-lookup"><span data-stu-id="23bf2-121">Retrieve a Sample from the Input Buffer</span></span>

<span data-ttu-id="23bf2-122">Во время каждой итерации цикла из входного буфера извлекается один пример.</span><span class="sxs-lookup"><span data-stu-id="23bf2-122">During each iteration of the loop, a single sample is retrieved from the input buffer.</span></span> <span data-ttu-id="23bf2-123">Для 8-разрядного звука образец перемещается в новый диапазон, а затем указатель на входной буфер переходит к следующему примеру.</span><span class="sxs-lookup"><span data-stu-id="23bf2-123">For 8-bit audio, the sample is shifted into the new range, and then the pointer to the input buffer is advanced to the next sample.</span></span> <span data-ttu-id="23bf2-124">Следующий код находится в мастере подключаемых модулей:</span><span class="sxs-lookup"><span data-stu-id="23bf2-124">The following code is from the plug-in wizard:</span></span>


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



<span data-ttu-id="23bf2-125">Для 16-разрядного звука процесс аналогичен, за исключением нормализации:</span><span class="sxs-lookup"><span data-stu-id="23bf2-125">For 16-bit audio, the process is the same except for the normalization:</span></span>


```C++
// Get the input sample.
int i = *pwInputData++;

```



<span data-ttu-id="23bf2-126">Помните, что указатели в 16-разрядном коде преобразованы в тип **Short**.</span><span class="sxs-lookup"><span data-stu-id="23bf2-126">Remember that the pointers in the 16-bit code have been converted to type **short**.</span></span>

## <a name="retrieve-a-sample-from-the-delay-buffer"></a><span data-ttu-id="23bf2-127">Получение примера из буфера задержки</span><span class="sxs-lookup"><span data-stu-id="23bf2-127">Retrieve a Sample from the Delay Buffer</span></span>

<span data-ttu-id="23bf2-128">Затем извлеките один пример из буфера задержки.</span><span class="sxs-lookup"><span data-stu-id="23bf2-128">Next, retrieve a single sample from the delay buffer.</span></span> <span data-ttu-id="23bf2-129">Для 8-разрядного кода примеры задержки хранятся в собственном диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="23bf2-129">For 8-bit code, the delay samples are stored in their native range of 0 to 255.</span></span> <span data-ttu-id="23bf2-130">Следующий код, который необходимо добавить, извлекает пример 8-разрядной задержки:</span><span class="sxs-lookup"><span data-stu-id="23bf2-130">The following code, which you must add, retrieves an 8-bit delay sample:</span></span>


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



<span data-ttu-id="23bf2-131">Для 16-разрядного звука процесс выглядит примерно так:</span><span class="sxs-lookup"><span data-stu-id="23bf2-131">For 16-bit audio, the process is similar:</span></span>


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a><span data-ttu-id="23bf2-132">Запись образца входных данных в буфер задержки</span><span class="sxs-lookup"><span data-stu-id="23bf2-132">Write the Input Sample to the Delay Buffer</span></span>

<span data-ttu-id="23bf2-133">Теперь необходимо сохранить образец входных данных в буфере задержки в том же расположении, из которого был получен образец Delay.</span><span class="sxs-lookup"><span data-stu-id="23bf2-133">Now, you must store the input sample in the delay buffer in the same location from which you retrieved the delay sample.</span></span> <span data-ttu-id="23bf2-134">Ниже приведен код, который необходимо добавить для 8-разрядного звука:</span><span class="sxs-lookup"><span data-stu-id="23bf2-134">The following is the code you must add for 8-bit audio:</span></span>


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



<span data-ttu-id="23bf2-135">Это код для добавления в 16-разрядный раздел:</span><span class="sxs-lookup"><span data-stu-id="23bf2-135">This is the code to add for the 16-bit section:</span></span>


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a><span data-ttu-id="23bf2-136">Перемещение указателя отложенного буфера</span><span class="sxs-lookup"><span data-stu-id="23bf2-136">Move the Delay Buffer Pointer</span></span>

<span data-ttu-id="23bf2-137">Теперь, когда работа в буфере задержки завершена для этой итерации, можно переместить перемещаемый указатель на буфер задержки.</span><span class="sxs-lookup"><span data-stu-id="23bf2-137">Now that the work in the delay buffer is finished for this iteration, you can advance the movable pointer to the delay buffer.</span></span> <span data-ttu-id="23bf2-138">Если указатель достигает конца круглого буфера, необходимо изменить его значение, чтобы оно указывало на заголовок буфера.</span><span class="sxs-lookup"><span data-stu-id="23bf2-138">If the pointer reaches the end of the circular buffer, you must change its value to point to the head of the buffer.</span></span> <span data-ttu-id="23bf2-139">Чтобы сделать это для 8-разрядного звука, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="23bf2-139">To do this for 8-bit audio, use the following code:</span></span>


```C++
// Increment the delay pointer.
// If it has passed the end of the buffer,
// then move it to the head of the buffer.
if (++m_pbDelayPointer > pbEOFDelayBuffer)
    m_pbDelayPointer = m_pbDelayBuffer;

```



<span data-ttu-id="23bf2-140">Ниже приведен код для 16-разрядного раздела.</span><span class="sxs-lookup"><span data-stu-id="23bf2-140">Here is the code for the 16-bit section:</span></span>


```C++
// Increment the local delay pointer.
// If it is past the end of the buffer,
// then move it to the head of the buffer.
if (++pwDelayPointer > pwEOFDelayBuffer)
    pwDelayPointer = pwDelayBuffer;

```



<span data-ttu-id="23bf2-141">Поскольку указатель в 16-разрядном разделе действительно является копией переменной-члена, необходимо не забывать обновить значение в переменной-члене новым адресом.</span><span class="sxs-lookup"><span data-stu-id="23bf2-141">Since the pointer in the 16-bit section is really a copy of the member variable, you must remember to update the value in the member variable with the new address.</span></span> <span data-ttu-id="23bf2-142">Если этого не сделать, указатель буфера задержки будет указывать на заголовок буфера несколько раз, и ваш экран эха не будет работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="23bf2-142">If you fail to do this, the delay buffer pointer will point to the head of the buffer repeatedly and your echo effect will not work as expected.</span></span> <span data-ttu-id="23bf2-143">Добавьте следующий код в 16-разрядный раздел:</span><span class="sxs-lookup"><span data-stu-id="23bf2-143">Add the following code to the 16-bit section:</span></span>


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a><span data-ttu-id="23bf2-144">Смешанный образец входных данных с образцом Delay</span><span class="sxs-lookup"><span data-stu-id="23bf2-144">Mix the Input Sample with the Delay Sample</span></span>

<span data-ttu-id="23bf2-145">В этом случае для создания окончательного примера выходных данных используются значения задолженности и набора сухой.</span><span class="sxs-lookup"><span data-stu-id="23bf2-145">This is where you use the wet mix and dry mix values to create the final output sample.</span></span> <span data-ttu-id="23bf2-146">Вы просто умножаете каждый выбор на значение с плавающей запятой, представляющее процент финального сигнала для образца.</span><span class="sxs-lookup"><span data-stu-id="23bf2-146">You simply multiply each sample by the floating-point value that represents the percentage of the final signal for the sample.</span></span> <span data-ttu-id="23bf2-147">Умножьте входную выборку на значение, хранящееся в m \_ фдримикс; умножьте образец задержки на значение, хранящееся в m \_ фветмикс.</span><span class="sxs-lookup"><span data-stu-id="23bf2-147">Multiply the input sample by the value stored in m\_fDryMix; multiply the delay sample by the value stored in m\_fWetMix.</span></span> <span data-ttu-id="23bf2-148">Затем добавьте два значения.</span><span class="sxs-lookup"><span data-stu-id="23bf2-148">Then, add the two values.</span></span> <span data-ttu-id="23bf2-149">Код, который необходимо добавить, идентичен для 8-разрядных и 16-разрядных разделов:</span><span class="sxs-lookup"><span data-stu-id="23bf2-149">The code you must add is identical for the 8-bit and 16-bit sections:</span></span>


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a><span data-ttu-id="23bf2-150">Запись данных в выходной буфер</span><span class="sxs-lookup"><span data-stu-id="23bf2-150">Write the Data to the Output Buffer</span></span>

<span data-ttu-id="23bf2-151">Наконец, скопируйте смешанный пример в выходной буфер, а затем переведите указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="23bf2-151">Finally, copy the mixed sample to the output buffer, and then advance the output buffer pointer.</span></span> <span data-ttu-id="23bf2-152">Для 8-разрядного звука мастер подключаемых модулей использует следующий код для возврата образца к исходному диапазону:</span><span class="sxs-lookup"><span data-stu-id="23bf2-152">For 8-bit audio, the plug-in wizard uses the following code to return the sample to its original range:</span></span>


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



<span data-ttu-id="23bf2-153">Для 16-разрядного звука мастер использует следующий код в качестве последнего шага цикла обработки:</span><span class="sxs-lookup"><span data-stu-id="23bf2-153">For 16-bit audio, the wizard uses the following code as the final step in the processing loop:</span></span>


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a><span data-ttu-id="23bf2-154">См. также</span><span class="sxs-lookup"><span data-stu-id="23bf2-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23bf2-155">**Реализация Цечо::D Опроцессаутпут**</span><span class="sxs-lookup"><span data-stu-id="23bf2-155">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




