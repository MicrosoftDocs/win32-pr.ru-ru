---
title: Сообщение ICM_DECOMPRESSEX_END (VFW. h)
description: '\_ \_ Сообщение об окончании ICM декомпрессекс уведомляет драйвер распаковки о завершении распаковки и освобождения ресурсов, выделенных для распаковки. Это сообщение можно отправить явно или с помощью макроса Икдекомпрессексенд.'
ms.assetid: 7ed63a4e-bb17-43a3-b593-25c4a51be942
keywords:
- ICM_DECOMPRESSEX_END сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e96f6a069e9ed2c9c52dc2f07f1ab4c5210ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535027"
---
# <a name="icm_decompressex_end-message"></a><span data-ttu-id="85e9f-105">\_ \_ Сообщение об окончании ICM декомпрессекс</span><span class="sxs-lookup"><span data-stu-id="85e9f-105">ICM\_DECOMPRESSEX\_END message</span></span>

<span data-ttu-id="85e9f-106">Сообщение **об \_ \_ окончании ICM декомпрессекс** уведомляет драйвер распаковки о завершении распаковки и освобождения ресурсов, выделенных для распаковки.</span><span class="sxs-lookup"><span data-stu-id="85e9f-106">The **ICM\_DECOMPRESSEX\_END** message notifies a video decompression driver to end decompression and free resources allocated for decompression.</span></span> <span data-ttu-id="85e9f-107">Это сообщение можно отправить явно или с помощью макроса [**икдекомпрессексенд**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) .</span><span class="sxs-lookup"><span data-stu-id="85e9f-107">You can send this message explicitly or by using the [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) macro.</span></span>


```C++
ICM_DECOMPRESSEX_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="85e9f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85e9f-108">Return Value</span></span>

<span data-ttu-id="85e9f-109">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="85e9f-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="85e9f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85e9f-110">Remarks</span></span>

<span data-ttu-id="85e9f-111">Драйвер освобождает все ресурсы, выделенные для сообщения [**о \_ \_ начале ICM декомпрессекс**](icm-decompressex-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="85e9f-111">The driver frees any resources allocated for the [**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) message.</span></span>

<span data-ttu-id="85e9f-112">[**ICM \_ ДЕКОМПРЕССЕКС \_ Begin**](icm-decompressex-begin.md) и **ICM \_ декомпрессекс \_ End** не вложены.</span><span class="sxs-lookup"><span data-stu-id="85e9f-112">[**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) and **ICM\_DECOMPRESSEX\_END** do not nest.</span></span> <span data-ttu-id="85e9f-113">Если драйвер получает **ICM \_ декомпрессекс \_ Begin** до остановки распаковки с помощью **ICM \_ декомпрессекс \_ End**, он должен перезапустить распаковку с новыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="85e9f-113">If your driver receives **ICM\_DECOMPRESSEX\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESSEX\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="85e9f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="85e9f-114">Requirements</span></span>



| <span data-ttu-id="85e9f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="85e9f-115">Requirement</span></span> | <span data-ttu-id="85e9f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="85e9f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="85e9f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85e9f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="85e9f-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="85e9f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="85e9f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85e9f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="85e9f-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="85e9f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="85e9f-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="85e9f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="85e9f-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="85e9f-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85e9f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85e9f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85e9f-124">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="85e9f-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="85e9f-125">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="85e9f-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





