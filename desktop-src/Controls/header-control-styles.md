---
title: Стили элемента управления "заголовок" (Коммктрл. h)
description: Элементы управления "заголовок" имеют ряд стилей, описанных в этом разделе, которые определяют внешний вид и поведение элемента управления. Начальные стили задаются при создании элемента управления "заголовок".
ms.assetid: e47dc6c3-a1af-456c-9235-29ce63f1e13b
topic_type:
- apiref
api_name:
- HDS_BUTTONS
- HDS_DRAGDROP
- HDS_FILTERBAR
- HDS_FLAT
- HDS_FULLDRAG
- HDS_HIDDEN
- HDS_HORZ
- HDS_HOTTRACK
- HDS_CHECKBOXES
- HDS_NOSIZING
- HDS_OVERFLOW
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8450ad39cdb965e3e4be15f0093ec4737a87c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648631"
---
# <a name="header-control-styles"></a><span data-ttu-id="8e425-104">Стили элемента управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="8e425-104">Header Control Styles</span></span>

<span data-ttu-id="8e425-105">Элементы управления "заголовок" имеют ряд стилей, описанных в этом разделе, которые определяют внешний вид и поведение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8e425-105">Header controls have a number of styles, described in this section, that determine the control's appearance and behavior.</span></span> <span data-ttu-id="8e425-106">Начальные стили задаются при создании элемента управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="8e425-106">You set the initial styles when you create the header control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="8e425-107">Константа</span><span class="sxs-lookup"><span data-stu-id="8e425-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="8e425-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8e425-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl> <span data-ttu-id="8e425-109"><dt><strong>HDS_BUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8e425-109"><dt><strong>HDS_BUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8e425-110">Каждый элемент в элементе управления выглядит и ведет себя как кнопка "Отправить".</span><span class="sxs-lookup"><span data-stu-id="8e425-110">Each item in the control looks and behaves like a push button.</span></span> <span data-ttu-id="8e425-111">Этот стиль удобен, если приложение выполняет задачу, когда пользователь щелкает элемент в элементе управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="8e425-111">This style is useful if an application carries out a task when the user clicks an item in the header control.</span></span> <span data-ttu-id="8e425-112">Например, приложение может сортировать сведения в столбцах по-разному в зависимости от того, какой элемент пользователь щелкает.</span><span class="sxs-lookup"><span data-stu-id="8e425-112">For example, an application could sort information in the columns differently depending on which item the user clicks.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl> <span data-ttu-id="8e425-113"><dt><strong>HDS_DRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8e425-113"><dt><strong>HDS_DRAGDROP</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8e425-114">Позволяет изменять порядок элементов заголовка с помощью перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="8e425-114">Allows drag-and-drop reordering of header items.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl> <span data-ttu-id="8e425-115"><dt><strong>HDS_FILTERBAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8e425-115"><dt><strong>HDS_FILTERBAR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8e425-116">Включите строку фильтра как часть стандартного элемента управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="8e425-116">Include a filter bar as part of the standard header control.</span></span> <span data-ttu-id="8e425-117">Эта панель позволяет пользователям удобно применять фильтр к отображению.</span><span class="sxs-lookup"><span data-stu-id="8e425-117">This bar allows users to conveniently apply a filter to the display.</span></span> <span data-ttu-id="8e425-118">Вызовы <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> возвращают новый размер элемента управления и вызывают обновление представления списка.</span><span class="sxs-lookup"><span data-stu-id="8e425-118">Calls to <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> will yield a new size for the control and cause the list view to update.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_FLAT"></span><span id="hds_flat"></span><dl> <span data-ttu-id="8e425-119"><dt><strong>HDS_FLAT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8e425-119"><dt><strong>HDS_FLAT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8e425-120"><a href="common-control-versions.md">Версия 6,0 и более поздние версии</a>.</span><span class="sxs-lookup"><span data-stu-id="8e425-120"><a href="common-control-versions.md">Version 6.0 and later</a>.</span></span> <span data-ttu-id="8e425-121">Приводит к тому, что элемент управления "заголовок" отображается плоским, когда операционная система работает в классическом режиме.</span><span class="sxs-lookup"><span data-stu-id="8e425-121">Causes the header control to be drawn flat when the operating system is running in classic mode.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8e425-122">Версия Comctl32.dll 6 не является распространяемой, но включена в Windows.</span><span class="sxs-lookup"><span data-stu-id="8e425-122">Comctl32.dll version 6 is not redistributable but it is included in Windows.</span></span> <span data-ttu-id="8e425-123">Чтобы использовать Comctl32.dll версии 6, укажите ее в манифесте.</span><span class="sxs-lookup"><span data-stu-id="8e425-123">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="8e425-124">Дополнительные сведения о манифестах см. в разделе <a href="cookbook-overview.md">Включение визуальных стилей</a>.</span><span class="sxs-lookup"><span data-stu-id="8e425-124">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl> <span data-ttu-id="8e425-125"><dt><strong>HDS_FULLDRAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8e425-125"><dt><strong>HDS_FULLDRAG</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8e425-126">Заставляет элемент управления "заголовок" отображать содержимое столбца, даже пока пользователь изменяет размер столбца.</span><span class="sxs-lookup"><span data-stu-id="8e425-126">Causes the header control to display column contents even while the user resizes a column.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl> <span data-ttu-id="8e425-127"><dt><strong>HDS_HIDDEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8e425-127"><dt><strong>HDS_HIDDEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8e425-128">Указывает элемент управления "заголовок", который должен быть скрытым.</span><span class="sxs-lookup"><span data-stu-id="8e425-128">Indicates a header control that is intended to be hidden.</span></span> <span data-ttu-id="8e425-129">Этот стиль не скрывает элемент управления.</span><span class="sxs-lookup"><span data-stu-id="8e425-129">This style does not hide the control.</span></span> <span data-ttu-id="8e425-130">Вместо этого при отправке <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> сообщения в элемент управления заголовка с HDS_HIDDEN стилем элемент управления возвращает ноль в элементе <strong>CY</strong> структуры <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8e425-130">Instead, when you send the <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> message to a header control with the HDS_HIDDEN style, the control returns zero in the <strong>cy</strong> member of the <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> structure.</span></span> <span data-ttu-id="8e425-131">Затем можно скрыть элемент управления, установив его высоту равным нулю.</span><span class="sxs-lookup"><span data-stu-id="8e425-131">You would then hide the control by setting its height to zero.</span></span> <span data-ttu-id="8e425-132">Это может быть полезно, если вы хотите использовать элемент управления как контейнер информации, а не визуальный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="8e425-132">This can be useful when you want to use the control as an information container instead of a visual control.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_HORZ"></span><span id="hds_horz"></span><dl> <span data-ttu-id="8e425-133"><dt><strong>HDS_HORZ</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8e425-133"><dt><strong>HDS_HORZ</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8e425-134">Создает элемент управления "заголовок" с горизонтальной ориентацией.</span><span class="sxs-lookup"><span data-stu-id="8e425-134">Creates a header control with a horizontal orientation.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl> <span data-ttu-id="8e425-135"><dt><strong>HDS_HOTTRACK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8e425-135"><dt><strong>HDS_HOTTRACK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8e425-136">Включает функцию оперативного отслеживания.</span><span class="sxs-lookup"><span data-stu-id="8e425-136">Enables hot tracking.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl> <span data-ttu-id="8e425-137"><dt><strong>HDS_CHECKBOXES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8e425-137"><dt><strong>HDS_CHECKBOXES</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8e425-138"><a href="common-control-versions.md">Версия 6,00 и более поздние версии</a>.</span><span class="sxs-lookup"><span data-stu-id="8e425-138"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="8e425-139">Разрешает размещение флажков для элементов заголовка.</span><span class="sxs-lookup"><span data-stu-id="8e425-139">Allows the placing of checkboxes on header items.</span></span> <span data-ttu-id="8e425-140">Дополнительные сведения см. в разделе <strong>FMT</strong> элемента <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>хдитем</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e425-140">For more information, see the <strong>fmt</strong> member of <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl> <span data-ttu-id="8e425-141"><dt><strong>HDS_NOSIZING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8e425-141"><dt><strong>HDS_NOSIZING</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8e425-142"><a href="common-control-versions.md">Версия 6,00 и более поздние версии</a>.</span><span class="sxs-lookup"><span data-stu-id="8e425-142"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="8e425-143">Пользователь не может перетащить разделитель в элементе управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="8e425-143">The user cannot drag the divider on the header control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl> <span data-ttu-id="8e425-144"><dt><strong>HDS_OVERFLOW</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8e425-144"><dt><strong>HDS_OVERFLOW</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8e425-145"><a href="common-control-versions.md">Версия 6,00 и более поздние версии</a>.</span><span class="sxs-lookup"><span data-stu-id="8e425-145"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="8e425-146">Кнопка отображается, когда в прямоугольнике элемента управления заголовка могут отображаться не все элементы.</span><span class="sxs-lookup"><span data-stu-id="8e425-146">A button is displayed when not all items can be displayed within the header control's rectangle.</span></span> <span data-ttu-id="8e425-147">При нажатии этой кнопки отправляется уведомление <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> .</span><span class="sxs-lookup"><span data-stu-id="8e425-147">When clicked, this button sends an <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> notification.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="8e425-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e425-148">Remarks</span></span>

<span data-ttu-id="8e425-149">Чтобы извлечь и изменить стили после создания элемента управления, используйте функции [**жетвиндовлонг**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) и [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="8e425-149">To retrieve and change the styles after creating the control, use the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) and [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e425-150">Требования</span><span class="sxs-lookup"><span data-stu-id="8e425-150">Requirements</span></span>



| <span data-ttu-id="8e425-151">Требование</span><span class="sxs-lookup"><span data-stu-id="8e425-151">Requirement</span></span> | <span data-ttu-id="8e425-152">Значение</span><span class="sxs-lookup"><span data-stu-id="8e425-152">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e425-153">Header</span><span class="sxs-lookup"><span data-stu-id="8e425-153">Header</span></span><br/> | <dl> <span data-ttu-id="8e425-154"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e425-154"><dt>CommCtrl.h</dt></span></span> </dl> |



