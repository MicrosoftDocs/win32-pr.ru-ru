---
title: Сообщение WM_CAP_SET_CALLBACK_WAVESTREAM (VFW. h)
description: '\_ \_ \_ Сообщение вавестреам для обратного вызова Set крепления WM \_ устанавливает функцию обратного вызова в приложении.'
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- WM_CAP_SET_CALLBACK_WAVESTREAM сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_WAVESTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36abc7848de082e033cfc25d4f15d90c86cf3b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492948"
---
# <a name="wm_cap_set_callback_wavestream-message"></a><span data-ttu-id="b0b5b-104">\_Сообщение о \_ \_ вавестреам обратного вызова Set крепления WM \_</span><span class="sxs-lookup"><span data-stu-id="b0b5b-104">WM\_CAP\_SET\_CALLBACK\_WAVESTREAM message</span></span>

<span data-ttu-id="b0b5b-105">Сообщение **\_ вавестреам для \_ \_ обратного \_ вызова Set крепления WM** устанавливает функцию обратного вызова в приложении.</span><span class="sxs-lookup"><span data-stu-id="b0b5b-105">The **WM\_CAP\_SET\_CALLBACK\_WAVESTREAM** message sets a callback function in the application.</span></span> <span data-ttu-id="b0b5b-106">Авикап вызывает эту процедуру при захвате потоковой передачи, когда новый звуковой буфер станет доступным.</span><span class="sxs-lookup"><span data-stu-id="b0b5b-106">AVICap calls this procedure during streaming capture when a new audio buffer becomes available.</span></span> <span data-ttu-id="b0b5b-107">Это сообщение можно отправить явно или с помощью макроса [**капсеткаллбакконвавестреам**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) .</span><span class="sxs-lookup"><span data-stu-id="b0b5b-107">You can send this message explicitly or by using the [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="b0b5b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0b5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0b5b-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*фппрок*</span><span class="sxs-lookup"><span data-stu-id="b0b5b-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="b0b5b-110">Указатель на функцию обратного вызова потока Wave типа [**капвавестреамкаллбакк**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback).</span><span class="sxs-lookup"><span data-stu-id="b0b5b-110">Pointer to the wave stream callback function, of type [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback).</span></span> <span data-ttu-id="b0b5b-111">Укажите **значение NULL** для этого параметра, чтобы отключить ранее установленную функцию обратного вызова потока Wave.</span><span class="sxs-lookup"><span data-stu-id="b0b5b-111">Specify **NULL** for this parameter to disable a previously installed wave stream callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0b5b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0b5b-112">Return Value</span></span>

<span data-ttu-id="b0b5b-113">Возвращает **значение true** в случае успеха или **false** , если выполняется захват потоковой передачи или однокадровый сеанс записи.</span><span class="sxs-lookup"><span data-stu-id="b0b5b-113">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0b5b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0b5b-114">Remarks</span></span>

<span data-ttu-id="b0b5b-115">Окно записи вызывает процедуру перед записью звукового буфера на диск.</span><span class="sxs-lookup"><span data-stu-id="b0b5b-115">The capture window calls the procedure before writing the audio buffer to disk.</span></span> <span data-ttu-id="b0b5b-116">Это позволяет приложениям изменять аудио буфер при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b0b5b-116">This allows applications to modify the audio buffer if desired.</span></span>

<span data-ttu-id="b0b5b-117">Если используется функция обратного вызова волнового потока, ее необходимо установить перед запуском сеанса записи, и она должна оставаться включенной в течение сеанса.</span><span class="sxs-lookup"><span data-stu-id="b0b5b-117">If a wave stream callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="b0b5b-118">Его можно отключить после завершения потоковой записи.</span><span class="sxs-lookup"><span data-stu-id="b0b5b-118">It can be disabled after streaming capture ends.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b5b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b0b5b-119">Requirements</span></span>



| <span data-ttu-id="b0b5b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b0b5b-120">Requirement</span></span> | <span data-ttu-id="b0b5b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b0b5b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b0b5b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0b5b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b0b5b-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0b5b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b0b5b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0b5b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b0b5b-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0b5b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b0b5b-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b0b5b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0b5b-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0b5b-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0b5b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0b5b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b5b-129">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="b0b5b-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b0b5b-130">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="b0b5b-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





