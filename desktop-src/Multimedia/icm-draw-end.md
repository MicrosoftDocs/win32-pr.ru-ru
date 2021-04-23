---
title: Сообщение ICM_DRAW_END (VFW. h)
description: '\_ \_ Сообщение о ЗАВЕРШЕНии ICM выводит драйвер подготовки к распаковке текущего изображения на экран и освобождения ресурсов, выделенных для распаковки и рисования. Это сообщение можно отправить явно или с помощью макроса Икдравенд.'
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- ICM_DRAW_END сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e420ac37791bc6c5aa7f660d71005be65fc87fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802621"
---
# <a name="icm_draw_end-message"></a><span data-ttu-id="301be-105">\_Сообщение окончания прорисовки ICM \_</span><span class="sxs-lookup"><span data-stu-id="301be-105">ICM\_DRAW\_END message</span></span>

<span data-ttu-id="301be-106">Сообщение **о \_ \_ завершении ICM** выводит драйвер подготовки к распаковке текущего изображения на экран и освобождения ресурсов, выделенных для распаковки и рисования.</span><span class="sxs-lookup"><span data-stu-id="301be-106">The **ICM\_DRAW\_END** message notifies a rendering driver to decompress the current image to the screen and to release resources allocated for decompression and drawing.</span></span> <span data-ttu-id="301be-107">Это сообщение можно отправить явно или с помощью макроса [**икдравенд**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) .</span><span class="sxs-lookup"><span data-stu-id="301be-107">You can send this message explicitly or by using the [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) macro.</span></span>


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="301be-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="301be-108">Return Value</span></span>

<span data-ttu-id="301be-109">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="301be-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="301be-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="301be-110">Remarks</span></span>

<span data-ttu-id="301be-111">[**\_ \_ Начало**](icm-draw-begin.md) и **\_ \_ конец** изображения ICM не вложены в сообщения.</span><span class="sxs-lookup"><span data-stu-id="301be-111">The [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) and **ICM\_DRAW\_END** messages do not nest.</span></span> <span data-ttu-id="301be-112">Если драйвер получает функцию **ICM \_ Draw \_** , то перед **\_ \_ завершением** распаковки с использованием ICM Draw необходимо перезапустить распаковку с новыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="301be-112">If your driver receives **ICM\_DRAW\_BEGIN** before decompression is stopped with **ICM\_DRAW\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="301be-113">Требования</span><span class="sxs-lookup"><span data-stu-id="301be-113">Requirements</span></span>



| <span data-ttu-id="301be-114">Требование</span><span class="sxs-lookup"><span data-stu-id="301be-114">Requirement</span></span> | <span data-ttu-id="301be-115">Значение</span><span class="sxs-lookup"><span data-stu-id="301be-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="301be-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="301be-116">Minimum supported client</span></span><br/> | <span data-ttu-id="301be-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="301be-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="301be-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="301be-118">Minimum supported server</span></span><br/> | <span data-ttu-id="301be-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="301be-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="301be-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="301be-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="301be-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="301be-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="301be-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="301be-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="301be-123">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="301be-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="301be-124">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="301be-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





