---
title: Сообщение ICM_DRAW_STOP_PLAY (VFW. h)
description: '\_ \_ \_ При завершении операции воспроизведения выводится сообщение о том, что средство ICM Draw останавливает воспроизведение уведомляет драйвер подготовки. Это сообщение можно отправить явно или с помощью макроса Икдравстопплай.'
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- ICM_DRAW_STOP_PLAY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea3964b623c93d452ab7bf9a32c6b9d9b1573fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137814"
---
# <a name="icm_draw_stop_play-message"></a><span data-ttu-id="2a23e-105">\_Сообщение о \_ зависании при прорисовке \_</span><span class="sxs-lookup"><span data-stu-id="2a23e-105">ICM\_DRAW\_STOP\_PLAY message</span></span>

<span data-ttu-id="2a23e-106">При завершении операции воспроизведения выводится сообщение о том, что средство **ICM \_ Draw \_ останавливает \_ Воспроизведение** уведомляет драйвер подготовки.</span><span class="sxs-lookup"><span data-stu-id="2a23e-106">The **ICM\_DRAW\_STOP\_PLAY** message notifies a rendering driver when a play operation is complete.</span></span> <span data-ttu-id="2a23e-107">Это сообщение можно отправить явно или с помощью макроса [**икдравстопплай**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) .</span><span class="sxs-lookup"><span data-stu-id="2a23e-107">You can send this message explicitly or by using the [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) macro.</span></span>


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="2a23e-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a23e-108">Return Value</span></span>

<span data-ttu-id="2a23e-109">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2a23e-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a23e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a23e-110">Remarks</span></span>

<span data-ttu-id="2a23e-111">Это сообщение используется по завершении операции воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="2a23e-111">Use this message when the play operation is complete.</span></span> <span data-ttu-id="2a23e-112">Используйте сообщение об ошибке [**ICM \_ Draw \_**](icm-draw-stop.md) для окончания времени.</span><span class="sxs-lookup"><span data-stu-id="2a23e-112">Use the [**ICM\_DRAW\_STOP**](icm-draw-stop.md) message to end timing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a23e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2a23e-113">Requirements</span></span>



| <span data-ttu-id="2a23e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2a23e-114">Requirement</span></span> | <span data-ttu-id="2a23e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2a23e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2a23e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a23e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2a23e-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2a23e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2a23e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a23e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2a23e-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2a23e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2a23e-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2a23e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a23e-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a23e-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a23e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a23e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a23e-123">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="2a23e-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2a23e-124">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="2a23e-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





