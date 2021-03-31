---
title: Сообщение ICM_GETBUFFERSWANTED (VFW. h)
description: В \_ сообщении ICM жетбуфферсвантед запрашивается драйвер для количества выделяемых буферов. Это сообщение можно отправить явно или с помощью макроса Икжетбуфферсвантед.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- ICM_GETBUFFERSWANTED сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_GETBUFFERSWANTED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06de8cc3bcfe463d0318651c8e2d51b269504769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988316"
---
# <a name="icm_getbufferswanted-message"></a><span data-ttu-id="2ca8a-105">\_Сообщение ICM жетбуфферсвантед</span><span class="sxs-lookup"><span data-stu-id="2ca8a-105">ICM\_GETBUFFERSWANTED message</span></span>

<span data-ttu-id="2ca8a-106">В сообщении **ICM \_ жетбуфферсвантед** запрашивается драйвер для количества выделяемых буферов.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-106">The **ICM\_GETBUFFERSWANTED** message queries a driver for the number of buffers to allocate.</span></span> <span data-ttu-id="2ca8a-107">Это сообщение можно отправить явно или с помощью макроса [**икжетбуфферсвантед**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) .</span><span class="sxs-lookup"><span data-stu-id="2ca8a-107">You can send this message explicitly or by using the [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) macro.</span></span>


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="2ca8a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ca8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ca8a-109"><span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*лпдвбуфферс*</span><span class="sxs-lookup"><span data-stu-id="2ca8a-109"><span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*</span></span>
</dt> <dd>

<span data-ttu-id="2ca8a-110">Адрес, который будет содержать число выборок, необходимых драйверу для эффективной визуализации данных.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-110">Address to contain the number of samples the driver needs to efficiently render the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ca8a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ca8a-111">Return Value</span></span>

<span data-ttu-id="2ca8a-112">Возвращает ИЦЕРР \_ ОК, если \_ в противном случае успешно или ИЦЕРР не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-112">Returns ICERR\_OK if successful or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ca8a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ca8a-113">Remarks</span></span>

<span data-ttu-id="2ca8a-114">Это сообщение используется драйверами, которые используют оборудование для визуализации данных и хотят обеспечить минимальную задержку, вызванную ожиданием прибытия буферов.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-114">This message is used by drivers that use hardware to render data and want to ensure a minimal time lag caused by waiting for buffers to arrive.</span></span> <span data-ttu-id="2ca8a-115">Например, если драйвер управляет платой распаковки видео, которая может содержать 10 кадров видео, это сообщение может вернуть 10.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-115">For example, if a driver controls a video decompression board that can hold 10 frames of video, it could return 10 for this message.</span></span> <span data-ttu-id="2ca8a-116">Это означает, что приложения попытаются остаться в 10 кадрах до конца фрейма, который им необходим.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-116">This instructs applications to try to stay 10 frames ahead of the frame it currently needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ca8a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2ca8a-117">Requirements</span></span>



| <span data-ttu-id="2ca8a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2ca8a-118">Requirement</span></span> | <span data-ttu-id="2ca8a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2ca8a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2ca8a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2ca8a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca8a-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2ca8a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2ca8a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2ca8a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca8a-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2ca8a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2ca8a-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2ca8a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ca8a-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ca8a-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ca8a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ca8a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca8a-127">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="2ca8a-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2ca8a-128">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="2ca8a-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





