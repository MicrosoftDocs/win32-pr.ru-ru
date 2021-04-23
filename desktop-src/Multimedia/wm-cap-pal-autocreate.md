---
title: Сообщение WM_CAP_PAL_AUTOCREATE (VFW. h)
description: Сообщение с \_ \_ \_ автоматическим созданием WM Cap PAL запрашивает в качестве примера видеодрайвера записи образец видеокадра и автоматическое создание новой палитры. Это сообщение можно отправить явно или с помощью макроса Каппалеттеауто.
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- WM_CAP_PAL_AUTOCREATE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba70de46167121aa9a83959c6d9e202039f65cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661863"
---
# <a name="wm_cap_pal_autocreate-message"></a><span data-ttu-id="38045-105">\_Сообщение с \_ \_ автосозданием WM Cap PAL</span><span class="sxs-lookup"><span data-stu-id="38045-105">WM\_CAP\_PAL\_AUTOCREATE message</span></span>

<span data-ttu-id="38045-106">Сообщение с автоматическим **\_ \_ \_ созданием WM Cap PAL** запрашивает в качестве примера видеодрайвера записи образец видеокадра и автоматическое создание новой палитры.</span><span class="sxs-lookup"><span data-stu-id="38045-106">The **WM\_CAP\_PAL\_AUTOCREATE** message requests that the capture driver sample video frames and automatically create a new palette.</span></span> <span data-ttu-id="38045-107">Это сообщение можно отправить явно или с помощью макроса [**каппалеттеауто**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) .</span><span class="sxs-lookup"><span data-stu-id="38045-107">You can send this message explicitly or by using the [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) macro.</span></span>


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a><span data-ttu-id="38045-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="38045-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38045-109"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*IFRAME*</span><span class="sxs-lookup"><span data-stu-id="38045-109"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span></span>
</dt> <dd>

<span data-ttu-id="38045-110">Число кадров для выборки.</span><span class="sxs-lookup"><span data-stu-id="38045-110">Number of frames to sample.</span></span>

</dd> <dt>

<span data-ttu-id="38045-111"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*иколорс*</span><span class="sxs-lookup"><span data-stu-id="38045-111"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span></span>
</dt> <dd>

<span data-ttu-id="38045-112">Число цветов в палитре.</span><span class="sxs-lookup"><span data-stu-id="38045-112">Number of colors in the palette.</span></span> <span data-ttu-id="38045-113">Максимальное значение этого параметра — 256.</span><span class="sxs-lookup"><span data-stu-id="38045-113">The maximum value for this parameter is 256.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38045-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38045-114">Return Value</span></span>

<span data-ttu-id="38045-115">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="38045-115">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="38045-116">Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.</span><span class="sxs-lookup"><span data-stu-id="38045-116">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="38045-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38045-117">Remarks</span></span>

<span data-ttu-id="38045-118">Последовательность видеороликов с выборкой должна включать все нужные цвета в палитре.</span><span class="sxs-lookup"><span data-stu-id="38045-118">The sampled video sequence should include all the colors you want in the palette.</span></span> <span data-ttu-id="38045-119">Для получения оптимальной палитры может потребоваться выборка всей последовательности, а не ее части.</span><span class="sxs-lookup"><span data-stu-id="38045-119">To obtain the best palette, you might have to sample the whole sequence rather than a portion of it.</span></span>

## <a name="requirements"></a><span data-ttu-id="38045-120">Требования</span><span class="sxs-lookup"><span data-stu-id="38045-120">Requirements</span></span>



| <span data-ttu-id="38045-121">Требование</span><span class="sxs-lookup"><span data-stu-id="38045-121">Requirement</span></span> | <span data-ttu-id="38045-122">Значение</span><span class="sxs-lookup"><span data-stu-id="38045-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="38045-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38045-123">Minimum supported client</span></span><br/> | <span data-ttu-id="38045-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="38045-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="38045-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38045-125">Minimum supported server</span></span><br/> | <span data-ttu-id="38045-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="38045-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="38045-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="38045-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="38045-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="38045-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38045-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38045-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38045-130">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="38045-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="38045-131">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="38045-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





