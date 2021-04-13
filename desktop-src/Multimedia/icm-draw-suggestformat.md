---
title: Сообщение ICM_DRAW_SUGGESTFORMAT (VFW. h)
description: Сообщение ICM \_ Draw \_ сугжестформат запрашивает драйвер подготовки к просмотру, чтобы предложить формат, который может нарисоваться в распакованном формате.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- ICM_DRAW_SUGGESTFORMAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_SUGGESTFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97c8782b16336427b3832f36b5a06987399df1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489594"
---
# <a name="icm_draw_suggestformat-message"></a><span data-ttu-id="89b3c-104">\_Сообщение ICM Draw \_ сугжестформат</span><span class="sxs-lookup"><span data-stu-id="89b3c-104">ICM\_DRAW\_SUGGESTFORMAT message</span></span>

<span data-ttu-id="89b3c-105">Сообщение **ICM \_ Draw \_ сугжестформат** запрашивает драйвер подготовки к просмотру, чтобы предложить формат, который может нарисоваться в распакованном формате.</span><span class="sxs-lookup"><span data-stu-id="89b3c-105">The **ICM\_DRAW\_SUGGESTFORMAT** message queries a rendering driver to suggest a decompressed format that it can draw.</span></span>


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a><span data-ttu-id="89b3c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="89b3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89b3c-107"><span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*икдрвсугжест*</span><span class="sxs-lookup"><span data-stu-id="89b3c-107"><span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*</span></span>
</dt> <dd>

<span data-ttu-id="89b3c-108">Указатель на структуру [**икдравсугжест**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) .</span><span class="sxs-lookup"><span data-stu-id="89b3c-108">Pointer to an [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure.</span></span>

</dd> <dt>

<span data-ttu-id="89b3c-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="89b3c-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="89b3c-110">Размер [**икдравсугжест**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)в байтах.</span><span class="sxs-lookup"><span data-stu-id="89b3c-110">Size, in bytes, of [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89b3c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89b3c-111">Return Value</span></span>

<span data-ttu-id="89b3c-112">Возвращает ИЦЕРР \_ ОК в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="89b3c-112">Returns ICERR\_OK if successful.</span></span> <span data-ttu-id="89b3c-113">Если элемент **лпбисугжест** структуры [**Икдравсугжест**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) имеет **значение NULL**, это сообщение возвращает объем памяти, необходимый для хранения рекомендуемого формата.</span><span class="sxs-lookup"><span data-stu-id="89b3c-113">If the **lpbiSuggest** member of the [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure is **NULL**, this message returns the amount of memory required to contain the suggested format.</span></span>

## <a name="remarks"></a><span data-ttu-id="89b3c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89b3c-114">Remarks</span></span>

<span data-ttu-id="89b3c-115">Драйвер должен проверить формат, указанный в элементе **лпбиин** структуры [**икдравсугжест**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) , и использовать элемент **лпбисугжест** для возврата формата, который он может нарисовать.</span><span class="sxs-lookup"><span data-stu-id="89b3c-115">The driver should examine the format specified in the **lpbiIn** member of the [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure and use the **lpbiSuggest** member to return a format it can draw.</span></span> <span data-ttu-id="89b3c-116">Формат вывода должен сохранять как можно больше данных из входного формата.</span><span class="sxs-lookup"><span data-stu-id="89b3c-116">The output format should preserve as much data as possible from the input format.</span></span>

<span data-ttu-id="89b3c-117">При необходимости драйвер может использовать установщик, который можно установить, переданный в члене **Хикдекомпрессор** [**икдравсугжест**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) , чтобы сделать более сложными выборки.</span><span class="sxs-lookup"><span data-stu-id="89b3c-117">Optionally, the driver can use the installable compressor handle passed in the **hicDecompressor** member of [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) to make more complex selections.</span></span> <span data-ttu-id="89b3c-118">Например, если входной формат имеет 24 бита данных в формате JPEG, модуль подготовки отчетов может запросить декомпрессор, чтобы выяснить, может ли он распаковать его в формат YUV (который может быть более эффективным), прежде чем выбирать нужный формат.</span><span class="sxs-lookup"><span data-stu-id="89b3c-118">For example, if the input format is 24-bit JPEG data, a renderer could query the decompressor to find out if it can decompress to a YUV format (which might be drawn more efficiently) before selecting the format to suggest.</span></span>

## <a name="requirements"></a><span data-ttu-id="89b3c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="89b3c-119">Requirements</span></span>



| <span data-ttu-id="89b3c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="89b3c-120">Requirement</span></span> | <span data-ttu-id="89b3c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="89b3c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="89b3c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89b3c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="89b3c-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="89b3c-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="89b3c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89b3c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="89b3c-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="89b3c-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="89b3c-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="89b3c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="89b3c-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="89b3c-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89b3c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89b3c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b3c-129">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="89b3c-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="89b3c-130">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="89b3c-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





