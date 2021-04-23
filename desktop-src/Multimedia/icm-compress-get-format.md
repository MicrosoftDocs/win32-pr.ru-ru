---
title: Сообщение ICM_COMPRESS_GET_FORMAT (VFW. h)
description: Сообщение ICM \_ \_ Get \_ Format запрашивает выходной формат сжатых данных из драйвера сжатия видео. Это сообщение можно отправить явно или с помощью макроса Иккомпрессжетформат.
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- ICM_COMPRESS_GET_FORMAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096ceafa382bdbae5e4efe16975b3518735e773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492360"
---
# <a name="icm_compress_get_format-message"></a><span data-ttu-id="ef850-105">ICM \_ сжимать \_ Получение \_ формата сообщения</span><span class="sxs-lookup"><span data-stu-id="ef850-105">ICM\_COMPRESS\_GET\_FORMAT message</span></span>

<span data-ttu-id="ef850-106">Сообщение **ICM \_ \_ Get \_ Format** запрашивает выходной формат сжатых данных из драйвера сжатия видео.</span><span class="sxs-lookup"><span data-stu-id="ef850-106">The **ICM\_COMPRESS\_GET\_FORMAT** message requests the output format of the compressed data from a video compression driver.</span></span> <span data-ttu-id="ef850-107">Это сообщение можно отправить явно или с помощью макроса [**иккомпрессжетформат**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) .</span><span class="sxs-lookup"><span data-stu-id="ef850-107">You can send this message explicitly or by using the [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) macro.</span></span>


```C++
ICM_COMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="ef850-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef850-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef850-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*лпбиинпут*</span><span class="sxs-lookup"><span data-stu-id="ef850-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="ef850-110">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую входной формат.</span><span class="sxs-lookup"><span data-stu-id="ef850-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="ef850-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*лпбиаутпут*</span><span class="sxs-lookup"><span data-stu-id="ef850-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="ef850-112">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , в которой будет содержаться выходной формат.</span><span class="sxs-lookup"><span data-stu-id="ef850-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure to contain the output format.</span></span> <span data-ttu-id="ef850-113">Для этого параметра можно указать ноль, чтобы запросить только размер выходного формата, как в макросе [**иккомпрессжетформатсизе**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) .</span><span class="sxs-lookup"><span data-stu-id="ef850-113">You can specify zero for this parameter to request only the size of the output format, as in the [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef850-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef850-114">Return Value</span></span>

<span data-ttu-id="ef850-115">Если *лпбиаутпут* равен нулю, возвращает размер структуры.</span><span class="sxs-lookup"><span data-stu-id="ef850-115">If *lpbiOutput* is zero, returns the size of the structure.</span></span>

<span data-ttu-id="ef850-116">Если *лпбиаутпут* имеет ненулевое значение, функция ВОЗВРАЩАЕТ значение ицерр \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ef850-116">If *lpbiOutput* is nonzero, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef850-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef850-117">Remarks</span></span>

<span data-ttu-id="ef850-118">Если *лпбиаутпут* имеет ненулевое значение, драйвер должен заполнить структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) с выходным форматом по умолчанию, соответствующим формату входных данных, указанному для *лпбиинпут*.</span><span class="sxs-lookup"><span data-stu-id="ef850-118">If *lpbiOutput* is nonzero, the driver should fill the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure with the default output format corresponding to the input format specified for *lpbiInput*.</span></span> <span data-ttu-id="ef850-119">Если программа сжатия может создать несколько форматов, то форматом по умолчанию должен быть тот, который сохраняет максимальный объем информации.</span><span class="sxs-lookup"><span data-stu-id="ef850-119">If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef850-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ef850-120">Requirements</span></span>



| <span data-ttu-id="ef850-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ef850-121">Requirement</span></span> | <span data-ttu-id="ef850-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ef850-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef850-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef850-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ef850-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ef850-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ef850-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef850-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ef850-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ef850-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ef850-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ef850-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef850-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef850-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef850-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef850-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef850-130">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="ef850-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ef850-131">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="ef850-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

