---
title: Код уведомления NM_CUSTOMDRAW (в виде дерева) (Коммктрл. h)
description: Посылается элементом управления "представление дерева" для уведомления родительского окна об операциях рисования. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- Элементы управления Windows для кода уведомления NM_CUSTOMDRAW (представление в виде дерева)
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
ms.openlocfilehash: 2bb3f7b44748c2ac9c5b9651c079a8b90df0c508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891441"
---
# <a name="nm_customdraw-tree-view-notification-code"></a><span data-ttu-id="d7817-105">\_Код уведомления NM кустомдрав (в виде дерева)</span><span class="sxs-lookup"><span data-stu-id="d7817-105">NM\_CUSTOMDRAW (tree view) notification code</span></span>

<span data-ttu-id="d7817-106">Посылается элементом управления "представление дерева" для уведомления родительского окна об операциях рисования.</span><span class="sxs-lookup"><span data-stu-id="d7817-106">Sent by a tree-view control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="d7817-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d7817-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d7817-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7817-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7817-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7817-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7817-110">Указатель на структуру [**нмтвкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) , которая содержит и получает сведения об операции рисования.</span><span class="sxs-lookup"><span data-stu-id="d7817-110">Pointer to an [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure that contains and receives information about the drawing operation.</span></span> <span data-ttu-id="d7817-111">Элемент **двитемспек** элемента **нмкд** этой структуры содержит маркер рисуемого элемента.</span><span class="sxs-lookup"><span data-stu-id="d7817-111">The **dwItemSpec** member of the **nmcd** member of this structure contains the handle of the item being drawn.</span></span> <span data-ttu-id="d7817-112">Элемент **литемлпарам** элемента **нмкд** этой структуры содержит *lParam* рисуемого элемента.</span><span class="sxs-lookup"><span data-stu-id="d7817-112">The **lItemlParam** member of the **nmcd** member of this structure contains the *lParam* of the item being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7817-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7817-113">Return value</span></span>

<span data-ttu-id="d7817-114">Значение, которое может возвращать приложение, зависит от текущей стадии рисования.</span><span class="sxs-lookup"><span data-stu-id="d7817-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="d7817-115">Элемент **двдравстаже** связанной структуры [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) содержит значение, указывающее стадию рисования.</span><span class="sxs-lookup"><span data-stu-id="d7817-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="d7817-116">Необходимо вернуть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d7817-116">You must return one of the following values.</span></span>



| <span data-ttu-id="d7817-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d7817-117">Return code</span></span>                                                                                            | <span data-ttu-id="d7817-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d7817-118">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7817-119"><dt>**КДРФ \_ додефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="d7817-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="d7817-120">Элемент управления рисует сам себя.</span><span class="sxs-lookup"><span data-stu-id="d7817-120">The control draws itself.</span></span> <span data-ttu-id="d7817-121">Он не отправляет дополнительные коды [ \_ кустомдрав](nm-customdraw.md) для этого цикла рисования.</span><span class="sxs-lookup"><span data-stu-id="d7817-121">It does not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) codes for this paint cycle.</span></span> <span data-ttu-id="d7817-122">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="d7817-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="d7817-123"><dt>**КДРФ \_ нотифитемдрав**</dt></span><span class="sxs-lookup"><span data-stu-id="d7817-123"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="d7817-124">Элемент управления уведомляет родителя о любых операциях рисования, связанных с элементами.</span><span class="sxs-lookup"><span data-stu-id="d7817-124">The control notifies the parent of any item-related drawing operations.</span></span> <span data-ttu-id="d7817-125">Он отправляет коды уведомлений [NM \_ кустомдрав](nm-customdraw.md) до и после прорисовки элементов.</span><span class="sxs-lookup"><span data-stu-id="d7817-125">It sends [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="d7817-126">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="d7817-126">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                |
| <dl> <span data-ttu-id="d7817-127"><dt>**КДРФ \_ нотифипостерасе**</dt></span><span class="sxs-lookup"><span data-stu-id="d7817-127"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="d7817-128">Элемент управления уведомляет родительский элемент после стирания элемента. Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="d7817-128">The control notifies the parent after erasing an item.This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="d7817-129"><dt>**КДРФ \_ нотифипостпаинт**</dt></span><span class="sxs-lookup"><span data-stu-id="d7817-129"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="d7817-130">Элемент управления уведомляет родительский элемент после прорисовки элемента.</span><span class="sxs-lookup"><span data-stu-id="d7817-130">The control notifies the parent after painting an item.</span></span> <span data-ttu-id="d7817-131">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="d7817-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="d7817-132"><dt>**КДРФ \_ нотифисубитемдрав**</dt></span><span class="sxs-lookup"><span data-stu-id="d7817-132"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | [<span data-ttu-id="d7817-133">Версия 4,71.</span><span class="sxs-lookup"><span data-stu-id="d7817-133">Version 4.71.</span></span>](common-control-versions.md) <span data-ttu-id="d7817-134">Элемент управления уведомляет родительский элемент при прорисовке подэлемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="d7817-134">The control notifies the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="d7817-135">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="d7817-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="d7817-136"><dt>**КДРФ \_ невфонт**</dt></span><span class="sxs-lookup"><span data-stu-id="d7817-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="d7817-137">В приложении указан новый шрифт для элемента. элемент управления будет использовать новый шрифт.</span><span class="sxs-lookup"><span data-stu-id="d7817-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="d7817-138">Дополнительные сведения об изменении шрифтов см. в разделе [Изменение шрифтов и цветов](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="d7817-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="d7817-139">Это происходит, когда **двдравстаже** равно кддс \_ итемпрепаинт.</span><span class="sxs-lookup"><span data-stu-id="d7817-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="d7817-140"><dt>**КДРФ \_ скипдефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="d7817-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="d7817-141">Приложение вынарисовало элемент вручную.</span><span class="sxs-lookup"><span data-stu-id="d7817-141">Your application drew the item manually.</span></span> <span data-ttu-id="d7817-142">Элемент управления не будет рисовать элемент.</span><span class="sxs-lookup"><span data-stu-id="d7817-142">The control will not draw the item.</span></span> <span data-ttu-id="d7817-143">Это происходит, когда **двдравстаже** равно кддс \_ итемпрепаинт.</span><span class="sxs-lookup"><span data-stu-id="d7817-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="d7817-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7817-144">Remarks</span></span>

[<span data-ttu-id="d7817-145">Версия 5,80.</span><span class="sxs-lookup"><span data-stu-id="d7817-145">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="d7817-146">При изменении шрифта путем возвращения [**кдрф \_ невфонт**](cdrf-constants.md)элемент управления "дерево-представление" может отображать обрезанный текст.</span><span class="sxs-lookup"><span data-stu-id="d7817-146">If you change the font by returning [**CDRF\_NEWFONT**](cdrf-constants.md), the tree-view control might display clipped text.</span></span> <span data-ttu-id="d7817-147">Это поведение необходимо для обеспечения обратной совместимости с более ранними версиями стандартных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="d7817-147">This behavior is necessary for backward compatibility with earlier versions of the common controls.</span></span> <span data-ttu-id="d7817-148">Если вы хотите изменить шрифт элемента управления "дерево", вы получите лучшие результаты, если отправите сообщение [**CCM \_ сетверсион**](ccm-setversion.md) с параметром *wParam* , равным 5, прежде чем добавлять элементы в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="d7817-148">If you want to change the font of a tree-view control, you will get better results if you send a [**CCM\_SETVERSION**](ccm-setversion.md) message with the *wParam* value set to 5 before adding any items to the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7817-149">Требования</span><span class="sxs-lookup"><span data-stu-id="d7817-149">Requirements</span></span>



| <span data-ttu-id="d7817-150">Требование</span><span class="sxs-lookup"><span data-stu-id="d7817-150">Requirement</span></span> | <span data-ttu-id="d7817-151">Значение</span><span class="sxs-lookup"><span data-stu-id="d7817-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7817-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7817-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d7817-153">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7817-153">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7817-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7817-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d7817-155">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7817-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7817-156">Header</span><span class="sxs-lookup"><span data-stu-id="d7817-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7817-157"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7817-157"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7817-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7817-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7817-159">Использование пользовательского рисования</span><span class="sxs-lookup"><span data-stu-id="d7817-159">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





