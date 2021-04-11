---
title: Сообщение LVM_SETCALLBACKMASK (Коммктрл. h)
description: Изменяет маску обратного вызова для элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Сеткаллбаккмаск ListView.
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- Элементы управления Windows для LVM_SETCALLBACKMASK сообщений
topic_type:
- apiref
api_name:
- LVM_SETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef6dd46228c4e4aeada30f469a77f9e67aff3a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135598"
---
# <a name="lvm_setcallbackmask-message"></a><span data-ttu-id="f7083-105">\_Сообщение LVM сеткаллбаккмаск</span><span class="sxs-lookup"><span data-stu-id="f7083-105">LVM\_SETCALLBACKMASK message</span></span>

<span data-ttu-id="f7083-106">Изменяет маску обратного вызова для элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="f7083-106">Changes the callback mask for a list-view control.</span></span> <span data-ttu-id="f7083-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сеткаллбаккмаск ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) .</span><span class="sxs-lookup"><span data-stu-id="f7083-107">You can send this message explicitly or by using the [**ListView\_SetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7083-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7083-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7083-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7083-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7083-110">Значение маски обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f7083-110">Value of the callback mask.</span></span> <span data-ttu-id="f7083-111">Биты маски указывают состояния или изображения элементов, для которых приложение хранит текущие данные о состоянии.</span><span class="sxs-lookup"><span data-stu-id="f7083-111">The bits of the mask indicate the item states or images for which the application stores the current state data.</span></span> <span data-ttu-id="f7083-112">Это значение может быть любым сочетанием следующих констант:</span><span class="sxs-lookup"><span data-stu-id="f7083-112">This value can be any combination of the following constants:</span></span>



| <span data-ttu-id="f7083-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f7083-113">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="f7083-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f7083-114">Meaning</span></span>                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="f7083-115"><dt>**ЛВИС \_ Вырезать**</dt></span><span class="sxs-lookup"><span data-stu-id="f7083-115"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="f7083-116">Элемент помечен для операции вырезания и вставки.</span><span class="sxs-lookup"><span data-stu-id="f7083-116">The item is marked for a cut-and-paste operation.</span></span><br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="f7083-117"><dt>**ЛВИС \_ дрофилитед**</dt></span><span class="sxs-lookup"><span data-stu-id="f7083-117"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="f7083-118">Элемент выделяется как цель перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="f7083-118">The item is highlighted as a drag-and-drop target.</span></span><br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="f7083-119"><dt>**ЛВИС \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f7083-119"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="f7083-120">Элемент находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="f7083-120">The item has the focus.</span></span><br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="f7083-121"><dt>**ЛВИС \_ выбрано**</dt></span><span class="sxs-lookup"><span data-stu-id="f7083-121"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="f7083-122">Элемент выбран.</span><span class="sxs-lookup"><span data-stu-id="f7083-122">The item is selected.</span></span> <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="f7083-123"><dt>**ЛВИС \_ оверлаймаск**</dt></span><span class="sxs-lookup"><span data-stu-id="f7083-123"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="f7083-124">Приложение сохраняет индекс списка изображений текущего наложенного изображения для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="f7083-124">The application stores the image list index of the current overlay image for each item.</span></span><br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="f7083-125"><dt>**ЛВИС \_ статеимажемаск**</dt></span><span class="sxs-lookup"><span data-stu-id="f7083-125"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="f7083-126">Приложение сохраняет индекс списка изображений текущего состояния для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="f7083-126">The application stores the image list index of the current state image for each item.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="f7083-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7083-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f7083-128">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="f7083-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7083-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7083-129">Return value</span></span>

<span data-ttu-id="f7083-130">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f7083-130">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7083-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7083-131">Remarks</span></span>

<span data-ttu-id="f7083-132">*Маска обратного вызова* элемента управления "представление списка" представляет собой набор битовых флагов, указывающих состояния элементов, для которых приложение, а не элемент управления, сохраняет текущие данные.</span><span class="sxs-lookup"><span data-stu-id="f7083-132">The *callback mask* of a list-view control is a set of bit flags that specify the item states for which the application, rather than the control, stores the current data.</span></span> <span data-ttu-id="f7083-133">Маска обратного вызова применяется ко всем элементам элемента управления, в отличие от конструкции элемента обратного вызова, которая применяется к конкретному элементу.</span><span class="sxs-lookup"><span data-stu-id="f7083-133">The callback mask applies to all of the control's items, unlike the callback item designation, which applies to a specific item.</span></span> <span data-ttu-id="f7083-134">По умолчанию маска обратного вызова равна нулю, то есть элемент управления "список" хранит все сведения о состоянии элемента.</span><span class="sxs-lookup"><span data-stu-id="f7083-134">The callback mask is zero by default, meaning that the list-view control stores all item state information.</span></span> <span data-ttu-id="f7083-135">После создания элемента управления "представление списка" и инициализации его элементов можно отправить сообщение **LVM \_ сеткаллбаккмаск** , чтобы изменить маску обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f7083-135">After creating a list-view control and initializing its items, you can send the **LVM\_SETCALLBACKMASK** message to change the callback mask.</span></span> <span data-ttu-id="f7083-136">Чтобы получить текущую маску обратного вызова, отправьте сообщение [**LVM \_ жеткаллбаккмаск**](lvm-getcallbackmask.md) .</span><span class="sxs-lookup"><span data-stu-id="f7083-136">To retrieve the current callback mask, send the [**LVM\_GETCALLBACKMASK**](lvm-getcallbackmask.md) message.</span></span>

<span data-ttu-id="f7083-137">Дополнительные сведения о изображениях наложения и изображениях состояний см. в разделе [добавление List-View списков изображений](using-list-view-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f7083-137">For more information about overlay images and state images, see [Adding List-View Image Lists](using-list-view-controls.md).</span></span>

<span data-ttu-id="f7083-138">Дополнительные сведения о обратных вызовах в представлении списка см. [в разделе элементы обратного вызова и маска обратного вызова](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f7083-138">For more information on list-view callbacks, see [Callback Items and the Callback Mask](list-view-controls-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7083-139">Требования</span><span class="sxs-lookup"><span data-stu-id="f7083-139">Requirements</span></span>



| <span data-ttu-id="f7083-140">Требование</span><span class="sxs-lookup"><span data-stu-id="f7083-140">Requirement</span></span> | <span data-ttu-id="f7083-141">Значение</span><span class="sxs-lookup"><span data-stu-id="f7083-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7083-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7083-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f7083-143">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7083-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7083-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7083-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f7083-145">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f7083-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7083-146">Header</span><span class="sxs-lookup"><span data-stu-id="f7083-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7083-147"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7083-147"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7083-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7083-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7083-149">**ЛВН \_ жетдиспинфо**</span><span class="sxs-lookup"><span data-stu-id="f7083-149">**LVN\_GETDISPINFO**</span></span>](lvn-getdispinfo.md)
</dt> </dl>

 

 





