---
title: Сообщение ICM_DRAW_RENDERBUFFER (VFW. h)
description: Сообщение ICM \_ Draw \_ рендербуффер уведомляет драйвер подготовки, чтобы вывести переданные ему кадры. Это сообщение можно отправить явно или с помощью макроса Икдраврендербуффер.
ms.assetid: b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9
keywords:
- ICM_DRAW_RENDERBUFFER сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_RENDERBUFFER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb02a1fbe334547b9679970ac7598df23237f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989122"
---
# <a name="icm_draw_renderbuffer-message"></a><span data-ttu-id="c6e1f-105">\_Сообщение ICM Draw \_ рендербуффер</span><span class="sxs-lookup"><span data-stu-id="c6e1f-105">ICM\_DRAW\_RENDERBUFFER message</span></span>

<span data-ttu-id="c6e1f-106">Сообщение **ICM \_ Draw \_ рендербуффер** уведомляет драйвер подготовки, чтобы вывести переданные ему кадры.</span><span class="sxs-lookup"><span data-stu-id="c6e1f-106">The **ICM\_DRAW\_RENDERBUFFER** message notifies a rendering driver to draw the frames that have been passed to it.</span></span> <span data-ttu-id="c6e1f-107">Это сообщение можно отправить явно или с помощью макроса [**икдраврендербуффер**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) .</span><span class="sxs-lookup"><span data-stu-id="c6e1f-107">You can send this message explicitly or by using the [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) macro.</span></span>


```C++
ICM_DRAW_RENDERBUFFER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="c6e1f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6e1f-108">Return Value</span></span>

<span data-ttu-id="c6e1f-109">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c6e1f-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6e1f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6e1f-110">Remarks</span></span>

<span data-ttu-id="c6e1f-111">Используйте это сообщение с оборудованием, которое выполняет собственное асинхронное распаковка, время и рисование.</span><span class="sxs-lookup"><span data-stu-id="c6e1f-111">Use this message with hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="c6e1f-112">Это сообщение обычно используется для выполнения операции поиска, когда драйверу необходимо специально указать отображение каждого кадра видео, переданного в него, а не воспроизведение последовательности видеокадров.</span><span class="sxs-lookup"><span data-stu-id="c6e1f-112">This message is typically used to perform a seek operation when the driver must be specifically instructed to display each video frame passed to it rather than playing a sequence of video frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e1f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c6e1f-113">Requirements</span></span>



| <span data-ttu-id="c6e1f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c6e1f-114">Requirement</span></span> | <span data-ttu-id="c6e1f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c6e1f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c6e1f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6e1f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c6e1f-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c6e1f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c6e1f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6e1f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c6e1f-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c6e1f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c6e1f-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c6e1f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6e1f-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6e1f-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6e1f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6e1f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6e1f-123">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="c6e1f-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="c6e1f-124">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="c6e1f-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





