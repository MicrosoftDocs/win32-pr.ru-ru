---
title: Сообщение ICM_DECOMPRESSEX (VFW. h)
description: Сообщение ICM \_ декомпрессекс уведомляет драйвер сжатия видео о необходимости распаковать кадр данных непосредственно на экран, распаковать его со слоем DIB или распаковать изображения, описанные в исходных и целевых прямоугольниках.
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- ICM_DECOMPRESSEX сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d33451547bc598250a97e73682712e157aa13a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071893"
---
# <a name="icm_decompressex-message"></a><span data-ttu-id="9c90d-104">\_Сообщение ICM декомпрессекс</span><span class="sxs-lookup"><span data-stu-id="9c90d-104">ICM\_DECOMPRESSEX message</span></span>

<span data-ttu-id="9c90d-105">Сообщение **ICM \_ декомпрессекс** уведомляет драйвер сжатия видео о необходимости распаковать кадр данных непосредственно на экран, распаковать его со слоем DIB или распаковать изображения, описанные в исходных и целевых прямоугольниках.</span><span class="sxs-lookup"><span data-stu-id="9c90d-105">The **ICM\_DECOMPRESSEX** message notifies a video compression driver to decompress a frame of data directly to the screen, decompress to an upside-down DIB, or decompress images described with source and destination rectangles.</span></span>


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="9c90d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c90d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c90d-107"><span id="icdex"></span><span id="ICDEX"></span>*икдекс*</span><span class="sxs-lookup"><span data-stu-id="9c90d-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="9c90d-108">Указатель на структуру [**икдекомпрессекс**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) .</span><span class="sxs-lookup"><span data-stu-id="9c90d-108">Pointer to an [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9c90d-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c90d-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="9c90d-110">Размер [**икдекомпрессекс**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)в байтах.</span><span class="sxs-lookup"><span data-stu-id="9c90d-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c90d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c90d-111">Return Value</span></span>

<span data-ttu-id="9c90d-112">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9c90d-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c90d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c90d-113">Remarks</span></span>

<span data-ttu-id="9c90d-114">Это сообщение похоже на [**\_ распаковку ICM**](icm-decompress.md) , за исключением того, что в нем используется структура [**икдекомпрессекс**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) для определения сведений о распаковке.</span><span class="sxs-lookup"><span data-stu-id="9c90d-114">This message is similar to [**ICM\_DECOMPRESS**](icm-decompress.md) except that it uses the [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure to define its decompression information.</span></span>

<span data-ttu-id="9c90d-115">Если требуется, чтобы драйвер распаковать данные непосредственно на экране, отправьте сообщение [**ICM \_ Draw**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="9c90d-115">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="9c90d-116">Драйвер возвращает ошибку, если это сообщение получено до сообщения [**ICM \_ декомпрессекс \_ Begin**](icm-decompressex-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="9c90d-116">The driver returns an error if this message is received before the [**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c90d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9c90d-117">Requirements</span></span>



| <span data-ttu-id="9c90d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9c90d-118">Requirement</span></span> | <span data-ttu-id="9c90d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9c90d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9c90d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c90d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9c90d-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c90d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9c90d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c90d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9c90d-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c90d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9c90d-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9c90d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c90d-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c90d-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c90d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c90d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c90d-127">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="9c90d-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="9c90d-128">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="9c90d-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





