---
title: Расширенные стили панелей инструментов (Коммктрл. h)
description: В этом разделе перечислены расширенные стили, поддерживаемые элементами управления ToolBar.
ms.assetid: da31dbbf-8d0a-4711-a1af-382c62e653cd
topic_type:
- apiref
api_name:
- TBSTYLE_EX_DRAWDDARROWS
- TBSTYLE_EX_HIDECLIPPEDBUTTONS
- TBSTYLE_EX_DOUBLEBUFFER
- TBSTYLE_EX_MIXEDBUTTONS
- TBSTYLE_EX_MULTICOLUMN
- TBSTYLE_EX_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056e48753485364017f04f7b84e609b19473bf5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648120"
---
# <a name="toolbar-extended-styles"></a>Расширенные стили панели инструментов

В этом разделе перечислены расширенные стили, поддерживаемые элементами управления ToolBar.



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
<td style="text-align: left;"><span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl> <dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Версия 4,71</a>. Этот стиль позволяет кнопкам иметь отдельную стрелку раскрывающегося списка. Кнопки, имеющие стиль <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> , будут отображаться с помощью раскрывающегося списка в отдельном разделе справа от кнопки. Если щелкнуть стрелку, будет Депресс только часть стрелки кнопки, а элемент управления панели инструментов отправит <a href="tbn-dropdown.md">TBN_DROPDOWN</a> код уведомления, чтобы запрос отображался в раскрывающемся меню. Если нажата основная часть кнопки, элемент управления ToolBar отправляет WM_COMMAND сообщение с ИДЕНТИФИКАТОРом кнопки. Приложение обычно отвечает, запустив первую команду в меню.<br/> Существует множество ситуаций, в которых может потребоваться только часть кнопок на панели инструментов с разделенными стрелками. Для этого задайте расширенный стиль TBSTYLE_EX_DRAWDDARROWS. Присвойте этим кнопкам, которые не будут разделены стрелками, <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> стиле. Кнопки с этим стилем будут отображаться рядом с изображением. Однако стрелка не будет разделяться и при нажатии любой части кнопки элемент управления ToolBar отправит <a href="tbn-dropdown.md">TBN_DROPDOWN</a> код уведомления. Чтобы избежать проблем с перерисовкой, этот стиль следует задать до того, как элемент управления ToolBar станет видимым.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl> <dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Версия 5,81</a>. Этот стиль скрывает частично обрезанные кнопки. Наиболее часто этот стиль используется для панелей инструментов, которые являются частью элемента управления главной панели. Если смежная полоса охватывает часть кнопки, кнопка не будет отображаться. Однако если полоса главной панели имеет стиль <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> , то кнопка будет отображаться в раскрывающемся меню шеврона. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl> <dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Версия 6</a>. Этот стиль требует двойной буферизации панели инструментов. Двойная буферизация — это механизм, который обнаруживает, что панель инструментов изменилась. <br/>
<blockquote>
[!Note]<br />
Версия Comctl32.dll 6 не является распространяемой, но включена в Windows или более поздней версии. Чтобы использовать Comctl32.dll версии 6, укажите ее в манифесте. Дополнительные сведения о манифестах см. в разделе <a href="cookbook-overview.md">Включение визуальных стилей</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl> <dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Версия 5,81</a>. Этот стиль позволяет задать текст для всех кнопок, но отображать его только для этих кнопок с помощью стиля кнопки <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> . Необходимо также задать стиль <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> . Как правило, если кнопка не отображает текст, приложение должно выполнить обработку <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> или <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> , чтобы отобразить подсказку. При использовании расширенного стиля TBSTYLE_EX_MIXEDBUTTONS текст, который задается, но не отображается на кнопке, будет автоматически использоваться в качестве текста подсказки для кнопки. Приложению требуется только обработку TBN_GETINFOTIP или или TTN_GETDISPINFO, если требуется больше гибкости при указании текста подсказки. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl> <dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Версия 5,82</a>. <strong>Предназначен для внутреннего использования; не рекомендуется для использования в приложениях.</strong> Этот стиль дает панели инструментов вертикальную ориентацию и упорядочивает кнопки на панели инструментов в столбцы. Кнопки передаются вниз по вертикали, пока кнопка не превысить ограничивающую высоту панели инструментов (см. <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>), а затем создается новый столбец. Панель инструментов направляет кнопки таким образом, пока не будут размещены все кнопки. Чтобы использовать этот стиль, необходимо также задать стиль TBSTYLE_EX_VERTICAL. <br/>
<blockquote>
[!Note]<br />
Этот стиль может не поддерживаться в будущих версиях Comctl32.dll. Кроме того, этот стиль не определен в коммктрл. h. Добавьте следующее определение в исходные файлы приложения для использования этого стиля: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl> <dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Версия 5,82</a>. <strong>Предназначен для внутреннего использования; не рекомендуется для использования в приложениях.</strong> Этот стиль дает панели инструментов вертикальную ориентацию. Кнопки панели инструментов передаются сверху вниз, а не горизонтально. <br/>
<blockquote>
[!Note]<br />
Этот стиль может не поддерживаться в будущих версиях Comctl32.dll. Кроме того, этот стиль не определен в коммктрл. h. Добавьте следующее определение в исходные файлы приложения для использования этого стиля: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Комментарии

Чтобы задать расширенный стиль, отправьте на панель инструментов сообщение [**\_ Сетекстендедстиле (ТБ**](tb-setextendedstyle.md) ). Чтобы определить, какие расширенные стили в настоящее время заданы, отправьте сообщение [**\_ Жетекстендедстиле в ТБ**](tb-getextendedstyle.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





