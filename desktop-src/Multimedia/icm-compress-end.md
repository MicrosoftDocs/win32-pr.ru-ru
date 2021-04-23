---
title: Сообщение ICM_COMPRESS_END (VFW. h)
description: '\_ \_ Сообщение о завершении сжатия ICM уведомляет драйвер сжатия видео о завершении сжатия и свободных ресурсах, выделенных для сжатия. Это сообщение можно отправить явно или с помощью макроса Иккомпрессенд.'
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- ICM_COMPRESS_END сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_COMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320cc99ed4223b7919b85d2b39e15d4d9b76aa90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489900"
---
# <a name="icm_compress_end-message"></a><span data-ttu-id="e2ab8-105">\_ \_ Завершающее сообщение сжатия ICM</span><span class="sxs-lookup"><span data-stu-id="e2ab8-105">ICM\_COMPRESS\_END message</span></span>

<span data-ttu-id="e2ab8-106">Сообщение **о \_ \_ завершении сжатия ICM** уведомляет драйвер сжатия видео о завершении сжатия и свободных ресурсах, выделенных для сжатия.</span><span class="sxs-lookup"><span data-stu-id="e2ab8-106">The **ICM\_COMPRESS\_END** message notifies a video compression driver to end compression and free resources allocated for compression.</span></span> <span data-ttu-id="e2ab8-107">Это сообщение можно отправить явно или с помощью макроса [**иккомпрессенд**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) .</span><span class="sxs-lookup"><span data-stu-id="e2ab8-107">You can send this message explicitly or by using the [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) macro.</span></span>


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="e2ab8-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2ab8-108">Return Value</span></span>

<span data-ttu-id="e2ab8-109">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e2ab8-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2ab8-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2ab8-110">Remarks</span></span>

<span data-ttu-id="e2ab8-111">ВКМ сохраняет параметры последнего сообщения о [**\_ \_ начале сжатия ICM**](icm-compress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="e2ab8-111">VCM saves the settings of the most recent [**ICM\_COMPRESS\_BEGIN**](icm-compress-begin.md) message.</span></span> <span data-ttu-id="e2ab8-112">**ICM \_ \_Begin** и сжатие ICM не вложены в **\_ \_ конец** .</span><span class="sxs-lookup"><span data-stu-id="e2ab8-112">**ICM\_COMPRESS\_BEGIN** and **ICM\_COMPRESS\_END** do not nest.</span></span> <span data-ttu-id="e2ab8-113">Если драйвер получает коэффициент **\_ сжатия ICM \_** , прежде чем сжатие будет остановлено с **\_ \_ окончанием сжатия ICM**, необходимо перезапустить сжатие с новыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="e2ab8-113">If your driver receives **ICM\_COMPRESS\_BEGIN** before compression is stopped with **ICM\_COMPRESS\_END**, it should restart compression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2ab8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e2ab8-114">Requirements</span></span>



| <span data-ttu-id="e2ab8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e2ab8-115">Requirement</span></span> | <span data-ttu-id="e2ab8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e2ab8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e2ab8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2ab8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e2ab8-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e2ab8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e2ab8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2ab8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e2ab8-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e2ab8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e2ab8-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e2ab8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2ab8-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2ab8-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2ab8-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2ab8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2ab8-124">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="e2ab8-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="e2ab8-125">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="e2ab8-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





