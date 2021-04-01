---
title: Сообщение ICM_DECOMPRESS (VFW. h)
description: Сообщение ICM \_ uncompression уведомляет драйвер распаковки видео о необходимости распаковки кадра данных в буфер, определенный приложением.
ms.assetid: 666f2ebf-80a5-4846-861d-c79c3001c5a0
keywords:
- ICM_DECOMPRESS сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c890a8ca15202f57fdaa02922e364af75f7b952
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071894"
---
# <a name="icm_decompress-message"></a><span data-ttu-id="0cc08-104">\_Сообщение распаковки ICM</span><span class="sxs-lookup"><span data-stu-id="0cc08-104">ICM\_DECOMPRESS message</span></span>

<span data-ttu-id="0cc08-105">Сообщение **ICM \_** uncompression уведомляет драйвер распаковки видео о необходимости распаковки кадра данных в буфер, определенный приложением.</span><span class="sxs-lookup"><span data-stu-id="0cc08-105">The **ICM\_DECOMPRESS** message notifies a video decompression driver to decompress a frame of data into an application-defined buffer.</span></span>


```C++
ICM_DECOMPRESS 
wParam = (DWORD) (LPVOID) &icd; 
lParam = sizeof(ICDECOMPRESS); 
```



## <a name="parameters"></a><span data-ttu-id="0cc08-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0cc08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cc08-107"><span id="icd"></span><span id="ICD"></span>*ICD*</span><span class="sxs-lookup"><span data-stu-id="0cc08-107"><span id="icd"></span><span id="ICD"></span>*icd*</span></span>
</dt> <dd>

<span data-ttu-id="0cc08-108">Указатель на структуру [**икдекомпресс**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) .</span><span class="sxs-lookup"><span data-stu-id="0cc08-108">Pointer to an [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0cc08-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="0cc08-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="0cc08-110">Размер [**икдекомпресс**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)в байтах.</span><span class="sxs-lookup"><span data-stu-id="0cc08-110">Size, in bytes, of [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cc08-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0cc08-111">Return Value</span></span>

<span data-ttu-id="0cc08-112">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0cc08-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cc08-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0cc08-113">Remarks</span></span>

<span data-ttu-id="0cc08-114">Если требуется, чтобы драйвер распаковать данные непосредственно на экране, отправьте сообщение [**ICM \_ Draw**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="0cc08-114">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="0cc08-115">Драйвер возвращает ошибку, если это сообщение получено до сообщения [**\_ \_ начала распаковки ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="0cc08-115">The driver returns an error if this message is received before the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cc08-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0cc08-116">Requirements</span></span>



| <span data-ttu-id="0cc08-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0cc08-117">Requirement</span></span> | <span data-ttu-id="0cc08-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0cc08-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc08-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0cc08-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0cc08-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0cc08-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0cc08-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0cc08-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0cc08-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0cc08-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0cc08-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0cc08-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cc08-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cc08-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cc08-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0cc08-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cc08-126">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="0cc08-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="0cc08-127">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="0cc08-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





