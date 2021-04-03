---
title: Использование окна или потока для обработки сообщений драйвера
description: Использование окна или потока для обработки сообщений драйвера
ms.assetid: 7a9eaaa1-d3b0-400e-8fbf-ee5fe59efc32
keywords:
- Звукозапись, обратный вызов окна
- блоки звуковых данных, обратный вызов окна
- звуковая волна, обратный вызов потока
- блоки звуковых данных, обратный вызов потока
- звуковая волна, обработка сообщений драйвера
- блоки звуковых данных, обработка сообщений драйверов
- Обработка сообщений драйвера
- Функция Вавеинопен
- Функция Вавеаутопен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a147bd86b3c8045456ef9961039f645fd4023f13
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987504"
---
# <a name="using-a-window-or-thread-to-process-driver-messages"></a><span data-ttu-id="b0fd0-112">Использование окна или потока для обработки сообщений драйвера</span><span class="sxs-lookup"><span data-stu-id="b0fd0-112">Using a Window or Thread to Process Driver Messages</span></span>

<span data-ttu-id="b0fd0-113">Чтобы использовать функцию обратного вызова окна, укажите флаг окна ОБРАТНОго вызова \_ в параметре *фдвопен* и маркер окна в младшем слове параметра *Двкаллбакк* функции [**вавеинопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) или [**вавеаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="b0fd0-113">To use a window callback function, specify the CALLBACK\_WINDOW flag in the *fdwOpen* parameter and a window handle in the low-order word of the *dwCallback* parameter of the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span> <span data-ttu-id="b0fd0-114">Сообщения драйвера будут отправляться в оконную процедуру для окна, идентифицируемого по маркеру в *двкаллбакк*.</span><span class="sxs-lookup"><span data-stu-id="b0fd0-114">Driver messages will be sent to the window procedure for the window identified by the handle in *dwCallback*.</span></span>

<span data-ttu-id="b0fd0-115">Аналогично, чтобы использовать обратный вызов потока, укажите поток ОБРАТНОго вызова \_ и обработчик потока в вызове **Вавеинопен** или **вавеаутопен**.</span><span class="sxs-lookup"><span data-stu-id="b0fd0-115">Similarly, to use a thread callback, specify CALLBACK\_THREAD and a thread handle in the call to **waveInOpen** or **waveOutOpen**.</span></span> <span data-ttu-id="b0fd0-116">В этом случае сообщения отправляются в указанный поток, а не в окно.</span><span class="sxs-lookup"><span data-stu-id="b0fd0-116">In this case, messages are posted to the specified thread instead of to a window.</span></span>

<span data-ttu-id="b0fd0-117">Сообщения, отправленные в обратный вызов окна или потока, относятся к используемому типу звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="b0fd0-117">Messages sent to the window or thread callback are specific to the audio device type used.</span></span> <span data-ttu-id="b0fd0-118">Дополнительные сведения об этих сообщениях см. в разделе [воспроизведение Waveform-Audio файлов](playing-waveform-audio-files.md).</span><span class="sxs-lookup"><span data-stu-id="b0fd0-118">For more information about these messages, see [Playing Waveform-Audio Files](playing-waveform-audio-files.md).</span></span>

 

 