---
title: Сообщение WM_CAP_SET_CALLBACK_ERROR (VFW. h)
description: '\_ \_ \_ Сообщение об ошибке обратного вызова установки крепления WM \_ устанавливает функцию обратного вызова ошибки в клиентском приложении. Авикап вызывает эту процедуру при возникновении ошибок. Это сообщение можно отправить явно или с помощью макроса Капсеткаллбакконеррор.'
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- WM_CAP_SET_CALLBACK_ERROR сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f50d62112d71f78196a17b958dc7d3d10702e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491139"
---
# <a name="wm_cap_set_callback_error-message"></a><span data-ttu-id="39678-106">\_ \_ \_ Сообщение об ошибке обратного вызова установки крепления WM \_</span><span class="sxs-lookup"><span data-stu-id="39678-106">WM\_CAP\_SET\_CALLBACK\_ERROR message</span></span>

<span data-ttu-id="39678-107">Сообщение **\_ \_ \_ \_ об ошибке обратного вызова установки крепления WM** устанавливает функцию обратного вызова ошибки в клиентском приложении.</span><span class="sxs-lookup"><span data-stu-id="39678-107">The **WM\_CAP\_SET\_CALLBACK\_ERROR** message sets an error callback function in the client application.</span></span> <span data-ttu-id="39678-108">Авикап вызывает эту процедуру при возникновении ошибок.</span><span class="sxs-lookup"><span data-stu-id="39678-108">AVICap calls this procedure when errors occur.</span></span> <span data-ttu-id="39678-109">Это сообщение можно отправить явно или с помощью макроса [**капсеткаллбакконеррор**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) .</span><span class="sxs-lookup"><span data-stu-id="39678-109">You can send this message explicitly or by using the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="39678-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="39678-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39678-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*фппрок*</span><span class="sxs-lookup"><span data-stu-id="39678-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="39678-112">Указатель на функцию обратного вызова ошибки типа [**каперроркаллбакк**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka).</span><span class="sxs-lookup"><span data-stu-id="39678-112">Pointer to the error callback function, of type [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka).</span></span> <span data-ttu-id="39678-113">Укажите **значение NULL** для этого параметра, чтобы отключить ранее установленную функцию обратного вызова ошибок.</span><span class="sxs-lookup"><span data-stu-id="39678-113">Specify **NULL** for this parameter to disable a previously installed error callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39678-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39678-114">Return Value</span></span>

<span data-ttu-id="39678-115">Возвращает **значение true** в случае успеха или **false** , если выполняется захват потоковой передачи или однокадровый сеанс записи.</span><span class="sxs-lookup"><span data-stu-id="39678-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="39678-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39678-116">Remarks</span></span>

<span data-ttu-id="39678-117">При необходимости приложения могут установить функцию обратного вызова ошибки.</span><span class="sxs-lookup"><span data-stu-id="39678-117">Applications can optionally set an error callback function.</span></span> <span data-ttu-id="39678-118">Если задано, Авикап вызывает процедуру Error в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="39678-118">If set, AVICap calls the error procedure in the following situations:</span></span>

-   <span data-ttu-id="39678-119">Диск полон.</span><span class="sxs-lookup"><span data-stu-id="39678-119">The disk is full.</span></span>
-   <span data-ttu-id="39678-120">Не удается подключить окно записи с помощью драйвера записи.</span><span class="sxs-lookup"><span data-stu-id="39678-120">A capture window cannot be connected with a capture driver.</span></span>
-   <span data-ttu-id="39678-121">Не удается открыть устройство звуковой волны.</span><span class="sxs-lookup"><span data-stu-id="39678-121">A waveform-audio device cannot be opened.</span></span>
-   <span data-ttu-id="39678-122">Число кадров, отбрасываемых во время записи, превышает указанный процент.</span><span class="sxs-lookup"><span data-stu-id="39678-122">The number of frames dropped during capture exceeds the specified percentage.</span></span>
-   <span data-ttu-id="39678-123">Невозможно записать кадры из-за проблем с вертикальным прерыванием синхронизации.</span><span class="sxs-lookup"><span data-stu-id="39678-123">The frames cannot be captured due to vertical synchronization interrupt problems.</span></span>

## <a name="requirements"></a><span data-ttu-id="39678-124">Требования</span><span class="sxs-lookup"><span data-stu-id="39678-124">Requirements</span></span>



| <span data-ttu-id="39678-125">Требование</span><span class="sxs-lookup"><span data-stu-id="39678-125">Requirement</span></span> | <span data-ttu-id="39678-126">Значение</span><span class="sxs-lookup"><span data-stu-id="39678-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="39678-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39678-127">Minimum supported client</span></span><br/> | <span data-ttu-id="39678-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39678-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="39678-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39678-129">Minimum supported server</span></span><br/> | <span data-ttu-id="39678-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39678-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="39678-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="39678-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="39678-132"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="39678-132"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39678-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39678-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39678-134">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="39678-134">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="39678-135">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="39678-135">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





