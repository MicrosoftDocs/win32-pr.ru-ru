---
title: Сообщение ICM_DECOMPRESS_GET_PALETTE (VFW. h)
description: Сообщение ICM \_ распаковка \_ Получение \_ палитры требует, чтобы драйвер распаковки видео предоставил таблицу цветов для выходной структуры битмапинфохеадер. Это сообщение можно отправить явно или с помощью макроса Икдекомпрессжетпалетте.
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- ICM_DECOMPRESS_GET_PALETTE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6255ea99b9177819dee6d227c45d2229deab57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672801"
---
# <a name="icm_decompress_get_palette-message"></a><span data-ttu-id="99a76-105">ICM \_ распаковка \_ Получение \_ сообщения палитры</span><span class="sxs-lookup"><span data-stu-id="99a76-105">ICM\_DECOMPRESS\_GET\_PALETTE message</span></span>

<span data-ttu-id="99a76-106">Сообщение **ICM \_ распаковка \_ Получение \_ палитры** требует, чтобы драйвер распаковки видео предоставил таблицу цветов для выходной структуры [**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="99a76-106">The **ICM\_DECOMPRESS\_GET\_PALETTE** message requests that the video decompression driver supply the color table of the output [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure.</span></span> <span data-ttu-id="99a76-107">Это сообщение можно отправить явно или с помощью макроса [**икдекомпрессжетпалетте**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="99a76-107">You can send this message explicitly or by using the [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) macro.</span></span>


```C++
ICM_DECOMPRESS_GET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="99a76-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="99a76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99a76-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*лпбиинпут*</span><span class="sxs-lookup"><span data-stu-id="99a76-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="99a76-110">Указатель на структуру [**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85)) , содержащую входной формат.</span><span class="sxs-lookup"><span data-stu-id="99a76-110">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="99a76-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*лпбиаутпут*</span><span class="sxs-lookup"><span data-stu-id="99a76-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="99a76-112">Указатель на структуру [**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85)) , в которой будет содержаться таблица цветов.</span><span class="sxs-lookup"><span data-stu-id="99a76-112">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure to contain the color table.</span></span> <span data-ttu-id="99a76-113">Пространство, зарезервированное для таблицы цветов, всегда имеет по крайней мере 256 цветов.</span><span class="sxs-lookup"><span data-stu-id="99a76-113">The space reserved for the color table is always at least 256 colors.</span></span> <span data-ttu-id="99a76-114">Для этого параметра можно указать ноль, чтобы возвращался только размер таблицы цветов.</span><span class="sxs-lookup"><span data-stu-id="99a76-114">You can specify zero for this parameter to return only the size of the color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99a76-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99a76-115">Return Value</span></span>

<span data-ttu-id="99a76-116">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="99a76-116">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="99a76-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99a76-117">Remarks</span></span>

<span data-ttu-id="99a76-118">Если *лпбиаутпут* имеет ненулевое значение, драйвер устанавливает для элемента **биклрусед** в [**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85)) число цветов в таблице цветов.</span><span class="sxs-lookup"><span data-stu-id="99a76-118">If *lpbiOutput* is nonzero, the driver sets the **biClrUsed** member of [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) to the number of colors in the color table.</span></span> <span data-ttu-id="99a76-119">Драйвер заполняет элемент **бмиколорс** в [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) на реальные цвета.</span><span class="sxs-lookup"><span data-stu-id="99a76-119">The driver fills the **bmiColors** member of [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) with the actual colors.</span></span>

<span data-ttu-id="99a76-120">Драйвер должен поддерживать это сообщение только в том случае, если используется палитра, отличная от указанной во входном формате.</span><span class="sxs-lookup"><span data-stu-id="99a76-120">The driver should support this message only if it uses a palette other than the one specified in the input format.</span></span>

## <a name="requirements"></a><span data-ttu-id="99a76-121">Требования</span><span class="sxs-lookup"><span data-stu-id="99a76-121">Requirements</span></span>



| <span data-ttu-id="99a76-122">Требование</span><span class="sxs-lookup"><span data-stu-id="99a76-122">Requirement</span></span> | <span data-ttu-id="99a76-123">Значение</span><span class="sxs-lookup"><span data-stu-id="99a76-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="99a76-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99a76-124">Minimum supported client</span></span><br/> | <span data-ttu-id="99a76-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="99a76-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="99a76-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99a76-126">Minimum supported server</span></span><br/> | <span data-ttu-id="99a76-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="99a76-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="99a76-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="99a76-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="99a76-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="99a76-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99a76-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99a76-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99a76-131">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="99a76-131">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="99a76-132">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="99a76-132">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

