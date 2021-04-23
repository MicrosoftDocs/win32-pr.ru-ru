---
title: Код уведомления NM_CUSTOMDRAW (заголовок) (Коммктрл. h)
description: Отправляется элементом управления "заголовок" для уведомления родительского окна об операциях рисования. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 44dab54b-45ef-4fba-93b8-2a3e35cda23f
keywords:
- Элементы управления Windows для кода уведомления NM_CUSTOMDRAW (заголовок)
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
ms.openlocfilehash: 89d6b35503aebed221da6cec212c6dbf614061f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654725"
---
# <a name="nm_customdraw-header-notification-code"></a><span data-ttu-id="d2399-105">\_Код уведомления "NM кустомдрав (заголовок)"</span><span class="sxs-lookup"><span data-stu-id="d2399-105">NM\_CUSTOMDRAW (header) notification code</span></span>

<span data-ttu-id="d2399-106">Отправляется элементом управления "заголовок" для уведомления родительского окна об операциях рисования.</span><span class="sxs-lookup"><span data-stu-id="d2399-106">Sent by a header control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="d2399-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d2399-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d2399-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2399-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2399-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2399-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2399-110">Указатель на структуру [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) , содержащую сведения об операции рисования.</span><span class="sxs-lookup"><span data-stu-id="d2399-110">A pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="d2399-111">Элемент **двитемспек** этой структуры содержит индекс рисуемого элемента, а элемент **литемлпарам** этой структуры содержит *lParam* элемента.</span><span class="sxs-lookup"><span data-stu-id="d2399-111">The **dwItemSpec** member of this structure contains the index of the item being drawn and the **lItemlParam** member of this structure contains the item's *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2399-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2399-112">Return value</span></span>

<span data-ttu-id="d2399-113">Значение, которое может возвращать приложение, зависит от текущей стадии рисования.</span><span class="sxs-lookup"><span data-stu-id="d2399-113">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="d2399-114">Элемент **двдравстаже** связанной структуры [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) содержит значение, указывающее стадию рисования.</span><span class="sxs-lookup"><span data-stu-id="d2399-114">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="d2399-115">Необходимо вернуть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d2399-115">You must return one of the following values.</span></span>



| <span data-ttu-id="d2399-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d2399-116">Return code</span></span>                                                                                            | <span data-ttu-id="d2399-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d2399-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d2399-118"><dt>**КДРФ \_ додефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="d2399-118"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="d2399-119">Элемент управления будет рисовать сам.</span><span class="sxs-lookup"><span data-stu-id="d2399-119">The control will draw itself.</span></span> <span data-ttu-id="d2399-120">Он не будет отсылать дополнительные [ \_ кустомдрав](nm-customdraw.md) сообщения для этого цикла рисования.</span><span class="sxs-lookup"><span data-stu-id="d2399-120">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) messages for this paint cycle.</span></span> <span data-ttu-id="d2399-121">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="d2399-121">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="d2399-122"><dt>**КДРФ \_ нотифитемдрав**</dt></span><span class="sxs-lookup"><span data-stu-id="d2399-122"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="d2399-123">Элемент управления будет уведомлять родителя всех операций рисования, связанных с элементами.</span><span class="sxs-lookup"><span data-stu-id="d2399-123">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="d2399-124">Он будет отсылать \_ кустомдрав коды уведомлений до и после прорисовки элементов.</span><span class="sxs-lookup"><span data-stu-id="d2399-124">It will send NM\_CUSTOMDRAW notification codes before and after drawing items.</span></span> <span data-ttu-id="d2399-125">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="d2399-125">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="d2399-126"><dt>**КДРФ \_ нотифипостерасе**</dt></span><span class="sxs-lookup"><span data-stu-id="d2399-126"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="d2399-127">Элемент управления будет уведомлять родительский элемент после стирания элемента.</span><span class="sxs-lookup"><span data-stu-id="d2399-127">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="d2399-128">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="d2399-128">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="d2399-129"><dt>**КДРФ \_ нотифипостпаинт**</dt></span><span class="sxs-lookup"><span data-stu-id="d2399-129"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="d2399-130">Элемент управления будет уведомлять родительский элемент после рисования элемента.</span><span class="sxs-lookup"><span data-stu-id="d2399-130">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="d2399-131">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="d2399-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="d2399-132"><dt>**КДРФ \_ нотифисубитемдрав**</dt></span><span class="sxs-lookup"><span data-stu-id="d2399-132"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="d2399-133">[Стандартные версии элементов управления](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="d2399-133">[Common Control Versions](common-control-versions.md).</span></span> <span data-ttu-id="d2399-134">Элемент управления будет уведомлять родительский элемент при прорисовке подэлемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="d2399-134">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="d2399-135">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="d2399-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="d2399-136"><dt>**КДРФ \_ невфонт**</dt></span><span class="sxs-lookup"><span data-stu-id="d2399-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="d2399-137">В приложении указан новый шрифт для элемента. элемент управления будет использовать новый шрифт.</span><span class="sxs-lookup"><span data-stu-id="d2399-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="d2399-138">Дополнительные сведения об изменении шрифтов см. в разделе [Изменение шрифтов и цветов](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="d2399-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="d2399-139">Это происходит, когда **двдравстаже** равно кддс \_ итемпрепаинт.</span><span class="sxs-lookup"><span data-stu-id="d2399-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="d2399-140"><dt>**КДРФ \_ скипдефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="d2399-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="d2399-141">Приложение вынарисовало элемент вручную.</span><span class="sxs-lookup"><span data-stu-id="d2399-141">Your application drew the item manually.</span></span> <span data-ttu-id="d2399-142">Элемент управления не будет рисовать элемент.</span><span class="sxs-lookup"><span data-stu-id="d2399-142">The control will not draw the item.</span></span> <span data-ttu-id="d2399-143">Это происходит, когда **двдравстаже** равно кддс \_ итемпрепаинт.</span><span class="sxs-lookup"><span data-stu-id="d2399-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="d2399-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2399-144">Remarks</span></span>

<span data-ttu-id="d2399-145">Дополнительные сведения см. [в статье Использование пользовательского рисования](custom-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="d2399-145">See [Using Custom Draw](custom-draw.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2399-146">Требования</span><span class="sxs-lookup"><span data-stu-id="d2399-146">Requirements</span></span>



| <span data-ttu-id="d2399-147">Требование</span><span class="sxs-lookup"><span data-stu-id="d2399-147">Requirement</span></span> | <span data-ttu-id="d2399-148">Значение</span><span class="sxs-lookup"><span data-stu-id="d2399-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2399-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2399-149">Minimum supported client</span></span><br/> | <span data-ttu-id="d2399-150">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2399-150">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2399-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2399-151">Minimum supported server</span></span><br/> | <span data-ttu-id="d2399-152">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2399-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2399-153">Header</span><span class="sxs-lookup"><span data-stu-id="d2399-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2399-154"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2399-154"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





