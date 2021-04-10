---
title: Сообщение WM_CAP_SEQUENCE_NOFILE (VFW. h)
description: Сообщение о том, что \_ \_ файл с последовательностью закрепления WM \_ инициирует потоковую передачу видео без записи данных в файл. Это сообщение можно отправить явно или с помощью макроса Капкаптуресекуенценофиле.
ms.assetid: 60cbcb62-3bfa-4182-a049-1e3cb2ede423
keywords:
- WM_CAP_SEQUENCE_NOFILE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE_NOFILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a08f470989b8000e9757c1cb81924b875b5303
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135262"
---
# <a name="wm_cap_sequence_nofile-message"></a><span data-ttu-id="d8351-105">Сообщение о том, что \_ файл имеет последовательность закрепления WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="d8351-105">WM\_CAP\_SEQUENCE\_NOFILE message</span></span>

<span data-ttu-id="d8351-106">Сообщение о том, что **\_ \_ \_ файл с последовательностью закрепления WM** инициирует потоковую передачу видео без записи данных в файл.</span><span class="sxs-lookup"><span data-stu-id="d8351-106">The **WM\_CAP\_SEQUENCE\_NOFILE** message initiates streaming video capture without writing data to a file.</span></span> <span data-ttu-id="d8351-107">Это сообщение можно отправить явно или с помощью макроса [**капкаптуресекуенценофиле**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) .</span><span class="sxs-lookup"><span data-stu-id="d8351-107">You can send this message explicitly or by using the [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) macro.</span></span>


```C++
WM_CAP_SEQUENCE_NOFILE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="d8351-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8351-108">Return Value</span></span>

<span data-ttu-id="d8351-109">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d8351-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8351-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8351-110">Remarks</span></span>

<span data-ttu-id="d8351-111">Это сообщение можно использовать в сочетании с потоком видео или с функциями обратного вызова потоковой передачи аудио, которые позволяют вашему приложению напрямую применять видео и аудио данные.</span><span class="sxs-lookup"><span data-stu-id="d8351-111">This message is useful in conjunction with video stream or waveform-audio stream callback functions that let your application use the video and audio data directly.</span></span>

<span data-ttu-id="d8351-112">Если вы хотите изменить параметры, управляющие захватом потоковой передачи, используйте сообщение [**\_ установки закрепления WM \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) перед началом записи.</span><span class="sxs-lookup"><span data-stu-id="d8351-112">If you want to alter the parameters controlling streaming capture, use the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message prior to starting the capture.</span></span>

<span data-ttu-id="d8351-113">По умолчанию окно Capture (захват) не позволяет другим приложениям продолжать выполнение во время записи.</span><span class="sxs-lookup"><span data-stu-id="d8351-113">By default, the capture window does not allow other applications to continue running during capture.</span></span> <span data-ttu-id="d8351-114">Чтобы переопределить это, либо установите для элемента **Фиелд** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) **значение true**, либо установите функцию обратного вызова yield.</span><span class="sxs-lookup"><span data-stu-id="d8351-114">To override this, either set the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to **TRUE**, or install a yield callback function.</span></span>

<span data-ttu-id="d8351-115">При захвате потоковой передачи окно отслеживания может при необходимости выдавать уведомления для приложения конкретных типов условий.</span><span class="sxs-lookup"><span data-stu-id="d8351-115">During streaming capture, the capture window can optionally issue notifications to your application of specific types of conditions.</span></span> <span data-ttu-id="d8351-116">Чтобы установить процедуры обратного вызова для этих уведомлений, используйте следующие сообщения:</span><span class="sxs-lookup"><span data-stu-id="d8351-116">To install callback procedures for these notifications, use the following messages:</span></span>

-   [<span data-ttu-id="d8351-117">**\_ \_ \_ ошибка обратного вызова установки крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="d8351-117">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="d8351-118">**\_ \_ \_ состояние обратного вызова Set Cap WM \_**</span><span class="sxs-lookup"><span data-stu-id="d8351-118">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="d8351-119">**\_ \_ \_ вызов функции обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="d8351-119">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="d8351-120">**\_ \_ \_ VIDEOSTREAM обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="d8351-120">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="d8351-121">**\_ \_ \_ вавестреам обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="d8351-121">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)

## <a name="requirements"></a><span data-ttu-id="d8351-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d8351-122">Requirements</span></span>



| <span data-ttu-id="d8351-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d8351-123">Requirement</span></span> | <span data-ttu-id="d8351-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d8351-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d8351-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8351-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d8351-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d8351-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d8351-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8351-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d8351-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d8351-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d8351-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d8351-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8351-130"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8351-130"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8351-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8351-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8351-132">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="d8351-132">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d8351-133">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="d8351-133">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





