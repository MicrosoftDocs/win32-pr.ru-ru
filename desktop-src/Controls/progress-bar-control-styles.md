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
ms.openlocfilehash: 1216171b116bffb962b3ebfe1a76497473cf2db2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465280"
---
# <a name="progress-bar-control-styles"></a>Стили элемента управления "индикатор выполнения"

Элементы управления "индикатор [выполнения](progress-bar-control.md) " поддерживают следующие стили элементов управления:




| Константа | Описание | 
|----------|-------------|
| <span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl><dt><strong>PBS_MARQUEE</strong></dt></dl> | <a href="common-control-versions.md">Версия 6,0</a> или более поздняя. Индикатор хода выполнения не увеличивается, а перемещается повторно вдоль длины полосы, указывая действие без указания того, какая часть хода выполнения завершена. <br /><blockquote>[!Note]<br />Comctl32.dll версии 6 не является распространяемой, но включена в Windows или более поздней версии. Чтобы использовать Comctl32.dll версии 6, укажите ее в манифесте. Дополнительные сведения о манифестах см. в разделе <a href="cookbook-overview.md">Включение визуальных стилей</a>.</blockquote><br /> | 
| <span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl><dt><strong>PBS_SMOOTH</strong></dt></dl> | <a href="common-control-versions.md">Версия 4,70</a> или более поздняя. Индикатор выполнения отображает состояние хода выполнения на гладкой полосе прокрутки, а не на сегментированной линейчатой диаграмме по умолчанию. <br /><blockquote>[!Note]<br />этот стиль поддерживается только в классической теме Windows. Все остальные темы переопределяют этот стиль.</blockquote><br /> | 
| <span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl><dt><strong>PBS_SMOOTHREVERSE</strong></dt></dl> | <a href="common-control-versions.md">версия 6,0</a> или более поздняя и <strong>Windows Vista.</strong> Определяет поведение анимации, которое должен использовать индикатор выполнения при перемещении назад (с более высоким значением до более низкого значения). Если этот параметр задан, произойдет «гладкий» переход, в противном случае элемент управления перейдет к меньшему значению.<br /> | 
| <span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl><dt><strong>PBS_VERTICAL</strong></dt></dl> | <a href="common-control-versions.md">Версия 4,70</a> или более поздняя. Индикатор выполнения отображает состояние хода выполнения по вертикали от нижнего к верхнему.<br /> | 




## <a name="remarks"></a>Комментарии

Стили индикаторов выполнения можно задать так же, как другие стандартные элементы управления с [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**жетвиндовлонг**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)или [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Коммктрл. h</dt> </dl> |



 

