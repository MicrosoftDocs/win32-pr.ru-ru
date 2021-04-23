---
title: Код уведомления NM_CUSTOMDRAW (подсказка) (Коммктрл. h)
description: Отправляется элементом управления ToolTip для уведомления родительского окна об операциях рисования. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 82939901-baed-452b-85bf-3c0c01e1f5df
keywords:
- Элементы управления Windows для кода уведомления NM_CUSTOMDRAW (подсказка)
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
ms.openlocfilehash: 9ce1047f63c8580051f7d57abf3308bde37238a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804133"
---
# <a name="nm_customdraw-tooltip-notification-code"></a><span data-ttu-id="dcb89-105">\_Код уведомления NM кустомдрав (подсказка)</span><span class="sxs-lookup"><span data-stu-id="dcb89-105">NM\_CUSTOMDRAW (tooltip) notification code</span></span>

<span data-ttu-id="dcb89-106">Отправляется элементом управления ToolTip для уведомления родительского окна об операциях рисования.</span><span class="sxs-lookup"><span data-stu-id="dcb89-106">Sent by a tooltip control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="dcb89-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="dcb89-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="dcb89-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dcb89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcb89-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dcb89-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dcb89-110">Указатель на структуру [**нмтткустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) , содержащую сведения об операции рисования.</span><span class="sxs-lookup"><span data-stu-id="dcb89-110">Pointer to an [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) structure that contains information about the drawing operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcb89-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcb89-111">Return value</span></span>

<span data-ttu-id="dcb89-112">Значение, которое может возвращать приложение, зависит от текущей стадии рисования.</span><span class="sxs-lookup"><span data-stu-id="dcb89-112">The value that your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="dcb89-113">Элемент **двдравстаже** связанной структуры [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) содержит значение, указывающее стадию рисования.</span><span class="sxs-lookup"><span data-stu-id="dcb89-113">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="dcb89-114">Необходимо вернуть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="dcb89-114">You must return one of the following values.</span></span>



| <span data-ttu-id="dcb89-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dcb89-115">Return code</span></span>                                                                                            | <span data-ttu-id="dcb89-116">Описание</span><span class="sxs-lookup"><span data-stu-id="dcb89-116">Description</span></span>                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dcb89-117"><dt>**КДРФ \_ додефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="dcb89-117"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="dcb89-118">Элемент управления будет рисовать сам.</span><span class="sxs-lookup"><span data-stu-id="dcb89-118">The control will draw itself.</span></span> <span data-ttu-id="dcb89-119">Он не будет отсылать дополнительные коды уведомлений [ \_ кустомдрав](nm-customdraw.md) для этого цикла рисования.</span><span class="sxs-lookup"><span data-stu-id="dcb89-119">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="dcb89-120">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="dcb89-120">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="dcb89-121"><dt>**КДРФ \_ нотифитемдрав**</dt></span><span class="sxs-lookup"><span data-stu-id="dcb89-121"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="dcb89-122">Элемент управления будет уведомлять родителя всех операций рисования, связанных с элементами.</span><span class="sxs-lookup"><span data-stu-id="dcb89-122">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="dcb89-123">Он будет отсылать [ \_ кустомдрав](nm-customdraw.md) коды уведомлений до и после прорисовки элементов.</span><span class="sxs-lookup"><span data-stu-id="dcb89-123">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="dcb89-124">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="dcb89-124">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                            |
| <dl> <span data-ttu-id="dcb89-125"><dt>**КДРФ \_ нотифипостерасе**</dt></span><span class="sxs-lookup"><span data-stu-id="dcb89-125"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="dcb89-126">Элемент управления будет уведомлять родительский элемент после стирания элемента.</span><span class="sxs-lookup"><span data-stu-id="dcb89-126">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="dcb89-127">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="dcb89-127">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="dcb89-128"><dt>**КДРФ \_ нотифипостпаинт**</dt></span><span class="sxs-lookup"><span data-stu-id="dcb89-128"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="dcb89-129">Элемент управления будет уведомлять родительский элемент после рисования элемента.</span><span class="sxs-lookup"><span data-stu-id="dcb89-129">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="dcb89-130">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="dcb89-130">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="dcb89-131"><dt>**КДРФ \_ нотифисубитемдрав**</dt></span><span class="sxs-lookup"><span data-stu-id="dcb89-131"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="dcb89-132">[Версия 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="dcb89-132">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="dcb89-133">Элемент управления будет уведомлять родительский элемент при прорисовке подэлемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="dcb89-133">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="dcb89-134">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="dcb89-134">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="dcb89-135"><dt>**КДРФ \_ невфонт**</dt></span><span class="sxs-lookup"><span data-stu-id="dcb89-135"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="dcb89-136">В приложении указан новый шрифт для элемента.</span><span class="sxs-lookup"><span data-stu-id="dcb89-136">Your application specified a new font for the item.</span></span> <span data-ttu-id="dcb89-137">Элемент управления будет использовать новый шрифт.</span><span class="sxs-lookup"><span data-stu-id="dcb89-137">The control will use the new font.</span></span> <span data-ttu-id="dcb89-138">Дополнительные сведения об изменении шрифтов см. в разделе [Изменение шрифтов и цветов](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="dcb89-138">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="dcb89-139">Это происходит, когда **двдравстаже** равно кддс \_ итемпрепаинт.</span><span class="sxs-lookup"><span data-stu-id="dcb89-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="dcb89-140"><dt>**КДРФ \_ скипдефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="dcb89-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="dcb89-141">Приложение вынарисовало элемент вручную.</span><span class="sxs-lookup"><span data-stu-id="dcb89-141">Your application drew the item manually.</span></span> <span data-ttu-id="dcb89-142">Элемент управления не будет рисовать элемент.</span><span class="sxs-lookup"><span data-stu-id="dcb89-142">The control will not draw the item.</span></span> <span data-ttu-id="dcb89-143">Это происходит, когда **двдравстаже** равно кддс \_ итемпрепаинт.</span><span class="sxs-lookup"><span data-stu-id="dcb89-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="dcb89-144">Требования</span><span class="sxs-lookup"><span data-stu-id="dcb89-144">Requirements</span></span>



| <span data-ttu-id="dcb89-145">Требование</span><span class="sxs-lookup"><span data-stu-id="dcb89-145">Requirement</span></span> | <span data-ttu-id="dcb89-146">Значение</span><span class="sxs-lookup"><span data-stu-id="dcb89-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb89-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dcb89-147">Minimum supported client</span></span><br/> | <span data-ttu-id="dcb89-148">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dcb89-148">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dcb89-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dcb89-149">Minimum supported server</span></span><br/> | <span data-ttu-id="dcb89-150">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dcb89-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dcb89-151">Header</span><span class="sxs-lookup"><span data-stu-id="dcb89-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcb89-152"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcb89-152"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcb89-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dcb89-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcb89-154">Использование пользовательского рисования</span><span class="sxs-lookup"><span data-stu-id="dcb89-154">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





