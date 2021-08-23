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
ms.openlocfilehash: fe76446196c565796388a5bcd402e9fb3a071e1b14626d7ead949ab9eb0e3b61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435104"
---
# <a name="header-control-styles"></a>Стили элемента управления "заголовок"

Элементы управления "заголовок" имеют ряд стилей, описанных в этом разделе, которые определяют внешний вид и поведение элемента управления. Начальные стили задаются при создании элемента управления "заголовок".



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
<td style="text-align: left;"><span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl> <dt><strong>HDS_BUTTONS</strong></dt> </dl></td>
<td style="text-align: left;">Каждый элемент в элементе управления выглядит и ведет себя как кнопка "Отправить". Этот стиль удобен, если приложение выполняет задачу, когда пользователь щелкает элемент в элементе управления "заголовок". Например, приложение может сортировать сведения в столбцах по-разному в зависимости от того, какой элемент пользователь щелкает. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl> <dt><strong>HDS_DRAGDROP</strong></dt> </dl></td>
<td style="text-align: left;">Позволяет изменять порядок элементов заголовка с помощью перетаскивания. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl> <dt><strong>HDS_FILTERBAR</strong></dt> </dl></td>
<td style="text-align: left;">Включите строку фильтра как часть стандартного элемента управления "заголовок". Эта панель позволяет пользователям удобно применять фильтр к отображению. Вызовы <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> возвращают новый размер элемента управления и вызывают обновление представления списка. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_FLAT"></span><span id="hds_flat"></span><dl> <dt><strong>HDS_FLAT</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Версия 6,0 и более поздние версии</a>. Приводит к тому, что элемент управления "заголовок" отображается плоским, когда операционная система работает в классическом режиме. <br/>
<blockquote>
[!Note]<br />
Comctl32.dll версии 6 не является распространяемой, но включена в Windows. Чтобы использовать Comctl32.dll версии 6, укажите ее в манифесте. Дополнительные сведения о манифестах см. в разделе <a href="cookbook-overview.md">Включение визуальных стилей</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl> <dt><strong>HDS_FULLDRAG</strong></dt> </dl></td>
<td style="text-align: left;">Заставляет элемент управления "заголовок" отображать содержимое столбца, даже пока пользователь изменяет размер столбца. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl> <dt><strong>HDS_HIDDEN</strong></dt> </dl></td>
<td style="text-align: left;">Указывает элемент управления "заголовок", который должен быть скрытым. Этот стиль не скрывает элемент управления. Вместо этого при отправке <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> сообщения в элемент управления заголовка с HDS_HIDDEN стилем элемент управления возвращает ноль в элементе <strong>CY</strong> структуры <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> . Затем можно скрыть элемент управления, установив его высоту равным нулю. Это может быть полезно, если вы хотите использовать элемент управления как контейнер информации, а не визуальный элемент управления. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_HORZ"></span><span id="hds_horz"></span><dl> <dt><strong>HDS_HORZ</strong></dt> </dl></td>
<td style="text-align: left;">Создает элемент управления "заголовок" с горизонтальной ориентацией. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl> <dt><strong>HDS_HOTTRACK</strong></dt> </dl></td>
<td style="text-align: left;">Включает функцию оперативного отслеживания. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl> <dt><strong>HDS_CHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Версия 6,00 и более поздние версии</a>. Разрешает размещение флажков для элементов заголовка. Дополнительные сведения см. в разделе <strong>FMT</strong> элемента <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>хдитем</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl> <dt><strong>HDS_NOSIZING</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Версия 6,00 и более поздние версии</a>. Пользователь не может перетащить разделитель в элементе управления "заголовок".<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl> <dt><strong>HDS_OVERFLOW</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Версия 6,00 и более поздние версии</a>. Кнопка отображается, когда в прямоугольнике элемента управления заголовка могут отображаться не все элементы. При нажатии этой кнопки отправляется уведомление <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> .<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Remarks

Чтобы извлечь и изменить стили после создания элемента управления, используйте функции [**жетвиндовлонг**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) и [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Коммктрл. h</dt> </dl> |



