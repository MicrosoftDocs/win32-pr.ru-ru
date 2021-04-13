---
title: Сообщение ICM_DRAW_STOP (VFW. h)
description: Сообщение об ошибке ICM \_ Draw \_ уведомляет драйвер подготовки к прекращению его внутренних часов на время рисования кадров. Это сообщение можно отправить явно или с помощью макроса Икдравстоп.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- ICM_DRAW_STOP сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3bde99dfcf483e67aa6a601de2718814cc22439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490137"
---
# <a name="icm_draw_stop-message"></a><span data-ttu-id="01b1f-105">\_ \_ Сообщение об ошибке ПРОРИСОВКи ICM</span><span class="sxs-lookup"><span data-stu-id="01b1f-105">ICM\_DRAW\_STOP message</span></span>

<span data-ttu-id="01b1f-106">Сообщение об ошибке **ICM \_ Draw \_** уведомляет драйвер подготовки к прекращению его внутренних часов на время рисования кадров.</span><span class="sxs-lookup"><span data-stu-id="01b1f-106">The **ICM\_DRAW\_STOP** message notifies a rendering driver to stop its internal clock for the timing of drawing frames.</span></span> <span data-ttu-id="01b1f-107">Это сообщение можно отправить явно или с помощью макроса [**икдравстоп**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) .</span><span class="sxs-lookup"><span data-stu-id="01b1f-107">You can send this message explicitly or by using the [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) macro.</span></span>


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="01b1f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01b1f-108">Return Value</span></span>

<span data-ttu-id="01b1f-109">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="01b1f-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01b1f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01b1f-110">Remarks</span></span>

<span data-ttu-id="01b1f-111">Это сообщение используется оборудованием, которое выполняет собственное асинхронное распаковка, время и рисование.</span><span class="sxs-lookup"><span data-stu-id="01b1f-111">This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="01b1f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="01b1f-112">Requirements</span></span>



| <span data-ttu-id="01b1f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="01b1f-113">Requirement</span></span> | <span data-ttu-id="01b1f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="01b1f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="01b1f-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01b1f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="01b1f-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="01b1f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="01b1f-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01b1f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="01b1f-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="01b1f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="01b1f-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="01b1f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="01b1f-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="01b1f-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01b1f-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01b1f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b1f-122">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="01b1f-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="01b1f-123">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="01b1f-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





