---
title: Сообщение STM_SETIMAGE (Winuser. h)
description: Приложение отправляет \_ сообщение STM сетимаже, чтобы связать новый образ со статическим элементом управления.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- Элементы управления Windows для STM_SETIMAGE сообщений
topic_type:
- apiref
api_name:
- STM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27c4f9c216d2e987727a1e2fa9bc6de12a823d52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988324"
---
# <a name="stm_setimage-message"></a><span data-ttu-id="20245-104">\_Сообщение СЕТИМАЖЕ STM</span><span class="sxs-lookup"><span data-stu-id="20245-104">STM\_SETIMAGE message</span></span>

<span data-ttu-id="20245-105">Приложение отправляет сообщение **STM \_ сетимаже** , чтобы связать новый образ со статическим элементом управления.</span><span class="sxs-lookup"><span data-stu-id="20245-105">An application sends an **STM\_SETIMAGE** message to associate a new image with a static control.</span></span>

## <a name="parameters"></a><span data-ttu-id="20245-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="20245-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20245-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="20245-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20245-108">Указывает тип изображения, связываемого с статическим элементом управления.</span><span class="sxs-lookup"><span data-stu-id="20245-108">Specifies the type of image to associate with the static control.</span></span> <span data-ttu-id="20245-109">Этот параметр может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="20245-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="20245-110">Значение</span><span class="sxs-lookup"><span data-stu-id="20245-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="20245-111">Значение</span><span class="sxs-lookup"><span data-stu-id="20245-111">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="20245-112"><dt>**\_точечный рисунок изображения**</dt></span><span class="sxs-lookup"><span data-stu-id="20245-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl>                | <span data-ttu-id="20245-113">Массив.</span><span class="sxs-lookup"><span data-stu-id="20245-113">Bitmap.</span></span><br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <span data-ttu-id="20245-114"><dt>**\_курсор изображения**</dt></span><span class="sxs-lookup"><span data-stu-id="20245-114"><dt>**IMAGE\_CURSOR**</dt></span></span> </dl>                | <span data-ttu-id="20245-115">Набора.</span><span class="sxs-lookup"><span data-stu-id="20245-115">Cursor.</span></span><br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <span data-ttu-id="20245-116"><dt>**\_ЕНХМЕТАФИЛЕ изображения**</dt></span><span class="sxs-lookup"><span data-stu-id="20245-116"><dt>**IMAGE\_ENHMETAFILE**</dt></span></span> </dl> | <span data-ttu-id="20245-117">Расширенный метафайл.</span><span class="sxs-lookup"><span data-stu-id="20245-117">Enhanced metafile.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="20245-118"><dt>**\_значок изображения**</dt></span><span class="sxs-lookup"><span data-stu-id="20245-118"><dt>**IMAGE\_ICON**</dt></span></span> </dl>                      | <span data-ttu-id="20245-119">Значок.</span><span class="sxs-lookup"><span data-stu-id="20245-119">Icon.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="20245-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="20245-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20245-121">Обрабатывайте изображение, чтобы связать его со статическим элементом управления.</span><span class="sxs-lookup"><span data-stu-id="20245-121">Handle to the image to associate with the static control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20245-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20245-122">Return value</span></span>

<span data-ttu-id="20245-123">Возвращаемое значение является обработкой изображения, ранее связанного со статическим элементом управления, если таковой имеется; в противном случае он имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="20245-123">The return value is a handle to the image previously associated with the static control, if any; otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="20245-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20245-124">Remarks</span></span>

<span data-ttu-id="20245-125">Чтобы связать изображение со статическим элементом управления, элемент управления должен иметь соответствующий стиль.</span><span class="sxs-lookup"><span data-stu-id="20245-125">To associate an image with a static control, the control must have the proper style.</span></span> <span data-ttu-id="20245-126">В следующей таблице показан стиль, необходимый для каждого типа изображений.</span><span class="sxs-lookup"><span data-stu-id="20245-126">The following table shows the style needed for each image type.</span></span>



| <span data-ttu-id="20245-127">Тип образа</span><span class="sxs-lookup"><span data-stu-id="20245-127">Image type</span></span>         | <span data-ttu-id="20245-128">Статический стиль элемента управления</span><span class="sxs-lookup"><span data-stu-id="20245-128">Static control style</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="20245-129">\_точечный рисунок изображения</span><span class="sxs-lookup"><span data-stu-id="20245-129">IMAGE\_BITMAP</span></span>      | <span data-ttu-id="20245-130">\_Битовая карта SS</span><span class="sxs-lookup"><span data-stu-id="20245-130">SS\_BITMAP</span></span>           |
| <span data-ttu-id="20245-131">\_курсор изображения</span><span class="sxs-lookup"><span data-stu-id="20245-131">IMAGE\_CURSOR</span></span>      | <span data-ttu-id="20245-132">\_значок SS</span><span class="sxs-lookup"><span data-stu-id="20245-132">SS\_ICON</span></span>             |
| <span data-ttu-id="20245-133">\_ЕНХМЕТАФИЛЕ изображения</span><span class="sxs-lookup"><span data-stu-id="20245-133">IMAGE\_ENHMETAFILE</span></span> | <span data-ttu-id="20245-134">СС \_ енхметафиле</span><span class="sxs-lookup"><span data-stu-id="20245-134">SS\_ENHMETAFILE</span></span>      |
| <span data-ttu-id="20245-135">\_значок изображения</span><span class="sxs-lookup"><span data-stu-id="20245-135">IMAGE\_ICON</span></span>        | <span data-ttu-id="20245-136">\_значок SS</span><span class="sxs-lookup"><span data-stu-id="20245-136">SS\_ICON</span></span>             |



 

> [!IMPORTANT]
>
> <span data-ttu-id="20245-137">В версии 6 элементов управления Microsoft Win32 точечный рисунок, переданный в статический элемент управления с **помощью \_ сетимаже** -сообщения STM, был таким же, как и последующее сообщение **STM \_ сетимаже** .</span><span class="sxs-lookup"><span data-stu-id="20245-137">In version 6 of the Microsoft Win32 controls, a bitmap passed to a static control using the **STM\_SETIMAGE** message was the same bitmap returned by a subsequent **STM\_SETIMAGE** message.</span></span> <span data-ttu-id="20245-138">Клиент несет ответственность за удаление любого растрового изображения, отправленного в статический элемент управления.</span><span class="sxs-lookup"><span data-stu-id="20245-138">The client is responsible to delete any bitmap sent to a static control.</span></span>
>
> <span data-ttu-id="20245-139">В Windows XP, если точечный рисунок, переданный в **STM \_ сетимаже** Message, содержит Пиксели с ненулевой альфа-составляющей, статический элемент управления создает копию точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="20245-139">With Windows XP, if the bitmap passed in the **STM\_SETIMAGE** message contains pixels with nonzero alpha, the static control takes a copy of the bitmap.</span></span> <span data-ttu-id="20245-140">Этот скопированный точечный рисунок возвращается следующим сообщением **STM \_ сетимаже** .</span><span class="sxs-lookup"><span data-stu-id="20245-140">This copied bitmap is returned by the next **STM\_SETIMAGE** message.</span></span> <span data-ttu-id="20245-141">Клиентский код может независимо отслеживаниь точечных рисунков, переданных в статический элемент управления, но если он не проверяет и не освобождает растровые изображения, возвращенные из **\_ Сетимаже сообщений STM** , точечные рисунки будут утеряны.</span><span class="sxs-lookup"><span data-stu-id="20245-141">The client code may independently track the bitmaps passed to the static control, but if it does not check and release the bitmaps returned from **STM\_SETIMAGE** messages, the bitmaps are leaked.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="20245-142">Требования</span><span class="sxs-lookup"><span data-stu-id="20245-142">Requirements</span></span>



| <span data-ttu-id="20245-143">Требование</span><span class="sxs-lookup"><span data-stu-id="20245-143">Requirement</span></span> | <span data-ttu-id="20245-144">Значение</span><span class="sxs-lookup"><span data-stu-id="20245-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20245-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20245-145">Minimum supported client</span></span><br/> | <span data-ttu-id="20245-146">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20245-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="20245-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20245-147">Minimum supported server</span></span><br/> | <span data-ttu-id="20245-148">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="20245-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="20245-149">Header</span><span class="sxs-lookup"><span data-stu-id="20245-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="20245-150"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20245-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20245-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20245-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20245-152">**STM, \_ образ**</span><span class="sxs-lookup"><span data-stu-id="20245-152">**STM\_GETIMAGE**</span></span>](stm-getimage.md)
</dt> </dl>

 

 





