---
title: Сообщение ICM_DRAW_BEGIN (VFW. h)
description: '\_ \_ Сообщение о начале ICM Draw уведомляет драйвер подготовки, чтобы подготовиться к прорисовке данных.'
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- ICM_DRAW_BEGIN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db7b9e20a0b0621038e1c7e092a871a6727566cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989158"
---
# <a name="icm_draw_begin-message"></a><span data-ttu-id="a95f3-104">\_Сообщение начала прорисовки ICM \_</span><span class="sxs-lookup"><span data-stu-id="a95f3-104">ICM\_DRAW\_BEGIN message</span></span>

<span data-ttu-id="a95f3-105">Сообщение **о \_ \_ начале ICM Draw** уведомляет драйвер подготовки, чтобы подготовиться к прорисовке данных.</span><span class="sxs-lookup"><span data-stu-id="a95f3-105">The **ICM\_DRAW\_BEGIN** message notifies a rendering driver to prepare to draw data.</span></span>


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a><span data-ttu-id="a95f3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a95f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a95f3-107"><span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*икдрвбгн*</span><span class="sxs-lookup"><span data-stu-id="a95f3-107"><span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*</span></span>
</dt> <dd>

<span data-ttu-id="a95f3-108">Указатель на структуру [**икдравбегин**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) , содержащую входной формат.</span><span class="sxs-lookup"><span data-stu-id="a95f3-108">Pointer to an [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="a95f3-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="a95f3-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="a95f3-110">Размер **икдравбегин** в байтах.</span><span class="sxs-lookup"><span data-stu-id="a95f3-110">Size, in bytes, of **ICDRAWBEGIN**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a95f3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a95f3-111">Return Value</span></span>

<span data-ttu-id="a95f3-112">Возвращает ИЦЕРР \_ ОК, если драйвер поддерживает отображение данных на экране с указанными форматом или с кодом ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a95f3-112">Returns ICERR\_OK if the driver supports drawing the data to the screen in the specified manner and format, or an error code otherwise.</span></span> <span data-ttu-id="a95f3-113">Возможные значения ошибок включают следующее.</span><span class="sxs-lookup"><span data-stu-id="a95f3-113">Possible error values include the following.</span></span>



| <span data-ttu-id="a95f3-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a95f3-114">Value</span></span>               | <span data-ttu-id="a95f3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a95f3-115">Meaning</span></span>                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="a95f3-116">ИЦЕРР \_ бадформат</span><span class="sxs-lookup"><span data-stu-id="a95f3-116">ICERR\_BADFORMAT</span></span>    | <span data-ttu-id="a95f3-117">Формат ввода или вывода не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a95f3-117">Input or output format is not supported.</span></span>                                      |
| <span data-ttu-id="a95f3-118">ИЦЕРР \_ NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="a95f3-118">ICERR\_NOTSUPPORTED</span></span> | <span data-ttu-id="a95f3-119">Драйвер не рисуется непосредственно на экране или не поддерживает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="a95f3-119">Driver does not draw directly to the screen or does not support this message.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a95f3-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a95f3-120">Remarks</span></span>

<span data-ttu-id="a95f3-121">Если требуется, чтобы драйвер распаковать данные в буфер, отправьте сообщение [**\_ \_ Begin распаковки**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="a95f3-121">If you want the driver to decompress data into a buffer, send the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="a95f3-122">**\_ \_ Начало** и [**\_ \_ конец**](icm-draw-end.md) изображения ICM не вложены в сообщения.</span><span class="sxs-lookup"><span data-stu-id="a95f3-122">The **ICM\_DRAW\_BEGIN** and [**ICM\_DRAW\_END**](icm-draw-end.md) messages do not nest.</span></span> <span data-ttu-id="a95f3-123">Если драйвер получает функцию **ICM \_ Draw \_** , то перед **\_ \_ завершением** распаковки с использованием ICM Draw необходимо перезапустить распаковку с новыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="a95f3-123">If your driver receives **ICM\_DRAW\_BEGIN** before decompression is stopped with **ICM\_DRAW\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a95f3-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a95f3-124">Requirements</span></span>



| <span data-ttu-id="a95f3-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a95f3-125">Requirement</span></span> | <span data-ttu-id="a95f3-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a95f3-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a95f3-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a95f3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a95f3-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a95f3-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a95f3-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a95f3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a95f3-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a95f3-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a95f3-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a95f3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a95f3-132"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a95f3-132"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a95f3-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a95f3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a95f3-134">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="a95f3-134">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a95f3-135">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="a95f3-135">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





