---
title: Сообщение WM_CAP_STOP (VFW. h)
description: Сообщение о \_ \_ прекращении крепления WM останавливает операцию записи. Это сообщение можно отправить явно или с помощью макроса Капкаптурестоп.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- WM_CAP_STOP сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ded89ea8999fa2b29f576a6d047f5147d492bc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803803"
---
# <a name="wm_cap_stop-message"></a><span data-ttu-id="15df0-105">\_ \_ Сообщение об ошибке крепления WM</span><span class="sxs-lookup"><span data-stu-id="15df0-105">WM\_CAP\_STOP message</span></span>

<span data-ttu-id="15df0-106">Сообщение **о \_ \_ прекращении крепления WM** останавливает операцию записи.</span><span class="sxs-lookup"><span data-stu-id="15df0-106">The **WM\_CAP\_STOP** message stops the capture operation.</span></span> <span data-ttu-id="15df0-107">Это сообщение можно отправить явно или с помощью макроса [**капкаптурестоп**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) .</span><span class="sxs-lookup"><span data-stu-id="15df0-107">You can send this message explicitly or by using the [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) macro.</span></span>

<span data-ttu-id="15df0-108">На этапе записи кадров данных изображение, собранное до отправки этого сообщения, сохраняется в файле записи.</span><span class="sxs-lookup"><span data-stu-id="15df0-108">In step frame capture, the image data that was collected before this message was sent is retained in the capture file.</span></span> <span data-ttu-id="15df0-109">Аналогичная длительность звуковых данных также сохраняется в файле записи, если запись звука включена.</span><span class="sxs-lookup"><span data-stu-id="15df0-109">An equivalent duration of audio data is also retained in the capture file if audio capture was enabled.</span></span>


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="15df0-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15df0-110">Return Value</span></span>

<span data-ttu-id="15df0-111">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="15df0-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="15df0-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15df0-112">Remarks</span></span>

<span data-ttu-id="15df0-113">Операция отслеживания должна использовать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="15df0-113">The capture operation must yield to use this message.</span></span> <span data-ttu-id="15df0-114">Используйте сообщение [**об \_ \_ отмене крепления WM**](wm-cap-abort.md) , чтобы отказаться от текущей операции записи.</span><span class="sxs-lookup"><span data-stu-id="15df0-114">Use the [**WM\_CAP\_ABORT**](wm-cap-abort.md) message to abandon the current capture operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="15df0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="15df0-115">Requirements</span></span>



| <span data-ttu-id="15df0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="15df0-116">Requirement</span></span> | <span data-ttu-id="15df0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="15df0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15df0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15df0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="15df0-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15df0-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="15df0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15df0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="15df0-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15df0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="15df0-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="15df0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="15df0-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="15df0-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15df0-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15df0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15df0-125">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="15df0-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="15df0-126">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="15df0-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





