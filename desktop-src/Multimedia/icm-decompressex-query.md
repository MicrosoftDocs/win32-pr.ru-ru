---
title: Сообщение ICM_DECOMPRESSEX_QUERY (VFW. h)
description: Сообщение с \_ \_ запросом ICM декомпрессекс запрашивает драйвер сжатия видео, чтобы определить, поддерживает ли он определенный входной формат, или же он может распаковать определенный входной формат в определенный выходной формат.
ms.assetid: 7778a52d-2ed8-495c-8656-c6beb1863499
keywords:
- ICM_DECOMPRESSEX_QUERY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b2ef5999b9e0619ccbd9ccabd9bc5223b3bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892421"
---
# <a name="icm_decompressex_query-message"></a><span data-ttu-id="96bbe-104">\_ \_ Сообщение запроса ICM декомпрессекс</span><span class="sxs-lookup"><span data-stu-id="96bbe-104">ICM\_DECOMPRESSEX\_QUERY message</span></span>

<span data-ttu-id="96bbe-105">Сообщение **с \_ \_ запросом ICM декомпрессекс** запрашивает драйвер сжатия видео, чтобы определить, поддерживает ли он определенный входной формат, или же он может распаковать определенный входной формат в определенный выходной формат.</span><span class="sxs-lookup"><span data-stu-id="96bbe-105">The **ICM\_DECOMPRESSEX\_QUERY** message queries a video compression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.</span></span>


```C++
ICM_DECOMPRESSEX_QUERY 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="96bbe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="96bbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96bbe-107"><span id="icdex"></span><span id="ICDEX"></span>*икдекс*</span><span class="sxs-lookup"><span data-stu-id="96bbe-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="96bbe-108">Указатель на структуру [**икдекомпрессекс**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) , содержащую входной формат.</span><span class="sxs-lookup"><span data-stu-id="96bbe-108">Pointer to a [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="96bbe-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="96bbe-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="96bbe-110">Размер [**икдекомпрессекс**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)в байтах.</span><span class="sxs-lookup"><span data-stu-id="96bbe-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96bbe-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96bbe-111">Return Value</span></span>

<span data-ttu-id="96bbe-112">Возвращает ИЦЕРР \_ ОК, если указанное распаковка поддерживается или ицерр \_ бадформат в противном случае.</span><span class="sxs-lookup"><span data-stu-id="96bbe-112">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="96bbe-113">Требования</span><span class="sxs-lookup"><span data-stu-id="96bbe-113">Requirements</span></span>



| <span data-ttu-id="96bbe-114">Требование</span><span class="sxs-lookup"><span data-stu-id="96bbe-114">Requirement</span></span> | <span data-ttu-id="96bbe-115">Значение</span><span class="sxs-lookup"><span data-stu-id="96bbe-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="96bbe-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96bbe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="96bbe-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96bbe-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="96bbe-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96bbe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="96bbe-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96bbe-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="96bbe-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="96bbe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="96bbe-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="96bbe-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96bbe-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96bbe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96bbe-123">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="96bbe-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="96bbe-124">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="96bbe-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





