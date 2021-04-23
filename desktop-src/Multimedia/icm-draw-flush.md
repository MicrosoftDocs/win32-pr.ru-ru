---
title: Сообщение ICM_DRAW_FLUSH (VFW. h)
description: '\_ \_ Сообщение о сбросе ICM Draw уведомляет драйвер подготовки, чтобы отобразить содержимое всех буферов изображений, которые ожидают прорисовки. Это сообщение можно отправить явно или с помощью макроса Икдравфлуш.'
ms.assetid: c29ed751-c773-4476-98fe-6edef3ff0cf4
keywords:
- ICM_DRAW_FLUSH сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_FLUSH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38ec42c51222313f7d3599c3b4f264dbd21a9434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672705"
---
# <a name="icm_draw_flush-message"></a><span data-ttu-id="542b4-105">\_Сообщение о \_ сбросе ICM Draw</span><span class="sxs-lookup"><span data-stu-id="542b4-105">ICM\_DRAW\_FLUSH message</span></span>

<span data-ttu-id="542b4-106">Сообщение **о \_ \_ сбросе ICM Draw** уведомляет драйвер подготовки, чтобы отобразить содержимое всех буферов изображений, которые ожидают прорисовки.</span><span class="sxs-lookup"><span data-stu-id="542b4-106">The **ICM\_DRAW\_FLUSH** message notifies a rendering driver to render the contents of any image buffers that are waiting to be drawn.</span></span> <span data-ttu-id="542b4-107">Это сообщение можно отправить явно или с помощью макроса [**икдравфлуш**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) .</span><span class="sxs-lookup"><span data-stu-id="542b4-107">You can send this message explicitly or by using the [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) macro.</span></span>


```C++
ICM_DRAW_FLUSH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="542b4-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="542b4-108">Return Value</span></span>

<span data-ttu-id="542b4-109">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="542b4-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="542b4-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="542b4-110">Remarks</span></span>

<span data-ttu-id="542b4-111">Это сообщение используется только оборудованием, которое выполняет собственное асинхронное распаковка, время и рисование.</span><span class="sxs-lookup"><span data-stu-id="542b4-111">This message is used only by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="542b4-112">Требования</span><span class="sxs-lookup"><span data-stu-id="542b4-112">Requirements</span></span>



| <span data-ttu-id="542b4-113">Требование</span><span class="sxs-lookup"><span data-stu-id="542b4-113">Requirement</span></span> | <span data-ttu-id="542b4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="542b4-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="542b4-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="542b4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="542b4-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="542b4-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="542b4-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="542b4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="542b4-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="542b4-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="542b4-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="542b4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="542b4-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="542b4-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="542b4-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="542b4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="542b4-122">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="542b4-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="542b4-123">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="542b4-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





