---
title: Сообщение WM_CAP_ABORT (VFW. h)
description: '\_ \_ Сообщение об отмене крепления WM останавливает операцию записи.'
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- WM_CAP_ABORT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2843e3c4d59b62f2b58be20cef63ed0dc2e79d4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534109"
---
# <a name="wm_cap_abort-message"></a><span data-ttu-id="6cc0d-104">\_ \_ Сообщение об отмене крепления WM</span><span class="sxs-lookup"><span data-stu-id="6cc0d-104">WM\_CAP\_ABORT message</span></span>

<span data-ttu-id="6cc0d-105">Сообщение **об \_ \_ отмене крепления WM** останавливает операцию записи.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-105">The **WM\_CAP\_ABORT** message stops the capture operation.</span></span> <span data-ttu-id="6cc0d-106">В случае записи шага данные изображения, собранные до точки **\_ \_ прерывания крепления WM** , будут сохранены в файле записи, но звук не будет записан.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-106">In the case of step capture, the image data collected up to the point of the **WM\_CAP\_ABORT** message will be retained in the capture file, but audio will not be captured.</span></span> <span data-ttu-id="6cc0d-107">Это сообщение можно отправить явно или с помощью макроса [**капкаптуреаборт**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) .</span><span class="sxs-lookup"><span data-stu-id="6cc0d-107">You can send this message explicitly or by using the [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) macro.</span></span>


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="6cc0d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6cc0d-108">Return Value</span></span>

<span data-ttu-id="6cc0d-109">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cc0d-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6cc0d-110">Remarks</span></span>

<span data-ttu-id="6cc0d-111">Операция отслеживания должна использовать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-111">The capture operation must yield to use this message.</span></span>

<span data-ttu-id="6cc0d-112">Используйте сообщение [**об \_ \_ остановке WM Cap**](wm-cap-stop.md) , чтобы остановить запись шагов в текущей позиции, а затем записать звук.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-112">Use the [**WM\_CAP\_STOP**](wm-cap-stop.md) message to halt step capture at the current position, and then capture audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cc0d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6cc0d-113">Requirements</span></span>



| <span data-ttu-id="6cc0d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6cc0d-114">Requirement</span></span> | <span data-ttu-id="6cc0d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6cc0d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6cc0d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cc0d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6cc0d-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6cc0d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6cc0d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cc0d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6cc0d-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6cc0d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6cc0d-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6cc0d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cc0d-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cc0d-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cc0d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cc0d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc0d-123">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="6cc0d-123">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="6cc0d-124">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="6cc0d-124">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





