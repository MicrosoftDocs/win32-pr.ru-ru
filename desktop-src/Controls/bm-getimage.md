---
title: Сообщение BM_GETIMAGE (Winuser. h)
description: Извлекает маркер изображения (значок или растровое изображение), связанного с кнопкой.
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- Элементы управления Windows для BM_GETIMAGE сообщений
topic_type:
- apiref
api_name:
- BM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9319f5310b40ff76a011e1a06b2be1d41be611f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340970"
---
# <a name="bm_getimage-message"></a><span data-ttu-id="d29a3-104">BM, \_ сообщение о СОобразе</span><span class="sxs-lookup"><span data-stu-id="d29a3-104">BM\_GETIMAGE message</span></span>

<span data-ttu-id="d29a3-105">Извлекает маркер изображения (значок или растровое изображение), связанного с кнопкой.</span><span class="sxs-lookup"><span data-stu-id="d29a3-105">Retrieves a handle to the image (icon or bitmap) associated with the button.</span></span>

## <a name="parameters"></a><span data-ttu-id="d29a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d29a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d29a3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d29a3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d29a3-108">Тип изображения, связываемого с кнопкой.</span><span class="sxs-lookup"><span data-stu-id="d29a3-108">The type of image to associate with the button.</span></span> <span data-ttu-id="d29a3-109">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="d29a3-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d29a3-110">Значение</span><span class="sxs-lookup"><span data-stu-id="d29a3-110">Value</span></span>                                                                                                                                                      | <span data-ttu-id="d29a3-111">Значение</span><span class="sxs-lookup"><span data-stu-id="d29a3-111">Meaning</span></span>              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="d29a3-112"><dt>**\_точечный рисунок изображения**</dt></span><span class="sxs-lookup"><span data-stu-id="d29a3-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl> | <span data-ttu-id="d29a3-113">Точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="d29a3-113">A bitmap.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="d29a3-114"><dt>**\_значок изображения**</dt></span><span class="sxs-lookup"><span data-stu-id="d29a3-114"><dt>**IMAGE\_ICON**</dt></span></span> </dl>       | <span data-ttu-id="d29a3-115">Значок.</span><span class="sxs-lookup"><span data-stu-id="d29a3-115">An icon.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="d29a3-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d29a3-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d29a3-117">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="d29a3-117">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d29a3-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d29a3-118">Return value</span></span>

<span data-ttu-id="d29a3-119">Возвращаемое значение — это обработчик изображения, если таковой имеется; в противном случае он имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d29a3-119">The return value is a handle to the image, if any; otherwise, it is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d29a3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d29a3-120">Requirements</span></span>



| <span data-ttu-id="d29a3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d29a3-121">Requirement</span></span> | <span data-ttu-id="d29a3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d29a3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d29a3-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d29a3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d29a3-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d29a3-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d29a3-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d29a3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d29a3-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d29a3-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d29a3-127">Header</span><span class="sxs-lookup"><span data-stu-id="d29a3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d29a3-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d29a3-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d29a3-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d29a3-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="d29a3-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d29a3-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d29a3-131">**BM \_ сетимаже**</span><span class="sxs-lookup"><span data-stu-id="d29a3-131">**BM\_SETIMAGE**</span></span>](bm-setimage.md)
</dt> <dt>

<span data-ttu-id="d29a3-132">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="d29a3-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d29a3-133">Кнопки</span><span class="sxs-lookup"><span data-stu-id="d29a3-133">Buttons</span></span>](buttons.md)
</dt> </dl>

 

 





