---
title: Сообщение ICM_DECOMPRESS_END (VFW. h)
description: '\_ \_ Сообщение об ОКОНЧАНИи распаковки ICM уведомляет драйвер распаковки о завершении распаковки и освобождения ресурсов, выделенных для распаковки. Это сообщение можно отправить явно или с помощью макроса Икдекомпрессенд.'
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- ICM_DECOMPRESS_END сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25155755b6bfbb893905e6facad890dbf98f175
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803377"
---
# <a name="icm_decompress_end-message"></a><span data-ttu-id="a04e6-105">\_Завершающее сообщение РАЗуплотнения ICM \_</span><span class="sxs-lookup"><span data-stu-id="a04e6-105">ICM\_DECOMPRESS\_END message</span></span>

<span data-ttu-id="a04e6-106">Сообщение **об \_ \_ окончании распаковки ICM** уведомляет драйвер распаковки о завершении распаковки и освобождения ресурсов, выделенных для распаковки.</span><span class="sxs-lookup"><span data-stu-id="a04e6-106">The **ICM\_DECOMPRESS\_END** message notifies a video decompression driver to end decompression and free resources allocated for decompression.</span></span> <span data-ttu-id="a04e6-107">Это сообщение можно отправить явно или с помощью макроса [**икдекомпрессенд**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) .</span><span class="sxs-lookup"><span data-stu-id="a04e6-107">You can send this message explicitly or by using the [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) macro.</span></span>


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="a04e6-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a04e6-108">Return Value</span></span>

<span data-ttu-id="a04e6-109">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a04e6-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a04e6-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a04e6-110">Remarks</span></span>

<span data-ttu-id="a04e6-111">Драйвер должен освободить все ресурсы, выделенные для [**сообщения \_ \_ Begin reуплотнения ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="a04e6-111">The driver should free any resources allocated for the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="a04e6-112">[**ICM \_ Конец СЖАТИЯ \_ Begin**](icm-decompress-begin.md) и **ICM \_ unуплотнение \_** не вложены.</span><span class="sxs-lookup"><span data-stu-id="a04e6-112">[**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) and **ICM\_DECOMPRESS\_END** do not nest.</span></span> <span data-ttu-id="a04e6-113">Если драйвер Получает подсистему **\_ распаковки ICM \_ Begin** до остановки распаковки **с \_ \_ окончанием распаковки ICM**, необходимо перезапустить распаковку с новыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="a04e6-113">If your driver receives **ICM\_DECOMPRESS\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESS\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a04e6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a04e6-114">Requirements</span></span>



| <span data-ttu-id="a04e6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a04e6-115">Requirement</span></span> | <span data-ttu-id="a04e6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a04e6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a04e6-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a04e6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a04e6-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a04e6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a04e6-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a04e6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a04e6-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a04e6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a04e6-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a04e6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a04e6-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a04e6-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a04e6-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a04e6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04e6-124">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="a04e6-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a04e6-125">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="a04e6-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





