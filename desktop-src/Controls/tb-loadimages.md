---
title: Сообщение TB_LOADIMAGES (Коммктрл. h)
description: Загружает определенные системой изображения кнопок в список изображений элемента управления ToolBar.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- Элементы управления Windows для TB_LOADIMAGES сообщений
topic_type:
- apiref
api_name:
- TB_LOADIMAGES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0ba6bf75855a0b81ac56438489d7eced3d589
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491982"
---
# <a name="tb_loadimages-message"></a><span data-ttu-id="b8186-104">\_Сообщение ЛОАДИМАЖЕС ТБ</span><span class="sxs-lookup"><span data-stu-id="b8186-104">TB\_LOADIMAGES message</span></span>

<span data-ttu-id="b8186-105">Загружает определенные системой изображения кнопок в список изображений элемента управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="b8186-105">Loads system-defined button images into a toolbar control's image list.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8186-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8186-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8186-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8186-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8186-108">Идентификатор определяемого системой списка изображений для кнопки.</span><span class="sxs-lookup"><span data-stu-id="b8186-108">Identifier of a system-defined button image list.</span></span> <span data-ttu-id="b8186-109">Этому параметру можно присвоить одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b8186-109">This parameter can be set to one of the following values.</span></span>



| <span data-ttu-id="b8186-110">Значение</span><span class="sxs-lookup"><span data-stu-id="b8186-110">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="b8186-111">Значение</span><span class="sxs-lookup"><span data-stu-id="b8186-111">Meaning</span></span>                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <span data-ttu-id="b8186-112"><dt>**IDB \_ хист, \_ крупный \_ Цвет**</dt></span><span class="sxs-lookup"><span data-stu-id="b8186-112"><dt>**IDB\_HIST\_LARGE\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="b8186-113">Точечные рисунки проводника имеют большой размер.</span><span class="sxs-lookup"><span data-stu-id="b8186-113">Windows Explorer bitmaps in large size.</span></span><br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <span data-ttu-id="b8186-114"><dt>**IDB \_ хист \_ мелкий \_ Цвет**</dt></span><span class="sxs-lookup"><span data-stu-id="b8186-114"><dt>**IDB\_HIST\_SMALL\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="b8186-115">Точечные рисунки проводника Windows небольшого размера.</span><span class="sxs-lookup"><span data-stu-id="b8186-115">Windows Explorer bitmaps in small size.</span></span><br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <span data-ttu-id="b8186-116"><dt>**нестандартные IDB — \_ \_ крупный \_ Цвет**</dt></span><span class="sxs-lookup"><span data-stu-id="b8186-116"><dt>**IDB\_STD\_LARGE\_COLOR**</dt></span></span> </dl>    | <span data-ttu-id="b8186-117">Стандартные точечные рисунки имеют большой размер.</span><span class="sxs-lookup"><span data-stu-id="b8186-117">Standard bitmaps in large size.</span></span><br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <span data-ttu-id="b8186-118"><dt>**неплашечный IDB по \_ \_ небольшому \_ цвету**</dt></span><span class="sxs-lookup"><span data-stu-id="b8186-118"><dt>**IDB\_STD\_SMALL\_COLOR**</dt></span></span> </dl>    | <span data-ttu-id="b8186-119">Стандартные точечные рисунки небольшого размера.</span><span class="sxs-lookup"><span data-stu-id="b8186-119">Standard bitmaps in small size.</span></span><br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <span data-ttu-id="b8186-120"><dt>**\_ \_ крупный цвет представления \_ IDB**</dt></span><span class="sxs-lookup"><span data-stu-id="b8186-120"><dt>**IDB\_VIEW\_LARGE\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="b8186-121">Просмотр точечных рисунков в большом размере.</span><span class="sxs-lookup"><span data-stu-id="b8186-121">View bitmaps in large size.</span></span><br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <span data-ttu-id="b8186-122"><dt>**\_ \_ малый цвет представления \_ IDB**</dt></span><span class="sxs-lookup"><span data-stu-id="b8186-122"><dt>**IDB\_VIEW\_SMALL\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="b8186-123">Просмотр точечных рисунков в небольшом размере.</span><span class="sxs-lookup"><span data-stu-id="b8186-123">View bitmaps in small size.</span></span><br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <span data-ttu-id="b8186-124"><dt>**IDB \_ хист, \_ Обычная**</dt></span><span class="sxs-lookup"><span data-stu-id="b8186-124"><dt>**IDB\_HIST\_NORMAL**</dt></span></span> </dl>                 | <span data-ttu-id="b8186-125">Проводник Windows кнопки перемещения и избранные рисунки в нормальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b8186-125">Windows Explorer travel buttons and favorites bitmaps in normal state.</span></span><br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <span data-ttu-id="b8186-126"><dt>**IDB \_ хист \_ Hot**</dt></span><span class="sxs-lookup"><span data-stu-id="b8186-126"><dt>**IDB\_HIST\_HOT**</dt></span></span> </dl>                          | <span data-ttu-id="b8186-127">Кнопки перемещения в проводнике Windows и избранные рисунки в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b8186-127">Windows Explorer travel buttons and favorites bitmaps in hot state.</span></span><br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <span data-ttu-id="b8186-128"><dt>**IDB \_ хист \_ отключена**</dt></span><span class="sxs-lookup"><span data-stu-id="b8186-128"><dt>**IDB\_HIST\_DISABLED**</dt></span></span> </dl>           | <span data-ttu-id="b8186-129">Кнопки перемещения в проводнике Windows и избранные рисунки в отключенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b8186-129">Windows Explorer travel buttons and favorites bitmaps in disabled state.</span></span><br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <span data-ttu-id="b8186-130"><dt>**\_ХИСТ IDB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8186-130"><dt>**IDB\_HIST\_PRESSED**</dt></span></span> </dl>              | <span data-ttu-id="b8186-131">Кнопки перемещения в проводнике Windows и избранные растровые изображения в нажатом состоянии.</span><span class="sxs-lookup"><span data-stu-id="b8186-131">Windows Explorer travel buttons and favorites bitmaps in pressed state.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="b8186-132">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8186-132">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8186-133">Маркер экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b8186-133">Instance handle.</span></span> <span data-ttu-id="b8186-134">Этот параметр должен иметь значение ХИНСТ \_ коммктрл.</span><span class="sxs-lookup"><span data-stu-id="b8186-134">This parameter must be set to HINST\_COMMCTRL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8186-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8186-135">Return value</span></span>

<span data-ttu-id="b8186-136">Число изображений в списке изображений.</span><span class="sxs-lookup"><span data-stu-id="b8186-136">The count of images in the image list.</span></span> <span data-ttu-id="b8186-137">Возвращает нуль, если на панели инструментов нет списка изображений или если существующий список изображений пуст.</span><span class="sxs-lookup"><span data-stu-id="b8186-137">Returns zero if the toolbar has no image list or if the existing image list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8186-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8186-138">Remarks</span></span>

<span data-ttu-id="b8186-139">При подготовке структур [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) перед отправкой сообщения [**\_ аддбуттонс ТБ**](tb-addbuttons.md) необходимо использовать правильные значения индекса образа.</span><span class="sxs-lookup"><span data-stu-id="b8186-139">You must use the proper image index values when you prepare [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structures prior to sending the [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span> <span data-ttu-id="b8186-140">Список значений индекса изображений для этих предустановленных точечных рисунков см. в разделе [значения индекса изображения стандартной кнопки панели инструментов](toolbar-standard-button-image-index-values.md).</span><span class="sxs-lookup"><span data-stu-id="b8186-140">For a list of image index values for these preset bitmaps, see [Toolbar Standard Button Image Index Values](toolbar-standard-button-image-index-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b8186-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="b8186-141">Examples</span></span>

<span data-ttu-id="b8186-142">В следующем примере кода загружаются системные изображения с мелкими цветами.</span><span class="sxs-lookup"><span data-stu-id="b8186-142">The following sample code loads the system standard small color images.</span></span>


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a><span data-ttu-id="b8186-143">Требования</span><span class="sxs-lookup"><span data-stu-id="b8186-143">Requirements</span></span>



| <span data-ttu-id="b8186-144">Требование</span><span class="sxs-lookup"><span data-stu-id="b8186-144">Requirement</span></span> | <span data-ttu-id="b8186-145">Значение</span><span class="sxs-lookup"><span data-stu-id="b8186-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8186-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8186-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b8186-147">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8186-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8186-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8186-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b8186-149">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8186-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8186-150">Header</span><span class="sxs-lookup"><span data-stu-id="b8186-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8186-151"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8186-151"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8186-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8186-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8186-153">**\_АДДБИТМАП ТБ**</span><span class="sxs-lookup"><span data-stu-id="b8186-153">**TB\_ADDBITMAP**</span></span>](tb-addbitmap.md)
</dt> </dl>

 

 





