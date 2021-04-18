---
title: Сообщение ICM_DRAW_GETTIME (VFW. h)
description: Сообщение ICM \_ Draw \_ запрашивает драйвер подготовки отчетов, который управляет временем рисования кадров, чтобы вернуть текущее значение его внутреннего времени. Это сообщение можно отправить явно или с помощью макроса Икдравжеттиме.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- ICM_DRAW_GETTIME сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_GETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f756a76408d01cb72ee1762f14bb8a5eab19e475
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672706"
---
# <a name="icm_draw_gettime-message"></a><span data-ttu-id="aca6a-105">\_Сообщение о \_ выполнении ICM Draw</span><span class="sxs-lookup"><span data-stu-id="aca6a-105">ICM\_DRAW\_GETTIME message</span></span>

<span data-ttu-id="aca6a-106">Сообщение **ICM \_ Draw \_** запрашивает драйвер подготовки отчетов, который управляет временем рисования кадров, чтобы вернуть текущее значение его внутреннего времени.</span><span class="sxs-lookup"><span data-stu-id="aca6a-106">The **ICM\_DRAW\_GETTIME** message requests a rendering driver that controls the timing of drawing frames to return the current value of its internal clock.</span></span> <span data-ttu-id="aca6a-107">Это сообщение можно отправить явно или с помощью макроса [**икдравжеттиме**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) .</span><span class="sxs-lookup"><span data-stu-id="aca6a-107">You can send this message explicitly or by using the [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) macro.</span></span>


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="aca6a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aca6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aca6a-109"><span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*лплтиме*</span><span class="sxs-lookup"><span data-stu-id="aca6a-109"><span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*</span></span>
</dt> <dd>

<span data-ttu-id="aca6a-110">Адрес, который будет содержать текущее время.</span><span class="sxs-lookup"><span data-stu-id="aca6a-110">Address to contain the current time.</span></span> <span data-ttu-id="aca6a-111">Возвращаемое значение должно быть указано в примерах.</span><span class="sxs-lookup"><span data-stu-id="aca6a-111">The return value should be specified in samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aca6a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aca6a-112">Return Value</span></span>

<span data-ttu-id="aca6a-113">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="aca6a-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aca6a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aca6a-114">Remarks</span></span>

<span data-ttu-id="aca6a-115">Это сообщение обычно поддерживается оборудованием, которое выполняет собственное асинхронное распаковка, время и рисование.</span><span class="sxs-lookup"><span data-stu-id="aca6a-115">This message is generally supported by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span> <span data-ttu-id="aca6a-116">Сообщение также может быть отправлено, если оборудование используется в качестве хозяина синхронизации.</span><span class="sxs-lookup"><span data-stu-id="aca6a-116">The message can also be sent if the hardware is being used as the synchronization master.</span></span>

## <a name="requirements"></a><span data-ttu-id="aca6a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="aca6a-117">Requirements</span></span>



| <span data-ttu-id="aca6a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="aca6a-118">Requirement</span></span> | <span data-ttu-id="aca6a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="aca6a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="aca6a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aca6a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aca6a-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aca6a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="aca6a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aca6a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aca6a-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aca6a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="aca6a-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="aca6a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aca6a-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="aca6a-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aca6a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aca6a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aca6a-127">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="aca6a-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="aca6a-128">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="aca6a-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





