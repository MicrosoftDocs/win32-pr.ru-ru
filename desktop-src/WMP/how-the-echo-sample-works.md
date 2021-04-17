---
title: Как работает образец Echo
description: Как работает образец Echo
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Подключаемые модули проигрывателя Windows Media, обзор эхо-образца
- подключаемые модули, Обзор примера эхо
- подключаемые модули обработки цифровых сигналов, обзор образца эха
- Подключаемые модули DSP, Обзор примера эхо
- Пример подключаемого модуля Echo DSP, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08814a6f0d604c7d566a0fc8d9f07b05446fca64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691248"
---
# <a name="how-the-echo-sample-works"></a><span data-ttu-id="3ee9c-108">Как работает образец Echo</span><span class="sxs-lookup"><span data-stu-id="3ee9c-108">How the Echo Sample Works</span></span>

<span data-ttu-id="3ee9c-109">Код создает эхо-результат, выделяя буфер достаточно большим, чтобы вместить ровно то количество звуковых данных, которое может быть визуализировано за кадр времени, заданный значением времени задержки.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-109">The code creates the echo effect by allocating a buffer large enough to contain exactly the amount of audio data that can be rendered in the time frame specified by the delay time value.</span></span> <span data-ttu-id="3ee9c-110">Размер буфера вычисляется в байтах по следующей формуле:</span><span class="sxs-lookup"><span data-stu-id="3ee9c-110">The size of the buffer is calculated, in bytes, by the following formula:</span></span>

<span data-ttu-id="3ee9c-111">Размер буфера = \* Частота выборки по времени задержки/1000. \* Выравнивание блока</span><span class="sxs-lookup"><span data-stu-id="3ee9c-111">buffer size = delay time \* sample rate / 1000 \* block alignment</span></span>

<span data-ttu-id="3ee9c-112">Время задержки в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-112">The delay time is in milliseconds.</span></span> <span data-ttu-id="3ee9c-113">Значения частоты выборки и выравнивания блока задаются в структуре ВАВЕФОРМАТЕКС.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-113">The sample rate and block alignment values are given in a WAVEFORMATEX structure.</span></span> <span data-ttu-id="3ee9c-114">Скорость выборки определяется в примерах в секунду; при делении на 1000 выдаются образцы на миллисекунду.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-114">The sample rate is in samples per second; dividing by 1000 yields samples per millisecond.</span></span> <span data-ttu-id="3ee9c-115">Выравнивание блока равно числу каналов (1 для Mono, 2 для стерео) и числу битов на выборку (8 или 16), деленную на 8 (бит на байт).</span><span class="sxs-lookup"><span data-stu-id="3ee9c-115">The block alignment is equal to the product of the number of channels (1 for mono, 2 for stereo) and the number of bits per sample (8 or 16) divided by 8 (bits per byte).</span></span>

<span data-ttu-id="3ee9c-116">В дополнение к переменной указателя, указывающей на заголовок буфера задержки, код создает перемещаемый указатель, который проходит через данные в буфере в процессе синхронизации с циклом обработки в функции **допроцессаутпут** .</span><span class="sxs-lookup"><span data-stu-id="3ee9c-116">In addition to the pointer variable that points to the head of the delay buffer, the code creates a movable pointer that steps through the data in the buffer in synchronization with the processing loop in the **DoProcessOutput** function.</span></span> <span data-ttu-id="3ee9c-117">Когда перемещаемый указатель достигает конца буфера задержки, он перемещается обратно в конец буфера.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-117">When the movable pointer reaches the end of the delay buffer, it moves back to the head of the buffer.</span></span> <span data-ttu-id="3ee9c-118">Буфер, используемый таким способом, называется циклическим буфером.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-118">A buffer used in this manner is called a circular buffer.</span></span>

<span data-ttu-id="3ee9c-119">Когда буфер задержки существует, и проигрыватель Windows Media выделил входной буфер для передачи звуковых данных и выходной буфер для получения обработанных звуковых данных, обработка эха продолжается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3ee9c-119">Once the delay buffer exists, and Windows Media Player has allocated an input buffer to supply audio data and an output buffer to receive processed audio data, the echo processing proceeds like this:</span></span>

1.  <span data-ttu-id="3ee9c-120">Введите цикл, который позволяет обрабатывать каждый звуковой образец во входном буфере.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-120">Enter a loop that allows processing of each audio sample in the input buffer.</span></span>
2.  <span data-ttu-id="3ee9c-121">Получение примера из входного буфера.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-121">Retrieve a sample from the input buffer.</span></span> <span data-ttu-id="3ee9c-122">Затем переместите указатель входного буфера вперед к следующему примеру, чтобы подготовиться к итерации следующего цикла.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-122">Then, move the input buffer pointer forward to the next sample to prepare for the next loop iteration.</span></span>
3.  <span data-ttu-id="3ee9c-123">Получение примера из буфера задержки.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-123">Retrieve a sample from the delay buffer.</span></span>
4.  <span data-ttu-id="3ee9c-124">Скопируйте пример из входного буфера в то же расположение в буфере задержки, из которого был получен образец с последней задержкой.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-124">Copy the sample from the input buffer to the same location in the delay buffer from which the last delay sample was retrieved.</span></span>
5.  <span data-ttu-id="3ee9c-125">Переместите указатель буфера задержки вперед к следующему примеру.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-125">Move the delay buffer pointer forward to the next sample.</span></span> <span data-ttu-id="3ee9c-126">Если указатель перемещается за концом буфера, переместите его в начало буфера.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-126">If the pointer moves past the end of the buffer, move it to the head of the buffer.</span></span>
6.  <span data-ttu-id="3ee9c-127">Объедините пример из входного буфера с примером из буфера задержки.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-127">Combine the sample from the input buffer with the sample from the delay buffer.</span></span>
7.  <span data-ttu-id="3ee9c-128">Скопируйте результат в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-128">Copy the result to the output buffer.</span></span> <span data-ttu-id="3ee9c-129">Затем переместите указатель выходного буфера на следующую единицу, чтобы подготовиться к итерации следующего цикла.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-129">Then, move the output buffer pointer forward to the next unit to prepare for the next loop iteration.</span></span>
8.  <span data-ttu-id="3ee9c-130">Повторяйте до тех пор, пока не будут обработаны все образцы.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-130">Repeat until all the samples are processed.</span></span>

<span data-ttu-id="3ee9c-131">Когда входной пример, полученный на шаге 2, копируется в буфер задержки на шаге 4, он остается там до тех пор, пока перемещаемый указатель не пойдет через каждый пример в буфере задержки и не вернется к той же позиции.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-131">When an input sample retrieved in step 2 is copied to the delay buffer in step 4, it remains there until the movable pointer steps through each sample in the delay buffer and finally returns to the same position.</span></span> <span data-ttu-id="3ee9c-132">Поскольку размер буфера задержки соответствует времени задержки, время, прошедшее между копированием выборки в буфер задержки и возвращаемым примером, равно заданной задержке (плюс любые задержки, появившиеся в реальной обработке).</span><span class="sxs-lookup"><span data-stu-id="3ee9c-132">Because the size of the delay buffer is designed to correspond to the delay time, the elapsed time between the sample being copied to the delay buffer and the sample being retrieved once again equals the specified delay (plus any latency introduced by the actual processing).</span></span>

<span data-ttu-id="3ee9c-133">При запуске потока данные задержки не создаются до истечения времени задержки.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-133">When a stream starts, no delay data is generated until the delay time has elapsed.</span></span> <span data-ttu-id="3ee9c-134">Поэтому важно, чтобы буфер задержки изначально содержал тишину.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-134">Therefore, it is important that the delay buffer initially contains silence.</span></span> <span data-ttu-id="3ee9c-135">Если буфер задержки содержит случайные данные, пользователь будет слышать белый шум до тех пор, пока подключаемый модуль не создаст достаточно данных задержки для перезаписи всего буфера задержки.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-135">If the delay buffer contains random data, the user will hear white noise until the plug-in generates enough delay data to overwrite the entire delay buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ee9c-136">См. также</span><span class="sxs-lookup"><span data-stu-id="3ee9c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ee9c-137">**Обзор образца эхо**</span><span class="sxs-lookup"><span data-stu-id="3ee9c-137">**Echo Sample Overview**</span></span>](echo-sample-overview.md)
</dt> </dl>

 

 




