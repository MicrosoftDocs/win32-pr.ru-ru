---
title: Сообщение ICM_COMPRESS (VFW. h)
description: Сообщение ICM \_ Compression уведомляет драйвер сжатия видео о необходимости сжатия фрейма данных в определенный приложением буфер.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- ICM_COMPRESS сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8021a4c18ab47c9b5b848dd1cb097358f2714bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650390"
---
# <a name="icm_compress-message"></a><span data-ttu-id="827f2-104">\_Сообщение о сжатии ICM</span><span class="sxs-lookup"><span data-stu-id="827f2-104">ICM\_COMPRESS message</span></span>

<span data-ttu-id="827f2-105">Сообщение **ICM \_** Compression уведомляет драйвер сжатия видео о необходимости сжатия фрейма данных в определенный приложением буфер.</span><span class="sxs-lookup"><span data-stu-id="827f2-105">The **ICM\_COMPRESS** message notifies a video compression driver to compress a frame of data into an application-defined buffer.</span></span>


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a><span data-ttu-id="827f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="827f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="827f2-107"><span id="icc"></span><span id="ICC"></span>*профилей*</span><span class="sxs-lookup"><span data-stu-id="827f2-107"><span id="icc"></span><span id="ICC"></span>*icc*</span></span>
</dt> <dd>

<span data-ttu-id="827f2-108">Указатель на структуру [**иккомпресс**](/windows/desktop/api/Vfw/ns-vfw-iccompress) .</span><span class="sxs-lookup"><span data-stu-id="827f2-108">Pointer to an [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) structure.</span></span> <span data-ttu-id="827f2-109">Следующие члены этой структуры определяют параметры сжатия: **лпбиинпут**, **лпинпут**, **лпбиаутпут**, **лпаутпут**, **лпбипрев**, **лппрев**, **лпккид**, **лпдвфлагс**, **двфрамесизе** и **двкуалити**.</span><span class="sxs-lookup"><span data-stu-id="827f2-109">The following members of this structure specify the compression parameters: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize**, and **dwQuality**.</span></span> <span data-ttu-id="827f2-110">Драйвер также должен использовать член **бисизеимаже** структуры [**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85)) , связанной с **лпбиаутпут** из **иккомпресс** , для получения размера сжатого кадра.</span><span class="sxs-lookup"><span data-stu-id="827f2-110">The driver should also use the **biSizeImage** member of the [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure associated with **lpbiOutput** of **ICCOMPRESS** to return the size of the compressed frame.</span></span>

</dd> <dt>

<span data-ttu-id="827f2-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="827f2-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="827f2-112">Размер [**иккомпресс**](/windows/desktop/api/Vfw/ns-vfw-iccompress)в байтах.</span><span class="sxs-lookup"><span data-stu-id="827f2-112">Size, in bytes, of [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="827f2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="827f2-113">Return Value</span></span>

<span data-ttu-id="827f2-114">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="827f2-114">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="827f2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="827f2-115">Requirements</span></span>



| <span data-ttu-id="827f2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="827f2-116">Requirement</span></span> | <span data-ttu-id="827f2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="827f2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="827f2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="827f2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="827f2-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="827f2-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="827f2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="827f2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="827f2-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="827f2-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="827f2-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="827f2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="827f2-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="827f2-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="827f2-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="827f2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="827f2-125">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="827f2-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="827f2-126">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="827f2-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

