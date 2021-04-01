---
description: Этот раздел содержит свойства для элемента управления InkPicture.
ms.assetid: d724c177-af57-4c99-94f2-c70904910b49
title: Свойства InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ae8149098b34a70af5e088814e2a5258b0fa0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817728"
---
# <a name="inkpicture-properties"></a>Свойства InkPicture

Этот раздел содержит свойства для элемента управления InkPicture.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Свойство</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>Ауторедрав, свойство</strong></a></td>
<td>Возвращает или задает значение, указывающее, перерисовывается ли элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> при недействительности окна (объект <a href="inkdisp-class.md"><strong>инкдисп</strong></a> , который в данный момент связан с элементом управления InkPicture, автоматически перерисовывается, когда окно, связанное с inkpicture, получает сообщение WM_PAINT).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></td>
<td>Возвращает или задает цвет фона для элемента управления <a href="inkpicture-control-reference.md">InkPicture</a> . Цвет фона по умолчанию — это цвет фона системного окна, который обычно является белым.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Коллектингинк, свойство</strong></a></td>
<td>Возвращает значение, указывающее, собирает ли элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> рукописный ввод (только время выполнения).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>Режиме CollectionMode</strong></a></td>
<td>Возвращает или задает режим сбора, определяющий, распознаются ли рукописный ввод, жесты или рукописный ввод и жесты при записи пользователем.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursor, свойство</strong></a></td>
<td>Возвращает коллекцию <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>иинккурсорс</strong></a> , доступную для использования в области рукописного ввода в элементе управления <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>кустомстрокес</strong></a></td>
<td>Возвращает коллекцию <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>иинккустомстрокес</strong></a> , которая должна быть сохранена с рукописным вводом (только во время разработки).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>DefaultDrawingAttributes, свойство</strong></a></td>
<td>Возвращает или задает коллекцию <a href="inkdrawingattributes-class.md"><strong>инкдравингаттрибутес</strong></a> по умолчанию, используемую при прорисовке и отображении рукописного ввода (только во время выполнения).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Десиредпаккетдескриптион, свойство</strong></a></td>
<td>Возвращает или задает описание пакета для элемента управления <a href="inkpicture-control-reference.md">InkPicture</a> (только время выполнения).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Динамикрендеринг, свойство</strong></a></td>
<td>Возвращает или задает значение, указывающее, будет ли элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> динамически отображать рукописный ввод при его сборе.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></td>
<td>Возвращает или задает значение, указывающее, находится ли элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> в режиме рукописного ввода, режиме удаления или режиме правки или выбора.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Активировано</strong></a></td>
<td>Возвращает или задает значение, определяющее, может ли элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> отвечать на создаваемые пользователем события.<br/>
<blockquote>
[!Note]<br />
Это свойство эквивалентно свойству <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>инкенаблед</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>ерасермоде</strong></a></td>
<td>Возвращает или задает значение, указывающее, удаляются ли рукописные данные по штрихам или по точкам.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>ерасервидс</strong></a></td>
<td>Возвращает или задает значение, указывающее ширину кончика пера ластика.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></td>
<td>Возвращает описатель окна, к которому привязан элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> . (только время выполнения)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Рукописный ввод</strong></a></td>
<td>Возвращает или задает объект <a href="inkdisp-class.md"><strong>инкдисп</strong></a> , связанный с элементом управления <a href="inkpicture-control-reference.md">InkPicture</a> (только время выполнения).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>инкенаблед</strong></a></td>
<td>Возвращает или задает значение, указывающее, собирает ли элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> входные данные пера (пакеты в сети Air, курсоры в пределах диапазона и т. д.).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Маргинкс, свойство</strong></a></td>
<td>Возвращает или задает поле оси x вокруг прямоугольника окна в экранных координатах.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>Свойство Margin</strong></a></td>
<td>Возвращает или задает поле оси y вокруг прямоугольника окна в экранных координатах.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Маусеикон, свойство</strong></a></td>
<td>Возвращает или задает текущий пользовательский значок мыши.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer, свойство</strong></a></td>
<td>Возвращает или задает значение, указывающее тип указателя мыши, который появляется при наведении указателя мыши на определенную часть элемента управления <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></td>
<td>Возвращает графический файл, отображаемый в элементе управления <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Свойство модуля подготовки отчетов</strong></a></td>
<td>Возвращает или задает объект <a href="inkrenderer-class.md"><strong>инкрендерер</strong></a> , используемый для рисования рукописного ввода в элементе управления <a href="inkpicture-control-reference.md">InkPicture</a> (только время выполнения).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Выбор</strong></a></td>
<td>Возвращает коллекцию <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">инкстрокес</a> , выбранную в данный момент в элементе управления <a href="inkpicture-control-reference.md">InkPicture</a> (только время выполнения).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></td>
<td>Возвращает или задает способ, которым элемент управления обрабатывает размещение и изменение размера изображения.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Суппорсигхконтрастинк, свойство</strong></a></td>
<td>Возвращает значение, указывающее, отображаются ли рукописные данные только в одном цвете, Color = COLOR_WINDOWTEXT (из вызова Жетсистемметрикс), когда система находится в режиме высокая контрастность.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>суппорсигхконтрастселектионуи</strong></a></td>
<td>Возвращает или задает значение, указывающее, отображаются ли все пользовательские интерфейсы выделения (ограничивающие прямоугольники выделения и маркеры выделения) с высокой контрастностью, когда система находится в режиме высокая контрастность.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Свойство планшета</strong></a></td>
<td>Возвращает объект <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>иинктаблет</strong></a> , который в настоящее время использует элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> для получения входных данных.<br/></td>
</tr>
</tbody>
</table>



 

