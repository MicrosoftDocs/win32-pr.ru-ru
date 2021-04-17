---
title: Расширенные стили Tree-View управления (Коммктрл. h)
description: В этом разделе перечислены расширенные стили, используемые при создании элементов управления "дерево-представление". Значение расширенных стилей является побитовым сочетанием этих стилей.
ms.assetid: b45e7b7c-2c7b-49fa-8679-57c478b2f796
topic_type:
- apiref
api_name:
- TVS_EX_AUTOHSCROLL
- TVS_EX_DIMMEDCHECKBOXES
- TVS_EX_DOUBLEBUFFER
- TVS_EX_DRAWIMAGEASYNC
- TVS_EX_EXCLUSIONCHECKBOXES
- TVS_EX_FADEINOUTEXPANDOS
- TVS_EX_MULTISELECT
- TVS_EX_NOINDENTSTATE
- TVS_EX_NOSINGLECOLLAPSE
- TVS_EX_PARTIALCHECKBOXES
- TVS_EX_RICHTOOLTIP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec20467e6a6bdeb98d57661d30292b55d4532f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657137"
---
# <a name="tree-view-control-extended-styles"></a>Расширенные стили Tree-View управления

В этом разделе перечислены расширенные стили, используемые при создании элементов управления "дерево-представление". Значение расширенных стилей является побитовым сочетанием этих стилей.



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
<td style="text-align: left;"><span id="TVS_EX_AUTOHSCROLL"></span><span id="tvs_ex_autohscroll"></span><dl> <dt><strong>TVS_EX_AUTOHSCROLL</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Удаление горизонтальной полосы прокрутки и автоматическая прокрутка в зависимости от положения мыши.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_DIMMEDCHECKBOXES"></span><span id="tvs_ex_dimmedcheckboxes"></span><dl> <dt><strong>TVS_EX_DIMMEDCHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Включать недоступное состояние флажка, если элемент управления имеет стиль <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_DOUBLEBUFFER"></span><span id="tvs_ex_doublebuffer"></span><dl> <dt><strong>TVS_EX_DOUBLEBUFFER</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Задает способ стирания или заливки фона.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_DRAWIMAGEASYNC"></span><span id="tvs_ex_drawimageasync"></span><dl> <dt><strong>TVS_EX_DRAWIMAGEASYNC</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Извлекает сведения о сетке календаря.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_EXCLUSIONCHECKBOXES"></span><span id="tvs_ex_exclusioncheckboxes"></span><dl> <dt><strong>TVS_EX_EXCLUSIONCHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Включить состояние флажка исключения, если элемент управления имеет стиль <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_FADEINOUTEXPANDOS"></span><span id="tvs_ex_fadeinoutexpandos"></span><dl> <dt><strong>TVS_EX_FADEINOUTEXPANDOS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Выцветание кнопки "expando" в или покидает, когда указатель мыши перемещается или находится в состоянии наведения на элемент управления.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_MULTISELECT"></span><span id="tvs_ex_multiselect"></span><dl> <dt><strong>TVS_EX_MULTISELECT</strong></dt> </dl></td>
<td style="text-align: left;">Не поддерживается. Не используйте.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_NOINDENTSTATE"></span><span id="tvs_ex_noindentstate"></span><dl> <dt><strong>TVS_EX_NOINDENTSTATE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Не следует понизить уровень представления в виде дерева для кнопок expando.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_NOSINGLECOLLAPSE"></span><span id="tvs_ex_nosinglecollapse"></span><dl> <dt><strong>TVS_EX_NOSINGLECOLLAPSE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. <strong>Предназначен для внутреннего использования; не рекомендуется для использования в приложениях.</strong> Не сверните ранее выбранный элемент древовидного представления, если он не имеет того же родителя, что и новый выбор. Этот стиль следует использовать с <a href="tree-view-control-window-styles.md"><strong>TVS_SINGLEEXPAND</strong></a> стилем. <br/>
<blockquote>
[!Note]<br />
Этот стиль может не поддерживаться в будущих версиях Comctl32.dll. Кроме того, этот стиль не определен в коммктрл. h. Добавьте следующее определение в исходные файлы приложения для использования этого стиля: <code>#define TVS_EX_NOSINGLECOLLAPSE 0x0001</code>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_PARTIALCHECKBOXES"></span><span id="tvs_ex_partialcheckboxes"></span><dl> <dt><strong>TVS_EX_PARTIALCHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Включить частичное состояние флажка, если элемент управления имеет стиль <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_RICHTOOLTIP"></span><span id="tvs_ex_richtooltip"></span><dl> <dt><strong>TVS_EX_RICHTOOLTIP</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Разрешить широкие подсказки в представлении в виде дерева (пользовательский вывод с помощью значка и текста).<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





