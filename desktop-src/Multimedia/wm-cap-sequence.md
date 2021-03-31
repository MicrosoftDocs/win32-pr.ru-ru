---
title: Сообщение WM_CAP_SEQUENCE (VFW. h)
description: '\_Последовательное сообщение с ограничением WM \_ инициирует потоковую передачу видео и звука в файл. Это сообщение можно отправить явно или с помощью макроса Капкаптуресекуенце.'
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- WM_CAP_SEQUENCE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ef945510d0d71f1aa0e0cb5827288a613f5991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988798"
---
# <a name="wm_cap_sequence-message"></a><span data-ttu-id="b4410-105">\_Сообщение о \_ последовательности крепления WM</span><span class="sxs-lookup"><span data-stu-id="b4410-105">WM\_CAP\_SEQUENCE message</span></span>

<span data-ttu-id="b4410-106">Последовательное сообщение с **\_ \_ ограничением WM** инициирует потоковую передачу видео и звука в файл.</span><span class="sxs-lookup"><span data-stu-id="b4410-106">The **WM\_CAP\_SEQUENCE** message initiates streaming video and audio capture to a file.</span></span> <span data-ttu-id="b4410-107">Это сообщение можно отправить явно или с помощью макроса [**капкаптуресекуенце**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) .</span><span class="sxs-lookup"><span data-stu-id="b4410-107">You can send this message explicitly or by using the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro.</span></span>


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="b4410-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4410-108">Return Value</span></span>

<span data-ttu-id="b4410-109">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b4410-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="b4410-110">Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.</span><span class="sxs-lookup"><span data-stu-id="b4410-110">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4410-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4410-111">Remarks</span></span>

<span data-ttu-id="b4410-112">Если вы хотите изменить параметры, управляющие захватом потоковой передачи, используйте сообщение [**\_ установки закрепления WM \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) перед началом записи.</span><span class="sxs-lookup"><span data-stu-id="b4410-112">If you want to alter the parameters controlling streaming capture, use the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message prior to starting the capture.</span></span>

<span data-ttu-id="b4410-113">По умолчанию окно Capture (захват) не позволяет другим приложениям продолжать выполнение во время записи.</span><span class="sxs-lookup"><span data-stu-id="b4410-113">By default, the capture window does not allow other applications to continue running during capture.</span></span> <span data-ttu-id="b4410-114">Чтобы переопределить это, либо установите для элемента **Фиелд** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) **значение true**, либо установите функцию обратного вызова yield.</span><span class="sxs-lookup"><span data-stu-id="b4410-114">To override this, either set the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to **TRUE**, or install a yield callback function.</span></span>

<span data-ttu-id="b4410-115">При захвате потоковой передачи окно отслеживания может при необходимости выдавать уведомления для приложения конкретных типов условий.</span><span class="sxs-lookup"><span data-stu-id="b4410-115">During streaming capture, the capture window can optionally issue notifications to your application of specific types of conditions.</span></span> <span data-ttu-id="b4410-116">Чтобы установить процедуры обратного вызова для этих уведомлений, используйте следующие сообщения:</span><span class="sxs-lookup"><span data-stu-id="b4410-116">To install callback procedures for these notifications, use the following messages:</span></span>

-   [<span data-ttu-id="b4410-117">**\_ \_ \_ ошибка обратного вызова установки крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="b4410-117">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="b4410-118">**\_ \_ \_ состояние обратного вызова Set Cap WM \_**</span><span class="sxs-lookup"><span data-stu-id="b4410-118">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="b4410-119">**\_ \_ \_ вызов функции обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="b4410-119">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="b4410-120">**\_ \_ \_ VIDEOSTREAM обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="b4410-120">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="b4410-121">**\_ \_ \_ вавестреам обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="b4410-121">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)

## <a name="requirements"></a><span data-ttu-id="b4410-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b4410-122">Requirements</span></span>



| <span data-ttu-id="b4410-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b4410-123">Requirement</span></span> | <span data-ttu-id="b4410-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b4410-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b4410-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4410-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b4410-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b4410-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b4410-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4410-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b4410-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b4410-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b4410-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b4410-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4410-130"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4410-130"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4410-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4410-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4410-132">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="b4410-132">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b4410-133">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="b4410-133">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





