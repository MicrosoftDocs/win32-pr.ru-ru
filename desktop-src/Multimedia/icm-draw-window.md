---
title: Сообщение ICM_DRAW_WINDOW (VFW. h)
description: Сообщение в \_ окне ICM Draw \_ уведомляет драйвер подготовки, что необходимо перерисовать окно, заданное для \_ \_ начала сообщения ICM Draw.
ms.assetid: 4df1b9a7-8d61-4e79-8f43-1e7ee266375c
keywords:
- ICM_DRAW_WINDOW сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 290b123fadcaf46a315c42e3ce9a530c5d5d36c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490134"
---
# <a name="icm_draw_window-message"></a><span data-ttu-id="19fde-104">\_ \_ Сообщение окна ICM Draw</span><span class="sxs-lookup"><span data-stu-id="19fde-104">ICM\_DRAW\_WINDOW message</span></span>

<span data-ttu-id="19fde-105">Сообщение **в \_ \_ окне ICM Draw** уведомляет драйвер подготовки, что необходимо перерисовать окно, заданное для [**\_ \_ начала сообщения ICM Draw**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="19fde-105">The **ICM\_DRAW\_WINDOW** message notifies a rendering driver that the window specified for the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message needs to be redrawn.</span></span> <span data-ttu-id="19fde-106">Окно перемещено или временно скрыто.</span><span class="sxs-lookup"><span data-stu-id="19fde-106">The window has moved or become temporarily obscured.</span></span> <span data-ttu-id="19fde-107">Это сообщение можно отправить явно или с помощью макроса [**икдраввиндов**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) .</span><span class="sxs-lookup"><span data-stu-id="19fde-107">You can send this message explicitly or by using the [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) macro.</span></span>


```C++
ICM_DRAW_WINDOW 
wParam = (DWORD_PTR) (LPVOID) prc; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="19fde-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="19fde-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19fde-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="19fde-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="19fde-110">Указатель на прямоугольник назначения в координатах экрана.</span><span class="sxs-lookup"><span data-stu-id="19fde-110">Pointer to the destination rectangle in screen coordinates.</span></span> <span data-ttu-id="19fde-111">Если этот параметр указывает на пустой прямоугольник, отрисовка должна быть отключена.</span><span class="sxs-lookup"><span data-stu-id="19fde-111">If this parameter points to an empty rectangle, drawing should be turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19fde-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19fde-112">Return Value</span></span>

<span data-ttu-id="19fde-113">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="19fde-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="19fde-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19fde-114">Remarks</span></span>

<span data-ttu-id="19fde-115">Это сообщение поддерживается оборудованием, которое выполняет собственное асинхронное распаковка, время и рисование.</span><span class="sxs-lookup"><span data-stu-id="19fde-115">This message is supported by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="19fde-116">Драйверы наложения видео это сообщение используется для рисования при скрытии или перемещении окна.</span><span class="sxs-lookup"><span data-stu-id="19fde-116">Video-overlay drivers use this message to draw when the window is obscured or moved.</span></span> <span data-ttu-id="19fde-117">Когда окно, заданное [**для \_ \_ начала отображения ICM**](icm-draw-begin.md) , полностью скрыто другими окнами, прямоугольник назначения пуст.</span><span class="sxs-lookup"><span data-stu-id="19fde-117">When a window specified for [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) is completely hidden by other windows, the destination rectangle is empty.</span></span> <span data-ttu-id="19fde-118">При возникновении этого условия драйверы должны отключать оборудование наложения видео.</span><span class="sxs-lookup"><span data-stu-id="19fde-118">Drivers should turn off video-overlay hardware when this condition occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="19fde-119">Требования</span><span class="sxs-lookup"><span data-stu-id="19fde-119">Requirements</span></span>



| <span data-ttu-id="19fde-120">Требование</span><span class="sxs-lookup"><span data-stu-id="19fde-120">Requirement</span></span> | <span data-ttu-id="19fde-121">Значение</span><span class="sxs-lookup"><span data-stu-id="19fde-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="19fde-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19fde-122">Minimum supported client</span></span><br/> | <span data-ttu-id="19fde-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="19fde-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="19fde-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19fde-124">Minimum supported server</span></span><br/> | <span data-ttu-id="19fde-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="19fde-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="19fde-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="19fde-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="19fde-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="19fde-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19fde-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19fde-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19fde-129">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="19fde-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="19fde-130">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="19fde-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





