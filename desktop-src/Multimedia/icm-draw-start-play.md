---
title: Сообщение ICM_DRAW_START_PLAY (VFW. h)
description: Сообщение ICM \_ Draw \_ Start \_ Play предоставляет время начала и окончания операции воспроизведения для драйвера подготовки к просмотру. Это сообщение можно отправить явно или с помощью макроса Икдравстартплай.
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- ICM_DRAW_START_PLAY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_START_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefea0f6344fb598fac1f0413bba5c377c5914e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135683"
---
# <a name="icm_draw_start_play-message"></a><span data-ttu-id="95edf-105">\_Сообщение о запуске ICM Draw \_ начать \_ Воспроизведение</span><span class="sxs-lookup"><span data-stu-id="95edf-105">ICM\_DRAW\_START\_PLAY message</span></span>

<span data-ttu-id="95edf-106">Сообщение **ICM \_ Draw \_ Start \_ Play** предоставляет время начала и окончания операции воспроизведения для драйвера подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="95edf-106">The **ICM\_DRAW\_START\_PLAY** message provides the start and end times of a play operation to a rendering driver.</span></span> <span data-ttu-id="95edf-107">Это сообщение можно отправить явно или с помощью макроса [**икдравстартплай**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) .</span><span class="sxs-lookup"><span data-stu-id="95edf-107">You can send this message explicitly or by using the [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) macro.</span></span>


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a><span data-ttu-id="95edf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="95edf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95edf-109"><span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*лфром*</span><span class="sxs-lookup"><span data-stu-id="95edf-109"><span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*</span></span>
</dt> <dd>

<span data-ttu-id="95edf-110">Время начала.</span><span class="sxs-lookup"><span data-stu-id="95edf-110">Start time.</span></span>

</dd> <dt>

<span data-ttu-id="95edf-111"><span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*</span><span class="sxs-lookup"><span data-stu-id="95edf-111"><span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*</span></span>
</dt> <dd>

<span data-ttu-id="95edf-112">Время окончания.</span><span class="sxs-lookup"><span data-stu-id="95edf-112">End time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95edf-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95edf-113">Return Value</span></span>

<span data-ttu-id="95edf-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="95edf-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95edf-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95edf-115">Remarks</span></span>

<span data-ttu-id="95edf-116">Это сообщение предшествует всем данным кадра, отправляемым драйверу подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="95edf-116">This message precedes any frame data sent to the rendering driver.</span></span>

<span data-ttu-id="95edf-117">Единицы для *лфром* и *lTo* задаются с помощью сообщения [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="95edf-117">Units for *lFrom* and *lTo* are specified with the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span> <span data-ttu-id="95edf-118">Для данных видео это обычно номер кадра.</span><span class="sxs-lookup"><span data-stu-id="95edf-118">For video data this is normally a frame number.</span></span> <span data-ttu-id="95edf-119">Дополнительные сведения о скорости воспроизведения см. в разделе **дврате** and **двскале** Members структуры [**икдравбегин**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) .</span><span class="sxs-lookup"><span data-stu-id="95edf-119">For more information about the playback rate, see the **dwRate** and **dwScale** members of the [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) structure.</span></span>

<span data-ttu-id="95edf-120">Если время окончания меньше времени начала, направление воспроизведения изменяется на противоположное.</span><span class="sxs-lookup"><span data-stu-id="95edf-120">If the end time is less than the start time, the playback direction is reversed.</span></span>

## <a name="requirements"></a><span data-ttu-id="95edf-121">Требования</span><span class="sxs-lookup"><span data-stu-id="95edf-121">Requirements</span></span>



| <span data-ttu-id="95edf-122">Требование</span><span class="sxs-lookup"><span data-stu-id="95edf-122">Requirement</span></span> | <span data-ttu-id="95edf-123">Значение</span><span class="sxs-lookup"><span data-stu-id="95edf-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="95edf-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95edf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="95edf-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="95edf-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="95edf-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95edf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="95edf-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="95edf-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="95edf-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="95edf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="95edf-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="95edf-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95edf-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95edf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95edf-131">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="95edf-131">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="95edf-132">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="95edf-132">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





