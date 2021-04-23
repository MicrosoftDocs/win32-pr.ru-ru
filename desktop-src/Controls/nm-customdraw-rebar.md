---
title: Код уведомления NM_CUSTOMDRAW (Главная панель) (Коммктрл. h)
description: Отправляется элементом управления "Главная панель" для уведомления родительского окна об операциях рисования. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 3ba9bb59-f297-4af1-a9a9-d8789def5bde
keywords:
- Элементы управления Windows для кода уведомления NM_CUSTOMDRAW (Главная панель)
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
ms.openlocfilehash: 329f3e9abfb20dbca8cebd3a6bf02673ad00f904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137862"
---
# <a name="nm_customdraw-rebar-notification-code"></a><span data-ttu-id="ef159-105">\_Код уведомления "NM кустомдрав" (Главная панель)</span><span class="sxs-lookup"><span data-stu-id="ef159-105">NM\_CUSTOMDRAW (rebar) notification code</span></span>

<span data-ttu-id="ef159-106">Отправляется элементом управления "Главная панель" для уведомления родительского окна об операциях рисования.</span><span class="sxs-lookup"><span data-stu-id="ef159-106">Sent by the rebar control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="ef159-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ef159-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ef159-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef159-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef159-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef159-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef159-110">Указатель на структуру [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) , содержащую сведения об операции рисования.</span><span class="sxs-lookup"><span data-stu-id="ef159-110">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="ef159-111">Элемент **двитемспек** этой структуры содержит идентификатор рисуемого диапазона.</span><span class="sxs-lookup"><span data-stu-id="ef159-111">The **dwItemSpec** member of this structure contains the identifier of the band being drawn.</span></span> <span data-ttu-id="ef159-112">Элемент **литемлпарам** этой структуры содержит *lParam* отображаемого диапазона.</span><span class="sxs-lookup"><span data-stu-id="ef159-112">The **lItemlParam** member of this structure contains the *lParam* of the band being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef159-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef159-113">Return value</span></span>

<span data-ttu-id="ef159-114">Значение, которое может возвращать приложение, зависит от текущей стадии рисования.</span><span class="sxs-lookup"><span data-stu-id="ef159-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="ef159-115">Элемент **двдравстаже** связанной структуры [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) содержит значение, указывающее стадию рисования.</span><span class="sxs-lookup"><span data-stu-id="ef159-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="ef159-116">Необходимо вернуть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ef159-116">You must return one of the following values.</span></span>



| <span data-ttu-id="ef159-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ef159-117">Return code</span></span>                                                                                            | <span data-ttu-id="ef159-118">Описание</span><span class="sxs-lookup"><span data-stu-id="ef159-118">Description</span></span>                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef159-119"><dt>**КДРФ \_ додефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="ef159-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="ef159-120">Элемент управления будет рисовать сам.</span><span class="sxs-lookup"><span data-stu-id="ef159-120">The control will draw itself.</span></span> <span data-ttu-id="ef159-121">Он не будет отправлять дополнительные [ \_ кустомдрав](nm-customdraw.md) уведомления для этого цикла рисования.</span><span class="sxs-lookup"><span data-stu-id="ef159-121">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notifications for this paint cycle.</span></span> <span data-ttu-id="ef159-122">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="ef159-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="ef159-123"><dt>**КДРФ \_ нотифитемдрав**</dt></span><span class="sxs-lookup"><span data-stu-id="ef159-123"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="ef159-124">Элемент управления будет уведомлять родителя всех операций рисования, связанных с элементами.</span><span class="sxs-lookup"><span data-stu-id="ef159-124">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="ef159-125">Он будет отсылать [ \_ кустомдрав](nm-customdraw.md) коды уведомлений до и после прорисовки элементов.</span><span class="sxs-lookup"><span data-stu-id="ef159-125">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="ef159-126">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="ef159-126">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                           |
| <dl> <span data-ttu-id="ef159-127"><dt>**КДРФ \_ нотифипостерасе**</dt></span><span class="sxs-lookup"><span data-stu-id="ef159-127"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="ef159-128">Элемент управления будет уведомлять родительский элемент после стирания элемента.</span><span class="sxs-lookup"><span data-stu-id="ef159-128">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="ef159-129">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="ef159-129">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="ef159-130"><dt>**КДРФ \_ нотифипостпаинт**</dt></span><span class="sxs-lookup"><span data-stu-id="ef159-130"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="ef159-131">Элемент управления будет уведомлять родительский элемент после рисования элемента.</span><span class="sxs-lookup"><span data-stu-id="ef159-131">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="ef159-132">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="ef159-132">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                               |
| <dl> <span data-ttu-id="ef159-133"><dt>**КДРФ \_ нотифисубитемдрав**</dt></span><span class="sxs-lookup"><span data-stu-id="ef159-133"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="ef159-134">Элемент управления будет уведомлять родителя всех операций рисования, связанных с элементами.</span><span class="sxs-lookup"><span data-stu-id="ef159-134">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="ef159-135">Он будет отсылать [ \_ кустомдрав](nm-customdraw.md) коды уведомлений до и после прорисовки элементов.</span><span class="sxs-lookup"><span data-stu-id="ef159-135">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="ef159-136">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="ef159-136">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                           |
| <dl> <span data-ttu-id="ef159-137"><dt>**КДРФ \_ невфонт**</dt></span><span class="sxs-lookup"><span data-stu-id="ef159-137"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="ef159-138">Приложение указало новый шрифт для элемента; элемент управления будет использовать новый шрифт.</span><span class="sxs-lookup"><span data-stu-id="ef159-138">The application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="ef159-139">Дополнительные сведения об изменении шрифтов см. в разделе [Изменение шрифтов и цветов](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="ef159-139">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="ef159-140">Это происходит, когда **двдравстаже** равно кддс \_ итемпрепаинт.</span><span class="sxs-lookup"><span data-stu-id="ef159-140">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="ef159-141"><dt>**КДРФ \_ скипдефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="ef159-141"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="ef159-142">Приложение назначит элемент вручную.</span><span class="sxs-lookup"><span data-stu-id="ef159-142">The application drew the item manually.</span></span> <span data-ttu-id="ef159-143">Элемент управления не будет рисовать элемент.</span><span class="sxs-lookup"><span data-stu-id="ef159-143">The control will not draw the item.</span></span> <span data-ttu-id="ef159-144">Это происходит, когда **двдравстаже** равно кддс \_ итемпрепаинт.</span><span class="sxs-lookup"><span data-stu-id="ef159-144">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="ef159-145">Требования</span><span class="sxs-lookup"><span data-stu-id="ef159-145">Requirements</span></span>



| <span data-ttu-id="ef159-146">Требование</span><span class="sxs-lookup"><span data-stu-id="ef159-146">Requirement</span></span> | <span data-ttu-id="ef159-147">Значение</span><span class="sxs-lookup"><span data-stu-id="ef159-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef159-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef159-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ef159-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef159-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef159-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef159-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ef159-151">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ef159-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef159-152">Header</span><span class="sxs-lookup"><span data-stu-id="ef159-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef159-153"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef159-153"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef159-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef159-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef159-155">Использование пользовательского рисования</span><span class="sxs-lookup"><span data-stu-id="ef159-155">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





