---
title: Остановка, приостановка и перезапуск воспроизведения
description: Остановка, приостановка и перезапуск воспроизведения
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- звуковая волна, остановка воспроизведения
- волна — аудио-интерфейс, остановка воспроизведения
- Воспроизведение аудио-файлов, остановка воспроизведения
- звуковая волна, приостановка воспроизведения
- волна-Audio Interface, приостановка воспроизведения
- Воспроизведение аудио-файлов, приостановка воспроизведения
- волна аудио, перезапуск воспроизведения
- волна-Audio Interface, перезапуск воспроизведения
- Воспроизведение аудио-файлов, перезапуск воспроизведения
- Функция Вавеаутпаусе
- Функция Вавеаутресет
- Функция Вавеаутрестарт
- Остановка воспроизведения аудио-сигнала
- Приостановка воспроизведения аудио-сигнала
- перезапуск воспроизведения аудио-сигнала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6a4756a08317923056114259588a95bc62e97f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133726"
---
# <a name="stopping-pausing-and-restarting-playback"></a><span data-ttu-id="7bdc0-118">Остановка, приостановка и перезапуск воспроизведения</span><span class="sxs-lookup"><span data-stu-id="7bdc0-118">Stopping, Pausing, and Restarting Playback</span></span>

<span data-ttu-id="7bdc0-119">Вы можете остановить или приостановить воспроизведение во время воспроизведения аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="7bdc0-119">You can stop or pause playback while waveform audio is playing.</span></span> <span data-ttu-id="7bdc0-120">После приостановки воспроизведения его можно перезапустить.</span><span class="sxs-lookup"><span data-stu-id="7bdc0-120">After playback has been paused, you can restart it.</span></span> <span data-ttu-id="7bdc0-121">Windows предоставляет следующие функции для управления воспроизведением аудио-звука.</span><span class="sxs-lookup"><span data-stu-id="7bdc0-121">Windows provides the following functions for controlling waveform-audio playback.</span></span>



| <span data-ttu-id="7bdc0-122">Функция</span><span class="sxs-lookup"><span data-stu-id="7bdc0-122">Function</span></span>                                 | <span data-ttu-id="7bdc0-123">Описание</span><span class="sxs-lookup"><span data-stu-id="7bdc0-123">Description</span></span>                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7bdc0-124">**вавеаутпаусе**</span><span class="sxs-lookup"><span data-stu-id="7bdc0-124">**waveOutPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | <span data-ttu-id="7bdc0-125">Приостанавливает воспроизведение на устройстве вывода аудио-аудио.</span><span class="sxs-lookup"><span data-stu-id="7bdc0-125">Pauses playback on a waveform-audio output device.</span></span>                                          |
| [<span data-ttu-id="7bdc0-126">**вавеаутресет**</span><span class="sxs-lookup"><span data-stu-id="7bdc0-126">**waveOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | <span data-ttu-id="7bdc0-127">Останавливает воспроизведение на устройстве вывода аудио-файлов и помечает все ожидающие блоки данных как выполненные.</span><span class="sxs-lookup"><span data-stu-id="7bdc0-127">Stops playback on a waveform-audio output device and marks all pending data blocks as done.</span></span> |
| [<span data-ttu-id="7bdc0-128">**вавеаутрестарт**</span><span class="sxs-lookup"><span data-stu-id="7bdc0-128">**waveOutRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | <span data-ttu-id="7bdc0-129">Возобновляет воспроизведение на приостановленном устройстве вывода аудио-аудио.</span><span class="sxs-lookup"><span data-stu-id="7bdc0-129">Resumes playback on a paused waveform-audio output device.</span></span>                                  |



 

<span data-ttu-id="7bdc0-130">Приостановка устройства аудио-сигнала с помощью [**вавеаутпаусе**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) может оказаться немгновенной. драйвер может завершить воспроизведение текущего блока перед приостановкой воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7bdc0-130">Pausing a waveform-audio device by using [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) might not be instantaneous; the driver may finish playing the current block before pausing playback.</span></span>

<span data-ttu-id="7bdc0-131">Как правило, после отправки первого блока данных звуковой волны с помощью функции [**вавеаутврите**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) устройство аудио-аудио начинает воспроизводиться.</span><span class="sxs-lookup"><span data-stu-id="7bdc0-131">Generally, as soon as the first waveform-audio data block is sent by using the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function, the waveform-audio device begins playing.</span></span> <span data-ttu-id="7bdc0-132">Если вы не хотите, чтобы воспроизведение было начато немедленно, вызовите **вавеаутпаусе** перед вызовом **вавеаутврите**.</span><span class="sxs-lookup"><span data-stu-id="7bdc0-132">If you do not want the sound to start playing immediately, call **waveOutPause** before calling **waveOutWrite**.</span></span> <span data-ttu-id="7bdc0-133">Затем, когда вы хотите начать воспроизведение аудио-данных, вызовите [**вавеаутрестарт**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).</span><span class="sxs-lookup"><span data-stu-id="7bdc0-133">Then, when you want to begin playing waveform-audio data, call [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).</span></span>

<span data-ttu-id="7bdc0-134">Нельзя использовать **вавеаутрестарт** для перезапуска устройства, которое было остановлено с помощью [**вавеаутресет**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); необходимо использовать **вавеаутврите** для отправки первого блока данных, чтобы возобновить воспроизведение на устройстве.</span><span class="sxs-lookup"><span data-stu-id="7bdc0-134">You cannot use **waveOutRestart** to restart a device that has been stopped with [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); you must use **waveOutWrite** to send the first data block to resume playback on the device.</span></span>

 

 