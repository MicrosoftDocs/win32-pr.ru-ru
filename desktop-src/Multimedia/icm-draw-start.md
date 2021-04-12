---
title: Сообщение ICM_DRAW_START (VFW. h)
description: '\_ \_ Сообщение об начальном изображении ICM уведомляет драйвер подготовки, чтобы запустить его внутреннее время для времени рисования кадров. Это сообщение можно отправить явно или с помощью макроса Икдравстарт.'
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- ICM_DRAW_START сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_START
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538659eb9878be819ee6ec1506403fcce314eb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415357"
---
# <a name="icm_draw_start-message"></a><span data-ttu-id="c02ed-105">\_Сообщение о \_ запуске ICM Draw</span><span class="sxs-lookup"><span data-stu-id="c02ed-105">ICM\_DRAW\_START message</span></span>

<span data-ttu-id="c02ed-106">Сообщение **об \_ \_ начальном изображении ICM** уведомляет драйвер подготовки, чтобы запустить его внутреннее время для времени рисования кадров.</span><span class="sxs-lookup"><span data-stu-id="c02ed-106">The **ICM\_DRAW\_START** message notifies a rendering driver to start its internal clock for the timing of drawing frames.</span></span> <span data-ttu-id="c02ed-107">Это сообщение можно отправить явно или с помощью макроса [**икдравстарт**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) .</span><span class="sxs-lookup"><span data-stu-id="c02ed-107">You can send this message explicitly or by using the [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) macro.</span></span>


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="c02ed-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c02ed-108">Return Value</span></span>

<span data-ttu-id="c02ed-109">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c02ed-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c02ed-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c02ed-110">Remarks</span></span>

<span data-ttu-id="c02ed-111">Это сообщение используется оборудованием, которое выполняет собственное асинхронное распаковка, время и рисование.</span><span class="sxs-lookup"><span data-stu-id="c02ed-111">This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="c02ed-112">Когда драйвер получает это сообщение, он должен начать отрисовку данных с частотой, указанной в сообщении о [**\_ \_ начале ICM Draw**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="c02ed-112">When the driver receives this message, it should start rendering data at the rate specified with the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span>

<span data-ttu-id="c02ed-113">Сообщения об [**\_ \_ ошибке начала и разрисовки**](icm-draw-stop.md) ICM Draw не вложены. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="c02ed-113">The **ICM\_DRAW\_START** and [**ICM\_DRAW\_STOP**](icm-draw-stop.md) messages do not nest.</span></span> <span data-ttu-id="c02ed-114">Если драйвер получает изображение **ICM \_ \_ Start** , прежде чем подготовка к просмотру остановлена с помощью **ICM \_ \_ Draw**, необходимо перезапустить визуализацию с новыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="c02ed-114">If your driver receives **ICM\_DRAW\_START** before rendering is stopped with **ICM\_DRAW\_STOP**, it should restart rendering with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="c02ed-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c02ed-115">Requirements</span></span>



| <span data-ttu-id="c02ed-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c02ed-116">Requirement</span></span> | <span data-ttu-id="c02ed-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c02ed-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c02ed-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c02ed-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c02ed-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c02ed-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c02ed-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c02ed-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c02ed-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c02ed-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c02ed-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c02ed-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c02ed-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c02ed-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c02ed-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c02ed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c02ed-125">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="c02ed-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="c02ed-126">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="c02ed-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





