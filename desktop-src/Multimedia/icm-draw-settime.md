---
title: Сообщение ICM_DRAW_SETTIME (VFW. h)
description: ICM \_ Draw \_ SETTIME предоставляет сведения о синхронизации драйверу подготовки отчетов, который обрабатывает время рисования кадров.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- ICM_DRAW_SETTIME сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e37709477ba6080219e5225b3fde02dfed75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891757"
---
# <a name="icm_draw_settime-message"></a><span data-ttu-id="9f2d1-104">\_Сообщение ICM Draw \_ SETTIME</span><span class="sxs-lookup"><span data-stu-id="9f2d1-104">ICM\_DRAW\_SETTIME message</span></span>

<span data-ttu-id="9f2d1-105">**ICM \_ Draw \_ SETTIME** предоставляет сведения о синхронизации драйверу подготовки отчетов, который обрабатывает время рисования кадров.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-105">The **ICM\_DRAW\_SETTIME** provides synchronization information to a rendering driver that handles the timing of drawing frames.</span></span> <span data-ttu-id="9f2d1-106">Сведения о синхронизации — это образец номера кадра для рисования.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-106">The synchronization information is the sample number of the frame to draw.</span></span> <span data-ttu-id="9f2d1-107">Это сообщение можно отправить явно или с помощью макроса [**икдравсеттиме**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) .</span><span class="sxs-lookup"><span data-stu-id="9f2d1-107">You can send this message explicitly or by using the [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) macro.</span></span>


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="9f2d1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f2d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f2d1-109"><span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*лптиме*</span><span class="sxs-lookup"><span data-stu-id="9f2d1-109"><span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*</span></span>
</dt> <dd>

<span data-ttu-id="9f2d1-110">Образец номера кадра для отображения.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-110">Sample number of the frame to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f2d1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f2d1-111">Return Value</span></span>

<span data-ttu-id="9f2d1-112">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f2d1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f2d1-113">Remarks</span></span>

<span data-ttu-id="9f2d1-114">Как правило, драйвер сравнивает указанное значение с номером кадра, связанным со временем его внутреннего времени, и пытается синхронизировать два, если разница существенна.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-114">Typically, the driver compares the specified value with the frame number associated with the time of its internal clock and attempts to synchronize the two if the difference is significant.</span></span>

<span data-ttu-id="9f2d1-115">Это сообщение используется, когда оборудование выполняет собственное асинхронное распаковку, время и рисование, а оборудование использует внешний сигнал синхронизации (оборудование не используется в качестве хозяина синхронизации).</span><span class="sxs-lookup"><span data-stu-id="9f2d1-115">Use this message when the hardware performs its own asynchronous decompression, timing, and drawing, and the hardware relies on an external synchronization signal (the hardware is not being used as the synchronization master).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f2d1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9f2d1-116">Requirements</span></span>



| <span data-ttu-id="9f2d1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9f2d1-117">Requirement</span></span> | <span data-ttu-id="9f2d1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9f2d1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9f2d1-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f2d1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9f2d1-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f2d1-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9f2d1-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f2d1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9f2d1-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f2d1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9f2d1-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9f2d1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f2d1-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f2d1-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f2d1-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f2d1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f2d1-126">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="9f2d1-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="9f2d1-127">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="9f2d1-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





