---
title: Устаревшие функции шаблона элемента управления
description: Устаревшие функции шаблона элемента управления
ms.assetid: 06434b07-7592-4909-8c4e-064382bdbf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f646f9a9e3139d487785e344b9d3fc242b1a40e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410693"
---
# <a name="deprecated-control-pattern-functions"></a>Устаревшие функции шаблона элемента управления

> [!Note]  
> Функции шаблона элемента управления, описанные в этом разделе, являются устаревшими. Клиентские приложения должны использовать интерфейсы модели COM, описанные в следующих разделах:
>
> -   [Интерфейсы элементов модели автоматизации пользовательского интерфейса для клиентов](uiauto-entry-uiautoclientinterfaces.md)
> -   [Интерфейс условий свойств для клиентов](uiauto-client-propconditioninterfaces.md)
> -   [Интерфейсы шаблонов элементов управления для клиентов](uiauto-client-controlpatterninterfaces.md)
> -   [Интерфейсы обработки событий для клиентов](uiauto-client-eventhandlinginterfaces.md)
> -   [Интерфейсы фабрики прокси-серверов для клиентов](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a>Содержание раздела



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать COM-интерфейсы модели автоматизации пользовательского интерфейса Майкрософт.
</blockquote>
<br/> Закрепляет элемент модели автоматизации пользовательского интерфейса в запрошенном <em>dockPosition</em> в контейнере закрепления.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Скрывает все узлы-потомки, элементы управления или содержимое элемента модели автоматизации пользовательского интерфейса.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Развертывает элемент управления на экране, чтобы показать дополнительные сведения.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает узел для элемента в сетке.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Направляет запрос на активацию элемента управления и инициирует его единственное, однозначное действие.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Извлекает узел внутри содержащего узла на основе указанного значения свойства.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Выполняет действие Microsoft Active Accessibility по умолчанию для элемента.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Извлекает объект <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>IAccessible</strong></a> , соответствующий элементу модели автоматизации пользовательского интерфейса.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Выполняет выбор Microsoft Active Accessibility.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Задает свойство Microsoft Active Accessibility Value для узла.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Извлекает имя представления для элемента управления.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Задает другой макет элемента управления.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Задает значение элемента управления с числовым диапазоном.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Прокручивает область содержимого объекта контейнера, чтобы отобразить элемент модели автоматизации пользовательского интерфейса в видимой области (окне просмотра) контейнера.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Прокручивает видимую в данный момент область содержимого на заданный <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>скролламаунт</strong></a>, по горизонтали, по вертикали или в обе части.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Прокручивает контейнер до определенной позицией по горизонтали, вертикали или обоим.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Добавляет невыбранный элемент к выделенному элементу в элементе управления.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Удаляет элемент из выделения в контейнере выбора.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Выбирает элемент в контейнере выбора.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Заставляет поставщик автоматизации пользовательского интерфейса прекращать прослушивание ввода мыши или клавиатуры.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Заставляет поставщик автоматизации пользовательского интерфейса начать прослушивание ввода с клавиатуры или мыши.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает текстовый диапазон для всего документа.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Определяет, можно ли выбрать содержимое текстового контейнера и отменить его выбор.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает текущий диапазон выбранного текста из текстового контейнера, поддерживающего текстовый шаблон.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает массив раздельных текстовых диапазонов из текстового контейнера, где каждый диапазон начинается с первой частично видимой строки и оканчивается последней частично видимой строкой. Например, макет с несколькими столбцами, в котором столбцы частично прокручивается из видимой области окна просмотра, и содержимое перемещается от нижнего края одного столбца к другому.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает текстовый диапазон, охватываемый данным узлом.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Извлекает вырожденный (пустой) текстовый диапазон, ближайший к указанным экранным координатам.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Добавляет к существующей коллекции выделенного текста в текстовом контейнере, который поддерживает несколько несвязных выделений, выделяя дополнительный текст, соответствующий <em>начальным</em> и <em>конечным</em> конечным точкам текстового диапазона.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Копирует текстовый диапазон.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Сравнивает два текстовых диапазона.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает значение, указывающее, имеют ли два текстовых диапазона одинаковые конечные точки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Расширяет текстовый диапазон до более крупной или меньшей единицы, такой как символ, слово, строка или страница.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Выполняет поиск первого фрагмента текста, поддерживающего указанный текстовый атрибут, в указанном направлении.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает первый текстовый диапазон в указанном направлении, который содержит текст, который ищет клиент.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает значение текстового атрибута для текстового диапазона.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает минимальное число ограничивающих прямоугольников, которые могут заключаться в диапазон, по одному прямоугольнику на строку.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает все элементы модели автоматизации пользовательского интерфейса, содержащиеся в указанном текстовом диапазоне.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает узел для следующего наименьшего поставщика, охватывающего диапазон.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает текст в текстовом диапазоне до указанного числа символов.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Перемещает текстовый диапазон на указанное число единиц, запрошенное клиентом.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Перемещает конечную точку одного диапазона в конечную точку другого диапазона.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Перемещает конечную точку в диапазоне на указанное число единиц.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Удаляет выделенный текст, соответствующий вызывающему текстовому диапазону <em>TextPatternRangeEndpoint_Start</em> и <em>TextPatternRangeEndpoint_End</em> конечные точки из существующей коллекции выделенного текста в текстовом контейнере, поддерживающем несколько несвязных выделений.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Прокручивает текст таким образом, чтобы указанный диапазон был виден в окне просмотра.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Выбирает текстовый диапазон.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Переключает элемент управления в следующее поддерживаемое состояние.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Перемещает элемент в указанное место на экране.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Изменяет размер элемента на экране.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Поворачивает элемент на экране.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Задает текстовое значение элемента.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Делает виртуальный элемент полностью доступным как элемент модели автоматизации пользовательского интерфейса.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Закрывает открытое окно.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Задает визуальное состояние окна; Например, чтобы развернуть окно.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Блокирует вызывающий код в течение заданного промежутка времени или до того момента, как связанный процесс перейдет в состояние бездействия, в зависимости от того, что произойдет раньше.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Клиенты автоматизации пользовательского интерфейса](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





