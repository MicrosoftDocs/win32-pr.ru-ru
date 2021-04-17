---
title: Сообщение ICM_COMPRESS_QUERY (VFW. h)
description: В \_ сообщении о \_ запросе сжатия ICM запрашивается драйвер сжатия видео, чтобы определить, поддерживает ли он определенный входной формат, или же он может сжимать определенный входной формат в определенный выходной формат.
ms.assetid: 6d0e735e-8252-4507-b8be-1ba87774f637
keywords:
- ICM_COMPRESS_QUERY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_COMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a00482cc39f21ef6ddfb241f0534924c503200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672806"
---
# <a name="icm_compress_query-message"></a><span data-ttu-id="98a6d-104">\_Сообщение о \_ запросе сжатия ICM</span><span class="sxs-lookup"><span data-stu-id="98a6d-104">ICM\_COMPRESS\_QUERY message</span></span>

<span data-ttu-id="98a6d-105">В сообщении о **\_ \_ запросе сжатия ICM** запрашивается драйвер сжатия видео, чтобы определить, поддерживает ли он определенный входной формат, или же он может сжимать определенный входной формат в определенный выходной формат.</span><span class="sxs-lookup"><span data-stu-id="98a6d-105">The **ICM\_COMPRESS\_QUERY** message queries a video compression driver to determine if it supports a specific input format or if it can compress a specific input format to a specific output format.</span></span> <span data-ttu-id="98a6d-106">Это сообщение можно отправить явно или с помощью макроса [**иккомпресскуери**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) .</span><span class="sxs-lookup"><span data-stu-id="98a6d-106">You can send this message explicitly or by using the [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) macro.</span></span>


```C++
ICM_COMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="98a6d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="98a6d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98a6d-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*лпбиинпут*</span><span class="sxs-lookup"><span data-stu-id="98a6d-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="98a6d-109">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую входной формат.</span><span class="sxs-lookup"><span data-stu-id="98a6d-109">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="98a6d-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*лпбиаутпут*</span><span class="sxs-lookup"><span data-stu-id="98a6d-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="98a6d-111">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую выходной формат.</span><span class="sxs-lookup"><span data-stu-id="98a6d-111">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span> <span data-ttu-id="98a6d-112">Для этого параметра можно указать ноль, чтобы указать допустимый выходной формат.</span><span class="sxs-lookup"><span data-stu-id="98a6d-112">You can specify zero for this parameter to indicate any output format is acceptable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98a6d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98a6d-113">Return Value</span></span>

<span data-ttu-id="98a6d-114">Возвращает ИЦЕРР \_ ОК, если указанное сжатие поддерживается или ицерр \_ бадформат в противном случае.</span><span class="sxs-lookup"><span data-stu-id="98a6d-114">Returns ICERR\_OK if the specified compression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="98a6d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98a6d-115">Remarks</span></span>

<span data-ttu-id="98a6d-116">Когда драйвер получает это сообщение, он должен проверить структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , связанную с *лпбиинпут* , чтобы определить, может ли он сжимать входной формат.</span><span class="sxs-lookup"><span data-stu-id="98a6d-116">When a driver receives this message, it should examine the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure associated with *lpbiInput* to determine if it can compress the input format.</span></span>

## <a name="requirements"></a><span data-ttu-id="98a6d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="98a6d-117">Requirements</span></span>



| <span data-ttu-id="98a6d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="98a6d-118">Requirement</span></span> | <span data-ttu-id="98a6d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="98a6d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="98a6d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98a6d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="98a6d-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="98a6d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="98a6d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98a6d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="98a6d-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="98a6d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="98a6d-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="98a6d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="98a6d-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="98a6d-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98a6d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98a6d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98a6d-127">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="98a6d-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="98a6d-128">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="98a6d-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

