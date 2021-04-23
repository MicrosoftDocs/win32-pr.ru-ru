---
title: Использование уровней времени
description: Использование уровней времени
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- визуализации, события с превышением времени
- Пользовательские визуализации, события с превышением времени
- визуализации, массив частоты
- Пользовательские визуализации, массив частоты
- визуализации, массив форм
- Пользовательские визуализации, массив форм
- визуализации, переменная состояния
- Пользовательские визуализации, переменная состояния
- визуализации, переменная timeStamp
- Пользовательские визуализации, переменная timeStamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d9a23818d57305b3b205ea2e17b6dda2884e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067999"
---
# <a name="using-timed-levels"></a><span data-ttu-id="58503-113">Использование уровней времени</span><span class="sxs-lookup"><span data-stu-id="58503-113">Using Timed Levels</span></span>

<span data-ttu-id="58503-114">Структура **тимедлевел** состоит из 2 2 многомерных массивов, значения состояния и значения метки времени.</span><span class="sxs-lookup"><span data-stu-id="58503-114">The **TimedLevel** structure is composed of two two-dimensional arrays, a state value, and a time stamp value.</span></span>

## <a name="frequency-array"></a><span data-ttu-id="58503-115">Массив частоты</span><span class="sxs-lookup"><span data-stu-id="58503-115">Frequency Array</span></span>

<span data-ttu-id="58503-116">Массив периодичности является двумерным массивом.</span><span class="sxs-lookup"><span data-stu-id="58503-116">The frequency array is a two-dimensional array.</span></span> <span data-ttu-id="58503-117">Первое измерение каждого массива соответствует стерео аудио-каналу (слева или справа), а второе соответствует уровню частоты (в байтах) моментального снимка, где спектр звука делится на 1024 регионов.</span><span class="sxs-lookup"><span data-stu-id="58503-117">The first dimension of each array corresponds to the stereo audio channel (left or right), and the second corresponds to the frequency levels (in bytes) of the snapshot, where the audio spectrum is divided up into 1024 regions.</span></span>

<span data-ttu-id="58503-118">Данные массива частоты, предоставляемые проигрывателем Windows Media, можно получить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="58503-118">You can get the frequency array data supplied from the Windows Media Player in the following manner:</span></span>


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



<span data-ttu-id="58503-119">Значение моментального снимка — для левого канала и содержит значение наименьшей части спектра частот.</span><span class="sxs-lookup"><span data-stu-id="58503-119">The value of snapshot is for the left channel and contains the value of the lowest part of the frequency spectrum.</span></span> <span data-ttu-id="58503-120">Например, если моментальный снимок имеет большое значение, это указывает на то, что самая низкая 1024th часть спектра частот имеет широкую частоту.</span><span class="sxs-lookup"><span data-stu-id="58503-120">For example, if snapshot has a large value, it indicates that the lowest 1024th part of the frequency spectrum is rich in frequency.</span></span> <span data-ttu-id="58503-121">Нулевое значение указывает на отсутствие значений с низкой частотой в части спектра для левого канала.</span><span class="sxs-lookup"><span data-stu-id="58503-121">A value of zero indicates no low frequency values in that part of the spectrum for the left channel.</span></span> <span data-ttu-id="58503-122">Если у вас есть сигнал монофоник, то только первое измерение имеет допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="58503-122">If you have a monophonic signal, only the first dimension has valid values.</span></span>

<span data-ttu-id="58503-123">Если сигнал не стерео, второй массив будет содержать копию сигнала Mono.</span><span class="sxs-lookup"><span data-stu-id="58503-123">If the signal is non-stereo, then the second array will contain a copy of the mono signal.</span></span> <span data-ttu-id="58503-124">То есть частота \[ 0 \] \[ *n* \] и частота \[ 1 \] \[ *n* \] будут содержать одни и те же данные, где *n* — индекс в определенной ячейке.</span><span class="sxs-lookup"><span data-stu-id="58503-124">That is, frequency\[0\]\[*n*\] and frequency\[1\]\[*n*\] will contain the same data, where *n* is the index into a particular cell.</span></span>

## <a name="waveform-array"></a><span data-ttu-id="58503-125">Массив форм</span><span class="sxs-lookup"><span data-stu-id="58503-125">Waveform Array</span></span>

<span data-ttu-id="58503-126">Массив форм-волнового типа также является двумерным массивом.</span><span class="sxs-lookup"><span data-stu-id="58503-126">The waveform array is also a two-dimensional array.</span></span> <span data-ttu-id="58503-127">Первое измерение массива соответствует каналу (слева или справа), а второе соответствует уровням питания (в байтах) моментального снимка, в котором звуковая мощность разбивается на 1024 смежных сегментов времени.</span><span class="sxs-lookup"><span data-stu-id="58503-127">The first dimension of the array corresponds to the channel (left or right), and the second corresponds to the power levels (in bytes) of the snapshot, where the audio power is broken up into 1024 contiguous time segments.</span></span>

<span data-ttu-id="58503-128">Данные массива волны можно получить из проигрывателя Windows Media следующим образом:</span><span class="sxs-lookup"><span data-stu-id="58503-128">You can get the waveform array data from Windows Media Player in the following manner:</span></span>


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



<span data-ttu-id="58503-129">Значение snapshot предназначено для левого канала и содержит первое значение квантованияного снимка значений питания.</span><span class="sxs-lookup"><span data-stu-id="58503-129">The value of snapshot is for the left channel and contains the first value of the quantized snapshot of the power values.</span></span> <span data-ttu-id="58503-130">При создании моментального снимка он состоит из 1024 маленьких добавочных измерений в отношении звуковых возможностей.</span><span class="sxs-lookup"><span data-stu-id="58503-130">When a snapshot is taken, it consists of 1024 tiny incremental measurements of the audio power.</span></span> <span data-ttu-id="58503-131">Наименьшее значение массива формируется первым добавочным измерением звуковой мощности.</span><span class="sxs-lookup"><span data-stu-id="58503-131">The lowest value of the array is generated by the first incremental measurement of audio power.</span></span> <span data-ttu-id="58503-132">Обратите внимание, что значения степени измеряются от-128 до + 127, а значения в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="58503-132">Note that the values of the power are measured from -128 to +127 but the values in the array range from 0 to 255.</span></span> <span data-ttu-id="58503-133">Если у вас есть монофоник волна, то только первое измерение будет иметь допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="58503-133">If you have a monophonic wave, only the first dimension will have valid values.</span></span>

<span data-ttu-id="58503-134">Если сигнал не стерео, второй массив будет содержать копию сигнала Mono.</span><span class="sxs-lookup"><span data-stu-id="58503-134">If the signal is non-stereo, then the second array will contain a copy of the mono signal.</span></span> <span data-ttu-id="58503-135">То есть, волна \[ 0 \] \[ *n* \] и волна \[ 1 \] \[ *n* \] будут содержать одни и те же данные, где *n* — индекс в определенной ячейке.</span><span class="sxs-lookup"><span data-stu-id="58503-135">That is, waveform\[0\]\[*n*\] and waveform\[1\]\[*n*\] will contain the same data, where *n* is the index into a particular cell.</span></span>

## <a name="state"></a><span data-ttu-id="58503-136">Состояние</span><span class="sxs-lookup"><span data-stu-id="58503-136">State</span></span>

<span data-ttu-id="58503-137">Переменная состояния отражает состояние воспроизведения звука проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="58503-137">The state variable reflects the audio playback state of Windows Media Player.</span></span> <span data-ttu-id="58503-138">Значения перечисления Плайерстате</span><span class="sxs-lookup"><span data-stu-id="58503-138">The PlayerState enumeration values are</span></span>


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



<span data-ttu-id="58503-139">Эту переменную можно использовать для выполнения различных действий в зависимости от состояния воспроизведения звука.</span><span class="sxs-lookup"><span data-stu-id="58503-139">You can use this variable to take different actions depending on the audio playback state.</span></span> <span data-ttu-id="58503-140">Например, можно воспроизвести один тип визуализации при воспроизведении звука, а другой — при его остановке.</span><span class="sxs-lookup"><span data-stu-id="58503-140">For example, you can play one kind of visualization when the audio is playing and another when it is stopped.</span></span>

## <a name="time-stamp"></a><span data-ttu-id="58503-141">Метка времени</span><span class="sxs-lookup"><span data-stu-id="58503-141">Time Stamp</span></span>

<span data-ttu-id="58503-142">Переменная timeStamp отражает текущее время создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="58503-142">The timeStamp variable reflects the current time when the snapshot is taken.</span></span> <span data-ttu-id="58503-143">Это можно использовать для измерения частоты создания моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="58503-143">This can be used to measure how frequently the snapshots are taken.</span></span>

<span data-ttu-id="58503-144">Эту переменную можно использовать для времени анимации.</span><span class="sxs-lookup"><span data-stu-id="58503-144">You can use this variable to time your animations.</span></span> <span data-ttu-id="58503-145">Если моментальные снимки слишком часто используются, вы можете постепенно снизить изображение, чтобы оно отображалось выбранным способом.</span><span class="sxs-lookup"><span data-stu-id="58503-145">If the snapshots are too frequent, you can gracefully degrade your image to display in the manner you choose.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58503-146">См. также</span><span class="sxs-lookup"><span data-stu-id="58503-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58503-147">**Реализация отрисовки**</span><span class="sxs-lookup"><span data-stu-id="58503-147">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




