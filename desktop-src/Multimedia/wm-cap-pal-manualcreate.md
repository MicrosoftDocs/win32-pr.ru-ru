---
title: Сообщение WM_CAP_PAL_MANUALCREATE (VFW. h)
description: Сообщение WM \_ Cap \_ PAL \_ мануалкреате запрашивает, что драйвер записи выводит образцы видеокадров вручную и создает новую палитру. Это сообщение можно отправить явно или с помощью макроса Каппалеттемануал.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- WM_CAP_PAL_MANUALCREATE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_PAL_MANUALCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dfd5b6588381ede0faaae539d3d8418b041f458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801870"
---
# <a name="wm_cap_pal_manualcreate-message"></a><span data-ttu-id="05d93-105">\_Сообщение о \_ мануалкреатее WM Cap PAL \_</span><span class="sxs-lookup"><span data-stu-id="05d93-105">WM\_CAP\_PAL\_MANUALCREATE message</span></span>

<span data-ttu-id="05d93-106">Сообщение **WM \_ Cap \_ PAL \_ мануалкреате** запрашивает, что драйвер записи выводит образцы видеокадров вручную и создает новую палитру.</span><span class="sxs-lookup"><span data-stu-id="05d93-106">The **WM\_CAP\_PAL\_MANUALCREATE** message requests that the capture driver manually sample video frames and create a new palette.</span></span> <span data-ttu-id="05d93-107">Это сообщение можно отправить явно или с помощью макроса [**каппалеттемануал**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) .</span><span class="sxs-lookup"><span data-stu-id="05d93-107">You can send this message explicitly or by using the [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) macro.</span></span>


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a><span data-ttu-id="05d93-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="05d93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05d93-109"><span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*фграб*</span><span class="sxs-lookup"><span data-stu-id="05d93-109"><span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*</span></span>
</dt> <dd>

<span data-ttu-id="05d93-110">Флаг гистограммы палитры.</span><span class="sxs-lookup"><span data-stu-id="05d93-110">Palette histogram flag.</span></span> <span data-ttu-id="05d93-111">Задайте для этого параметра **значение true** для каждого кадра, включенного при создании оптимальной палитры.</span><span class="sxs-lookup"><span data-stu-id="05d93-111">Set this parameter to **TRUE** for each frame included in creating the optimal palette.</span></span> <span data-ttu-id="05d93-112">После сбора последнего кадра присвойте этому параметру **значение false** , чтобы вычислить оптимальную палитру и отправить ее драйверу записи.</span><span class="sxs-lookup"><span data-stu-id="05d93-112">After the last frame has been collected, set this parameter to **FALSE** to calculate the optimal palette and send it to the capture driver.</span></span>

</dd> <dt>

<span data-ttu-id="05d93-113"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*иколорс*</span><span class="sxs-lookup"><span data-stu-id="05d93-113"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span></span>
</dt> <dd>

<span data-ttu-id="05d93-114">Число цветов в палитре.</span><span class="sxs-lookup"><span data-stu-id="05d93-114">Number of colors in the palette.</span></span> <span data-ttu-id="05d93-115">Максимальное значение этого параметра — 256.</span><span class="sxs-lookup"><span data-stu-id="05d93-115">The maximum value for this parameter is 256.</span></span> <span data-ttu-id="05d93-116">Это значение используется только во время сбора первого кадра в последовательности.</span><span class="sxs-lookup"><span data-stu-id="05d93-116">This value is used only during collection of the first frame in a sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05d93-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05d93-117">Return Value</span></span>

<span data-ttu-id="05d93-118">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="05d93-118">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="05d93-119">Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.</span><span class="sxs-lookup"><span data-stu-id="05d93-119">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="05d93-120">Требования</span><span class="sxs-lookup"><span data-stu-id="05d93-120">Requirements</span></span>



| <span data-ttu-id="05d93-121">Требование</span><span class="sxs-lookup"><span data-stu-id="05d93-121">Requirement</span></span> | <span data-ttu-id="05d93-122">Значение</span><span class="sxs-lookup"><span data-stu-id="05d93-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="05d93-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05d93-123">Minimum supported client</span></span><br/> | <span data-ttu-id="05d93-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="05d93-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="05d93-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05d93-125">Minimum supported server</span></span><br/> | <span data-ttu-id="05d93-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="05d93-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="05d93-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="05d93-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="05d93-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="05d93-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05d93-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05d93-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d93-130">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="05d93-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="05d93-131">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="05d93-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





