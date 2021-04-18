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
# <a name="progress-bar-control-styles"></a>Стили элемента управления "индикатор выполнения"

Элементы управления "индикатор [выполнения](progress-bar-control.md) " поддерживают следующие стили элементов управления:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl> <dt><strong>PBS_MARQUEE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Версия 6,0</a> или более поздняя. Индикатор хода выполнения не увеличивается, а перемещается повторно вдоль длины полосы, указывая действие без указания того, какая часть хода выполнения завершена. <br/>
<blockquote>
[!Note]<br />
Версия Comctl32.dll 6 не является распространяемой, но включена в Windows или более поздней версии. Чтобы использовать Comctl32.dll версии 6, укажите ее в манифесте. Дополнительные сведения о манифестах см. в разделе <a href="cookbook-overview.md">Включение визуальных стилей</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl> <dt><strong>PBS_SMOOTH</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Версия 4,70</a> или более поздняя. Индикатор выполнения отображает состояние хода выполнения на гладкой полосе прокрутки, а не на сегментированной линейчатой диаграмме по умолчанию. <br/>
<blockquote>
[!Note]<br />
Этот стиль поддерживается только в классической теме Windows. Все остальные темы переопределяют этот стиль.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl> <dt><strong>PBS_SMOOTHREVERSE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Версия 6,0</a> или более поздняя и <strong>Windows Vista.</strong> Определяет поведение анимации, которое должен использовать индикатор выполнения при перемещении назад (с более высоким значением до более низкого значения). Если этот параметр задан, произойдет &quot; плавный &quot; переход, в противном случае элемент управления будет &quot; переходить &quot; к меньшему значению.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl> <dt><strong>PBS_VERTICAL</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Версия 4,70</a> или более поздняя. Индикатор выполнения отображает состояние хода выполнения по вертикали от нижнего к верхнему.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Комментарии

Стили индикаторов выполнения можно задать так же, как другие стандартные элементы управления с [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**жетвиндовлонг**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)или [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Коммктрл. h</dt> </dl> |



 

