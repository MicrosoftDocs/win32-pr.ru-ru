---
title: Константы СЕЛФЛАГ (Олеакк. h)
description: В этом разделе описываются константные значения, используемые для указания способа выбора доступного объекта или фокуса.
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb49daffd2bb20e705d17aa51c3bff3d9622a6de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717911"
---
# <a name="selflag-constants"></a>Константы СЕЛФЛАГ

В этом разделе описываются константные значения, используемые для указания способа выбора доступного объекта или фокуса. Константы определяются в олеакк. h и используются с методом [**IAccessible:: аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) .

Следующие сочетания не допускаются:

-   СЕЛФЛАГ \_ аддселектион \| селфлаг \_ ремовеселектион
-   СЕЛФЛАГ \_ аддселектион \| селфлаг \_ такеселектион
-   СЕЛФЛАГ \_ ремовеселектион \| селфлаг \_ такеселектион
-   СЕЛФЛАГ \_ екстендселектион \| селфлаг \_ такеселектион

**Примечание для клиентов:** Microsoft Active Accessibility не поддерживает выбор текста, содержащегося в элементах управления Edit и Rich Edit, поскольку текст представлен в виде строки в [свойстве Value](value-property.md)объекта.

Дополнительные сведения о выполнении сложных операций выбора см. в разделе [Выбор дочерних объектов](selecting-child-objects.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа/значение</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl> <dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </dl></td>
<td style="text-align: left;">Не выполняет никаких действий. Microsoft Active Accessibility не изменяет выделенный фрагмент или фокус.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl> <dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </dl></td>
<td style="text-align: left;">Устанавливает фокус на объект и делает его привязкой к выделенной области. Используется сама по себе, этот флаг не изменяет выбор. Этот результат аналогичен перемещению фокуса вручную с помощью клавиши со стрелкой, удерживая нажатой клавишу CTRL в проводнике Windows или в любом списке с множественным выбором. <br/> С объектами, имеющими <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS объединяется со следующими значениями:<br/>
<ul>
<li>SELFLAG_TAKESELECTION</li>
<li>SELFLAG_EXTENDSELECTION</li>
<li>SELFLAG_ADDSELECTION</li>
<li>SELFLAG_REMOVESELECTION</li>
<li>SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</li>
<li>SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</li>
</ul>
При вызове метода <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible:: аккселект</strong></a> с флагом SELFLAG_TAKEFOCUS для объекта, имеющего <strong>HWND</strong>, флаг вступит в силу только в том случае, если родительский объект уже имеет фокус.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl> <dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </dl></td>
<td style="text-align: left;">Выбирает объект и удаляет выделение из всех других объектов в контейнере. <br/> Если он не сочетается с SELFLAG_TAKEFOCUS, этот флаг не изменяет фокус или привязку выделения. SELFLAG_TAKESELECTION | Сочетание SELFLAG_TAKEFOCUS эквивалентно щелчку одного элемента в проводнике Windows.<br/> Этот флаг не должен сочетаться со следующими флагами:<br/>
<ul>
<li>SELFLAG_ADDSELECTION</li>
<li>SELFLAG_REMOVESELECTION</li>
<li>SELFLAG_EXTENDSELECTION</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl> <dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </dl></td>
<td style="text-align: left;">Изменяет выделенный фрагмент таким образом, что все объекты между точкой привязки и этим объектом принимают состояние выбора объекта привязки. Если объект точки привязки не выделен, объекты удаляются из выделения. Если выбран объект привязки, выбор расширяется, чтобы включить этот объект и все объекты между ними. Задайте состояние выбора, объединив этот флаг с SELFLAG_ADDSELECTION или SELFLAG_REMOVESELECTION. <br/> Если он не сочетается с SELFLAG_TAKEFOCUS, этот флаг не изменяет фокус или привязку выделения. SELFLAG_EXTENDSELECTION | Сочетание SELFLAG_TAKEFOCUS эквивалентно добавлению элемента к выделению вручную путем нажатия клавиши SHIFT и щелчка невыделенного объекта в проводнике Windows.<br/> Этот флаг не сочетается с SELFLAG_TAKESELECTION.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl> <dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </dl></td>
<td style="text-align: left;">Добавляет объект к текущему выделению; возможный результат — несмежный выбор. <br/> Если он не сочетается с SELFLAG_TAKEFOCUS, этот флаг не изменяет фокус или привязку выделения. SELFLAG_ADDSELECTION | Сочетание SELFLAG_TAKEFOCUS эквивалентно добавлению элемента в выделение вручную путем нажатия клавиши CTRL и щелчка невыделенного объекта в проводнике Windows.<br/> Этот флаг не сочетается с SELFLAG_REMOVESELECTION или SELFLAG_TAKESELECTION.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl> <dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </dl></td>
<td style="text-align: left;">Удаляет объект из текущего выбора. возможный результат — несмежный выбор. <br/> Если он не сочетается с SELFLAG_TAKEFOCUS, этот флаг не изменяет фокус или привязку выделения. SELFLAG_REMOVESELECTION | Сочетание SELFLAG_TAKEFOCUS эквивалентно удалению элемента из выделения вручную путем нажатия клавиши CTRL при щелчке выбранного объекта в проводнике Windows.<br/> Этот флаг не сочетается с SELFLAG_ADDSELECTION или SELFLAG_TAKESELECTION.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Олеакк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IAccessible:: Аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[Выбор дочерних объектов](selecting-child-objects.md)
</dt> </dl>

 

 





