---
title: Использование оконных сообщений для управления записью Waveform-Audio
description: Использование оконных сообщений для управления записью Waveform-Audio
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- волна аудио, управление записью с помощью сообщений
- аудио-интерфейс, управление записью с помощью сообщений
- запись звука звукозаписи, управление записью с помощью сообщений
- звуковая волна, сообщения
- волна — аудио-интерфейс, сообщения
- запись аудио звукового сигнала, сообщений
- Сообщение MM_WIM_CLOSE
- Сообщение MM_WIM_DATA
- Сообщение MM_WIM_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bb1cfe1ed0f7ba6052fc1eb6af8fca8355d87d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487580"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a><span data-ttu-id="04501-112">Использование оконных сообщений для управления записью Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="04501-112">Using Window Messages to Manage Waveform-Audio Recording</span></span>

<span data-ttu-id="04501-113">Следующие сообщения могут быть отправлены в функцию процедуры Windows для управления записью аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="04501-113">The following messages can be sent to a window procedure function for managing waveform-audio recording.</span></span>



| <span data-ttu-id="04501-114">Сообщение</span><span class="sxs-lookup"><span data-stu-id="04501-114">Message</span></span>                                | <span data-ttu-id="04501-115">Описание</span><span class="sxs-lookup"><span data-stu-id="04501-115">Description</span></span>                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04501-116">**MM \_ , \_ закрытие WIM**</span><span class="sxs-lookup"><span data-stu-id="04501-116">**MM\_WIM\_CLOSE**</span></span>](mm-wim-close.md) | <span data-ttu-id="04501-117">Отправляется, когда устройство закрывается с помощью функции [**вавеинклосе**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) .</span><span class="sxs-lookup"><span data-stu-id="04501-117">Sent when the device is closed by using the [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) function.</span></span>                                     |
| [<span data-ttu-id="04501-118">**MM \_ . \_ данные WIM**</span><span class="sxs-lookup"><span data-stu-id="04501-118">**MM\_WIM\_DATA**</span></span>](mm-wim-data.md)   | <span data-ttu-id="04501-119">Посылается, когда драйвер устройства завершает работу с буфером, отправленным с помощью функции [**вавеинаддбуффер**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) .</span><span class="sxs-lookup"><span data-stu-id="04501-119">Sent when the device driver is finished with a buffer sent by using the [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) function.</span></span> |
| [<span data-ttu-id="04501-120">**ММ — \_ открытый WIM-файл \_**</span><span class="sxs-lookup"><span data-stu-id="04501-120">**MM\_WIM\_OPEN**</span></span>](mm-wim-open.md)   | <span data-ttu-id="04501-121">Отправляется при открытии устройства с помощью функции [**вавеинопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) .</span><span class="sxs-lookup"><span data-stu-id="04501-121">Sent when the device is opened by using the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function.</span></span>                                       |



 

<span data-ttu-id="04501-122">Параметр *lParam* [**\_ \_ данных типа mm**](mm-wim-data.md) указывает указатель на структуру [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , которая идентифицирует буфер.</span><span class="sxs-lookup"><span data-stu-id="04501-122">The *lParam* parameter of [**MM\_WIM\_DATA**](mm-wim-data.md) specifies a pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer.</span></span> <span data-ttu-id="04501-123">Этот буфер может быть не полностью заполнен данными волны-Audio. запись может быть прервана до заполнения буфера.</span><span class="sxs-lookup"><span data-stu-id="04501-123">This buffer might not be completely filled with waveform-audio data; recording can stop before the buffer is filled.</span></span> <span data-ttu-id="04501-124">Используйте элемент **двбитесрекордед** структуры **вавехдр** , чтобы определить объем допустимых данных, имеющихся в буфере.</span><span class="sxs-lookup"><span data-stu-id="04501-124">Use the **dwBytesRecorded** member of the **WAVEHDR** structure to determine the amount of valid data present in the buffer.</span></span>

<span data-ttu-id="04501-125">Наиболее полезное сообщение —, скорее всего, [**mm- \_ \_ данные WIM**](mm-wim-data.md).</span><span class="sxs-lookup"><span data-stu-id="04501-125">The most useful message is probably [**MM\_WIM\_DATA**](mm-wim-data.md).</span></span> <span data-ttu-id="04501-126">Когда приложение завершает работу с блоком данных, отправленным драйвером устройства, можно очистить и освободить блок данных.</span><span class="sxs-lookup"><span data-stu-id="04501-126">When your application finishes using the data block sent by the device driver, you can clean up and free the data block.</span></span> <span data-ttu-id="04501-127">Если вам не нужно выделять память или инициализировать переменные, вам, скорее всего, не нужно использовать сообщения закрытия WIM [**\_ \_ Open**](mm-wim-open.md) и [**mm \_ WIM \_**](mm-wim-close.md) .</span><span class="sxs-lookup"><span data-stu-id="04501-127">Unless you need to allocate memory or initialize variables, you probably do not need to use the [**MM\_WIM\_OPEN**](mm-wim-open.md) and [**MM\_WIM\_CLOSE**](mm-wim-close.md) messages.</span></span>

<span data-ttu-id="04501-128">Функция обратного вызова для устройств ввода аудио-сигналов предоставляется приложением.</span><span class="sxs-lookup"><span data-stu-id="04501-128">The callback function for waveform-audio input devices is supplied by the application.</span></span> <span data-ttu-id="04501-129">Сведения об этой функции обратного вызова см. в описании функции [**вавеинпрок**](/previous-versions//dd743849(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="04501-129">For information about this callback function, see the [**waveInProc**](/previous-versions//dd743849(v=vs.85)) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04501-130">См. также</span><span class="sxs-lookup"><span data-stu-id="04501-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04501-131">Запись звука звукозаписи</span><span class="sxs-lookup"><span data-stu-id="04501-131">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 