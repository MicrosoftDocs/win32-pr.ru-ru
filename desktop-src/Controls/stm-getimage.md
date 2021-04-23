---
title: Сообщение STM_GETIMAGE (Winuser. h)
description: Приложение отправляет сообщение STM- \_ Image для получения маркера изображения (значка или точечного рисунка), связанного со статическим элементом управления.
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- Элементы управления Windows для STM_GETIMAGE сообщений
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071177"
---
# <a name="stm_getimage-message"></a><span data-ttu-id="2b6e0-104">\_Сообщение STM</span><span class="sxs-lookup"><span data-stu-id="2b6e0-104">STM\_GETIMAGE message</span></span>

<span data-ttu-id="2b6e0-105">Приложение отправляет сообщение **STM- \_ Image** для получения маркера изображения (значка или точечного рисунка), связанного со статическим элементом управления.</span><span class="sxs-lookup"><span data-stu-id="2b6e0-105">An application sends an **STM\_GETIMAGE** message to retrieve a handle to the image (icon or bitmap) associated with a static control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b6e0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b6e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b6e0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b6e0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b6e0-108">Указывает тип извлекаемого изображения.</span><span class="sxs-lookup"><span data-stu-id="2b6e0-108">Specifies the type of image to retrieve.</span></span> <span data-ttu-id="2b6e0-109">Этот параметр может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2b6e0-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="2b6e0-110">Значение</span><span class="sxs-lookup"><span data-stu-id="2b6e0-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="2b6e0-111">Значение</span><span class="sxs-lookup"><span data-stu-id="2b6e0-111">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="2b6e0-112"><dt>**\_точечный рисунок изображения**</dt></span><span class="sxs-lookup"><span data-stu-id="2b6e0-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl>                | <span data-ttu-id="2b6e0-113">Массив.</span><span class="sxs-lookup"><span data-stu-id="2b6e0-113">Bitmap.</span></span><br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <span data-ttu-id="2b6e0-114"><dt>**\_курсор изображения**</dt></span><span class="sxs-lookup"><span data-stu-id="2b6e0-114"><dt>**IMAGE\_CURSOR**</dt></span></span> </dl>                | <span data-ttu-id="2b6e0-115">Набора.</span><span class="sxs-lookup"><span data-stu-id="2b6e0-115">Cursor.</span></span><br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <span data-ttu-id="2b6e0-116"><dt>**\_ЕНХМЕТАФИЛЕ изображения**</dt></span><span class="sxs-lookup"><span data-stu-id="2b6e0-116"><dt>**IMAGE\_ENHMETAFILE**</dt></span></span> </dl> | <span data-ttu-id="2b6e0-117">Расширенный метафайл.</span><span class="sxs-lookup"><span data-stu-id="2b6e0-117">Enhanced metafile.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="2b6e0-118"><dt>**\_значок изображения**</dt></span><span class="sxs-lookup"><span data-stu-id="2b6e0-118"><dt>**IMAGE\_ICON**</dt></span></span> </dl>                      | <span data-ttu-id="2b6e0-119">Значок.</span><span class="sxs-lookup"><span data-stu-id="2b6e0-119">Icon.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="2b6e0-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b6e0-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b6e0-121">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="2b6e0-121">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b6e0-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b6e0-122">Return value</span></span>

<span data-ttu-id="2b6e0-123">Возвращаемое значение — это обработчик изображения, если таковой имеется; в противном случае он имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2b6e0-123">The return value is a handle to the image, if any; otherwise, it is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b6e0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2b6e0-124">Requirements</span></span>



| <span data-ttu-id="2b6e0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2b6e0-125">Requirement</span></span> | <span data-ttu-id="2b6e0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2b6e0-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6e0-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b6e0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2b6e0-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b6e0-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2b6e0-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b6e0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2b6e0-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2b6e0-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2b6e0-131">Header</span><span class="sxs-lookup"><span data-stu-id="2b6e0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b6e0-132"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b6e0-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b6e0-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b6e0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b6e0-134">**STM \_ сетимаже**</span><span class="sxs-lookup"><span data-stu-id="2b6e0-134">**STM\_SETIMAGE**</span></span>](stm-setimage.md)
</dt> </dl>

 

 





