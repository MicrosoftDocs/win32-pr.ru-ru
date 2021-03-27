---
description: В этом разделе описываются флаги, используемые методами интерфейса Иактиведесктоп.
title: Флаги Иактиведесктоп (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d1a2f69-0730-4805-8b50-071332ff7070
api_name:
- AD_APPLY_ALL
- AD_APPLY_BUFFERED_REFRESH
- AD_APPLY_DYNAMICREFRESH
- AD_APPLY_FORCE
- AD_APPLY_HTMLGEN
- AD_APPLY_REFRESH
- AD_APPLY_SAVE
- COMP_ELEM_ALL
- COMP_ELEM_CHECKED
- COMP_ELEM_CURITEMSTATE
- COMP_ELEM_FRIENDLYNAME
- COMP_ELEM_NOSCROLL
- COMP_ELEM_ORIGINAL_CSI
- COMP_ELEM_POS_LEFT
- COMP_ELEM_POS_TOP
- COMP_ELEM_POS_ZINDEX
- COMP_ELEM_RESTORED_CSI
- COMP_ELEM_SIZE_HEIGHT
- COMP_ELEM_SIZE_WIDTH
- COMP_ELEM_SOURCE
- COMP_ELEM_TYPE
- COMP_TYPE_CFHTML
- COMP_TYPE_CONTROL
- COMP_TYPE_HTMLDOC
- COMP_TYPE_MAX
- COMP_TYPE_PICTURE
- COMP_TYPE_WEBSITE
- COMPONENT_TOP
- WPSTYLE_CENTER
- WPSTYLE_MAX
- WPSTYLE_STRETCH
- WPSTYLE_TILE
- WPSTYLE_SPAN
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dae164c696ae54963f802a6ddd5cb1f6862b2f14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987488"
---
# <a name="iactivedesktop-flags"></a><span data-ttu-id="ff27e-103">Флаги Иактиведесктоп</span><span class="sxs-lookup"><span data-stu-id="ff27e-103">IActiveDesktop Flags</span></span>

<span data-ttu-id="ff27e-104">В этом разделе описываются флаги, используемые методами интерфейса [**иактиведесктоп**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .</span><span class="sxs-lookup"><span data-stu-id="ff27e-104">This section describes the flags used by [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface methods.</span></span>

<dl> <dt>

<span data-ttu-id="ff27e-105"><span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD — \_ применить \_ все**</span><span class="sxs-lookup"><span data-stu-id="ff27e-105"><span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD\_APPLY\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-106">Статистическая функция \* \* \* \* AD Apply \* \* \* \*, \* \* \* \* \_ \_ AD \_ Apply хтмлжен \* \* \* \* \_ и \* \* \* \* AD \_ применить \_ обновление \* \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="ff27e-106">Aggregate of the \*\*\*\*AD\_APPLY\_SAVE\*\*\*\*, \*\*\*\*AD\_APPLY\_HTMLGEN\*\*\*\*, and \*\*\*\*AD\_APPLY\_REFRESH\*\*\*\* values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-107"><span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD — \_ применение \_ буферизованного \_ обновления**</span><span class="sxs-lookup"><span data-stu-id="ff27e-107"><span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD\_APPLY\_BUFFERED\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-108">Запускает таймер и объединяет все запросы на обновление, выполненные с этим флагом в течение этого интервала, в одно обновление.</span><span class="sxs-lookup"><span data-stu-id="ff27e-108">Starts a timer and aggregates all the refresh requests made with this flag during that time interval into a single refresh.</span></span> <span data-ttu-id="ff27e-109">Этот интервал задается через пять секунд.</span><span class="sxs-lookup"><span data-stu-id="ff27e-109">This interval is set at five seconds.</span></span> <span data-ttu-id="ff27e-110">В конце интервала, или, если обновление запрашивается в течение интервала без флага \* \* \* \* AD \_ Apply \_ rerefresh \* \* \* \*, выполняется \_ обновление и таймер останавливается.</span><span class="sxs-lookup"><span data-stu-id="ff27e-110">At the end of the interval, or if a refresh is requested during the interval without an \*\*\*\*AD\_APPLY\_BUFFERED\_REFRESH\*\*\*\* flag, the refresh is made and the timer is stopped.</span></span> <span data-ttu-id="ff27e-111">Этот флаг должен сочетаться с флагом \* \* \* \* AD \_ Apply Refresh \* \* \* \* \* \_ .</span><span class="sxs-lookup"><span data-stu-id="ff27e-111">This flag must be combined with the \*\*\*\*AD\_APPLY\_REFRESH\*\*\*\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-112"><span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD \_ Apply \_ динамикрефреш**</span><span class="sxs-lookup"><span data-stu-id="ff27e-112"><span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD\_APPLY\_DYNAMICREFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-113">[Версия 5,0](versions.md).</span><span class="sxs-lookup"><span data-stu-id="ff27e-113">[Version 5.0](versions.md).</span></span> <span data-ttu-id="ff27e-114">Используйте динамический HTML, чтобы обновить только те элементы, которые были изменены с момента последнего обновления, а не весь рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="ff27e-114">Use dynamic HTML to refresh only those items that have changed since the last refresh, not the entire desktop.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-115"><span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**\_применение \_ принудительной установки AD**</span><span class="sxs-lookup"><span data-stu-id="ff27e-115"><span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**AD\_APPLY\_FORCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-116">Принудительное изменение активного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ff27e-116">Force an Active Desktop change.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-117"><span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD \_ Apply \_ хтмлжен**</span><span class="sxs-lookup"><span data-stu-id="ff27e-117"><span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD\_APPLY\_HTMLGEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-118">Повторно создайте HTML-файл рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ff27e-118">Regenerate the desktop HTML file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-119"><span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**\_Обновление применения \_ AD**</span><span class="sxs-lookup"><span data-stu-id="ff27e-119"><span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**AD\_APPLY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-120">Обновите элемент рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ff27e-120">Refresh the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-121"><span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**\_сохранение применения \_ AD**</span><span class="sxs-lookup"><span data-stu-id="ff27e-121"><span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD\_APPLY\_SAVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-122">Сохраните элемент рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ff27e-122">Save the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-123"><span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP \_ ELEM \_ все**</span><span class="sxs-lookup"><span data-stu-id="ff27e-123"><span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP\_ELEM\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-124">Статистическая обработка \_ значений Comp ELEM \_ \* .</span><span class="sxs-lookup"><span data-stu-id="ff27e-124">Aggregate of the COMP\_ELEM\_\* values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-125"><span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**\_Проверка ELEM \_**</span><span class="sxs-lookup"><span data-stu-id="ff27e-125"><span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**COMP\_ELEM\_CHECKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-126">Элемент был проверен.</span><span class="sxs-lookup"><span data-stu-id="ff27e-126">The item has been checked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-127"><span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP \_ ELEM \_ куритемстате**</span><span class="sxs-lookup"><span data-stu-id="ff27e-127"><span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP\_ELEM\_CURITEMSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-128">Текущее состояние элемента рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ff27e-128">The current state of the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-129"><span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP \_ ELEM \_ FRIENDLYNAME**</span><span class="sxs-lookup"><span data-stu-id="ff27e-129"><span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP\_ELEM\_FRIENDLYNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-130">Понятное имя элемента.</span><span class="sxs-lookup"><span data-stu-id="ff27e-130">The friendly name of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-131"><span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**\_ELEMная \_ прокрутка Comp**</span><span class="sxs-lookup"><span data-stu-id="ff27e-131"><span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP\_ELEM\_NOSCROLL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-132">Элемент не поддается прокрутке.</span><span class="sxs-lookup"><span data-stu-id="ff27e-132">The item is not scrollable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-133"><span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**\_ELEM \_ \_ CSI**</span><span class="sxs-lookup"><span data-stu-id="ff27e-133"><span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP\_ELEM\_ORIGINAL\_CSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-134">Сведения о состоянии исходного элемента рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ff27e-134">The original desktop item state information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-135"><span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP \_ ELEM \_ POS \_ Left**</span><span class="sxs-lookup"><span data-stu-id="ff27e-135"><span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP\_ELEM\_POS\_LEFT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-136">Горизонтальное расположение элемента.</span><span class="sxs-lookup"><span data-stu-id="ff27e-136">The horizontal position of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-137"><span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP \_ ELEM \_ POS \_ сверху**</span><span class="sxs-lookup"><span data-stu-id="ff27e-137"><span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP\_ELEM\_POS\_TOP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-138">Вертикальная позиция элемента.</span><span class="sxs-lookup"><span data-stu-id="ff27e-138">The vertical position of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-139"><span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP \_ ELEM \_ POS \_ ZINDEX**</span><span class="sxs-lookup"><span data-stu-id="ff27e-139"><span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP\_ELEM\_POS\_ZINDEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-140">Z-индекс элемента.</span><span class="sxs-lookup"><span data-stu-id="ff27e-140">The z-index of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-141"><span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**\_ELEM, \_ восстановленный \_ CSI**</span><span class="sxs-lookup"><span data-stu-id="ff27e-141"><span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP\_ELEM\_RESTORED\_CSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-142">Сведения о состоянии восстановленного элемента рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ff27e-142">The restored desktop item state information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-143"><span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**\_Высота ELEM \_ размера \_**</span><span class="sxs-lookup"><span data-stu-id="ff27e-143"><span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**COMP\_ELEM\_SIZE\_HEIGHT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-144">Высота элемента.</span><span class="sxs-lookup"><span data-stu-id="ff27e-144">The height of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-145"><span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**\_Ширина ELEM \_ размера \_**</span><span class="sxs-lookup"><span data-stu-id="ff27e-145"><span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**COMP\_ELEM\_SIZE\_WIDTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-146">Ширина элемента.</span><span class="sxs-lookup"><span data-stu-id="ff27e-146">The width of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-147"><span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**\_источник ELEM \_**</span><span class="sxs-lookup"><span data-stu-id="ff27e-147"><span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**COMP\_ELEM\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-148">Исходный источник элемента.</span><span class="sxs-lookup"><span data-stu-id="ff27e-148">The original source of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-149"><span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**\_тип ELEMа Comp \_**</span><span class="sxs-lookup"><span data-stu-id="ff27e-149"><span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**COMP\_ELEM\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-150">Тип элемента.</span><span class="sxs-lookup"><span data-stu-id="ff27e-150">The item type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-151"><span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**\_тип Comp \_ кфхтмл**</span><span class="sxs-lookup"><span data-stu-id="ff27e-151"><span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**COMP\_TYPE\_CFHTML**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-152">Формат HTML.</span><span class="sxs-lookup"><span data-stu-id="ff27e-152">Compressed format HTML.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-153"><span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**\_ \_ элемент управления типа Comp**</span><span class="sxs-lookup"><span data-stu-id="ff27e-153"><span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**COMP\_TYPE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-154">Элемент является элементом управления.</span><span class="sxs-lookup"><span data-stu-id="ff27e-154">The item is a control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-155"><span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**\_тип Comp \_ хтмлдок**</span><span class="sxs-lookup"><span data-stu-id="ff27e-155"><span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**COMP\_TYPE\_HTMLDOC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-156">Элемент является HTML-документом.</span><span class="sxs-lookup"><span data-stu-id="ff27e-156">The item is an HTML document.</span></span> <span data-ttu-id="ff27e-157">Этот флаг следует использовать только при крайней необходимости.</span><span class="sxs-lookup"><span data-stu-id="ff27e-157">This flag should only be used when absolutely necessary.</span></span> <span data-ttu-id="ff27e-158">Это приводит к вставке HTML-документа в файл Desktop. htt, используемый для управления разметкой рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ff27e-158">It causes an HTML document to be inserted verbatim into the Desktop.htt file used to control layout of the desktop.</span></span> <span data-ttu-id="ff27e-159">В большинстве случаев для \_ \_ добавления элементов на Рабочий стол следует использовать флаг \* \* \* \* Comp Type Web \* \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="ff27e-159">For most cases, you should use the \*\*\*\*COMP\_TYPE\_WEBSITE\*\*\*\* flag to add items to the desktop.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-160"><span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**\_тип Comp \_ Max**</span><span class="sxs-lookup"><span data-stu-id="ff27e-160"><span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**COMP\_TYPE\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-161">Максимальное значение \_ \_ \* флага типа Comp.</span><span class="sxs-lookup"><span data-stu-id="ff27e-161">The maximum value of a COMP\_TYPE\_\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-162"><span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**\_изображение типа \_ comp**</span><span class="sxs-lookup"><span data-stu-id="ff27e-162"><span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**COMP\_TYPE\_PICTURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-163">Элемент является изображением.</span><span class="sxs-lookup"><span data-stu-id="ff27e-163">The item is a picture.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-164"><span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**\_ \_ веб-сайт типа Comp**</span><span class="sxs-lookup"><span data-stu-id="ff27e-164"><span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**COMP\_TYPE\_WEBSITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-165">Элемент является веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="ff27e-165">The item is a website.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-166"><span id="COMPONENT_TOP"></span><span id="component_top"></span>**в \_ Начало компонента**</span><span class="sxs-lookup"><span data-stu-id="ff27e-166"><span id="COMPONENT_TOP"></span><span id="component_top"></span>**COMPONENT\_TOP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-167">Значение z-порядка, означающее, что элемент находится в верхней части.</span><span class="sxs-lookup"><span data-stu-id="ff27e-167">A z-order value meaning the item is at the top.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-168"><span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**ВПСТИЛЕ \_ Center**</span><span class="sxs-lookup"><span data-stu-id="ff27e-168"><span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**WPSTYLE\_CENTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-169">Фоновый рисунок выравнивается по центру.</span><span class="sxs-lookup"><span data-stu-id="ff27e-169">The wallpaper is centered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-170"><span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**ВПСТИЛЕ \_ Max**</span><span class="sxs-lookup"><span data-stu-id="ff27e-170"><span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-171">Максимальное значение \_ \* флага впстиле.</span><span class="sxs-lookup"><span data-stu-id="ff27e-171">The maximum value of a WPSTYLE\_\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-172"><span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**ВПСТИЛЕ \_ Stretch**</span><span class="sxs-lookup"><span data-stu-id="ff27e-172"><span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE\_STRETCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-173">Фоновый рисунок растягивается, чтобы вместить весь экран.</span><span class="sxs-lookup"><span data-stu-id="ff27e-173">The wallpaper is stretched to fit the entire screen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-174"><span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**\_плитка впстиле**</span><span class="sxs-lookup"><span data-stu-id="ff27e-174"><span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**WPSTYLE\_TILE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-175">Фоновый рисунок является мозаичным.</span><span class="sxs-lookup"><span data-stu-id="ff27e-175">The wallpaper is tiled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff27e-176"><span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**\_диапазон впстиле**</span><span class="sxs-lookup"><span data-stu-id="ff27e-176"><span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**WPSTYLE\_SPAN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff27e-177">**Windows 8 и более поздние версии**: фоновый рисунок охватывает несколько мониторов.</span><span class="sxs-lookup"><span data-stu-id="ff27e-177">**Windows 8 and later**: The wallpaper spans multiple monitors.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff27e-178">Требования</span><span class="sxs-lookup"><span data-stu-id="ff27e-178">Requirements</span></span>



| <span data-ttu-id="ff27e-179">Требование</span><span class="sxs-lookup"><span data-stu-id="ff27e-179">Requirement</span></span> | <span data-ttu-id="ff27e-180">Значение</span><span class="sxs-lookup"><span data-stu-id="ff27e-180">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ff27e-181">Header</span><span class="sxs-lookup"><span data-stu-id="ff27e-181">Header</span></span><br/> | <dl> <span data-ttu-id="ff27e-182"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff27e-182"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
