---
title: Стили элемента управления "индикатор выполнения" (Коммктрл. h)
description: Элементы управления "индикатор выполнения" поддерживают следующие стили элементов управления
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55ec928fb1ee2715576f3131dde0f661a91fcf8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657281"
---
# <a name="progress-bar-control-styles"></a><span data-ttu-id="73b62-103">Стили элемента управления "индикатор выполнения"</span><span class="sxs-lookup"><span data-stu-id="73b62-103">Progress Bar Control Styles</span></span>

<span data-ttu-id="73b62-104">Элементы управления "индикатор [выполнения](progress-bar-control.md) " поддерживают следующие стили элементов управления:</span><span class="sxs-lookup"><span data-stu-id="73b62-104">The following control styles are supported by [Progress Bar](progress-bar-control.md) controls:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="73b62-105">Константа</span><span class="sxs-lookup"><span data-stu-id="73b62-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="73b62-106">Описание</span><span class="sxs-lookup"><span data-stu-id="73b62-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl> <span data-ttu-id="73b62-107"><dt><strong>PBS_MARQUEE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="73b62-107"><dt><strong>PBS_MARQUEE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="73b62-108"><a href="common-control-versions.md">Версия 6,0</a> или более поздняя.</span><span class="sxs-lookup"><span data-stu-id="73b62-108"><a href="common-control-versions.md">Version 6.0</a> or later.</span></span> <span data-ttu-id="73b62-109">Индикатор хода выполнения не увеличивается, а перемещается повторно вдоль длины полосы, указывая действие без указания того, какая часть хода выполнения завершена.</span><span class="sxs-lookup"><span data-stu-id="73b62-109">The progress indicator does not grow in size but instead moves repeatedly along the length of the bar, indicating activity without specifying what proportion of the progress is complete.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="73b62-110">Версия Comctl32.dll 6 не является распространяемой, но включена в Windows или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="73b62-110">Comctl32.dll version 6 is not redistributable but it is included in Windows or later.</span></span> <span data-ttu-id="73b62-111">Чтобы использовать Comctl32.dll версии 6, укажите ее в манифесте.</span><span class="sxs-lookup"><span data-stu-id="73b62-111">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="73b62-112">Дополнительные сведения о манифестах см. в разделе <a href="cookbook-overview.md">Включение визуальных стилей</a>.</span><span class="sxs-lookup"><span data-stu-id="73b62-112">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl> <span data-ttu-id="73b62-113"><dt><strong>PBS_SMOOTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="73b62-113"><dt><strong>PBS_SMOOTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="73b62-114"><a href="common-control-versions.md">Версия 4,70</a> или более поздняя.</span><span class="sxs-lookup"><span data-stu-id="73b62-114"><a href="common-control-versions.md">Version 4.70</a> or later.</span></span> <span data-ttu-id="73b62-115">Индикатор выполнения отображает состояние хода выполнения на гладкой полосе прокрутки, а не на сегментированной линейчатой диаграмме по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="73b62-115">The progress bar displays progress status in a smooth scrolling bar instead of the default segmented bar.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="73b62-116">Этот стиль поддерживается только в классической теме Windows.</span><span class="sxs-lookup"><span data-stu-id="73b62-116">This style is supported only in the Windows Classic theme.</span></span> <span data-ttu-id="73b62-117">Все остальные темы переопределяют этот стиль.</span><span class="sxs-lookup"><span data-stu-id="73b62-117">All other themes override this style.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl> <span data-ttu-id="73b62-118"><dt><strong>PBS_SMOOTHREVERSE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="73b62-118"><dt><strong>PBS_SMOOTHREVERSE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="73b62-119"><a href="common-control-versions.md">Версия 6,0</a> или более поздняя и <strong>Windows Vista.</strong></span><span class="sxs-lookup"><span data-stu-id="73b62-119"><a href="common-control-versions.md">Version 6.0</a> or later and <strong>Windows Vista.</strong></span></span> <span data-ttu-id="73b62-120">Определяет поведение анимации, которое должен использовать индикатор выполнения при перемещении назад (с более высоким значением до более низкого значения).</span><span class="sxs-lookup"><span data-stu-id="73b62-120">Determines the animation behavior that the progress bar should use when moving backward (from a higher value to a lower value).</span></span> <span data-ttu-id="73b62-121">Если этот параметр задан, произойдет &quot; плавный &quot; переход, в противном случае элемент управления будет &quot; переходить &quot; к меньшему значению.</span><span class="sxs-lookup"><span data-stu-id="73b62-121">If this is set, then a &quot;smooth&quot; transition will occur, otherwise the control will &quot;jump&quot; to the lower value.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl> <span data-ttu-id="73b62-122"><dt><strong>PBS_VERTICAL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="73b62-122"><dt><strong>PBS_VERTICAL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="73b62-123"><a href="common-control-versions.md">Версия 4,70</a> или более поздняя.</span><span class="sxs-lookup"><span data-stu-id="73b62-123"><a href="common-control-versions.md">Version 4.70</a> or later.</span></span> <span data-ttu-id="73b62-124">Индикатор выполнения отображает состояние хода выполнения по вертикали от нижнего к верхнему.</span><span class="sxs-lookup"><span data-stu-id="73b62-124">The progress bar displays progress status vertically, from bottom to top.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="73b62-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73b62-125">Remarks</span></span>

<span data-ttu-id="73b62-126">Стили индикаторов выполнения можно задать так же, как другие стандартные элементы управления с [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**жетвиндовлонг**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)или [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="73b62-126">You can set progress bar styles, in the same way as other common controls, with [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga), or [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="73b62-127">Требования</span><span class="sxs-lookup"><span data-stu-id="73b62-127">Requirements</span></span>



| <span data-ttu-id="73b62-128">Требование</span><span class="sxs-lookup"><span data-stu-id="73b62-128">Requirement</span></span> | <span data-ttu-id="73b62-129">Значение</span><span class="sxs-lookup"><span data-stu-id="73b62-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73b62-130">Header</span><span class="sxs-lookup"><span data-stu-id="73b62-130">Header</span></span><br/> | <dl> <span data-ttu-id="73b62-131"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="73b62-131"><dt>CommCtrl.h</dt></span></span> </dl> |



 

