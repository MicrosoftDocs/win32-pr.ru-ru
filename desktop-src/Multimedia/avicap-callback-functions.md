---
title: Функции обратного вызова Авикап
description: Функции обратного вызова Авикап
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- Класс Авикап, функции обратного вызова
- Функции обратного вызова Авикап, сведения
- Сообщение WM_CAP_SET_CALLBACK_CAPCONTROL
- Сообщение WM_CAP_SET_CALLBACK_ERROR
- Сообщение WM_CAP_SET_CALLBACK_FRAME
- Сообщение WM_CAP_SET_CALLBACK_STATUS
- Сообщение WM_CAP_SET_CALLBACK_VIDEOSTREAM
- Сообщение WM_CAP_SET_CALLBACK_WAVESTREAM
- Сообщение WM_CAP_SET_CALLBACK_YIELD
- макрос Капсеткаллбакконкапконтрол
- капсеткаллбакконеррормакро
- макрос Капсеткаллбакконфраме
- макрос Капсеткаллбакконстатус
- макрос Капсеткаллбакконвидеостреам
- макрос Капсеткаллбакконвавестреам
- макрос Капсеткаллбаккониелд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9edf96a6ff5b359acb6ef6d6a302b798742ffb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986809"
---
# <a name="avicap-callback-functions"></a><span data-ttu-id="07c53-119">Функции обратного вызова Авикап</span><span class="sxs-lookup"><span data-stu-id="07c53-119">AVICap Callback Functions</span></span>

<span data-ttu-id="07c53-120">Приложение может регистрировать функции обратного вызова с помощью окна записи, чтобы оно уведомило ваше приложение об изменении состояния, при возникновении ошибок, когда видеобуферы и звуковые буфера становятся доступными, а также для получения во время потоковой записи.</span><span class="sxs-lookup"><span data-stu-id="07c53-120">Your application can register callback functions with a capture window to have it notify your application when the status changes, when errors occur, when video frame and audio buffers become available, and to yield during streaming capture.</span></span> <span data-ttu-id="07c53-121">В следующих сообщениях задается функция обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="07c53-121">The following messages set the callback function.</span></span>



| <span data-ttu-id="07c53-122">Сообщение</span><span class="sxs-lookup"><span data-stu-id="07c53-122">Message</span></span>                                                                        | <span data-ttu-id="07c53-123">Описание</span><span class="sxs-lookup"><span data-stu-id="07c53-123">Description</span></span>                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07c53-124">**\_ \_ \_ капконтрол обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="07c53-124">**WM\_CAP\_SET\_CALLBACK\_CAPCONTROL**</span></span>](wm-cap-set-callback-capcontrol.md)   | <span data-ttu-id="07c53-125">Указывает функцию обратного вызова в приложении, вызываемую, чтобы обеспечить точный контроль над началом и завершением записи.</span><span class="sxs-lookup"><span data-stu-id="07c53-125">Specifies the callback function in the application called to give precise control over capture start and end.</span></span> <span data-ttu-id="07c53-126">Для отправки этого сообщения можно также использовать макрос [**капсеткаллбакконкапконтрол**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) .</span><span class="sxs-lookup"><span data-stu-id="07c53-126">You can also use the [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) macro to send this message.</span></span>                   |
| [<span data-ttu-id="07c53-127">**\_ \_ \_ ошибка обратного вызова установки крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="07c53-127">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)             | <span data-ttu-id="07c53-128">Указывает функцию обратного вызова в приложении, вызываемой при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="07c53-128">Specifies the callback function in the application called when an error occurs.</span></span> <span data-ttu-id="07c53-129">Для отправки этого сообщения можно также использовать макрос [**капсеткаллбакконеррор**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) .</span><span class="sxs-lookup"><span data-stu-id="07c53-129">You can also use the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro to send this message.</span></span>                                                           |
| [<span data-ttu-id="07c53-130">**\_ \_ \_ кадр обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="07c53-130">**WM\_CAP\_SET\_CALLBACK\_FRAME**</span></span>](wm-cap-set-callback-frame.md)             | <span data-ttu-id="07c53-131">Указывает функцию обратного вызова в приложении, вызываемом при записи кадров предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="07c53-131">Specifies the callback function in the application called when preview frames are captured.</span></span> <span data-ttu-id="07c53-132">Для отправки этого сообщения можно также использовать макрос [**капсеткаллбакконфраме**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) .</span><span class="sxs-lookup"><span data-stu-id="07c53-132">You can also use the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro to send this message.</span></span>                                               |
| [<span data-ttu-id="07c53-133">**\_ \_ \_ состояние обратного вызова Set Cap WM \_**</span><span class="sxs-lookup"><span data-stu-id="07c53-133">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)           | <span data-ttu-id="07c53-134">Указывает функцию обратного вызова в приложении, вызываемом при изменении состояния.</span><span class="sxs-lookup"><span data-stu-id="07c53-134">Specifies the callback function in the application called when the status changes.</span></span> <span data-ttu-id="07c53-135">Для отправки этого сообщения можно также использовать макрос [**капсеткаллбакконстатус**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) .</span><span class="sxs-lookup"><span data-stu-id="07c53-135">You can also use the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro to send this message.</span></span>                                                      |
| [<span data-ttu-id="07c53-136">**\_ \_ \_ VIDEOSTREAM обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="07c53-136">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md) | <span data-ttu-id="07c53-137">Указывает функцию обратного вызова в приложении, вызываемом во время сбора потоковой передачи, когда новый буфер видео станет доступным.</span><span class="sxs-lookup"><span data-stu-id="07c53-137">Specifies the callback function in the application called during streaming capture when a new video buffer becomes available.</span></span> <span data-ttu-id="07c53-138">Для отправки этого сообщения можно также использовать макрос [**капсеткаллбакконвидеостреам**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) .</span><span class="sxs-lookup"><span data-stu-id="07c53-138">You can also use the [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) macro to send this message.</span></span> |
| [<span data-ttu-id="07c53-139">**\_ \_ \_ вавестреам обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="07c53-139">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)   | <span data-ttu-id="07c53-140">Указывает функцию обратного вызова в приложении, вызываемом во время сбора потоковой передачи, когда новый звуковой буфер станет доступным.</span><span class="sxs-lookup"><span data-stu-id="07c53-140">Specifies the callback function in the application called during streaming capture when a new audio buffer becomes available.</span></span> <span data-ttu-id="07c53-141">Для отправки этого сообщения можно также использовать макрос [**капсеткаллбакконвавестреам**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) .</span><span class="sxs-lookup"><span data-stu-id="07c53-141">You can also use the [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) macro to send this message.</span></span>   |
| [<span data-ttu-id="07c53-142">**\_ \_ \_ вызов функции обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="07c53-142">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)             | <span data-ttu-id="07c53-143">Указывает функцию обратного вызова в приложении, вызываемой при передаче потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="07c53-143">Specifies the callback function in the application called when yielding during streaming capture.</span></span> <span data-ttu-id="07c53-144">Для отправки этого сообщения можно также использовать макрос [**капсеткаллбаккониелд**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) .</span><span class="sxs-lookup"><span data-stu-id="07c53-144">You can also use the [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) macro to send this message.</span></span>                                         |



 

<span data-ttu-id="07c53-145">В следующих разделах описываются различные функции обратного вызова, уведомления, отправляемые в функции, и их использование.</span><span class="sxs-lookup"><span data-stu-id="07c53-145">The following topics describe the different callback functions, the notifications sent to the functions, and their uses.</span></span>

 

 




