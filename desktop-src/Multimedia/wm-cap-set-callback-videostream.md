---
title: Сообщение WM_CAP_SET_CALLBACK_VIDEOSTREAM (VFW. h)
description: '\_ \_ \_ Сообщение VIDEOSTREAM для обратного вызова Set крепления WM \_ устанавливает функцию обратного вызова в приложении.'
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde1d2b44ba3786f2d17934e6e92e0894d8d3bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414797"
---
# <a name="wm_cap_set_callback_videostream-message"></a><span data-ttu-id="6cb26-104">\_Сообщение о \_ \_ VIDEOSTREAM обратного вызова Set крепления WM \_</span><span class="sxs-lookup"><span data-stu-id="6cb26-104">WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM message</span></span>

<span data-ttu-id="6cb26-105">Сообщение **\_ VIDEOSTREAM для \_ \_ обратного \_ вызова Set крепления WM** устанавливает функцию обратного вызова в приложении.</span><span class="sxs-lookup"><span data-stu-id="6cb26-105">The **WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM** message sets a callback function in the application.</span></span> <span data-ttu-id="6cb26-106">Авикап вызывает эту процедуру при захвате потоковой передачи при заполнении буфера видео.</span><span class="sxs-lookup"><span data-stu-id="6cb26-106">AVICap calls this procedure during streaming capture when a video buffer is filled.</span></span> <span data-ttu-id="6cb26-107">Это сообщение можно отправить явно или с помощью макроса [**капсеткаллбакконвидеостреам**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) .</span><span class="sxs-lookup"><span data-stu-id="6cb26-107">You can send this message explicitly or by using the [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="6cb26-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cb26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cb26-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*фппрок*</span><span class="sxs-lookup"><span data-stu-id="6cb26-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="6cb26-110">Указатель на функцию обратного вызова видео-Stream типа [**капвидеостреамкаллбакк**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span><span class="sxs-lookup"><span data-stu-id="6cb26-110">Pointer to the video-stream callback function, of type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span></span> <span data-ttu-id="6cb26-111">Укажите **значение NULL** для этого параметра, чтобы отключить ранее установленную функцию обратного вызова видео-потока.</span><span class="sxs-lookup"><span data-stu-id="6cb26-111">Specify **NULL** for this parameter to disable a previously installed video-stream callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cb26-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6cb26-112">Return Value</span></span>

<span data-ttu-id="6cb26-113">Возвращает **значение true** в случае успеха или **false** , если выполняется захват потоковой передачи или однокадровый сеанс записи.</span><span class="sxs-lookup"><span data-stu-id="6cb26-113">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cb26-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6cb26-114">Remarks</span></span>

<span data-ttu-id="6cb26-115">Окно Capture вызывает функцию обратного вызова перед записью захваченного кадра на диск.</span><span class="sxs-lookup"><span data-stu-id="6cb26-115">The capture window calls the callback function before writing the captured frame to disk.</span></span> <span data-ttu-id="6cb26-116">Это позволяет приложениям изменять фрейм при необходимости.</span><span class="sxs-lookup"><span data-stu-id="6cb26-116">This allows applications to modify the frame if desired.</span></span>

<span data-ttu-id="6cb26-117">Если для потоковой передачи используется функция обратного вызова видеопотока, она должна быть установлена перед запуском сеанса записи и должна оставаться включенной в течение сеанса.</span><span class="sxs-lookup"><span data-stu-id="6cb26-117">If a video stream callback function is used for streaming capture, the procedure must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="6cb26-118">Его можно отключить после завершения потоковой записи.</span><span class="sxs-lookup"><span data-stu-id="6cb26-118">It can be disabled after streaming capture ends.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cb26-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6cb26-119">Requirements</span></span>



| <span data-ttu-id="6cb26-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6cb26-120">Requirement</span></span> | <span data-ttu-id="6cb26-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6cb26-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6cb26-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cb26-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6cb26-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6cb26-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6cb26-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cb26-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6cb26-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6cb26-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6cb26-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6cb26-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cb26-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cb26-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cb26-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cb26-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cb26-129">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="6cb26-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="6cb26-130">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="6cb26-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





