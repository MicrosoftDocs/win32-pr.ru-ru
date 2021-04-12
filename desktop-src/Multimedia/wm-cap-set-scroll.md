---
title: Сообщение WM_CAP_SET_SCROLL (VFW. h)
description: '\_Сообщение SCROLL Set с закреплением WM \_ \_ определяет часть видеокадра, отображаемую в окне Capture (захват).'
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- WM_CAP_SET_SCROLL сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812b76bdcad166b9f766957032f232293d4083c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492945"
---
# <a name="wm_cap_set_scroll-message"></a><span data-ttu-id="4ea6b-104">\_ \_ \_ Сообщение прокрутки установки крепления WM</span><span class="sxs-lookup"><span data-stu-id="4ea6b-104">WM\_CAP\_SET\_SCROLL message</span></span>

<span data-ttu-id="4ea6b-105">Сообщение **\_ \_ \_ SCROLL Set с закреплением WM** определяет часть видеокадра, отображаемую в окне Capture (захват).</span><span class="sxs-lookup"><span data-stu-id="4ea6b-105">The **WM\_CAP\_SET\_SCROLL** message defines the portion of the video frame to display in the capture window.</span></span> <span data-ttu-id="4ea6b-106">Это сообщение задает для левого верхнего угла клиентской области окна захвата координаты указанного пикселя в кадре видео.</span><span class="sxs-lookup"><span data-stu-id="4ea6b-106">This message sets the upper left corner of the client area of the capture window to the coordinates of a specified pixel within the video frame.</span></span> <span data-ttu-id="4ea6b-107">Это сообщение можно отправить явно или с помощью макроса [**капсетскроллпос**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="4ea6b-107">You can send this message explicitly or by using the [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) macro.</span></span>


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a><span data-ttu-id="4ea6b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ea6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ea6b-109"><span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*лпп*</span><span class="sxs-lookup"><span data-stu-id="4ea6b-109"><span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*</span></span>
</dt> <dd>

<span data-ttu-id="4ea6b-110">Адрес, содержащий нужную точку прокрутки.</span><span class="sxs-lookup"><span data-stu-id="4ea6b-110">Address to contain the desired scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ea6b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ea6b-111">Return Value</span></span>

<span data-ttu-id="4ea6b-112">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4ea6b-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ea6b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ea6b-113">Remarks</span></span>

<span data-ttu-id="4ea6b-114">Расположение прокрутки влияет на изображение в режимах предварительного просмотра и наложения.</span><span class="sxs-lookup"><span data-stu-id="4ea6b-114">The scroll position affects the image in both preview and overlay modes.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ea6b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4ea6b-115">Requirements</span></span>



| <span data-ttu-id="4ea6b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4ea6b-116">Requirement</span></span> | <span data-ttu-id="4ea6b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4ea6b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4ea6b-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ea6b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4ea6b-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4ea6b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4ea6b-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ea6b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4ea6b-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4ea6b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4ea6b-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4ea6b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ea6b-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ea6b-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ea6b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ea6b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ea6b-125">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="4ea6b-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="4ea6b-126">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="4ea6b-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





