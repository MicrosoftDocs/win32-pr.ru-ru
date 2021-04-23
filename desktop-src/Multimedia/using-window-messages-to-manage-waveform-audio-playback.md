---
title: Использование оконных сообщений для управления воспроизведением Waveform-Audio
description: Использование оконных сообщений для управления воспроизведением Waveform-Audio
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- звуковая волна, Управление воспроизведением с помощью сообщений
- аудио-интерфейс, Управление воспроизведением с помощью сообщений
- Воспроизведение аудио-файлов, Управление воспроизведением с помощью сообщений
- звуковая волна, сообщения
- волна — аудио-интерфейс, сообщения
- Воспроизведение аудио-файлов, сообщений
- Сообщение MM_WOM_CLOSE
- Сообщение MM_WOM_DONE
- Сообщение MM_WOM_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02794222274e10498e31e0f38939d930ef3745
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337100"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a><span data-ttu-id="7fe49-112">Использование оконных сообщений для управления воспроизведением Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="7fe49-112">Using Window Messages to Manage Waveform-Audio Playback</span></span>

<span data-ttu-id="7fe49-113">Следующие сообщения могут быть отправлены в функцию окна процедуры для управления воспроизведением аудио-звука.</span><span class="sxs-lookup"><span data-stu-id="7fe49-113">The following messages can be sent to a window procedure function for managing waveform-audio playback.</span></span>



| <span data-ttu-id="7fe49-114">Сообщение</span><span class="sxs-lookup"><span data-stu-id="7fe49-114">Message</span></span>                                | <span data-ttu-id="7fe49-115">Описание</span><span class="sxs-lookup"><span data-stu-id="7fe49-115">Description</span></span>                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fe49-116">**вом мм, \_ \_ закрытие**</span><span class="sxs-lookup"><span data-stu-id="7fe49-116">**MM\_WOM\_CLOSE**</span></span>](mm-wom-close.md) | <span data-ttu-id="7fe49-117">Отправляется, когда устройство закрывается с помощью функции [**вавеаутклосе**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) .</span><span class="sxs-lookup"><span data-stu-id="7fe49-117">Sent when the device is closed by using the [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) function.</span></span>                                 |
| [<span data-ttu-id="7fe49-118">**MM \_ вом \_ done**</span><span class="sxs-lookup"><span data-stu-id="7fe49-118">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)   | <span data-ttu-id="7fe49-119">Посылается, когда драйвер устройства завершает работу с блоком данных, отправленным с помощью функции [**вавеаутврите**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) .</span><span class="sxs-lookup"><span data-stu-id="7fe49-119">Sent when the device driver is finished with a data block sent by using the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function.</span></span> |
| [<span data-ttu-id="7fe49-120">**\_вом мм \_ Open**</span><span class="sxs-lookup"><span data-stu-id="7fe49-120">**MM\_WOM\_OPEN**</span></span>](mm-wom-open.md)   | <span data-ttu-id="7fe49-121">Отправляется при открытии устройства с помощью функции [**вавеаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="7fe49-121">Sent when the device is opened by using the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>                                   |



 

<span data-ttu-id="7fe49-122">С каждым из этих сообщений связан параметр *wParam* и *lParam* .</span><span class="sxs-lookup"><span data-stu-id="7fe49-122">A *wParam* and *lParam* parameter is associated with each of these messages.</span></span> <span data-ttu-id="7fe49-123">Параметр *wParam* всегда задает маркер открытого устройства аудио-аудио.</span><span class="sxs-lookup"><span data-stu-id="7fe49-123">The *wParam* parameter always specifies a handle of the open waveform-audio device.</span></span> <span data-ttu-id="7fe49-124">Для сообщения [**о \_ \_ завершении вом mm**](mm-wom-done.md) параметр *lParam* указывает указатель на структуру [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , которая идентифицирует завершенный блок данных.</span><span class="sxs-lookup"><span data-stu-id="7fe49-124">For the [**MM\_WOM\_DONE**](mm-wom-done.md) message, *lParam* specifies a pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the completed data block.</span></span> <span data-ttu-id="7fe49-125">Параметр *lParam* не используется для открытых сообщений [**mm \_ вом \_ Close**](mm-wom-close.md) и [**mm \_ вом \_**](mm-wom-open.md) .</span><span class="sxs-lookup"><span data-stu-id="7fe49-125">The *lParam* parameter is unused for the [**MM\_WOM\_CLOSE**](mm-wom-close.md) and [**MM\_WOM\_OPEN**](mm-wom-open.md) messages.</span></span>

<span data-ttu-id="7fe49-126">Наиболее полезное сообщение, скорее всего, равно MM \_ вом \_ .</span><span class="sxs-lookup"><span data-stu-id="7fe49-126">The most useful message is probably MM\_WOM\_DONE.</span></span> <span data-ttu-id="7fe49-127">Когда это сообщение сигнализирует о завершении воспроизведения блока данных, можно очистить и освободить блок данных.</span><span class="sxs-lookup"><span data-stu-id="7fe49-127">When this message signals that playback of a data block is complete, you can clean up and free the data block.</span></span> <span data-ttu-id="7fe49-128">Если вам не нужно распределять память или инициализировать переменные, вам, вероятно, не нужно обрабатывать \_ \_ сообщения вом Open и mm \_ вом \_ Close.</span><span class="sxs-lookup"><span data-stu-id="7fe49-128">Unless you need to allocate memory or initialize variables, you probably do not need to process the MM\_WOM\_OPEN and MM\_WOM\_CLOSE messages.</span></span>

<span data-ttu-id="7fe49-129">Функция обратного вызова для устройств вывода аудио-аудиосигнала предоставляется приложением.</span><span class="sxs-lookup"><span data-stu-id="7fe49-129">The callback function for waveform-audio output devices is supplied by the application.</span></span> <span data-ttu-id="7fe49-130">Сведения об этой функции обратного вызова см. в описании функции [**вавеаутпрок**](/previous-versions//dd743869(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7fe49-130">For information about this callback function, see the [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) function.</span></span>

 

 