---
title: Сообщение WM_CAP_SET_OVERLAY (VFW. h)
description: '\_ \_ \_ Сообщение наложения WM Cap Set включает или отключает режим наложения. В режиме наложения видео отображается с помощью наложения оборудования. Это сообщение можно отправить явно или с помощью макроса Каповерлай.'
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- WM_CAP_SET_OVERLAY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_OVERLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f197ae3a7df9ad1520b84cf27fd15a1c76524ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672869"
---
# <a name="wm_cap_set_overlay-message"></a><span data-ttu-id="b0fac-106">\_ \_ \_ Сообщение наложения WM Cap Set</span><span class="sxs-lookup"><span data-stu-id="b0fac-106">WM\_CAP\_SET\_OVERLAY message</span></span>

<span data-ttu-id="b0fac-107">Сообщение **\_ \_ \_ наложения WM Cap Set** включает или отключает режим наложения.</span><span class="sxs-lookup"><span data-stu-id="b0fac-107">The **WM\_CAP\_SET\_OVERLAY** message enables or disables overlay mode.</span></span> <span data-ttu-id="b0fac-108">В режиме наложения видео отображается с помощью наложения оборудования.</span><span class="sxs-lookup"><span data-stu-id="b0fac-108">In overlay mode, video is displayed using hardware overlay.</span></span> <span data-ttu-id="b0fac-109">Это сообщение можно отправить явно или с помощью макроса [**каповерлай**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) .</span><span class="sxs-lookup"><span data-stu-id="b0fac-109">You can send this message explicitly or by using the [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) macro.</span></span>


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="b0fac-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0fac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0fac-111"><span id="f"></span><span id="F"></span>*ж*</span><span class="sxs-lookup"><span data-stu-id="b0fac-111"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="b0fac-112">Флаг наложения.</span><span class="sxs-lookup"><span data-stu-id="b0fac-112">Overlay flag.</span></span> <span data-ttu-id="b0fac-113">Укажите **true** для этого параметра, чтобы включить режим наложения, или **false** , чтобы отключить его.</span><span class="sxs-lookup"><span data-stu-id="b0fac-113">Specify **TRUE** for this parameter to enable overlay mode or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0fac-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0fac-114">Return Value</span></span>

<span data-ttu-id="b0fac-115">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b0fac-115">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0fac-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0fac-116">Remarks</span></span>

<span data-ttu-id="b0fac-117">Использование оверлея не требует ресурсов ЦП.</span><span class="sxs-lookup"><span data-stu-id="b0fac-117">Using an overlay does not require CPU resources.</span></span>

<span data-ttu-id="b0fac-118">Элемент **фхасоверлай** структуры [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) указывает, поддерживает ли устройство наложение.</span><span class="sxs-lookup"><span data-stu-id="b0fac-118">The **fHasOverlay** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure indicates whether the device is capable of overlay.</span></span> <span data-ttu-id="b0fac-119">Элемент **фоверлайвиндов** структуры [**капстатус**](/windows/win32/api/vfw/ns-vfw-capstatus) указывает, включен ли режим оверлея в данный момент.</span><span class="sxs-lookup"><span data-stu-id="b0fac-119">The **fOverlayWindow** member of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure indicates whether overlay mode is currently enabled.</span></span>

<span data-ttu-id="b0fac-120">Включение режима наложения автоматически отключает режим предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="b0fac-120">Enabling overlay mode automatically disables preview mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0fac-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b0fac-121">Requirements</span></span>



| <span data-ttu-id="b0fac-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b0fac-122">Requirement</span></span> | <span data-ttu-id="b0fac-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b0fac-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b0fac-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0fac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b0fac-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0fac-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b0fac-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0fac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b0fac-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0fac-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b0fac-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b0fac-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0fac-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0fac-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0fac-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0fac-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0fac-131">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="b0fac-131">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b0fac-132">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="b0fac-132">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





