---
title: Код уведомления NM_CUSTOMDRAW (Коммктрл. h)
description: Сообщает родительскому окну элемента управления о пользовательских операциях рисования. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 2ca51ee0-4431-45c0-880c-a8b74318d8a9
keywords:
- NM_CUSTOMDRAW кода уведомления элементы управления Windows
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
ms.openlocfilehash: d5f91f5197c7ecaf0ae4356fe00c48221a83ebd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489048"
---
# <a name="nm_customdraw-notification-code"></a><span data-ttu-id="3945a-105">\_Код уведомления кустомдрав (NM)</span><span class="sxs-lookup"><span data-stu-id="3945a-105">NM\_CUSTOMDRAW notification code</span></span>

<span data-ttu-id="3945a-106">Сообщает родительскому окну элемента управления о пользовательских операциях рисования.</span><span class="sxs-lookup"><span data-stu-id="3945a-106">Notifies a control's parent window about custom drawing operations.</span></span> <span data-ttu-id="3945a-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3945a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

#ifdef LIST_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;

#elif TOOL_TIPS_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;

#elif TREE_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;

#elif TOOL_BAR_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTBCUSTOMDRAW) lParam;

#else

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;

#endif
```



## <a name="parameters"></a><span data-ttu-id="3945a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3945a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3945a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3945a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3945a-110">Указатель на пользовательскую структуру, связанную с рисованием, которая содержит сведения об операции рисования.</span><span class="sxs-lookup"><span data-stu-id="3945a-110">A pointer to a custom draw-related structure that contains information about the drawing operation.</span></span> <span data-ttu-id="3945a-111">В следующем списке указаны элементы управления и связанные с ними структуры.</span><span class="sxs-lookup"><span data-stu-id="3945a-111">The following list specifies the controls and their associated structures.</span></span>



| <span data-ttu-id="3945a-112">Control</span><span class="sxs-lookup"><span data-stu-id="3945a-112">Control</span></span>                     | <span data-ttu-id="3945a-113">Пользовательская структура рисования</span><span class="sxs-lookup"><span data-stu-id="3945a-113">Custom Draw Structure</span></span>                    |
|-----------------------------|------------------------------------------|
| <span data-ttu-id="3945a-114">Главная панель, линейка и заголовок</span><span class="sxs-lookup"><span data-stu-id="3945a-114">Rebar, trackbar, and header</span></span> | [<span data-ttu-id="3945a-115">**нмкустомдрав**</span><span class="sxs-lookup"><span data-stu-id="3945a-115">**NMCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     |
| <span data-ttu-id="3945a-116">Представление списка</span><span class="sxs-lookup"><span data-stu-id="3945a-116">List view</span></span>                   | [<span data-ttu-id="3945a-117">**нмлвкустомдрав**</span><span class="sxs-lookup"><span data-stu-id="3945a-117">**NMLVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) |
| <span data-ttu-id="3945a-118">Всплывающая подсказка</span><span class="sxs-lookup"><span data-stu-id="3945a-118">Tooltip</span></span>                     | [<span data-ttu-id="3945a-119">**нмтткустомдрав**</span><span class="sxs-lookup"><span data-stu-id="3945a-119">**NMTTCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) |
| <span data-ttu-id="3945a-120">Представление в виде дерева</span><span class="sxs-lookup"><span data-stu-id="3945a-120">Tree view</span></span>                   | [<span data-ttu-id="3945a-121">**нмтвкустомдрав**</span><span class="sxs-lookup"><span data-stu-id="3945a-121">**NMTVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) |
| <span data-ttu-id="3945a-122">Панель инструментов</span><span class="sxs-lookup"><span data-stu-id="3945a-122">Toolbar</span></span>                     | [<span data-ttu-id="3945a-123">**нмтбкустомдрав**</span><span class="sxs-lookup"><span data-stu-id="3945a-123">**NMTBCUSTOMDRAW**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3945a-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3945a-124">Return value</span></span>

<span data-ttu-id="3945a-125">Значение, которое может возвращать приложение, зависит от текущей стадии рисования.</span><span class="sxs-lookup"><span data-stu-id="3945a-125">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="3945a-126">Элемент **двдравстаже** связанной структуры [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) содержит значение, указывающее стадию рисования.</span><span class="sxs-lookup"><span data-stu-id="3945a-126">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="3945a-127">Необходимо вернуть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3945a-127">You must return one of the following values.</span></span>



| <span data-ttu-id="3945a-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3945a-128">Return code</span></span>                                                                                            | <span data-ttu-id="3945a-129">Описание</span><span class="sxs-lookup"><span data-stu-id="3945a-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3945a-130"><dt>**КДРФ \_ додефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="3945a-130"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="3945a-131">Элемент управления будет рисовать сам.</span><span class="sxs-lookup"><span data-stu-id="3945a-131">The control will draw itself.</span></span> <span data-ttu-id="3945a-132">Он не будет отсылать дополнительные коды уведомлений [ \_ кустомдрав](nm-customdraw.md) для этого цикла рисования.</span><span class="sxs-lookup"><span data-stu-id="3945a-132">It will not send additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="3945a-133">Этот флаг нельзя использовать с любым другим флагом.</span><span class="sxs-lookup"><span data-stu-id="3945a-133">This flag cannot be used with any other flag.</span></span> <br/>                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="3945a-134"><dt>**КДРФ \_ доерасе**</dt></span><span class="sxs-lookup"><span data-stu-id="3945a-134"><dt>**CDRF\_DOERASE**</dt></span></span> </dl>           | <span data-ttu-id="3945a-135">Элемент управления будет рисовать только фон.</span><span class="sxs-lookup"><span data-stu-id="3945a-135">The control will only draw the background.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="3945a-136"><dt>**КДРФ \_ невфонт**</dt></span><span class="sxs-lookup"><span data-stu-id="3945a-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="3945a-137">В приложении указан новый шрифт для элемента. элемент управления будет использовать новый шрифт.</span><span class="sxs-lookup"><span data-stu-id="3945a-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="3945a-138">Дополнительные сведения об изменении шрифтов см. в разделе [Изменение шрифтов и цветов](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="3945a-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="3945a-139">Это происходит, когда **двдравстаже** равно кддс \_ итемпрепаинт.</span><span class="sxs-lookup"><span data-stu-id="3945a-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="3945a-140"><dt>**КДРФ \_ нотифитемдрав**</dt></span><span class="sxs-lookup"><span data-stu-id="3945a-140"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="3945a-141">Элемент управления будет уведомлять родителя всех операций рисования, связанных с элементами.</span><span class="sxs-lookup"><span data-stu-id="3945a-141">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="3945a-142">Он будет отсылать [ \_ кустомдрав](nm-customdraw.md) коды уведомлений до и после прорисовки элементов.</span><span class="sxs-lookup"><span data-stu-id="3945a-142">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="3945a-143">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="3945a-143">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="3945a-144"><dt>**КДРФ \_ нотифипостерасе**</dt></span><span class="sxs-lookup"><span data-stu-id="3945a-144"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="3945a-145">Элемент управления будет уведомлять родительский элемент после стирания элемента.</span><span class="sxs-lookup"><span data-stu-id="3945a-145">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="3945a-146">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="3945a-146">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="3945a-147"><dt>**КДРФ \_ нотифипостпаинт**</dt></span><span class="sxs-lookup"><span data-stu-id="3945a-147"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="3945a-148">Элемент управления будет отсылать код уведомления [NM \_ кустомдрав](nm-customdraw.md) при завершении цикла рисования для всего элемента управления.</span><span class="sxs-lookup"><span data-stu-id="3945a-148">The control will send an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code when the painting cycle for the entire control is complete.</span></span> <span data-ttu-id="3945a-149">Это происходит, когда **двдравстаже** равно кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="3945a-149">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="3945a-150"><dt>**КДРФ \_ нотифисубитемдрав**</dt></span><span class="sxs-lookup"><span data-stu-id="3945a-150"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="3945a-151">Приложение получит код уведомления [NM \_ Кустомдрав](nm-customdraw.md) с **двдравстаже** , для которого задано значение кддс \_ итемпрепаинт \| кддс \_ подэлемент перед прорисовкой каждого подэлемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="3945a-151">Your application will receive an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code with **dwDrawStage** set to CDDS\_ITEMPREPAINT \| CDDS\_SUBITEM before each list-view subitem is drawn.</span></span> <span data-ttu-id="3945a-152">Затем можно указать шрифт и цвет для каждого подэлемента отдельно или вернуть [**кдрф \_ додефаулт**](cdrf-constants.md) для обработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3945a-152">You can then specify font and color for each subitem separately or return [**CDRF\_DODEFAULT**](cdrf-constants.md) for default processing.</span></span> <span data-ttu-id="3945a-153">Это происходит, когда **двдравстаже** равно кддс \_ итемпрепаинт.</span><span class="sxs-lookup"><span data-stu-id="3945a-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="3945a-154"><dt>**КДРФ \_ скипдефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="3945a-154"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="3945a-155">Приложение вынарисовало элемент вручную.</span><span class="sxs-lookup"><span data-stu-id="3945a-155">Your application drew the item manually.</span></span> <span data-ttu-id="3945a-156">Элемент управления не будет рисовать элемент.</span><span class="sxs-lookup"><span data-stu-id="3945a-156">The control will not draw the item.</span></span> <span data-ttu-id="3945a-157">Это происходит, когда **двдравстаже** равно кддс \_ итемпрепаинт.</span><span class="sxs-lookup"><span data-stu-id="3945a-157">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="3945a-158"><dt>**КДРФ \_ скиппостпаинт**</dt></span><span class="sxs-lookup"><span data-stu-id="3945a-158"><dt>**CDRF\_SKIPPOSTPAINT**</dt></span></span> </dl>     | <span data-ttu-id="3945a-159">Элемент управления не будет рисовать прямоугольник фокуса вокруг элемента.</span><span class="sxs-lookup"><span data-stu-id="3945a-159">The control will not draw the focus rectangle around an item.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="3945a-160">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3945a-160">Remarks</span></span>

<span data-ttu-id="3945a-161">В настоящее время следующие элементы управления поддерживают пользовательскую функциональность рисования: заголовок, представление списка, панель инструментов, подсказка, TrackBar и представление в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="3945a-161">Currently, the following controls support custom draw functionality: header, list view, rebar, toolbar, tooltip, trackbar, and tree view.</span></span> <span data-ttu-id="3945a-162">Пользовательская прорисовка также поддерживается для элементов управления "Кнопка", если имеется манифест приложения, чтобы гарантировать доступность Comctl32.dll версии 6.</span><span class="sxs-lookup"><span data-stu-id="3945a-162">Custom draw is also supported for button controls if you have an application manifest to ensure that Comctl32.dll version 6 is available.</span></span>

<span data-ttu-id="3945a-163">Если это сообщение обрабатывается в диалоговой процедуре, необходимо задать возвращаемое значение как часть данных окна перед возвратом значения **true**.</span><span class="sxs-lookup"><span data-stu-id="3945a-163">If this message is handled in a dialog procedure, you must set the return value as part of the window data before returning **TRUE**.</span></span> <span data-ttu-id="3945a-164">Дополнительные сведения см. в разделе [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).</span><span class="sxs-lookup"><span data-stu-id="3945a-164">For more information, see [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).</span></span>

## <a name="requirements"></a><span data-ttu-id="3945a-165">Требования</span><span class="sxs-lookup"><span data-stu-id="3945a-165">Requirements</span></span>



| <span data-ttu-id="3945a-166">Требование</span><span class="sxs-lookup"><span data-stu-id="3945a-166">Requirement</span></span> | <span data-ttu-id="3945a-167">Значение</span><span class="sxs-lookup"><span data-stu-id="3945a-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3945a-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3945a-168">Minimum supported client</span></span><br/> | <span data-ttu-id="3945a-169">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3945a-169">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3945a-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3945a-170">Minimum supported server</span></span><br/> | <span data-ttu-id="3945a-171">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3945a-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3945a-172">Header</span><span class="sxs-lookup"><span data-stu-id="3945a-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="3945a-173"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3945a-173"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3945a-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3945a-174">See also</span></span>

<dl> <dt>

<span data-ttu-id="3945a-175">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="3945a-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3945a-176">Пользовательская прорисовка</span><span class="sxs-lookup"><span data-stu-id="3945a-176">Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

