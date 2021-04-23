---
title: Сообщение WM_CAP_SET_CALLBACK_STATUS (VFW. h)
description: '\_ \_ \_ Сообщение о состоянии обратного вызова для установки крепления WM \_ устанавливает функцию обратного вызова состояния в приложении. Авикап вызывает эту процедуру при каждом изменении состояния окна записи. Это сообщение можно отправить явно или с помощью макроса Капсеткаллбакконстатус.'
ms.assetid: 451ba9f9-7bfb-4c57-af6c-d5f691f39618
keywords:
- WM_CAP_SET_CALLBACK_STATUS сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493893a51d51b1ce61d43ff54461bb71c08a9f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489384"
---
# <a name="wm_cap_set_callback_status-message"></a><span data-ttu-id="fa721-106">\_ \_ \_ Сообщение о состоянии обратного вызова для установки крепления WM \_</span><span class="sxs-lookup"><span data-stu-id="fa721-106">WM\_CAP\_SET\_CALLBACK\_STATUS message</span></span>

<span data-ttu-id="fa721-107">Сообщение **\_ \_ \_ \_ о состоянии обратного вызова для установки крепления WM** устанавливает функцию обратного вызова состояния в приложении.</span><span class="sxs-lookup"><span data-stu-id="fa721-107">The **WM\_CAP\_SET\_CALLBACK\_STATUS** message sets a status callback function in the application.</span></span> <span data-ttu-id="fa721-108">Авикап вызывает эту процедуру при каждом изменении состояния окна записи.</span><span class="sxs-lookup"><span data-stu-id="fa721-108">AVICap calls this procedure whenever the capture window status changes.</span></span> <span data-ttu-id="fa721-109">Это сообщение можно отправить явно или с помощью макроса [**капсеткаллбакконстатус**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) .</span><span class="sxs-lookup"><span data-stu-id="fa721-109">You can send this message explicitly or by using the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_STATUS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="fa721-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa721-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa721-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*фппрок*</span><span class="sxs-lookup"><span data-stu-id="fa721-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="fa721-112">Указатель на функцию обратного вызова состояния типа [**капстатускаллбакк**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka).</span><span class="sxs-lookup"><span data-stu-id="fa721-112">Pointer to the status callback function, of type [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka).</span></span> <span data-ttu-id="fa721-113">Укажите **значение NULL** для этого параметра, чтобы отключить ранее установленную функцию обратного вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="fa721-113">Specify **NULL** for this parameter to disable a previously installed status callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa721-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa721-114">Return Value</span></span>

<span data-ttu-id="fa721-115">Возвращает **значение true** в случае успеха или **false** , если выполняется захват потоковой передачи или однокадровый сеанс записи.</span><span class="sxs-lookup"><span data-stu-id="fa721-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa721-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa721-116">Remarks</span></span>

<span data-ttu-id="fa721-117">При необходимости в приложениях можно задать функцию обратного вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="fa721-117">Applications can optionally set a status callback function.</span></span> <span data-ttu-id="fa721-118">Если задано, Авикап вызывает эту процедуру в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="fa721-118">If set, AVICap calls this procedure in the following situations:</span></span>

-   <span data-ttu-id="fa721-119">Сеанс отслеживания завершен.</span><span class="sxs-lookup"><span data-stu-id="fa721-119">A capture session is completed.</span></span>
-   <span data-ttu-id="fa721-120">Драйвер записи успешно подключен к окну записи.</span><span class="sxs-lookup"><span data-stu-id="fa721-120">A capture driver successfully connected to a capture window.</span></span>
-   <span data-ttu-id="fa721-121">Создается оптимальная палитра.</span><span class="sxs-lookup"><span data-stu-id="fa721-121">An optimal palette is created.</span></span>
-   <span data-ttu-id="fa721-122">Отображается число захваченных кадров.</span><span class="sxs-lookup"><span data-stu-id="fa721-122">The number of captured frames is reported.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa721-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fa721-123">Requirements</span></span>



| <span data-ttu-id="fa721-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fa721-124">Requirement</span></span> | <span data-ttu-id="fa721-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fa721-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fa721-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa721-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fa721-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fa721-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fa721-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa721-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fa721-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fa721-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fa721-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fa721-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa721-131"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa721-131"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa721-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa721-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa721-133">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="fa721-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="fa721-134">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="fa721-134">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





