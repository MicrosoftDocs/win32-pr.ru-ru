---
title: Сообщение ICM_COMPRESS_GET_SIZE (VFW. h)
description: Сообщение ICM \_ \_ \_ Request Size получает запрос о том, что драйверу сжатия видео предоставлен максимальный размер одного кадра данных при сжатии в указанный формат вывода. Это сообщение можно отправить явно или с помощью макроса Иккомпрессжетсизе.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- ICM_COMPRESS_GET_SIZE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_SIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b0b61c78cc684de27d1e9a2747498e30eb3fe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989161"
---
# <a name="icm_compress_get_size-message"></a><span data-ttu-id="6711a-105">\_Сообщение о сжатии \_ получения \_ размера ICM</span><span class="sxs-lookup"><span data-stu-id="6711a-105">ICM\_COMPRESS\_GET\_SIZE message</span></span>

<span data-ttu-id="6711a-106">Сообщение **ICM Request \_ \_ \_ Size получает** запрос о том, что драйверу сжатия видео предоставлен максимальный размер одного кадра данных при сжатии в указанный формат вывода.</span><span class="sxs-lookup"><span data-stu-id="6711a-106">The **ICM\_COMPRESS\_GET\_SIZE** message requests that the video compression driver supply the maximum size of one frame of data when compressed into the specified output format.</span></span> <span data-ttu-id="6711a-107">Это сообщение можно отправить явно или с помощью макроса [**иккомпрессжетсизе**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) .</span><span class="sxs-lookup"><span data-stu-id="6711a-107">You can send this message explicitly or by using the [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) macro.</span></span>


```C++
ICM_COMPRESS_GET_SIZE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="6711a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6711a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6711a-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*лпбиинпут*</span><span class="sxs-lookup"><span data-stu-id="6711a-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="6711a-110">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую входной формат.</span><span class="sxs-lookup"><span data-stu-id="6711a-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="6711a-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*лпбиаутпут*</span><span class="sxs-lookup"><span data-stu-id="6711a-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="6711a-112">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую выходной формат.</span><span class="sxs-lookup"><span data-stu-id="6711a-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6711a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6711a-113">Return Value</span></span>

<span data-ttu-id="6711a-114">Возвращает максимальное число байтов, которое может занимать один сжатый кадр.</span><span class="sxs-lookup"><span data-stu-id="6711a-114">Returns the maximum number of bytes a single compressed frame can occupy.</span></span>

## <a name="remarks"></a><span data-ttu-id="6711a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6711a-115">Remarks</span></span>

<span data-ttu-id="6711a-116">Как правило, приложения отправляют это сообщение, чтобы определить размер буфера, выделяемого для сжатого кадра.</span><span class="sxs-lookup"><span data-stu-id="6711a-116">Typically, applications send this message to determine how large a buffer to allocate for the compressed frame.</span></span>

<span data-ttu-id="6711a-117">Драйвер должен вычислить размер максимально возможного кадра на основе входных и выходных форматов.</span><span class="sxs-lookup"><span data-stu-id="6711a-117">The driver should calculate the size of the largest possible frame based on the input and output formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="6711a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6711a-118">Requirements</span></span>



| <span data-ttu-id="6711a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6711a-119">Requirement</span></span> | <span data-ttu-id="6711a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6711a-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6711a-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6711a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6711a-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6711a-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6711a-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6711a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6711a-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6711a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6711a-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6711a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6711a-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6711a-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6711a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6711a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6711a-128">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="6711a-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="6711a-129">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="6711a-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

