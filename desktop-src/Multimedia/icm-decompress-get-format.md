---
title: Сообщение ICM_DECOMPRESS_GET_FORMAT (VFW. h)
description: '\_ \_ \_ Сообщение о формате ICM uncompression получает запрос к выходному формату распакованных данных из драйвера распаковки видео. Это сообщение можно отправить явно или с помощью макроса Икдекомпрессжетформат.'
ms.assetid: 51753f47-758b-4d3e-9a53-9db284da2473
keywords:
- ICM_DECOMPRESS_GET_FORMAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7eefa655646deae8e67fa16a87bfdb81a8b936
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071896"
---
# <a name="icm_decompress_get_format-message"></a><span data-ttu-id="ce309-105">Выводит \_ \_ сообщение о \_ форматировании ICM</span><span class="sxs-lookup"><span data-stu-id="ce309-105">ICM\_DECOMPRESS\_GET\_FORMAT message</span></span>

<span data-ttu-id="ce309-106">Сообщение **о \_ \_ \_ формате ICM** uncompression получает запрос к выходному формату распакованных данных из драйвера распаковки видео.</span><span class="sxs-lookup"><span data-stu-id="ce309-106">The **ICM\_DECOMPRESS\_GET\_FORMAT** message requests the output format of the decompressed data from a video decompression driver.</span></span> <span data-ttu-id="ce309-107">Это сообщение можно отправить явно или с помощью макроса [**икдекомпрессжетформат**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) .</span><span class="sxs-lookup"><span data-stu-id="ce309-107">You can send this message explicitly or by using the [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) macro.</span></span>


```C++
ICM_DECOMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="ce309-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce309-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce309-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*лпбиинпут*</span><span class="sxs-lookup"><span data-stu-id="ce309-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="ce309-110">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую входной формат.</span><span class="sxs-lookup"><span data-stu-id="ce309-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="ce309-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*лпбиаутпут*</span><span class="sxs-lookup"><span data-stu-id="ce309-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="ce309-112">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , в которой будет содержаться выходной формат.</span><span class="sxs-lookup"><span data-stu-id="ce309-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure to contain the output format.</span></span> <span data-ttu-id="ce309-113">Можно указать ноль, чтобы запросить только размер выходного формата, как в макросе [**икдекомпрессжетформатсизе**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) .</span><span class="sxs-lookup"><span data-stu-id="ce309-113">You can specify zero to request only the size of the output format, as in the [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce309-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce309-114">Return Value</span></span>

<span data-ttu-id="ce309-115">Если *лпбиаутпут* равен нулю, возвращает размер структуры.</span><span class="sxs-lookup"><span data-stu-id="ce309-115">If *lpbiOutput* is zero, returns the size of the structure.</span></span>

<span data-ttu-id="ce309-116">Если *лпбиаутпут* имеет ненулевое значение, функция ВОЗВРАЩАЕТ значение ицерр \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ce309-116">If *lpbiOutput* is nonzero, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce309-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce309-117">Remarks</span></span>

<span data-ttu-id="ce309-118">Если *лпбиаутпут* имеет ненулевое значение, драйвер должен заполнить структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) с выходным форматом по умолчанию, соответствующим формату входных данных, указанному для *лпбиинпут*.</span><span class="sxs-lookup"><span data-stu-id="ce309-118">If *lpbiOutput* is nonzero, the driver should fill the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure with the default output format corresponding to the input format specified for *lpbiInput*.</span></span> <span data-ttu-id="ce309-119">Если программа сжатия может создать несколько форматов, то форматом по умолчанию должен быть тот, который сохраняет максимальный объем информации.</span><span class="sxs-lookup"><span data-stu-id="ce309-119">If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce309-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ce309-120">Requirements</span></span>



| <span data-ttu-id="ce309-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ce309-121">Requirement</span></span> | <span data-ttu-id="ce309-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ce309-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ce309-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce309-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ce309-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ce309-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ce309-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce309-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ce309-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ce309-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ce309-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ce309-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce309-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce309-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce309-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce309-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce309-130">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="ce309-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ce309-131">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="ce309-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

