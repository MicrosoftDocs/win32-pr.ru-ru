---
title: Сообщение MCIWNDM_REALIZE (VFW. h)
description: Сообщение о \_ реализации мЦивндм понимает палитру, которая в настоящее время используется устройством MCI в окне мЦивнд. Этот макрос определяется с помощью сообщения о \_ реализации мЦивндм. Это сообщение можно отправить явно или с помощью макроса МЦивндреализе.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- MCIWNDM_REALIZE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef3a803791a4f8dfe94d128d42ea06a7b28e739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988260"
---
# <a name="mciwndm_realize-message"></a><span data-ttu-id="ad57e-106">\_Сообщение о реализации мЦивндм</span><span class="sxs-lookup"><span data-stu-id="ad57e-106">MCIWNDM\_REALIZE message</span></span>

<span data-ttu-id="ad57e-107">Сообщение **о \_ реализации мЦивндм** понимает палитру, которая в настоящее время используется устройством MCI в окне мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="ad57e-107">The **MCIWNDM\_REALIZE** message realizes the palette currently used by the MCI device in an MCIWnd window.</span></span> <span data-ttu-id="ad57e-108">Этот макрос определяется с помощью сообщения **о \_ реализации мЦивндм** .</span><span class="sxs-lookup"><span data-stu-id="ad57e-108">This macro is defined with the **MCIWNDM\_REALIZE** message.</span></span> <span data-ttu-id="ad57e-109">Это сообщение можно отправить явно или с помощью макроса [**мЦивндреализе**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .</span><span class="sxs-lookup"><span data-stu-id="ad57e-109">You can send this message explicitly or by using the [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) macro.</span></span>


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="ad57e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad57e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad57e-111"><span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*фбкгнд*</span><span class="sxs-lookup"><span data-stu-id="ad57e-111"><span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*</span></span>
</dt> <dd>

<span data-ttu-id="ad57e-112">Флаг фона.</span><span class="sxs-lookup"><span data-stu-id="ad57e-112">Background flag.</span></span> <span data-ttu-id="ad57e-113">Укажите **значение true** для этого параметра, если окно является фоновым приложением.</span><span class="sxs-lookup"><span data-stu-id="ad57e-113">Specify **TRUE** for this parameter if the window is a background application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad57e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad57e-114">Return Value</span></span>

<span data-ttu-id="ad57e-115">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ad57e-115">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad57e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad57e-116">Remarks</span></span>

<span data-ttu-id="ad57e-117">**МЦивндм \_** В процессе реализации используется палитра устройства MCI и вызывается функция [**реализепалетте**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) .</span><span class="sxs-lookup"><span data-stu-id="ad57e-117">**MCIWNDM\_REALIZE** uses the palette of the MCI device and calls the [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) function.</span></span> <span data-ttu-id="ad57e-118">Если приложение явным образом обрабатывает сообщения [**WM \_ Палеттечанжед**](/windows/desktop/gdi/wm-palettechanged) и [**WM \_ куериневпалетте**](/windows/desktop/gdi/wm-querynewpalette) , следует использовать это сообщение в приложении вместо использования **реализепалетте**.</span><span class="sxs-lookup"><span data-stu-id="ad57e-118">If your application explicitly handles the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) messages, you should use this message in your application instead of using **RealizePalette**.</span></span> <span data-ttu-id="ad57e-119">Если тело одного из этих обработчиков сообщений содержит только **реализепалетте**, перешлите сообщение в окно мЦивнд, которое будет автоматически реализовывать палитру.</span><span class="sxs-lookup"><span data-stu-id="ad57e-119">If the body of one of these message handlers contains only **RealizePalette**, forward the message to the MCIWnd window, which will automatically realize the palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad57e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ad57e-120">Requirements</span></span>



| <span data-ttu-id="ad57e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ad57e-121">Requirement</span></span> | <span data-ttu-id="ad57e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ad57e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ad57e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad57e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ad57e-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ad57e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ad57e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad57e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ad57e-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ad57e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ad57e-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ad57e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad57e-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad57e-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad57e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad57e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad57e-130">**мЦивндреализе**</span><span class="sxs-lookup"><span data-stu-id="ad57e-130">**MCIWndRealize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[<span data-ttu-id="ad57e-131">**реализепалетте**</span><span class="sxs-lookup"><span data-stu-id="ad57e-131">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="ad57e-132">**WM \_ палеттечанжед**</span><span class="sxs-lookup"><span data-stu-id="ad57e-132">**WM\_PALETTECHANGED**</span></span>](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[<span data-ttu-id="ad57e-133">**WM \_ куериневпалетте**</span><span class="sxs-lookup"><span data-stu-id="ad57e-133">**WM\_QUERYNEWPALETTE**</span></span>](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

