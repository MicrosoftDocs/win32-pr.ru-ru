---
title: Сообщение WM_CAP_SET_PREVIEW (VFW. h)
description: Сообщение " \_ Установка закрепления WM" \_ \_ включает или отключает режим предварительного просмотра.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- WM_CAP_SET_PREVIEW сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4a7e490809efa2e2d9f1ad27bca697c6333e682
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137522"
---
# <a name="wm_cap_set_preview-message"></a><span data-ttu-id="65ef3-104">\_Сообщение для \_ \_ предварительного просмотра набора закрепления WM</span><span class="sxs-lookup"><span data-stu-id="65ef3-104">WM\_CAP\_SET\_PREVIEW message</span></span>

<span data-ttu-id="65ef3-105">Сообщение **" \_ Установка закрепления \_ \_ WM** " включает или отключает режим предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="65ef3-105">The **WM\_CAP\_SET\_PREVIEW** message enables or disables preview mode.</span></span> <span data-ttu-id="65ef3-106">В режиме предварительного просмотра кадры передаются из оборудования захвата в системную память, а затем отображаются в окне записи с помощью функций GDI.</span><span class="sxs-lookup"><span data-stu-id="65ef3-106">In preview mode, frames are transferred from the capture hardware to system memory and then displayed in the capture window using GDI functions.</span></span> <span data-ttu-id="65ef3-107">Это сообщение можно отправить явно или с помощью макроса [**каппревиев**](/windows/desktop/api/Vfw/nf-vfw-cappreview) .</span><span class="sxs-lookup"><span data-stu-id="65ef3-107">You can send this message explicitly or by using the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro.</span></span>


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="65ef3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="65ef3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65ef3-109"><span id="f"></span><span id="F"></span>*ж*</span><span class="sxs-lookup"><span data-stu-id="65ef3-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="65ef3-110">Флаг предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="65ef3-110">Preview flag.</span></span> <span data-ttu-id="65ef3-111">Укажите **true** для этого параметра, чтобы включить режим предварительного просмотра, или **false** , чтобы отключить его.</span><span class="sxs-lookup"><span data-stu-id="65ef3-111">Specify **TRUE** for this parameter to enable preview mode or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65ef3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65ef3-112">Return Value</span></span>

<span data-ttu-id="65ef3-113">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="65ef3-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="65ef3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65ef3-114">Remarks</span></span>

<span data-ttu-id="65ef3-115">В режиме предварительного просмотра используются существенные ресурсы ЦП.</span><span class="sxs-lookup"><span data-stu-id="65ef3-115">The preview mode uses substantial CPU resources.</span></span> <span data-ttu-id="65ef3-116">Приложения могут отключить предварительный просмотр или уменьшить частоту предварительной версии, когда фокус находится на другом приложении.</span><span class="sxs-lookup"><span data-stu-id="65ef3-116">Applications can disable preview or lower the preview rate when another application has the focus.</span></span> <span data-ttu-id="65ef3-117">Элемент **фливевиндов** структуры [**капстатус**](/windows/win32/api/vfw/ns-vfw-capstatus) указывает, включен ли режим предварительного просмотра в данный момент.</span><span class="sxs-lookup"><span data-stu-id="65ef3-117">The **fLiveWindow** member of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure indicates if preview mode is currently enabled.</span></span>

<span data-ttu-id="65ef3-118">Включение режима предварительного просмотра автоматически отключает режим наложения.</span><span class="sxs-lookup"><span data-stu-id="65ef3-118">Enabling preview mode automatically disables overlay mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="65ef3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="65ef3-119">Requirements</span></span>



| <span data-ttu-id="65ef3-120">Требование</span><span class="sxs-lookup"><span data-stu-id="65ef3-120">Requirement</span></span> | <span data-ttu-id="65ef3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="65ef3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="65ef3-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65ef3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="65ef3-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="65ef3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="65ef3-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65ef3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="65ef3-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="65ef3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="65ef3-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="65ef3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="65ef3-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="65ef3-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ef3-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65ef3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ef3-129">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="65ef3-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="65ef3-130">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="65ef3-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





