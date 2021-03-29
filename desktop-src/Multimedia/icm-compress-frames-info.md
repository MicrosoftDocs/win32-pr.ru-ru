---
title: Сообщение ICM_COMPRESS_FRAMES_INFO (VFW. h)
description: '\_ \_ \_ Информационное сообщение ICM сжимать кадры уведомляет драйвер сжатия, чтобы задать параметры для ожидающего сжатия.'
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- ICM_COMPRESS_FRAMES_INFO сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_COMPRESS_FRAMES_INFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb6df0eab7706ebfc03a5e3069d4323be26ecdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492357"
---
# <a name="icm_compress_frames_info-message"></a><span data-ttu-id="5f876-104">\_ \_ Сообщение о сжатии кадров ICM \_</span><span class="sxs-lookup"><span data-stu-id="5f876-104">ICM\_COMPRESS\_FRAMES\_INFO message</span></span>

<span data-ttu-id="5f876-105">**\_ \_ \_ Информационное сообщение ICM сжимать кадры** уведомляет драйвер сжатия, чтобы задать параметры для ожидающего сжатия.</span><span class="sxs-lookup"><span data-stu-id="5f876-105">The **ICM\_COMPRESS\_FRAMES\_INFO** message notifies a compression driver to set the parameters for the pending compression.</span></span>


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a><span data-ttu-id="5f876-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f876-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f876-107"><span id="icf"></span><span id="ICF"></span>*к*</span><span class="sxs-lookup"><span data-stu-id="5f876-107"><span id="icf"></span><span id="ICF"></span>*icf*</span></span>
</dt> <dd>

<span data-ttu-id="5f876-108">Указатель на структуру [**иккомпрессфрамес**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) .</span><span class="sxs-lookup"><span data-stu-id="5f876-108">Pointer to an [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) structure.</span></span> <span data-ttu-id="5f876-109">Элементы **GetData** и **путдата** этой структуры не используются с этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="5f876-109">The **GetData** and **PutData** members of this structure are not used with this message.</span></span>

</dd> <dt>

<span data-ttu-id="5f876-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f876-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="5f876-111">Размер [**иккомпрессфрамес**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes)в байтах.</span><span class="sxs-lookup"><span data-stu-id="5f876-111">Size, in bytes, of [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f876-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f876-112">Return Value</span></span>

<span data-ttu-id="5f876-113">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5f876-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f876-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f876-114">Remarks</span></span>

<span data-ttu-id="5f876-115">Программа сжатия может использовать это сообщение для определения объема пространства, выделяемого для каждого кадра при сжатии.</span><span class="sxs-lookup"><span data-stu-id="5f876-115">A compressor can use this message to determine how much space to allocate for each frame while compressing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f876-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5f876-116">Requirements</span></span>



| <span data-ttu-id="5f876-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5f876-117">Requirement</span></span> | <span data-ttu-id="5f876-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5f876-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5f876-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f876-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5f876-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5f876-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5f876-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f876-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5f876-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5f876-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5f876-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5f876-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f876-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f876-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f876-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f876-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f876-126">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="5f876-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="5f876-127">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="5f876-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





