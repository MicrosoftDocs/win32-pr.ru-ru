---
title: Код уведомления NM_CUSTOMDRAW (TrackBar) (Коммктрл. h)
description: Отправляется элементом управления TrackBar для уведомления своих родительских окон о операциях рисования. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- Элементы управления Windows для кода уведомления NM_CUSTOMDRAW (TrackBar)
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ebbffd531fb44e2491d72954ce111db208f2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137859"
---
# <a name="nm_customdraw-trackbar-notification-code"></a><span data-ttu-id="0a7d6-105">\_Код уведомления NM кустомдрав (TrackBar)</span><span class="sxs-lookup"><span data-stu-id="0a7d6-105">NM\_CUSTOMDRAW (trackbar) notification code</span></span>

<span data-ttu-id="0a7d6-106">Отправляется элементом управления TrackBar для уведомления своих родительских окон о операциях рисования.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-106">Sent by a trackbar control to notify its parent windows about drawing operations.</span></span> <span data-ttu-id="0a7d6-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0a7d6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0a7d6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a7d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a7d6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a7d6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a7d6-110">Указатель на структуру [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) , содержащую сведения об операции рисования.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-110">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="0a7d6-111">Элемент **двитемспек** этой структуры будет содержать одно из [пользовательских значений рисования](custom-draw-values.md) , которое указывает, какая часть элемента управления рисуется.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-111">The **dwItemSpec** member of this structure will contain one of the [Custom Draw Values](custom-draw-values.md) that indicates which part of the control is being drawn.</span></span> <span data-ttu-id="0a7d6-112">Элементы управления TrackBar вставляют следующие значения в элемент **двитемспек** этой структуры для обнаружения части рисуемого элемента управления:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-112">Trackbar controls insert the following values into the **dwItemSpec** member of this structure to identify the portion of the control being drawn:</span></span>



| <span data-ttu-id="0a7d6-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0a7d6-113">Value</span></span>                                                                                                                                                      | <span data-ttu-id="0a7d6-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0a7d6-114">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <span data-ttu-id="0a7d6-115"><dt>**\_канал тбкд**</dt></span><span class="sxs-lookup"><span data-stu-id="0a7d6-115"><dt>**TBCD\_CHANNEL**</dt></span></span> </dl> | <span data-ttu-id="0a7d6-116">Определяет канал, вдоль которого проводятся маркеры Thumb элемента управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-116">Identifies the channel that the trackbar control's thumb marker slides along.</span></span> <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <span data-ttu-id="0a7d6-117"><dt>**ТБКД \_ бегунок**</dt></span><span class="sxs-lookup"><span data-stu-id="0a7d6-117"><dt>**TBCD\_THUMB**</dt></span></span> </dl>       | <span data-ttu-id="0a7d6-118">Определяет маркер Thumb элемента управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-118">Identifies the trackbar control's thumb marker.</span></span> <span data-ttu-id="0a7d6-119">Это часть элемента управления, который перемещает пользователь.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-119">This is the portion of the control that the user moves.</span></span> <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <span data-ttu-id="0a7d6-120"><dt>**ТБКД \_ ТИКС**</dt></span><span class="sxs-lookup"><span data-stu-id="0a7d6-120"><dt>**TBCD\_TICS**</dt></span></span> </dl>          | <span data-ttu-id="0a7d6-121">Определяет деления приращения, которые отображаются вдоль края элемента управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-121">Identifies the increment tick marks that appear along the edge of the trackbar control.</span></span> <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a7d6-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a7d6-122">Return value</span></span>

<span data-ttu-id="0a7d6-123">Значение, которое может возвращать приложение, зависит от текущей стадии рисования.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-123">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="0a7d6-124">Элемент **двдравстаже** связанной структуры [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) содержит значение, указывающее стадию рисования.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-124">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="0a7d6-125">Необходимо вернуть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-125">You must return one of the following values.</span></span>



| <span data-ttu-id="0a7d6-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0a7d6-126">Return code</span></span>                                                                                            | <span data-ttu-id="0a7d6-127">Описание</span><span class="sxs-lookup"><span data-stu-id="0a7d6-127">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a7d6-128"><dt>**КДРФ \_ додефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="0a7d6-128"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="0a7d6-129">Элемент управления будет рисовать сам.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-129">The control will draw itself.</span></span> <span data-ttu-id="0a7d6-130">Он не будет отсылать дополнительные коды уведомлений [ \_ кустомдрав](nm-customdraw.md) для этого цикла рисования.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-130">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="0a7d6-131">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="0a7d6-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="0a7d6-132"><dt>**КДРФ \_ нотифитемдрав**</dt></span><span class="sxs-lookup"><span data-stu-id="0a7d6-132"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="0a7d6-133">Элемент управления будет уведомлять родителя всех операций рисования, связанных с элементами.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-133">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="0a7d6-134">Он будет отсылать [ \_ кустомдрав](nm-customdraw.md) коды уведомлений до и после прорисовки элементов.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-134">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="0a7d6-135">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="0a7d6-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                         |
| <dl> <span data-ttu-id="0a7d6-136"><dt>**КДРФ \_ нотифипостерасе**</dt></span><span class="sxs-lookup"><span data-stu-id="0a7d6-136"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="0a7d6-137">Элемент управления будет уведомлять родительский элемент после стирания элемента.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-137">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="0a7d6-138">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="0a7d6-138">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="0a7d6-139"><dt>**КДРФ \_ нотифипостпаинт**</dt></span><span class="sxs-lookup"><span data-stu-id="0a7d6-139"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="0a7d6-140">Элемент управления будет уведомлять родительский элемент после рисования элемента.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-140">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="0a7d6-141">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="0a7d6-141">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="0a7d6-142"><dt>**КДРФ \_ нотифисубитемдрав**</dt></span><span class="sxs-lookup"><span data-stu-id="0a7d6-142"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="0a7d6-143">[Версия 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="0a7d6-143">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="0a7d6-144">Элемент управления будет уведомлять родительский элемент при прорисовке подэлемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-144">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="0a7d6-145">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="0a7d6-145">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0a7d6-146"><dt>**КДРФ \_ невфонт**</dt></span><span class="sxs-lookup"><span data-stu-id="0a7d6-146"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="0a7d6-147">В приложении указан новый шрифт для элемента. элемент управления будет использовать новый шрифт.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-147">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="0a7d6-148">Дополнительные сведения об изменении шрифтов см. в разделе [Изменение шрифтов и цветов](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="0a7d6-148">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="0a7d6-149">Это происходит, когда **двдравстаже** равно кддс \_ итемпрепаинт.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-149">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="0a7d6-150"><dt>**КДРФ \_ скипдефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="0a7d6-150"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="0a7d6-151">Приложение вынарисовало элемент вручную.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-151">Your application drew the item manually.</span></span> <span data-ttu-id="0a7d6-152">Элемент управления не будет рисовать элемент.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-152">The control will not draw the item.</span></span> <span data-ttu-id="0a7d6-153">Это происходит, когда **двдравстаже** равно кддс \_ итемпрепаинт.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="0a7d6-154">Требования</span><span class="sxs-lookup"><span data-stu-id="0a7d6-154">Requirements</span></span>



| <span data-ttu-id="0a7d6-155">Требование</span><span class="sxs-lookup"><span data-stu-id="0a7d6-155">Requirement</span></span> | <span data-ttu-id="0a7d6-156">Значение</span><span class="sxs-lookup"><span data-stu-id="0a7d6-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a7d6-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a7d6-157">Minimum supported client</span></span><br/> | <span data-ttu-id="0a7d6-158">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a7d6-158">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a7d6-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a7d6-159">Minimum supported server</span></span><br/> | <span data-ttu-id="0a7d6-160">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0a7d6-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a7d6-161">Header</span><span class="sxs-lookup"><span data-stu-id="0a7d6-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a7d6-162"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a7d6-162"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a7d6-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a7d6-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a7d6-164">Использование пользовательского рисования</span><span class="sxs-lookup"><span data-stu-id="0a7d6-164">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





